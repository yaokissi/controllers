<div class="container">
<nav>
    <div class="logo">
        <a href="#"> Donu.co </a>
    </div>
    <div class="menu">
        <ul>
            <li><a href="#">Franchise</a></li>
            <li><a href="#">Catering</a></li>
            <li><a href="#">Shipping</a></li>
            <li><a href="#">Locations</a></li>
        </ul>
    </div>
    <a href="#" class="cta-btn">Buy Now</a>
</nav>
</div>
<slot />

<style>
    @import url("https://fonts.googleapis.com/css2?family=Montserrat:wght@300;400;500;600;900&display=swap");

:global(*) {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

:global(body) {
  font-family: "Montserrat", sans-serif;
  font-weight: 500;
}
.container {
  width: 80vw;
  margin: auto;
  padding: 0 1vw;
}
    nav{
        padding: 1.5vh 0;
        display: flex;
        justify-content: space-between;
        align-items: center;
    }

    nav .logo a{
        text-decoration: none;
        font-size: 2rem;
        font-weight: 800;
        color: #552c10;
    }

    nav .menu ul{
        display: flex;
    }

    nav .menu ul li{
        margin: 0 1vw;
    }

    nav .menu ul li a{
        color: #000;
        transition: color 0.2s ease;
    }

    nav .menu ul li a:hover{
        color: #552c10;
        font-weight: 600;
    }
    :global(ul) {
  list-style-type: none;
}

:global(a) {
  text-decoration: none;
}

.cta-btn {
  border: 1px solid;
  padding: 0.8rem 1.8rem;
  border-radius: 2rem;
  color: #552c10;
  transition: background-color 0.2s ease, color 0.2s ease;
}
.cta-btn:hover {
  background-color: #552c10;
  color: #fff;
}

h1{
    font-size: 20.5vw;
     color: #552c10;
}
</style>
