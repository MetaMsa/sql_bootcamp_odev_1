/*
Çalışanların sadece FirstName, LastName ve Salary bilgilerini getiren bir SQL sorgusu yazın.
SELECT komutunun aldığı argüman sütunları ve from komutunun aldığı argüman tabloları belirtir.
*/
SELECT FirstName , LastName , Salary FROM employees;
/*
Çalışanların çalıştıkları departmanları benzersiz olarak listeleyen bir SQL sorgusu yazınız. 
DISTINCT komutu tekrarlayan öğeleri tekil sayar ve join komutu employees tablosunda departmentid sütun değerini departments tablosunda arar.
*/
SELECT DISTINCT departments.departmentname FROM employees JOIN departments ON employees.departmentid = departments.departmentid;
/*
Sadece IT departmanında çalışanların bilgilerini getiren bir SQL sorgusu yazınız. 
Employees tablosunda departmentid değeri departments tablosunda IT'nin departmentid değeri ile eşleşen girdileri listeler.
*/
SELECT * FROM employees JOIN departments ON employees.departmentid = departments.departmentid WHERE departments.departmentname = 'IT';
/*
Çalışanları maaşlarına göre büyükten küçüğe sıralayan bir SQL sorgusu yazınız.
ORDER BY maaş sütununa göre DESC yani azalan sırayla sıralama yapar.
*/
SELECT * FROM employees ORDER BY salary DESC;
/*
Çalışanların FirstName ve LastName alanlarını birleştirerek, tam adlarını içeren yeni bir kolon 
oluşturan bir SQL sorgusu yazınız.
CONCAT yani birleştirme string değerleri AS komutunun argümanına birleştirir.
*/
SELECT CONCAT(firstname, ' ', lastname) AS fullname FROM employees;