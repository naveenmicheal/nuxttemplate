<template>
	<div>
		<div data-aos="slide-up" data-aos-duration="1000">
			<v-container class="pa-3" >
				<h1 class="text--h3 text-center">Media</h1>
				<v-row wrap>	
					<v-col  cols="6" md="3">
						<v-img   @click="openimage('/print/9.jpeg')" src="/print/9.jpeg" aspect-ratio="1"></v-img>
					</v-col>
					<v-col  cols="6" md="3">
						<v-img @click="openimage('/print/11.jpeg')" src="/print/11.jpeg" aspect-ratio="1"></v-img>
					</v-col>
					<v-col  cols="6" md="3">
						<v-img @click="openimage('/print/12.jpeg')" src="/print/12.jpeg" aspect-ratio="1"></v-img>
					</v-col>
					<v-col  cols="6" md="3">
						<v-img @click="openimage('/print/13.jpeg')"src="/print/13.jpeg" aspect-ratio="1"></v-img>
					</v-col>
					<v-col  cols="6" md="3">
						<v-img  @click="openimage('/print/14.jpeg')"  src="/print/14.jpeg" aspect-ratio="1"></v-img>
					</v-col>
					<v-col  cols="6" md="3">
						<v-img  @click="openimage('/print/15.jpeg')" src="/print/15.jpeg" aspect-ratio="1"></v-img>
					</v-col>
					<v-col  cols="6" md="3">
						<v-img  @click="openimage('/print/16.jpeg')" src="/print/16.jpeg" aspect-ratio="1"></v-img>
					</v-col>
					<v-col  cols="6" md="3">
						<v-img @click="openimage('/print/17.jpeg')"  src="/print/17.jpeg" aspect-ratio="1"></v-img>
					</v-col>
					<v-col  cols="6" md="3">
						<v-img  @click="openimage('/print/18.jpeg')" src="/print/18.jpeg" aspect-ratio="1"></v-img>
					</v-col>
					<v-col  cols="6" md="3">
						<v-img  @click="openimage('/print/19.jpeg')" src="/print/19.jpeg" aspect-ratio="1"></v-img>
					</v-col>
					<v-col  cols="6" md="3">
						<v-img  @click="openimage('/print/20.jpeg')" src="/print/20.jpeg" aspect-ratio="1"></v-img>
					</v-col>
					<v-col  cols="6" md="3">
						<v-img  @click="openimage('/print/21.jpeg')" src="/print/21.jpeg" aspect-ratio="1"></v-img>
					</v-col>
					<v-col  cols="6" md="3">
						<v-img  @click="openimage('/print/22.jpeg')" src="/print/22.jpeg" aspect-ratio="1"></v-img>
					</v-col>
					<v-col  cols="6" md="3">
						<v-img  @click="openimage('/print/23.jpeg')" src="/print/23.jpeg" aspect-ratio="1"></v-img>
					</v-col>

				</v-row>
			</v-container>
		</div>

		<v-dialog v-model="dialog" max-width="800">
			<v-card class="pa-1" >
				<v-img contain aspect-ratio="1.5"  v-if="imageurl" :src="imageurl"></v-img>
				<v-card-actions>
					<v-spacer></v-spacer>
					<v-btn color="black darken-1" text @click="closeimage()">
						Close
					</v-btn>
				</v-card-actions>
			</v-card>
		</v-dialog>

	</div>
</template>

<script type="text/javascript">
	export default{
		layout:"page",
		data(){
			return{
				dialog : false,
				imageurl: null
			}
		},
		methods:{
			openimage(e){
				this.imageurl = e
				this.dialog = !this.dialog
			},
			closeimage(){
				this.imageurl = null
				this.dialog = !this.dialog
			}
		},
		mounted(){
			let audio = document.getElementsByTagName('audio')
			audio[0].play()
		}
	}
</script>
