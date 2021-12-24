# react-inerview-important-questions
## Controlled and Uncontrolled Components
### 1. Controlled Components
####   In one sentence, Form data is handled by React componenets (state).
![controlled_exampple](https://user-images.githubusercontent.com/31300915/147195673-a6de7816-c519-4e64-ace1-cecf484d43f8.PNG)

### 2. Uncontrolled Component
####   In one sentence, Form data is handled by DOM itself.
![uncontrolled_example](https://user-images.githubusercontent.com/31300915/147196147-324ccf77-e72b-4391-9b9e-d4187a7664fd.PNG)

## What is Pure Componenet in react ?
### PURE COMPONENT in React does not re-rendered, if states or props is updated with SAME VALUES.
#### In other word, If previous states or props values and current states or props value are same then PURE COMPONENT is not re-rendered.
#### PURE COMPONENT is used for increasing the performance of component.
##### Features of PURE COMPONENT:---
###### . Prevents re-rendering of Component if props or state is the same
###### . Takes care of “shouldComponentUpdate” implicitly
###### . State and Props are Shallow Compared
###### . Pure Components are more performant in certain cases
### Without PURE Component:---
#### Continuasly 0 is updating in highlighted area in inspect console...
![without_pureCompo](https://user-images.githubusercontent.com/31300915/147215865-2d0ed852-cdbe-4cdd-b6ac-8db665c638fe.PNG)
![without_pureCompoCode](https://user-images.githubusercontent.com/31300915/147216142-1fdb9557-f386-4ba8-b16f-2c7c2a623000.PNG)
### With PURE Component:---
#### Here 0 is not updating...
![with_pureComp](https://user-images.githubusercontent.com/31300915/147216586-5d67dede-d115-42c4-b960-044afc4e794f.PNG)
![with_pureCompcode](https://user-images.githubusercontent.com/31300915/147216713-3ad1c84c-8552-439b-87e8-fe16a230bb35.PNG)
### PURE component is implemented in functional using MEMO
![pureCompUsingFunt](https://user-images.githubusercontent.com/31300915/147217847-17290bc7-9425-498d-bd89-54279c52c5c6.PNG)
### What is Shallow Comparison ?
#### Shallow Comparison is used for compare the previous value of states or props with current value of states or props. If the variable is primitive like "var a = 10" then the comaprision is not dificult but It is big concern in the case of objectives and arrays. 
   
![Capture1](https://user-images.githubusercontent.com/31300915/147223128-592e6935-f6eb-4c3c-96f1-86cbf8b64132.PNG)
#### In above example the result will be false because javascript looks the reference of objects (Starting Address of the Object).
![Capture2](https://user-images.githubusercontent.com/31300915/147223448-39079198-5f28-4135-992f-3b3067dce09c.PNG)
#### In above example the value will be true because now we are assiging the same reference of an object to other.
#### We can use spread oparator for assigning the value like below:--
![Capture3](https://user-images.githubusercontent.com/31300915/147224342-46422378-1287-4828-807f-4807f53ebb99.PNG)
#### This spread oparator is useful in the case of array. If we assign or update the value of an array like below then the pure componenet will not be updated because refernce of array object are same.
![Capture5](https://user-images.githubusercontent.com/31300915/147224706-419446e5-6ab8-40a7-a547-85b68acb2de8.PNG)
#### So here we need to change the reference and this will happen using spread oparator like below:---
![Capture4](https://user-images.githubusercontent.com/31300915/147224911-828dc4ef-38f1-45f4-8cb9-ba2410f72796.PNG)
## What is RECONCILIATION ?
### RECONCILIATION is the process where virtual DOM is created in-memory of real DOM and is compaired with real DOM for any changes in DOM node. If any changes is found then the perticular node is updated in real DOM and render it for display to user.
