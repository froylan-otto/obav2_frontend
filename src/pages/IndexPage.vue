<template>
  <q-page padding>
    <div class="row">
      <div class="col-9 full-height">
        <q-card class="my-card bg-white text-black" flat>
          <q-card-section>
            <q-table
              title="Treats"
              :rows="rows"
              :columns="columns"
              row-key="name"
              flat
            />
          </q-card-section>

          <q-separator dark />

          <q-card-actions>
            <q-btn color="primary" icon="save">Action 1</q-btn>
          </q-card-actions>
        </q-card>
      </div>
      <div class="q-pl-sm col-3">
        <q-btn color="primary" icon="upload" style="width: 100%">
          Upload File
        </q-btn>

        <q-card class="q-mt-sm my-card bg-white text-black" flat>
          <q-card-section>
            <div class="text-h5 q-pb-sm">Last activity</div>
            <hr />
            <div class="text-subtitle2">file5.csv uploaded 50 minutes ago</div>
            <hr />
            <div class="text-subtitle2">file4.csv uploaded 51 minutes ago</div>
            <hr />
            <div class="text-subtitle2">file3.csv uploaded 52 minutes ago</div>
            <hr />
            <div class="text-subtitle2">file2.csv uploaded 53 minutes ago</div>
            <hr />
            <div class="text-subtitle2">file1.csv uploaded 54 minutes ago</div>
          </q-card-section>

          <q-separator dark />

          <q-card-actions>
            <q-btn color="primary " icon="upload"> Upload </q-btn>
          </q-card-actions>
        </q-card>
      </div>
    </div>

    <q-page-sticky position="bottom-right" :offset="[40, 18]">
      <q-btn fab icon="chat" color="accent" label="Chatbot" />
    </q-page-sticky>
  </q-page>
</template>

<script>
import { defineComponent } from "vue";

const columns = [
  {
    name: "name",
    required: true,
    label: "Dessert (100g serving)",
    align: "left",
    field: (row) => row.name,
    format: (val) => `${val}`,
    sortable: true,
  },
  {
    name: "calories",
    align: "center",
    label: "Calories",
    field: "calories",
    sortable: true,
  },
  { name: "fat", label: "Fat (g)", field: "fat", sortable: true },
  { name: "carbs", label: "Carbs (g)", field: "carbs" },
  { name: "protein", label: "Protein (g)", field: "protein" },
  { name: "sodium", label: "Sodium (mg)", field: "sodium" },
  {
    name: "calcium",
    label: "Calcium (%)",
    field: "calcium",
    sortable: true,
    sort: (a, b) => parseInt(a, 10) - parseInt(b, 10),
  },
  {
    name: "iron",
    label: "Iron (%)",
    field: "iron",
    sortable: true,
    sort: (a, b) => parseInt(a, 10) - parseInt(b, 10),
  },
];

const rows = [
  {
    name: "Frozen Yogurt",
    calories: 159,
    fat: 6.0,
    carbs: 24,
    protein: 4.0,
    sodium: 87,
    calcium: "14%",
    iron: "1%",
  },
  {
    name: "Ice cream sandwich",
    calories: 237,
    fat: 9.0,
    carbs: 37,
    protein: 4.3,
    sodium: 129,
    calcium: "8%",
    iron: "1%",
  },
  {
    name: "Eclair",
    calories: 262,
    fat: 16.0,
    carbs: 23,
    protein: 6.0,
    sodium: 337,
    calcium: "6%",
    iron: "7%",
  },
  {
    name: "Cupcake",
    calories: 305,
    fat: 3.7,
    carbs: 67,
    protein: 4.3,
    sodium: 413,
    calcium: "3%",
    iron: "8%",
  },
  {
    name: "Gingerbread",
    calories: 356,
    fat: 16.0,
    carbs: 49,
    protein: 3.9,
    sodium: 327,
    calcium: "7%",
    iron: "16%",
  },
  {
    name: "Jelly bean",
    calories: 375,
    fat: 0.0,
    carbs: 94,
    protein: 0.0,
    sodium: 50,
    calcium: "0%",
    iron: "0%",
  },
  {
    name: "Lollipop",
    calories: 392,
    fat: 0.2,
    carbs: 98,
    protein: 0,
    sodium: 38,
    calcium: "0%",
    iron: "2%",
  },
  {
    name: "Honeycomb",
    calories: 408,
    fat: 3.2,
    carbs: 87,
    protein: 6.5,
    sodium: 562,
    calcium: "0%",
    iron: "45%",
  },
  {
    name: "Donut",
    calories: 452,
    fat: 25.0,
    carbs: 51,
    protein: 4.9,
    sodium: 326,
    calcium: "2%",
    iron: "22%",
  },
  {
    name: "KitKat",
    calories: 518,
    fat: 26.0,
    carbs: 65,
    protein: 7,
    sodium: 54,
    calcium: "12%",
    iron: "6%",
  },
];

/*export default defineComponent({
  name: "IndexPage",
  setup() {
    return {
      columns,
      rows,
    };
  },
});*/
export default {
  setup() {
    return {
      columns,
      rows,
    };
  },
};
</script>
