<script>
	let value = 1;
  
  function handleClick(buttonType) {
    if (buttonType === 'user') {
      value = 1;
    } else if (buttonType === 'distributor') {
      value = 2;
    }
  }
</script>

<style>
	/* Global Styles */
:global(body) {
    font-family: Arial, sans-serif;
    margin: 0;
    background-color: #232857;
    color: #fff;
    font-size: 16px;
}

/* Container Styles */
.container {
    max-width: 400px;
    margin: 5% auto;
    padding: 20px;
    background-color: #343a7d;
    border-radius: 10px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
    overflow: hidden;
    text-align: center;
}

/* Header Styles */
.header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 30px;
}

.time {
    font-size: 1.5rem;
    font-weight: bold;
}

/* Icon Styles */
.icons .wifi, 
.icons .battery {
    width: 24px;
    height: 24px;
    background-color: #fff;
    border-radius: 50%;
    display: inline-block;
    margin-left: 10px;
}

/* Form Styles */
.form label {
    display: block;
    font-weight: bold;
    margin-bottom: 10px;
    text-align: left;
    color: grey;
}

.form input {
    width: 100%;
    padding: 10px;
    margin-bottom: 20px;
    background-color: #232857;
    border: 2px solid #565f9f;
    border-radius: 5px;
    color: #fff;
    font-size: 1rem;
    box-sizing: border-box;
}

/* Button Styles */
button {
    width: 100%;
    padding: 15px;
    background-color: #57d2f7;
    border: none;
    border-radius: 5px;
    color: #fff;
    font-size: 1.1rem;
    font-weight: bold;
    cursor: pointer;
}

/* Footer Styles */
.footer {
    margin-top: 20px;
    text-align: center;
    font-size: 1rem;
}

/* Link Styles */
a {
    color: #57d2f7;
    font-weight: bold;
}

/* Button Group Styles */
.button-group {
    display: flex;
    justify-content: center;
    margin: 20px 0;
}

/* Tab Button Styles */
.tab-button {
    background: transparent;
    border: none;
    padding: 10px 20px;
    margin: 0 10px;
    font-size: 1rem;
    cursor: pointer;
    outline: none;
    color: white;
}

.tab-button.active {
    border: 2px solid white;
}

/* Media Queries */
@media only screen and (max-width: 600px) {
    .container {
        margin: 2% auto;
        padding: 15px;
    }

    .header .time,
    .form input,
    .form label,
    .footer,
    button {
        font-size: 0.9rem;
    }

    button {
        padding: 12px;
    }
}

@media only screen and (max-width: 400px) {
    .header .time {
        font-size: 1rem;
    }

    .icons .wifi, 
    .icons .battery {
        width: 20px;
        height: 20px;
        margin-left: 8px;
    }
}

</style>

<div class="container">
  <h1>Get Started</h1>
  <p>Let's create your account <a>Privacy Policy</a></p>

  <div class="button-group">
    <button class="tab-button {value==1?"active":""}" id="user-btn" on:click={() => handleClick('user')}>User</button>
    <button class="tab-button {value==2?"active":""}" id="distributor-btn" on:click={() => handleClick('distributor')}>Distributor</button>
  </div>

  <div class="form">
    <label for="tron">Tron Address (TRC20)</label>
    <input type="text" id="tron" placeholder="TGkrZNSJQ3rdKvhu2WwoJ7MzZ8rAg9gF3d">

    <label for="ethereum">Ethereum Address (ERC20)</label>
    <input type="text" id="ethereum" placeholder="0xfc6949b3a539ff60cfd51af66a4e46611c033a7">

    <label for="telegram">Telegram ID</label>
    <input type="text" id="telegram" placeholder="yc_bc_dev">

    <label for="password">Transaction password</label>
    <input type="password" id="password" placeholder="********">

    <label for="confirm">Confirm password</label>
    <input type="password" id="confirm" placeholder="********">

    <button>Get Started</button>
  </div>

  <div class="footer">
    Already have an account? <a href="#">Sign In</a>
  </div>
</div>