## 🧠 JSX কি?
JSX এর পূর্ণরূপ হলো JavaScript XML। এটি দেখতে অনেকটা HTML-এর মতো হলেও, আসলে এটি JavaScript এর একটি সিনট্যাক্টিক সুগার (syntactic sugar) — যা React এ ব্যবহার করা হয় UI তৈরির জন্য।

JSX মূলত এমন একটি উপায়, যার মাধ্যমে আমরা JavaScript কোডের মধ্যেই HTML-এর মতো স্ট্রাকচার লিখতে পারি।
যেমন:
```
const element = <h1>Hello, world!</h1>;
```
এই কোড দেখতে HTML এর মতো হলেও, বাস্তবে এটা HTML না — এবং একে ব্রাউজার সরাসরি বুঝতে পারে না।

## কেন ব্রাউজার JSX বুঝতে পারে না?
ব্রাউজার কেবল তিনটি ভাষা বুঝতে পারে:

- HTML
- CSS
- JavaScript

JSX হলো JavaScript এর ওপর একটি এক্সটেনশন — তাই ব্রাউজার সরাসরি JSX রান করতে পারে না। এজন্য প্রয়োজন হয় একটি কম্পাইলার, যা JSX কে ব্রাউজারে বোঝার মতো ভ্যালিড JavaScript কোডে রূপান্তর করে দেয়।

## কে এই JSX কে JavaScript এ রূপান্তর করে?
JSX কে JavaScript এ রূপান্তর করার জন্য সাধারণত দুইটি টুল ব্যবহার হয়:

### Babel: 
সবচেয়ে জনপ্রিয় কম্পাইলার, যা JSX কে pure JS এ রূপান্তর করে।

### TypeScript (React with TSX): 
TypeScript এর JSX-compatible version — একে TSX বলে।

যখন তুমি React অ্যাপ বানাও (যেমন create-react-app দিয়ে), তখন এই Babel + Webpack বা Vite-এর মতো টুলগুলো তোমার JSX কোডকে JavaScript-এ কনভার্ট করে দেয় behind-the-scenes।

JSX কনভার্ট হওয়ার উদাহরণ:
JSX:
```
const element = <h1>Hello, world!</h1>;
```
Babel এটিকে রূপান্তর করে এমন JavaScript-এ:
```
const element = React.createElement("h1", null, "Hello, world!");
```