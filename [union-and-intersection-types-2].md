সূচনা:
TypeScript এ Union এবং Intersection দুই ধরনের Type আছে। 
Union (|) দিয়ে একাধিক Type এর মধ্যে যেকোনো একটি ব্যবহার করা যায়। আর Intersection (&) দিয়ে দুই বা তার বেশি Type একসঙ্গে ব্যবহার করা যায়।
union type:
type id = string | number;
let userid:id =100;
userid= "nahid-100";

intersction type:

type Name = {
  name: string;
};
type Age = {
  age: number;
};
type Student = Name & Age;
const student: Student = {
  name: "newz",
  age: 22
};

উদাহরণ :
ধরি 
একটা কোম্পানিতে দুই ধরনের কর্মচারী আছে। 
একজন Developer আরেকজন Designer। .

type Person = { name: string };
type Developer = { skill: string };
type Designer = { tool: string };
type Employee = Person & (Developer | Designer);

const emp1: Employee = {
  name: "newaz",
  skill: "JavaScript"
};

const emp2: Employee = {
  name: "nahid",
  tool: "Figma"
};

এখানে Person দিয়ে সবার নাম রাখা হয়েছে। Developer | Designer দিয়ে বোঝানো হয়েছে একজন কর্মচারী Developer অথবা Designer হতে পারবে। 
আর & দিয়ে Person
এর তথ্যের সঙ্গে অন্য একটি Type যোগ করা হয়েছে।

ব্যবহারের পার্থক্য:

Union এবং Intersectionএর মধ্যে মূল পার্থক্য হলো তাদের কাজের ধরন। Union ব্যবহার করলে একাধিক Type এর মধ্যে যেকোনো একটি Type ব্যবহার করা যায়। অন্যদিকে
Intersection ব্যবহার করলে সবগুলো Type-এর Property একসঙ্গে পাওয়া যায়। তাই প্রয়োজন অনুযায়ী এগুলো ব্যবহার করলে Code সহজে সাজানো যায়।


উপসংহার : 
Union দিয়ে একাধিক Type থেকে যেকোনো একটি নেওয়া যায়।
 আর Intersection দিয়ে একাধিক Type-এর তথ্য একসঙ্গে রাখা যায়। এই দুটো একসঙ্গে ব্যবহার করলে একই Code দিয়ে বিভিন্ন ধরনের তথ্য সহজে রাখা যায়।