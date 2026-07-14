/* --------------------------------------------------
 * © Copyright 2016 - BuildPro by Designesia
 * --------------------------------------------------*/
(function($) {

	$('span.mouse').parents('.vc_column_container').css('position', 'inherit');
	$('.widget_recent_entries .post-date').prev().css('padding-left', '60px');
	/* --------------------------------------------------
	 * template options (customable)
	 * --------------------------------------------------*/
	var de_header_style = 2; // 1 - solid, 2 - transparent
	var de_header_layout = 2; // 1 - default, 2 - extended
	var de_menu_separator = 0; // 1 - dotted, 2 - border, 3 - circle, 4 - square, 5 - plus, 6 - strip, 0 - none
	var de_header_color = 1; // 1 - dark, - 2 light
	var de_header_scroll_color = 1; // 1 - dark, - 2 light
	/* --------------------------------------------------
	 * predefined vars
	 * --------------------------------------------------*/
	var mobile_menu_show = 0;
	var v_count = '0';
	var mb;
	var instances = [];
	var $window = $(window);

	/* --------------------------------------------------
	 * header | style
	 * --------------------------------------------------*/
	function header_styles() {
		if (de_header_style == 2) {
			$('header').addClass('transparent')
			$('body.error404').find('header').removeClass('transparent');
		}
		
		if (de_header_layout == 2) {
			$('header').addClass('de_header_2');
			$('header .info').show();
		}
		if (de_header_color == 2) {
			$('header').addClass('light');
		}
		if (de_header_scroll_color == 2) {
			$('header').addClass('scroll-light')
		};
	}
	/* --------------------------------------------------
	 * header | sticky
	 * --------------------------------------------------*/
	
	/* --------------------------------------------------
	 * plugin | magnificPopup
	 * --------------------------------------------------*/
	function load_magnificPopup() {
		$('.simple-ajax-popup-align-top').magnificPopup({
			type: 'ajax',
			alignTop: true,
			overflowY: 'scroll'
		});
		$('.simple-ajax-popup').magnificPopup({
			type: 'ajax'
		});
		// zoom gallery
		$('.zoom-gallery').magnificPopup({
			delegate: 'a',
			type: 'image',
			closeOnContentClick: false,
			closeBtnInside: false,
			mainClass: 'mfp-with-zoom mfp-img-mobile',
			image: {
				verticalFit: true,
				titleSrc: function(item) {
					return item.el.attr('title');
					//return item.el.attr('title') + ' &middot; <a class="image-source-link" href="'+item.el.attr('data-source')+'" target="_blank">image source</a>';
				}
			},
			gallery: {
				enabled: true
			},
			zoom: {
				enabled: true,
				duration: 300, // don't foget to change the duration also in CSS
				opener: function(element) {
					return element.find('img');
				}
			}
		});
		// popup youtube, video, gmaps
		$('.popup-vimeo, .popup-gmaps').magnificPopup({
			disableOn: 700,
			type: 'iframe',
			mainClass: 'mfp-fade',
			removalDelay: 160,
			preloader: false,
			fixedContentPos: false
		});
		// image popup
		$('.image-popup').magnificPopup({
			type: 'image',
			closeOnContentClick: true,
			mainClass: 'mfp-img-mobile',
			image: {
				verticalFit: true
			}
		});

		$('.image-popup-gallery, .popup-youtube').magnificPopup({
		     callbacks: {
		       elementParse: function(item) {
		          // the class name
		          if(item.el.context.className == 'popup-youtube') {
		            item.type = 'iframe';
		          } else {
		            item.type = 'image';
		          }
		       }
		     },
		     gallery:{
		      enabled:true
		     },
		     type: 'image',
		     closeOnContentClick: false,
		  closeBtnInside: false,
		  mainClass: 'mfp-with-zoom mfp-img-mobile',
		  image: {
		   verticalFit: true,
		   titleSrc: function(item) {
		    return item.el.attr('title');
		    //return item.el.attr('title') + ' &middot; <a class="image-source-link" href="'+item.el.attr('data-source')+'" target="_blank">image source</a>';
		   }
		  },
		});

		$('.image-popup-vertical-fit').magnificPopup({
			type: 'image',
			closeOnContentClick: true,
			mainClass: 'mfp-img-mobile',
			image: {
				verticalFit: true
			}
		});
		$('.image-popup-fit-width').magnificPopup({
			type: 'image',
			closeOnContentClick: true,
			image: {
				verticalFit: false
			}
		});
		$('.image-popup-no-margins').magnificPopup({
			type: 'image',
			closeOnContentClick: true,
			closeBtnInside: false,
			fixedContentPos: true,
			mainClass: 'mfp-no-margins mfp-with-zoom', // class to remove default margin from left and right side
			image: {
				verticalFit: true
			},
			zoom: {
				enabled: true,
				duration: 300 // don't foget to change the duration also in CSS
			}
		});
		
	}

	/* --------------------------------------------------
	 * plugin | enquire.js
	 * --------------------------------------------------*/
	function init_resize() {
		var mq = window.matchMedia("(min-width: 1025px)");
		var maxq = window.matchMedia("(max-width: 1024px)");

		if (mq.matches) {
			$('#mainmenu').show();
			mobile_menu_show = 1;
		} else {
			$('#mainmenu').hide();
			mobile_menu_show = 0;
			$("#menu-btn").show();
		}
		if (maxq.matches) {
			$('header').addClass("header-mobile");
		} else {
			$('header').removeClass("header-mobile");
		}

		init();
		init_de();
		video_autosize();
		var $container = $('#gallery');
		$container.isotope({
			itemSelector: '.item',
			filter: '*'
		});
		
		$('header').removeClass('smaller');
		$('header').removeClass('logo-smaller');
		$('header').removeClass('clone');
	};
	/* --------------------------------------------------
	 * plugin | owl carousel
	 * --------------------------------------------------*/
	function load_owl() {
		$("#gallery-carousel").owlCarousel({
			items: 4,
			navigation: false,
			pagination: false
		});
		$(".carousel-gallery").owlCarousel({
			items: 4,
			navigation: false,
			pagination: false
		});
		
		$("#testimonial-carousel").owlCarousel({
			items: 2,
			itemsDesktop: [1199, 2],
			itemsDesktopSmall: [980, 2],
			itemsTablet: [768, 1],
			itemsTabletSmall: false,
			itemsMobile: [479, 1],
			navigation: false,
		});
		$("#logo-carousel").owlCarousel({
			items: 6,
			navigation: false,
			pagination: false,
			autoPlay: true
		});
		$("#contact-carousel").owlCarousel({
			items: 1,
			singleItem: true,
			navigation: false,
			pagination: false,
			autoPlay: true
		});
		$(".text-slider").owlCarousel({
			items: 1,
			singleItem: true,
			navigation: false,
			pagination: false,
			mouseDrag: false,
			touchDrag: false,
			autoPlay: 2500,
			transitionStyle: "goDown"
		});
		$(".blog-slide").owlCarousel({
			items: 1,
			singleItem: true,
			navigation: false,
			pagination: false,
			autoPlay: false
		});
		$(".project-slide").owlCarousel({
			items: 1,
			singleItem: true,
			navigation: false,
			pagination: false,
			autoPlay: false,
			mouseDrag: false,
			touchDrag: true,
			transitionStyle: "fade"
		});
		$(".testimonial-list").owlCarousel({
			items: 1,
			singleItem: true,
			navigation: false,
			pagination: true,
			autoPlay: false
		});
		// Custom Navigation owlCarousel
		$(".next").on("click", function() {
			$(this).parent().parent().find('.blog-slide').trigger('owl.next');
		});
		$(".prev").on("click", function() {
			$(this).parent().parent().find('.blog-slide').trigger('owl.prev');
		});
		
		$('.owl-custom-nav').each(function() {
			var owl = $('.owl-custom-nav').next();
			var ow = parseInt(owl.css("height"), 10);
			$(this).css("margin-top", (ow / 2) - 25);
			owl.owlCarousel();
			// Custom Navigation Events
			$(".btn-next").on("click", function() {
				owl.trigger('owl.next');
			});
			$(".btn-prev").on("click", function() {
				owl.trigger('owl.prev');
			});
		});
	}
	/* --------------------------------------------------
	 * plugin | isotope
	 * --------------------------------------------------*/
	function filter_gallery() {
		var $container = $('#gallery');
		$container.isotope({
			itemSelector: '.item',
			filter: '*'
		});
		$('#filters a').on("click", function() {
			var $this = $(this);
			if ($this.hasClass('selected')) {
				return false;
			}
			var $optionSet = $this.parents();
			$optionSet.find('.selected').removeClass('selected');
			$this.addClass('selected');
			var selector = $(this).attr('data-filter');
			$container.isotope({
				filter: selector
			});
			return false;
		});
	}
	/* --------------------------------------------------
	 * plugin | fitvids
	 * --------------------------------------------------*/
	/*!
	* FitVids 1.0
	*
	* Copyright 2011, Chris Coyier - http://css-tricks.com + Dave Rupert - http://daverupert.com
	* Credit to Thierry Koblentz - http://www.alistapart.com/articles/creating-intrinsic-ratios-for-video/
	* Released under the WTFPL license - http://sam.zoy.org/wtfpl/
	*
	* Date: Thu Sept 01 18:00:00 2011 -0500
	*/
	!function(a){a.fn.fitVids=function(b){var c={customSelector:null},d=document.createElement("div"),e=document.getElementsByTagName("base")[0]||document.getElementsByTagName("script")[0];return d.className="fit-vids-style",d.innerHTML="&shy;<style> .fluid-width-video-wrapper { width: 100%; position: relative; padding: 0; } .fluid-width-video-wrapper iframe, .fluid-width-video-wrapper object, .fluid-width-video-wrapper embed { position: absolute; top: 0; left: 0; width: 100%; height: 100%; } </style>",e.parentNode.insertBefore(d,e),b&&a.extend(c,b),this.each(function(){var b=["iframe[src*='player.vimeo.com']","iframe[src*='www.youtube.com']","iframe[src*='www.kickstarter.com']","object","embed"];c.customSelector&&b.push(c.customSelector);var d=a(this).find(b.join(","));d.each(function(){var b=a(this);if(!("embed"==this.tagName.toLowerCase()&&b.parent("object").length||b.parent(".fluid-width-video-wrapper").length)){var c="object"==this.tagName.toLowerCase()||b.attr("height")?b.attr("height"):b.height(),d=b.attr("width")?b.attr("width"):b.width(),e=c/d;if(!b.attr("id")){var f="fitvid"+Math.floor(999999*Math.random());b.attr("id",f)}b.wrap('<div class="fluid-width-video-wrapper"></div>').parent(".fluid-width-video-wrapper").css("padding-top",100*e+"%"),b.removeAttr("height").removeAttr("width")}})})}}($);
	/* --------------------------------------------------
	 * back to top
	 * --------------------------------------------------*/
	var scrollTrigger = 500; // px
	function backToTop() {
		var scrollTop = $(window).scrollTop();
		if (scrollTop > scrollTrigger) {
			$('#back-to-top').addClass('show');
		} else {
			$('#back-to-top').removeClass('show');
		}
		$('#back-to-top').on('click', function(e) {
			e.preventDefault();
			$('html,body').stop(true).animate({
				scrollTop: 0
			}, 700);
		});
	};
	/* --------------------------------------------------
	 * plugin | scroll to
	 * --------------------------------------------------*/
	/*!
	 * $.scrollto.js 0.0.1 - https://github.com/yckart/$.scrollto.js
	 * Scroll smooth to any element in your DOM.
	 *
	 * Copyright (c) 2012 Yannick Albert (http://yckart.com)
	 * Licensed under the MIT license (http://www.opensource.org/licenses/mit-license.php).
	 * 2013/02/17
	 **/
	$.scrollTo = $.fn.scrollTo = function(x, y, options){
		if (!(this instanceof $)) return $.fn.scrollTo.apply($('html, body'), arguments);

		options = $.extend({}, {
			gap: {
				x: 0,
				y: 0
			},
			animation: {
				easing: 'easeInOutExpo',
				duration: 600,
				complete: $.noop,
				step: $.noop
			}
		}, options);

		return this.each(function(){
			var elem = $(this);
			elem.stop().animate({
				scrollLeft: !isNaN(Number(x)) ? x : $(y).offset().left + options.gap.x,
				scrollTop: !isNaN(Number(y)) ? y : $(y).offset().top + options.gap.y - 69 // *edited
			}, options.animation);
		});
	};
	/* --------------------------------------------------
	 * counting number
	 * --------------------------------------------------*/
	function de_counter() {
		$('.timer').each(function() {
			var imagePos = $(this).offset().top;
			var topOfWindow = $(window).scrollTop();
			if (imagePos < topOfWindow + $(window).height() && v_count == '0') {
				$(function($) {
					// start all the timers
					$('.timer').each(count);

					function count(options) {
						v_count = '1';
						var $this = $(this);
						options = $.extend({}, options || {}, $this.data('countToOptions') || {});
						$this.countTo(options);
					}
				});
			}
		});
	}
	/* --------------------------------------------------
	 * progress bar
	 * --------------------------------------------------*/
	function de_progress() {
		$('.de-progress').each(function() {
			var pos_y = $(this).offset().top;
			var value = $(this).find(".progress-bar").attr('data-value');
			var topOfWindow = $(window).scrollTop();
			if (pos_y < topOfWindow + 900) {
				$(this).find(".progress-bar").css({
					'width': value
				}, "slow");
			}
		});
	}
	/* --------------------------------------------------
	 * progress bar
	 * --------------------------------------------------*/

	text_rotate = function(){
    var quotes = $(".text-rotate-wrap .text-item");
    var quoteIndex = -1;
    
    function showNextQuote() {
        ++quoteIndex;
        quotes.eq(quoteIndex % quotes.length)
            .fadeIn(1)
            .delay(1500)
            .fadeOut(1, showNextQuote);
    }
    
    showNextQuote();
    
	};
	/* --------------------------------------------------
	 * custom background
	 * --------------------------------------------------*/
	function custom_bg() {
		$("div,section").css('background-color', function() {
			return $(this).data('bgcolor');
		});
		$("div,section").css('background-image', function() {
			return $(this).data('bgimage');
		});
		$("section.parallax").css('background-size', function() {
			return 'cover';
		});
	}
	/* --------------------------------------------------
	 * custom elements
	 * --------------------------------------------------*/
	function custom_elements() {
		// --------------------------------------------------
		// tabs
		// --------------------------------------------------
		$('.de_tab').find('.de_tab_content > div').hide();
		$('.de_tab').find('.de_tab_content > div:first').show();
		$('li').find('.v-border').fadeTo(150, 0);
		$('li.active').find('.v-border').fadeTo(150, 1);
		$('.de_nav li').on("click", function() {
			$(this).parent().find('li').removeClass("active");
			$(this).addClass("active");
			$(this).parent().parent().find('.v-border').fadeTo(150, 0);
			$(this).parent().parent().find('.de_tab_content > div').hide();
			var indexer = $(this).index(); //gets the current index of (this) which is #nav li
			$(this).parent().parent().find('.de_tab_content > div:eq(' + indexer + ')').fadeIn(); //uses whatever index the link has to open the corresponding box 
			$(this).find('.v-border').fadeTo(150, 1);
		});
		// --------------------------------------------------
		// tabs
		// --------------------------------------------------
		$('.de_review').find('.de_tab_content > div').hide();
		$('.de_review').find('.de_tab_content > div:first').show();
		//$('.de_review').find('.de_nav li').fadeTo(150,.5);
		$('.de_review').find('.de_nav li:first').fadeTo(150, 1);
		$('.de_nav li').on("click", function() {
			$(this).parent().find('li').removeClass("active");
			//$(this).parent().find('li').fadeTo(150,.5);
			$(this).addClass("active");
			$(this).fadeTo(150, 1);
			$(this).parent().parent().find('.de_tab_content > div').hide();
			var indexer = $(this).index(); //gets the current index of (this) which is #nav li
			$(this).parent().parent().find('.de_tab_content > div:eq(' + indexer + ')').show(); //uses whatever index the link has to open the corresponding box 
		});
		// --------------------------------------------------
		// toggle
		// --------------------------------------------------
		$(".toggle-list h2").addClass("acc_active");
		$(".toggle-list h2").toggle(function() {
			$(this).addClass("acc_noactive");
			$(this).next(".ac-content").slideToggle(200);
		}, function() {
			$(this).removeClass("acc_noactive").addClass("acc_active");
			$(this).next(".ac-content").slideToggle(200);
		})
	}
	/* --------------------------------------------------
	 * video autosize
	 * --------------------------------------------------*/
	function video_autosize() {
		$('.de-video-container').each(function() {
			var height_1 = $(this).css("height");
			var height_2 = $(this).find(".de-video-content").css("height");
			var newheight = (height_1.substring(0, height_1.length - 2) - height_2.substring(0, height_2.length - 2)) / 2;
			$(this).find('.de-video-overlay').css("height", height_1);
			$(this).find(".de-video-content").animate({
				'margin-top': newheight
			}, 'fast');
		});
	}
	/* --------------------------------------------------
	 * center x and y
	 * --------------------------------------------------*/
	function center_xy() {
		$('.center-xy').each(function() {
			$(this).parent().find("img").on('load', function() {
				var w = parseInt($(this).parent().find(".center-xy").css("width"), 10);
				var h = parseInt($(this).parent().find(".center-xy").css("height"), 10);
				var pic_w = $(this).css("width");
				var pic_h = $(this).css("height");
				$(this).parent().find(".center-xy").css("left", parseInt(pic_w, 10) / 2 - w / 2);
				$(this).parent().find(".center-xy").css("top", parseInt(pic_h, 10) / 2 - h / 2);
				$(this).parent().find(".bg-overlay").css("width", pic_w);
				$(this).parent().find(".bg-overlay").css("height", pic_h);
			}).each(function() {
				if (this.complete) $(this).load();
			});
		});
	}
	/* --------------------------------------------------
	 * add arrow for mobile menu
	 * --------------------------------------------------*/
	function menu_arrow() {
		// mainmenu create span
		$('#mainmenu li a').each(function() {
			if ($(this).next("ul").length > 0) {
				$("<span></span>").insertAfter($(this));
			}
		});
		// mainmenu arrow click
		$("#mainmenu > li > span").on("click", function() {
			$('header').css("height", "auto");
			var iteration = $(this).data('iteration') || 1;
			switch (iteration) {
				case 1:
					$(this).addClass("active");
					$(this).parent().find("ul:first").css("height", "auto");
					var curHeight = $(this).parent().find("ul:first").height();
					$(this).parent().find("ul:first").css("height", "0");
					$(this).parent().find("ul:first").animate({
						'height': curHeight
					}, 400, 'easeInOutQuint');
					break;
				case 2:
					$(this).removeClass("active");
					$(this).parent().find("ul:first").animate({
						'height': "0"
					}, 400, 'easeInOutQuint');
					break;
			}
			iteration++;
			if (iteration > 2) iteration = 1;
			$(this).data('iteration', iteration);
		});
		$("#mainmenu > li > ul > li > span").on("click", function() {
			var iteration = $(this).data('iteration') || 1;
			switch (iteration) {
				case 1:
					$(this).addClass("active");
					$(this).parent().find("ul:first").css("height", "auto");
					$(this).parent().parent().parent().find("ul:first").css("height", "auto");
					var curHeight = $(this).parent().find("ul:first").height();
					$(this).parent().find("ul:first").css("height", "0");
					$(this).parent().find("ul:first").animate({
						'height': curHeight
					}, 400, 'easeInOutQuint');
					break;
				case 2:
					$(this).removeClass("active");
					$(this).parent().find("ul:first").animate({
						'height': "0"
					}, 400, 'easeInOutQuint');
					break;
			}
			iteration++;
			if (iteration > 2) iteration = 1;
			$(this).data('iteration', iteration);
		});
	}
	/* --------------------------------------------------
	 * show gallery item sequence
	 * --------------------------------------------------*/
	sequence = function(){
		var sq = $(".sequence > .sq-item .picframe");
		var count = sq.length;
		sq.addClass("slideInUp");
		for (var i = 0; i <= count; i++) {
		  sqx = $(".sequence > .sq-item:eq("+i+") .picframe");
		  sqx.attr('data-wow-delay',(i/8)+'s');
		}		
	}
	/* --------------------------------------------------
	 * show gallery item sequence
	 * --------------------------------------------------*/
	sequence_a = function(){
		var sq = $(".sequence > .sq-item");
		var count = sq.length;
		sq.addClass("slideInUp");
		for (var i = 0; i <= count; i++) {
		  sqx = $(".sequence > .sq-item:eq("+i+")");
		  sqx.attr('data-wow-delay',(i/8)+'s');
		}		
	}
	/* --------------------------------------------------
	 * custom scroll
	 * --------------------------------------------------*/
	$.fn.moveIt = function(){	  
	  $(this).each(function(){
		instances.push(new moveItItem($(this)));
	  });
	}
	moveItItemNow = function(){
	var scrollTop = $window.scrollTop();
		instances.forEach(function(inst){
		  inst.update(scrollTop);
		});
	}
	var moveItItem = function(el){
	  this.el = $(el);
	  this.speed = parseInt(this.el.attr('data-scroll-speed'));
	};
	moveItItem.prototype.update = function(scrollTop){
	  var pos = scrollTop / this.speed;
	  this.el.css('transform', 'translateY(' + pos + 'px)');
	};
	$(function(){
	  $('[data-scroll-speed]').moveIt();
	});
	/* --------------------------------------------------
	 * multiple function
	 * --------------------------------------------------*/
	function init() {
		var sh = $('#de-sidebar').css("height");
		var dh = $(window).innerHeight();
		var h = parseInt(sh) - parseInt(dh);

		function scrolling() {
			var mq = window.matchMedia("(min-width: 1025px)");
			var ms = window.matchMedia("(min-width: 768px)");
			var mt = window.matchMedia("(max-width: 1024px)");
			
			if (mq.matches) {
				var distanceY = window.pageYOffset || document.documentElement.scrollTop,
					shrinkOn = 55,
					header = jQuery("header");
				if (distanceY > shrinkOn) {
					if(!jQuery('#wrapper').hasClass('side-layout')){
						header.addClass("smaller");
					}
				} else {
					if (header.hasClass('smaller')) {
						header.removeClass('smaller');
					}
				}
				
				if (jQuery("#wrapper").hasClass("side-content")) {
					jQuery("#wrapper").addClass("side-layout");
				}
			}
			if (mq.matches) {
				if ($("header").hasClass("side-header")) {
					if ($(document).scrollTop() >= h) {
						$('#de-sidebar').css("position", "fixed");
						if (parseInt(sh) > parseInt(dh)) {
							$('#de-sidebar').css("top", -h);
						}
						$('#main').addClass("col-md-offset-3");
						$('h1#logo img').css("padding-left", "7px");
						$('header .h-content').css("padding-left", "7px");
						$('#mainmenu li').css("width", "103%");
					} else {
						$('#de-sidebar').css("position", "relative");
						if (parseInt(sh) > parseInt(dh)) {
							$('#de-sidebar').css("top", 0);
						}
						$('#main').removeClass("col-md-offset-3");
						$('h1#logo img').css("padding-left", "0px");
						$('header .h-content').css("padding-left", "0px");
						$('#mainmenu li').css("width", "100%");
					}
				}
			}
			if (mt.matches) {
				if (jQuery("#wrapper").hasClass("side-content")) {
					jQuery("#wrapper").removeClass("side-layout");
				}
			}
		}
		scrolling();
	}
	/* --------------------------------------------------
	 * multiple function
	 * --------------------------------------------------*/
	function init_de() {
		$('.de-team-list').each(function() {
			$(this).find("img").on('load', function() {
				var w = $(this).css("width");
				var h = $(this).css("height");
				//nh = (h.substring(0, h.length - 2)/2)-48;
				$(this).parent().parent().find(".team-pic").css("height", h);
				$(this).parent().parent().find(".team-desc").css("width", w);
				$(this).parent().parent().find(".team-desc").css("height", h);
				$(this).parent().parent().find(".team-desc").css("top", h);
			}).each(function() {
				if (this.complete) $(this).load();
			});
		});
		
		$(".de-team-list").on("mouseenter", function() {
				var h;
				h = $(this).find("img").css("height");
				$(this).find(".team-desc").stop(true).animate({
					'top': "0px"
				}, 350, 'easeOutQuad');
				$(this).find("img").stop(true).animate({
					'margin-top': "-100px"
				}, 400, 'easeOutQuad');
			}).on("mouseleave", function() {
				var h;
				h = $(this).find("img").css("height");
				$(this).find(".team-desc").stop(true).animate({
					'top': h
				}, 350, 'easeOutQuad');
				$(this).find("img").stop(true).animate({
					'margin-top': "0px"
				}, 400, 'easeOutQuad');
			})
			// portfolio
		$('.item .picframe').each(function() {
			$(this).find("img").css("width", "100%");
			$(this).find("img").css("height", "auto");
			$(this).find("img").on('load', function() {
				var w = $(this).css("width");
				var h = $(this).css("height");
				//nh = (h.substring(0, h.length - 2)/2)-48;
				$(this).parent().css("height", h);
			}).each(function() {
				if (this.complete) $(this).load();
			});
		});
		// --------------------------------------------------
		// portfolio hover
		// --------------------------------------------------
		$('.overlay').fadeTo(1, 0);
		// gallery hover
		$(".item .picframe").on("mouseenter", function() {
			$(this).parent().find(".overlay").width($(this).find("img").css("width"));
			$(this).parent().find(".overlay").height($(this).find("img").css("height"));
			$(this).parent().find(".overlay").stop(true).fadeTo(200, .9);
			var picheight = $(this).find("img").css("height");
			var newheight;
			newheight = (picheight.substring(0, picheight.length - 2) / 2) - 10;
			$(this).parent().find(".pf_text").css('margin-top', newheight);
			$(this).parent().find(".pf_text").stop(true).animate({
				'opacity': '1'
			}, 1000, 'easeOutCubic');
			var w = $(this).find("img").css("width");
			var h = $(this).find("img").css("height");
			var w = parseInt(w, 10);
			var h = parseInt(h, 10);
			var $scale = 1.1;
			$(this).find("img").stop(true).animate({
				width: w * $scale,
				height: h * $scale,
				'margin-left': -w * ($scale - 1) / 2,
				'margin-top': -h * ($scale - 1) / 2
			}, 400, 'easeOutCubic');
		}).on("mouseleave", function() {
			var newheight;
			var picheight = $(this).find("img").css("height");
			newheight = (picheight.substring(0, picheight.length - 2) / 2) - 10;
			$(this).parent().find(".pf_text").stop(true).animate({
				'opacity': '0'
			}, 400, 'easeOutCubic');
			$(this).parent().find(".overlay").stop(true).fadeTo(200, 0);
			$(this).find("img").stop(true).animate({
				width: '100%',
				height: '100%',
				'margin-left': 0,
				'margin-top': 0
			}, 400, 'easeOutQuad');
		})
		$('.overlay').fadeTo(1, 0);
		$.stellar('refresh');
	}

	active_menu = function(){
		if ($('body').hasClass('one-page')) {
		jQuery('#mainmenu li a').each(function () {
                if (this.href.indexOf('#') != -1) {
                    var href = jQuery(this).attr('href');
                    if (jQuery(window).scrollTop() > jQuery(href).offset().top - 140) {
                        jQuery('nav li a').removeClass('active');
                        jQuery(this).addClass('active');
                    }
                }
            });	
		}			
	}
	
	/* --------------------------------------------------
	 * document ready
	 * --------------------------------------------------*/
	$(document).ready(function() {
		'use strict';
		$("body").show();
		$('body').addClass('de_light');
		new WOW().init();
		header_styles();
		load_magnificPopup();
		center_xy();
		init_de();
		init_resize();
		// --------------------------------------------------
		// custom positiion
		// --------------------------------------------------
		var $doc_height = $(window).innerHeight();
		$('#homepage #content.content-overlay').css("margin-top", $doc_height);
		$('.full-height').css("height", $doc_height);
		var picheight = $('.center-y').css("height");
		picheight = parseInt(picheight, 10);
		$('.center-y').css('margin-top', (($doc_height - picheight) / 2) - 90);
		$('.full-height .de-video-container').css("height", $doc_height);
		// --------------------------------------------------
		// blog list hover
		// --------------------------------------------------
		$(".blog-list").on("mouseenter", function() {
				var v_height = $(this).find(".blog-slide").css("height");
				var v_width = $(this).find(".blog-slide").css("width");
				var newheight = ( v_height - 2 / 2 ) - 40;
				$(this).find(".owl-arrow").css("margin-top", newheight);
				$(this).find(".owl-arrow").css("width", v_width);
				$(this).find(".owl-arrow").fadeTo(150, 1);
				//alert(v_height);
			}).on("mouseleave", function() {
				$(this).find(".owl-arrow").fadeTo(150, 0);
			})
			//  logo carousel hover
		$("#logo-carousel img").on("mouseenter", function() {
			$(this).fadeTo(150, .5);
		}).on("mouseleave", function() {
			$(this).fadeTo(150, 1);
		})
		if ($('#back-to-top').length) {
			backToTop();
		}
		$(".nav-exit").on("click", function() {
			$.magnificPopup.close();
		});
		// --------------------------------------------------
		// navigation for mobile
		// --------------------------------------------------
		$('#menu-btn').on("click", function() {
				if (mobile_menu_show == 0) {
					$('#mainmenu').slideDown();
					mobile_menu_show = 1;
				} else {
					$('#mainmenu').slideUp();
					mobile_menu_show = 0;
				}
			})
		$("a.btn").on("click", function(evn) {
			if (this.href.indexOf('#') != -1) {
				evn.preventDefault();
				$('html,body').scrollTo(this.hash, this.hash);
			}
		});
		$('.de-gallery .item .icon-info').on("click", function() {
			$('.page-overlay').show();
			url = $(this).attr("data-value");
			$("#loader-area .project-load").load(url, function() {
				$("#loader-area").slideDown(500, function() {
					$('.page-overlay').hide();
					$('html, body').animate({
						scrollTop: $('#loader-area').offset().top - 70
					}, 500, 'easeOutCubic');
					//
					$(".image-slider").owlCarousel({
						items: 1,
						singleItem: true,
						navigation: false,
						pagination: true,
						autoPlay: false
					});
					$(".container").fitVids();
					$('#btn-close-x').on("click", function() {
						$("#loader-area").slideUp(500, function() {
							$('html, body').animate({
								scrollTop: $('#section-portfolio').offset().top - 70
							}, 500, 'easeOutCirc');
						});
						return false;
					});
				});
			});
		});
		$('.de-gallery .item').on("click", function() {
			$('#navigation').show();
		});
		// btn arrow up
		$(".arrow-up").on("click", function() {
			$(".coming-soon .coming-soon-content").fadeOut("medium", function() {
				$("#hide-content").fadeIn(600, function() {
					$('.arrow-up').animate({
						'bottom': '-40px'
					}, "slow");
					$('.arrow-down').animate({
						'top': '0'
					}, "slow");
				});
			});
		});
		// btn arrow down
		$(".arrow-down").on("click", function() {
			$("#hide-content").fadeOut("slow", function() {
				$(".coming-soon .coming-soon-content").fadeIn(800, function() {
					$('.arrow-up').animate({
						'bottom': '0px'
					}, "slow");
					$('.arrow-down').animate({
						'top': '-40'
					}, "slow");
				});
			});
		});
		/* --------------------------------------------------
		 * window | on load
		 * --------------------------------------------------*/
		$(window).on('load', function() {
			video_autosize();
			filter_gallery();
			custom_bg();
			menu_arrow();
			load_owl();
			custom_elements();
			init();

			// hide preloader after loaded
			$('#preloader').delay(500).fadeOut(500);
			
			// one page navigation
			/**
			 * This part causes smooth scrolling using scrollto.js
			 * We target all a tags inside the nav, and apply the scrollto.js to it.
			 */
			$("#mainmenu a, .scroll-to").on("click", function(evn) {
				if (this.href.indexOf('#') != -1) {
					$('html,body').scrollTo(this.hash, this.hash);
					evn.preventDefault();
				}
			});
			sequence();
			sequence_a();
		});
		/* --------------------------------------------------
		 * window | on resize
		 * --------------------------------------------------*/
		window.onresize = function(event) {
			init_resize();
		};
		/* --------------------------------------------------
		 * window | on scroll
		 * --------------------------------------------------*/
		$(window).on("scroll", function() {
			/* functions */
			//header_sticky();
			de_counter();
			de_progress();
			init();
			backToTop();
			moveItItemNow();
			active_menu();
			/* plugin | stellar */
			$.stellar({
				horizontalScrolling: false,
				verticalOffset: 0
			});
			/* fade base scroll position */
			var target = $('.fadeScroll');
			var targetHeight = target.outerHeight();
			var scrollPercent = (targetHeight - window.scrollY) / targetHeight;
			if (scrollPercent >= 0) {
				target.css('opacity', scrollPercent);
			}else{
				target.css('opacity', 0);
			}
			// custom page with background on side
			$('.side-bg').each(function() {
				$(this).find(".image-container").css("height", $(this).find(".image-container").parent().css("height"));
			});
			/* go to anchor */
			$('#homepage nav li a').each(function() {
				if (this.href.indexOf('#') != -1) {
					var href = $(this).attr('href');
					if (typeof offset !== 'undefined') {
						if ($(window).scrollTop() > $(href).offset().top - 140) {
							$('nav li a').removeClass('active');
							$(this).addClass('active');
						}
					}
				}
			});
		});
	});

	
	// --------------------------------------------------
	// paralax background
	// --------------------------------------------------
	var $window = $(window);
   	$('section[data-type="background"]').each(function(){
		var $bgobj = $(this); // assigning the object
						
		$(window).scroll(function() {
			var yPos = -($window.scrollTop() / $bgobj.data('speed')); 
			var coords = '50% '+ yPos + 'px';
			$bgobj.css({ backgroundPosition: coords });
			
		});
 	});

})(jQuery);