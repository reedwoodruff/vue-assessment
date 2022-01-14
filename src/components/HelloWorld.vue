<template>
  <div class="hello">
    <h1 class="title" :class="{ active: isActive }">Explore</h1>
    <div class="subtitle-box">
      <div>
        <div class="subtitle-expandable" :class="{ active: isActive }">
          <div
            v-on:click="toggleIsActive()"
            class="toggle-button"
            :class="{ active: isActive }"
          >
            <img
              src="../assets/Plus.svg"
              class="button-svg"
              :class="{ active: isActive }"
            />
          </div>
          <div class="inner-content" :class="{ active: isActive }">
            <h2 class="inner-header">Explore</h2>
            <hr class="inner-hr"/>
            <br/>
            <div class="inner-filler" :class="{ active: isActive }">
              Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque ipsa quae ab illo inventore veritatis et quasi architecto beatae vitae dicta sunt explicabo. Nemo enim ipsam voluptatem quia voluptas sit aspernatur aut odit aut fugit, sed quia consequuntur magni dolores eos qui ratione voluptatem sequi nesciunt. Neque porro quisquam est, qui dolorem ipsum quia dolor sit amet, consectetur, adipisci velit, sed quia non numquam eius modi tempora incidunt ut labore et dolore magnam aliquam quaerat voluptatem. Ut enim ad minima veniam, quis nostrum exercitationem ullam corporis suscipit laboriosam, nisi ut aliquid ex ea commodi consequatur? 
              </div>
              <br/>
            <div class="inner-button-background">
              READ MORE
              </div>
            </div>
        </div>
      </div>
      <div class="subtitle-text" :class="{ active: isActive }">
        More Details
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  props: {
    detailsOpen: Boolean,
  },
  data() {
    return {
      isActive: false,
    };
  },
  methods: {
    toggleIsActive() {
      this.isActive = !this.isActive;
    },
  },
};
</script>

<style scoped>
.active {
}
.title {
  position: absolute;
  left: 10vw;
  top: 40vh;
  color: white;
  font-size: 150px;
  font-weight: 500;
  letter-spacing: 0.05em;
  transition: all 0.5s ease-in-out;
}
.title.active {
  opacity: 0;
  margin-top: 30px;
}
.subtitle-box {
  display: flex;
  position: absolute;
  top: 78vh;
  left: 12vw;
}
.subtitle-text {
  color: white;
  font-size: 20px;
  padding-left: 60px;
  padding-top: 20px;
  transition: all 0.5s ease-in-out;
}
.subtitle-text.active {
  opacity: 0;
  margin-top: 30px;
}
.subtitle-expandable {
  position: absolute;
  border-radius: 100px;
  text-align: right;
  left: 10px;
  top: 20px;
  transition: all 0.5s ease-in-out;
  background-color: white;
  width: 10px;
  height: 10px;
}
.subtitle-expandable.active {
  border-radius: 0;
  width: 50vw;
  height: 75vh;
  top: -60vh;
  background-color: white;
}
.toggle-button {
  transition: all 0.5s ease-in-out;
  margin-left: -10px;
  margin-top: -10px;
  text-align: right;
}
.toggle-button.active {
  margin-left: 0px;
  margin-top: 0px;
}
.button-svg {
  transition: all 0.5s ease-in-out;
}
.button-svg.active {
  transform: rotate(45deg);
}
.inner-content {
  transition: all 0.1s ease-in-out;
  opacity: 0;
  text-align: left;
  padding: 20px 60px;
  height: 0px;
}
.inner-content.active {
  transition: all 1s ease-in-out;
  opacity: 1;
  height: auto;
  overflow: auto;
}
.inner-header {
  font-size: 50px;
  color: #611818;
  margin: 0px;
}
.inner-hr {
  height: 2px;
  border: none;
  background: rgb(97,24,24);
  background: linear-gradient(90deg, rgba(97,24,24,1) 0%, rgba(97,24,24,1) 10%, rgba(255,255,255,1) 65%);
}
.inner-button-background {
  max-width: 150px;
  text-align: center;
  padding: 10px;
  color: white;
  background: rgb(97,24,24);
  background: linear-gradient(90deg, rgba(97,24,24,1) 0%, rgba(163,103,84,1) 100%);
}
.inner-filler {
  font-size: 13px;
}
</style>
