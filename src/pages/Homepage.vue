<template>
  <div class="relative-position">

    <!-- Hero section  -->
    <div class="hero">
      <!-- <h1>Hello</h1> -->
      <div class="write_up">
        <h1 class="">GIDARH</h1>
        <h4>FIND YOUR BEST <span class="text-primary">HOME</span></h4>
      </div>
    </div>

    <!-- Tab on Hero  -->
    <div class="tab">
      <div class="q-gutter-y-md" style="width: 100%">
        <!-- <q-card> -->
          <q-tabs
            v-model="tab"
            dense
            class=" text-grey-7 bg-white q-my-none"
            active-color="white"
            active-bg-color="primary"
            align="justify"
            style="width: 50%; height: 4rem; border-radius: 8px 8px 0 0"

          >
            <q-tab name="sale" label="FOR SALE" />
            <q-tab name="rent" label="FOR RENT" />
            <q-tab name="shortlet" label="FOR SHORTLET" />
          </q-tabs>

          <q-tab-panels v-model="tab" animated class="bg-primary text-white q-my-none">
            <q-tab-panel name="sale">
              <div class="row justify-evenly q-py-md">
                <q-input style="width:20%" color="" v-model="search" placeholder="Search" filled class="bg-white">
                  <template v-slot:prepend>
                    <q-icon name="search" />
                  </template>
                </q-input>

                <q-select style="width:15%" filled v-model="minimum" :options="options" label=" NGN Minimum" class="bg-white" />
                <q-select style="width:15%" filled v-model="maximum" :options="options" label="NGN maximum" class="bg-white"/>
                <q-select style="width:15%" filled v-model="bedroom" :options="options" label="Bedroom" class="bg-white" >
                   <template v-slot:prepend>
                    <q-icon name="bed" />
                  </template>
                </q-select>
                <q-select style="width:15%" filled v-model="bathroom" :options="options" label="Bathroom" class="bg-white">
                   <template v-slot:prepend>
                    <q-icon name="bathtub" />
                  </template>
                </q-select>


                <q-btn label="SEARCH" icon="search" style="width:12%"/>
              </div>
            </q-tab-panel>

            <q-tab-panel name="rent">
              <div class="row justify-evenly q-py-md">
                <q-input style="width:20%" color="" v-model="search" placeholder="Search" filled class="bg-white">
                  <template v-slot:prepend>
                    <q-icon name="search" />
                  </template>
                </q-input>

                <q-select style="width:15%" filled v-model="minimum" :options="options" label=" NGN Minimum" class="bg-white" />
                <q-select style="width:15%" filled v-model="maximum" :options="options" label="NGN maximum" class="bg-white"/>
                <q-select style="width:15%" filled v-model="bedroom" :options="options" label="Bedroom" class="bg-white" >
                   <template v-slot:prepend>
                    <q-icon name="bed" />
                  </template>
                </q-select>
                <q-select style="width:15%" filled v-model="bathroom" :options="options" label="Bathroom" class="bg-white">
                   <template v-slot:prepend>
                    <q-icon name="bathtub" />
                  </template>
                </q-select>


                <q-btn label="SEARCH" icon="search" style="width:12%"/>
              </div>
            </q-tab-panel>

            <q-tab-panel name="shortlet">
              <div class="row justify-evenly q-py-md">
                <q-input style="width:20%" color="" v-model="search" placeholder="Search" filled class="bg-white">
                  <template v-slot:prepend>
                    <q-icon name="search" />
                  </template>
                </q-input>

                <q-select style="width:15%" filled v-model="minimum" :options="options" label=" NGN Minimum" class="bg-white" />
                <q-select style="width:15%" filled v-model="maximum" :options="options" label="NGN maximum" class="bg-white"/>
                <q-select style="width:15%" filled v-model="bedroom" :options="options" label="Bedroom" class="bg-white" >
                   <template v-slot:prepend>
                    <q-icon name="bed" />
                  </template>
                </q-select>
                <q-select style="width:15%" filled v-model="bathroom" :options="options" label="Bathroom" class="bg-white">
                   <template v-slot:prepend>
                    <q-icon name="bathtub" />
                  </template>
                </q-select>


                <q-btn label="SEARCH" icon="search" style="width:12%"/>
              </div>
            </q-tab-panel>
          </q-tab-panels>
        <!-- </q-card> -->
      </div>
    </div>

    <!-- Properties for sale -->
    <div class="sale">
      <!-- Heading -->
      <div class="row justify-between" style="width:100%; ">
        <h5 class="border_left">Properties of <span class="text-blue">Sale</span></h5>
        <q-btn label="See more properties" icon-right="arrow_right_alt" class="" color="primary"  style="height: 50%; margin: auto 0;"/>
      </div>

      <!-- Cards -->

        <q-scroll-area visible="false" style="height: 400px; width: 100%;">
          <div class="row no-wrap">
            <div v-for="n in 10" :key="n"  class="q-pa-sm col-3">
              <q-card class="my-card">
                <img src="/Homepage/homee.png">

                <q-card-section class="q-px-none q-pb-lg">
                  <div class="q-px-md">
                    <div class="text-subtitle1 q-mb-sm">4 Bedroom Apartment for Rent</div>
                    <div class="text-subtitle2 q-mb-sm"><q-icon name="place" /> U/Rimi Kaduna </div>
                    <div class="text-subtitle1 q-mb-sm"> N10,000,000  <span>Fixed Price</span> </div>
                  </div>

                  <hr>
                  <div class="row q-px-md q-pt-sm">
                    <div class="text-subtitle2 q-mr-lg"> 4 <q-icon name="bed" size="1.1rem" /> </div>
                    <div class=" q-mr-lg text-4"> 4 <q-icon name="bathtub" size="1.1rem" /> </div>
                    <div class="text-subtitle2 q-mr-lg"> 4 <q-icon name="directions_car" size="1.1rem" /> </div>
                  </div>

                </q-card-section>
              </q-card>
            </div>
          </div>
        </q-scroll-area>

    </div>

    <!-- Properties for Rent -->
    <div class="sale">
      <!-- Heading -->
      <div class="row justify-between" style="width:100%; ">
        <h5 class="border_left">Properties of <span class="text-blue">Rent</span></h5>
        <q-btn label="See more properties" icon-right="arrow_right_alt" class="" color="primary"  style="height: 50%; margin: auto 0;"/>
      </div>

      <!-- Cards -->

        <q-scroll-area visible="false" style="height: 400px;">
          <div class="row no-wrap">
            <div v-for="n in 10" :key="n"  class="q-pa-sm col-3">
              <q-card class="my-card">
                <img src="/Homepage/homee.png">

                <q-card-section class="q-px-none q-pb-lg">
                  <div class="q-px-md">
                    <div class="text-subtitle1 q-mb-sm">4 Bedroom Apartment for Rent</div>
                    <div class="text-subtitle2 q-mb-sm"><q-icon name="place" /> U/Rimi Kaduna </div>
                    <div class="text-subtitle1 q-mb-sm"> N10,000,000  <span>Fixed Price</span> </div>
                  </div>

                  <hr>
                  <div class="row q-px-md q-pt-sm">
                    <div class="text-subtitle2 q-mr-lg"> 4 <q-icon name="bed" size="1.1rem" /> </div>
                    <div class=" q-mr-lg text-4"> 4 <q-icon name="bathtub" size="1.1rem" /> </div>
                    <div class="text-subtitle2 q-mr-lg"> 4 <q-icon name="directions_car" size="1.1rem" /> </div>
                  </div>

                </q-card-section>
              </q-card>
            </div>
          </div>
        </q-scroll-area>

    </div>

    <!-- Our Services -->
    <div style="background: rgba(88, 93, 249, 0.08)" class=" q-py-lg">
      <h3 class="text-center">OUR <span>SERVICES</span></h3>
      <p style="width:25%" class="text-center q-mx-auto"> When it comes to real estate and properties, we’re here
