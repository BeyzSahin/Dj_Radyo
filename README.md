# 🎧 DJ-Radyo: Duyguya Göre DJ Anonsu + Şarkı + Renk Teması

DJ-Radyo, kullanıcının seçtiği ruh haline göre yapay zeka destekli DJ anonsları üreten, duygusal uyumlu şarkılar ve renk temaları öneren bir web uygulamasıdır.  
Bu proje, `flan-t5-small` modeli üzerine Türkçe olarak fine-tune edilmiş bir model ile geliştirilmiştir.

---

## 🚀 Özellikler

- 🎙️ DJ tarzı yaratıcı anons üretimi
- 🎵 Duyguya göre Spotify şarkı önerisi
- 🌈 Ruh halini yansıtan renk ve açıklama teması
- 💬 Çoklu duygu seçimi desteği
- 🖥️ Gradio arayüzü ile web uygulaması

---

## 🧠 Kullanılan Teknolojiler

- Python 3.11
- [Transformers (Hugging Face)](https://huggingface.co/docs/transformers/)
- [Gradio](https://www.gradio.app/)
- Google Colab
- Google Drive (model depolama)

---

## 📦 Kurulum

```bash
pip install transformers gradio
```

Google Colab kullanıyorsanız Google Drive bağlantısı kurmanız gerekir:

```python
from google.colab import drive
drive.mount('/content/drive')
```

---

## 📁 Proje Dosya Yapısı

```
📁 dj_radyo
├── app.py                        # Gradio arayüz ve sistem fonksiyonu
├── sarki_veritabani.py          # Duyguya göre şarkı verileri
├── renk_anlam.py                # Renk - duygu eşleşmeleri ve anlamlar
├── dj_model_flan_t5/            # Fine-tuned Türkçe T5 modeli
└── README.md                    # Proje tanıtımı
```

---

## 🧪 Model Yükleme (Google Colab)

```python
from transformers import AutoTokenizer, AutoModelForSeq2SeqLM

model_path = "/content/drive/MyDrive/dj_model_flan_t5"
tokenizer = AutoTokenizer.from_pretrained(model_path, local_files_only=True)
model = AutoModelForSeq2SeqLM.from_pretrained(model_path, local_files_only=True)
```

---

## 💡 Kullanım

```bash
python app.py
```

Veya Colab üzerinde:

```python
interface.launch(share=True)
```

---

## 🔮 Örnek

- **Seçilen Duygular:** hüzünlü, nostaljik  
- **DJ Anonsu:**  
  > 🎙️ DJ kabininden tüm frekanslara selam! Ruhunla aynı tondayız. İçinde sakladığın her şey birazdan melodilere dönüşecek... 🎶

- **🎵 Şarkı:** Cem Kısmet - Kızım  
- **🌈 Renk Teması:** Mavi (Sakinlik ve huzur)

---

## 📚 Kaynaklar

- [MT5 Modeli](https://huggingface.co/google/mt5-small)
- [Gradio Belgeleri](https://www.gradio.app)
- [Transformers Belgeleri](https://huggingface.co/docs/transformers/)

---

## 👩‍💻 Geliştirici

**Beyza Şahin**  
OSTİM Teknik Üniversitesi — Yapay Zeka Mühendisliği  
2024 Final Projesi
