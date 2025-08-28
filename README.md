# Joshua-Super-Store
Perfect! 🔥 Here’s your **fully polished Joshua Super Store homepage** with:

* **Animated sliding hamburger menu** for mobile/tablet
* **Header, product cards, and footer with smooth fade-up scroll animations**
* **Floating Watch Video button**
* Fully **responsive design** for desktop, tablet, and mobile
* Black & red **branding maintained throughout**

You can paste this directly into Shopify or any HTML environment.

---

### 🔹 Full Animated & Responsive Homepage

```html
<!-- ===== Navigation Menu ===== -->
<div style="background:#000; color:#fff; position:sticky; top:0; z-index:1000; border-bottom:3px solid #d00; font-family: Arial, sans-serif;">
  <div style="display:flex; justify-content:space-between; align-items:center; padding:15px 20px;">
    
    <!-- Logo -->
    <div style="font-size:22px; font-weight:bold; color:#d00;">Joshua Super Store</div>
    
    <!-- Hamburger Icon -->
    <div id="hamburger" style="font-size:28px; cursor:pointer; display:none;">☰</div>
    
    <!-- Navigation Links -->
    <div id="nav-links" style="display:flex; gap:15px;">
      <a href="#" style="color:#fff; text-decoration:none; font-weight:bold; transition:color 0.3s;">Home</a>
      <a href="#" style="color:#fff; text-decoration:none; font-weight:bold; transition:color 0.3s;">Shop</a>
      <a href="#" style="color:#fff; text-decoration:none; font-weight:bold; transition:color 0.3s;">About</a>
      <a href="#" style="color:#fff; text-decoration:none; font-weight:bold; transition:color 0.3s;">Contact</a>
    </div>
    
  </div>
</div>

<style>
  /* Hover Effect */
  #nav-links a:hover { color:#d00; }

  /* Mobile Styles */
  @media (max-width:768px) {
    #nav-links {
      display:flex;
      flex-direction:column;
      overflow:hidden;
      max-height:0;
      transition:max-height 0.5s ease;
      background:#000;
      padding:0 20px;
      border-top:3px solid #d00;
    }
    #hamburger { display:block; }
  }

  img { max-width:100%; height:auto; }

  /* Featured Products adjustments for small screens */
  @media (max-width:768px) {
    .featured-product { width:100% !important; max-width:100% !important; }
    h1 { font-size:28px; }
    h2 { font-size:24px; }
    p { font-size:15px; }
  }

  /* Scroll Animations */
  .fade-up { opacity:0; transform:translateY(30px); transition:opacity 0.8s ease, transform 0.8s ease; }
  .fade-up.show { opacity:1; transform:translateY(0); }
</style>

<script>
  // Hamburger Menu Animation
  const hamburger = document.getElementById('hamburger');
  const navLinks = document.getElementById('nav-links');
  let menuOpen = false;
  hamburger.addEventListener('click', () => {
    if(menuOpen) { navLinks.style.maxHeight='0'; menuOpen=false; } 
    else { navLinks.style.maxHeight = navLinks.scrollHeight + 'px'; menuOpen=true; }
  });

  // Scroll Fade-up Animation
  function scrollFadeUp() {
    const elements = document.querySelectorAll('.fade-up');
    const windowBottom = window.innerHeight;
    elements.forEach(el => {
      const rect = el.getBoundingClientRect();
      if(rect.top < windowBottom - 50) el.classList.add('show');
    });
  }
  window.addEventListener('scroll', scrollFadeUp);
  window.addEventListener('load', scrollFadeUp);
</script>

<!-- ===== Header Banner ===== -->
<div class="fade-up" style="background:#000; color:#fff; text-align:center; padding:60px 20px; border-bottom:5px solid #d00;">
  <h1 style="font-family: Arial, sans-serif; font-size:32px; font-weight:bold; margin-bottom:15px;">
    Welcome to <span style="color:#d00;">Joshua Super Store</span>
  </h1>
  <p style="font-family: Arial, sans-serif; font-size:16px; margin-bottom:25px;">
    Fashion. Tech. Lifestyle. Exclusive Deals Just for You.
  </p>
  <a href="https://www.youtube.com/watch?v=JoshuaSuperStoreDemo" target="_blank" 
     style="display:inline-block; background:#d00; color:#fff; padding:12px 28px; 
            border-radius:50px; font-size:16px; font-weight:bold; text-decoration:none;
            font-family: Arial, sans-serif; box-shadow:0 4px 12px rgba(0,0,0,0.3); 
            transition:background 0.3s ease;">
    ▶ Watch Video
  </a>
</div>

<!-- ===== Featured Products ===== -->
<div class="fade-up" style="background:#111; color:#fff; padding:40px 10px; text-align:center;">
  <h2 style="font-family: Arial, sans-serif; font-size:28px; font-weight:bold; margin-bottom:30px; color:#d00;">
    Featured Products
  </h2>
  
  <div style="display:flex; flex-wrap:wrap; justify-content:center; gap:20px;">
    
    <!-- Product 1 -->
    <div class="featured-product fade-up" style="background:#000; border-radius:12px; padding:20px; width:100%; max-width:250px; box-shadow:0 4px 12px rgba(0,0,0,0.5);">
      <img src="https://via.placeholder.com/250x250?text=Product+1" alt="Product 1" style="width:100%; border-radius:8px; margin-bottom:15px;">
      <h3 style="font-family: Arial, sans-serif; font-size:18px; color:#fff; margin-bottom:10px;">Product 1</h3>
      <p style="font-family: Arial, sans-serif; font-size:14px; color:#bbb; margin-bottom:15px;">Short product description here.</p>
      <a href="#" style="display:inline-block; background:#d00; color:#fff; padding:10px 20px; 
             border-radius:50px; font-size:14px; font-weight:bold; text-decoration:none; 
             transition:background 0.3s ease;">Buy Now</a>
    </div>
    
    <!-- Product 2 -->
    <div class="featured-product fade-up" style="background:#000; border-radius:12px; padding:20px; width:100%; max-width:250px; box-shadow:0 4px 12px rgba(0,0,0,0.5);">
      <img src="https://via.placeholder.com/250x250?text=Product+2" alt="Product 2" style="width:100%; border-radius:8px; margin-bottom:15px;">
      <h3 style="font-family: Arial, sans-serif; font-size:18px; color:#fff; margin-bottom:10px;">Product 2</h3>
      <p style="font-family: Arial, sans-serif; font-size:14px; color:#bbb; margin-bottom:15px;">Short product description here.</p>
      <a href="#" style="display:inline-block; background:#d00; color:#fff; padding:10px 20px; 
             border-radius:50px; font-size:14px; font-weight:bold; text-decoration:none; 
             transition:background 0.3s ease;">Buy Now</a>
    </div>
    
    <!-- Product 3 -->
    <div class="featured-product fade-up" style="background:#000; border-radius:12px; padding:20px; width:100%; max-width:250px; box-shadow:0 4px 12px rgba(0,0,0,0.5);">
      <img src="https://via.placeholder.com/250x250?text=Product+3" alt="Product 3" style="width:100%; border-radius:8px; margin-bottom:15px;">
      <h3 style="font-family: Arial, sans-serif; font-size:18px; color:#fff; margin-bottom:10px;">Product 3</h3>
      <p style="font-family: Arial, sans-serif; font-size:14px; color:#bbb; margin-bottom:15px;">Short product description here.</p>
      <a href="#" style="display:inline-block; background:#d00; color:#fff; padding:10px 20px; 
             border-radius:50px; font-size:14px; font-weight:bold; text-decoration:none; 
             transition:background 0.3s ease;">Buy Now</a>
    </div>
    
  </div>
</div>

<!-- ===== Footer ===== -->
<div class="fade-up" style="background:#000; color:#fff; text-align:center; padding:30px 15px; border-top:5px solid #d00; margin-top:40px;">
  <h2 style="font-family: Arial, sans-serif; font-size:22px; font-weight:bold; margin-bottom:12px;">
    Stay Connected with <span style="color:#d00;">Joshua Super Store</span>
  </h2>
  
  <div style="margin-bottom:15px; font-size:16px;">
    <a href="#" style="margin:0 8px; color:#fff; text-decoration:none;">Facebook</a> |
    <a href="#" style="margin:0 8px; color:#fff; text-decoration:none;">Instagram</a> |
    <a href="#" style="margin:0 8px; color:#fff; text-decoration:none;">Twitter</a>
  </div>
  
  <a href="https://www.youtube.com/watch?v=JoshuaSuperStoreDemo" target="_blank" 
     style="display:inline-block; background:#d00; color:#fff; padding:12px 28px; 
            border-radius:50px; font-size:16px; font-weight:bold; text-decoration:none;
            font-family: Arial, sans-serif; box-shadow:0 4px 12px rgba(0,0,0,0.3); 
            transition:background 0.3s ease;">
    ▶ Watch Video
  </a>
  
  <p style="margin-top:20px; font-size:14px; color:#bbb;">
    © 2025 Joshua Super Store. All rights reserved.
  </p>
</div>

<!-- ===== Floating Watch Video Button ===== -->
<a href="https://www.youtube.com/watch?v=JoshuaSuperStoreDemo" target="_blank" 
   style="position:fixed; bottom:15
```https://www.tiktok.com/@theonlyemiliaa/video/7343561047246228742?lang=en
