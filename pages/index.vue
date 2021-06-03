<template>
    <div>
        <header>
            <input type="checkbox" class="nav-collapse" />
            <nav>
                <nuxt-link to="#">Home</nuxt-link>
                <nuxt-link to="#">Travel Information</nuxt-link>
                <nuxt-link to="#">Properties</nuxt-link>
                <nuxt-link to="#">Activities</nuxt-link>
                <nuxt-link to="#">About</nuxt-link>
                <nuxt-link to="#">Contact</nuxt-link>
                <nuxt-link to="#">Kauai</nuxt-link>
                <nuxt-link to="#">Long Term Rentals</nuxt-link>
            </nav>
            <nuxt-link to="/">
                <img
                    class="logo"
                    src="https://pure-kauai-hurleytechnologi.netdna-ssl.com/images/logo_new.png"
                    alt="Pure Kauai Logo"
                />
            </nuxt-link>
            <a href="tel:+1 866 457 7873">(866) 457-7873</a>
        </header>
        <main>
            <section class="banner-container">
                <img
                    src="https://pure-kauai-hurleytechnologi.netdna-ssl.com/cmsb/uploads/cave.jpg"
                    alt="Kauai Images"
                />
            </section>
            <section class="rentals-cta constrain">
                <h2>The finest luxury vacation homes on Kauai.</h2>
                <div>
                    <nuxt-link class="button-like" to="#"
                        >Short Term Rentals</nuxt-link
                    >
                    <nuxt-link class="button-like" to="#"
                        >Long Term Rentals</nuxt-link
                    >
                </div>
            </section>
            <section class="featured-properties">
                <h2>Featured Properties</h2>
                <section class="featured-properties-container">
                    <featured-property
                        src="https://pure-kauai-hurleytechnologi.netdna-ssl.com/cmsb/uploads/thumb2/hale-ae-kai-exterior-03.jpg"
                        to="#"
                        name="Hale ‘Ae Kai"
                        price="$14,000"
                        sleeps="8"
                        >A lush Balinese-inspired masterpiece on 15 acres, Hale
                        ‘Ae Kai is one of Kauai’s finest estates.
                    </featured-property>
                    <featured-property
                        src="https://pure-kauai-hurleytechnologi.netdna-ssl.com/cmsb/uploads/thumb2/secret-beach-hideaway-14.jpg"
                        to="#"
                        name="Secret Cove"
                        price="$4,250"
                        sleeps="8"
                        >Beauty and modernity meet in this standout oceanfront
                        home perched above Secret Beach.</featured-property
                    >
                </section>
            </section>
        </main>
        <footer>
            <section class="footer-contact">
                <img
                    class="logo"
                    src="https://pure-kauai-hurleytechnologi.netdna-ssl.com/images/logo_new_footer.png"
                    alt="Pure Kauai Logo"
                />
                <p>
                    Contact our on-island hosts to start planning your dream
                    vacation
                </p>
                <address>
                    <a href="tel:+1 866 457 7873">(866) 457-7873</a>
                    <a href="mailto:info@purekauai.com">info@purekauai.com</a>
                </address>
            </section>
            <section class="footer-social">
                <a href="https://www.facebook.com/purekauai/">Facebook</a>
                <a href="https://www.instagram.com/purekauai/">Instagram</a>
            </section>
            <section class="footer-copyright">
                Copyright &copy; 2021, Pure Hawaii Travel, LLC
            </section>
        </footer>
    </div>
</template>

<style>
@import url("https://fonts.googleapis.com/css2?family=Open+Sans&display=swap");

:root {
    --background: #fff;
    --background-dark: #f8f8ff;
    --background-darker: #dcdcdc;
    --foreground: #123;
    --foreground-light: #445;
    --primary-light: #0099ff;
    --primary: #035993;
    --primary-dark: #074772;
}

body {
    font-family: "Open Sans", sans-serif;
    font-size: 18px;
    margin: 0;
    color: var(--foreground);
}

/* Text and general styling */

h1,
h2,
h3,
h4,
h5,
h6 {
    font-weight: lighter;
    color: var(--primary);
    text-align: center;
    margin: 0;
    line-height: 1;
    margin-bottom: 1em;
}

a {
    transition: 0.15s;
    text-decoration: none;
    color: var(--primary);
}

a:hover {
    color: var(--primary-light);
}

button,
.button-like {
    background-color: var(--primary);
    color: var(--background);
    text-decoration: none;
    padding: 1rem;
    display: inline-block;
}

button:hover,
.button-like:hover {
    color: var(--background);
    cursor: pointer;
}

/* General layout */

.constrain {
    margin: 0 auto;
    max-width: 60rem;
}

main > section:not(:first-child) {
    padding: 3rem 0;
}

main > section:nth-child(odd) {
    background-color: var(--background-dark);
}

/* Page layout */

header {
    background-color: var(--background);
    display: flex;
    justify-content: space-between;
    align-items: center;
    position: sticky;
    top: 0;
    padding: 0 1rem;
}

header > * {
    display: block;
    flex-basis: 0;
    min-width: fit-content;
}

/* Closed / default nav */

.nav-collapse {
    transition: 0.5s;
    position: relative;
    left: 0;
    appearance: none;
    min-width: 2rem;
    height: 2rem;
    margin: auto 0;
    z-index: 2;
}

.nav-collapse::after {
	content: "";
	border-top: 4px solid var(--primary);
	border-bottom: 4px solid var(--primary);
	width: 100%;
	height: 16px;
	position: absolute;
	left: 50%;
	top: 50%;
	transform: translate(-50%, -50%);
	box-sizing: border-box;
}

nav {
    transition: 0.5s;
    transform: translateX(-100%);
    display: flex;
    flex-direction: column;
    padding: 4rem 2rem;
    width: 20rem;
    height: 100vh;
    overflow: hidden;
    position: fixed;
    top: 0;
    left: 0;
    background-color: inherit;
}

nav > a {
    transition: 0.15s;
    margin: 0.5rem;
    font-size: 1.5em;
    text-decoration: none;
    color: var(--foreground-light);
    border-bottom: 1px solid var(--background-darker);
}

nav > a:hover {
    color: var(--primary-light);
}

/* Open nav */

.nav-collapse:checked {
    left: 20rem;
}

.nav-collapse:checked + nav {
    transform: initial;
}

/* Banner */

.banner-container {
    height: 40rem;
    width: 100%;
    overflow: hidden;
}

.banner-container > img {
    width: 100%;
    height: 100%;
    object-fit: cover;
}

/* Rentals call to action */

.rentals-cta {
    text-align: center;
}

/* Featured properties */

.featured-properties-container {
    display: flex;
    justify-content: center;
}

.featured-property {
    flex-basis: 0;
}

/* Footer */

footer {
    background-color: var(--primary);
    text-align: center;
    color: var(--background);
}

footer > section {
    padding: 3rem 0;
}

.footer-contact {
    color: var(--primary-light);
}

.footer-social,
.footer-copyright {
    background-color: var(--primary-dark);
}

footer .logo {
    height: 4rem;
}

footer a {
    color: var(--background-dark);
}

footer address a {
    margin: 0 3rem;
}
</style>

<script>
export default {
    head() {
        return {
            title: "Pure Kauai - Luxury Island Vacation Rentals",
            meta: [
                {
                    name: "description",
                    content:
                        "Pure Kauai offers vacation rentals to ensure the very best in exclusive luxury travel. Choose from private homes, oceanfront villas, and beachfront estates.",
                },
            ],
        };
    },
};
</script>