# JSF - Life Cycle

JSF application lifecycle consist of six phases which are as follows

    1. Restore view phase
    2. Apply request values phase; process events
    3. Process validations phase; process events
    4. Update model values phase; process events
    5. Invoke application phase; process events
    6. Render response phase
	
![The six phases](http://www.tutorialspoint.com/jsf/images/jsf_life_cycle.jpg "The six phases")

## Phase 1: Restore view
JSF begins the restore view phase as soon as a link or a button is clicked and JSF receives a request.
During this phase, the JSF builds the view, wires event handlers and validators to UI components and saves the view in the FacesContext instance. The FacesContext instance will now contains all the information required to process a request.

## Phase 2: Apply request values
After the component tree is created/restored, each component in component tree uses decode method to extract its new value from the request parameters. Component stores this value. If the conversion fails, an error message is generated and queued on FacesContext. This message will be displayed during the render response phase, along with any validation errors.
If any decode methods / event listeners called renderResponse on the current FacesContext instance, the JSF moves to the render response phase.

## Phase 3: Process validation
During this phase, the JSF processes all validators registered on component tree. It examines the component attribute rules for the validation and compares these rules to the local value stored for the component.
If the local value is invalid, the JSF adds an error message to the FacesContext instance, and the life cycle advances to the render response phase and display the same page again with the error message.

## Phase 4: Update model values
After the JSF checks that the data is valid, it walks over the component tree and set the corresponding server-side object properties to the components' local values. The JSF will update the bean properties corresponding to input component's value attribute.
If any updateModels methods called renderResponse on the current FacesContext instance, the JSF moves to the render response phase.

## Phase 5: Invoke application
During this phase, the JSF handles any application-level events, such as submitting a form / linking to another page.

## Phase 6: Render response
During this phase, the JSF asks container/application server to render the page if the application is using JSP pages. For initial request, the components represented on the page will be added to the component tree as the JSP container executes the page. If this is not an initial request, the component tree is already built so components need not to be added again. In either case, the components will render themselves as the JSP container/Application server traverses the tags in the page.

After the content of the view is rendered, the response state is saved so that subsequent requests can access it and it is available to the restore view phase.