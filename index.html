const FOODS = {

biryani:{
id:"biryani",
name:"Chicken Biryani",
price:80,
category:"Rice",
emoji:"🍗",
description:"Aromatic basmati rice with tender chicken and delicious campus-style masala."
},

friedrice:{
id:"friedrice",
name:"Chicken Fried Rice",
price:80,
category:"Rice",
emoji:"🍳",
description:"Hot and tasty chicken fried rice prepared fresh for your campus table."
},

parotta:{
id:"parotta",
name:"Parotta",
price:20,
category:"Meals",
emoji:"🥞",
description:"Soft layered parotta served fresh and hot."
},

puff:{
id:"puff",
name:"Veg Puff",
price:20,
category:"Puffs",
emoji:"🥐",
description:"Crispy golden puff with tasty vegetable filling."
},

lemon:{
id:"lemon",
name:"Lemon Rice",
price:40,
category:"Rice",
emoji:"🍋",
description:"Fresh lemon rice with peanuts and mild spices."
},

curd:{
id:"curd",
name:"Curd Rice",
price:40,
category:"Rice",
emoji:"🥣",
description:"Cool and creamy curd rice, perfect for a quick campus lunch."
},

tomato:{
id:"tomato",
name:"Tomato Rice",
price:40,
category:"Rice",
emoji:"🍅",
description:"Flavourful tomato rice prepared with fresh spices."
},

meals:{
id:"meals",
name:"Mini Veg Meals",
price:60,
category:"Meals",
emoji:"🍛",
description:"A satisfying mini meal for a quick campus lunch."
},

juice:{
id:"juice",
name:"Bottled Fruit Juice",
price:12,
category:"Drinks",
emoji:"🧃",
description:"Chilled bottled fruit juice."
},

water:{
id:"water",
name:"Mineral Water",
price:10,
category:"Drinks",
emoji:"💧",
description:"Chilled bottled drinking water."
}

};


function getCart(){
return JSON.parse(localStorage.getItem("qb_cart") || "[]");
}


function saveCart(cart){
localStorage.setItem("qb_cart",JSON.stringify(cart));
updateCartCount();
}


function updateCartCount(){

const count=getCart().reduce((sum,item)=>sum+item.qty,0);

document.querySelectorAll("[data-cart-count]").forEach(el=>{
el.textContent=count;
});

}


function showToast(message){

const toast=document.getElementById("toast");

if(!toast)return;

toast.textContent=message;
toast.classList.add("show");

setTimeout(()=>{
toast.classList.remove("show");
},1800);

}


function addToCart(id,qty=1){

const food=FOODS[id];

if(!food)return;

const cart=getCart();

const existing=cart.find(item=>item.id===id);

if(existing){
existing.qty+=qty;
}else{
cart.push({
id:id,
qty:qty
});
}

saveCart(cart);

showToast(`${food.name} added to Smart Tray`);

}


function removeFromCart(id){

let cart=getCart();

cart=cart.filter(item=>item.id!==id);

saveCart(cart);

renderCart();

}


function changeQty(id,amount){

const cart=getCart();

const item=cart.find(item=>item.id===id);

if(!item)return;

item.qty+=amount;

if(item.qty<=0){
removeFromCart(id);
return;
}

saveCart(cart);

renderCart();

}


function getTotals(){

const cart=getCart();

const subtotal=cart.reduce((sum,item)=>{

const food=FOODS[item.id];

return sum+(food.price*item.qty);

},0);

const service=cart.length ? 2 : 0;

return{
subtotal,
service,
total:subtotal+service
};

}


