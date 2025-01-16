<template>
    <div>
        <h2>Formulario de registro</h2>
        <Form :validation-schema="schema" @submit="onSubmit">
            <div class="form">
                <label for="nombre">Nombre: </label>
                <Field type="text" name="nombre" id="nombre" placeholder="Ingrese su nombre" />
                <ErrorMessage name="nombre"></ErrorMessage>
            </div>
            <div class="form">
                <label for="email">Correo: </label>
                <Field type="text" name="email" id="nombre" placeholder="Ingrese su correo" />
                <ErrorMessage name="email"></ErrorMessage>
            </div>
            <div class="form">
                <button type="submit">Registrar</button>
            </div>
        </Form>
    </div>
</template>

<script setup>
    import { Form, Field, ErrorMessage } from 'vee-validate';
    import {schema} from '../schemas/ValidationSchema';

    const onSubmit = () => {
        console.log("se ha Enviado el registro de formulario");
        
    }
</script>

<style scoped>
    .form {
        margin-bottom: 10px;
    }
</style>