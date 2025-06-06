function updateTotal(price) {
    document.getElementById('total-price').textContent = `$${price.toFixed(2)} USD`;
    
    // Update selected styling for bogo options
    const options = document.querySelectorAll('.bogo-option');
    options.forEach(option => {
        option.classList.remove('selected');
        if (option.querySelector('input').checked) {
            option.classList.add('selected');
        }
    });
}

// Initialize total on page load
updateTotal(18);
