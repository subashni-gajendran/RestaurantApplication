
1.How long did you spend on the coding test? What would you add to your solution if you had more time? If you didn't spend much time on the coding test then use this as an opportunity to explain what you would add.

I spent 2 days to complete the Restaurant Application. I took less time to complete the coding test. Because, I choosen the AngularCLI. 


2.What was the most useful feature that was added to the latest version of your chosen language? Please include a snippet of code that shows how you've used it.

Some of the useful feauture added in the Application such as 

Routing - loaded the view without refreshing the page.
import { RouterModule, Routes } from '@angular/router';

const routes: Routes = [
  {
    path: '',
    redirectTo: '/home',
    pathMatch: 'full'
  },
   {
    path: 'restaurants',
    component: RestaurantsComponent,
    },
    {
        path: 'home',
        component: HomeComponent,
    },
    {
      path: '**',
      component: PageNotFoundComponent,
  },
];

Sorting, Paging and filter - Implemented using the below code.

import { Ng2OrderModule } from 'ng2-order-pipe'; 
import { Ng2SearchPipeModule } from 'ng2-search-filter'; 
import {NgxPaginationModule} from 'ngx-pagination';


Http Observable - It return the muttiple event and fetch the data from API.

constructor(private http: HttpClient) { }

  getRestaurant(url:string):Observable<RestaurantDetails[]>{
    this._url = url;
    return this.http.get<RestaurantDetails[]>(this._url).catch(this.errorHandler);
  }

3.How would you track down a performance issue in production? Have you ever had to do this?

	I did not face any performance issue in production.

4.How would you improve the API that you just used?

	I dont want to improve much. Because it is providing better result and responding quickly each and evey request according to the parameter passing in the request header. 

5.Please describe yourself using JSON.

{
	"FirstName": "Subashni",
	"LastName": "Gajendran",
	"Address": "Unit 312 100 Parkway Forest Drive",
    "Postcode": "M2J 1L6",
    "City": "Tronto",
    "Province":"ON",
    "Passions": [{
			"Programming": "AngularJS & PHP",
			"Cooking" :"Indian & Chinese Cusine"
			 }],
	"Interests":[{
			"DIY": "Jewelery making & Birthday Decoration Ideas",
			"Education": "Teaching Others",
			"Languages": "Learn and speak Languages"
			}],
"Dreams": [
		"To make something no one did it before , and live in peace with silence"
	],
"Believes": [
		" That there is god who made us , in best functions , and everything is possible just need works and sweat "
	]
}


