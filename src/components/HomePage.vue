<template>
  <div class="row justify-between header">
    <img class="image-logo" src="@/assets/logo.png" alt="logo" />
    <div class="row">
      <div class="q-my-auto" v-for="(nav, i) in navs" :key="i">
        <q-btn :label="nav.label" flat :to="nav.value" />
      </div>
    </div>
  </div>
  <div class="main">
    <div class="row full-width justify-between banner">
      <div class="column justify-center">
        <div class="heading-section">
          <h5 class="heading">
            Design, deployment, and <br />
            management <br />partner for your cloud
          </h5>
          <q-btn
            size="18px"
            class="book-now-btn"
            label="Book Now"
            color="primary"
            rounded
          />
        </div>
      </div>
      <img class="page-slider" src="@/assets/home-1.png" alt="Home" />
    </div>
    <div class="row full-width our-partners">
      <div class="row partner-card">
        <img
          class="partner-img q-my-auto q-mr-lg"
          src="@/assets/partner-icon.png"
          alt="partner-logo"
        />
        <div class="text-section">
          <h5 class="q-my-none text-weight-bold">Our Partners</h5>
          <p>
            The benefits of adopting a DevOps methodology are numerous, and
            selecting the proper managed DevOps partners is a crucial part of
            the transformation
          </p>
        </div>
      </div>
      <div class="row justify-between full-width">
        <div v-for="(partner, i) in partners" :key="i" class="all-partners">
          <q-card class="my-card" flat bordered>
            <div class="partner-image">
              <q-img class="image" fit="contain" :src="partner.value" />
            </div>

            <q-card-section class="text-center">
              <div class="text-h5 q-mt-sm q-mb-xs">{{ partner.label }}</div>
            </q-card-section>
          </q-card>
        </div>
      </div>
    </div>
    <div class="row justify-between full-width services">
      <div class="col-12 text-center q-mb-md">
        <h3 class="q-my-none">Services</h3>
      </div>
      <div
        v-for="(service, i) in services"
        class="service-card relative-position"
        :key="i"
      >
        <q-card flat bordered>
          <q-card-section class="q-pa-none text-center">
            <img src="/images/service-cards/service-card-1.png" />
            <div class="text-white q-mt-sm q-mb-xs q-px-md absolute-bottom">
              <h5 class="text-h5 q-my-lg">
                {{ service.label }}
              </h5>
              <p class="text-body1">
                {{ service.miniDescription }}
              </p>
              <q-btn label="Know More" color="secondary" class="q-mb-md" />
            </div>
          </q-card-section>
        </q-card>
      </div>
    </div>
  </div>
  <div class="row full-width justify-between footer">
    <div class="col-12 q-mb-sm">
      <h4 class="q-my-sm">CloudDrive</h4>
    </div>
    <div class="col-4 column">
      <h5 class="q-my-sm">We Listen Your Prosper</h5>
      <p class="text-body1">
        Ready to Shift to the DevOps Culture? Talk to our experts at Cloud Drove
        to understand in detail the process and benefits.
      </p>
    </div>
    <div class="col-4 text-center column">
      <h5 class="q-my-sm">Site</h5>
      <p class="text-body1">About Us</p>
      <p class="text-body1">Services</p>
      <p class="text-body1">Our Partners</p>
      <p class="text-body1">Contact Us</p>
    </div>
    <div class="col-4 text-right column">
      <div class="q-ml-auto text-left">
        <h5 class="q-my-sm">Contact</h5>
        <p>Write us at hello@clouddrive.com</p>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from "vue";