every step of the way to help you move forward.  </p>

      <div class="row justify-center q-pb-xl">
        <q-card class="my-card shadow" style="margin-right: 5%;">
          <q-card-section class="q-px-none q-pb-lg">
            <div class="q-px-md">
              <div class=" q-mb-sm border_leftt text-h6">Fixed Fee &  Support</div>
              <p> Lorem ipsum dolor sit amet consectetur adipisicing elitpiciatis est vitae provident doloribus asperiores perferendis laborum, porro distinctio nisi itaque dolorum architecto? </p>
              <router-link to="#" style="padding-left: 8%"> Learn More </router-link>
            </div>
          </q-card-section>
        </q-card>

        <q-card class="my-card shadow" style="margin-right: 5%;">
          <q-card-section class="q-px-none q-pb-lg">
            <div class="q-px-md">
              <div class=" q-mb-sm border_leftt text-h6">Local Estate Agents</div>
              <p> Lorem ipsum dolor sit amet consectetur adipisicing elitpiciatis est vitae provident doloribus asperiores perferendis laborum, porro distinctio nisi itaque dolorum architecto? </p>
              <router-link to="#" style="padding-left: 8%"> Learn More </router-link>
            </div>
          </q-card-section>
        </q-card>

        <q-card class="my-card shadow" style="margin-right: 5%;">
          <q-card-section class="q-px-none q-pb-lg">
            <div class="q-px-md">
              <div class=" q-mb-sm border_leftt text-h6">Quick & Easy</div>
              <p> Lorem ipsum dolor sit amet consectetur adipisicing elitpiciatis est vitae provident doloribus asperiores perferendis laborum, porro distinctio nisi itaque dolorum architecto? </p>
              <router-link to="#" style="padding-left: 8%"> Learn More </router-link>
            </div>
          </q-card-section>
        </q-card>
      </div>
    </div>

    <!-- Call To Action section  -->
    <div class="row q-pa-xl cta" >
      <div class="col-7">
        <q-card class="shadow action">
          <q-card-section class="q-px-none q-pb-lg">
            <div class="q-px-md action_text">
              <div class=" q-mb-sm text-h4">Buy, Rent and Sell</div>
              <p class=""> Lorem ipsum dolor sit amet consectetur adipisicing elitpiciatis est vitae provident doloribus asperiores perferendis laborum, porro distinctio nisi itaque dolorum architecto? </p>
              <q-btn label="SIGN UP" color="primary" style="width:80%" />
            </div>
          </q-card-section>
        </q-card>
      </div>

      <div class="col-5 q-px-xl relative-position">
          <q-img src="/Homepage/dots.png" class="dots" width="50%" height="30%rem" />
          <q-img src="/Homepage/house.png" class="upper_img" />
      </div>

    </div>

  </div>
