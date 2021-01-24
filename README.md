# Dynamic Website Design for a Manufacturing Company
## AIM:
To design a dynamic website for a chip manufacturing company.

## DESIGN STEPS:
### Step 1: 
Requirement collection.
### Step 2:
Creating the layout using HTML and CSS.
### Step 3:
Updating the sample content.
### Step 4:
Choose the appropriate style and color scheme.
### Step 5:
Validate the layout in various browsers.
### Step 6:
Validate the HTML code.
### Step 6:
Publish the website in the given URL.

## PROGRAM:

### base.html
```
{% load static %}
<!DOCTYPE html>
<html lang="en">

<head>
    <title>Hexabyte Private Limited</title>
    <link rel="stylesheet" href="{% static 'css/layout.css' %}">
    <link rel = "icon" href ="{% static 'css/img/hb.jpg' %}" type = "image/x-icon"> 
              
</head>

<body>
    <div class="container">
    <div class="banner">
       HEXABYTE PRIVATE LIMITED
    </div>
    <div class="menu">
        <div class="menuitem"><a href="/home">Home</a></div> 
        <div class="menuitem"><a href="/products">Products</a></div> 
        <div class="menuitem"><a href="/people">People</a></div>
        <div class="menuitem"><a href="/contact">Contact Us</a></div> 
    </div><div class="content">
    {% block content %}    
    {% endblock  %}
    </div>
    <div class="footer">
        Copyright © 2021 Hexabyte Private Limited, Developed by Divya Meenakshi
    </div>
    </div>
</body>

</html>
```

### home.html
```
{% extends "website/base.html" %}

{% block content %}
    <div class="homecontent">    
        <h1><u>ABOUT US</u></h1>
        <img src="/static/img/office.jpg" alt="office">
    
        <div class="contenttext">
            Hexabyte Pvt Ltd, provides a broad range of semiconductor and infrastructure software applications that serve the data center, networking, software, broadband, wireless, and storage and industrial markets. Common applications for its products include: data center networking, home connectivity, broadband access, telecommunications equipment, smartphones, base stations, data center servers and storage, factory automation, power generation and alternative energy systems, displays, and mainframe operations and management, and application software development. Some of Silicon's core technologies and products include:
            <ul>
                <li>Memory Chips</li>
                <li>SATA HDD</li>
                <li>SATA SSD </li>
                <li>Broadband Modems</li>
                <li>Wifi Devices</li>
                <li>Switching Devices</li>
                <li>Optical Sensors</li>
            </ul> 
        </div>
    </div>
{% endblock  %}
```
### products.html
```
{% extends "website/base.html" %}

{% block content %}
<div class="productcontent">
    <h1>Our Premium Products</h1>
    <div class="productitems">
        {% for products in productss %}
        <div class="productitem">
            <div class="itemimage">
                <img src="{{ products.photo.url }}" alt="product image" height="200" width="200">
            </div>
            <div class="productsname">{{ products.name }}</div>
            <div class="productsprice">{{ products.price }}</div>
        </div>
        {% endfor %}
    </div>
</div>
{% endblock  %}
```
### people.html
```

{% extends "website/base.html" %}

{% block content %}
<div class="peoplecontent">
    <h1>Our Crew</h1>
    <div class="crewmembers">
        {% for people in peoples %}
        <div class="crewmember">
            <div class="memberimage">
                <img src="{{ people.photo.url }}" alt="member image" height="250" width="200">
            </div>
            <div class="membername">{{ people.name }}</div>
            <div class="designation">{{ people.designation }}</div>
        </div>
        {% endfor %}
    </div>
</div>

{% endblock  %}
```
### contact.html
```
{% extends "website/base.html" %}

{% block content %}
    <div class="content">

        <p class="free">

        </p>
        <div class="contain">
            <div class="image">
                <img src="/static/img/cons.jpeg" alt="contact" width="1050" height="300">
            </div>
            <div class="text">
            <h2><u>CONTACT NO:</u><br>
                +822 34440105</h2>
            </div>
        </div>
        <div class="contain">
            <div class="image">
            </div>
            <div class="text">
                <h2><u>EMAIL:</u><br>
                hexabytepvt.ltd@gmail.com</h2>
            </div>
            <div class="text">
                <h2><u>ADDRESS:</u><br>
                42 Teheran-ro 108-gil, Daechi-dong,<br>
                Gangnam-gu, Seoul, South Korea
                </h2>
            </div>
        </div>
    </div>

{% endblock  %}
```



## OUTPUT:
![output](./static/img/o1.png)

![output](./static/img/op.png)

![output](./static/img/op2.png)

![output](./static/img/o3.png)

![output](./static/img/o4.png)

![output](./static/img/o5.png)

## ADMIN PAGE:
![output](./static/img/ad.png)

![output](./static/img/ad1.png)

![output](./static/img/ad2.png)


## CODE VALIDATION REPORT:
![output](./static/img/c1.png)

![output](./static/img/c2.png)

![output](./static/img/c3.png)

![output](./static/img/c4.png)
## RESULT:
Thus a website is designed for the chip manufacturing company and is hosted in the URL http://divya.student.saveetha.in:8000/. HTML code is validated.

##  REPOSITORY URL:
https://github.com/divyameenakshi24/companywebsitedynamic.git