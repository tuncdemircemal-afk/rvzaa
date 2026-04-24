import streamlit as st

# Sayfa ayarlarını yapıyoruz (Tarayıcı sekmesinde isim yazsın)
st.set_page_config(page_title="Ravza'ya Özel ❤️", layout="wide", initial_sidebar_state="collapsed")

# Streamlit'in kendi gri arayüzünü gizleyip bizim pembe tasarımı eziyoruz
html_css = """
<style>
    /* Streamlit'in varsayılan üst menü ve alt yazılarını gizle */
    #MainMenu {visibility: hidden;}
    footer {visibility: hidden;}
    header {visibility: hidden;}
    
    /* Arka planı tamamen açık pembe yap */
    .stApp {
        background-color: #FFB6C1 !important;
    }

    /* Ortadaki ana yazı ayarı */
    .main-text {
        display: flex;
        justify-content: center;
        align-items: center;
        height: 70vh;
        font-size: 80px;
        color: #FF1493; /* Koyu pembe */
        font-family: 'Comic Sans MS', cursive, sans-serif;
        text-shadow: 2px 2px 4px rgba(0,0,0,0.2);
        z-index: 10;
        text-align: center;
    }

    /* Uçuşan emojiler için genel ayar */
    .emoji {
        position: fixed;
        font-size: 50px;
        animation: fall infinite linear;
        z-index: 5;
    }

    /* Düşme animasyonu */
    @keyframes fall {
        0% { top: -100px; opacity: 0; }
        10% { opacity: 1; }
        90% { opacity: 1; }
        100% { top: 100vh; opacity: 0; }
    }

    /* Emojilerin farklı hızlarda ve yerlerde düşmesi */
    .e1 { left: 10%; animation-duration: 5s; animation-delay: 0s; }
    .e2 { left: 30%; animation-duration: 7s; animation-delay: 2s; }
    .e3 { left: 50%; animation-duration: 6s; animation-delay: 1s; }
    .e4 { left: 70%; animation-duration: 8s; animation-delay: 3s; }
    .e5 { left: 90%; animation-duration: 5.5s; animation-delay: 0.5s; }
    .e6 { left: 20%; animation-duration: 9s; animation-delay: 4s; }
</style>

<div class="emoji e1">👶🏿</div>
<div class="emoji e2">🌹</div>
<div class="emoji e3">👶🏿</div>
<div class="emoji e4">🌹</div>
<div class="emoji e5">👶🏿</div>
<div class="emoji e6">🌹</div>

<div class="main-text">mal ravza 🥰</div>
"""

# HTML ve CSS'i Streamlit'in içine zorla basıyoruz (unsafe_allow_html=True bu işe yarar)
st.markdown(html_css, unsafe_allow_html=True)
