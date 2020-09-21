<template>
  <div class="accordion" role="tablist">
    <b-card no-body class="mb-1">
      <b-card-header header-tag="header" class="p-1" role="tab">
        <b-button block v-b-toggle.accordion-1 variant="info"
          >Wifi Troubleshooter</b-button
        >
      </b-card-header>
      <b-collapse id="accordion-1" accordion="my-accordion" role="tabpanel">
        <b-card-body>
          <b-card-text v-html="wifi"></b-card-text>
        </b-card-body>
      </b-collapse>
    </b-card>

    <b-card no-body class="mb-1">
      <b-card-header header-tag="header" class="p-1" role="tab">
        <b-button block v-b-toggle.accordion-2 variant="info"
          >BYOD on Mac</b-button
        >
      </b-card-header>
      <b-collapse id="accordion-2" accordion="my-accordion" role="tabpanel">
        <b-card-body>
          <object
            :data="pdfLink"
            type="application/pdf"
            width="800px”"
            height="600px"
          ></object>
        </b-card-body>
      </b-collapse>
    </b-card>

    <b-card no-body class="mb-1">
      <b-card-header header-tag="header" class="p-1" role="tab">
        <b-button block v-b-toggle.accordion-3 variant="info"
          >Accordion 3</b-button
        >
      </b-card-header>
      <b-collapse id="accordion-3" accordion="my-accordion" role="tabpanel">
        <b-card-body>
          <b-card-text v-html="generic"></b-card-text>
        </b-card-body>
      </b-collapse>
    </b-card>
  </div>
</template>

<script>
import troubleshooter from "../modules/troubleshooter";

export default {
  data() {
    return {
      pdfLink: require("../assets/BYODonMac.pdf"),
      wifi: troubleshooter.wifi,
      generic: troubleshooter.generic
    };
  }
};
</script>

<style scoped>
ol {
  margin: 0;
  padding: 0;
}

table td,
table th {
  padding: 0;
}

.c1 {
  color: #000000;
  font-weight: 400;
  text-decoration: none;
  vertical-align: baseline;
  font-size: 11pt;
  font-family: "Arial";
  font-style: normal;
}

.c4 {
  color: #000000;
  font-weight: 400;
  text-decoration: none;
  vertical-align: baseline;
  font-size: 14pt;
  font-family: "Arial";
  font-style: italic;
}

.c0 {
  padding-top: 0pt;
  padding-bottom: 0pt;
  line-height: 1.15;
  orphans: 2;
  widows: 2;
  text-align: left;
}

.c3 {
  background-color: #ffffff;
  max-width: 468pt;
  padding: 72pt 72pt 72pt 72pt;
}

.c6 {
  font-size: 14pt;
  font-style: italic;
}

.c5 {
  height: 11pt;
}

.c2 {
  font-weight: 700;
}

.title {
  padding-top: 0pt;
  color: #000000;
  font-size: 26pt;
  padding-bottom: 3pt;
  font-family: "Arial";
  line-height: 1.15;
  page-break-after: avoid;
  orphans: 2;
  widows: 2;
  text-align: left;
}

.subtitle {
  padding-top: 0pt;
  color: #666666;
  font-size: 15pt;
  padding-bottom: 16pt;
  font-family: "Arial";
  line-height: 1.15;
  page-break-after: avoid;
  orphans: 2;
  widows: 2;
  text-align: left;
}

li {
  color: #000000;
  font-size: 11pt;
  font-family: "Arial";
}

p {
  margin: 0;
  color: #000000;
  font-size: 11pt;
  font-family: "Arial";
}

h1 {
  padding-top: 20pt;
  color: #000000;
  font-size: 20pt;
  padding-bottom: 6pt;
  font-family: "Arial";
  line-height: 1.15;
  page-break-after: avoid;
  orphans: 2;
  widows: 2;
  text-align: left;
}

h2 {
  padding-top: 18pt;
  color: #000000;
  font-size: 16pt;
  padding-bottom: 6pt;
  font-family: "Arial";
  line-height: 1.15;
  page-break-after: avoid;
  orphans: 2;
  widows: 2;
  text-align: left;
}

h3 {
  padding-top: 16pt;
  color: #434343;
  font-size: 14pt;
  padding-bottom: 4pt;
  font-family: "Arial";
  line-height: 1.15;
  page-break-after: avoid;
  orphans: 2;
  widows: 2;
  text-align: left;
}

h4 {
  padding-top: 14pt;
  color: #666666;
  font-size: 12pt;
  padding-bottom: 4pt;
  font-family: "Arial";
  line-height: 1.15;
  page-break-after: avoid;
  orphans: 2;
  widows: 2;
  text-align: left;
}

h5 {
  padding-top: 12pt;
  color: #666666;
  font-size: 11pt;
  padding-bottom: 4pt;
  font-family: "Arial";
  line-height: 1.15;
  page-break-after: avoid;
  orphans: 2;
  widows: 2;
  text-align: left;
}

h6 {
  padding-top: 12pt;
  color: #666666;
  font-size: 11pt;
  padding-bottom: 4pt;
  font-family: "Arial";
  line-height: 1.15;
  page-break-after: avoid;
  font-style: italic;
  orphans: 2;
  widows: 2;
  text-align: left;
}
</style>
