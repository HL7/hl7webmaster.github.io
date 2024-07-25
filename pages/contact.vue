<template>
  <div
    class="mx-8 mt-11 md:mt-[7.75rem] mb-6 bg-darkgrey text-white flex flex-col !justify-center md:flex-nowrap md:flex-row md:gap-8 lg:gap-16 xl:gap-32">
    <div class="flex flex-col justify-center items-center md:justify-start md:items-start md:w-1/2 xl:w-1/4">
      <div class="self-start">
        <h2 class="satoshi-black font-bold contact-heading pb-2">
          Let's Connect!
        </h2>
      </div>
      <div class="flex justify-center py-8 max-w-sm md:hidden">
        <img class="max-w-l" alt="Email and letter illustration" src="~/assets/img/letter.png" />
      </div>
      <div class="w-full">
        <p class="py-2 font-normal">
          Learn more about our current domains, use cases and how to engage with
          the Codex community. Attend an event, become a member, participate in
          a use case, partner on an initiative, directly support the CodeX
          mission.
        </p>
        <p class="py-4 font-normal">
          Get in touch! Email us at
          <a class="underline" href="mailto:codeX@hl7.org">CodeX@hl7.org</a>
          or fill out the contact form.
        </p>
      </div>
    </div>
    <div v-once id="hubspotForm" class="bg-white px-8 py-2 rounded-lg w-full md:w-1/2 mt-6 md:mt-0 xl:w-1/3"></div>
  </div>
</template>
<script>

export default {
  layout: 'DefaultGrey',
  head() {
    return {
      title: 'Codex Contact',
      meta: [
        // hid is used as unique identifier. Do not use `vmid` for it as it will not work
        {
          hid: 'description',
          name: 'description',
          content:
            'Instructions on how to contact CodeX community organizers and a form for easily doing this from the CodeX website.',
        },
      ],
    }
  },
  mounted() {
    const contactFormScript = document.createElement('script')
    contactFormScript.src = "https://js.hsforms.net/forms/v2.js";
    document.body.appendChild(contactFormScript);
    contactFormScript.addEventListener("load", () => {
      if (window.hbspt) {
        window.hbspt.forms.create({
          region: "na1",
          portalId: "8047841",
          formId: "9f72a8ab-5458-49c6-a88b-f27688d23792",
          target: "#hubspotForm"
        })
      }
    })
  },
}
</script>