function renderCart(){

const box=document.getElementById("cartItems");

const summary=document.getElementById("cartSummary");

if(!box)return;

const cart=getCart();

if(!cart.length){

box.innerHTML=`
<div class="success-card">
<div class="success-icon">🛒</div>
<h2>Your Smart Tray is empty</h2>
<p>Add something delicious from today's menu.</p>
<a href="menu.html" class="btn primary">Explore Menu</a>
</div>`;

if(summary)summary.innerHTML="";

return;

}


box.innerHTML=cart.map(item=>{

const food=FOODS[item.id];

return`
<div class="cart-row">

<div class="cart-img">${food.emoji}</div>

<div class="cart-info">
<h3>${food.name}</h3>
<p>₹${food.price} × ${item.qty}</p>
</div>

<div class="cart-actions">
<button onclick="changeQty('${item.id}',-1)">−</button>
<b>${item.qty}</b>
<button onclick="changeQty('${item.id}',1)">+</button>
</div>

<strong>₹${food.price*item.qty}</strong>

<button onclick="removeFromCart('${item.id}')">✕</button>

</div>`;

}).join("");


const totals=getTotals();

summary.innerHTML=`

<div class="summary-line">
<span>Food Total</span>
<b>₹${totals.subtotal}</b>
</div>

<div class="summary-line">
<span>Campus Service</span>
<b>₹${totals.service}</b>
</div>

<div class="summary-total">
<span>Grand Total</span>
<strong>₹${totals.total}</strong>
</div>

<a href="checkout.html" class="btn primary full">
Continue to Checkout →
</a>

`;

}


function renderMenu(){

const grid=document.getElementById("menuGrid");

if(!grid)return;

const searchInput=document.getElementById("menuSearch");

let category="All";

function draw(){

const search=(searchInput?.value || "").toLowerCase();

const foods=Object.values(FOODS).filter(food=>{

const categoryMatch=category==="All" || food.category===category;

const searchMatch=
food.name.toLowerCase().includes(search) ||
food.description.toLowerCase().includes(search);

return categoryMatch && searchMatch;

});


grid.innerHTML=foods.map(food=>`

<div class="food-card">

<a href="food.html?id=${food.id}">

<div class="food-img">${food.emoji}</div>

<div class="food-content">

<span class="tag">${food.category}</span>

<h3>${food.name}</h3>

<p>${food.description}</p>

<div class="food-bottom">

<strong>₹${food.price}</strong>

</div>

</div>

</a>

<div class="food-content" style="padding-top:0">

<button class="small-btn"
onclick="addToCart('${food.id}')">
+ Add
</button>

</div>

</div>

`).join("");

}


document.querySelectorAll(".chip").forEach(chip=>{

chip.addEventListener("click",()=>{

document.querySelectorAll(".chip").forEach(c=>c.classList.remove("active"));

chip.classList.add("active");

category=chip.dataset.cat;

draw();

});

});


searchInput?.addEventListener("input",draw);

draw();

}


function renderFoodDetails(){

const box=document.getElementById("foodDetails");

if(!box)return;

const params=new URLSearchParams(location.search);

const id=params.get("id") || "biryani";

const food=FOODS[id] || FOODS.biryani;

let qty=1;

box.innerHTML=`

<div class="detail-image">${food.emoji}</div>

<div class="detail-content">

<span class="tag">${food.category}</span>

<h1>${food.name}</h1>

<p>${food.description}</p>

<div class="detail-price">₹${food.price}</div>

<div class="qty">

<button id="minus">−</button>

<span id="foodQty">1</span>

<button id="plus">+</button>

</div>

<button id="detailAdd" class="btn primary full">
Add to Smart Tray
</button>

</div>
`;


document.getElementById("minus").onclick=()=>{

if(qty>1)qty--;

document.getElementById("foodQty").textContent=qty;

};


document.getElementById("plus").onclick=()=>{

qty++;

document.getElementById("foodQty").textContent=qty;

};


document.getElementById("detailAdd").onclick=()=>{

addToCart(food.id,qty);

};

}


function changeTable(){

const table=prompt("Enter your table number","T-12");

if(!table)return;

const value=table.toUpperCase();

localStorage.setItem("qb_table",value);

document.querySelectorAll("#currentTable,#heroTable").forEach(el=>{
el.textContent=`Table ${value.replace("TABLE ","")}`;
});

showToast(`Dining spot changed to ${value}`);

}


