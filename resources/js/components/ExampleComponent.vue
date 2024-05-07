<template>
    <div class="container">
        <div class="row justify-content-center">
            <div class="col-md-12">
                <div class="card">
                    <div class="card-header">Example Component</div>

                    <div class="card-body">
                        I'm an example component.
                    </div>
                </div>
            </div>
            <div class="col-md-12">
                <form>
                    <div class="form-group">
                        <label>Name</label>
                        <input type="text" name="name" class="form-control" v-model="name" @keyup.up="handleSubmit" />
                        {{ name }}
                    </div>
                    <div class="form-group">
                        <label>Radio1</label>
                        <input type="radio" name="numbers" class="form-control" v-model="numbers" value="v1" />
                    </div>
                    <div class="form-group">
                        <label>Radio2</label>
                        <input type="radio" name="numbers" class="form-control" v-model="numbers" value="v2" />
                        {{ numbers }}
                    </div>

                    <div class="form-group">
                        <label>Checkbox</label>
                        <input type="checkbox" name="checkval" class="form-control" v-model="checkedVal" true-value="yes" false-value="no" />
                        {{ checkedVal }}
                    </div>
                    <button class="btn btn-primary" type="button" @click.prevent="(event) => handleSubmit(event)">
                        Click Me
                    </button>
                </form>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        mounted(){
            console.log('Component mounted.')
        },
        data(){
            return {
                name: 'Text defaults',
                numbers: 'Radio default',
                checkedVal: 'Checkbox default'
            }
        },
        methods: {
            handleSubmit(event)
            {
                console.log('abcdss', event);
            }
        }
    }
</script>
