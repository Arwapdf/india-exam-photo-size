# India Exam Photo & Signature Size List (2026)

Photo, signature, thumb and document sizes for Indian online exam forms (NEET, JEE Main, CUET, UPSC, SSC, RRB, IBPS, SBI, AFCAT and CTET) in one place. The same data is in [`exam-photo-sizes.json`](exam-photo-sizes.json) for apps and scripts.

> Last checked: 16 November 2026. Rules can change every year. Always confirm the sizes in the official notification before you submit the form.

## Quick table

| Exam | Photo | Signature | Other |
|---|---|---|---|
| **IBPS / SBI** | 200 × 230 px, 20–50 KB | 140 × 60 px, 10–20 KB | Left thumb 240 × 240 px, 20–50 KB · Declaration 800 × 400 px, 50–100 KB |
| **NEET UG** | 10–200 KB | 4–30 KB | Postcard photo 4 × 6 inch, 10–200 KB · Finger impressions 10–200 KB |
| **JEE Main** | 10–200 KB | 10–100 KB | — |
| **CUET UG** | 10–200 KB | 10–50 KB | Certificate PDF 50–300 KB |
| **UPSC** | 20–200 KB | 20–100 KB (one image with 3 signatures) | — |
| **SSC** | Live photo in the form | About 4 × 2 cm, 10–20 KB | — |
| **RRB (Railway)** | Live photo in the form | At least 140 × 60 px, 30–49 KB | Some notices say 10–20 KB |
| **AFCAT 01/2027** | 100–200 KB | 80–150 KB | Thumb impression 50–100 KB (men left, women right) |
| **CTET** (Feb 2026 bulletin) | 3.5 × 4.5 cm, 10–100 KB | 3.5 × 1.5 cm, 3–30 KB | — |

## Resize your photo to the right size (free)

You can make a photo or signature fit these limits in your browser with the free [Exam Photo & Signature Resizer](https://www.arwapdf.com/exam-photo-resizer). It has ready presets for each exam, and the photo is not uploaded.

| Exam | Step-by-step guide |
|---|---|
| NEET UG | [NEET photo, postcard photo and signature size](https://www.arwapdf.com/blog/neet-photo-signature-size) |
| JEE Main | [JEE Main photo and signature size](https://www.arwapdf.com/blog/jee-main-photo-signature-size) |
| CUET UG | [CUET photo, signature and certificate size](https://www.arwapdf.com/blog/cuet-photo-signature-certificate-size) |
| UPSC | [UPSC photo and signature size](https://www.arwapdf.com/blog/upsc-photo-signature-size) |
| SSC | [SSC signature size](https://www.arwapdf.com/blog/ssc-signature-size) |
| RRB | [RRB railway signature size](https://www.arwapdf.com/blog/rrb-railway-signature-size) |
| IBPS / SBI | [Bank exam photo, signature, thumb and declaration size](https://www.arwapdf.com/blog/ibps-sbi-photo-signature-size) |
| AFCAT | [AFCAT 2027 photo, signature and thumb size](https://www.arwapdf.com/blog/afcat-photo-signature-thumb-size) |
| CTET | [CTET photo and signature size](https://www.arwapdf.com/blog/ctet-photo-signature-size) |
| JEE Main correction | [What you can change in the JEE Main correction window](https://www.arwapdf.com/blog/jee-main-correction-window-photo-signature) |

Other free tools that help with forms:
- [Compress image to 50 KB](https://www.arwapdf.com/compress-image-to-50kb)
- [Passport size photo maker](https://www.arwapdf.com/passport-photo)
- [Compress PDF](https://www.arwapdf.com/reduce-pdf-size) for certificates and marksheets

## हिंदी में

ऊपर की तालिका में NEET, JEE Main, CUET, UPSC, SSC, रेलवे (RRB) और बैंक (IBPS/SBI) फ़ॉर्म के लिए फ़ोटो और सिग्नेचर का साइज़ है। अपनी फ़ोटो सही KB में बदलने के लिए मुफ़्त [एग्ज़ाम फ़ोटो रिसाइज़र](https://www.arwapdf.com/hi/exam-photo-resizer) इस्तेमाल करें, या [NEET फ़ोटो साइज़ गाइड](https://www.arwapdf.com/hi/blog/neet-photo-signature-size-kaise-kare) पढ़ें। फ़ॉर्म भरने से पहले साइज़ हमेशा आधिकारिक नोटिफ़िकेशन में मिला लें।

## Using the data

`exam-photo-sizes.json` has one entry per exam with `kb_min`, `kb_max`, `pixels` where the exam gives them, a link to the guide and a ready resize link.

```js
const data = await fetch(
  'https://raw.githubusercontent.com/Arwapdf/india-exam-photo-size/main/exam-photo-sizes.json'
).then((r) => r.json());
const neet = data.exams.find((e) => e.exam.startsWith('NEET'));
console.log(neet.items); // photo, postcard photo, signature, finger impressions
```

## Contributing

Found a new notification or a wrong size? Open an issue or a pull request with a link to the official notice. Please add only sizes that the notice itself gives.

## License

The data is free to use under [CC0 1.0](LICENSE): copy it, change it, use it in your app. A link back is welcome but not required.

Maintained by [ArwaPDF](https://www.arwapdf.com), free PDF and photo tools for Indian forms.
