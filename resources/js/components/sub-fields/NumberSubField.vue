<template>
    <div>
        <input
            :id="subField.name + '-' + index"
            :name="subField.name"
            type="number"
            class="w-full form-control form-input form-input-bordered"
            :value="value"
            v-bind="subField.attributes"
            :placeholder="subField.placeholder"
            @input="$emit('input', $event.target.value)"
        />
    </div>

</template>

<script>

    export default {

        props: [
            'subField',
            'value',
            'index'
        ]

    }
</script>
