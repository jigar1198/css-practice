<template>
  <div>
    <nav class="navigation" id="navigation">
      <div class="navigation__left-part" id="navigation__left-part">
        <a class="navigation-brand">
          <img
            src="~/assets/images/logo/saffola-oats-logo-4-x-copy.png"
            class="navigation-logo"
          />
        </a>
      </div>
      <div class="navigation__right-part">
        <div
          class="navigation__right-part--desktop"
          id="navigation__right-part--desktop"
        >
          <a href="#products" style="text-decoration: none"
            ><h5 class="navigation__right-part--desktop__text">Products</h5></a
          >
          <a href="#features" style="text-decoration: none"
            ><h5 class="navigation__right-part--desktop__text">Features</h5></a
          >
          <a href="#steps" style="text-decoration: none"
            ><h5 class="navigation__right-part--desktop__text">
              Preparation
            </h5></a
          >
          <a href="#recipes" style="text-decoration: none"
            ><h5 class="navigation__right-part--desktop__text">Recipes</h5></a
          >
          <a href="#testimonials" style="text-decoration: none"
            ><h5 class="navigation__right-part--desktop__text">
              Testimonials
            </h5></a
          >
          <div
            class="navigation__right-part--desktop__button"
            @click="openBuyNowSection('desktop')"
          >
            Buy Now
          </div>
          <div class="buy-now__section--hide" id="buy-now__section--desktop">
            <div class="buy-now-container">
              <div>
                <div class="buy-now__company-logo">
                  <a href="#"
                    ><img src="~/assets/images/buy-now/saffola.png" alt=""
                  /></a>
                </div>
                <div class="buy-now__company-logo">
                  <a href="#"
                    ><img src="~/assets/images/buy-now/amazon.png" alt=""
                  /></a>
                </div>
              </div>
              <div>
                <div class="buy-now__company-logo">
                  <a href="#"
                    ><img src="~/assets/images/buy-now/big-basket.png" alt=""
                  /></a>
                </div>
                <div class="buy-now__company-logo">
                  <a href="#"
                    ><img src="~/assets/images/buy-now/grofers.png" alt=""
                  /></a>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div class="navigation__right-part--mobile">
          <img
            src="~/assets/images/hamburger-icon.svg"
            class="hamburger__menu"
            id="hamburger__menu"
            @click="openMobileNavigation"
          />
          <img
            src="~/assets/images/hamburger-icon-yellow.svg"
            class="hamburger__menu--yellow removeClass"
            id="hamburger__menu--yellow"
            @click="openMobileNavigation"
          />
        </div>
      </div>
      <div
        class="navigation__mobile"
        :class="showNavBar ? 'show__navigation__mobile' : ''"
        id="navigation__mobile"
      >
        <div class="close__menu">
          <img
            src="~/assets/images/close.svg"
            id="close__menu"
            @click="closeMobileNavigation"
          />
        </div>
        <a
          href="#products"
          @click="showNavBar = false"
          style="text-decoration: none"
        >
          <h5 class="navigation__mobile-text">Products</h5>
        </a>
        <a
          href="#features"
          @click="showNavBar = false"
          style="text-decoration: none"
          ><h5 class="navigation__mobile-text">Features</h5></a
        >
        <a
          href="#steps"
          @click="showNavBar = false"
          style="text-decoration: none"
        >
          <h5 class="navigation__mobile-text">Preparation</h5></a
        >
        <a
          href="#recipes"
          @click="showNavBar = false"
          style="text-decoration: none"
        >
          <h5 class="navigation__mobile-text">Recipes</h5></a
        >
        <a
          href="#testimonials"
          @click="showNavBar = false"
          style="text-decoration: none"
        >
          <h5 class="navigation__mobile-text">Testimonials</h5>
        </a>
      </div>
    </nav>
    <div
      class="buy-now-button__mobile"
      @click="openBuyNowSection('mobile')"
      v-show="showBottomBuyNow"
    >
      Buy Now
      <span>
        <img
          src="~/assets/images/down-buyNow.svg"
          class="buy-now-button__mobile-image"
        />
      </span>
      <div class="buy-now__section--hide" id="buy-now__section--mobile">
        <div class="buy-now-container">
          <div>
            <div class="buy-now__company-logo">
              <a href="#"
                ><img src="~/assets/images/buy-now/saffola.png" alt=""
              /></a>
            </div>
            <div class="buy-now__company-logo">
              <a href="#"
                ><img src="~/assets/images/buy-now/amazon.png" alt=""
              /></a>
            </div>
          </div>
          <div>
            <div class="buy-now__company-logo">
              <a href="#"
                ><img src="~/assets/images/buy-now/big-basket.png" alt=""
              /></a>
            </div>
            <div class="buy-now__company-logo">
              <a href="#"
                ><img src="~/assets/images/buy-now/grofers.png" alt=""
              /></a>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="back-to-top__container--hide" id="back-to-top__container">
      <a href="#top-banner" style="text-decoration: none">
        <img
          src="~/assets/images/up-arrow.svg"
          class="back-to-top__image img-responsive img-fluid"
        />
      </a>
    </div>
    <section id="top-banner">
      <VueSlickCarousel
        :arrows="false"
        :dots="true"
        class="top-banner-carousel"
      >
        <div class="bannerOne">
          <div class="leftPart">
            <img
              class="img-responsive img-fluid images"
              src="~/assets/images/top-banner/product1.png"
            />
            <div class="disclaimer-text disclamer-text__large-screen">
              Disclaimer: Vegetables are dehydrated to maintain goodness and
              taste, Creative visualization, Suggested garnishing
            </div>
          </div>
          <div class="rightPart">
            <h1 class="right-side__main-text">
              Lip-smacking<br />flavours to
              <span class="right-side__main-text--yellow">snack healthy</span>
            </h1>
            <p class="right-side__sub-text">
              With wholegrain oats + real veggies*
            </p>
            <div class="disclaimer-text disclamer-text__small-screen">
              Disclaimer: Vegetables are dehydrated to maintain goodness and
              taste, Creative visualization, Suggested garnishing
            </div>
          </div>
        </div>
        <div class="bannerTwo">
          <div class="leftPart">
            <img
              class="img-responsive img-fluid images"
              src="~/assets/images/top-banner/bowl.png"
            />
          </div>
          <div class="rightPart">
            <h1 class="right-side__main-text">
              Oh-so delicious!
              <span class="right-side__main-text--yellow"> A snack for</span>
              <span class="right-side__main-text--yellow">your anytime</span>
              <span class="right-side__main-text--yellow"> cravings! </span>
            </h1>
            <div class="disclaimer-text disclamer-text__small-screen">
              Disclaimer: Vegetables are dehydrated to maintain goodness and
              taste, Creative visualization, Suggested garnishing
            </div>
          </div>
        </div>
        <div class="bannerThree">
          <div class="leftPart">
            <img
              class="img-responsive img-fluid images"
              src="~/assets/images/top-banner/product1.png"
            />
          </div>
          <div class="rightPart">
            <h1 class="right-side__main-text">
              Delightful<br />snack ready
              <span class="right-side__main-text--yellow">in just</span>
              <span class="right-side__main-text--yellow">3 minutes!</span>
            </h1>
            <div class="disclaimer-text disclamer-text__small-screen">
              Disclaimer: Vegetables are dehydrated to maintain goodness and
              taste, Creative visualization, Suggested garnishing
            </div>
          </div>
        </div>
      </VueSlickCarousel>
    </section>
    <section class="products" id="products">
      <Slick id="productItems" :options="productItemsSettings">
        <div class="product-item">
          <div class="product-item__left-part">
            <img
              src="~/assets/images/products/description/classic-masala.png"
              class="product-image"
            />
          </div>
          <div class="product-item__right-part">
            <h2 class="product-item__right-part--heading">Classic Masala</h2>
            <p class="product-item__right-part--description">
              The heart wants what it wants, so why hold back! Have it as a hot
              bowl of Oats or as a cold yummy dessert, or as a healthy add-on to
              your exiting sweet and savoury delights.
            </p>
            <div class="product-image__mobile-container">
              <img
                src="~/assets/images/products/description/classic-masala.png"
                class="product-image product-image-mobile"
              />
            </div>
            <div class="product-item__right-part--add-on">
              <p class="product-item__right-part--add-on__top-text">Add On</p>
              <div
                class="product-item__right-part--add-on__background-image-container"
              >
                <img
                  src="~/assets/images/products/combined-shape.png"
                  class="product-item__right-part--add-on__background-image img-responsive img-fluid"
                />
              </div>
              <div
                class="product-item__right-part--add-on__product-image-container"
              >
                <img
                  src="~/assets/images/products/addOns/classic-masala-peanuts.png"
                  class="product-item__right-part--add-on__product-image img-responsive img-fluid"
                />
              </div>
              <p class="product-item__right-part--add-on-text">
                Top your bowl of classic masala oats with crushed peanuts for
                the extra bite
              </p>
            </div>
          </div>
        </div>
        <div class="product-item">
          <div class="product-item__left-part">
            <img
              src="~/assets/images/products/description/peppy-tomato.png"
              class="product-image"
            />
          </div>
          <div class="product-item__right-part">
            <h2 class="product-item__right-part--heading">Peppy Tomato</h2>
            <p class="product-item__right-part--description">
              Relish a tangy bowl of Peppy Tomato flavour for the uplifting
              tingling taste. Indulge your tastebuds in savoury mix of spices
              and crunchy veggies.
            </p>
            <div class="product-image__mobile-container">
              <img
                src="~/assets/images/products/description/peppy-tomato.png"
                class="product-image product-image-mobile"
              />
            </div>
            <div class="product-item__right-part--add-on">
              <p class="product-item__right-part--add-on__top-text">Add On</p>
              <div
                class="product-item__right-part--add-on__background-image-container"
              >
                <img
                  src="~/assets/images/products/combined-shape.png"
                  class="product-item__right-part--add-on__background-image img-responsive img-fluid"
                />
              </div>
              <div
                class="product-item__right-part--add-on__product-image-container"
              >
                <img
                  src="~/assets/images/products/addOns/peppy-tomato-green-pepper.png"
                  class="product-item__right-part--add-on__product-image img-responsive img-fluid"
                />
              </div>
              <p class="product-item__right-part--add-on-text">
                Add some capsicum to your Peppy Tomato for a desi Mexican touch.
              </p>
            </div>
          </div>
        </div>
        <div class="product-item">
          <div class="product-item__left-part">
            <img
              src="~/assets/images/products/description/veggie-twist.png"
              class="product-image"
            />
          </div>
          <div class="product-item__right-part">
            <h2 class="product-item__right-part--heading">Veggie Twist</h2>
            <p class="product-item__right-part--description">
              Satiate your anytime craving with a comforting bowl of your
              favourite veggies in aromatic blend of chili, garlic, and curry
              leaves that will leave you wanting for more!
            </p>
            <div class="product-image__mobile-container">
              <img
                src="~/assets/images/products/description/veggie-twist.png"
                class="product-image product-image-mobile"
              />
            </div>
            <div class="product-item__right-part--add-on">
              <p class="product-item__right-part--add-on__top-text">Add On</p>
              <div
                class="product-item__right-part--add-on__background-image-container"
              >
                <img
                  src="~/assets/images/products/combined-shape.png"
                  class="product-item__right-part--add-on__background-image img-responsive img-fluid"
                />
              </div>
              <div
                class="product-item__right-part--add-on__product-image-container"
              >
                <img
                  src="~/assets/images/products/addOns/veggie-twist-spring-onions.png"
                  class="product-item__right-part--add-on__product-image img-responsive img-fluid"
                />
              </div>
              <p class="product-item__right-part--add-on-text">
                Top up your veggie twist with some spring onions for the
                freshness and crunch
              </p>
            </div>
          </div>
        </div>
        <div class="product-item">
          <div class="product-item__left-part">
            <img
              src="~/assets/images/products/description/masala-coriander.png"
              class="product-image"
            />
          </div>
          <div class="product-item__right-part">
            <h2 class="product-item__right-part--heading">Masala Coriander</h2>
            <p class="product-item__right-part--description">
              Popular in the south, Masala Coriander is a flavourful blend of
              tempting well-loved spices of South and aromatic coriander.
            </p>
            <div class="product-image__mobile-container">
              <img
                src="~/assets/images/products/description/masala-coriander.png"
                class="product-image product-image-mobile"
              />
            </div>
            <div class="product-item__right-part--add-on">
              <p class="product-item__right-part--add-on__top-text">Add On</p>
              <div
                class="product-item__right-part--add-on__background-image-container"
              >
                <img
                  src="~/assets/images/products/combined-shape.png"
                  class="product-item__right-part--add-on__background-image img-responsive img-fluid"
                />
              </div>
              <div
                class="product-item__right-part--add-on__product-image-container"
              >
                <img
                  src="~/assets/images/products/addOns/masala-coriander-gun-powder.png"
                  class="product-item__right-part--add-on__product-image img-responsive img-fluid"
                />
              </div>
              <p class="product-item__right-part--add-on-text">
                Top it up with drizzle of ghee & some gun powder
              </p>
            </div>
          </div>
        </div>
        <div class="product-item">
          <div class="product-item__left-part">
            <img
              src="~/assets/images/products/description/flavours-of south-pack.png"
              class="product-image product-image__flavours-of-south"
            />
          </div>
          <div class="product-item__right-part">
            <h2 class="product-item__right-part--heading">Flavours of South</h2>
            <p class="product-item__right-part--description">
              The magic of well-loved spices of south in three delicious south
              flavours that would leave everyone craving for more! Be it
              aromatic Sambar or fiery Chettinad or hot Curry Pepper, these
              flavours make for delightful warm family snacks that are too hot
              to handle - Mind it!
            </p>
            <div class="product-image__mobile-container">
              <img
                src="~/assets/images/products/description/flavours-of south-pack.png"
                class="product-image product-image-mobile"
              />
            </div>
            <div
              class="product-item__right-part--add-on product-item__right-part--add-on__flavours-of-south"
            >
              <p class="product-item__right-part--add-on__top-text">Add On</p>
              <div
                class="product-item__right-part--add-on__background-image-container"
              >
                <img
                  src="~/assets/images/products/combined-shape.png"
                  class="product-item__right-part--add-on__background-image img-responsive img-fluid"
                />
              </div>
              <div
                class="product-item__right-part--add-on__product-image-container"
              >
                <img
                  src="~/assets/images/products/addOns/south-of-flavours-cashews.png"
                  class="product-item__right-part--add-on__product-image img-responsive img-fluid"
                />
              </div>
              <p class="product-item__right-part--add-on-text">
                Top it up with your favourite nuts!
              </p>
            </div>
          </div>
        </div>
        <div class="product-item">
          <div class="product-item__left-part">
            <img
              src="~/assets/images/products/description/plain-oats-pack.png"
              class="product-image"
            />
          </div>
          <div class="product-item__right-part">
            <h2 class="product-item__right-part--heading">Saffola Oats</h2>
            <p class="product-item__right-part--description">
              The heart wants what it wants, so why hold back! Have it as a hot
              bowl of Oats or as a cold yummy dessert, or as a healthy add-on to
              your exiting sweet and savoury delights.
            </p>
            <div class="product-image__mobile-container">
              <img
                src="~/assets/images/products/description/plain-oats-pack.png"
                class="product-image product-image-mobile"
              />
            </div>
            <div class="product-item__right-part--add-on">
              <p class="product-item__right-part--add-on__top-text">Add On</p>
              <div
                class="product-item__right-part--add-on__background-image-container"
              >
                <img
                  src="~/assets/images/products/combined-shape.png"
                  class="product-item__right-part--add-on__background-image img-responsive img-fluid"
                />
              </div>
              <div
                class="product-item__right-part--add-on__product-image-container"
              >
                <img
                  src="~/assets/images/products/addOns/plain-oats-nuts-berries.png"
                  class="product-item__right-part--add-on__product-image img-responsive img-fluid"
                />
              </div>
              <p class="product-item__right-part--add-on-text">
                Drizzle some honey or maple syrup and top it off with chocolate
                chips, fresh berries, raisins, or nuts!
              </p>
            </div>
          </div>
        </div>
      </Slick>
      <Slick
        id="productCards"
        :options="productCardsSettings"
        class="products-carousel"
      >
        <div class="product-card">
          <div class="product-card__content-container">
            <div class="product-card--image">
              <img src="~/assets/images/products/cards/bitmap1.png" />
            </div>
            <div class="product-card--text">
              <p>Classic Masala</p>
            </div>
          </div>
        </div>
        <div class="product-card">
          <div class="product-card__content-container">
            <div class="product-card--image">
              <img src="~/assets/images/products/cards/bitmap2.png" />
            </div>
            <div class="product-card--text">
              <p>Peppy Tomato</p>
            </div>
          </div>
        </div>
        <div class="product-card">
          <div class="product-card__content-container">
            <div class="product-card--image">
              <img src="~/assets/images/products/cards/bitmap3.png" />
            </div>
            <div class="product-card--text">
              <p>Veggie Twist</p>
            </div>
          </div>
        </div>
        <div class="product-card">
          <div class="product-card__content-container">
            <div class="product-card--image">
              <img src="~/assets/images/products/cards/bitmap4.png" />
            </div>
            <div class="product-card--text">
              <p>Masala Coriander</p>
            </div>
          </div>
        </div>
        <div class="product-card">
          <div class="product-card__content-container">
            <div class="product-card--image">
              <img src="~/assets/images/products/cards/bitmap5.png" />
            </div>
            <div class="product-card--text">
              <p>Flavours of South</p>
            </div>
          </div>
        </div>
        <div class="product-card">
          <div class="product-card__content-container">
            <div class="product-card--image">
              <img src="~/assets/images/products/cards/bitmap6.png" />
            </div>
            <div class="product-card--text">
              <p>Saffola Oats</p>
            </div>
          </div>
        </div>
      </Slick>
    </section>
    <section class="features" id="features">
      <div class="features__container">
        <div class="features__left-part">
          <h2 class="features__heading">Delicious and healthy too!</h2>
          <div class="features__left-part--icons-container">
            <div class="features__column">
              <div class="feature__item">
                <div class="feature__item--image">
                  <img
                    src="~/assets/images/features/oats.svg"
                    class="feature-image img-responsive img-fluid"
                  />
                  <h4 class="feature-text">100%<br />wholegrain oats</h4>
                </div>
              </div>
              <div class="feature__item">
                <div class="feature__item--image">
                  <img
                    src="~/assets/images/features/hi-fiber.svg"
                    class="feature-image img-responsive img-fluid"
                  />
                  <h4 class="feature-text">100%<br />wholegrain oats</h4>
                </div>
              </div>
            </div>
            <div class="features__column">
              <div class="feature__item">
                <div class="feature__item--image">
                  <img
                    src="~/assets/images/features/vegetable.svg"
                    class="feature-image img-responsive img-fluid"
                  />
                  <h4 class="feature-text">Real<br />Vegetables*</h4>
                </div>
              </div>
              <div class="feature__item">
                <div class="feature__item--image">
                  <img
                    src="~/assets/images/features/weight.svg"
                    class="feature-image img-responsive img-fluid"
                  />
                  <h4 class="feature-text">Upto 70%<br />less fat***</h4>
                </div>
              </div>
            </div>
            <div class="features__column">
              <div class="feature__item">
                <div class="feature__item--image">
                  <img
                    src="~/assets/images/features/no-additives.svg"
                    class="feature-image img-responsive img-fluid"
                  />
                  <h4 class="feature-text">No added<br />preservatives</h4>
                </div>
              </div>
              <div class="feature__item">
                <div class="feature__item--image">
                  <img
                    src="~/assets/images/features/clock.svg"
                    class="feature-image img-responsive img-fluid"
                  />
                  <h4 class="feature-text">Ready in<br />3 minutes</h4>
                </div>
              </div>
            </div>
          </div>
          <div class="disclaimer-container">
            <h6 class="features__disclaimer-text">
              *Vegetables are dehydrated to maintain its goodness and taste.
            </h6>
            <h6 class="features__disclaimer-text">
              **Oats have beta- glucan fiber that keeps you fuller for longer
            </h6>
            <h6 class="features__disclaimer-text">
              ***Study dated 31/08/17 based on declared nutrient information of
              instant noodles vs Saffola Masala Oats.
            </h6>
          </div>
        </div>
        <div class="features__right-part">
          <picture>
            <source
              srcset="~/assets/images/features/mobile/img.png"
              media="(max-width: 600px)"
              class="img-responsve img-fluid"
            />
            <source
              srcset="~/assets/images/features/tablet/img.png"
              media="(max-width: 992px)"
              class="img-reponsive img-fluid"
            />
            <img
              src="~/assets/images/features/img.png"
              class="img-reponsive img-fluid features__right-part--image"
            />
          </picture>
        </div>
      </div>
    </section>
    <section class="steps" id="steps">
      <h2 class="steps__heading">Easy to cook, easy to serve!</h2>
      <div class="steps__container">
        <div class="step">
          <div class="step--image">
            <picture>
              <source
                srcset="~/assets/images/steps/mobile/step-1.png"
                media="(max-width: 767px)"
              />
              <img src="~/assets/images/steps/step-1.png" />
            </picture>
          </div>
          <p class="step--text">
            For every cup of Saffola Oats, add 1 ½ cups of water in a pan
          </p>
        </div>
        <div class="arrow">
          <picture>
            <source
              srcset="~/assets/images/steps/mobile/arrow-1.svg"
              media="(max-width: 600px)"
            />
            <img src="~/assets/images/steps/arrow-1.svg" class="arrow__image" />
          </picture>
        </div>
        <div class="step">
          <div class="step--image">
            <picture>
              <source
                srcset="~/assets/images/steps/mobile/step-2.png"
                media="(max-width: 767px)"
              />
              <img src="~/assets/images/steps/step-2.png" />
            </picture>
          </div>
          <p class="step--text">
            Cook on medium flame for 3 minutes or microwave for 3 minutes on
            full power. Stir occasionally
          </p>
        </div>
        <div class="arrow">
          <picture>
            <source
              srcset="~/assets/images/steps/mobile/arrow-2.svg"
              media="(max-width: 600px)"
            />
            <img src="~/assets/images/steps/arrow-2.svg" class="arrow__image" />
          </picture>
        </div>
        <div class="step">
          <div class="step--image">
            <picture>
              <source
                srcset="~/assets/images/steps/mobile/step-3.png"
                media="(max-width: 767px)"
              />
              <img src="~/assets/images/steps/step-3.png" />
            </picture>
          </div>
          <p class="step--text">
            Serve hot to enjoy the distinct flavours. Garnish with veggies,
            herbs and choice of toppings.
          </p>
        </div>
      </div>
    </section>
    <div class="section-divider--bottom"></div>
    <section class="recipes" id="recipes">
      <h2 class="recipes__heading">Steaming Yummy Recipes with Saffola Oats</h2>
      <ul class="nav" id="cuisines" role="tablist">
        <li class="nav-item">
          <a
            class="nav-link active recipes__cuisines"
            id="indian-tab"
            data-toggle="tab"
            href="#indian"
            role="tab"
            aria-controls="indian"
            aria-selected="true"
            >Indian</a
          >
        </li>
        <li class="nav-item">
          <a
            class="nav-link recipes__cuisines"
            id="italian-tab"
            data-toggle="tab"
            href="#italian"
            role="tab"
            aria-controls="italian"
            aria-selected="false"
            >Italian/Chinese</a
          >
        </li>
        <li class="nav-item">
          <a
            class="nav-link recipes__cuisines"
            id="continental-tab"
            data-toggle="tab"
            href="#continental"
            role="tab"
            aria-controls="contitnental"
            aria-selected="false"
            >Continental</a
          >
        </li>
        <li class="nav-item">
          <a
            class="nav-link recipes__cuisines"
            id="more-tab"
            href="http://fitfoodie.in/"
            target="_blank"
            >More Recipes
            <span> <img src="~/assets/images/recipes/next.svg" /> </span
          ></a>
        </li>
      </ul>
      <div class="tab-content" id="recipes-tabs">
        <div
          class="tab-pane fade show active"
          id="indian"
          role="tabpanel"
          aria-labelledby="indian-tab"
        >
          <VueSlickCarousel v-bind="recipesSettings" class="recipes-carousel">
            <div
              v-for="recipe in indianRecipes"
              class="recipe"
              :key="recipe.id"
            >
              <div class="recipe-container">
                <div class="recipe__image-container">
                  <img
                    :src="
                      require(`~/assets/images/recipes/indian/${recipe.recipeImage}.png`)
                    "
                  />
                </div>
                <div class="recipe__text-container">
                  <h3 class="recipe--title">
                    {{ recipe.title }}
                  </h3>
                  <div class="recipe__details-container">
                    <div class="recipe__serving">
                      <img
                        src="~/assets/images/recipes/food.svg"
                        class="recipe__serving--image"
                      />
                      <p class="recipe__serving--text">{{ recipe.serving }}</p>
                    </div>
                    <div class="recipe__cooking-time">
                      <img
                        src="~/assets/images/recipes/chronometer.svg"
                        class="recipe__cooking-time--image"
                      />
                      <p class="recipe__cooking-time--text">
                        {{ recipe.cookingTime }}
                      </p>
                    </div>
                  </div>
                </div>
                <div
                  class="recipe-open__image-container"
                  @click="activateRecipe(recipe.id)"
                >
                  <img
                    src="~/assets/images/recipes/up-arrow.svg"
                    class="recipe__open-image img-responsive img-fluid"
                  />
                </div>
                <div
                  class="recipe__method-container"
                  :class="addRecipeActiveClass(recipe.id)"
                >
                  <h5 class="recipe__method--heading">Ingredients:</h5>
                  <p
                    class="recipe__method--sub-text"
                    v-for="ingredients in recipe.recipeIngredients"
                    :key="ingredients"
                  >
                    {{ ingredients }}
                  </p>
                  <h5 class="recipe__method--heading">Method:</h5>
                  <p
                    class="recipe__method--sub-text"
                    v-for="methods in recipe.recipeMethods"
                    :key="methods"
                  >
                    {{ methods }}
                  </p>
                  <div
                    class="recipe-close__image-container"
                    @click="deactivateRecipe(recipe.id)"
                  >
                    <img
                      src="~/assets/images/recipes/close.svg"
                      class="recipe__close-image img-responsive img-fluid"
                    />
                  </div>
                </div>
              </div>
            </div>
          </VueSlickCarousel>
        </div>
        <div
          class="tab-pane fade"
          id="italian"
          role="tabpanel"
          aria-labelledby="italian-tab"
        >
          <VueSlickCarousel v-bind="recipesSettings" class="recipes-carousel">
            <div
              v-for="recipe in italianRecipes"
              class="recipe"
              :key="recipe.id"
            >
              <div class="recipe-container">
                <div class="recipe__image-container">
                  <img
                    :src="
                      require(`~/assets/images/recipes/italian/${recipe.recipeImage}.png`)
                    "
                  />
                </div>
                <div class="recipe__text-container">
                  <h3 class="recipe--title">
                    {{ recipe.title }}
                  </h3>
                  <div class="recipe__details-container">
                    <div class="recipe__serving">
                      <img
                        src="~/assets/images/recipes/food.svg"
                        class="recipe__serving--image"
                      />
                      <p class="recipe__serving--text">{{ recipe.serving }}</p>
                    </div>
                    <div class="recipe__cooking-time">
                      <img
                        src="~/assets/images/recipes/chronometer.svg"
                        class="recipe__cooking-time--image"
                      />
                      <p class="recipe__cooking-time--text">
                        {{ recipe.cookingTime }}
                      </p>
                    </div>
                  </div>
                </div>
                <div
                  class="recipe-open__image-container"
                  @click="activateRecipe(recipe.id)"
                >
                  <img
                    src="~/assets/images/recipes/up-arrow.svg"
                    class="recipe__open-image img-responsive img-fluid"
                  />
                </div>
                <div
                  class="recipe__method-container"
                  :class="addRecipeActiveClass(recipe.id)"
                >
                  <h5 class="recipe__method--heading">Ingredients:</h5>
                  <p
                    class="recipe__method--sub-text"
                    v-for="ingredients in recipe.recipeIngredients"
                    :key="ingredients"
                  >
                    {{ ingredients }}
                  </p>
                  <h5 class="recipe__method--heading">Method:</h5>
                  <p
                    class="recipe__method--sub-text"
                    v-for="methods in recipe.recipeMethods"
                    :key="methods"
                  >
                    {{ methods }}
                  </p>
                  <div
                    class="recipe-close__image-container"
                    @click="deactivateRecipe(recipe.id)"
                  >
                    <img
                      src="~/assets/images/recipes/close.svg"
                      class="recipe__close-image img-responsive img-fluid"
                    />
                  </div>
                </div>
              </div>
            </div>
          </VueSlickCarousel>
        </div>
        <div
          class="tab-pane fade"
          id="continental"
          role="tabpanel"
          aria-labelledby="continental-tab"
        >
          <VueSlickCarousel v-bind="recipesSettings" class="recipes-carousel">
            <div
              v-for="recipe in continentalRecipes"
              class="recipe"
              :key="recipe.id"
            >
              <div class="recipe-container">
                <div class="recipe__image-container">
                  <img
                    :src="
                      require(`~/assets/images/recipes/continental/${recipe.recipeImage}.png`)
                    "
                  />
                </div>
                <div class="recipe__text-container">
                  <h3 class="recipe--title">
                    {{ recipe.title }}
                  </h3>
                  <div class="recipe__details-container">
                    <div class="recipe__serving">
                      <img
                        src="~/assets/images/recipes/food.svg"
                        class="recipe__serving--image"
                      />
                      <p class="recipe__serving--text">{{ recipe.serving }}</p>
                    </div>
                    <div class="recipe__cooking-time">
                      <img
                        src="~/assets/images/recipes/chronometer.svg"
                        class="recipe__cooking-time--image"
                      />
                      <p class="recipe__cooking-time--text">
                        {{ recipe.cookingTime }}
                      </p>
                    </div>
                  </div>
                </div>
                <div
                  class="recipe-open__image-container"
                  @click="activateRecipe(recipe.id)"
                >
                  <img
                    src="~/assets/images/recipes/up-arrow.svg"
                    class="recipe__open-image img-responsive img-fluid"
                  />
                </div>
                <div
                  class="recipe__method-container"
                  :class="addRecipeActiveClass(recipe.id)"
                >
                  <h5 class="recipe__method--heading">Ingredients:</h5>
                  <p
                    class="recipe__method--sub-text"
                    v-for="ingredients in recipe.recipeIngredients"
                    :key="ingredients"
                  >
                    {{ ingredients }}
                  </p>
                  <h5 class="recipe__method--heading">Method:</h5>
                  <p
                    class="recipe__method--sub-text"
                    v-for="methods in recipe.recipeMethods"
                    :key="methods"
                  >
                    {{ methods }}
                  </p>
                  <div
                    class="recipe-close__image-container"
                    @click="deactivateRecipe(recipe.id)"
                  >
                    <img
                      src="~/assets/images/recipes/close.svg"
                      class="recipe__close-image img-responsive img-fluid"
                    />
                  </div>
                </div>
              </div>
            </div>
          </VueSlickCarousel>
        </div>
      </div>
    </section>
    <section class="testimonials" id="testimonials">
      <h2 class="testimonials__heading">From one foodie to another</h2>
      <VueSlickCarousel
        v-bind="testimonialsSettings"
        class="testimonial-carousel"
      >
        <div class="testimonial">
          <div class="testimonail__image-container">
            <img
              src="~/assets/images/testimonials/doubleQuotes.svg"
              class="testimonial__image"
            />
          </div>
          <div class="testimonial__text">
            <p class="testimonial__text--main">
              Saffola Masala Oats is a good option to increase the fiber content
              in your food and minimize carbohydrates in your diet.
            </p>
            <hr class="testimonial__horizontal-line" />
            <h4 class="testimonial__author--name">Jane Doe</h4>
            <h6 class="testimonial__author--designation">Student</h6>
          </div>
        </div>
        <div class="testimonial">
          <div class="testimonail__image-container">
            <img
              src="~/assets/images/testimonials/doubleQuotes.svg"
              class="testimonial__image"
            />
          </div>
          <div class="testimonial__text">
            <p class="testimonial__text--main">
              Saffola Masala Oats is a good option to increase the fiber content
              in your food and minimize carbohydrates in your diet.
            </p>
            <hr class="testimonial__horizontal-line" />
            <h4 class="testimonial__author--name">Jane Doe</h4>
            <h6 class="testimonial__author--designation">Student</h6>
          </div>
        </div>
        <div class="testimonial">
          <div class="testimonail__image-container">
            <img
              src="~/assets/images/testimonials/doubleQuotes.svg"
              class="testimonial__image"
            />
          </div>
          <div class="testimonial__text">
            <p class="testimonial__text--main">
              Saffola Masala Oats is a good option to increase the fiber content
              in your food and minimize carbohydrates in your diet.
            </p>
            <hr class="testimonial__horizontal-line" />
            <h4 class="testimonial__author--name">Jane Doe</h4>
            <h6 class="testimonial__author--designation">Student</h6>
          </div>
        </div>
        <div class="testimonial">
          <div class="testimonail__image-container">
            <img
              src="~/assets/images/testimonials/doubleQuotes.svg"
              class="testimonial__image"
            />
          </div>
          <div class="testimonial__text">
            <p class="testimonial__text--main">
              Saffola Masala Oats is a good option to increase the fiber content
              in your food and minimize carbohydrates in your diet.
            </p>
            <hr class="testimonial__horizontal-line" />
            <h4 class="testimonial__author--name">Jane Doe</h4>
            <h6 class="testimonial__author--designation">Student</h6>
          </div>
        </div>
      </VueSlickCarousel>
    </section>
    <footer class="footer">
      <div class="social-media-container">
        <div class="social-media__left-part">
          <h2 class="social-media__left-part--white">Follow us</h2>
          <h2 class="social-media__left-part--yellow">@saffolafitfoodie</h2>
        </div>
        <div class="social-media__right-part">
          <span class="social-media-icons">
            <img src="~/assets/images/footer/facebook.svg" />
          </span>
          <span class="social-media-icons">
            <img src="~/assets/images/footer/instagram.svg" />
          </span>
          <span class="social-media-icons">
            <img src="~/assets/images/footer/youtube.svg" />
          </span>
        </div>
      </div>
      <div class="instagram-feed">
        <h2>Instagram feed</h2>
      </div>
      <div class="footer-bottom-container">
        <div class="footer-bottom__left-part">
          <div class="footer-bottom__left-part--mail">
            <span class="footer-bottom__left-part--mail-image">
              <img src="~/assets/images/footer/mail.svg" />
            </span>
            <span class="footer-bottom__left-part--mail-text">
              csc@marico.com
            </span>
          </div>
          <div class="footer-bottom__left-part--phone">
            <span class="footer-bottom__left-part--phone-image">
              <img src="~/assets/images/footer/phone.svg" />
            </span>
            <span class="footer-bottom__left-part--phone-image"
              >1800 - 2345 - 3445</span
            >
          </div>
        </div>
        <div class="footer-bottom__right-part">
          <div class="footer-bottom__right-part--text">
            Terms & Conditions &nbsp;|&nbsp;&nbsp;Privacy Policy
            &nbsp;|&nbsp;&nbsp;© 2021 Saffola. All Rights Reserved
          </div>
        </div>
      </div>
    </footer>
  </div>
