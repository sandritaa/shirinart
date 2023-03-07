# MadalasArt

MadalasArt is a web application that allows for an artist to showcase and sell their artwork. As an artist, you can upload your art pieces to the web application using the Cloudinary API and sell them through your own personalized virtual gallery. You can also view all the orders you have in place and send order updates directly to your customer’s inbox using the Twilio SendGrid API. As a customer, you can view the artist gallery and purchase a multiple items from the artist in one transaction. As a subscribed customer, you are also able to like different art pieces and keep track of your orders.

![alt text](/static/styles/img/img7.png)

## About the developer

MadalasArt was created by Sandra. Learn more about the developer on [LinkedIn](https://www.linkedin.com/in/sandramilenan/).

## Tech stack

- **Database:** PostgreSQL, SQLAlchemy
- **Backend:** Python 3, Flask
- **Frontend:** JavaScript, Jinja2, Bootstrap, HTML, CSS

### Dependencies

- Python packages:
  - SQLAlchemy
  - Flask
- APIs/external data sources:
  - Cloudinary API
  - Twilio SendGrid API
- Browser/client-side:
  - Bootstrap
  - Cloudinary Upload Widget

## Features

### Login as an artist

After having followed the installation instructions listed further down, you can login using as credentials:

- Email: shirin@gmail.com
- Password: testtest

Once you login as an artist, you can access the admin page from where it is possible to:

- Add a new item to the gallery using the Cloudinary API
- Remove an item from the gallery
- Update an order status; this will automatically send an update via email to the customer using the Twilio SendGrid API

### Login as a customer

You can login as a customer using as credentials:

- Email: john@gmail.com
- Password: testtest

Once you are logged in as a customer you can browse around the artist gallery to admire the art and do some of the following things:

- Like items
- Add items to the cart

You can then proceed to checkout by clicking on the cart and create new order(s) by entering your shipping, billing and payment details. Before proceeding to checkout, you still have the possibility to remove items from the cart if you change your mind. Note that the transaction is at this stage a fake transaction.

You can then click on profile and keep track of your previous orders, which artists you are following and which items you liked.

You can also shop if you are not logged in as a customer but you will not be able to like items and follow artists.

Please enjoy browsing around Galleria Milena.

## Installation

### Requirements:

- PostgreSQL
- Python 3.10.8
- Twilio SendGrid API keys

To run this web app on your local machine, follow these instructions.

Clone the repository:

```
git clone https://github.com/sandritaa/galleriamilena.git
```

Create a virtual environment:

```
virtualenv env
```

Activate the virtual environment:

```
source env/bin/activate
```

Install dependencies:

```
pip install -r requirements.txt
```

Create a file called `keys.py` at the top level and and get your [Twilio SendGrid API](https://sendgrid.com) keys. Then place your keys (`$API_KEY`) inside the file `keys.py`. The file should look as follows:

```
import os
os.environ['SENDGRID_KEY'] = '$API_KEY'
```

You can then create and seed the PostgreSQL database using some dummy data by running the following command:

```
python3 seeddb.py
```

Now you can start the server with:

```
python3 server.py
```

Finally, follow the link to open the application.

## Upcoming features

- **Stripe API**: Integrate API to enable real transactions
- **Order Tracker**: Enable to search for orders and view status based on order number
