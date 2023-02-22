<template>
    <div class="container">
        <div class="card">
            <div class="card-header">
                Agregar Días Habiles
            </div>
            <div class="card-body">
                <form>
                    <div class="form-group">
                      <label for="codigo">Código</label>
                      <input type="text" name="" id="" class="form-control" placeholder="Escribe el Código" aria-describedby="helpId">
                      <small id="helpId" class="text-muted"></small>
                    </div>
                    <div class="form-group">
                      <label for="descripción">Descripción</label>
                      <input type="text" name="" id="" class="form-control" placeholder="Escribe la descripción" aria-describedby="helpId">
                      <small id="helpId" class="text-muted"></small>
                    </div>
                    <div class="btn-group" role="group" aria-label="">
                        <button type="button" class="btn btn-success">Agregar</button>
                        <router-link :to="{name:'Listar'}" class="btn btn-warning">Cancelar</router-link>
                    </div>
                </form>
            </div>
        </div>
    </div>
</template>