function loadTable(){

const table=localStorage.getItem("qb_table") || "T-12";

document.querySelectorAll("#currentTable,#heroTable").forEach(el=>{
el.textContent=`Table ${table.replace("TABLE ","")}`;
});

}


function checkout(){

const form=document.getElementById("checkoutForm");

if(!form)return;

const profile=JSON.parse(localStorage.getItem("qb_profile") || "{}");

const table=localStorage.getItem("qb_table");

if(profile.name){
document.getElementById("studentName").value=profile.name;
}

if(profile.reg){
document.getElementById("registerNo").value=profile.reg;
}

if(table){
document.getElementById("tableNo").value=table;
}


form.addEventListener("submit",e=>{

e.preventDefault();

if(!getCart().length){

showToast("Your Smart Tray is empty");

return;

}


const details={

name:document.getElementById("studentName").value.trim(),

reg:document.getElementById("registerNo").value.trim(),

table:document.getElementById("tableNo").value,

note:document.getElementById("note").value.trim()

};

localStorage.setItem("qb_checkout",JSON.stringify(details));

localStorage.setItem("qb_table",details.table);

location.href="payment.html";

});

}


function renderPayment(){

const summary=document.getElementById("paymentSummary");

if(!summary)return;

const totals=getTotals();

summary.innerHTML=`

<h2>Order Summary</h2>

${getCart().map(item=>{

const food=FOODS[item.id];

return`
<div class="summary-line">
<span>${food.name} × ${item.qty}</span>
<b>₹${food.price*item.qty}</b>
</div>`;

}).join("")}

<div class="summary-line">
<span>Campus Service</span>
<b>₹${totals.service}</b>
</div>

<div class="summary-total">
<span>Total</span>
<strong>₹${totals.total}</strong>
</div>

`;


document.getElementById("placeOrderBtn")?.addEventListener("click",placeOrder);

}


function placeOrder(){

const checkout=JSON.parse(localStorage.getItem("qb_checkout") || "{}");

const payment=document.querySelector("input[name='payment']:checked")?.value || "UPI";

const cart=getCart();

if(!cart.length){

showToast("Your Smart Tray is empty");

return;

}


const totals=getTotals();

const order={

id:"QB"+Date.now().toString().slice(-6),

date:new Date().toLocaleString(),

items:cart,

name:checkout.name || "Campus Student",

reg:checkout.reg || "",

table:checkout.table || localStorage.getItem("qb_table") || "T-12",

note:checkout.note || "",

payment:payment,

subtotal:totals.subtotal,

service:totals.service,

total:totals.total,

status:0

};


const orders=JSON.parse(localStorage.getItem("qb_orders") || "[]");

orders.unshift(order);

localStorage.setItem("qb_orders",JSON.stringify(orders));

localStorage.setItem("qb_current_order",order.id);

localStorage.setItem("qb_cart","[]");

location.href="confirmation.html";

}


function renderConfirmation(){

const box=document.getElementById("confirmationInfo");

if(!box)return;

const orders=JSON.parse(localStorage.getItem("qb_orders") || "[]");

const order=orders[0];

if(!order){

box.innerHTML="<p>No recent order found.</p>";

return;

}

box.innerHTML=`

<div class="summary-card">

<div class="summary-line">
<span>Order ID</span>
<b>${order.id}</b>
</div>

<div class="summary-line">
<span>Dining Table</span>
<b>${order.table}</b>
</div>

<div class="summary-line">
<span>Payment</span>
<b>${order.payment}</b>
</div>

<div class="summary-total">
<span>Total Paid</span>
<strong>₹${order.total}</strong>
</div>

</div>

`;

}


const STATUSES=[
"Order Placed",
"Preparing",
"Ready",
"Delivered"
];


