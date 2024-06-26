<template>
  <div>
    <twoColumnTemplate :projectTitle="projectTitle" :author="author" :pictures="pictures" :video="video">
      <template v-slot:description>
        <p>This application is intended for writers to keep track of the stories they are
          currently working on and the characters for their stories. This is meant to help avoid
          plot holes when writers are working on their character development. The application allows the user to create
          a story and then within their story, they can create characters that have a name, description, age, home and
          picture. </p>
      </template>
      <template v-slot:story>
        <p>This application was actually something my friends have been asking me to build for a while!
          These friends are both aspiring authors and play writers who deal with the complications of character
          development on the daily. To complete this project I worked with SwiftUI, XCode, switched computers to use a MAC
          laptop and learned how to structure an IOS app correctly. To meet my goal, I overloaded my workplans. Especially
          because this project was started halfway through the semester. I first created all of the views I initially
          thought I needed.
          From there, I focused on the functionality and specific features of the app. Then, towards the end of each
          sprint, this is
          when I worked on styling the app. I tended to focus on tasks that I thought would take a longer time during the
          earlier
          sprints, leaving the last sprint full of tasks I already knew how to do. </p>
      </template>
      <template v-slot:strugglesAndTriumphs>
        <p>This project tested my patience. While I already knew a decent amount about SwiftUI there were specific
          features
          of this application that were not a part of my last project. The main roadblock I faced was
          allowing the user to pick an image for their character and having that image save to AppStorage. This involved
          switching back and forth between different Image types and encorporating classes designed by other developers
          that have fun into the same issues that I was facing. In order to overcome this, I just focused on one
          small step at a time and would frequently make separate views or projects to make sure that the functionality of
          what I was aiming for was working correctly before I encorporated it into my final project.
          Although, the big win here was being able to pull this project together in a short amount of time.</p>
      </template>
      <template v-slot:links>
        <div style="padding-bottom: 10vh;">
          <a
            href="https://www.hackingwithswift.com/quick-start/swiftui/how-to-let-users-select-pictures-using-photospicker">PhotoPicker</a>
          <br>
          <a href="https://gist.github.com/nikitamounier/299e6083d2f0554b48173b2361bef4ad">ProfileImage Class Source</a>
          <br>
          <a href="https://developer.apple.com/tutorials/swiftui/building-lists-and-navigation">Apple Documentation for
            Lists</a>
          <br>
          <a href="https://developer.apple.com/tutorials/swiftui/interfacing-with-uikit">Apple Documentation for
            UIKits</a>
        </div>
      </template>
    </twoColumnTemplate>
  </div>
</template>
  
<script>
import twoColumnTemplate from '../components/templates/twoColumnTemplate.vue'
import imgOne from '../projects/project_images/CharCreatorImg.png';
import imgTwo from '../projects/project_images/CharCreatorImg2.png';
import imgThree from '../projects/project_images/CharCreatorImg3.png';
import charVideo from '../projects/project_videos/CharacterCreatorVid.mp4'
//import video from '../projects/project_videos/CharacterCreatorVid.mp4

export default {
  name: 'characterCreator',
  components: {
    twoColumnTemplate
  },
  data() {
    return {
      projectTitle: "Character Creator",
      author: "Emily Balboni",
      pictures: [imgOne, imgThree],
      video: charVideo //get rid of the quotes when putting in your video variable
    }
  },
  info: {
    title: 'Character Creator',
    author: 'Emily Balboni',
    tags: ["IOS", "Spring 2024", "Open Source", "Creative Writing"]
  }
}
</script>

<style scoped>
a {
  color: white;
}

h1,
h2,
h3 {
  color: white;
  max-width: 90%;
}

h3 {
  padding-bottom: 5vh;
}

p {
  padding-bottom: 10vh;
  text-align: left;
  max-width: 90%;
}

h1 {
  padding-bottom: 2vh;
}
</style>