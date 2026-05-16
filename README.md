# Rohit-Dabas-organic-farming-
content://com.google.android.apps.search.assistant.surfaces.voice.robin.fileprovider/attachments/index.html
<div class="lead-form-container" style="max-width: 500px; margin: 30px auto; padding: 25px; border: 2px solid #27ae60; border-radius: 12px; background: #fff; box-shadow: 0 10px 25px rgba(0,0,0,0.05);">
    <h3 style="color: #145a32; text-align: center; margin-bottom: 20px; font-family: 'Noto Sans Devanagari', sans-serif;">🌱 जैविक कृषि महाअभियान से जुड़ें</h3>
    
    <form id="whatsappForm" onsubmit="sendToWhatsapp(event)">
        <div style="margin-bottom: 15px;">
            <label style="display: block; margin-bottom: 5px; font-weight: 600;">आपका नाम (Full Name):</label>
            <input type="text" id="farmerName" required style="width: 100%; padding: 10px; border: 1px solid #cbd5e1; border-radius: 6px;">
        </div>
        
        <div style="margin-bottom: 15px;">
            <label style="display: block; margin-bottom: 5px; font-weight: 600;">मोबाइल नंबर (WhatsApp No.):</label>
            <input type="tel" id="farmerPhone" required style="width: 100%; padding: 10px; border: 1px solid #cbd5e1; border-radius: 6px;">
        </div>
        
        <div style="margin-bottom: 15px;">
            <label style="display: block; margin-bottom: 5px; font-weight: 600;">गांव और जिला (Village & District):</label>
            <input type="text" id="farmerLocation" required style="width: 100%; padding: 10px; border: 1px solid #cbd5e1; border-radius: 6px;">
        </div>

        <div style="margin-bottom: 20px;">
            <label style="display: block; margin-bottom: 5px; font-weight: 600;">आप किस रूप में जुड़ना चाहते हैं?</label>
            <select id="userRole" style="width: 100%; padding: 10px; border: 1px solid #cbd5e1; border-radius: 6px;">
                <option value="किसान (Farmer)">किसान (Farmer)</option>
                <option value="युवा / छात्र (Youth / Student)">युवा / छात्र (Youth / Student)</option>
                <option value="अन्य सहयोगी">अन्य सहयोगी</option>
            </select>
        </div>
        
        <button type="submit" style="width: 100%; background: #27ae60; color: white; border: none; padding: 12px; border-radius: 6px; font-size: 16px; font-weight: bold; cursor: pointer; display: flex; align-items: center; justify-content: center; gap: 10px;">
            <i class="fa-brands fa-whatsapp" style="font-size: 20px;"></i> मुहिम से जुड़ें (Send Details)
        </button>
    </form>
</div>

<script>
function sendToWhatsapp(event) {
    event.preventDefault();
    
    // डेटा कलेक्ट करना
    const name = document.getElementById('farmerName').value;
    const phone = document.getElementById('farmerPhone').value;
    const location = document.getElementById('farmerLocation').value;
    const role = document.getElementById('userRole').value;
    
    // व्हाट्सएप मैसेज का टेक्स्ट फॉर्मेट करना
    const baseText = `*🌱 जैविक कृषि महाअभियान - नई लीड *\\n\\n` +
                     `*नाम:* ${name}\\n` +
                     `*व्हाट्सएप नंबर:* ${phone}\\n` +
                     `*गांव/जिला:* ${location}\\n` +
                     `*श्रेणी:* ${role}\\n\\n` +
                     `मैं चौधरी रोहित सिंह डबास जी और योगी जी के ऑर्गेनिक फार्मिंग विज़न में आपके साथ जुड़ना चाहता हूँ।`;
                     
    const encodedText = encodeURIComponent(baseText);
    
    // आपके व्हाट्सएप नंबर पर रीडायरेक्ट करना
    const whatsappUrl = `https://wa.me/918630775134?text=${encodedText}`;
    
    // नए टैब में व्हाट्सएप खोलना
    window.open(whatsappUrl, '_blank');
    
    // इसके तुरंत बाद यूजर को आपके व्हाट्सएप चैनल पर भेज देना ताकि वो फॉलो भी कर ले
    setTimeout(() => {
        window.location.href = "https://whatsapp.com/channel/0029Vb7k6ZO77qVOk6S3BX2W";
    }, 1500);
}
</script>
