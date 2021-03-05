# postman-collections
My Postman collections for testing purposes:
* [Randomization Testing of Filter Handler in Postman](https://adequatica.medium.com/randomization-testing-of-filter-handler-in-postman-5cc37432602c)
* [Brief Comparison of Responses in Postman](https://adequatica.medium.com/brief-comparison-of-responses-in-postman-aea23ee9d342)
* [Loop Through Array in Postman](https://adequatica.medium.com/loop-through-array-in-postman-f944a5265d62)
* «Astronomy Picture of the Day» based on [APOD NASA API](https://api.nasa.gov) to show how to generate data in the demanded format in JavaScript?
```
// https://stackoverflow.com/a/5511591
// Для указания даты относительно сегодняшнего числа (-1 — означает вчера):
let date = new Date(new Date().setDate(new Date().getDate() - 1));
// Если просто нужно сегодняшнее число, то:
// let date = new Date();
// В переменную date записывается время в формате:
// Wed Nov 25 2020 15:24:40 GMT+0300 (Moscow Standard Time)

// Если месяц надо преобразовать в MM (как 03):
let dateMM;
//  +1 делаем из-за того, что в JS месяцы начинаются с 0
if ((date.getMonth() + 1).length === 1){
	dateMM = `0${date.getMonth() + 1}`;
} else {
	dateMM = date.getMonth() + 1;
}
// Если дату надо преобразовать в DD (как 05):
let dateDD;
if (date.getDate() === 1) {
	dateDD = `0${date.getDate()}`;
} else {
	dateDD = date.getDate();
}
// Собираем дату вида: 2020-03-05
let dateDemanded = `${date.getFullYear()}-${dateMM}-${dateDD}`
```
