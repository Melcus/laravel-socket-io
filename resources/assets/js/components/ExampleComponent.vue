<template>
    <div class="container">
        <div class="row justify-content-center">
            <div class="col-md-8">
                <div class="card card-default">
                    <div class="card-header">Example Component</div>

                    <div class="card-body">
                        I'm an example component.
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
  mounted() {
    console.log("initiating here");
    window.Echo.channel("echo-channel").listen("MessagePushed", e => {
      console.log("message received from event >>>> ", e.message);
      console.log("------------- ");
    });
  }
};
</script>
