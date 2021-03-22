<template>
  <div class="form-wrapper w-full flex items-center">
    <FormulateForm v-model="formData">
      <FormulateInput type="group" name="attendees" :repeatable="true" label="Who is going to attend?" add-label="+ Add Attendee" validation="required" element-class="w-full ml-4 h-6 -mb-4">
        <div class="flex">
          <FormulateInput
            name="product"
            :options="{
              sp3a: 'SP3A',
              sp3w: 'SP3W or STU1800',
              sp4w: 'SP4W or STU2700',
              z25: 'Z25-800-1600mm wide',
              sch5: 'SCH5-750',
              clutch: 'CP2 Weld-on Clutch',
              section: 'V20 Corner Section',
              cornerSection: 'V20T 3 Way Corner Section',
              clamp: 'Pile Lifting Clamp',
              sealant: 'Swellseal-Joint Sealant',
            }"
            type="select"
            placeholder="Select an option"
            label="Type of Product"
            element-class="mr-2"
          />
          <FormulateInput type="number" name="length" validation="required" label="Length of pile" element-class="mr-2" />
          <FormulateInput type="number" name="custom" validation="required" label="Custom Length" element-class="mr-2" />
          <FormulateInput type="number" name="quantity" validation="required" label="Quantity" element-class="mr-2" />
        </div>
      </FormulateInput>
    </FormulateForm>
  </div>
</template>

<script>
export default {
  data() {
    return {
      formData: {},
    }
  },
}
</script>
