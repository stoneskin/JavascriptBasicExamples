# Basic Javascript  #
## Content ##
1. JavaScript in Web Pages
2. Variables and Types
3. Functions
4. Conditional Statements
5. Loops
6. JavaScript Usage



## 1.JavaScript in Web Pages ##
- _<script>_
- _src attribute_
- _<noscript>_
### 1.1 Script ##
```
<!DOCTYPE html>
<html>
  <head>
    <script>
    console.log('Hello!');
    </script>
  </head>
  <body>
    <h1>Our Page</h1>
    <script>
      console.log('In Body');
    </script>
    <script type="text/javascript" src="js/01-basic-1.js">
      console.log('Hello in Body!');
    </script>
  </body>
</html>
```
### 1.2 Noscript ###
```
<!DOCTYPE html>
<html>
  <head>
  </head>
  <body>
    <noscript>
      <h1>This application requires JavaScript.</h1>
    </noscript>
  </body>
</html>

```

## 2. Variables ##
- Fundamentals
- undefined
- PrimitiveTypes
- Object and Function Types
### 2.1 Defing variables ###
```
orderId= 9001;  //no var
console.log(orderId);
```
```
var orderId= 9001;  //def var
console.log(orderId);
```
```
var orderId = "ORD-9001";
console.log(orderId);
```
```
var orderId= "ORD-9001";
orderId= 1201;
console.log(orderId);
```
### 2.2 undefined ###
```
var orderId;
console.log(orderId); //undefined
```
** use stirict **
```
‘use strict’;
orderId= 9001;
console.log(orderId);  //error
```
### 2.3 Primitive TYPEs ###
- number string, NaN
```
var orderId1= 9001;
console.log(typeof orderId1);

var orderId2= 9001.01;
console.log(typeof orderId2);

var orderId3= "Ord-9001.01";
console.log(typeof orderId3);

var orderId4= "9001.01";
console.log(typeof orderId4)
```

- boolean
```
var isActive= true;
console.log(typeof isActive);
```

### 2.4 Object and Function Types ###
- object
```
var order = {
  orderId: 9001,
  isActive: true
};
console.log(typeof order);

var cancelledOrders= [9001, 9002, 9003];
console.log(typeof cancelledOrders);

var order = null;
console.log(typeof order);

```

- function
```
function cancelOrder(orderId) {
};
console.log(typeof cancelOrder);
```

## 3. Function Fundamentals ##
- Declaring Functions
- Arguments
- Returning Values
- Fnction Expressions

```
function printOrder() {
  console.log(‘Printing order.’);
};
printOrder();
```
```
function printOrder(orderId) {
  console.log(‘Printing order: ’ + orderId);
};
printOrder(‘9002’);
```
```
var getActivateOrder= function() {
  retrun "id";
};
console.log(typeof activateOrder);
getActivateOrder();

getActivateOrder; //nothing show
```

## 4. If and Switch Statements ##
```
var total = 99.99;
var freeShipping;
if(total >= 100.00)
  freeShipping= true;
else
  freeShipping= false;

console.log(freeShipping);
```

```
var orderType= 'business';
var shipMethod;

switch (orderType) {
  case'business':
    shipMethod= 'FedEx'; //be skipped
    // break;
  case 'personal':
    shipMethod= 'UPS Ground';
    break;
  default:
    shipMethod= 'USPS';
}
console.log(shipMethod);
```
## 5 Loop ##
### 5.1 while and do...while Statements ###
```
var lineItemCount= 3;
var currentItem= 0;
while(currentItem< lineItemCount) {
  console.log("item: "+ currentItem);
  currentItem++;
}
```
```
var lineItemCount= 3;
var currentItem= 0;
do {
  console.log("item: "+ currentItem);
  currentItem++;
} while(currentItem< lineItemCount);
```

### 5.2 for and for...in ###
- for
```
var lineItemCount= 3;
for(vari = 0; i < lineItemCount; i++)
  console.log(i);
```
- break
```
var lineItemCount= 5;
for(vari = 0; i < lineItemCount; i++) {
  console.log(i);
  if(i == 1)
  break;
}
```
- continue
```
var lineItemCount= 5;
for(vari = 0; i < lineItemCount; i++) {
if(i == 1)
  continue;
  console.log(i);
}
```
- for in
```
var lineItem= {
  product: 'Widget 1',
  quantity: 4,
  price: 9.50
};
for(varfield in lineItem)
  console.log(field + " : " + lineItem[field]);
```

## 6. JavsScript Usage Feature ##
- Case sensitive
```
varorderId= 5005;
console.log(OrderId);
```
- Comments
```
/*
console.log(1);
*/
console.log(2);
// console.log(3);
```
- Name
```
var@product = 'PRD-2000';
console.log(@product);

var 2product = 'PRD-2000';
console.log(2product);

var $product = 'PRD-4000'
$product += 'X2'
console.log($product)
```
