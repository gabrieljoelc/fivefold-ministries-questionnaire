<template>
  <h1>Building a Discipling Culture
  <small>Appendix 2: Fivefold Ministry Questionnaire</small>
  </h1>
  <div class="question">
    <ul>
      <li v-for="question in questions">
        <p>{{ question }}</p>
        <input type="radio" id="often" value="often" v-model="newAnswer" />
        <label for="often">Often</label>
        <input type="radio" id="somewhat" value="somewhat" v-model="newAnswer" />
        <label for="somewhat">Somewhat</label>
        <input type="radio" id="rarely" value="rarely" v-model="newAnswer" />
        <label for="rarely">Rarely</label>
        <button type="button" v-on:click="addAnswer($index)">Confirm</button>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  methods: {
    addAnswer: function (index) {
      var answer = this.newAnswer.trim()
      if (answer) {
        this.answers.push({ questionIndex: index, answer: answer })
        this.newAnswer = ''
      }
      console.log(answer)
    }
  },
  data () {
    return {
      newAnswer: '',
      answers: [],
      questions: [
        'I am good at listening and taking in what people say.',
        'People say I am good at presenting information and ideas.',
        'When I’m excited about something, I get others interested in it too.',
        'I can accurately assess a person based on first impressions and know instinctively if they are being real with me.',
        'I can be counted on to contribute original ideas.',
        'I see more value in building up something meaningful and useful than always striking out into new territory.',
        'I try explaining things in different ways if people are finding a concept difficult to grasp or understand.',
        'People with different value systems have said that they feel comfortable when they are around me, and that I have a positive effect on them being open to new ideas.',
        'People comment that I am unusually creative.',
        'People describe me as entrepreneurial.',
        'When I communicate truth to others in love, I see resulting changes in their knowledge, attitudes, values or conduct.',
        'I love to share information with others.',
        'I like to tell stories, especially my own.',
        'I have just suddenly known something about someone.',
        'I’ll be the first to try new things out if it will encourage others to do the same.',
        'I like to create safe places for people to flourish and grow.',
        'People have told me that I have helped them learn important truth in a meaningful way.',
        'I like to share what I believe.',
        'Sometimes I just intuitively know things that others seem to miss.',
        'I can clarify goals, develop strategies, and cast a vision to accomplish tasks.',
        'I remember names or at least where I first met someone.',
        'I generally appreciate hard facts more than theories.',
        'I enjoy relating to people, sharing personally in their successes and their failures.',
        'I sometimes get frustrated and even depressed at the lack of faith or understanding of others around me.',
        'I like change even when it makes others uncomfortable.',
        'I get concerned, and maybe even upset, at other people’s difficulties and problems even if I haven’t experienced them myself.',
        'I share what knowledge I have with others.',
        'I think I would do well selling a product I really believed in.',
        'I am sensitively able to discern the real meaning behind things.',
        'I love new challenges that require me to stretch and change.',
        'I am quick to help when help is needed and often do things which I see need to be done without even being asked.',
        'I love to show people how to do things that I do well.',
        'I mix easily with a wide variety of people without having to try to be one of them.',
        'I sometimes feel compelled to speak the truth even if it makes others feel uncomfortable.',
        'I enjoy coming up with new and original ideas, dreaming big and thinking about visions for the future.',
        'I like to provide a safe and comfortable environment where people feel they are welcome, that they belong, are listened to and cared for.',
        'I enjoy relating stories and sharing my experiences.',
        'People say I get passionate about the things I believe in and it shows.',
        'I enjoy meditation and thinking deeply about spiritual things.',
        'I’ve always wanted to build a business/organization from the ground up so I can give my specific vision to it.',
        'I am faithful in providing support, care and nurture for others over long periods of time, even when others have stopped.',
        'I get great satisfaction in accomplishing the details of a task.',
        'I look for opportunities to socialize and build relationships with people that are different from me.',
        'I have expressed my spiritual feelings as pictures or analogies.',
        'Others have suggested that I am a person of unusual vision.',
        'I find that people trust me and come to me regularly, wanting to chat, and looking for my advice and help.',
        'I enjoy taking notes when someone is speaking and pay close attention to the details of what they are saying.',
        'I don’t mind getting on a soap box for things that are important to me.',
        'I have had dreams that I know were more significant than regular dreams.',
        'I like to help organizations, groups and leaders become more efficient and often find myself thinking about how things function.',
        'I have a real aversion to gossip and often stop it when I hear it.',
        'Friends often ask me to help clarify a situation or issue.',
        'When I like a movie or a restaurant, everyone will hear about it.',
        'I sometimes have an urge to share my thoughts with people, and I have been told they meant something or were relevant to the person’s current situation.',
        'People tell me that the things I say often help them to try new things.',
        'People sometimes tell me that I care too much for others.',
        'I enjoy coming up with the best, most efficient way to do a task right.',
        'I find myself talking about things I’m passionate about to the people I meet.',
        'Social justice for the poor and marginalized means a great deal to me.',
        'Despite not enjoying the nitty-gritty details of leadership, I still often end up leading.',
        'I think before I speak.',
        'I like to create safe environments where people can learn and mature.',
        'I don’t shy away from controversial subjects if they are important to me.',
        'I have a strong sense of what to say to people in response to a particular situation.',
        'When in a group, I am the one others often look to for vision and direction.',
        'I am willing to challenge or confront people in order to help them mature.',
        'I enjoy digging out information and ideas or metaphors to explain a concept.',
        'In my enthusiasm, I push my views too far with people.',
        'My inspired thoughts surprise me with their clarity and unexpected direction.',
        'I have a clear vision and others have said that they feel confident to go along with me.',
        'I sometimes have difficulty setting boundaries with needy people.',
        'I try to think of different ways of expressing the truth.',
        'I am interested in living and working overseas or among people from a different culture.',
        'I regularly like to be alone for long periods of time to reflect and think.',
        'I get frustrated when I feel I’m not experiencing new things in my life.',
        'I empathize with those who are hurting or broken and can support them through their pain to wholeness.',
        'I see more value in building up something meaningful and useful than always striking out into new territory.',
        'I love to meet new people and get to know their story.',
        'Sometimes I am able to reveal specific things which have then happened or meant something at a later date.',
        'When reading, it is easier for me to grasp the wider picture or message than the specific details.',
        'I have enjoyed relating to a certain group of people over a period of time, sharing personally in their successes and their failures.',
        'When I communicate truth to others I notice that they understand and some even put it into practice.',
        'I remember the faces of most people I meet.',
        'People have told me that I have communicated timely words or pictures which must have come directly from some higher plane.',
        'I delegate tasks to others in order to achieve more with my time.'
      ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1 {
  color: #42b983;
}
ul {
  padding-left: 0;
}
li {
  list-style: none;
}
button {
  display: block;
  margin: 15px auto 0 auto;
}
</style>
