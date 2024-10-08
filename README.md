# Nakama'S

[Nakama'S](https://amazingsafari.haidar.dev) is an online store for one-piece products merchandise

Table of Contents:

- [Namkama's](#nakama's)
  - [Links](#links)
  - [Features](#features)
  - [UI Designs](#ui-designs)
    - [Home Page](#home-page)
  - [REST API Endpoints](#rest-api-endpoints)

## Links

- Website Live
  - Frontend: <https://nakama.endabelyu.store/>
  - Backend: <https://nakama-api.endabelyu.store/api>
- Repositories:
  - General: <https://github.com/Endabelyu/nakama-general>
  - Nakama's Web: <https://github.com/Endabelyu/nakama-api>
  - Nakama's API: <https://github.com/Endabelyu/nakama-web>

Inspirations:

- [Onepiece Store](https://onepiece.store/)

## Features

- Home page
  - Hero section
  - Products catalogue. Example: <https://onepiece.store/>
- Product page
  - Image
  - SKU (stock keeping unit)
  - Name
  - Price
  - Description
  - Add to cart form: quantity input & add to cart button
- Shopping cart page
  - Product items to buy
    - Image, name, price, quantity, total (price x quantity)
    - Remove item
  - Link: continue shopping, go to products catalogue
  - Link: checkout
- Checkout page
  - Order summary
    - Product items to buy
    - Grand total of all product items to buy
- Place order / transaction is being processed

## UI Designs

- Figma: <https://www.figma.com/design/luxhLAkLvGDRt5FxMB2FMn/Untitled?node-id=0-1&node-type=canvas&t=QNHsR2Y5VMMbDEh6-0>

### Home Page

<!-- <img alt="Home Page" src="./designs/home.jpg" width="400" /> -->

## Entity Relationship Diagram (ERD)

![ERD](./Diagram/Nakama.svg)

## REST API Endpoints

| Endpoint         | HTTP     | Description               |
| ---------------- | -------- | ------------------------- |
| `/products`      | `GET`    | Get all products          |
| `/products/:id`  | `GET`    | Get product by id         |
| `/products/seed` | `POST`   | Seed all initial products |
| `/products`      | `POST`   | Add new product           |
| `/products`      | `DELETE` | Delete all products       |
| `/products/:id`  | `DELETE` | Delete product by id      |
| `/products/:id`  | `PUT`    | Update product by id      |

### Product

```json
{
  "id": "abc123",
  "name": "Ace Neclacke",
  "price": 120000,
  "slug": "Ace-necklace",
  "imageUrl": "http://image.com/ace-necklace",
  "description": "Favourite necklace of Portgas D. Ace",
  "category": "necklace",
  "stock": 5,
  "createdAt": "23-11-2023",
  "updatedAt": "26-12-2023"
}
```

### Add New Product

Request Body:

```json
{
  "name": "Ace Neclacke",
  "price": 120000,
  "slug": "Ace-necklace",
  "imageUrl": "http://image.com/ace-necklace",
  "description": "Favourite necklace of Portgas D. Ace",
  "category": "necklace",
  "stock": 5
}
```

Response Body:

```json
{
  "name": "Ace Neclacke",
  "price": 120000,
  "slug": "Ace-necklace",
  "imageUrl": "http://image.com/ace-necklace",
  "description": "Favourite necklace of Portgas D. Ace",
  "category": "necklace",
  "stock": 5
}
```
