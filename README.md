/* New Things Every Day — Day 112 */
/* Analyzes inventory data and prints a stock summary */

function dailyLog112() {
    const inventory = [
        { item: "Keyboard", quantity: 12 },
        { item: "Mouse", quantity: 8 },
        { item: "Monitor", quantity: 5 },
        { item: "USB Cable", quantity: 20 }
    ];

    const totalItems = inventory.reduce(
        (sum, product) => sum + product.quantity,
        0
    );

    const lowStock = inventory.filter(product => product.quantity < 10);

    const report = {
        day: 112,
        timestamp: new Date().toISOString(),
        totalProducts: inventory.length,
        totalItems,
        lowStock: lowStock.map(product => product.item)
    };

    console.log("Day 112 Inventory Report:", report);
}

dailyLog112();
