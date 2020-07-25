<template>
  <div id="main">
    <div class="content">
      <div class="table px-3">
        <div class="table-nav">
          <b-row class="py-4">
            <b-col class="text-left" cols="5">Barber Shop</b-col>
            <b-col cols="4">
              <b-form>
                <b-input-group prepend="@" class="mb-2 mr-sm-2 mb-sm-0">
                  <b-input placeholder="Search for barber shop..."></b-input>
                </b-input-group>
              </b-form>
            </b-col>
            <b-col class="text-left" cols="3">Filter by</b-col>
          </b-row>
        </div>
        <b-table
          sticky-header="60vh"
          :no-border-collapse="false"
          responsive
          :items="items"
          :fields="fields"
        >
          <!-- We are using utility class `text-nowrap` to help illustrate horizontal scrolling -->
          <template>
            <div class="text-nowrap">Row ID</div>
          </template>
          <template v-slot:head()="scope">
            <div class="text-nowrap">Heading {{ scope.label }}</div>
          </template>
        </b-table>
        <div class="table-footer">
          <b-row class="py-4 justify-content-between" align-center>
            <b-col class="text-left" cols="4"
              >Showing 1 to 8 of 16 entries</b-col
            >
            <b-col class="text-right" cols="4"
              ><div>
                <b-pagination-nav
                  pills
                  size="sm"
                  number-of-pages="10"
                  base-url="#"
                  align="right"
                  limit="2"
                ></b-pagination-nav></div
            ></b-col>
          </b-row>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      stickyHeader: true,
      noCollapse: false,
      fields: [
        {
          key: "id",
          stickyColumn: true,
          isRowHeader: true,
          variant: "primary",
        },
        "a",
        "b",
        "c",
        "d",
        "e",
        "f",
        "g",
        "h",
        "i",
      ],
      items: [
        {
          id: 1,
          a: 0,
          b: 1,
          c: 2,
          d: 3,
          e: 4,
          f: 5,
          g: 6,
          h: 7,
          i: 8,
          j: 9,
          k: 10,
          l: 11,
        },
        {
          id: 2,
          a: 0,
          b: 1,
          c: 2,
          d: 3,
          e: 4,
          f: 5,
          g: 6,
          h: 7,
          i: 8,
          j: 9,
          k: 10,
          l: 11,
        },
        {
          id: 3,
          a: 0,
          b: 1,
          c: 2,
          d: 3,
          e: 4,
          f: 5,
          g: 6,
          h: 7,
          i: 8,
          j: 9,
          k: 10,
          l: 11,
        },
        {
          id: 4,
          a: 0,
          b: 1,
          c: 2,
          d: 3,
          e: 4,
          f: 5,
          g: 6,
          h: 7,
          i: 8,
          j: 9,
          k: 10,
          l: 11,
        },
        {
          id: 5,
          a: 0,
          b: 1,
          c: 2,
          d: 3,
          e: 4,
          f: 5,
          g: 6,
          h: 7,
          i: 8,
          j: 9,
          k: 10,
          l: 11,
        },
        {
          id: 6,
          a: 0,
          b: 1,
          c: 2,
          d: 3,
          e: 4,
          f: 5,
          g: 6,
          h: 7,
          i: 8,
          j: 9,
          k: 10,
          l: 11,
        },
        {
          id: 7,
          a: 0,
          b: 1,
          c: 2,
          d: 3,
          e: 4,
          f: 5,
          g: 6,
          h: 7,
          i: 8,
          j: 9,
          k: 10,
          l: 11,
        },
        {
          id: 8,
          a: 0,
          b: 1,
          c: 2,
          d: 3,
          e: 4,
          f: 5,
          g: 6,
          h: 7,
          i: 8,
          j: 9,
          k: 10,
          l: 11,
        },
        {
          id: 9,
          a: 0,
          b: 1,
          c: 2,
          d: 3,
          e: 4,
          f: 5,
          g: 6,
          h: 7,
          i: 8,
          j: 9,
          k: 10,
          l: 11,
        },
        {
          id: 10,
          a: 0,
          b: 1,
          c: 2,
          d: 3,
          e: 4,
          f: 5,
          g: 6,
          h: 7,
          i: 8,
          j: 9,
          k: 10,
          l: 11,
        },
      ],
    };
  },
};
</script>

<style scoped>
#main /deep/ {
  position: absolute;
  z-index: -1;
  top: 0;
  right: 0;
  height: 100vh;
  width: 85vw;
  background-color: #348f6c;
}

#main .content {
  background-color: #F7F6F9;
  height: 100%;
  border: 1vmin solid #348f6c;
  border-radius: 4vmin;
}

#main .content .table {
  width: 60vw;
  margin: 0 auto;
  background-color: #fff;
  border-radius: 1.5vmin;
}
</style>
