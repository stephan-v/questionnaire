<template>
  <div class="modal-background">
    <div class="modal-content d-flex">
      <button class="close-button" @click="$emit('close')"></button>

      <div class="avatar">
        <div class="avatar-image"></div>
      </div>

      <div class="question">
        <h1>Do you think Sun is really an unlimited energy source just burning there for someone to use it’s infinite power?</h1>

        <hr>

        <div class="form-group mb-1">
          <input type="radio" id="one" value="Yes" v-model="picked">
          <label for="one">Yes</label>
        </div>

        <div class="form-group mb-1">
          <input type="radio" id="two" value="No" v-model="picked">
          <label for="two">No</label>
        </div>

        <hr>

        <button class="btn btn-primary submit d-flex ml-auto">Submit</button>
      </div>
    </div>
  </div>
</template>

<script>
  // const questions = [
  //   {
  //     question: 'Do you think Sun is really an unlimited energy source just burning there for someone to use it’s infinite power?',
  //     answers: [
  //         'Yes',
  //         'No'
  //     ],
  //     yes: {
  //       question: 'But, unlimited or limited is a relative term! Is it not?',
  //       answers: [
  //         'Yes',
  //         'No'
  //       ]
  //     },
  //     no: {
  //       //
  //     }
  //   }
  // ]

  export default {
    data() {
      return {
        picked: '',
      }
    },
  };
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
  .modal-background {
    position: fixed;
    width: 100%;
    height: 100%;
    left: 0;
    top: 0;
    z-index: 1;

    .modal-content {
      flex-direction: row;
      width: 675px;
      background: white;
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);

      .close-button {
        position: absolute;
        top: 0;
        right: 0;
        width: 20px;
        height: 20px;
        border: 2px solid black;
        border-radius: 50%;
        transform: translate(50%, -50%);
        background: white;
      }

      .avatar {
        background: #F1F1F1;
        padding: 20px;

        .avatar-image {
          border-radius: 50%;
          width: 100px;
          height: 100px;
          background: black;
        }
      }

      .question {
        padding: 1.5rem;

        .submit {
          background: #C63040;
          border-color: #C63040;
        }
      }

      h1 {
        margin-top: 0;
        font-size: 18px;
      }
    }
  }
</style>
