; (function ($) {

	$(document).on('click', '.header-area .navbar-wrapper ul li', function () {
		$('.header-area .navbar-wrapper ul li').removeClass('active');
		$(this).toggleClass('active');
	})
	$(document).on('click', '.header-area .navbar-wrapper ul > li.active', function () {
		$(this).removeClass('active');
	})

	$(document).on('click', '.header-area .menu-bar', function () {
		$('.header-area .navbar-wrapper').addClass('active');
	})
	$(document).on('click', '.header-area .navbar-wrapper .close-menu-bar', function () {
		$('.header-area .navbar-wrapper').removeClass('active');
	})

	$(document).on("mouseenter", ".mega-menu-item", function(e) {
		const menu = e.target.getElementsByClassName('mega-menu')[0];
		if (menu) {
			menu.style.display = "block"
		}
	})
	$(document).on("mouseleave", ".mega-menu-inner", function(e) {
		const menu = e.target.offsetParent;
		if (menu) {
			menu.style.display = "none"
		}
	})


	// Testimonial Slider
	if ($('.testimonial-slider').length) {
		const swiper = new Swiper('.testimonial-slider', {
			// Optional parameters
			loop: true,
			spaceBetween: 30,

			// Navigation arrows
			navigation: {
				nextEl: '.swiper-button-next',
				prevEl: '.swiper-button-prev',
			},
			speed: 800, 
			easing: 'easeOutQuad',
		});
	}

	

	// Project Slider
	if ($('.project-slider').length) {
		const swiper2 = new Swiper(".project-slider", {
			spaceBetween: 24,
			centeredSlides: false,
			loop:false,
			items: 2,
			autoHeight: true,
			pagination: {
				el: ".swiper-pagination",
				clickable: true,
			},
			breakpoints: {
				485: {
					// slidesPerView: 1,
				},
				768: {
					slidesPerView: 2,
				},
				1024: {
					slidesPerView: 3,
				}
			}
		});
	}

	// Contact Form Budget Slider

	if ($('#budget-value').length) {
		const value = document.querySelector("#budget-value");
		const input = document.querySelector("#pi_input");
		const budgetInput = document.querySelector('input[name="budget"]'); // Added this line
	
		value.textContent = input.value;
		budgetInput.value = input.value; // Store the budget value in the hidden input field
	
		input.addEventListener("input", (event) => {
			value.textContent = event.target.value;
			budgetInput.value = event.target.value; // Update the hidden input field when the user changes the budget
		});
	}
	

	//Menu bar 
	
	if ($('.header-2').length) {
		$(window).scroll(function () {
			if ($(window).scrollTop() > 50) {
				$('.header-2').addClass('is-fixed');
			} else {
				$('.header-2').removeClass('is-fixed');
			}
		});
	}

})(jQuery)

// Service Cards PopIn Animation //
const observer = new IntersectionObserver(entries => {
	// Loop over the entries
	entries.forEach(entry => {
		// If the element is visible
		if (entry.isIntersecting) {
			// Add the animation class
			entry.target.classList.add('pop-in');
		}
	});
});

const cards = document.getElementsByClassName('service-card');

for (let i = 0; i < cards.length; i++) {
	observer.observe(cards.item(i));
}

// Slide-left Animation
const slideLeftElements = document.querySelectorAll('.animation-slide-left');

function checkSlideLeft() {
    const windowHeight = window.innerHeight;
    const windowTop = window.pageYOffset;
    const windowBottom = windowTop + windowHeight;

    slideLeftElements.forEach(function (element) {
        const elementTop = element.getBoundingClientRect().top + window.pageYOffset;
        const elementBottom = elementTop + element.offsetHeight;

        if (elementBottom >= windowTop && elementTop <= windowBottom) {
            element.classList.add('slide-left');
        }
    });
}

window.addEventListener('scroll', checkSlideLeft);
window.addEventListener('resize', checkSlideLeft);
checkSlideLeft();

// Slide-Right Animation
const slideRightElements = document.querySelectorAll('.animation-slide-right');

function checkSlideRight() {
    const windowHeight = window.innerHeight;
    const windowTop = window.pageYOffset;
    const windowBottom = windowTop + windowHeight;

    slideRightElements.forEach(function (element) {
        const elementTop = element.getBoundingClientRect().top + window.pageYOffset;
        const elementBottom = elementTop + element.offsetHeight;

        if (elementBottom >= windowTop && elementTop <= windowBottom) {
            element.classList.add('slide-right');
        }
    });
}

window.addEventListener('scroll', checkSlideRight);
window.addEventListener('resize', checkSlideRight);
checkSlideRight();


