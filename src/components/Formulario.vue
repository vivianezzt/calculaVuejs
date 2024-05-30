<script setup>
    const props = defineProps(["getNumber1", "getNumber2", "getOperador", "resultado"]);
</script>

<template>
    <form class="text-center">
      <div class="row">
        <div class="col">
          <input required type="number" placeholder="0" class="form-control mb-4" @keyup="props.getNumber1"/> 
        </div>
        <div class="col-md-2 mb-4 text-center">
          <select class="form-control text-center" @change="props.getOperador">
            <option class="dividir-text-center" value="dividir"><p>÷</p></option>
            <option class="multiplicar-text-center" value="multiplicar"><p>x</p></option>
            <option class="subtrair-text-center" value="subtrair"><p>-</p></option>
            <option class="somar-text-center" selected value="somar"><p>+</p></option>
          </select>
        </div>
        <div class="col">
          <input required type="number" placeholder="0" class="form-control mb-4" @keyup="props.getNumber2"/>
        </div>
      </div>
      <div class="row">
        <div class="col p-2 mb-2 mt-4 bg-dark rounded-4 text-center">
          <h3  class=" black-text">Resultado</h3>
          <h2 class="black-text fs-1 fw-bold ps-2 ">{{ props.resultado }}</h2>
        </div>
      </div>
    </form>
</template>

<style scoped>

.black-text {
  color: #faf6f6;
}

</style>