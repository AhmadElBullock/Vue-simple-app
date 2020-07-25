<template>
    <div>
        <img alt="Vue logo" src="../assets/logo.png">
        <div class="jumbotron">
            <div class="container">
                <h1 class="display-4">Category: {{ $route.params.category }}</h1>
                <h1 class="display-4">Name of the product: {{ $route.params.name }}</h1>
                <h1 class="display-4">Price: {{ $route.params.price }}</h1>
            </div>
        </div>
    </div>
</template>
