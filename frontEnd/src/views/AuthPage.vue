<template>
  <div class="container">
    <div class="bluebg">
      <div class="box signin">
        <h2>Already have an Account?</h2>
        <button class="signinbtn btn" @click="ClickSignIn">Sign In</button>
      </div>
      <div class="box signup">
        <h2>Don't have an Account?</h2>
        <button class="signupbtn btn" @click="ClickSignUp">Sign Up</button>
      </div>
    </div>
    <div
      class="
        formBx
        absolute
        t-0
        left-0
        w-1/2
        h-full
        bg-gray-200
        z-50
        flex
        justify-center
        items-center
      "
    >
      <div class="form signinform">
        <form action="/login" method="POST">
          <div>
            <label for="email">Your Email:</label>
            <div class="col-sm-10">
              <input type="email" name="email" id="email" required />
            </div>
          </div>
          <div>
            <label for="password">Your Password:</label>
            <div class="col-sm-10">
              <input type="password" name="password" id="password" required />
            </div>
          </div>
          <br />
          <p class="text-red-600">
            <!-- <% if (messages.error){%>
                                <%=messages.error%>
                                    <%}%> -->
          </p>
          <button class="btn" type="submit">Login</button>
        </form>
      </div>
      <div class="form signupform">
        <form action="/register" method="POST">
          <div>
            <label for="name">Your Name:</label>
            <div class="col-sm-10">
              <input type="text" name="name" id="name" required />
            </div>
          </div>
          <div>
            <label for="email">Your Email:</label>
            <div class="col-sm-10">
              <input type="email" name="email" id="email" required />
            </div>
          </div>
          <div>
            <label for="password">Your Password:</label>
            <div class="col-sm-10">
              <input type="password" name="password" id="password" required />
            </div>
          </div>

          <br />
          <button class="btn mt-10 mb-10" type="submit">Register</button>
        </form>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: "AuthPage",
  methods: {
    ClickSignUp() {
      const formBx = document.querySelector(".formBx");
      const body = document.querySelector("body");
      formBx.classList.add("active");
      body.classList.add("active");
    },
    ClickSignIn() {
      const formBx = document.querySelector(".formBx");
      const body = document.querySelector("body");
      formBx.classList.remove("active");
      body.classList.remove("active");
    },
  },
};
</script>
<style>
body {
  display: flex;
  justify-content: center;
  justify-items: center;
  align-items: center;
  min-height: 100vh;
}
</style>
