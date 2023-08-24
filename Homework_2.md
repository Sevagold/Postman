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



