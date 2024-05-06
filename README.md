<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Hari Dyes</title>
    <link rel="stylesheet" href="styles.css">
    <link href='https://unpkg.com/boxivons@2.1.1/css/boxicons.min.css' rel='stylesheet'>
</head>
<body>

<!-- Login Section -->
<section id="login">
    <div class="logo">
        <img src="https://mail-attachment.googleusercontent.com/attachment/u/1/?ui=2&ik=538c1ca84e&attid=0.1&permmsgid=msg-a:r-6816714388909896349&th=18ed22b5d8bf5409&view=att&disp=safe&saddbat=ANGjdJ-WJGSFoL2YuZG91PEhfmNibT4QlrA9GFm7SQSzTIkLKzmebSh5-2oy5eqprLg1tJUPu5Xl5m_2gYuiIGyVkZ1R4aR-USOQksVvEdglO-gLmbMMwQHCFTsd1wemHghDDmlUHHYYXRuOxbYJ9uF8SK26aYbylAPvYHFkLFWD-YOauVblfyJTUyZ0JPSnd8XfivfzyJUD7T3BqbJp6tCKZ90sZerMiQF4UBjXU0PSZMzZ13S9QWCziP7BHPmlRXAwgMerwE0YBv6UQX9LYGNIaxJdYgUWcU0sOokIaFY5eVoYgoc_2vfODCKExlLbOgDJxK9GNwWZgMV87RZo6ME56I9TKKpfGra4ek6OoioZkMQ0LoAUxcuVq1-Omryod-BbTTEGbiGWmK2SKJumUdPQRK7U5K9T3-IPxW1yoJinLbHEAKtGohyD1vE398FlwRrc4CrxvPD-fYLOCcMl1FfeX25UFJya6uB4HuqzaDrMJXIjOsfpx252ZeIQbkmmsjE0qvhS_Dh5uoVru4aAjD6ehU8JsJrjy2kduaKS8OME0M92T09yPG43b9UrEScl9EITxAtt5jyToUSc5Q9HcuCUzRx0tFz4hCl8ckA49NFl2PulZjRwmnFWlwvmRlET5Ple4CGWoYO8CI1-b4BouTOllDgAoSLEe7_Evie8qKX6X7lgv560ak6j1prOiGBgXyXCsF4tQnI8N_x5mSwcc8Da5jXEq-S1oWZ2JoP340z8qImDmlynuUr48I0e3JvwVkbxOVFuRYpeMLvuQvZJxviKmZFNQ7d1pdacbBwHnPF9Q4SSi1zxCXo_gQMbkoOt1lZlsdlN2CQvuSR7Dqvf2eCrO6VWmZfpHwRNQupq-Mhw5W23GeR0jpPyIgyGRf4WP5IMWekojXSc6He5gXhB1jHm911YEPZgy8Cc7NubdimxI6E-taFYOvVpU42BL2JwtjNdR0zIJEUniqc5_UWf2caNQp_6QhfnjyDm7CtX9URtrMtouAZfx_N58jcfn34" alt="Logo">
    </div>
    <form class="form" id="loginForm">
        <h1 class="form__title">Welcome To Hari Dyes Marketing</h1>
        <div class="form__message form__message--error"></div>
        <div class="form__input-group">
            <input type="text" class="form__input" id="loginUsername" autofocus placeholder="Username or Email">
            <div class="form__input-error-message"></div>
        </div>
        <div class="form__input-group">
            <input type="password" class="form__input" id="loginPassword" autofocus placeholder="Password">
            <div class="form__input-error-message"></div>
        </div>
        <button class="form__button" type="button" onclick="login()">Log In</button>
        <button type="button" onclick="showSignUpForm()">Sign Up</button>
    </form>
</section>

