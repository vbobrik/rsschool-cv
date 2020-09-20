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
1. `console.log('Any example')`
2. `console.log('Any example2')`
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

