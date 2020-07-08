# Table of contents
- [About](#-about)
- [Main libs and techs used](#-main-libs-and-techs-used)
- [Downloading and setting up the project](#-downloading-and-setting-up-the-project)
- [Expected routes](#-expected-routes)
- [License & copyright](#-license-&-copyright)

## 📄 About

This project was done during a Rocketseat's GoStack bootcamp challenge. It is a NodeJS server that stores transactions locally.

---

## 👨‍💻 Main libs and techs used

The project was developed using the following techs:

- [NodeJS](https://nodejs.org/en/)
- [uuidv4](https://www.npmjs.com/package/uuidv4)
- [insomnia](https://insomnia.rest/)

---

## Downloading and setting up the project

Simply clone this template or download it to your device and run the command **yarn** on your terminal to install all required dependencies.
To make sure erything is running properly, run **yarn test**.
To run the server, run the command **yarn dev:server**.
To test the routes, I recommend using the [insomnia](https://insomnia.rest/) app.

---

## Expected routes

- `POST /transactions`: This route should receive a `title`, `value` and `type` inside the requistion body, note that `type` is the transaction type. The transaction type `income` should be used for deposits and `outcome` for withdraws. When storing a new transaction, it should be submitted in the following format.

```json
{
  "id": "uuid",
  "title": "Salário",
  "value": 3000,
  "type": "income"
}
```
- `GET /transactions`: This route must return an object with a list of all the transactions that were registered while the server is running, along with another object containing the **incomes - outcomes**, represented in the object `"balance"` as `"total"`. See the example below:

```json
{
  "transactions": [
    {
      "id": "uuid",
      "title": "Salário",
      "value": 4000,
      "type": "income"
    },
    {
      "id": "uuid",
      "title": "Freela",
      "value": 2000,
      "type": "income"
    },
    {
      "id": "uuid",
      "title": "Pagamento da fatura",
      "value": 4000,
      "type": "outcome"
    },
    {
      "id": "uuid",
      "title": "Cadeira Gamer",
      "value": 1200,
      "type": "outcome"
    }
  ],
  "balance": {
    "income": 6000,
    "outcome": 5200,
    "total": 800
  }
}
```
## License & copyright

Developed by Pedro Igor C. de Oliveira.

Licensed under the [MIT License](LICENSE).