<!-- Sign Up Section (Initially Hidden) -->
<section id="signup" style="display: none;">
    <div class="logo">
        <img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAASwAAACoCAMAAABt9SM9AAAAdVBMVEX///8AAAC3t7e0tLTT09O8vLw9PT1HR0fJyckwMDCJiYl2dnZzc3Ph4eFOTk5lZWUdHR329vYtLS3p6enMzMxUVFQ3NzfAwMBbW1sLCwvv7+9sbGyCgoIlJSWlpaWSkpLb29ufn5+ioqIWFhaWlpZBQUEaGhoLBS80AAAEyElEQVR4nO2ci3KiMBSGEwXrDVtEar0htnbf/xEXpasJnJMEL7Ob7P/NdKajCRy+4ZKTHBQCAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAALOskWsT95aJM0r8dyuPpLR+3raT4kAqrfD+0GsuiKwm7YaVRybRJI1fWZP/S2kKIWMbGg0n6V3rGlsVcErwUZl9bpe2Ga7RRGr0zbYbU3know1Cj7zP7iKUsTAfTV7bxZmj3yQc3Yc+YirHakGs0Ve0zbdxl0WfHwKrzLEvuDQfTU7YxYluV5Fl1Ycqd1x7Kklv2WNxkFdYA2bPXP1n83cJJ1t4hwg+mr4eyZM7F6SDr4BTiK93ZR1lywHxvl7VwijCkM6syQT/i7bK+XAKcch78lCXfyEeWVdbRJT7+eeupLCmp8ZBVVjOUyTITp4F5oYwkDSO5p8jiBq4musqSZft7m6ylrmqqXszLWf2hKaPyV5Yctr63ydpq/Y/NI9hVH0amGJ8iix8983SX1b6ebbLe1d7EbXxCXtxXfJbVur3YZGmdqUeEZd7Ba1nNB1cXWbfE6LesRqLYRdYt91XPZel3nk6X4Q2To77L0lITmyx1H/LQPUbvZakB2WRNtI7toYcN/2XJ+eWCssnq6R1N84gkAciSX9nP9zZZaaPjruMCSAiyLomiNTecNDuOLEsUOk6y1H38O+mOSp2lWGVlRNfpwjlGVdbqjWHVUdYqnxl4hqz6bm2fz6LnaLbGjJCW5cT9UzRPkXXu4zCtnDPdnXwFI+uUKLosWAy4/rsDvwYWnKxqJOC0FMbaqm7aGdcpOFlyrE7u8U/kKbsBwzMuOFlyp/xvGL4MTcsWpmoKb2UZrqYzxrGeaeGCX8P1V9YmWzU3rGEeGKdH/uwasONUb2W9imzX3LKKNYtYfnBddy6y8rhHEquDExdZ8ywx8ChZItXm1LvKqvoXM7ovVx/gbbpzLkd4uUtWxbpP+mIKxLxNpOvaDfZSco8hO7TrtVZ0U89ltecRbolh0UqC6FPLd1nsE6pbDOW33ps+Su9licMjZLUKAsk80X9ZWtntHTHo0sk51ABkNes9bo1BG7aRtTQhyBLRQ2Rp1aZjqkUQskT5CFna5UzWRIchSyStRNEwReMw5Az5zKpSl2aiyMbwWvUln3Vad1JoKLJaiSIXQz3+PLZnFvRkgFzyCUaWEHqWR8eQXnYz1hP6dSNHJKdpvC2TJOr6tXODlLXW5lL3iz9KombWRM8APkXWbrjkielVgQfI0t5eo2QRa6zf+SYftT+mF8a8Le0m3xhRKmwJWYlziMwrFmHJUgaWbVnuEdKZYXCyru9dtmU1Co4McNUPocm6jMOJyzDl1u6dAhQByvoTCPk07JlXhGr4isDwZP2k1cw4y7qaNTIs4Qcoq06ruYHxWn8npUnzHRWNEGWdx1N8FpEW7Gr22FxI0/mnCri3SO+V5fJTBerzjH3390T6y5xyrQtiWSjndnshUn43gq0XXCiNuJrVrO8KvcoaW1uI+t2aND392UpB5+yy8iXg4ed+ms/eK17ybREF+AsrzpguUwAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA4D/jN0/ZTUoS5ClIAAAAAElFTkSuQmCC" alt="Logo">
    </div>
    <form class="form" id="signUpForm" style="display: none;">
        <h1 class="form__title">Sign Up</h1>
        <div class="form__message form__message--error"></div>
        <div class="form__input-group">
            <input type="text" class="form__input" id="signupFullName" autofocus placeholder="Full Name">
            <div class="form__input-error-message"></div>
        </div>
        <div class="form__input-group">
            <input type="email" class="form__input" id="signupEmail" autofocus placeholder="Email">
            <div class="form__input-error-message"></div>
        </div>
        <div class="form__input-group">
            <input type="password" class="form__input" id="signupPassword" autofocus placeholder="Password">
            <div class="form__input-error-message"></div>
        </div>
        <div class="form__input-group">
            <input type="password" class="form__input" id="signupConfirmPassword" autofocus placeholder="Confirm Password">
            <div class="form__input-error-message"></div>
        </div>
        <button class="form__button" type="button" onclick="signup()">Sign Up</button>
        <p class="form__text"><button type="button" onclick="showLoginForm()">Log In</button></p>
    </form>
