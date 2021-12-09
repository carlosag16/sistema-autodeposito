<template >
   <section class="section" style="border: solid 1px; " >
        <b-field >
            <b-field label="Nome " :label-position="on-border">
                <b-input  v-model="name"></b-input>
            </b-field>
            <b-field label="Items per page">
                <b-input type="number" v-model="perPage"></b-input>
            </b-field>
        </b-field>
        <b-field grouped group-multiline>
            <b-field label="Show buttons before current">
                <b-input type="number" v-model="rangeBefore" min="0"></b-input>
            </b-field>
            <b-field label="Show buttons after current">
                <b-input type="number" v-model="rangeAfter" min="0"></b-input>
            </b-field>
        </b-field>
        <b-field grouped group-multiline>
            <b-field label="Order">
                <b-select v-model="order">
                    <option value="">default</option>
                    <option value="is-centered">is-centered</option>
                    <option value="is-right">is-right</option>
                </b-select>
            </b-field>
            <b-field label="Size">
                <b-select v-model="size">
                    <option value="">default</option>
                    <option value="is-small">is-small</option>
                    <option value="is-medium">is-medium</option>
                    <option value="is-large">is-large</option>
                </b-select>
            </b-field>
        </b-field>
        <b-field grouped group-multiline>
            <b-field label="Previous icon">
                <b-select v-model="prevIcon">
                    <option value="chevron-left">Chevron</option>
                    <option value="arrow-left">Arrow</option>
                </b-select>
            </b-field>
            <b-field label="Next icon">
                <b-select v-model="nextIcon">
                    <option value="chevron-right">Chevron</option>
                    <option value="arrow-right">Arrow</option>
                </b-select>
            </b-field>
        </b-field>
        

        <hr>
        <b-pagination
            :total="total"
            v-model="current"
            :range-before="rangeBefore"
            :range-after="rangeAfter"
            :order="order"
            :size="size"
            :simple="isSimple"
            :rounded="isRounded"
            :per-page="perPage"
            :icon-prev="prevIcon"
            :icon-next="nextIcon"
            aria-next-label="Next page"
            aria-previous-label="Previous page"
            aria-page-label="Page"
            aria-current-label="Current page">
        </b-pagination>
    </section>
</template>

<script>
import Card from '~/components/Card'

export default {
  name: 'HomePage',

  components: {
    Card
  },
  data() {
    return {
    total: 20,
    current: 10,
    perPage: 10,
    rangeBefore: 3,
    rangeAfter: 1,
    order: 'is-centered',
    size: '',
    isSimple: false,
    isRounded: true,
    prevIcon: 'chevron-left',
    nextIcon: 'chevron-right'
    }
  }
}
</script>