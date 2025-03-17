// Wait for the DOM to be fully loaded
document.addEventListener('DOMContentLoaded', function() {
    // Smooth scrolling for navigation links
    document.querySelectorAll('a[href^="#"]').forEach(anchor => {
        anchor.addEventListener('click', function (e) {
            e.preventDefault();
            
            const targetId = this.getAttribute('href');
            const targetElement = document.querySelector(targetId);
            
            if (targetElement) {
                window.scrollTo({
                    top: targetElement.offsetTop - 56, // Adjust for navbar height
                    behavior: 'smooth'
                });
            }
        });
    });
    
    // Form submission handling
    const contactForm = document.getElementById('contact-form');
    if (contactForm) {
        contactForm.addEventListener('submit', function(e) {
            e.preventDefault();
            
            // Get form values
            const name = document.getElementById('name').value;
            const email = document.getElementById('email').value;
            const message = document.getElementById('message').value;
            
            // In a real application, you would send this data to a server
            // For demonstration, we'll just log it and show a success message
            console.log('Form submitted:', { name, email, message });
            
            // Show success message
            alert('Thank you for your message! I will get back to you soon.');
            
            // Reset form
            contactForm.reset();
        });
    }
    
    // Add animation to skills section
    const animateSkills = () => {
        const skillsSection = document.getElementById('skills');
        const progressBars = document.querySelectorAll('.progress-bar');
        
        // Check if skills section is visible
        if (isElementInViewport(skillsSection)) {
            progressBars.forEach(bar => {
                const value = bar.getAttribute('aria-valuenow');
                bar.style.width = value + '%';
                bar.classList.add('animated');
            });
        }
    };
    
    // Check if element is in viewport
    function isElementInViewport(el) {
        const rect = el.getBoundingClientRect();
        return (
            rect.top <= (window.innerHeight || document.documentElement.clientHeight) &&
            rect.top >= 0
        );
    }
    
    // Run animation on scroll
    window.addEventListener('scroll', animateSkills);
    
    // Run animation on page load
    animateSkills();
});
