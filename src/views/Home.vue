<template>
  <div class="home">
    <div class="head"></div>
    <div id="team">
      <h2>OUR TEAM</h2>
      <h4>meet the team - our office rats:</h4>
      <div class="theTeam">
        <div class="person item" v-for="(guy, index) in team" :key="index">
          <img :src="guy.pic" alt="" />
          <h3>{{ guy.name }}</h3>
          <p>{{ guy.position }}</p>
        </div>
      </div>
    </div>
    <div id="work">
      <div class="work-desc item">
        <h2>Our Work</h2>
        <p>
          Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
          eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad
          minim veniam, quis nostrud exercitation ullamco laboris nisi ut
          aliquip ex ea commodo consequat. Duis aute irure dolor in
          reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla
          pariatur. Excepteur sint occaecat cupidatat non proident, sunt in
          culpa qui officia deserunt mollit anim id est laborum.
        </p>
      </div>
      <div class="work-card item" v-for="(card, index) in cards" :key="index">
        <img :src="card.pic" alt="" />
        <div class="card-text">
          <h3>{{ card.title }}</h3>
          <p>dumy text</p>
          <p>dumy text</p>
          <p>dumy text</p>
          <p>dumy text</p>
          <p>dumy text</p>
        </div>
      </div>
      <div class="fas">+</div>
    </div>
    <div id="contact">
      <div class="info item">
        <h2>Contact Us</h2>
        <h3>Address</h3>
        <p>swing by for a cup of coffee or whatever.</p>
        <p><i class="fas fa-map-marker-alt"></i> Amman,Jordan</p>
        <p><i class="fas fa-phone-alt"></i> +96279000000</p>
        <p><i class="far fa-envelope"></i> test@test.com</p>
      </div>
      <div class="form item">
        <label for="Name">Name</label>
        <input type="text" />
        <label for="Email">Email</label>
        <input type="text" />
        <label for="Message">Message</label>
        <input type="text" />
        <div class="sub">
          <div class="box">
            <input type="checkbox" name="" id="" />
            <label for="like">I like it!</label>
          </div>
          <button>Send</button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src

export default {
  name: "Home",
  data() {
    return {
      team: [
        {
          name: "Ahmad Naser",
          position: "Support",
          pic: require("../assets/guy.jpg"),
        },
        {
          name: "Ahmad Naser",
          position: "Support",
          pic: require("../assets/guy.jpg"),
        },
        {
          name: "Ahmad Naser",
          position: "Support",
          pic: require("../assets/guy.jpg"),
        },
        {
          name: "Ahmad Naser",
          position: "Support",
          pic: require("../assets/guy.jpg"),
        },
      ],
      cards: [
        { pic: require("../assets/card.jpg"), title: "Customer 1" },
        { pic: require("../assets/card.jpg"), title: "Customer 2" },
        { pic: require("../assets/card.jpg"), title: "Customer 3" },
      ],
    };
  },
};
</script>

<style scoped>
.head {
  height: 50vh;
  background: url("../assets/desert.jpg") no-repeat center center;
  background-size: cover;
}
#team {
  padding: 2rem 0;
}
.theTeam {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
  align-items: center;
  margin: 3rem 0;
}
.person {
  margin: 1rem 0;
}
.person img {
  border-radius: 50%;
  height: 150px;
  width: 150px;
}
#work {
  display: flex;
  flex-wrap: wrap;
  background-color: rgb(51, 51, 51);
  color: white;
  padding: 3rem 1rem;
  gap: 0.8rem;
  position: relative;
}
#work .fas {
  position: absolute;
  bottom: -15px;
  right: 1rem;
  background-color: rgb(0, 119, 119);
  padding: 0.5rem;
  height: 20px;
  width: 20px;
  border-radius: 50%;
  font-size: 1.3rem;
  font-weight: 700;
}
.item {
  flex: 1 1 250px;
}
.work-desc {
  text-align: left;
}
.work-card {
  background-color: white;
  height: 500px;
}
.work-card img {
  height: 50%;
  width: 100%;
  object-fit: cover;
}
.card-text {
  text-align: left;
  padding: 0.5rem;
  color: black;
}
#contact {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  text-align: left;
  padding: 3rem 1rem;
}
.form {
  display: flex;
  flex-direction: column;
  box-shadow: 0 0 5px black;
  padding: 1.5rem 1rem;
}
.form input {
  border: 2px rgb(182, 182, 182);
  border-style: none none solid none;
  margin: 0.5rem 0;
}
.form input:focus {
  outline: none;
}
.form label {
  font-weight: 600;
  margin: 0.5rem 0;
}
.sub {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 0.5rem 0;
}
.sub button {
  background-color: black;
  color: white;
  border: none;
  padding: 0.5rem 0.7rem;
  cursor: pointer;
}
.sub input {
  margin: 0.5rem;
}
.info h2 {
  border-bottom: 5px solid rgb(0, 119, 119);
  width: fit-content;
}
.info .fas,
.far {
  color: rgb(0, 119, 119);
}
</style>