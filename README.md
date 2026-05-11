export default function SportsBrandWebsite() {
  const products = [
    {
      name: 'Pro Cricket Bat',
      price: '₹4,999',
      image:
        'https://images.unsplash.com/photo-1624880357913-a8539238245b?q=80&w=1200&auto=format&fit=crop',
    },
    {
      name: 'Elite Football',
      price: '₹1,299',
      image:
        'https://images.unsplash.com/photo-1575361204480-aadea25e6e68?q=80&w=1200&auto=format&fit=crop',
    },
    {
      name: 'Volleyball Kit',
      price: '₹2,199',
      image:
        'https://images.unsplash.com/photo-1547347298-4074fc3086f0?q=80&w=1200&auto=format&fit=crop',
    },
    {
      name: 'Badminton Racket',
      price: '₹1,899',
      image:
        'https://images.unsplash.com/photo-1626224583764-f87db24ac4ea?q=80&w=1200&auto=format&fit=crop',
    },
  ];

  return (
    <div className="min-h-screen bg-gray-100 text-gray-900">
      {/* Header */}
      <header className="bg-black text-white sticky top-0 z-50 shadow-lg">
        <div className="max-w-7xl mx-auto flex items-center justify-between px-6 py-4">
          <h1 className="text-3xl font-bold tracking-wide">Apex Sports India</h1>
          <nav className="hidden md:flex gap-8 text-sm font-medium">
            <a href="#home" className="hover:text-yellow-400">Home</a>
            <a href="#products" className="hover:text-yellow-400">Products</a>
            <a href="#about" className="hover:text-yellow-400">About</a>
            <a href="#contact" className="hover:text-yellow-400">Contact</a>
          </nav>
          <button className="bg-yellow-400 text-black px-4 py-2 rounded-xl font-semibold hover:scale-105 transition">
            Shop Now
          </button>
        </div>
      </header>

      {/* Hero Section */}
      <section
        id="home"
        className="relative h-[85vh] flex items-center justify-center text-center bg-cover bg-center"
        style={{
          backgroundImage:
            "url('https://images.unsplash.com/photo-1517649763962-0c623066013b?q=80&w=1600&auto=format&fit=crop')",
        }}
      >
        <div className="absolute inset-0 bg-black/60"></div>
        <div className="relative z-10 px-6 max-w-3xl text-white">
          <h2 className="text-5xl md:text-7xl font-extrabold leading-tight mb-6">
            Premium Sports Gear for Champions
          </h2>
          <p className="text-lg md:text-xl text-gray-200 mb-8">
            High-quality volleyball, football, cricket, and badminton products delivered across India.
          </p>
          <div className="flex flex-wrap gap-4 justify-center">
            <button className="bg-yellow-400 text-black px-8 py-3 rounded-2xl font-bold hover:scale-105 transition">
              Explore Products
            </button>
            <button className="border border-white px-8 py-3 rounded-2xl font-bold hover:bg-white hover:text-black transition">
              Contact Us
            </button>
          </div>
        </div>
      </section>

      {/* Categories */}
      <section className="max-w-7xl mx-auto px-6 py-16">
        <div className="grid grid-cols-2 md:grid-cols-4 gap-6">
          {['Cricket', 'Football', 'Volleyball', 'Badminton'].map((sport) => (
            <div
              key={sport}
              className="bg-white rounded-3xl shadow-md p-8 text-center hover:shadow-2xl hover:-translate-y-1 transition"
            >
              <h3 className="text-2xl font-bold">{sport}</h3>
            </div>
          ))}
        </div>
      </section>

      {/* Products */}
      <section id="products" className="bg-white py-20 px-6">
        <div className="max-w-7xl mx-auto">
          <div className="flex items-center justify-between mb-12 flex-wrap gap-4">
            <div>
              <h2 className="text-4xl font-bold">Featured Products</h2>
              <p className="text-gray-600 mt-2">Top-selling products for athletes and sports lovers.</p>
            </div>
            <input
              type="text"
              placeholder="Search products..."
              className="border border-gray-300 rounded-xl px-4 py-3 w-full md:w-80"
            />
          </div>

          <div className="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-8">
            {products.map((product) => (
              <div
                key={product.name}
                className="bg-gray-50 rounded-3xl overflow-hidden shadow-md hover:shadow-2xl transition"
              >
                <img
                  src={product.image}
                  alt={product.name}
                  className="h-64 w-full object-cover"
                />
                <div className="p-5">
                  <h3 className="text-xl font-bold mb-2">{product.name}</h3>
                  <p className="text-lg text-gray-700 mb-4">{product.price}</p>
                  <button className="w-full bg-black text-white py-3 rounded-xl font-semibold hover:bg-yellow-400 hover:text-black transition">
                    Add to Cart
                  </button>
                </div>
              </div>
            ))}
          </div>
        </div>
      </section>

      {/* Payment Section */}
      <section className="max-w-7xl mx-auto px-6 py-20">
        <div className="bg-black text-white rounded-[32px] p-10 md:p-16 grid md:grid-cols-2 gap-10 items-center">
          <div>
            <h2 className="text-4xl font-bold mb-6">Secure Online Payments</h2>
            <p className="text-gray-300 text-lg leading-relaxed">
              Accept payments through Razorpay, UPI, Credit/Debit Cards, Net Banking, and Paytm for fast and secure online orders.
            </p>
          </div>
          <div className="grid grid-cols-2 gap-4">
            {['UPI', 'Razorpay', 'Paytm', 'Visa / MasterCard'].map((method) => (
              <div
                key={method}
                className="bg-white/10 backdrop-blur-md rounded-2xl p-6 text-center text-lg font-semibold"
              >
                {method}
              </div>
            ))}
          </div>
        </div>
      </section>

      {/* About */}
      <section id="about" className="bg-gray-900 text-white py-20 px-6">
        <div className="max-w-5xl mx-auto text-center">
          <h2 className="text-4xl font-bold mb-6">About Apex Sports India</h2>
          <p className="text-lg text-gray-300 leading-relaxed">
            We are an India-based sports brand dedicated to delivering premium-quality sports equipment and accessories for athletes, schools, academies, and sports enthusiasts. Our mission is to inspire performance and confidence through reliable products.
          </p>
        </div>
      </section>

      {/* Contact */}
      <section id="contact" className="py-20 px-6 bg-white">
        <div className="max-w-4xl mx-auto bg-gray-100 rounded-[32px] p-10 shadow-lg">
          <h2 className="text-4xl font-bold mb-8 text-center">Contact Us</h2>
          <div className="grid md:grid-cols-2 gap-6">
            <input
              type="text"
              placeholder="Your Name"
              className="px-4 py-4 rounded-xl border border-gray-300"
            />
            <input
              type="email"
              placeholder="Email Address"
              className="px-4 py-4 rounded-xl border border-gray-300"
            />
            <input
              type="text"
              placeholder="Phone Number"
              className="px-4 py-4 rounded-xl border border-gray-300 md:col-span-2"
            />
            <textarea
              placeholder="Your Message"
              rows="5"
              className="px-4 py-4 rounded-xl border border-gray-300 md:col-span-2"
            ></textarea>
          </div>
          <button className="mt-6 w-full bg-black text-white py-4 rounded-2xl text-lg font-semibold hover:bg-yellow-400 hover:text-black transition">
            Send Inquiry
          </button>
        </div>
      </section>

      {/* Footer */}
      <footer className="bg-black text-gray-400 py-8 text-center">
        <p>© 2026 Apex Sports India. All rights reserved.</p>
      </footer>
    </div>
  );
}

