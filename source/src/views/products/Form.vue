<template>
    <div class="b-form">
        <div class="pricing-header px-3 py-3 pt-md-5 pd-md-4 mx-auto text-center">
            <h3 class="display-5">Products Infomation </h3>
            <router-link to="/product">Back </router-link>
        </div>
        <div class="container">
            <form @submit.prevent="save()">
                <div class="form-group row mb-3">
                    <label class="col-sm-3 col-form-label">Product name</label>
                    <div class="col-sm-9">
                        <input type="text" v-model="product.name" @blur="validate()" class="form-control" v-bind:class="{'is-invalid': errors.name}" />
                        <div class="invalid-feedback text-start" v-if="errors.name">{{ errors.name }}</div>
                    </div>
                </div>
                <div class="form-group row mb-3">
                    <label class="col-sm-3 col-form-label">Product Price</label>
                    <div class="col-sm-9">
                        <input type="text" v-model="product.price" @blur="validate()"  class="form-control" v-bind:class="{'is-invalid': errors.price}" />
                        <div class="invalid-feedback text-start">{{ errors.price }}</div>
                    </div>
                </div>
                <div class="form-group row mb-3">
                    <label class="col-sm-3 col-form-label">Description</label>
                    <div class="col-sm-9">
                        <textarea type="text"  v-model="product.description" @blur="validate()"  class="form-control"  rows="4" v-bind:class="{'is-invalid': errors.description}" />
                        <div class="invalid-feedback text-start">{{ errors.description }}</div>
                    </div>
                </div>
                <div class="form-group row mb-3">
                    <label class="col-sm-3 col-form-label"></label>
                    <div class="col-sm-9 justify-content-start text-start">
                        <button type="submit" class="btn btn-primary">Save</button> &nbsp;
                        <button type="reset" class="btn btn-danger">Cancel</button>
                    </div>
                </div>
            </form>
        </div>
    </div>
</template>

<script> 

export default {
  name: 'ProductForm', 
  data() {
    return {
        errors: {
            name: '',
            price: '',
            description:'',
        },
        product: {
            name: '',
            price: '',
            description:'',
        }
    }
  },
  methods: {
    validate () {
        this.errors = {
            name: '',
            price: '',
            description:'',
        }
        if (!this.product.name) {
            this.errors.name = "Product name is required"
        }
        if (!this.product.price) {
            this.errors.price = "Product price number is required"
        }else if (!this.isNumber(this.product.price)){
            this.errors.price = 'Product price must be number'
        }
        if (!this.product.description) {
            this.errors.description = "Product description name is required"
        } 
        
    },

    // Kiểm tra chỉ cho nhập số, ko cho nhập ký tự khác ngoài số
    isNumber (value) {
        return /^\d*$/.test(value)
    },
    
    save() {
        this.validate() 
    }
  },
}
</script>