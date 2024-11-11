<template>
  <div class="home">

    <h1>THIS IS HOME PAGE</h1>

    <h3>Testing and practing the FETCH,.then and .catch HERE</h3>

  </div>
</template>

<script>

  // fetch("/database/db.json")

  // .then((response)=>{
  //   // console.log("resolved", response.json);
    
  //   if (response.status===404){
  //     throw new Error("ur link no good")
  //   }
  //   return response.json();
  // })
  // .then((data)=>{
  //   console.log(data);
  // })
  // .catch((err)=>{
  //   console.log(err.message);
  // })

  // fetch("/database/db.json")

  // .then((response)=>{
  //   return response.json();
  // })
  // .then((data)=>{
  //   console.log(data);
  // })
  // .catch((err)=>{
  //   console.log(err);
  // })

  // let getJson = async()=>{
  //   let response = await fetch("/database/db.json");

  //   let datas = await response.json();
  //   // console.log(datas);
  //   return datas;

  // }
  // getJson()
  // .then((datas)=>{
  //   console.log(datas);
  // })

  // let getmyJson = async()=>{
  //   let response = await fetch("/database/db.json")

  //   let datas = await response.json();
  //   return datas;

  // }
  // getmyJson()
  // .then((datas)=>{
  //   console.log(datas);
  // })


  let GetMyJson = async()=>{
    let response = await fetch("/database/db.json");

    if(response.status===404){
      throw new Error ("Not Found URL")
    }

    let datas = await response.json();
    return datas
  }
  GetMyJson()
  .then((datas)=>{
    console.log(datas);
  })
  .catch((err)=>{
    console.log(err.message)
  })


  let GETmyJson = async()=>{
    let Response = await fetch ("/database/db.json");

    if (Response.status===404){
      throw new Error("URL IS USELESS MAN")
    }

    let datas = await Response.json();
    return datas
  }
  GETmyJson()
  .then((datas)=>{
    console.log(datas);
  })
  .catch((err)=>{
    console.log(err.message)
  })


  export default {
    name: 'HomeView',
    components: {
      
    }
  }

</script>
