<template>
  <section id="experience">
    <AnimateOnVisible name="fadeDown" :duration="1">
      <Title
        class="title"
        :title="'EXPERIENCE'"
        :description="'PROFESSIONAL AND ACADEMIC'"
      />
    </AnimateOnVisible>

	<AnimateOnVisible name="fadeUp" :duration="1">
		<div class="container-fluid">
			<div class="row">
				<ExperienceColumn
					:posts="academic"
					title="Education"
					class="col-12 col-md left"
				/>
				<ExperienceColumn
					:posts="professional"
					title="Professional"
					class="col-12 col-md right"
				/>
			</div>
		</div>
	</AnimateOnVisible>
  </section>
</template>

<script>
import Title from "./Title.vue";
import ExperienceColumn from "./ExperienceColumn.vue";

export default {
  name: "Experience",
  props: ["content"],
  components: {
    Title,
    ExperienceColumn
  },
  data(){
    return{
    data:"james",
    professional:[
                {
                "year":"08.2020 - 11.2020",
                "title":"Pennsylvania Front end Tool",
                "content":"Vuejs"
                },
                {
                "year":"09.2017 - 08.2020",
                "title":"Pfeiffer Vacuum SAS, Annecy",
                "content":"Web API, Vuejs, JavaScript, HTML, CSS, Angualar1.5"
                },
                {
                "year":"03.2017 - 08-2017",
                "title":"TimeTracker",
                "content":"C#.NET, Angualar1.5"
                }
            ],
          academic:[
              {
              "year":"2021 - 2021",
              "title":"Bioinfomatics",
              "content":"University of Skovde, Skövde, Sweden"
              },
              {
              "year":"2011 - 2014",
              "title":"BCA / Computer Science",
              "content":"Santhigiri college of computer science, Mahatma Gandhi University, Kerala, India"
              },
              {
              "year":"2014 - 2016",
              "title":"MCA / Computer Science",
              "content":"Santhigiri college of computer science, Mahatma Gandhi University, Kerala, India"
              }
              ]
    }
  }
};
</script>

<style scoped lang="scss">
@import "@/styles/constants.scss";

$linear: map-get($colors, dark);

#experience {
  background-color: lighten(map-get($colors, primary), 5%);
}

.title {
  color: map-get($colors, light);
}

.row {
  padding-top: 20px;
  text-align: center;
}

@media (min-width: #{map-get($breakpoints, small)}) {
  .left {
    text-align: right;
    border-right: 2px solid $linear;
  }
  .right {
    text-align: left;
  }
}

@media (max-width: #{map-get($breakpoints, small)}) {
  .right {
    margin-top: 20px;
  }
  .left:before {
    content : "";
    position: absolute;
    left    : 20%;
    bottom  : 0;
    height  : 2px;
    width   : 60%;  /* or 100px */
    border-bottom:2px solid $linear;
}
}

/deep/ .text-wrapper {
  &:after {
    border-bottom: 1px solid map-get($colors, dark);
  }
}
</style>
