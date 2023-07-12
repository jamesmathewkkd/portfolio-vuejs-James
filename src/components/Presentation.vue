<template>
  <div class="paragraph">
    <h3>Who am I ?</h3>
    <div class="begin">Efficient professional 6 years’ experience in design, analysis and development of client/server, web based applications using Microsoft Technology. Aiming to leverage my skills to successfully fill the Software Engineer role at your company.</div>
    <h3 style="padding-top:12px!important">CAREER SUMMARY</h3>
    <p class="begin">
          •	Expertise in developing web applications using ASP.Net Web API, C#,Vue js, HTML, JavaScript SQL Server and Influx db.
          </p>
          <p class="begin"> 
          •	Hands on experience of debugging an application using the tools provided by the Microsoft Visual Studio 2022.
          </p>
          <p class="begin">
          •	Expertise in tracking Bug reports using Bug Tracking Tool- Bugzilla and Jira.
          </p>
          <p class="begin">
        •	Effective in working independently and collaboratively in teams.
          </p>
          <p class="begin">
          •	Good experience with Agile/SCRUM Methodologies.
          </p>

  </div>
</template>

<script>
export default {
    name: 'Description',
    props: ['content']
}
</script>

<style scoped lang="scss">
    @import '@/styles/constants.scss';

    .paragraph {
        color: map-get($colors, primary);
        .begin {
            color: map-get($colors, secondary);
        }
    }
</style>