</section>
<!-- Header -->
<header id="header" style="display: none;">
    <img src="https://mail-attachment.googleusercontent.com/attachment/u/1/?ui=2&ik=538c1ca84e&attid=0.1&permmsgid=msg-a:r-1647255721203284238&th=18ed21035ae72125&view=att&disp=safe&realattid=18ed21027a57a6531981&saddbat=ANGjdJ_0QooMQfQXEz4yKMJh0KTGApfmmyyC8Nr_I7CYf8O9ZXcdqFJItQmA-BDFMYUM_w0GWW2kpwijrNEtinB2c6ST3loDCWP36vHC0v9nrr7jsq2vopyaxm2mFh2gc3Ex9jdTJLSZqnmInfiyWP10AJLiTHrHEr3U1waJ70SmPk0LHuPfEJIy3dVJmfTqGMOJsVhJuZ5c26qeM8QQGW3phACoxS_SfFYEnkYqtyHW7ggxlQ0xO4hmh504La3k2_01slcrYG-J2PlihmUX5_y8oKxFBn4mOCqDYiryP62SHR30upHcWTCdIccHKhAqvSovbfR28AZDvu14Jgd0ZqfflHBohHsVGKDD7u8Ls1XPKHA4hmdUIbqjBnay50TC0nkXnn-h86cQUoGVfReATDVx35_5lsihX0DcPaf4XXM-nVjKmRyk0Wr23Z0VL_gLi1wy-oTNFSraZCdiXo1mZmvUrsWGcEyREcz-XCAfS7tqNFubj7f1C2MXabrFADugJUhrXVFAhEXSB6FbEpncFHURgN2EmozvNmiT4nKnPSfYlnmxOjx1meg1huV85VAVJhJAJ54_-B_gn-ewiLIOEC8Nnxo4KdEaqVNQldlXo2pcDOPNeLE-ft-R2710iF9p5YUdF_fLQWySOz6z_QcT_PyCye0Bfh5LxQBxH3kZbxSzF1_TkiIjIhQuJ9t09jvvgymw5EB40bFr7IMDSYAmHYb1yDMXkMr9rH32vcnB4HJLyAm5T4X4imiYYwyt0eMXzBB8yb8lk3D3gtS-45KZ5Tq5QQ7vatApw0eMtBgT4kKh40ILalDVWV1uPcioP3T5riGwVCn7SOdNo3Fo84uqrdOuefnL9v0Ee4r3-nJ_XT8IokeMLjm45TgPuWSvtAfnWuzbUC-UlCKfbfbjN08ALZxx8QjM52xDUKIJWQUa65xJ36MBc2pO3RwWxeEGPStSHwLe_zctrZRsr0Q6iZ0IKo_-ChgPnHt9qAQjX3tnMv2IU-cBpo3R7JQ93sjFu80BY4XJJQ0qylnY5u0EkzAbC4pzVc3YSP-YqespN5b2uw" alt="" width="200" height="200">
    <div class="logo">Logo</div>
    <nav>
        <ul class="navigation">
            <li><a href="#" onclick="showPage('home')">Home</a></li>
            <li><a href="#" onclick="showPage('products')">Products</a></li>
            <li><a href="#" onclick="showPage('about')">About</a></li>
            <li><a href="#" onclick="showPage('contact')">Contact</a></li>
        </ul>
    </nav>
