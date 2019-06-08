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

		<v-container fluid class="google-font">
			<v-layout wrap align-center justify-center row fill-height>
			<v-flex xs12 md10 class="">
			We have sent out tickets for all those who have been selected as invitees. Please note that 
			only the people who have valid tickets will be allowed to enter. Anyone without a ticket will not be 
			able to pass the front door security of Dialog and we will also not allow anyone without a valid ticket to remain in the event.

			<h3 style="color: red">Exchanging the ticket with your friends is not possible due to the ID check</h3>

			</v-flex>
			<v-flex xs12 md10 class="">
			Please note that you are expected to <b>NOT</b> bring any laptops or similar electronics because of security requirements of Dialog. We are sorry about the inconvinience this might cause. However, smartphone are allowed and you are welcome to use them for taking down notes or other requirements.
			
			</v-flex>
		</v-layout>
		</v-container>


		<v-container fluid class="">
		<v-layout wrap align-center justify-center row fill-height>
			<v-flex xs12 md10 class="">
			<p class="google-font mb-0" style="font-size:200%;color:#0277bd">Slide Resources</p>
			</v-flex>
			<v-flex xs12 md10 class="google-font">
				<h3>What is SRE?</h3>
				<h4>by <a href="https://twitter.com/tdevinda">@tdevinda</a> and <a
						href="https://twitter.com/agentmilindu"> @agentmilindu</a></h4>
				<p>The following resources were used in making the slides.</p>
				<ul>
					<li><a href="https://google.com/sre">Google SRE Homepage</a> and the SRE Handbook</li>
					<li><a href="https://cloud.google.com/blog/products/gcp/sre-vs-devops-competing-standards-or-close-friends">SRE vs DevOps</a> </li>
					<li><p>SRE vs DevOps youtube channel</p>
						<br/>
						<iframe width="560" height="315" src="https://www.youtube.com/embed/uTEL8Ff1Zvk"
								frameborder="0"
								allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen>

					</iframe></li>
				</ul>
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