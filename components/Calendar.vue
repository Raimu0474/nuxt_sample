<template>
  <section class="container">
    {{num}}
    {{num2}}
    {{num3}}
    {{sample}}
  </section>
</template>

<script>

export default {
  data: function(){
    const now = new Date
    const nowYear = now.getFullYear();
    const nowMonth = now.getMonth();
    const firstDayOfMonth = new Date(nowYear, nowMonth, 1).getDay();
    const lastDateOfMonth = new Date(nowYear, nowMonth + 1, 0).getDate();
    const weeks = []
    let day = 1
    const calendarDate = Array.from([...Array(firstDayOfMonth),
      ...[...Array(lastDateOfMonth).keys()].map((k)=> k + 1)
    ])
    // const sample = calendarDate.map((k,v)=>{

    // })

    return {
      num: test,
      num2: firstDayOfMonth,
      num3: lastDateOfMonth,
      sample: [...[1,2,3], ...[4,5,6]]
    }
  }
}
</script>
