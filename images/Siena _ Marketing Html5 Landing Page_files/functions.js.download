/*global jQuery */
/* Contents
// ------------------------------------------------>
	2.  BACKGROUND INSERT
	9.  OWL CAROUSEL
	10. MAGNIFIC POPUP
	11. MAGNIFIC POPUP VIDEO
	14. SCROLL TO
	15. NAVABR TOGGLER
	16. PRICING FILTER

*/
(function ($) {
    "use strict";

    /* ------------------  Background INSERT ------------------ */

    var $bgSection = $(".bg-section");
    var $bgPattern = $(".bg-pattern");
    var $colBg = $(".col-bg");

    $bgSection.each(function () {
        var bgSrc = $(this).children("img").attr("src");
        var bgUrl = 'url(' + bgSrc + ')';
        $(this).parent().css("backgroundImage", bgUrl);
        $(this).parent().addClass("bg-section");
        $(this).remove();
    });

    $bgPattern.each(function () {
        var bgSrc = $(this).children("img").attr("src");
        var bgUrl = 'url(' + bgSrc + ')';
        $(this).parent().css("backgroundImage", bgUrl);
        $(this).parent().addClass("bg-pattern");
        $(this).remove();
    });

    $colBg.each(function () {
        var bgSrc = $(this).children("img").attr("src");
        var bgUrl = 'url(' + bgSrc + ')';
        $(this).parent().css("backgroundImage", bgUrl);
        $(this).parent().addClass("col-bg");
        $(this).remove();
    });

    /* ------------------ OWL CAROUSEL ------------------ */

    $(".carousel").each(function () {
        var $Carousel = $(this);
        $Carousel.owlCarousel({
            loop: $Carousel.data('loop'),
            autoplay: $Carousel.data("autoplay"),
            margin: $Carousel.data('space'),
            nav: $Carousel.data('nav'),
            dots: $Carousel.data('dots'),
            center: $Carousel.data('center'),
            dotsSpeed: $Carousel.data('speed'),
            responsive: {
                0: {
                    items: 1,
                },
                600: {
                    items: $Carousel.data('slide-rs'),
                },
                1000: {
                    items: $Carousel.data('slide'),
                }
            }
        });
    });

    /* ------------------ MAGNIFIC POPUP ------------------ */

    var $imgPopup = $(".img-popup");
    $imgPopup.magnificPopup({
        type: "image"
    });
    $('.img-gallery-item').magnificPopup({
        type: 'image',
        gallery: {
            enabled: true
        }
    });

    /* ------------------  MAGNIFIC POPUP VIDEO ------------------ */

    $('.popup-video,.popup-gmaps').magnificPopup({
        disableOn: 700,
        mainClass: 'mfp-fade',
        removalDelay: 0,
        preloader: false,
        fixedContentPos: false,
        type: 'iframe',
        iframe: {
            markup: '<div class="mfp-iframe-scaler">' +
                '<div class="mfp-close"></div>' +
                '<iframe class="mfp-iframe" frameborder="0" allowfullscreen></iframe>' +
                '</div>',
            patterns: {
                youtube: {
                    index: 'youtube.com/',
                    id: 'v=',
                    src: '//www.youtube.com/embed/%id%?autoplay=1'
                }
            },
            srcAction: 'iframe_src',
        }
    });

    /* ------------------  SCROLL TO ------------------ */

    var aScroll = $('a[data-scroll="scrollTo"]');
    aScroll.on('click', function (event) {
        var target = $($(this).attr('href'));
        if (target.length) {
            event.preventDefault();
            $('html, body').animate({
                scrollTop: target.offset().top - 100
            }, 1000);
            if ($(this).hasClass("menu-item")) {
                $(this).parent().addClass("active");
                $(this).parent().siblings().removeClass("active");
            }
        }
    });

    /* ------------------ NAVABR TOGGLER  ------------------ */

    var $toggler = $('.navbar-toggler');

    $toggler.on('click', function () {
        $(this).toggleClass('toggler-active');
    })

    /* ------------------ PRICING FILTER  ------------------ */

    if ($('.pricing-filter'.length > 0)) {

        var $pricingMonthly = $('.pricing-filter .monthly'),
            $pricingYearly = $('.pricing-filter .yearly'),
            $pricingSwitcher = $('.pricing-switcher');

        $pricingYearly.on('click', function (e) {
            e.preventDefault();
            $(this).toggleClass('is-active');
            $(this).siblings().removeClass('is-active');
            $(this).siblings('.switch').toggleClass('switch-yearly').removeClass('switch-monthly');
            $pricingSwitcher.toggleClass('active-yearly').removeClass('active-monthly');
        });

        $pricingMonthly.on('click', function (e) {
            e.preventDefault();
            $(this).toggleClass('is-active');
            $(this).siblings().removeClass('is-active');
            $(this).siblings('.switch').toggleClass('switch-monthly').removeClass('switch-yearly');
            $pricingSwitcher.toggleClass('active-monthly').removeClass('active-yearly');
        });
    }

    /* ------------------ ANIMATION  ------------------ */

    ScrollReveal().reveal('.reveal', {
        duration: 1000,
        delay: 300
    });


}(jQuery));