</template>

<script>
import VueSlickCarousel from "vue-slick-carousel";
import Slick from "vue-slick";
import "slick-carousel/slick/slick.css";
import "slick-carousel/slick/slick-theme.css";
import "vue-slick-carousel/dist/vue-slick-carousel.css";
import "vue-slick-carousel/dist/vue-slick-carousel-theme.css";
export default {
  head: {
    meta: [
      { charset: "utf-8" },
      {
        name: "viewport",
        content:
          "width=device-width, initial-scale=1.0, maximum-scale=1.0,user-scalable=0",
      },
    ],
    link: [
      {
        href:
          "https://maxcdn.bootstrapcdn.com/bootstrap/3.4.1/css/bootstrap.min.css",
        rel: "stlyesheet",
      },
    ],
    script: [
      { src: "https://use.fontawesome.com/2c3e198de1.js" },
      {
        src: "https://code.jquery.com/jquery-3.2.1.slim.min.js",
        integrity:
          "sha384-KJ3o2DKtIkvYIK3UENzmM7KCkRr/rE9/Qpg6aAZGJwFDMVNA/GpGFF93hXpG5KkN",
        crossorigin: "anonymous",
      },
      {
        src:
          "https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.12.9/umd/popper.min.js",
        integrity:
          "sha384-ApNbgh9B+Y1QKtv3Rn7W3mgPxhU9K/ScQsAP7hUibX39j7fakFPskvXusvfa0b4Q",
        crossorigin: "anonymous",
      },
      {
        src:
          "https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0/js/bootstrap.min.js",
        integrity:
          "sha384-JZR6Spejh4U02d8jOt6vLEHfe/JQGiRRSQQxSfFWpi1MquVdAyjUar5+76PVCmYl",
        crossorigin: "anonymous",
      },
    ],
  },
  methods: {
    openBuyNowSection(variant) {
      if (variant == "desktop") {
        var buyNowSectionDesktop = document.getElementById(
          "buy-now__section--desktop"
        );
        if (buyNowSectionDesktop.classList.contains("buy-now__section--hide")) {
          buyNowSectionDesktop.classList.remove("buy-now__section--hide");
          buyNowSectionDesktop.classList.add("buy-now__section--show");
          return;
        }
        if (buyNowSectionDesktop.classList.contains("buy-now__section--show")) {
          buyNowSectionDesktop.classList.remove("buy-now__section--show");
          buyNowSectionDesktop.classList.add("buy-now__section--hide");
        }
      } else {
        var buyNowSectionMobile = document.getElementById(
          "buy-now__section--mobile"
        );
        if (buyNowSectionMobile.classList.contains("buy-now__section--hide")) {
          buyNowSectionMobile.classList.remove("buy-now__section--hide");
          buyNowSectionMobile.classList.add("buy-now__section--show");
          return;
        }
        if (buyNowSectionMobile.classList.contains("buy-now__section--show")) {
          buyNowSectionMobile.classList.remove("buy-now__section--show");
          buyNowSectionMobile.classList.add("buy-now__section--hide");
        }
      }
    },

    handleScroll() {
      var navbar = document.getElementById("navigation");
      var hamburgerMenu = document.getElementById("hamburger__menu");
      var hamburgerMenuYellow = document.getElementById(
        "hamburger__menu--yellow"
      );
      var backToTop = document.getElementById("back-to-top__container");

      if (window.scrollY > 800) {
        backToTop.classList.remove("back-to-top__container--hide");
        backToTop.classList.add("back-to-top__container--show");
      } else {
        backToTop.classList.remove("back-to-top__container--show");
        backToTop.classList.add("back-to-top__container--hide");
      }

      if (window.scrollY > 10) {
        navbar.classList.add("navigation-red");
        hamburgerMenu.classList.remove("show");
        hamburgerMenu.classList.add("removeClass");
        hamburgerMenuYellow.classList.add("show");
      } else {
        navbar.classList.remove("navigation-red");
        hamburgerMenu.classList.add("show");
        hamburgerMenuYellow.classList.remove("show");
        hamburgerMenuYellow.classList.add("removeClass");
      }
    },
    openMobileNavigation() {
      this.showNavBar = !this.showNavBar;
      var backToTop = document.getElementById("back-to-top__container");
      backToTop.classList.remove("back-to-top__container--show");
      this.showBottomBuyNow = false;
    },

    closeMobileNavigation() {
      this.showNavBar = false;
      var backToTop = document.getElementById("back-to-top__container");
      backToTop.classList.add("back-to-top__container--show");
      this.showBottomBuyNow = true;
    },

    activateRecipe(id) {
      this[id] = true;
    },
    deactivateRecipe(id) {
      this[id] = false;
    },
    addRecipeActiveClass(id) {
      if (this[id]) {
        return "active";
      } else {
        return "";
      }
    },
  },
  data() {
    return {
      showNavBar: false,
      showBottomBuyNow: true,
      indianRecipes: [
        {
          cuisine: "indian",
          id: "indianRecipe1Active",
          recipeImage: "img1",
          title: "Peppy Tomato Oats Crumb Fried Chicken",
          serving: "3-4",
          cookingTime: "20 min",
          recipeIngredients: [
            "Saffola masala peppy tomato oats - 1 packet",
            "Saffola Oil - 3 tablespoons",
            "40 grams plain nonfat corn flakes",
            "Eggs - 2",
            "25 grams grated parmesan cheese",
            "Homemade green chutney - 3 tablespoons",
            "Whole wheat Flour - ½ cup",
            "700 grams boneless chicken breast fillets (3 chicken breasts x 2 fillets each)",
          ],
          recipeMethods: [
            "1. Place chicken fillets into a zip lock bag and pound gently until thin.",
            "2. In a flattish deep-dish whisk the eggs and chutney with a fork",
            "3. Put Saffola masala oats, corn flakes, walnuts, and cheese in a processor to get a coarse mix",
            "4. Place wheat flour, egg mixture and half oats in three separate dishes. Take one fillet at a time to coat them and deep fry in 1 tablespoon of oil at a time, and serve hot",
          ],
        },
        {
          cuisine: "indian",
          id: "indianRecipe2Active",
          recipeImage: "img2",
          title: "Masaledar Oats Tikki",
          serving: "4",
          cookingTime: "30 min",
          recipeIngredients: [
            "Saffola CLASSIC MASALA OATS - 1/2 packet + 1/4 packet",
            "YELLOW MOONG DAL - 1/3 CUP",
            "ONION & CARROT - 1 each",
            "GARAM MASALA & Red Chilli Powder - 1/4 TSP",
            "CORIANDER LEAVES - FEW",
          ],
          recipeMethods: [
            "1. Dry roast the 1/2 cup of masala Oats in a pan for 5 minutes, without burning it. Once cooled, grind it into a fine powder.",
            "2. Soak dal for 10 minutes in water and cook in open flame till it becomes soft. Drain the excess water and allow this to cool. Grind the moong dal coarsely without adding any water.",
            "3. Put this in a wide bowl and add the oats powder, veggies, spices and salt. Mix well to make small tikkis.",
          ],
        },
        {
          cuisine: "indian",
          id: "indianRecipe3Active",
          recipeImage: "img3",
          title: "Peppy Tomato Vegetable Roll",
          serving: "2",
          cookingTime: "20 min",
          recipeIngredients: [
            "Saffola Peppy Tomato Oats – 40 g",
            "Saffola Active oil – 2 tsp 5 ml",
            "Cumin seeds – 1 tsp 2 g",
            "Carrot – ½ cup 100 g",
            "Capsicum & Onion – ½ cup 50 g each",
            "Salt & Black pepper - ½ tsp 1g each",
            "Spinach Tortilla - 2 100 g",
          ],
          recipeMethods: [
            "1. Follow the directions to cook Saffola Peppy Tomato Oats and set aside to cool",
            "2. Heat Saffola Active Oil in a pan and add cumin seeds, capsicum, onion, salt to taste, and black pepper. Cook for 3-4 minutes on a low flame",
            "3. Keep a spinach tortilla on a plate and add some vegetable filling in the centre to make a tight roll.",
            "4. Spread oats on top and serve hot with a dip of your choice.",
          ],
        },
        {
          cuisine: "indian",
          id: "indianRecipe4Active",
          recipeImage: "img4",
          title: "Classic Masala Oats Chicken Curry",
          serving: "2",
          cookingTime: "30 min",
          recipeIngredients: [
            "1 cup chopped chicken breast",
            "2 tsp each chopped garlic & ginger",
            "1 tsp garam masala",
            "Salt to taste",
            "1 tbsp lemon juice",
            "1 tbsp Saffola oil",
            "1/2 cup sliced onions",
          ],
          recipeMethods: [
            "1. Add chicken, garlic, ginger, garam masala, salt, lemon juice to a bowl and mix it well. Add Saffola Masala Oats Classic Masala to the mixture and combine well",
            "2. Heat oil in a pan and sauté the onions till they are translucent. Add green chillies and the marinated chicken and mix well",
            "3. Add tomatoes, tomato puree, and chicken stock and cook with the lid on for 3-4 mins. Layer it with capsicum and cook for 1-2 minutes more to prepare your Classic Masala Oats Chicken Curry!",
          ],
        },
      ],
      italianRecipes: [
        {
          cuisine: "italian",
          id: "italianRecipe1Active",
          recipeImage: "img1",
          title: "Spring Rolls",
          serving: "4",
          cookingTime: "30 min",
          recipeIngredients: [
            "Spring roll wrappers - 10",
            "Onion thinly sliced 50 gms",
            "Spring onions thinly sliced 100 gms",
            "Carrots cut into thin strips - 2",
            "Green capsicum cut into thin strips - 1",
            "Cabbage finely shredded 75 gms",
            "Saffola Oil 1 tbsp",
            "White pepper powder 1/4 teaspoon",
            "Soy sauce 1 tablespoon",
            "Bean sprouts 40 gms",
            "Spring onion greens chopped2 stalks",
            "40 gms Classic Masala Oats",
            "Salt to taste",
          ],
          recipeMethods: [
            "1. Heat 2 tbsps oil in a non-stick wok. Add onion, spring onions, carrots, capsicum, cabbage, and salt, and toss.",
            "2. Add pepper powder, soy sauce, bean sprouts, and spring onion greens and mix. Add SMO oats and cook till the vegetables soften. Set aside to cool",
            "3. Spread the spring roll wrappers on the wok top. Divide the stuffing into 10 portions and place a portion on one side of each wrapper. Fold in the edges and roll tightly.",
            "4. Apply cornflour paste to the open-end and seal. Keep the rolls under a damp cloth.",
            "5. Shallow fry till golden and crisp. Serve hot.",
          ],
        },
        {
          cuisine: "italian",
          id: "italianRecipe2Active",
          recipeImage: "img2",
          title: "Peppy Tomato Oats Pasta in Pink Sauce",
          serving: "4",
          cookingTime: "30 min",
          recipeIngredients: [
            "200 grams whole wheat penne pasta (cooked)",
            "1/2 teaspoon Saffola oil",
            "1/4 onion, diced",
            "1/2 clove garlic, minced",
            "4 tablespoon tomato puree",
            "1 basil leaf",
            "1/8 teaspoon dried oregano & back pepper each",
            "1/4 teaspoon salt",
            "1 Packet Saffola masala peppy tomato oats",
            "200 ml low-fat milk",
          ],
          recipeMethods: [
            "1. Boil penne pasta in water for 15 minutes. Cut a piece to check if it’s cooked properly.",
            "2. Combine Saffola Masala peppy tomato oats and milk to cook for 3-5 minutes. Blend together to make a creamy puree",
            "3. In a saucepan, sauté onion and garlic in olive oil over medium heat. Add tomato puree, basil, oregano, salt, and pepper. Stir in oats puree and simmer for 5 minutes",
            "4. Toss the sauce with penne, garnish with basil leaves and serve",
          ],
        },
        {
          cuisine: "italian",
          id: "italianRecipe3Active",
          recipeImage: "img3",
          title: "Veggie Twist Momos",
          serving: "2-4",
          cookingTime: "80 min",
          recipeIngredients: [
            "1 cup whole wheat & finger millet flour (Ragi ka atta)",
            "¼ teaspoon salt",
            "2 tablespoon curd",
            "Water as needed",
            "2 teaspoon Saffola oil",
            "1/2 cup chopped button mushrooms",
            "1 Packet Saffola Masala Oats Veggie Twist",
            "1 spring onion greens",
            "1 teaspoon black pepper powder",
            "1 tablespoon chopped cabbage, carrots, and red bell pepper",
          ],
          recipeMethods: [
            "1. In a mixing bowl add wheat flour, finger millet flour (Ragi ka atta), salt, curd, water and make a dough. Rest the dough for 1 hour",
            "2. Heat oil in a pan. Add red bell peppers, button mushrooms, Saffola Masala Oats Veggie Twist, spring onions, and black pepper powder cook for 4-5 minutes. Add chopped cabbage, carrots and cook for 1-2 minutes",
            "3. Roll the dough into small discs and stuff it with the filling. Place it in the momos basket and steam it for 6 to 7 minutes.",
          ],
        },
        {
          cuisine: "italian",
          id: "italianRecipe4Active",
          recipeImage: "img4",
          title: "Veggie Twist Oats Chicken Meatball Soup",
          serving: "2",
          cookingTime: "20 min",
          recipeIngredients: [
            "400 gm Ground chicken",
            "3/4 Cup Saffola Masala Oats Veggie Twist",
            "2 Tablespoon lite soy sauce",
            "1 Tablespoon dry vinegar & Saffola Oil",
            "1-1/2 teaspoon minced fresh ginger",
            "1/2 Teaspoon Black pepper",
            "1/4 cup chicken broth",
            "1 cup chicken broth & water",
            "1 1/2 Cup Green Peas",
            "1 cup thinly sliced carrots",
            "1-1/2 Cup bean sprouts",
            "1/4 cup thinly sliced spring onions",
          ],
          recipeMethods: [
            "1. Spray rack of broiler pan with cooking oil.",
            "2. In a large bowl, combine meatball ingredients and mix thoroughly. Shape into 1-inch meatballs and place on the rack of broiler pan",
            "3. Broil 6 to 8 inches from heat 7 to 10 minutes or until cooked through.",
            "4. In a saucepan, combine meatballs with chicken broth and water and bring to a boil. Add pea pods, carrots, bean sprouts, and green onions and cook properly. Serve immediately",
          ],
        },
      ],
      continentalRecipes: [
        {
          cuisine: "continental",
          id: "continentalRecipe1Active",
          recipeImage: "img1",
          title: "Chickpea Zucchini Cakes",
          serving: "4",
          cookingTime: "30 min",
          recipeIngredients: [
            "Saffola Aura - Refined Olive [for cooking & brushing]",
            "Chickpeas – 1 cup",
            "Zucchini – 1 cup ( Grated )",
            "Fresh parsley – 2 tbsp ( Chopped )",
            "Cumin powder – ½ tsp",
            "Salt to taste",
            "Garlic – 2-3 cloves ( Finely chopped )",
          ],
          recipeMethods: [
            "1. Soak some washed chickpeas in 4 cups of water for 5-6 water.",
            "2. Drain the water and pressure-cook the chickpeas until cooked. Keep separate. Add grated zucchini, parsley, cumin powder, salt, and garlic.",
            "3. Mix well and make small cakes. Preheat the oven to 180 degrees C. Arrange the cakes on a baking tray and brush them with Saffola Oil.",
            "4. Bake for 15-20 mins. Flip the sides and bake again for 10-12 mins. Serve hot.",
          ],
        },
        {
          cuisine: "continental",
          id: "continentalRecipe2Active",
          recipeImage: "img2",
          title: "Cottage Cheese Balls",
          serving: "3",
          cookingTime: "30 min",
          recipeIngredients: [
            "Cottage Cheese sourced from 1 litre fat-free milk",
            "Saffola masala oats curry & pepper - 1 packet",
            "Red onion & fresh coriander - 1 (finely chopped)",
            "Green chili - 1 (finely chopped)",
            "Saffola oil (1/2 teaspoon per ball)",
            "Pancake puff pan",
          ],
          recipeMethods: [
            "1. Cook Curry and Pepper masala oats and bring them to room temperature",
            "2. In a large bowl, add cottage cheese, coriander, chilies, and cooked curry and pepper oats, mix well. Make balls of this mixture big enough to fit the pancake puff pan.",
            "3. Roll the balls evenly in dried oats and carefully put the cheese balls, cooking them on a pancake puff pan on medium-low flame.",
            "4. Cook consistently until you achieve an even golden brown colour. Serve hot with tomato basil sauce",
          ],
        },
        {
          cuisine: "continental",
          id: "continentalRecipe3Active",
          recipeImage: "img3",
          title: "Grilled Tofu Spinach Sandwich",
          serving: "3",
          cookingTime: "30 min",
          recipeIngredients: [
            "Tofu or Paneer - 1 packet",
            "Sesame seeds (mustard) - 1/4 cup",
            "Dijon Mustard & Olive Oil - 1 tablespoon each",
            "Whole wheat bread - 4 slices (toasted)",
            "Tomato - 1 (sliced)",
            "Onion - ½ (sliced/ringed)",
            "Spinach leaves - a handful",
            "Salt to taste & Tabasco sauce - for added flavour",
          ],
          recipeMethods: [
            "1. In a large bowl, combine olive oil, dijon mustard, and a pinch of salt. Toss the tofu in the mustard and allow it to rest for 30 minutes to marinate or place in the refrigerator for 3 hours",
            "2. Preheat an iron grill on medium heat and toss the tofu with sesame seeds and place it on the grill",
            "3. In a toaster, simultaneously toast each of the bread slices until lightly browned and crisp. Proceed to evenly place the tomato slices, onion, and spinach on the bread slices.",
            "4. Add the grilled tofu and drizzle some Tabasco sauce and dijon mustard on the sandwich. Serve warm",
          ],
        },
        {
          cuisine: "continental",
          id: "continentalRecipe4Active",
          recipeImage: "img4",
          title: "Strawberry Smoothie Bowl",
          serving: "1",
          cookingTime: "50 min",
          recipeIngredients: [
            "Saffola Oats - 2 tablespoons",
            "Prunes - 3 (finely chopped)",
            "Almonds - 1 tablespoon (finely chopped)1 tablespoon almonds, finely chopped",
            "Honey - 1 teaspoon",
            "Low-fat yogurt - 1 cup",
            "Saffola Multigrain Flakes - Nutty Crunch - 3 tablespoons",
            "Strawberries - 5 (chopped)",
            "Chia Seeds - 1 tablespoon1 tablespoon chia seeds",
          ],
          recipeMethods: [
            "1. Cook oats, honey, and water in a saucepan for 5 mins. Allow it to cool a bit.",
            "2. Stir in the yogurt, prunes, and almonds and mix well. Transfer the smoothie to a serving bowl. Refrigerate this for a few hours so you can have a chilled smoothie bowl.",
            "3. Top it up with some chopped strawberries, multigrain flakes, and crunchy chia seeds",
          ],
        },
      ],
      indianRecipe1Active: false,
      indianRecipe2Active: false,
      indianRecipe3Active: false,
      indianRecipe4Active: false,
      italianRecipe1Active: false,
      italianRecipe2Active: false,
      italianRecipe3Active: false,
      italianRecipe4Active: false,
      continentalRecipe1Active: false,
      continentalRecipe2Active: false,
      continentalRecipe3Active: false,
      continentalRecipe4Active: false,
      testimonialsSettings: {
        infinite: false,
        slidesToShow: 3,
        arrow: true,
        speed: 500,
        slideToScroll: 1,
        responsive: [
          {
            breakpoint: 992,
            settings: {
              slidesToShow: 2,
            },
          },
          {
            breakpoint: 767,
            settings: {
              slidesToShow: 1,
            },
          },
        ],
      },

      recipesSettings: {
        infinite: false,
        slidesToShow: 3,
        arrows: true,
        speed: 500,
        slideToScroll: 1,
        responsive: [
          {
            breakpoint: 1400,
            settings: {
              slidesToShow: 2,
            },
          },

          {
            breakpoint: 992,
            settings: {
              slidesToShow: 2,
              arrows: false,
            },
          },
          {
            breakpoint: 767,
            settings: {
              slidesToShow: 1,
              arrows: false,
              dots: true,
            },
          },
        ],
      },
    };
  },
  components: {
    VueSlickCarousel,
    Slick,
  },
  beforeMount() {
    window.addEventListener("scroll", this.handleScroll);
  },
  computed: {
    productItemsSettings() {
      return {
        slidesToShow: 1,
        arrows: false,
        focusOnSelect: true,
      };
    },
    productCardsSettings() {
      return {
        asNavFor: "#productItems",
        focusOnSelect: true,
        speed: 500,
        arrows: true,
        slidesToScroll: 1,
        slidesToShow: 4,
        variableWidth: true,
        responsive: [
          {
            breakpoint: 1400,
            settings: {
              slidesToShow: 3,
            },
          },
          {
            breakpoint: 992,
            settings: {
              slidesToShow: 2,
              arrows: false,
            },
          },
          {
            breakpoint: 767,
            settings: {
              slidesToShow: 1,
              arrows: false,
            },
          },
        ],
      };
    },
  },
};
</script>
