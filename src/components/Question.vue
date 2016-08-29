<template>
  <h1>Building a Discipling Culture
  <small>Appendix 2: Fivefold Ministry Questionnaire</small>
  </h1>
  <div class="question">
    <ul>
      <li v-for="question in questions">
        <p>{{ question.text }}</p>
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
  data () {
    return {
      newAnswer: '',
      answers: [],
      questions: [
        {
          text: 'Question 1'
        }
      ]
    }
  },
  methods: {
    addAnswer: function (index) {
      var answer = this.newAnswer.trim()
      if (answer) {
        this.answers.push({ questionIndex: index, answer: answer })
        this.newAnswer = ''
      }
      console.log(answer)
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
