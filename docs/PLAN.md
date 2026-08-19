# E-Commerce Backend API — Plan

## Models

### Category
- name — text, up to 80 characters
- slug — text, URL-friendly version of the name, unique

### Product
- name — text, up to 120 characters
- price — decimal with 2 values
- stock — whole nuumbers
- category — link to Category
- description — long text
- is_active — True/False

### Cart
- user — link to User (whose cart is this?)
- created_at — date/time

### CartItem
- cart — link to Cart
- product — link to Product
- quantity — whole numbers

## Endpoints

| Method | Endpoint | Description |
|---|---|---|
| GET | /api/products/ | List all products |
| GET | /api/products/5/ | Get one product |
| POST | /api/products/ | add one product |
| GET | /api/categories/ | list all categories |
| GET | /api/cart/ | list all cart |
| POST | /api/cart/items/ | add item in cart |
| DELETE | /api/cart/items/3/ | delete item 3 in cart |
| POST | /api/orders/ | put order |

## Design note

Why is `quantity` on CartItem instead of on Product?

ANSWER: ... Quantity of the item is cart