const navs = ref([
  {
    label: "Home",
    value: "home",
  },
  {
    label: "Services",
    value: "services",
  },
  {
    label: "About Us",
    value: "about-us",
  },
  {
    label: "Portfolio",
    value: "portfolio",
  },
  {
    label: "Teams",
    value: "teams",
  },
  {
    label: "Contact Us",
    value: "contact-us",
  },
]);
const partners = ref([
  {
    label: "Amazaon Web Services",
    value: "/images/aws.png",
  },
  {
    label: "Digital Ocean",
    value: "/images/digital-ocean.png",
  },
  {
    label: "Microsoft",
    value: "/images/microsoft.png",
  },
  {
    label: "Datadog",
    value: "/images/data-dog.png",
  },
]);
const services = ref([
  {
    label: "Cloud Migration",
    miniDescription:
      "Get the right solution of Cloud to take your organisation into the Next Generation of Operations. Migrate hassel free.",
    description:
      "CloudDrove makes your cloud adoption journey security centric, defined infrastructure towards a structured with a risk-mitigated approach to address your migration challenges. Reduce application downtime with Terraform and ensure uninterrupted transition",
  },
  {
    label: "Dev Environments ",
    miniDescription:
      "Bring the world of developers work for your project, under one roof - without creating a chaos of codes & dependencies",
    description:
      "Work on Next Gen Dockerized Dev Environments driven by Automated and Self Serve based catalogue solutions. Hasselfree onboarding of new developers without bleeding on deadlines.",
  },
  {
    label: "Release Engineering",
    miniDescription:
      "Automate your development pipelines with an ease of operations and enable rapid iterations.",
    description:
      "Facilitate rapid Software Development cycle with Dockerization for continuous development and testing. Aim for defectless releases with short release cycles. Create a dedicated pipeline to remove manual error and enable you for a rapid iteration so that you can focus on product release.",
  },
]);
</script>

<style lang="scss">
@font-face {
  font-family: "c1bold";
  src: url("../assets/fonts/GlacialIndifference-Bold.otf");
}
@font-face {
  font-family: "c1italic";
  src: url("../assets/fonts/GlacialIndifference-Italic.otf");
}
@font-face {
  font-family: "c1regular";
  src: url("../assets/fonts/GlacialIndifference-Regular.otf");
}
.header {
  padding: 10px 100px;
  box-shadow: 0 0 5px rgb(0 0 0 / 40%);
  .image-logo {
    max-width: 150px;
    max-height: 150px;
    width: 100%;
    height: 100%;
  }
}
.main {
  .banner {
    .heading-section {
      margin-left: 80px;
    }
    .heading {
      font-family: "c1bold" !important;
      line-height: 3rem;
      font-size: 2.5rem;
      color: #555555;
    }
    .page-slider {
      margin-top: 40px;
      max-width: 50%;
      width: 100%;
    }
    .book-now-btn {
      width: 200px;
      height: 50px;
      font-weight: 600;
    }
  }
  .our-partners {
    padding: 80px 100px;
    background-image: linear-gradient(90deg, #f3f3f3, #d2d2d2);

    .partner-card {
      background-image: linear-gradient(90deg, #5fb4f8, #0a7ffe);
      padding: 2rem 2.5rem;
      border-radius: 0.5rem;
      box-shadow: 4px 5px 15px rgb(0 0 0 / 60%);

      .text-section {
        max-width: 500px;
        width: 100%;
        color: white;
        p {
          font-size: 18px;
        }
      }
      .partner-img {
        background-color: rgba(38, 143, 204, 0.822);
        border-radius: 50%;
        padding: 10px;
        max-width: 80px;
        max-height: 80px;
        object-fit: contain;
        width: 100%;
        height: 100%;
      }
    }
    .all-partners {
      padding-top: 50px;
      .my-card {
        background: #fff5f5;
        text-align: center;
        padding: 1.25rem;
        border-radius: 0.3rem;
        box-shadow: 0 0 20px rgb(0 0 0 / 10%);
        transition: all 0.3s;
        min-height: 325px;
        max-width: 350px;
        width: 100%;
        border: unset !important;
        .partner-image {
          display: flex;
          width: 250px;
          height: 250px;
          margin: auto;
          .image {
            object-fit: contain !important;
            max-width: 90px;
            max-height: 90px;
            width: 100%;
            height: 100%;
            margin: auto;
          }
        }
      }
    }
  }
  .services {
    padding: 80px 100px;
    background: linear-gradient(0deg, #ababab, #ccc 41.07%, #fff 76.05%);
    h3 {
      margin-bottom: 1.875rem;
      color: #606060;
      font-weight: 700;
      font-size: 2.225rem;
    }
    .service-card {
      width: 500px;
      height: 600px;
      overflow: hidden;
      img {
        width: 500px;
        height: 600px;
        object-fit: cover;
      }
    }
  }
}
.footer {
  background: #262626;
  padding: 50px 100px;
  color: #fff;
}
</style>
