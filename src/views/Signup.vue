<template>
  <v-content>
    <v-container class="fill-height" fluid>
      <v-row align="center" justify="center">
        <v-col cols="12" sm="8" md="4">
          <v-card class="elevation-12">
            <v-toolbar color="amber" dark flat>
              <v-toolbar-title class="black--text">SignUp form</v-toolbar-title>
              <v-spacer />
            </v-toolbar>
            <v-card-text>
              <v-form>
                <v-text-field
                  label="Name"
                  name="name"
                  prepend-icon="person"
                  type="text"
                />

                <v-text-field
                  label="Phone"
                  name="phone"
                  prepend-icon="phone"
                  type="number"
                />

                <v-text-field
                  label="Email"
                  name="email"
                  prepend-icon="email"
                  type="email"
                />

                <v-text-field
                  id="password"
                  label="Password"
                  name="password"
                  prepend-icon="lock"
                  type="password"
                />
              </v-form>
            </v-card-text>
            <v-card-actions>
              <v-btn color="amber">SignIn</v-btn>
              <v-spacer />
              <v-btn color="amber" text to="/login">Login instead</v-btn>
            </v-card-actions>
          </v-card>
        </v-col>
      </v-row>
      <v-spacer></v-spacer>
    </v-container>
  </v-content>
</template>

<script>
export default {
  props: {
    source: String
  }
};
</script>
