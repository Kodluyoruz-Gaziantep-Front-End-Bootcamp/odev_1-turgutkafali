# 1.HAFTA ÖDEVİ

``````let arr1 = ['2', 'a', '3', 3, 4, 3, 5, 5]
let arr2 = ['c', 'c', 'h', 1, 1, 1, 4]
let arr3 = [
    { name: 'ali', id: 221 },
    { name: 'veli', id: 343 },
    { name: 'konya', id: 333 },
    { name: 'ali', id: 664 },
    { name: 'selim', id: 112 }
]
let arr4 = [1, 1, 1, 4, 5, 5, 3, 2]
/* 
1- arr1 başına 'a' elemanını ekleyiniz
2- arr1 sonuna 6 elemanını ekleyiniz
3- arr1 sonundaki elemanı siliniz
4- arr1 başındaki elemanı siliniz
5- arr1 ile arr2 arraylerini iki farklı yöntemle birleştiriniz
6- kendisine gönderilen arrayde verilen elemanın olup olmadığını bulan array ve 
    aranan eleman olmak üzere iki parametre alan ve geriye boolean değer döndüren bir fonksiyon yazınız
    ve bu fonkisiyona arr2 ve 'h' parametresini verip çağırınız
7- arr2 içindeki 'h' elemanın indexsini bulunuz
8- arr2 nin eleman sayısını 3 adete 2 faklı yöntemle düşrünüz
9- kendisine verilecek array elemanlarını döngü ile dönüp, array içindeki number
    değerlerinin toplamını geriye dönen bir fonkiyon yazınız ve arr1 değeri ile çağırınız   
10- arr1 elemanlarını string değere çeviren bir map fonksiyonu yazınız    
11- arr3 içindeki id değeri 221 olan elemanı bulunuz
12- arr3 içindeki user değerleri ali olan elemanları bulunuz
13- arr3 içindeki elemanlarının id değerlerinin toplamlarını bulan bir reduce fonsiyonu yazınız

her sorunun cevabını console.log ile yazıdırın
*/

// 1- arr1 başına 'a' elemanını ekleyiniz
arr1.unshift("a");
console.log(arr1);

//2- arr1 sonuna 6 elemanını ekleyiniz
arr1.push(6);
console.log(arr1);

//3- arr1 sonundaki elemanı siliniz
arr1.pop();
console.log(arr1);

//4- arr1 başındaki elemanı siliniz
arr1.shift();
console.log(arr1);

//5- arr1 ile arr2 arraylerini iki farklı yöntemle birleştiriniz
let arr5 = arr1.concat(arr2);
console.log(arr5);
let arr6 = [...arr1, ...arr2];
console.log(arr6);

// 6- kendisine gönderilen arrayde verilen elemanın olup olmadığını bulan array ve
//     aranan eleman olmak üzere iki parametre alan ve geriye boolean değer döndüren bir fonksiyon yazınız
//     ve bu fonkisiyona arr2 ve 'h' parametresini verip çağırınız
const check = (arr, el) => {
  return arr.includes(el);
};
console.log(check(arr2, "h"));

//7- arr2 içindeki 'h' elemanın indexsini bulunuz
console.log(arr2.indexOf("h"));

//8- arr2 nin eleman sayısını 3 adete 2 faklı yöntemle düşrünüz
console.log(arr2.splice(0, 3));

let item = arr2.filter((value) => {
  return value > 0;
});
console.log(item);

// 9- kendisine verilecek array elemanlarını döngü ile dönüp, array içindeki number
//     değerlerinin toplamını geriye dönen bir fonkiyon yazınız ve arr1 değeri ile çağırınız
const sum1 = (sum) => {
  return sum.reduce(
    (s1, s2) =>
      typeof s1 === "number" && (typeof s2 === "number" ? s1 + s2 : 0),
    0
  );
};
console.log(sum1(arr1)) ;

//10- arr1 elemanlarını string değere çeviren bir map fonksiyonu yazınız
function result(arr) {
  arr.map((item) => {
    let i = item.toString();
    console.log(typeof i);
  });
}
result(arr1);

//11- arr3 içindeki id değeri 221 olan elemanı bulunuz
console.log(arr3[0]);

let i = arr3.filter((item) => item.id === 221);
console.log(i);

//12- arr3 içindeki user değerleri ali olan elemanları bulunuz
let e = arr3.filter((item) => item.name === "ali");
console.log(e);

//13- arr3 içindeki elemanlarının id değerlerinin toplamlarını bulan bir reduce fonsiyonu yazınız
const sumFunc = () => {
  let arrId = [];
  arr3.map((item) => arrId.push(item.id));

  return arrId.reduce((acc, value) => acc + value);
};
console.log(sumFunc());``````



# DESCRİPTİON

Bu ödevi JS Array meetotlarını kullanarak tamamladım. 


# AUTHOR

Turgut KAFALI
