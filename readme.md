


# 🌟 Jubayer Talukdar — Personal Portfolio Website

এই রেপোজিটরিতে জুবায়ের তালুকদারের ব্যক্তিগত পোর্টফোলিও ওয়েবসাইটের সম্পূর্ণ কোড রয়েছে। এটি একটি একক এইচটিএমএল ফাইল (`index.html`) ভিত্তিক মিনিমালিস্ট, রেসপনসিভ এবং অ্যাসথেটিক ওয়েবসাইট।

---

## 📁 ১. ফাইল ও ফোল্ডার সিস্টেম (Directory Structure)

your-project-folder/

│

├── index.html # ওয়েবসাইটের মূল কোড (HTML, CSS & JS)

├── profile.jpg # মূল হোমপেজের প্রফেশনাল প্রোফাইল পিকচার

├── README.md # প্রজেক্টের নির্দেশিকা ও ডকুমেন্টেশন

│

└── photos/ # গ্যালারির সব ছবির ফোল্ডার

├── photo (1).jpg # Title: Last day of HSC

├── photo (2).jpg # Title: Going to coaching...

├── photo (3).jpg # Title: college

├── photo (4).jpg # Title: udvash classroom

└── photo (5).jpg # Title: visit to railline...

  


---

## ⚙️ ২. ওয়েবসাইট মেকানিজম (How It Works)

১. **Single Page Tab Navigation (Fade Effect):**
   * ওয়েবসাইটের কোনো পেজ রিফ্রেশ না করেই ডাইনামিকালি ট্যাবগুলো পরিবর্তন হয়।
   * `switchTab(tabId)` জাভাস্ক্রিপ্ট ফাংশন ব্যবহারের মাধ্যমে একটি ট্যাবস্মুথলি Fade Out হয়ে পরবর্তী ট্যাবটি Fade In হয়।

২. **Dynamic & Random Gallery (Shuffled Layout):**
   * পেজ রিফ্রেশ বা প্রথমবার লোড করার সময় JavaScript-এর `shuffle()` ফাংশন গ্যালারির ছবিগুলোর ক্রম র্যান্ডমলি পরিবর্তন করে দেখায়।

৩. **Lazy Loading & Blur-Up Progressive Effect:**
   * ছবি লোড হওয়ার সময় মূল পেজের পারফরম্যান্স উন্নত করতে Native `loading="lazy"` ব্যবহার করা হয়েছে।
   * ছবি সম্পূর্ণ লোড না হওয়া পর্যন্ত একটি ব্লাড (Blur) ইফেক্ট থাকে এবং লোড শেষ হলে `loaded` ক্লাস যুক্ত হয়ে সম্পূর্ণ স্পষ্ট হয়।

৪. **Image Lightbox Preview:**
   * গ্যালারির যেকোনো ছবি বা কার্ডে ক্লিক করলে একটি ফুল-স্ক্রিন পপ-আপ (Lightbox Modal) ওপেন হয় এবং ছবির আসল সাইজ ও কাস্টম ক্যাপশন দেখায়।

৫. **Live Search Filter:**
   * গ্যালারিতে টাইটেল অনুযায়ী রিয়েল-টাইম সার্চ করার সুবিধা রয়েছে। টাইপ করার সাথে সাথেই অনাকাঙ্ক্ষিত কার্ডগুলো হাইড হয়ে যায়।

৬. **Mobile Responsive & Social Links:**
   * ডেসটপে সোশ্যাল আইকনগুলো ডানপাশে ফিক্সড সাইডবার হিসেবে থাকে এবং মোবাইলে তা নিচে বটম বার হিসেবে স্ক্রিনে ফিক্সড হয়ে যায়।
   * `truejubayer` ইউজারনেমে ফেসবুক, এক্স (টুইটার), হোয়াটসঅ্যাপ, গিটহাব, ইউটিউব, ইনস্টাগ্রাম এবং ইমেইল লিঙ্ক যুক্ত করা আছে।

---

## 🛠️ ৩. ভবিষ্যতে কীভাবে আপডেট বা পরিবর্তন করবে?

### ক) গ্যালারিতে নতুন ছবি যোগ করতে:
১. তোমার ছবিটি `photos/` ফোল্ডারের ভেতর রাখো (যেমন: `photo (6).jpg`)।
২. `index.html` ফাইলের একদম নিচের দিকে থাকা `photosConfig` অ্যারেতে (Array) নতুন লাইন যোগ করো:
```javascript
const photosConfig = [
    { file: "photo (1).jpg", title: "Last day of HSC" },
    { file: "photo (2).jpg", title: "Going to coaching..." },
    { file: "photo (3).jpg", title: "college" },
    { file: "photo (4).jpg", title: "udvash classroom" },
    { file: "photo (5).jpg", title: "visit to railline..." },
    { file: "photo (6).jpg", title: "My New Photo Title" } // <--- নতুন ফটো এভাবে যোগ করবে
];