</header>

<!-- Main Content -->
<main id="main-content" style="display: none;">
    <!-- Home Page -->
    <section id="home">
    <div class="image-container">
    <img src="https://c02.purpledshub.com/uploads/sites/41/2021/08/Alamy_2F3Y8J0-crop-ff47efc.jpg" alt="shoes">
    <div class="text-container">
    <div class="welcome-text">
                <h2>Welcome to our website!</h2>
                <p>Explore our products and find what you need.</p>
            </div>
            <div class="shop-now-box">
            <button>Shop Now</button>
            </div>
        </div>
    </div>
</section>

    <!-- Products Page -->
    <section id="products" style="display: none;">
     <button id="cart-btn" onclick="showCart()">Cart (0)</button>
        <h2>Our Products</h2>
        <div class="product">
            <h3>Product 1</h3>
            <p>Description of Product 1</p>
          
            <button onclick="addToCart('Product 1', 10)">Add to Cart</button>
        </div>
        <div class="product">
            <h3>Product 2</h3>
            <p>Description of Product 2</p>
            <button onclick="addToCart('Product 2', 20)">Add to Cart</button>
        </div>
    </section>

    <!-- About Page -->
    <section id="about" style="display: none;">
        <h2>About Us</h2>
        <p>Welcome to HARI DYES, your one-stop online destination for everything
                fashionable in the Philippines. Bringing you insights on global and local
                trends, we feature your favorite international designers as well as the 
                most relevant Filipino brands. </p>
        <p> We constantly update ourselves with the latest fashion trends to make 
                sure we offer you only the most exciting styles for clothing, shoes,
                bags, watches, beauty, and all things fashion. </p>

            <p> At HARI DYES, we believe your shopping experience should be easy and 
                fun. That's why we have an awesome team of local customer service 
                consultants (located in our Manila office) to assist you on all your
                inquires or concerns.</p>

            <h5> Free Returns </h5>
            <p> Shoes and clothing size will always vary, so if an item does not fit 
                to your liking, HARI DYES will accept returns within 30 days after you 
                recieve your goods. With drop-off locations located all over the country,
                as well as free pick-up services in certain areas, it's super convenient 
                to return and exchange your item. </p>

            <h5> Comprehensive And Personal Service </h5>
            <p> Our objective is to offer you an effortless online shopping 
                experience, so for any question, you can reach HARI DYES's customer
                service experts via phone and email. Our team is eager to answer any 
                questions or concerns you might have! </p>
      <h5> Unparalleled Product Range </h5>
            <p> At HARI DYES, you will find the biggest international brands as well
                as the most relevant Filipino products. From apparel to footwear to 
                sportswear to accessories, you've sure to find what you're looking for 
                among the thousands of styles available.</p>

            <h4>Sell With Us</h4>

            <h5> Join the HARI DYES PH Marketplace Today! </h5>
            Wouldn't it be wonderful to be part of HARI DYES, the online shopping 
            destination for all fashion lovers? By joining the HARI DYES PH 
            Marketplace, your store will be featured alongside the most successful 
            brands in the Philippines.</p>
    </section>

    <!-- Contact Page -->
    <section id="contact" style="display: none;">
        <h2>Contact Us</h2>
        <p>Email: info@haridyes.com</p>
        <p>Phone: +63 123 456 789</p>
        <p>Address: 123 Main Street, Manila, Philippines</p>
    </section>
</main>

<script src="scripts.js"></script>
</body>
</html>
