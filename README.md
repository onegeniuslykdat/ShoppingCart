# Shopping Cart
<h3> Backend services for a shopping cart built using ASP.NET.

The code contained in the zipped file are a set of APIs that can be consumed by a Shopping Cart client.

API URLs follow the form: {controller}/api/{action}/{param}; where param is one or more optional parameters. Parameters are passed as query strings. </h3>

<h4> Endpoints and URLs: </h4>
<br>
<h4>Product: Properties: [ProductID, "ProductName", Quantity, Price, "PictureURL", "OwnerEmail", "OutofStock"] </h4>
<ul>
  <li> product/api/getall        -  gets all products, requires no parameters. </li>
<li> product/api/get           -  gets a specific product, requires the integer id parameter. </li>
<li> product/api/posttocart    -  allows a customer to add a product to the cart, requires three integer parameters, prodid,custid, custqn. </li>
<li> product/api/post          -  creates a new product, requires 5 parameters, string n, integer q, integer pr, string u and string o. </li>
<li> product/api/update        -  updates a product, requires the same 6 parameters as above. </li>
<li> product/api/delete        -  deletes a product, reuires the integer id parameter </li>
</ul>

<h4> Customer : Properties: [CustomerID, "CustomerName", "CustomerPhone", Price, "pwd", "CustomerEmail"] </h4>
<ul>
<li> customer/api/signin       -  gets a specific customer after signing in, requires two string parameters, e and w. </li>
<li> customer/api/signup       -  creates a new customer on sign up, requires 4 string paramaters, n, p, e and pw. </li>
<li> customer/api/update       -  updates a customer, requires 4 parameters, integer id, string n, string p and string e. </li>
<li> customer/api/delete       -  deletes a customer, requires the integer id parameter. </li>
  </ul>


<h4> Cart: Properties: [CartID, CustomerID, ProductID, CustomerQuantity] </h4>
<ul>
<li> cart/api/customercart     -  gets all products in a customer's cart, requires the integer custid parameter. </li>
<li> cart/api/delete           -  removes a product from a customer's cart, requires two integer parameters, custid and prodid. </li>
  </ul>
