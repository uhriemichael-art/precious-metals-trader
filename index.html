// ===== Precious Metals Data =====
const metalsData = {
    gold: {
        name: 'Gold',
        symbol: 'AU',
        color: '#ffd700',
        price: 2145.50,
        highToday: 2155.00,
        lowToday: 2135.25,
        change: 15.50,
        history: [2130, 2135, 2140, 2138, 2142, 2147, 2145]
    },
    silver: {
        name: 'Silver',
        symbol: 'AG',
        color: '#c0c0c0',
        price: 28.75,
        highToday: 29.10,
        lowToday: 28.50,
        change: 0.85,
        history: [28.15, 28.30, 28.50, 28.40, 28.60, 28.70, 28.75]
    },
    platinum: {
        name: 'Platinum',
        symbol: 'PT',
        color: '#e8e8e8',
        price: 975.25,
        highToday: 985.00,
        lowToday: 970.50,
        change: -5.75,
        history: [980, 975, 972, 975, 976, 974, 975]
    },
    palladium: {
        name: 'Palladium',
        symbol: 'PD',
        color: '#71797e',
        price: 850.00,
        highToday: 860.00,
        lowToday: 845.00,
        change: 12.50,
        history: [837.5, 840, 842.5, 845, 847.5, 850, 850]
    }
};

let charts = {};
let updateInterval;

// ===== Initialize Page =====
document.addEventListener('DOMContentLoaded', function() {
    displayPrices();
    initializeCharts();
    setupEventListeners();
    startAutoUpdate();
    updateLastUpdatedTime();
});

// ===== Display Prices =====
function displayPrices() {
    const pricesGrid = document.getElementById('prices-grid');
    pricesGrid.innerHTML = '';

    for (let metal in metalsData) {
        const data = metalsData[metal];
        const metalClass = metal.charAt(0).toUpperCase() + metal.slice(1).toLowerCase();
        const changeClass = data.change >= 0 ? 'positive' : 'negative';
        const changeIcon = data.change >= 0 ? 'fa-arrow-up' : 'fa-arrow-down';
        const changeSymbol = data.change >= 0 ? '+' : '';

        const priceCard = document.createElement('div');
        priceCard.className = `price-card ${metal}`;
        priceCard.innerHTML = `
            <div class="metal-name">
                <i class="fas fa-coins" style="color: ${data.color}"></i>
                ${data.name}
                <span class="metal-symbol">(${data.symbol})</span>
            </div>
            <div class="price-display">
                <span class="currency">$</span>${data.price.toFixed(2)}
                <span style="font-size: 0.6em; opacity: 0.7;"> / oz</span>
            </div>
            <div class="price-info">
                <span>
                    <strong>High:</strong> $${data.highToday.toFixed(2)}
                </span>
                <span>
                    <strong>Low:</strong> $${data.lowToday.toFixed(2)}
                </span>
            </div>
            <div class="price-change ${changeClass}">
                <i class="fas ${changeIcon}"></i>
                ${changeSymbol}${data.change.toFixed(2)} (${changeSymbol}${((data.change / (data.price - data.change)) * 100).toFixed(2)}%)
            </div>
        `;
        pricesGrid.appendChild(priceCard);
    }
}

// ===== Initialize Charts =====
function initializeCharts() {
    const chartConfig = {
        gold: {
            canvasId: 'goldChart',
            label: 'Gold Price (USD/oz)',
            borderColor: '#ffd700',
            backgroundColor: 'rgba(255, 215, 0, 0.1)'
        },
        silver: {
            canvasId: 'silverChart',
            label: 'Silver Price (USD/oz)',
            borderColor: '#c0c0c0',
            backgroundColor: 'rgba(192, 192, 192, 0.1)'
        },
        platinum: {
            canvasId: 'platinumChart',
            label: 'Platinum Price (USD/oz)',
            borderColor: '#e8e8e8',
            backgroundColor: 'rgba(232, 232, 232, 0.1)'
        },
        palladium: {
            canvasId: 'palladiumChart',
            label: 'Palladium Price (USD/oz)',
            borderColor: '#71797e',
            backgroundColor: 'rgba(113, 121, 126, 0.1)'
        }
    };

    for (let metal in chartConfig) {
        const config = chartConfig[metal];
        const ctx = document.getElementById(config.canvasId).getContext('2d');
        
        charts[metal] = new Chart(ctx, {
            type: 'line',
            data: {
                labels: ['Day 1', 'Day 2', 'Day 3', 'Day 4', 'Day 5', 'Day 6', 'Day 7'],
                datasets: [{
                    label: config.label,
                    data: metalsData[metal].history,
                    borderColor: config.borderColor,
                    backgroundColor: config.backgroundColor,
                    borderWidth: 3,
                    fill: true,
                    tension: 0.4,
                    pointRadius: 5,
                    pointBackgroundColor: config.borderColor,
                    pointBorderColor: '#fff',
                    pointBorderWidth: 2,
                    pointHoverRadius: 7
                }]
            },
            options: {
                responsive: true,
                maintainAspectRatio: true,
                plugins: {
                    legend: {
                        display: true,
                        labels: {
                            font: { size: 12 },
                            color: '#333'
                        }
                    }
                },
                scales: {
                    y: {
                        beginAtZero: false,
                        grid: {
                            color: 'rgba(0, 0, 0, 0.05)'
                        },
                        ticks: {
                            color: '#999'
                        }
                    },
                    x: {
                        grid: {
                            display: false
                        },
                        ticks: {
                            color: '#999'
                        }
                    }
                }
            }
        });
    }
}

