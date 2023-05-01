Download Link: https://assignmentchef.com/product/solved-atis-assignment-2
<br>
<strong>Modeling with UML</strong>

Imagine you work in the software department of a manufacturer of a fancy coffee machine. The coffee machine consists of the following internal parts:

<ul>

 <li>user interface,</li>

 <li>embedded controller,</li>

 <li>water tank with a level indicator,</li>

 <li>beans container,</li>

 <li>water pump,</li>

 <li>heating unit,</li>

 <li>bean grinder,</li>

 <li>beverage dispenser,</li>

 <li>brewing unit.</li>

</ul>




We expect that the user fills in water into the water tank and adds beans to the beans container. The machine is intended for free usage in office spaces: no payment options are needed. Model all following tasks with the <strong>Modelio</strong> tool.

<strong> </strong>

<strong>Task 1: Describe the various parts of the coffee machine in a <em><u>component diagram</u></em> assigning the different parts into four different subsystems. Connect all components with appropriate connectors and ports. </strong>

<strong> </strong>













<h1>Architectural Thinking for Intelligent Systems</h1>




The company wants to develop a new user interface for the coffee machine consisting of a hardware button and a touch screen. The button allows the user to switch the coffee machine on or off. The touchscreen contains several buttons called control elements. When a control element on the touch screen or the on/off-button are pressed, the embedded controller processes the user input. If the embedded controller produces a notification to display, the touchscreen needs to display this notification.

The following control elements are offered on the touch screen:

<ul>

 <li>Screen controls allow the user to specify the various settings of the controller:

  <ol>

   <li>size of coffee cup: small, medium, large</li>

   <li>coffee roasting: mild, strong</li>

   <li>type of coffee: espresso, cappuccino, black coffee</li>

  </ol></li>

 <li>“Quick-choice” buttons allow a user to directly select a specific, frequently ordered type of coffee with a single touch: large strong black coffee, mild medium cappuccino, and small strong espresso.</li>

</ul>




<strong>Task 2: Design a <em><u>class diagram</u></em> for the user interface.  Model the order options for the user. Add methods that allow a software developer to implement the interaction with the controller. Use inheritance, aggregation, and composition where appropriate and add multiplicities, role names, visibilities, and association names to your associations. </strong>

The machine behavior always follows the same pattern:

<ul>

 <li>The machine can only work if the user has switched it on via the button.</li>

 <li>When the machine starts, the main menu is displayed.</li>

 <li>From this menu the user can select a coffee by setting the screen controls or order a coffee directly via the quick choice buttons. So long as the coffee is not ordered yet, the menu will be displayed.</li>

 <li>When a coffee is ordered by the user, the machine must be sufficiently filled with water and must contain enough beans to perform the order. Both checks are performed in parallel.</li>

</ul>










<h1>Architectural Thinking for Intelligent Systems</h1>




<ul>

 <li>Otherwise, the brewing unit ensures that coffee is brewed.</li>

 <li>The brewed coffee is dispensed by the beverage dispenser and a new coffee can be ordered/ selected.</li>

 <li>If the machine cannot select/ order/ brew/ dispense a coffee or the water or bean check fails, the machine displays an error on the screen. When a user touches the screen, the machine turns off.</li>

</ul>







<strong>Task 3: Describe this behavior using a <em><u>state diagram</u></em>. Use concurrent substates, and transitions with trigger events and guards where appropriate. </strong>

<strong> </strong>

<strong>Task 4: Model the interaction of the coffee machine components using a <em><u>sequence diagram</u></em> in the following situation: The user orders a coffee, and the machine reports an error due to an</strong> <strong>insufficient amount of water, which is displayed on the screen. Assume that the machine is running. </strong>