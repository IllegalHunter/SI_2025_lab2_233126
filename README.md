Mario Andonovski, 233126
2. Контролни точки во методот checkCart:
if (allItems == null)

for (int i = 0; i < allItems.size(); i++)

if (item.getName() == null || item.getName().length() == 0)

if (item.getPrice() > 300 || item.getDiscount() > 0 || item.getQuantity() > 10)

if (item.getDiscount() > 0)

if (cardNumber != null && cardNumber.length() == 16)

for (int j = 0; j < cardNumber.length(); j++)

if (allowed.indexOf(c) == -1)

3. Цикломатска комплексност на овој код инзесува 8, ако одиме според формулата V(G)=E-N+2 каде N претставува бројот на нодови, а Е претставува edges
   Тоа значи дека имаме вкупно 20 нодови и 26 еџови па така 26-20+2=6+2=8. Предикантни точки има вкупно 8 бидејќи ги броиме разгранувањата и циклусите, па така на овој начин цикломатската комплексност ќе биде 8+1=9. Понекогаш според второто пресметување Ц. комплексност изнесува повеќе бидејќи директно ги броиме логичките гранки.
4. Мора да има мининмум 4 тест случаи за да се препокрие Every Statement Testing.
   -Првиот тест случај треба да провери дали имаме предмети во корпата, во случај да немаме треба да фрла исклучок тоа ќе го направиме ако не внесеме ниту еден предмет во корпата.
   -Вториот тест случај внесуваме валиден артикл, но без попуст и вредноста е помала од 300. Со ова имаме валиден артикл, но не се извршува if условот чиј резултат е да се намали вкупната сума за 30, се проверува бројот на картичка и се враќа резултат sum.
   Item item = new Item("Milk", 2, 50, 0.0);
List<Item> items = List.of(item);
String cardNumber = "1234567812345678";
   -Tретиот тест случај ги исполнува условите за валиден артикл, валиден попуст и валиден број на картичка со тоа се исполнуваат сите if услови
   Item item = new Item("Toaster", 1, 400, 0.1); 
List<Item> items = List.of(item);
String cardNumber = "1234567812345678";
   -Четвртиот тест случај е со внесување на валиден производ но со невалиден број на кратичка и со тоа ќе провериме дали фрла исклучок, односно дали е функционален делот за проверка на бројот на картичка.
   Item item = new Item("Chocolate", 1, 20, 0.0);
List<Item> items = List.of(item);
String cardNumber = "1234abcd5678efgh";
5. Според MUltiple condition критериуммот треба да се покријат сите можни случаи  при извршување на if условот. Со тоа пресметката на минимум тест случаи ќе се изврши според формулата 2ⁿ, каде n e бројот на различни услови па така ќе имаме минимум 8 тест случаи.
   Тест случаите на некој начин изгледаат како бинарен формат на броевите од 0 до 7
   TC1-"Item item = new Item("Chocolate", 1, 20, 0.0);" false || false || false
   TC2-"Item item = new Item("Chocolate", 15, 20, 0.0);" false || false || true
   TC3-"Item item = new Item("Chocolate", 5, 20, 3.5);"  false || true || false
   TC4-"Item item = new Item("Chocolate", 15, 20, 2.5);" false || true || true
   TC5-"Item item = new Item("Chocolate", 5, 305, 0.0);" true || false || false
   TC6-"Item item = new Item("Chocolate", 15, 320, 0.0);" true || false || true
   TC7-"Item item = new Item("Chocolate", 1, 350, 3.5);" true || true || false
   TC8-"Item item = new Item("Chocolate", 12, 400, 2.8);" true || true || true
   
