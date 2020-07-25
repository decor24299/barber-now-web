<template>
  <div id="nav-bar">
    <b-nav vertical>
      <div class="branch pt-4 pb-3">
        <h1>Barber<span class="highlight">Now</span></h1>
      </div>
      <div class="section">
        <b-nav-item>
          <b-icon-exclamation-triangle-fill></b-icon-exclamation-triangle-fill>
          <span>Home</span>
        </b-nav-item>
        <b-nav-item>
          <b-icon-exclamation-triangle-fill></b-icon-exclamation-triangle-fill>
          <span>Barber shop</span>
        </b-nav-item>
        <b-nav-item>
          <b-icon-exclamation-triangle-fill></b-icon-exclamation-triangle-fill>
          <span v-b-toggle.sidebar-variant>Filter</span>
        </b-nav-item>
        <b-nav-item>
          <b-icon-exclamation-triangle-fill></b-icon-exclamation-triangle-fill>
          <span>Admin</span>
        </b-nav-item>
      </div>

      <div class="section">
        <b-nav-item>
          <b-icon-exclamation-triangle-fill></b-icon-exclamation-triangle-fill>
          <span>Settings</span>
        </b-nav-item>
        <b-nav-item>
          <b-icon-exclamation-triangle-fill></b-icon-exclamation-triangle-fill>
          <span>Support</span>
        </b-nav-item>
        <b-nav-item>
          <b-icon-exclamation-triangle-fill></b-icon-exclamation-triangle-fill>
          <span>Quit</span>
        </b-nav-item>
      </div>

      <div>
        <b-sidebar id="sidebar-variant" title="Add New Shop" shadow>
          <div class="px-3 py-2">
            <b-card
              title="SHOP IMAGE"
              tag="article"
              style="max-width: 20rem;"
              class="mb-2"
            >
              <b-row>
                <b-col cols="4">
                  <b-img
                    src="https://picsum.photos/300/300/?image=41"
                    fluid
                    alt="Fluid image"
                  ></b-img>
                </b-col>
                <b-col cols="4">
                  <b-img
                    src="https://picsum.photos/300/300/?image=41"
                    fluid
                    alt="Fluid image"
                  ></b-img>
                </b-col>
                <b-col cols="4">
                  <b-img
                    src="https://picsum.photos/300/300/?image=41"
                    fluid
                    alt="Fluid image"
                  ></b-img>
                </b-col>
              </b-row>

              <b-row class="justify-content-center">
                <b-button class="mx-2 mt-4" href="#" variant="primary"
                  >Re-add</b-button
                >
                <b-button class="mx-2 mt-4" href="#" variant="primary"
                  >Delete</b-button
                >
              </b-row>
            </b-card>

            <b-card
              title="SHOP INFO"
              tag="article"
              style="max-width: 20rem;"
              class="mb-2"
            >
              <b-form-group
                id="fieldset-1"
                label="Enter your name"
                label-for="input-1"
                :invalid-feedback="invalidFeedback"
                :valid-feedback="validFeedback"
                :state="state"
              >
                <b-form-input
                  id="input-1"
                  v-model="name"
                  :state="state"
                  trim
                ></b-form-input>
              </b-form-group>
            </b-card>
          </div>
        </b-sidebar>
      </div>
    </b-nav>
  </div>
</template>

<script>
export default {
  data() {
    return {
      options: [
        { text: "Java", value: "java" },
        { text: "C#", value: "c#" },
        { text: "Python", value: "python" },
        { text: "Dart", value: "dart" },
      ],
    };
  },
};
</script>

<style scoped>
#nav-bar /deep/ {
  position: fixed;
  top: 0;
  height: 100vh;
  width: 15vw;
  padding: 0 3vmin;
  background: #348f6c;
  text-align: left;
  font-size: 1.8vmin;
}

#nav-bar .branch {
  text-align: center;
}

#nav-bar .branch h1 {
  font-size: 3vmin;
}

#nav-bar .branch .highlight {
  color: #fff;
  font-weight: 700;
}

#nav-bar .section {
  padding-top: 2.5vmin;
  padding-bottom: 2.5vmin;
  border-top: 1px solid #d9c791;
}

#nav-bar .nav-item a {
  color: #fff;
}

#nav-bar .nav-item span {
  padding-left: 2vmin;
}

#nav-bar .nav-item svg {
  color: #d9c791;
}
</style>
