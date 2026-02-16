let selected = null;
let price = 0;

function selectPackage(diamonds, amount) {
  document.querySelectorAll('.card').forEach(card => {
    card.classList.remove('active');
  });

  event.target.classList.add('active');
  selected = diamonds;
  price = amount;

  document.getElementById("selectedPackage").innerText =
    diamonds + " Diamonds";
  document.getElementById("price").innerText = price;
}

function checkout() {
  const player = document.getElementById("playerId").value;
  const server = document.getElementById("serverId").value;

  if (!player || !server || !selected) {
    alert("Please complete all details");
    return;
  }

  alert("Order placed! Diamonds will be delivered shortly.");
}