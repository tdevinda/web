<template>
	<v-content class="pa-0">
		<v-container fluid class="">
		<v-layout wrap align-center justify-center row fill-height>
		<v-flex xs12 md10 class="">
			<p class="google-font mb-0" style="font-size:200%;color:#0277bd">Google Cloud Next Extended 2019 Sri Lanka</p>

			<v-img
                :src="require('@/assets/img/featureEvent/cn19.jpg')"
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
				<p class="google-font mb-0">
				The extended event for the Cloud Next 2019 recently concluded in San Francisco, will be hapenning in Colombo on the 8th. Google Cloud Developer Community Sri Lanka will be hosting this event to spread awareness on new technologies launched in the main event.</p>	
				<p class="google-font mb-0">
				Please refer to the agenda of this event.
				</p>
			</v-flex>
			</v-layout>
		</v-container>

		<v-container fluid class="">
			<v-layout wrap align-center justify-center row fill-height>
			<v-flex xs12 md10 class="">
				<table>
					<thead>
					<tr>
						<th style="align: center;" v-for="title in prettyTitles">
						{{ title }}
						</th>
					</tr>
					</thead>
					<tbody>
						<tr v-for="item in schedule">
							<td style='padding-right: 1em;' v-for="key in titles">
								{{ item[key] }}
							</td>
						</tr>
					</tbody>
					
				</table>
			</v-flex>
			</v-layout>
		</v-container>

		<v-container fluid class="">
			<v-layout wrap align-center justify-center row fill-height>
			<v-flex xs12 md10 class="">
			Await more information. 
			</v-flex>
		</v-layout>
		</v-container>
	</v-content>
</template>
<script>
	import cloudNextSchedule from '@/assets/data/cn19schedule.json'
	export default {
		data() {
			return {
				titles: ['from', 'to', 'title', 'speaker'],
				prettyTitles: ['From', 'To', 'Session title', 'Speaker'],
				schedule: cloudNextSchedule
			}
		}
	}
</script>