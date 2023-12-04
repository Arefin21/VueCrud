<template>
    <div>
      <div class="card">
        <div class="card-header">
          <h4>
            Students
            <RouterLink to="/student/create" class="btn btn-primary float-end" >Add Students</RouterLink>
          </h4>
        </div>
        <div class="car-body">
          <table class="table table-bordered">
            <thead>
              <tr>
                <th>ID</th>
                <th>Name</th>
                <th>Course</th>
                <th>Email</th>
                <th>Phone</th>
                <th>Created At</th>
                <th>Action</th>
              </tr>
            </thead>
            <tbody>
              <tr>
                <td>

                </td>
              </tr>
            </tbody>
          </table>
        </div>
      </div>
    </div>
  </template>

  <script>
  import axios from 'axios'
  export default{
    name:'students',
    data(){
      return{
        students:[]
      }
    },
    mounted(){
      this.getStudent();
      //console.log('i am here');
    },
    methods:{
      getStudent(){
        axios.get('').then(res=>{
          this.students=res.data.students
          //console.log(this.students)
        });
      }
    },
  }
</script>