// ===== Update Prices =====
function updatePrices() {
    // Simulate price updates with small random changes
    for (let metal in metalsData) {
        const data = metalsData[metal];
        const randomChange = (Math.random() - 0.5) * 10;
        const oldPrice = data.price;
        
        data.price += randomChange;
        data.change = data.price - oldPrice;
        
        // Update history
        data.history.shift();
        data.history.push(data.price);
        
        // Update high/low
        data.highToday = Math.max(data.highToday, data.price);
        data.lowToday = Math.min(data.lowToday, data.price);
    }

    displayPrices();
    updateCharts();
    updateLastUpdatedTime();
    showNotification('Prices updated successfully!');
}

// ===== Update Charts =====
function updateCharts() {
    for (let metal in charts) {
        charts[metal].data.datasets[0].data = metalsData[metal].history;
        charts[metal].update();
    }
}

// ===== Setup Event Listeners =====
function setupEventListeners() {
    // Hamburger menu toggle
    const hamburger = document.getElementById('hamburger');
    const navbarMenu = document.getElementById('navbar-menu');

    if (hamburger) {
        hamburger.addEventListener('click', function() {
            navbarMenu.classList.toggle('active');
        });
    }

    // Close menu when clicking on a link
    if (navbarMenu) {
        navbarMenu.querySelectorAll('a').forEach(link => {
            link.addEventListener('click', function() {
                navbarMenu.classList.remove('active');
            });
        });
    }

    // Contact form submission
    const contactForm = document.getElementById('contact-form');
    if (contactForm) {
        contactForm.addEventListener('submit', function(e) {
            e.preventDefault();
            showNotification('Thank you! We will get back to you soon.');
            this.reset();
        });
    }
}

// ===== Auto Update Prices =====
function startAutoUpdate() {
    updateInterval = setInterval(function() {
        updatePrices();
    }, 60000); // Update every minute
}

// ===== Update Last Updated Time =====
function updateLastUpdatedTime() {
    const now = new Date();
    const timeString = now.toLocaleTimeString();
    const lastUpdatedElement = document.getElementById('last-updated-time');
    if (lastUpdatedElement) {
        lastUpdatedElement.textContent = timeString;
    }
}

// ===== Show Notification =====
function showNotification(message) {
    const notification = document.createElement('div');
    notification.style.cssText = `
        position: fixed;
        top: 100px;
        right: 20px;
        background: linear-gradient(135deg, #ffd700, #ffed4e);
        color: #333;
        padding: 15px 25px;
        border-radius: 5px;
        box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
        z-index: 9999;
        animation: slideInRight 0.5s ease;
        font-weight: 600;
        max-width: 300px;
    `;
    notification.textContent = message;

    document.body.appendChild(notification);

    setTimeout(function() {
        notification.style.animation = 'slideOutRight 0.5s ease';
        setTimeout(function() {
            notification.remove();
        }, 500);
    }, 3000);
}

// ===== Add Notification Animations =====
const style = document.createElement('style');
style.innerHTML = `
    @keyframes slideInRight {
        from {
            opacity: 0;
            transform: translateX(100px);
        }
        to {
            opacity: 1;
            transform: translateX(0);
        }
    }
    
    @keyframes slideOutRight {
        from {
            opacity: 1;
            transform: translateX(0);
        }
        to {
            opacity: 0;
            transform: translateX(100px);
        }
    }
`;
document.head.appendChild(style);
