<template>
    <v-content class="pa-0">

	<v-container fluid class="">
		<v-layout wrap align-center justify-center row fill-height>
		<v-flex xs12 md10 class="">
			<v-img
                :src="require('@/assets/img/featureEvent/rewind19.png')"
                :lazy-src="require('@/assets/img/gdglk_lazy.png')"
                width="100%">
                <v-layout
                    slot="placeholder"
                    fill-height
                    align-center
                    justify-center
                    ma-0
                >
                    <v-progress-circular indeterminate color="grey lighten-5"></v-progress-circular>
                </v-layout>
            </v-img>

		</v-flex>
		</v-layout>
		</v-container>

		<v-container fluid class="">
			<v-layout wrap align-center justify-center row fill-height>
			<v-flex xs12 md10 class="">
				<p class="google-font mb-0" style="font-size:200%;color:#0277bd">Google I/O Rewind 2019 Ruhuna</p>
				<p class="google-font mb-0">
				Google I/O is the company's developer conference. It concluded in May 2019 at San Francisco. GDG's around the world send their participants to bring back the technologies which were unveiled at the conference, to local communitie as post-I/O events</p>

				<p class="google-font mb-0">
				I/O Rewind is the post I/O event name for GDG Sri Lanka. 
				</p>
			</v-flex>
			</v-layout>
		</v-container>

		<v-container fluid class="">
			<v-layout wrap align-center justify-center row fill-height>
			<v-flex xs12 md10 class="">
				<p class="google-font mb-0" style="font-size:200%;color:#0277bd">Schedule</p>
				<table width="100%">
					<thead>
						<tr>
							<th style="align: center;">Track A</th>
							<th style="align: center;">Track B</th>
						</tr>
					</thead>
					<tbody>
						<tr v-for="item in schedule.outline">
							<td v-if="item.common != null" colspan="2" class="session-container-common" v-bind:style="{'background-color': schedule.common[item.common].background}">
								<div style="margin-bottom: 4%;font-size: 80%">{{schedule.common[item.common].from}} - {{schedule.common[item.common].to}}</div>
								<h4>{{schedule.common[item.common].topic}}</h4>
								<div style="margin-left: 6%;margin-bottom: 10%">
									<h5>{{schedule.common[item.common].speaker.name}}</h5>
									<h6>{{schedule.common[item.common].speaker.post}}</h6>
								</div>
							</td>
							<td v-if="item.trackA != null" :rowspan="schedule.trackA[item.trackA].span" class="session-container-track" v-bind:style="{'background-color': schedule.trackA[item.trackA].background}">
								<div class="session-element-time">{{schedule.trackA[item.trackA].from}} - {{schedule.trackA[item.trackA].to}}</div>
								<h4 class="session-element-title">{{schedule.trackA[item.trackA].topic}}</h4>
								<div class="session-element-speakerdetails">
									<h5>{{schedule.trackA[item.trackA].speaker.name}}</h5>
									<h6>{{schedule.trackA[item.trackA].speaker.post}}</h6>
								</div>
							</td>
							<td v-if="item.trackB != null" :rowspan="schedule.trackB[item.trackB].span" class="session-container-track" v-bind:style="{'background-color': schedule.trackB[item.trackB].background}">
								<div class="session-element-time">{{schedule.trackB[item.trackB].from}} - {{schedule.trackB[item.trackB].to}}</div>
								<h4 class="session-element-title">{{schedule.trackB[item.trackB].topic}}</h4>
								<div class="session-element-speakerdetails">
									<h5>{{schedule.trackB[item.trackB].speaker.name}}</h5>
									<h6>{{schedule.trackB[item.trackB].speaker.post}}</h6>
								</div>
							</td>
							
						</tr>

					</tbody>

				</table>


			</v-flex>
			</v-layout>
		</v-container>


    </v-content>
</template>

<script>
	import io19Schedule from '@/assets/data/io19schedule.json'
    export default {
        data() {
			return {
				schedule: io19Schedule
			}
		}
    }
</script>

<style scoped>
	.session-container-common {
		padding-right: 1em; 
		text-align: center;
	}

	.session-container-track {
		padding-right: 1em; 
		paddng-left: 1em;
	}

	.session-element-time {
		margin-bottom: 4%;
		font-size: 80%;
	}

	.session-element-title {
		margin-left: 20%;
	}

	.session-element-speakerdetails {
		margin-left: 6%;
		margin-bottom: 10%;
	}
</style>
