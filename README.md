1) Task 1
Create two new files in the screens/ folder: AboutScreen.js and ContactScreen.js.
Inside these files, set up the AboutScreen and ContactScreen components as function components, and have them both return an empty ScrollView component, with both the opening and closing tags like this: <ScrollView> </ScrollView> (you will be adding content inside the ScrollView in Task 2). Include the necessary imports and set up both components as the default export. 
Next, update MainComponent. Import the AboutScreen and ContactScreen components.
You need to create a Stack Navigator for both the AboutScreen and ContactScreen components. Use the Stack Navigator for the HomeScreen (HomeNavigator) as your guide. 
For the AboutScreen Stack Navigator give the Stack.Screen a name of 'About' (the options prop here can be omitted since the title will by default be set to whatever the name prop is set to).
For the ContactScreen Stack Navigator give the Stack.Screen a name of 'Contact' and in the options give it a title of 'Contact Us'.
Then add Drawer.Screen tags inside the Drawer.Navigator opening and closing tags below the tags that are already being used for the Home and Directory screens (the order of these tags determine the order displayed in the drawer).
In the Drawer.Screen tag for the AboutNavigator set the name to 'AboutNav' and in the options give it a title of 'About Us' and set headerShown to false. Set the component to AboutNavigator.
In the Drawer.Screen tag for the ContactNavigator set the name to 'ContactNav' and in the options give it a title of 'Contact Us' and set headerShown to false. Set the component to ContactNavigator.
At the end of this task, you should be able to swipe right on your emulator to bring up the drawer navigator and see the About and Contact Us links there. When you follow them, you will be taken to a blank page, with just the screen title at the top.

https://learn.nucamp.co/pluginfile.php/3322/mod_assign/intro/WorkshopTask1.jpg![image](https://github.com/user-attachments/assets/23c65302-355b-466e-97d7-6aef5294cb74)

2) Task 2
In this task, you will update the ContactScreen component to show the address of the company HQ as shown in the instruction video as well as the screenshot below. You will only need to update the ContactScreen.js file.

Address information:

You should display the address, phone, and email as shown in the screenshot below:
                            1 Nucamp Way
                            Seattle, WA 98001
                            U.S.A.

                            Phone: 1-206-555-1234
                            Email: campsites@nucamp.co

Use a Card component from react-native-elements (RNE) to design this page. Place the Card inside the ScrollView component you created in Task 1. 
Set the wrapperStyle prop on the Card to give it an inner margin of 10, using the object format: 
wrapperStyle={{margin: 20}}
Use the Card.Title component inside the opening and closing tag of the Card to set the title to Contact Information (this component works similar to the Text tag where you can put plain text inside the opening and closing tags).
Add a Card.Divider self-closing tag after the Card.Title.
Use multiple Text components from React Native for the address, phone number, and email lines. To add space between the address and the phone number, add a style prop with the value of marginBottom: 10 to the final Text component. (The one that displays "U.S.A")

https://learn.nucamp.co/pluginfile.php/3322/mod_assign/intro/WorkshopTask2.jpg![image](https://github.com/user-attachments/assets/2a398e3f-cb5d-47ad-bddd-efe5d950192f)



3) Task 3
In this task, you will update the AboutScreen component to show the Mission and Community Partners of the company. You will only need to update the AboutScreen.js file.

You will use the Card layout similar to the ContactScreen to display the company mission statement. This should be implemented in a separate functional component named Mission.
Use the Card, Card.Title, Card.Divider, and Text components in the Mission component.
On the Card component do not apply a wrapperStyle prop and on the Text component give it a style prop with margin: 10.
The mission statement should be preceded by a title of "Our Mission". You can use the Card.Title component for this, with a Card.Divider after the title.
Text for the mission statement:
We present a curated database of the best campsites in the vast woods and backcountry of the World Wide Web Wilderness. We increase access to adventure for the public while promoting safe and respectful use of resources. The expert wilderness trekkers on our staff personally verify each campsite to make sure that they are up to our standards. We also present a platform for campers to share reviews on campsites they have visited with each other.
 
The community partnership information is obtained from the partners.js file in the shared folder by the AboutScreen component, so you will need to import it. Set up a state variable inside the function body of AboutScreen and initialize 
Go to the empty ScrollView component that you set up in Task 1 in the AboutScreen function's return statement. Inside the ScrollView, render the Mission component you set up earlier. 
After the rendering of the Mission component, render a Card component with the title "Community Partners". Again, you can use a Card.Title component for this with a Card.Divider after the title).
Then, inside the Card use the map method on the partners data passing partner as a parameter to the map method's function. (Remember when using map in JSX you must put everything inside curly brackets)
Then the map's function should return a ListItem component. Make sure to set a key prop on the ListItem using the partner.id value. (Unlike the Directory component, this ListItem will not need a onPress prop nor the navigate function as, unlike the items in the Directory screen, the items in this list will not be links.)
Use an Avatar component in the ListItem with the prop rounded and source setting the source prop to partner.image.
 
Use a ListItem.Content component below the Avatar tag nesting a ListItem.Title and ListItem.Subtitle between the opening and closing tags and using the partner.name for the ListItem.Title and the partner.description for the ListItem.Subtitle.

https://learn.nucamp.co/pluginfile.php/3322/mod_assign/intro/image%20%281%29.png![image](https://github.com/user-attachments/assets/2142ff39-5ff2-4231-8907-5235ad390f68)

