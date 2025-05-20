Mario Andonovski, 233126
Контролни точки во методот checkCart:
if (allItems == null)

for (int i = 0; i < allItems.size(); i++)

if (item.getName() == null || item.getName().length() == 0)

if (item.getPrice() > 300 || item.getDiscount() > 0 || item.getQuantity() > 10)

if (item.getDiscount() > 0)

if (cardNumber != null && cardNumber.length() == 16)

for (int j = 0; j < cardNumber.length(); j++)

if (allowed.indexOf(c) == -1)
