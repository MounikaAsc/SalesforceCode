# SalesforceCode
<apex:page StandardController="Dashboard__c" Extensions="CreateSignupController" setup="false" sidebar="false" showHeader="true" tabStyle="Opportunity">
<apex:sectionHeader title="Please fill in this form to sign up" subtitle="New User"/>
<apex:form >
    <apex:pageMessages id="id1"></apex:pageMessages>
    <apex:pageBlock >
        <apex:pageBlockSection columns="1" >
            <apex:inputText label="First Name: " html-placeholder="First Name" value="{!fName}"/>
            <apex:inputText label="Last Name: " html-placeholder="Last Name" value="{!lName}"/>
            <apex:inputText label="Username: " html-placeholder="Username" value="{!uName}"/>
            <apex:inputsecret label="Password: " html-placeholder="Password" value="{!password}" redisplay="true"/>
            <apex:inputsecret label="Confirm Password: " html-placeholder="Confirm Password" value="{!cPassword}" redisplay="true"/>
            <apex:commandButton value="Sign Up" action="{!SignUp}" reRender="id1"/>
        </apex:pageBlockSection>    
    <apex:pageBlocksection >
                        <apex:commandlink value="Go to Sign In" action="{!GoToSignIn}"/>
    </apex:pageBlocksection>
    
        </apex:pageBlock>

</apex:form>
</apex:page>
