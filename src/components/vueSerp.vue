<template>
    <div class="vue-google-serp">
        <div class="preview">
            <h3>{{title | truncate(title_length)}}</h3>
            <cite>{{url}}</cite>
            <p>{{description | truncate(description_length)}}</p>
        </div>
    </div>
</template>

<script>
export default {
	name: "vueSerp",
	props: {
        title: { required: true, type: String },
        url: { required: true, type: String },
        description: { required: true, type: String },
        title_length: {type: Number, default:  60 }, //standard google serp title length
        description_length: {type: Number, default:  160 } //standard google serp description length
        
	},
	filters: {
		truncate(string, length) {
			return string.length > length ? string.slice(0, length) + '...' : string;
		}
	}
}
</script>

<style lang="scss">
.vue-google-serp {
	font-family: arial, sans-serif !important;
	margin: 0;
	padding: 0;
    .preview {
	padding: 20px;
	max-width: 600px;
	border: 1px solid #ddd;
	border-radius: 5px;
    }
    h3 {
    margin: 0;
    color: rgb(26, 13, 171);
    font-size: 18px;
    font-weight: 400;
    line-height: 1.2;
    }
    p {
    margin: 0;
    color: rgb(84, 84, 84);
    font-size: 13px;
    line-height: 1.4;
    }
    cite {
    margin: 0;
    font-style: normal;
    height: 18px;
    color: rgb(0, 102, 33);
    font-size: 14px;
    line-height: 16px;
    white-space: nowrap;
    overflow: hidden;
    text-overflow: ellipsis;
    }
}

</style>