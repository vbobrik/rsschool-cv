# Valentina Bobrik
#### QA Automation Engineer
#### Minsk, Belarus. Phone +375295969503 
## Summary
QA Automation Engineer with skills in E2E testing, API testing and experience in manual and automated testing, testing against NoSQL data storages.
Good knowledge of QA processes.
------
## Skills
*	Automation/manual testing;
*	Jira, Redmine, Confluence;
*	Kibana, Redash (logs);
*	MongoDB (SQL – basic knowledge);
*	Jenkins;
*	JavaScript;
*	DevTools (Network, Console, Elements, Application);
*	HTML, CSS (basic);
*	APITesting (Postman, Swagger);
*	Microsoft Azure;
*	Putty (Linux);
*	Windows, MacOs;
*	GIT;
*	TestNG, Rest Assured;
*	Java (basic knowledge);
*	Selenium WebDriver;
*	Cucumber;
*	Protractor, Jasmine;
*	Puppeteer, Chai;
*	Axios
*	Xray plugin for execution and storing tests;
*	NodeJS;
*	Async JS.
------
## Code examples:
1. ```
   public String updateClient(Client client) {
        return given()
                .header("km-auth", getToken())
                .header("Content-Type", "application/json")
                .body(client)
                .when()
                .post(baseUrl + "/client/" + client.get_id())
                .getBody().asString();
    }
   ```
2. ```
   public static String getToken() {
           Response token = given().contentType("application/json")
                   .baseUri(BASE_URI + BASE_PATH)
                   .basePath("/session")
                   .get();
   
           if (token.jsonPath().getInt("status") == 200) {
               return token.jsonPath().getString("message.sessionToken");
           } else {
               JsonObject credentials = new JsonObject();
               credentials.addProperty("password", password);
               credentials.addProperty("username", userName);
   
               Response response = given()
                       .contentType("application/json")
                       .body(credentials)
                       .put(BASE_URI + BASE_PATH + "/session");
               return response.jsonPath().getString("message.sessionToken");
           }
       }

   ```
3. ```
   describe('Test case №1, verification of onliner page:', function () {
        it('go to catalog on the onliner and verify title', async function () {
          expect(await basePage.goToCatalog()).toMatch('Каталог Onliner', 'The title is not "Каталог Onliner"');
        })
      
        it('go to "Mobile phones" tab', async function () {
          await basePage.goToMobilePhones();
          expect(await basePage.getPageTitle()).toContain('Мобильный телефон', 'The title doesn\'t contain "Мобильный телефон"');
          expect(await basePage.getPageHeader()).toMatch('Мобильные телефоны', 'The header is not "Мобильные телефоны"');
        })
      
        it('sort elements by "HONOR" producer', async function () {
          const sortedPhones = await basePage.sortByProducer();
          for await (let phone of sortedPhones) {
            expect(phone).toContain("HONOR", 'Found pages does not match goal of search "HONOR"');
          }
        })
      
        it('sort elements by price descending', async function () {
          const elements = await basePage.sortByPriceDown();
          elements.forEach((item, index) => {
            if (index == elements.length - 1) return;
            expect(item >= elements[index + 1]).toBeTruthy();
            expect(elements[index]).toBeGreaterThanOrEqual(elements[index + 1], 'sort by price is absent');
          })
        })
   })
   ```
------
## Experience
### Web Trader Application
__Responsibilities__:  
*	Write and update test scripts (JavaScript);
*	Maintenance test framework;
*	Make test automation reports;
*	Run builds using Teamcity;
*	UI, E2E testing (Cucumber, Protractor, Jasmine, Selenium). 
### API automation test
__Responsibilities__:  
*	Development of test scripts (KOTLIN, testNG, REST Assured);
*	Run builds using Jenkins, view reports using Allure.
### 3D-modelweb app
__Responsibilities__: 
*	GUI and functional testing;
*	Work with OBJ, MTL, GLTF, PNG, JPG, SVG files;
*	Checking of bundles after 3D models export;
*	View queues in RabbitMQ, emulate message sending;
*	Checking Business Requirements;
*	Work with Unity services;
*	Integration testing;
*	Software testing fundamentals.
### Platform
__Responsibilities__: 
*	Regression using test cases;
*	API Testing (postman);
*	Checking/modifying data in MongoDB;
*	Firmware and registration of devices;
*	Work with Linux (putty);
*	Google Analytics;
*	Tracking errors using logs (kibana, redash).
### CRM-system
__Responsibilities__: 
*	Work on ScrumMethodology;
*	Testing (AT, MAT, smoke) based on requirements;
*	Functional testing;
*	Testing of user interface;
*	Writing documentation (checklists, test cases).
------
## Education
* BSPU (higher education)
* Software testing courses
* Automation testing courses
------
## English
Intermediate level
