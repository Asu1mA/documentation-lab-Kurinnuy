# API OVERVIEW — Food Delivery API (демо)

Це приклад технічної документації для вигаданого API сервісу доставки їжі.
Base URL: `/api/v1`

---

## 1) GET /restaurants
Повертає список ресторанів.

### Приклад запиту
```http
GET /api/v1/restaurants
{
  "restaurants": [
    { "id": 1, "name": "Pizza House", "rating": 4.7, "deliveryTimeMin": 35 },
    { "id": 2, "name": "Sushi Go", "rating": 4.5, "deliveryTimeMin": 50 }
  ]
}
POST /api/v1/orders
Content-Type: application/json
{
  "restaurantId": 1,
  "items": [
    { "itemId": 101, "quantity": 2 }
  ],
  "deliveryAddress": "м. Київ, вул. Хрещатик, 10",
  "phone": "+380991112233",
  "paymentMethod": "card",
  "comment": "Подзвоніть за 5 хв до прибуття"
}
{
  "orderId": 9001,
  "status": "accepted",
  "estimatedDeliveryMin": 40
}
{
  "error": "VALIDATION_ERROR",
  "message": "Items list cannot be empty"
}