function renderTracking(){

const box=document.getElementById("trackingCard");

if(!box)return;

const orders=JSON.parse(localStorage.getItem("qb_orders") || "[]");

const order=orders[0];

if(!order){

box.innerHTML=`
<div class="success-card">
<h2>No active order</h2>
<a href="menu.html" class="btn primary">Order Food</a>
</div>`;

return;

}


document.getElementById("trackingId").textContent=
`${order.id} · ${order.table}`;


box.innerHTML=STATUSES.map((status,index)=>{

const done=index<=order.status;

const current=index===order.status;

return`

<div class="track-item ${done?"done":""} ${current?"current":""}">

<div class="track-icon">
${done ? "✓" : index+1}
</div>

${index<STATUSES.length-1 ? `<div class="track-line"></div>` : ""}

<div class="track-text">

<h3>${status}</h3>

<p>${
index<order.status
?"Completed"
:
index===order.status
?"Current status"
:"Waiting"
}</p>

</div>

</div>`;

}).join("");


const button=document.getElementById("nextStatus");

if(order.status>=STATUSES.length-1){

button.textContent="Order Delivered ✓";

button.disabled=true;

}else{

button.textContent=`Move to "${STATUSES[order.status+1]}"`;

button.disabled=false;

button.onclick=()=>{

order.status++;

localStorage.setItem("qb_orders",JSON.stringify(orders));

renderTracking();

showToast(STATUSES[order.status]);

};

}

}


function renderOrders(){

const box=document.getElementById("ordersList");

if(!box)return;

const orders=JSON.parse(localStorage.getItem("qb_orders") || "[]");

if(!orders.length){

box.innerHTML=`
<div class="success-card">
<div class="success-icon">📦</div>
<h2>No orders yet</h2>
<p>Your Quick Bytes orders will appear here.</p>
<a class="btn primary" href="menu.html">Explore Menu</a>
</div>`;

return;

}


box.innerHTML=orders.map(order=>{

const status=STATUSES[order.status];

const items=order.items.map(item=>{

return `${FOODS[item.id].name} × ${item.qty}`;

}).join(", ");


return`

<div class="order-card">

<div class="order-head">

<div>
<b>${order.id}</b>
<small>${order.date}</small>
</div>

<span class="order-status">${status}</span>

</div>

<div class="order-items">
${items}
</div>

<div class="order-footer">

<strong>₹${order.total}</strong>

<a href="tracking.html" class="btn outline">
Track
</a>

</div>

</div>

`;

}).join("");

}


function loadProfile(){

const profile=JSON.parse(localStorage.getItem("qb_profile") || "{}");

const nameInput=document.getElementById("profileNameInput");

const regInput=document.getElementById("profileRegInput");

const tableInput=document.getElementById("profileTable");

if(!nameInput)return;

nameInput.value=profile.name || "";

regInput.value=profile.reg || "";

tableInput.value=profile.table || "T-12";

document.getElementById("profileName").textContent=
profile.name || "Campus Student";

document.getElementById("profileReg").textContent=
profile.reg || "Register number not added";


document.getElementById("saveProfile").onclick=()=>{

const data={

name:nameInput.value.trim(),

reg:regInput.value.trim(),

table:tableInput.value

};

localStorage.setItem("qb_profile",JSON.stringify(data));

localStorage.setItem("qb_table",data.table);

document.getElementById("profileName").textContent=
data.name || "Campus Student";

document.getElementById("profileReg").textContent=
data.reg || "Register number not added";

showToast("Profile saved successfully");

};

}


function feedback(){

const form=document.getElementById("feedbackForm");

if(!form)return;

form.addEventListener("submit",e=>{

e.preventDefault();

const rating=document.querySelector("input[name='rating']:checked")?.value || 3;

const text=document.getElementById("feedbackText").value;

localStorage.setItem("qb_feedback",JSON.stringify({
rating,
text,
date:new Date().toLocaleString()
}));

form.classList.add("hidden");

document.getElementById("feedbackSuccess").classList.remove("hidden");

});

}


document.addEventListener("DOMContentLoaded",()=>{

updateCartCount();

loadTable();

renderMenu();

renderFoodDetails();

renderCart();

checkout();

renderPayment();

renderConfirmation();

renderTracking();

renderOrders();

loadProfile();

feedback();

});