</template>

<script>
import { ref } from 'vue'

export default {
  data () {
    return {
      tab: ref('sale')
    }
  }
}
</script>

<style scoped>
  .hero{
    background-image: url('/Homepage/hero.png');
    background-position: 100%;
    background-repeat: no-repeat;
    height: 550px;
    position: relative;
    /* width: 100%; */
  }
.write_up{
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  width: 70%;
  text-align: center;
  color: white;
}

.tab{
  padding: 0 8%;
  position: relative;
  width: 100%;
  top: -3rem;
}

.sale{
  padding: 0 8% 3%;
}

.border_left{
  border-left: 5px solid #037BE0;
  padding: 1%;
}

.border_leftt{
  border-left: 5px solid #037BE0;
  padding: 1% 4%;
}

.my-card{
  width: 100%;
  max-width: 280px;
  margin-right: 1%;
}

.my-card p{
  padding-left: 8%;
}

hr{
  color:  rgb(128, 128, 128,0.5);
}

.shadow{
  box-shadow: 4px 4px 9px 2px rgba(137,241,177,0.45);
}

.action{
  padding: 18% 8%;
  margin: auto 0;
  width:100%;
  position: relative;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}
.action_text{
  width: 50%;
}

.dots{
  position: relative;
  top: 50%;
  left: 50%;
  transform: translate(-50%,-50%);
}

.upper_img{
  position: relative;
  top: -20%;
  left: -50%;

}

.cta{
  background: rgb(152, 152, 152, 0.1)
}

</style>
