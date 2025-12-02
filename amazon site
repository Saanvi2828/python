import streamlit as st

st.set_page_config(page_title="Amazon Demo", layout="wide")

st.title("🛒 Amazon Demo Website")
st.write("This is a simple Streamlit mockup of an Amazon-style shopping page.")

# --- Search Bar ---
search_query = st.text_input("Search for products", "")

# --- Mock Product Data ---
products = [
    {
        "name": "Wireless Headphones",
        "price": 59.99,
        "rating": 4.5,
        "description": "Bluetooth over-ear headphones with noise cancellation.",
    },
    {
        "name": "Mechanical Keyboard",
        "price": 89.99,
        "rating": 4.7,
        "description": "RGB backlit keyboard with blue switches.",
    },
    {
        "name": "Smart Watch",
        "price": 129.99,
        "rating": 4.3,
        "description": "Fitness tracking smartwatch with heart-rate monitoring.",
    },
]

# --- Product Filtering ---
if search_query:
    products = [p for p in products if search_query.lower() in p["name"].lower()]

# --- Product Listing ---
st.subheader("Results")

for product in products:
    with st.container():
        st.markdown(f"### {product['name']}")
        st.write(product["description"])
        st.write(f"**Price:** ${product['price']}")
        st.write(f"⭐ Rating: {product['rating']}/5")
        st.button("Add to Cart", key=product["name"])
        st.markdown("---")

if not products:
    st.write("No products found.")
