<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Spray & Toy's</title>
  <meta name="description" content="Private personal-care products delivered discreetly across Nepal." />
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=DM+Sans:wght@400;500;600;700&family=Playfair+Display:wght@600;700&display=swap" rel="stylesheet">
  <style>
    :root{
      --ink:#32122f; --muted:#705f6e; --cream:#fff9f2; --paper:#fffdf9;
      --accent:#ef6670; --line:#eaded8; --dark:#271124;
    }
    *{box-sizing:border-box}
    html{scroll-behavior:smooth}
    body{
      margin:0;
      background:var(--cream);
      color:var(--ink);
      font-family:'DM Sans',sans-serif;
      line-height:1.6;
    }
    a{color:inherit;text-decoration:none}
    .container{width:min(1120px,92%);margin:auto}
    .topbar{
      position:sticky;
      top:0;
      z-index:20;
      background:rgba(255,249,242,.94);
      backdrop-filter:blur(12px);
      border-bottom:1px solid var(--line);
    }
    .nav{min-height:76px;display:flex;align-items:center;gap:28px}
    .brand img{width:115px;height:55px;object-fit:contain}
    nav{
      display:flex;
      gap:24px;
      flex:1;
      justify-content:center;
      font-size:14px;
    }
    nav a:hover{text-decoration:underline}
    .whatsapp{
      border:1px solid var(--ink);
      padding:9px 15px;
      border-radius:999px;
      font-size:13px;
    }
    .hero{
      display:grid;
      grid-template-columns:1.25fr .75fr;
      gap:50px;
      align-items:center;
      padding:85px 0 70px;
    }
    .eyebrow{
      text-transform:uppercase;
      letter-spacing:.15em;
      font-size:11px;
      font-weight:700;
      color:var(--accent);
      margin:0 0 12px;
    }
    h1,h2{font-family:'Playfair Display',serif;line-height:1.08;margin:0 0 20px}
    h1{font-size:clamp(48px,7vw,84px)}
    h1 em{font-style:normal;color:var(--accent)}
    h2{font-size:clamp(34px,4vw,54px)}
    h3{margin:7px 0 8px;line-height:1.2}
    .hero-copy{max-width:620px;color:var(--muted);font-size:17px}
    .hero-actions{display:flex;gap:12px;margin:28px 0}
    .btn{
      border:0;
      border-radius:999px;
      padding:13px 21px;
      font:inherit;
      font-weight:700;
      cursor:pointer;
      display:inline-block;
    }
    .btn-primary{background:var(--ink);color:white}
    .btn-primary:hover{opacity:.9}
    .btn-ghost{
      border:1px solid var(--ink);
      background:transparent;
      color:var(--ink);
    }
    .trust-row{
      display:flex;
      flex-wrap:wrap;
      gap:12px 18px;
      font-size:12px;
      color:var(--muted);
    }
    .hero-card{
      background:white;
      border:1px solid var(--line);
      border-radius:28px;
      padding:38px;
      text-align:center;
      box-shadow:0 18px 50px rgba(50,18,47,.07);
    }
    .hero-card img{
      width:80%;
      max-width:290px;
      height:auto;
    }
    .hero-card p{
      margin:12px 0 2px;
      color:var(--accent);
      text-transform:uppercase;
      letter-spacing:.18em;
      font-size:11px;
    }
    .section{padding:75px 0}
    .section-head{
      display:flex;
      justify-content:space-between;
      gap:30px;
      align-items:end;
      margin-bottom:28px;
    }
    .section-head>p{
      max-width:420px;
      color:var(--muted);
      margin:0;
    }
    .products{
      display:grid;
      grid-template-columns:repeat(4,1fr);
      gap:18px;
    }
    .product-card{
      background:var(--paper);
      border:1px solid var(--line);
      border-radius:20px;
      padding:18px;
      display:flex;
      flex-direction:column;
    }
    .product-placeholder{
      height:230px;
      border-radius:14px;
      background:#f4e8e2;
      display:grid;
      place-items:center;
      text-align:center;
      font-family:'Playfair Display',serif;
      font-size:30px;
      letter-spacing:.06em;
      color:var(--ink);
      margin-bottom:17px;
    }
    .product-placeholder.dark{background:var(--dark);color:#fff}
    .tag{
      font-size:11px;
      text-transform:uppercase;
      letter-spacing:.1em;
      color:var(--accent);
      font-weight:700;
      margin:0;
    }
    .product-card h3{font-size:20px}
    .desc{
      font-size:13px;
      color:var(--muted);
      min-height:60px;
    }
    .price{
      font-weight:800;
      font-size:18px;
      margin-top:auto;
      padding:10px 0;
    }
    .price del{
      font-size:12px;
      color:#a6959e;
      margin-left:6px;
    }
    .price small{
      font-size:11px;
      color:var(--muted);
      font-weight:500;
    }
    .order-product{
      background:transparent;
      border:1px solid var(--ink);
      border-radius:999px;
      padding:10px 13px;
      cursor:pointer;
      font-weight:700;
      color:var(--ink);
    }
    .order-section{
      background:var(--dark);
      color:#fff;
    }
    .order-grid{
      display:grid;
      grid-template-columns:.85fr 1.15fr;
      gap:60px;
      align-items:start;
    }
    .order-grid p{color:#dbcdd8}
    .order-form{
      background:var(--paper);
      color:var(--ink);
      padding:28px;
      border-radius:24px;
    }
    label{
      display:block;
      font-size:13px;
      font-weight:700;
      margin-bottom:15px;
    }
    input,select,textarea{
      display:block;
      width:100%;
      margin-top:7px;
      border:1px solid var(--line);
      border-radius:12px;
      padding:12px 13px;
      font:inherit;
      background:white;
      outline:none;
    }
    input:focus,select:focus,textarea:focus{border-color:var(--accent)}
    .two{
      display:grid;
      grid-template-columns:.35fr .65fr;
      gap:12px;
    }
    .optional{font-weight:400;color:var(--muted)}
    .form-summary{
      display:flex;
      justify-content:space-between;
      border-top:1px solid var(--line);
      padding:15px 0;
      margin-top:4px;
    }
    .full{width:100%}
    .form-note{
      font-size:11px!important;
      color:var(--muted)!important;
      text-align:center;
      margin:10px 0 0!important;
    }
    .mini-points{
      display:grid;
      gap:10px;
      margin-top:25px;
    }
    .promise-grid{
      display:grid;
      grid-template-columns:repeat(4,1fr);
      gap:18px;
    }
    .promise-grid>div,.steps>div{
      border-top:1px solid var(--line);
      padding-top:18px;
    }
    .promise-grid span{
      font-size:12px;
      color:var(--accent);
      font-weight:700;
    }
    .promise-grid p,.steps p{
      color:var(--muted);
      font-size:14px;
    }
    .soft{background:#f5ebe5}
    .steps{
      display:grid;
      grid-template-columns:repeat(3,1fr);
      gap:35px;
      margin-top:30px;
    }
    .steps b{color:var(--accent);font-size:13px}
    .faq details{
      border-top:1px solid var(--line);
      padding:18px 0;
    }
    .faq summary{cursor:pointer;font-weight:700}
    .faq details p{
      color:var(--muted);
      max-width:700px;
    }
    footer{background:#1e0d1b;color:#eee}
    .footer{
      padding:48px 0;
      display:grid;
      grid-template-columns:2fr 1fr 1fr;
      gap:40px;
    }
    .footer img{
      width:120px;
      height:60px;
      object-fit:contain;
      filter:brightness(0) invert(1);
      opacity:.95;
    }
    .footer p,.footer span,.footer a{
      display:block;
      color:#c9bbc6;
      font-size:13px;
      margin:5px 0;
    }
    .footer strong{display:block;margin-bottom:10px}
    .copyright{
      text-align:center;
      border-top:1px solid #3d2939;
      padding:15px;
      color:#9e8c9b;
      font-size:11px;
    }
    .age-gate{
      position:fixed;
      inset:0;
      background:rgba(32,10,29,.98);
      z-index:100;
      display:grid;
      place-items:center;
      padding:20px;
    }
    .age-card{
      background:var(--cream);
      max-width:480px;
      width:100%;
      border-radius:28px;
      padding:40px;
      text-align:center;
      box-shadow:0 30px 90px rgba(0,0,0,.35);
    }
    .age-logo{
      width:220px;
      max-width:80%;
      height:auto;
      margin-bottom:10px;
    }
    .age-card h1{font-size:44px}
    .age-card p:not(.eyebrow){color:var(--muted)}
    .age-card .btn{width:100%;margin:6px 0}
    .age-card small{
      display:block;
      color:#9b8994;
      margin-top:12px;
      font-size:11px;
    }
    @media(max-width:900px){
      nav{display:none}
      .hero{grid-template-columns:1fr;padding-top:55px}
      .hero-card{max-width:480px;margin:auto}
      .products{grid-template-columns:repeat(2,1fr)}
      .promise-grid{grid-template-columns:repeat(2,1fr)}
      .order-grid{grid-template-columns:1fr;gap:30px}
      .footer{grid-template-columns:1fr 1fr}
    }
    @media(max-width:560px){
      .nav{justify-content:space-between}
      .whatsapp{padding:8px 12px}
      .hero{padding:45px 0}
      .hero-actions{flex-direction:column}
      .hero-actions .btn{text-align:center}
      .products{grid-template-columns:1fr}
      .section{padding:55px 0}
      .section-head{display:block}
      .section-head>p{margin-top:12px}
      .promise-grid,.steps{grid-template-columns:1fr}
      .footer{grid-template-columns:1fr}
      .age-card{padding:28px 20px}
      .age-card h1{font-size:38px}
    }
  </style>
</head>
<body>
  <div class="age-gate" id="ageGate">
    <div class="age-card">
      <img class="age-logo" src="https://via.placeholder.com/220x110?text=Spray+%26+Toy%27s" alt="Spray & Toy's logo">
      <p class="eyebrow">Adults only · 18+</p>
      <h1>Enter after dark.</h1>
      <p>This website contains intimate products intended for adults. Please confirm you are 18 or older.</p>
      <button class="btn btn-primary" id="enterBtn">I am 18 or older</button>
      <button class="btn btn-ghost" id="leaveBtn">Leave</button>
      <small>By entering, you confirm that you are 18 or older.</small>
    </div>
  </div>

  <header class="topbar">
    <div class="container nav">
      <a href="#" class="brand" aria-label="Spray & Toy's">
        <img src="https://via.placeholder.com/200x90?text=Spray+%26+Toy%27s" alt="Spray & Toy's logo">
      </a>

      <nav aria-label="Main navigation">
        <a href="#collection">Collection</a>
        <a href="#promise">Our Promise</a>
        <a href="#how-to-order">How to Order</a>
        <a href="#faq">FAQ</a>
      </nav>

      <a class="whatsapp" href="https://wa.me/9779713673974" target="_blank" rel="noreferrer">WhatsApp</a>
    </div>
  </header>

  <main>
    <section class="container hero">
      <div>
        <p class="eyebrow">Certified · Original · Discreet</p>
        <h1>Private care,<br>delivered <em>discreetly.</em></h1>
        <p class="hero-copy">
          Intimate and personal-care products delivered quietly across Nepal. Order directly through our simple private order form.
        </p>

        <div class="hero-actions">
          <a href="#collection" class="btn btn-primary">Explore collection</a>
          <a href="#order" class="btn btn-ghost">Order privately</a>
        </div>

        <div class="trust-row">
          <span>✓ Original products</span>
          <span>✓ Cash on delivery</span>
          <span>✓ All over Nepal</span>
          <span>✓ Discreet packaging</span>
        </div>
      </div>

      <div class="hero-card">
        <img src="https://via.placeholder.com/420x360?text=Spray+%26+Toy%27s" alt="Spray & Toy's product display">
        <p>Spray & Toy's</p>
        <h2>Condom House</h2>
      </div>
    </section>

    <section class="section">
      <div class="container">
        <div class="section-head">
          <h2>Simple. Private. Reliable.</h2>
        </div>
      </div>
    </section>

    <section id="collection" class="section">
      <div class="container">
        <div class="section-head">
          <h2>The collection</h2>
          <p>Choose your product. Prices shown below. Select a product to open the order form.</p>
        </div>

        <div class="products">
          <article class="product-card">
            <div class="product-placeholder">LIQO</div>
            <p class="tag">For him · 20g</p>
            <h3>Liqo Care Long Lasting Spray</h3>
            <p class="desc">Personal-care spray for men. For external use only.</p>
            <div class="price">Rs. 899 <del>Rs. 1200</del></div>
            <button class="order-product" data-product="Liqo Care Long Lasting Spray">Order now →</button>
          </article>

          <article class="product-card">
            <div class="product-placeholder dark">SUPER</div>
            <p class="tag">For him</p>
            <h3>Super Dooz 44000</h3>
            <p class="desc">Delay spray for men. Genuine product. For external use only.</p>
            <div class="price">Rs. 999 <small>per piece</small></div>
            <button class="order-product" data-product="Super Dooz 44000">Order now →</button>
          </article>

          <article class="product-card">
            <div class="product-placeholder">SUPER</div>
            <p class="tag">For him · 45ml</p>
            <h3>Super Viga 50000</h3>
            <p class="desc">Personal-care spray with vitamin E. For external use only.</p>
            <div class="price">Rs. 799</div>
            <button class="order-product" data-product="Super Viga 50000">Order now →</button>
          </article>

          <article class="product-card">
            <div class="product-placeholder dark">CONDOM</div>
            <p class="tag">Private catalogue</p>
            <h3>Condoms & more</h3>
            <p class="desc">Ask us privately for currently available products and prices.</p>
            <div class="price">Private</div>
            <button class="order-product" data-product="Private catalogue">Ask for availability</button>
          </article>
        </div>
      </div>
    </section>

    <section id="order" class="section order-section">
      <div class="container order-grid">
        <div>
          <h2>Private order form</h2>
          <p>Place your order in under a minute. Your details are used to arrange delivery. After you submit, WhatsApp opens with a ready-to-send order message.</p>

          <div class="mini-points">
            <div>✓ Cash on delivery</div>
            <div>✓ Nepal-wide delivery</div>
            <div>✓ Plain packaging</div>
          </div>
        </div>

        <form id="orderForm" class="order-form">
          <label>
            Product
            <select id="product" name="product">
              <option value="">Select a product</option>
              <option value="Liqo Care Long Lasting Spray" data-price="899">Liqo Care Long Lasting Spray</option>
              <option value="Super Dooz 44000" data-price="999">Super Dooz 44000</option>
              <option value="Super Viga 50000" data-price="799">Super Viga 50000</option>
              <option value="Private catalogue" data-price="0">Private catalogue / Ask availability</option>
            </select>
          </label>

          <div class="two">
            <label>
              Quantity
              <input id="quantity" name="quantity" type="number" min="1" value="1">
            </label>

            <label>
              Full name
              <input id="name" name="name" type="text" placeholder="Your name">
            </label>
          </div>

          <label>
            Phone number
            <input id="phone" name="phone" type="tel" placeholder="98XXXXXXXX">
          </label>

          <label>
            Delivery address
            <textarea id="address" name="address" rows="3" placeholder="Municipality, ward, area, landmark..."></textarea>
          </label>

          <label>
            Order note <span class="optional">(optional)</span>
            <textarea id="note" name="note" rows="3" placeholder="Any delivery instruction"></textarea>
          </label>

          <div class="form-summary">
            <strong>Estimated total</strong>
            <strong id="total">—</strong>
          </div>

          <button class="btn btn-primary full" type="submit">Continue on WhatsApp →</button>
          <p class="form-note">By submitting, WhatsApp will open with your order details. You can review the message before sending it.</p>
        </form>
      </div>
    </section>

    <section id="promise" class="section">
      <div class="container">
        <div class="section-head">
          <h2>Our promise</h2>
        </div>

        <div class="promise-grid">
          <div>
            <span>I</span>
            <h3>Discreet delivery</h3>
            <p>Plain, unmarked packaging for customer privacy.</p>
          </div>

          <div>
            <span>II</span>
            <h3>Quality products</h3>
            <p>We aim to provide genuine, quality-checked products.</p>
          </div>

          <div>
            <span>III</span>
            <h3>Cash on delivery</h3>
            <p>Pay when your order arrives, where COD is available.</p>
          </div>

          <div>
            <span>IV</span>
            <h3>Private support</h3>
            <p>Call or WhatsApp us for product and delivery questions.</p>
          </div>
        </div>
      </div>
    </section>

    <section class="section soft">
      <div class="container">
        <div class="section-head">
          <h2>Simple & private</h2>
        </div>

        <div class="steps">
          <div>
            <b>01</b>
            <h3>Choose</h3>
            <p>Select your product and fill in the order form.</p>
          </div>

          <div>
            <b>02</b>
            <h3>Confirm</h3>
            <p>Review your WhatsApp order message and send it to us.</p>
          </div>

          <div>
            <b>03</b>
            <h3>Receive</h3>
            <p>We confirm delivery details and arrange your order.</p>
          </div>
        </div>
      </div>
    </section>

    <section id="faq" class="section faq">
      <div class="container">
        <div class="section-head">
          <h2>Good to know</h2>
        </div>

        <div>
          <details open>
            <summary>Will anyone know what's in the package?</summary>
            <p>Yes. We use discreet, plain packaging to protect your privacy and keep your order private.</p>
          </details>

          <details>
            <summary>Do you deliver outside Kathmandu?</summary>
            <p>Yes. We aim to deliver across Nepal depending on service availability and destination.</p>
          </details>

          <details>
            <summary>Is cash on delivery available?</summary>
            <p>Cash on delivery may be available depending on your location and product stock.</p>
          </details>

          <details>
            <summary>Do you provide medical advice?</summary>
            <p>We do not provide medical advice. Please use the products responsibly and follow the product instructions.</p>
          </details>
        </div>
      </div>
    </section>
  </main>

  <footer>
    <div class="container footer">
      <div>
        <img src="https://via.placeholder.com/200x90?text=Spray+%26+Toy%27s" alt="Spray & Toy's logo">
        <p>Private personal-care products delivered discreetly across Nepal.</p>
      </div>

      <div>
        <strong>Contact</strong>
        <a href="https://wa.me/9779713673974" target="_blank" rel="noreferrer">+977 971-3673974</a>
        <span>WhatsApp</span>
      </div>

      <div>
        <strong>Location</strong>
        <span>Kathmandu, Nepal</span>
        <span>18+ only</span>
      </div>
    </div>
    <div class="copyright">© Spray & Toy's. Adults 18+ only</div>
  </footer>

  <script>
    const WHATSAPP = "9779713673974";

    const ageGate = document.getElementById("ageGate");
    const enterBtn = document.getElementById("enterBtn");
    const leaveBtn = document.getElementById("leaveBtn");

    if (sessionStorage.getItem("ageVerified") === "yes") ageGate.style.display = "none";

    enterBtn.addEventListener("click", () => {
      sessionStorage.setItem("ageVerified", "yes");
      ageGate.style.display = "none";
    });

    leaveBtn.addEventListener("click", () => {
      window.location.href = "https://www.google.com/";
    });

    const productSelect = document.getElementById("product");
    const quantity = document.getElementById("quantity");
    const total = document.getElementById("total");

    function updateTotal() {
      const option = productSelect.options[productSelect.selectedIndex];
      const price = Number(option?.dataset.price || 0);
      const qty = Math.max(1, Number(quantity.value || 1));
      total.textContent = price ? `Rs. ${(price * qty).toLocaleString()}` : "Ask for availability";
    }
    productSelect.addEventListener("change", updateTotal);
    quantity.addEventListener("input", updateTotal);

    document.querySelectorAll(".order-product").forEach(btn => {
      btn.addEventListener("click", () => {
        const name = btn.dataset.product;
        [...productSelect.options].some(opt => {
          if (opt.value === name) { opt.selected = true; return true; }
          return false;
        });
        updateTotal();
        document.getElementById("order").scrollIntoView({behavior:"smooth"});
      });
    });

    document.getElementById("orderForm").addEventListener("submit", (e) => {
      e.preventDefault();

      const product = productSelect.value;
      const qty = quantity.value;
      const name = document.getElementById("name").value.trim();
      const phone = document.getElementById("phone").value.trim();
      const address = document.getElementById("address").value.trim();
      const note = document.getElementById("note").value.trim();

      if (!product || !name || !phone || !address) return;

      const selected = productSelect.options[productSelect.selectedIndex];
      const price = Number(selected?.dataset.price || 0);
      const estimated = price ? `Rs. ${(price * Number(qty)).toLocaleString()}` : "Please confirm availability and price";

      const message =
`Hello Spray & Toy's, I would like to place an order.

Product: ${product}
Quantity: ${qty}
Estimated total: ${estimated}

Name: ${name}
Phone: ${phone}
Address: ${address}
Note: ${note || "None"}

Please confirm availability and delivery details.`;

      window.open(`https://wa.me/${WHATSAPP}?text=${encodeURIComponent(message)}`, "_blank");
    });
  </script>
</body>
</html>