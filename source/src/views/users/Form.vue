<template>
    <div class="b-form">
        <div class="pricing-header px-3 py-3 pt-md-5 pd-md-4 mx-auto text-center">
            <h3 class="display-5">User Infomation </h3>
            <router-link to="/user">Back </router-link>
        </div>
        <div class="container">
            <form @submit.prevent="save()">
                <div class="form-group row mb-3">
                    <label class="col-sm-3 col-form-label">Product name</label>
                    <div class="col-sm-9">
                        <input type="text" class="form-control" />
                    </div>
                </div>
                <div class="form-group row mb-3">
                    <label class="col-sm-3 col-form-label">Product Price</label>
                    <div class="col-sm-9">
                        <input type="text" class="form-control" />
                    </div>
                </div>
                <div class="form-group row mb-3">
                    <label class="col-sm-3 col-form-label">Description</label>
                    <div class="col-sm-9">
                        <textarea type="text" class="form-control"  rows="4"/>
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
    
</script>