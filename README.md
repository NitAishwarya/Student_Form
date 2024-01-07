# STUDENT ENROLLMENT FORM

Student Enrollment Form is a web application designed to simplify the process of enrolling students in an educational institution. This app provides an intuitive interface for capturing essential student information during the enrollment process.



# BENEFITS OF USING JSONPOWERDB

- User-friendly Form: Easily fill out the enrollment form with required details.
- Validation: Real-time validation to ensure accurate and complete information.
- Submit Form: Submit the form data to the server for processing.




# How to Use 

1. Open the web app in your preferred web browser. eg: chrome, web, etc
1. Fill out the enrollment form with the following information:
   - Student Roll-No.
   - Full Name
   - Class
   - Date of Birth
   - Address
   - Enrollment Date
1. Click on "Save" button on save data in JPDB.
1. Click on "reset" button to clear the form.
1. Click on "change" button to update data in database.





# Technologies Used 

+ **Client:** HTML,CSS, bootstrap, Javascript
+ **Server:** JsonPowerDB
+ **IDE :** NetBeans


#### Create a PUT Request String

```
var baseUrl = "http://api.login2explore.com:5577";
function executeCommand(reqString, apiEndPointUrl) {
    var url = baseUrl + apiEndPointUrl;
    var jsonObj;
    
    $.post(url, reqString, function (result) {
        jsonObj = JSON.parse(result);
    }).fail(function (result) {
        var dataJsonObj = result.responseText;
        jsonObj = JSON.parse(dataJsonObj);
    });
    return jsonObj;
}
```




```
function createPUTRequest(connToken, jsonObj, dbName, relName) {
    var putRequest = "{\n"
            + "\"token\" : \""
            + connToken
            + "\","
            + "\"dbName\": \""
            + dbName
            + "\",\n" + "\"cmd\" : \"PUT\",\n"
            + "\"rel\" : \""
            + relName + "\","
            + "\"jsonStr\": \n"
            + jsonObj
            + "\n"
            + "}";
    return putRequest;
}

```


# SCREENSHOT OF FORM 

![PC1](https://i.ibb.co/Y2MG5c9/sc1.png)

# SCREENSHOT OF JPDB

![PC2](https://i.ibb.co/tzLXkdc/sc2.png)

