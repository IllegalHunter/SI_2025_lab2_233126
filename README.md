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
   
