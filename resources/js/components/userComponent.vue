<template>
  <div class="card" style="width: 18rem;">
    <div class="card-body">
      <h4 class="card-title"> {{dati_user.username}} </h4>
      <h5 class="card-title"> {{dati_user.name}} </h5>
    </div>
    <ul class="list-group list-group-flush">
      <li class="list-group-item"> {{dati_user.email}} </li>
      <li class="list-group-item"> {{dati_user.address.street}}, {{dati_user.address.city}} </li>
      <li class="list-group-item"> {{dati_user.phone}} </li>
    </ul>
    <div class="card-body">
      <h5 class="card-title"> {{dati_user.company.name}} </h5>
      <a href="#" class="card-link">Vai alla pagina dell'azienda</a>
    </div>
  </div>
</template>

<script>
    export default {
      props : ['dati_user']
    }
</script>
