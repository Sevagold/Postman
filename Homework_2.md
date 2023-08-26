# POSTMAN
## _HOMEWORK 2_tests

- Protocol: http
- IP: 162.55.220.72
- Port: 5005

#### **Test 1**
***GET*** http://162.55.220.72:5005/first
1. Статус код 200
2. Проверить, что в body приходит правильный string.
```sh
pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});
pm.test("Body matches string", function () {
    pm.expect(pm.response.text()).to.include("This is the first responce from server!ss");
});
```
#### **Test 2**
***POST*** http://162.55.220.72:5005/user_info_3
1. Отправить запрос. 
2. Статус код 200
3. Спарсить response body в json.
4. Проверить, что name в ответе равно name s request (name вбить руками.)
5. Проверить, что age в ответе равно age s request (age вбить руками.)
6. Проверить, что salary в ответе равно salary s request (salary вбить руками.)
7. Спарсить request.
8. Проверить, что name в ответе равно name s request (name забрать из request.)
9. Проверить, что age в ответе равно age s request (age забрать из request.)
10. Проверить, что salary в ответе равно salary s request (salary забрать из request.)
11. Вывести в консоль параметр family из response.
12. Проверить что u_salary_1_5_year в ответе равно salary*4 (salary забрать из request)

```sh
var response = pm.response.json();
pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});
var response_body = JSON.parse;
pm.test("name correct", function () {
    pm.expect(response.name).to.eql("Seva");
});
pm.test("Age correct", function () {
    pm.expect(response.age).to.eql(null);
});
pm.test("Salary correct", function () {
    pm.expect(response.salary).to.eql(1000);
});
var request = request.data;
console.log(request)

pm.test("Name correct2 ", function () {
    pm.expect(response.name).to.eql(request.name);
});
pm.test("age correct2 ", function () {
    pm.expect(response.age).to.eql(request.age);
});
    pm.test("salary correct2", function () {
    pm.expect(response.salary).to.eql(+request.salary);
});
console.log(response.family)
 pm.test("salary correct*4", function () {
    pm.expect(response.family.u_salary_1_5_year).to.eql(request.salary*4);
});
```
#### **Test 2**
***POST*** http://162.55.220.72:5005/user_info_3
1. Отправить запрос.
2. Статус код 200
3. Спарсить response body в json.
4. Спарсить request.
5. Проверить, что name в ответе равно name s request (name забрать из request.)
6. Проверить, что age в ответе равно age s request (age забрать из request.)
7. Проверить, что salary в ответе равно salary s request (salary забрать из request.)
8. Вывести в консоль параметр family из response.
9. Проверить, что у параметра dog есть параметры name.
10. Проверить, что у параметра dog есть параметры age.
11. Проверить, что параметр name имеет значение Luky.
12. Проверить, что параметр age имеет значение 4.
```sh
var response = pm.response.json();
var request = request.data;
pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});
var response_body = JSON.parse;
console.log(request)
pm.test("Name correct2 ", function () {
    pm.expect(response.name).to.eql(request.name);
});
pm.test("age correct2 ", function () {
    pm.expect(response.age).to.eql(request.age);
});
    pm.test("salary correct2", function () {
    pm.expect(response.salary).to.eql(+request.salary);
});
console.log(response.family)
    pm.test("dog has name", function () {
    pm.expect(response.family.pets.dog).to.have.property('name');
});
    pm.test("dog has age", function () {
    pm.expect(response.family.pets.dog).to.have.property('age');
});
    pm.test("dog has name", function () {
    pm.expect(response.family.pets.dog.name).to.have.eql('Luky');
});
    pm.test("age is 4", function () {
    pm.expect(response.family.pets.dog.age).to.have.eql(4);
});
```
#### **Test 2**
***GET*** http://162.55.220.72:5005/user_info_4
1. Отправить запрос.
2. Статус код 200
3. Спарсить response body в json.
4. Спарсить request.
5. Проверить, что name в ответе равно name s request (name забрать из request.)
6. Проверить, что age в ответе равно age из request (age забрать из request.)
7. Вывести в консоль параметр salary из request.
8. Вывести в консоль параметр salary из response.
9. Вывести в консоль 0-й элемент параметра salary из response.
10. Вывести в консоль 1-й элемент параметра salary параметр salary из response.
11. Вывести в консоль 2-й элемент параметра salary параметр salary из response.
12. Проверить, что 0-й элемент параметра salary равен salary из request (salary забрать из request.)
13. Проверить, что 1-й элемент параметра salary равен salary*2 из request (salary забрать из request.)
14. Проверить, что 2-й элемент параметра salary равен salary*3 из request (salary забрать из request.)
15. Создать в окружении переменную name
16. Создать в окружении переменную age
17. Создать в окружении переменную salary
18. Передать в окружение переменную name
19. Передать в окружение переменную age
20. Передать в окружение переменную salary
21. Написать цикл который выведет в консоль по порядку элементы списка из параметра salary.
```sh
pm.test("Verify status 200", function()
{
pm.response.to.have.status(200);
});
var response_body = JSON.parse;
var request = request.data;
var response = pm.response.json();
var params = pm.request.url.query.toObject()

pm.test("name=name s request", function () {
pm.expect(response.name).to.eql(params.name);
});
pm.test("name=name s request", function () {
pm.expect(response.age).to.eql(+params.age);
});
console.log(params.salary)
console.log(response.salary)
console.log(response.salary[0])
console.log(response.salary[1])
console.log(response.salary[2])
pm.test("salary1 = sallary1", function () {
pm.expect(response.salary[0]).to.eql(+params.salary);
});
pm.test("salary= salary2x ", function () {
pm.expect(+response.salary[1]).to.eql(+params.salary*2);
});
pm.test("salary= salary3x ", function () {
pm.expect(+response.salary[2]).to.eql(+params.salary*3);
});
var name = response.name;
var age = response.age;
var salary = response.salary;
pm.environment.set("name", "Seva");
pm.environment.set("age", 24);
pm.environment.set("salary", 1000);
var step = 0;
while (step < 1) {
postman.setNextRequest(response.salary);
console.log(+response.salary[0]);
console.log(+response.salary[1]);
console.log(+response.salary[2]);
step++;
}
```






