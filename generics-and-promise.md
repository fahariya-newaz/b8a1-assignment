সূচনা:
Generics হলো TypeScript এর একটি ফিচার যার মাধ্যমে একই Function বিভিন্ন Data Type নিয়ে কাজ করতে পারে। এতে বারবার আলাদা Function লেখার প্রয়োজন হয় না। 
সাধারণত T দিয়ে Generic Type বোঝানো হয়

Generics কিভাবে কাজ করে:

Generics ব্যবহার করে আমরা Function এর মধ্যে Type Parameter হিসেবে পাঠাতে পারি। 

যেমন:

function identity<T>(value: T)
: T {
  return value;
}
 const numberResult = identity<number>(100);
 const stringResult = 
 identity<string>("nahid");

বিস্তারিত :

এখানে T হলো একটি Generic Type Parameter।

প্রথমবার Function এ 100 পাঠানো হয়েছে তাই এটি 
Number Type হিসেবে কাজ করছে।

দ্বিতীয়বার "nahid" পাঠানো হলো তাই এটি String Type হিসেবে কাজ করছে।

একই Function ব্যবহার করে আমরা একাধিক Data Type
 নিয়ে কাজ করতে পারছি।

Generics with Promise:

Promise হলো JavaScript এর একটি বিষয় যা Asynchronous কাজ শেষ হলে Result দেয়। TypeScript এ Promise <T> ব্যবহার করে আগে থেকেই বলে দেওয়া যায় যে Function থেকে কী ধরনের Result পাওয়া যাবে।

উদাহরণ:

async function getUser(): Promise<string> {
  return "Nahid";
}
getUser().then((user) => {
  console.log(user);
});

Explanation:
এখানে async ব্যবহার করে একটি Asynchronous Function তৈরি করা হয়েছে।
Promise <string> দিয়ে বোঝানো হয়েছে যে Function থেকে String Value পাওয়া যাবে।

Function টি "Nahid" নামে একটি String Return করছে।
.then() ব্যবহার করে Promise এর Result পাওয়া যাচ্ছে এবং সেটি Console এ দেখানো হচ্ছে।

API থেকে Data আনার সময়ও Generics কাজে লাগে। কারণ বিভিন্ন API থেকে বিভিন্ন ধরনের Data পাওয়া যায়। Generics ব্যবহার করলে সেই Data এর Type ঠিকভাবে নির্ধারণ করা যায়।

উপসংহার:

Generics ব্যবহার করলে একই Code দিয়ে বিভিন্ন Data Type নিয়ে কাজ করা যায়। আর Promise <T> ব্যবহার করলে Asynchronous Function থেকে কী ধরনের Data পাওয়া যাবে তা জানা যায়। দুটো একসঙ্গে ব্যবহার করলে API এর Data নিয়ে কাজ করা সহজ হয় এবং ভুল হওয়ার সম্ভাবনা কমে।