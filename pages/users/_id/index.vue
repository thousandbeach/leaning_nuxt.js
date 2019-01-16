<template>
  <div>
    <h1>{{ $route.params }}</h1>
    <h2>{{ $route.params.id }}</h2>
  </div>
</template>

<script>
// context を使って、params にアクセスする。
  export default {
    validate(context) {
      return /^\d+$/.test(context.params.id);
    }
  }


/* context を使わない場合
  export default {
    validate({params}) {
      return /^\d+$/.test(params.id);
    }
  }
*/
</script>
