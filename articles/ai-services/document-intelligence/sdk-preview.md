---
title: Document Intelligence SDKs (preview)
titleSuffix: Azure AI services
description: The preview Document Intelligence software development kits (SDKs) expose Document Intelligence models, features and capabilities that are in active development for C#, Java, JavaScript, or Python programming language.
author: laujan
manager: nitinme
ms.service: applied-ai-services
ms.subservice: forms-recognizer
ms.custom: devx-track-python
ms.topic: conceptual
ms.date: 07/18/2023
ms.author: lajanuar
monikerRange: 'doc-intel-3.0.0'
---


<!-- markdownlint-disable MD024 -->
<!-- markdownlint-disable MD036 -->
<!-- markdownlint-disable MD001 -->
<!-- markdownlint-disable MD051 -->

# Document Intelligence SDK (public preview)

**The SDKs referenced in this article are supported by:** ![Document Intelligence checkmark](media/yes-icon.png) **Document Intelligence REST API version 2023-02-28-preview**.

> [!IMPORTANT]
>
> * Document Intelligence public preview releases provide early access to features that are in active development.
> * Features, approaches, and processes may change, prior to General Availability (GA), based on user feedback.
> * The public preview version of Document Intelligence client libraries default to service version [**Document Intelligence 2023-02-28-preview REST API**](https://westus.dev.cognitive.microsoft.com/docs/services/form-recognizer-api-2023-02-28-preview/operations/AnalyzeDocument).

Azure AI Document Intelligence is a cloud service that uses machine learning to analyze text and structured data from documents. The Document Intelligence software development kit (SDK) is a set of libraries and tools that enable you to easily integrate Document Intelligence models and capabilities into your applications. Document Intelligence SDK is available across platforms in C#/.NET, Java, JavaScript, and Python programming languages.

## Supported languages

Document Intelligence SDK supports the following languages and platforms:

| Language → Document Intelligence SDK version | Package| Supported API version| Platform support |
|:----------------------:|:----------|:----------| :----------------|
| [.NET/C# → 4.1.0-beta.1 (preview)](https://azuresdkdocs.blob.core.windows.net/$web/dotnet/Azure.AI.FormRecognizer/4.1.0-beta.1/index.html)|[NuGet](https://www.nuget.org/packages/Azure.AI.FormRecognizer/4.1.0-beta.1)|[**2023-02-28-preview**](https://westus.dev.cognitive.microsoft.com/docs/services/form-recognizer-api-2023-02-28-preview/operations/AnalyzeDocument)</br> [**2022-08-31 (GA)**](https://westus.dev.cognitive.microsoft.com/docs/services/form-recognizer-api-2022-08-31/operations/AnalyzeDocument)</br> [**v2.1**](https://westus.dev.cognitive.microsoft.com/docs/services/form-recognizer-api-v2-1/operations/AnalyzeBusinessCardAsync)</br>[**v2.0**](https://westus.dev.cognitive.microsoft.com/docs/services/form-recognizer-api-v2/operations/AnalyzeLayoutAsync) |[Windows, macOS, Linux, Docker](https://dotnet.microsoft.com/download)|
|[Java →  4.1.0-beta.1 (preview)](https://azuresdkdocs.blob.core.windows.net/$web/java/azure-ai-formrecognizer/4.1.0-beta.1/index.html) |[MVN repository](https://mvnrepository.com/artifact/com.azure/azure-ai-formrecognizer/4.1.0-beta.1) |[**2023-02-28-preview**](https://westus.dev.cognitive.microsoft.com/docs/services/form-recognizer-api-2023-02-28-preview/operations/AnalyzeDocument)</br> [**2022-08-31 (GA)**](https://westus.dev.cognitive.microsoft.com/docs/services/form-recognizer-api-2022-08-31/operations/AnalyzeDocument)</br> [**v2.1**](https://westus.dev.cognitive.microsoft.com/docs/services/form-recognizer-api-v2-1/operations/AnalyzeBusinessCardAsync)</br>[**v2.0**](https://westus.dev.cognitive.microsoft.com/docs/services/form-recognizer-api-v2/operations/AnalyzeLayoutAsync) |[Windows, macOS, Linux](/java/openjdk/install)|
|[JavaScript → 4.1.0-beta.1 (preview)](https://azuresdkdocs.blob.core.windows.net/$web/javascript/azure-ai-form-recognizer/4.1.0-beta.1/index.html)| [npm](https://www.npmjs.com/package/@azure/ai-form-recognizer/v/4.1.0-beta.1)| [**2023-02-28-preview**](https://westus.dev.cognitive.microsoft.com/docs/services/form-recognizer-api-2023-02-28-preview/operations/AnalyzeDocument)</br> [**2022-08-31 (GA)**](https://westus.dev.cognitive.microsoft.com/docs/services/form-recognizer-api-2022-08-31/operations/AnalyzeDocument)</br> [**v2.1**](https://westus.dev.cognitive.microsoft.com/docs/services/form-recognizer-api-v2-1/operations/AnalyzeBusinessCardAsync)</br>[**v2.0**](https://westus.dev.cognitive.microsoft.com/docs/services/form-recognizer-api-v2/operations/AnalyzeLayoutAsync) | [Browser, Windows, macOS, Linux](https://nodejs.org/en/download/) |
|[Python → 3.3.0b1 (preview)](https://azuresdkdocs.blob.core.windows.net/$web/python/azure-ai-formrecognizer/3.3.0b1/index.html) | [PyPI](https://pypi.org/project/azure-ai-formrecognizer/3.3.0b1/)| [**2023-02-28-preview**](https://westus.dev.cognitive.microsoft.com/docs/services/form-recognizer-api-2023-02-28-preview/operations/AnalyzeDocument)</br> [**2022-08-31 (GA)**](https://westus.dev.cognitive.microsoft.com/docs/services/form-recognizer-api-2022-08-31/operations/AnalyzeDocument)</br> [**v2.1**](https://westus.dev.cognitive.microsoft.com/docs/services/form-recognizer-api-v2-1/operations/AnalyzeBusinessCardAsync)</br>[**v2.0**](https://westus.dev.cognitive.microsoft.com/docs/services/form-recognizer-api-v2/operations/AnalyzeLayoutAsync) |[Windows, macOS, Linux](/azure/developer/python/configure-local-development-environment?tabs=windows%2Capt%2Ccmd#use-the-azure-cli)

## Supported Clients

| Language| SDK version | API version (default) | Supported clients|
| :------ | :-----------|:---------- | :-----------------|
|**.NET/C#**</br> **Java**</br> **JavaScript**</br>| 4.1.0-beta-1 (preview)| 2023_02_28_preview|**DocumentAnalysisClient**</br>**DocumentModelAdministrationClient** |
|**.NET/C#**</br> **Java**</br> **JavaScript**</br>| 4.0.0 (GA)| v3.0 / 2022-08-31|  **DocumentAnalysisClient**</br>**DocumentModelAdministrationClient** |
|**.NET/C#**</br> **Java**</br> **JavaScript**</br>| 3.1.x |  v2.1 |  **FormRecognizerClient**</br>**FormTrainingClient** |
|**.NET/C#**</br> **Java**</br> **JavaScript**</br>| 3.0.x| v2.0 |  **FormRecognizerClient**</br>**FormTrainingClient** |
| **Python**| 3.3.0bx (preview) | 2023-02-28-preview |  **DocumentAnalysisClient**</br>**DocumentModelAdministrationClient**|
| **Python**| 3.2.x (GA) | v3.0 / 2022-08-31|  **DocumentAnalysisClient**</br>**DocumentModelAdministrationClient**|
| **Python**| 3.1.x |  v2.1  |  **FormRecognizerClient**</br>**FormTrainingClient** |
| **Python** | 3.0.0 |  v2.0 |**FormRecognizerClient**</br>**FormTrainingClient** |

## Use Document Intelligence SDK in your applications

The Document Intelligence SDK enables the use and management of the Document Intelligence service in your application. The SDK builds on the underlying Document Intelligence REST API allowing you to easily use those APIs within your programming language paradigm. Here's how you use the Document Intelligence SDK for your preferred language:

### 1. Install the SDK client library

### [C#/.NET](#tab/csharp)

```dotnetcli
dotnet add package Azure.AI.FormRecognizer --version 4.1.0-beta.1
```

```powershell
Install-Package Azure.AI.FormRecognizer -Version 4.1.0-beta.1
```

### [Java](#tab/java)

```xml
  <dependency>
  <groupId>com.azure</groupId>
  <artifactId>azure-ai-formrecognizer</artifactId>
  <version>4.1.0-beta.1</version>
  </dependency>
```

```kotlin
implementation("com.azure:azure-ai-formrecognizer:4.1.0-beta.1")
```

### [JavaScript](#tab/javascript)

```javascript
npm i @azure/ai-form-recognizer@4.1.0-beta.1
```

### [Python](#tab/python)

```python
pip install azure-ai-formrecognizer==3.3.0b1
```

---


### 2. Import the SDK client library into your application

### [C#/.NET](#tab/csharp)

```csharp
using Azure;
using Azure.AI.FormRecognizer.DocumentAnalysis;
```

### [Java](#tab/java)

```java
import com.azure.ai.formrecognizer.*;
import com.azure.ai.formrecognizer.models.*;
import com.azure.ai.formrecognizer.DocumentAnalysisClient.*;

import com.azure.core.credential.AzureKeyCredential;
```

### [JavaScript](#tab/javascript)

```javascript
const { AzureKeyCredential, DocumentAnalysisClient } = require("@azure/ai-form-recognizer");
```

### [Python](#tab/python)

```python
from azure.ai.formrecognizer import DocumentAnalysisClient
from azure.core.credentials import AzureKeyCredential
```

---


### 3. Set up authentication

There are two supported methods for authentication

* Use a [Document Intelligence API key](#use-your-api-key) with AzureKeyCredential from azure.core.credentials.

* Use a [token credential from azure-identity](#use-an-azure-active-directory-azure-ad-token-credential) to authenticate with [Azure Active Directory](../../active-directory/fundamentals/active-directory-whatis.md).

#### Use your API key

Here's where to find your Document Intelligence API key in the Azure portal:

:::image type="content" source="media/containers/keys-and-endpoint.png" alt-text="Screenshot of the keys and endpoint location in the Azure portal.":::

### [C#/.NET](#tab/csharp)

```csharp

//set `<your-endpoint>` and `<your-key>` variables with the values from the Azure portal to create your `AzureKeyCredential` and `DocumentAnalysisClient` instance
string key = "<your-key>";
string endpoint = "<your-endpoint>";
AzureKeyCredential credential = new AzureKeyCredential(key);
DocumentAnalysisClient client = new DocumentAnalysisClient(new Uri(endpoint), credential);
```

### [Java](#tab/java)

```java

// create your `DocumentAnalysisClient` instance and `AzureKeyCredential` variable
DocumentAnalysisClient client = new DocumentAnalysisClientBuilder()
            .credential(new AzureKeyCredential("<your-key>"))
            .endpoint("<your-endpoint>")
            .buildClient();
```

### [JavaScript](#tab/javascript)

```javascript

// create your `DocumentAnalysisClient` instance and `AzureKeyCredential` variable
async function main() {
    const client = new DocumentAnalysisClient("<your-endpoint>", new AzureKeyCredential("<your-key>"));
```

### [Python](#tab/python)

```python

# create your `DocumentAnalysisClient` instance and `AzureKeyCredential` variable
    document_analysis_client = DocumentAnalysisClient(endpoint="<your-endpoint>", credential=AzureKeyCredential("<your-key>"))
```

---


#### Use an Azure Active Directory (Azure AD) token credential

> [!NOTE]
> Regional endpoints do not support AAD authentication. Create a [custom subdomain](../../ai-services/authentication.md?tabs=powershell#create-a-resource-with-a-custom-subdomain) for your resource in order to use this type of authentication.

Authorization is easiest using the `DefaultAzureCredential`. It provides a default token credential, based upon the running environment, capable of handling most Azure authentication scenarios.

### [C#/.NET](#tab/csharp)

Here's how to acquire and use the [DefaultAzureCredential](/dotnet/api/azure.identity.defaultazurecredential?view=azure-dotnet&preserve-view=true) for .NET applications:

1. Install the [Azure Identity library for .NET](/dotnet/api/overview/azure/identity-readme):

    ```console
        dotnet add package Azure.Identity
    ```

    ```powershell
        Install-Package Azure.Identity
    ```

1. [Register an Azure AD application and create a new service principal](../../ai-services/authentication.md?tabs=powershell#assign-a-role-to-a-service-principal).

1. Grant access to Document Intelligence by assigning the **`Cognitive Services User`** role to your service principal.

1. Set the values of the client ID, tenant ID, and client secret in the Azure AD application as environment variables: **`AZURE_CLIENT_ID`**, **`AZURE_TENANT_ID`**, and **`AZURE_CLIENT_SECRET`**, respectively.

1. Create your **`DocumentAnalysisClient`** instance including the **`DefaultAzureCredential`**:

    ```csharp
    string endpoint = "<your-endpoint>";
    var client = new DocumentAnalysisClient(new Uri(endpoint), new DefaultAzureCredential());
    ```

For more information, *see* [Authenticate the client](https://github.com/Azure/azure-sdk-for-net/tree/Azure.AI.FormRecognizer_4.0.0-beta.4/sdk/formrecognizer/Azure.AI.FormRecognizer#authenticate-the-client)

### [Java](#tab/java)

Here's how to acquire and use the [DefaultAzureCredential](/java/api/com.azure.identity.defaultazurecredential?view=azure-java-stable&preserve-view=true) for Java applications:

1. Install the [Azure Identity library for Java](/java/api/overview/azure/identity-readme?view=azure-java-stable&preserve-view=true):

    ```xml
    <dependency>
        <groupId>com.azure</groupId>
        <artifactId>azure-identity</artifactId>
        <version>1.5.3</version>
    </dependency>
    ```

1. [Register an Azure AD application and create a new service principal](../../ai-services/authentication.md?tabs=powershell#assign-a-role-to-a-service-principal).

1. Grant access to Document Intelligence by assigning the **`Cognitive Services User`** role to your service principal.

1. Set the values of the client ID, tenant ID, and client secret of the Azure AD application as environment variables: **`AZURE_CLIENT_ID`**, **`AZURE_TENANT_ID`**, and **`AZURE_CLIENT_SECRET`**, respectively.

1. Create your **`DocumentAnalysisClient`** instance and **`TokenCredential`** variable:

    ```java
    TokenCredential credential = new DefaultAzureCredentialBuilder().build();
    DocumentAnalysisClient documentAnalysisClient = new DocumentAnalysisClientBuilder()
        .endpoint("{your-endpoint}")
        .credential(credential)
        .buildClient();
    ```

For more information, *see* [Authenticate the client](https://github.com/Azure/azure-sdk-for-java/tree/main/sdk/formrecognizer/azure-ai-formrecognizer#authenticate-the-client)

### [JavaScript](#tab/javascript)

Here's how to acquire and use the [DefaultAzureCredential](/javascript/api/@azure/identity/defaultazurecredential?view=azure-node-latest&preserve-view=true) for JavaScript applications:

1. Install the [Azure Identity library for JavaScript](/javascript/api/overview/azure/identity-readme?view=azure-node-latest&preserve-view=true):

    ```javascript
    npm install @azure/identity
    ```

1. [Register an Azure AD application and create a new service principal](../../ai-services/authentication.md?tabs=powershell#assign-a-role-to-a-service-principal).

1. Grant access to Document Intelligence by assigning the **`Cognitive Services User`** role to your service principal.

1. Set the values of the client ID, tenant ID, and client secret of the Azure AD application as environment variables: **`AZURE_CLIENT_ID`**, **`AZURE_TENANT_ID`**, and **`AZURE_CLIENT_SECRET`**, respectively.

1. Create your **`DocumentAnalysisClient`** instance including the **`DefaultAzureCredential`**:

    ```javascript
    const { DocumentAnalysisClient } = require("@azure/ai-form-recognizer");
    const { DefaultAzureCredential } = require("@azure/identity");

    const client = new DocumentAnalysisClient("<your-endpoint>", new DefaultAzureCredential());
    ```

For more information, *see* [Create and authenticate a client](https://github.com/Azure/azure-sdk-for-js/tree/main/sdk/formrecognizer/ai-form-recognizer#create-and-authenticate-a-client).

### [Python](#tab/python)

Here's how to acquire and use the [DefaultAzureCredential](/python/api/azure-identity/azure.identity.defaultazurecredential?view=azure-python&preserve-view=true) for Python applications.

1. Install the [Azure Identity library for Python](/python/api/overview/azure/identity-readme?view=azure-python&preserve-view=true):

    ```python
    pip install azure-identity
    ```

1. [Register an Azure AD application and create a new service principal](../../ai-services/authentication.md?tabs=powershell#assign-a-role-to-a-service-principal).

1. Grant access to Document Intelligence by assigning the **`Cognitive Services User`** role to your service principal.

1. Set the values of the client ID, tenant ID, and client secret of the Azure AD application as environment variables: **`AZURE_CLIENT_ID`**, **`AZURE_TENANT_ID`**, and **`AZURE_CLIENT_SECRET`**, respectively.

1. Create your **`DocumentAnalysisClient`** instance including the **`DefaultAzureCredential`**:

    ```python
    from azure.identity import DefaultAzureCredential
    from azure.ai.formrecognizer import DocumentAnalysisClient

    credential = DefaultAzureCredential()
    document_analysis_client = DocumentAnalysisClient(
        endpoint="https://<my-custom-subdomain>.cognitiveservices.azure.com/",
        credential=credential
    )
    ```

For more information, *see* [Authenticate the client](https://github.com/Azure/azure-sdk-for-python/tree/azure-ai-formrecognizer_3.2.0b5/sdk/formrecognizer/azure-ai-formrecognizer#authenticate-the-client)

---


### 4. Build your application

Create a client object to interact with the Document Intelligence SDK, and then call methods on that client object to interact with the service. The SDKs provide both synchronous and asynchronous methods. For more insight, try a [quickstart](quickstarts/get-started-sdks-rest-api.md?view=doc-intel-3.0.0&preserve-view=true) in a language of your choice.

## Help options

The [Microsoft Q&A](/answers/topics/azure-form-recognizer.html) and [Stack Overflow](https://stackoverflow.com/questions/tagged/azure-form-recognizer) forums are available for the developer community to ask and answer questions about Azure AI Document Intelligence and other services. Microsoft monitors the forums and replies to questions that the community has yet to answer. To make sure that we see your question, tag it with **`azure-form-recognizer`**.

## Next steps

> [!div class="nextstepaction"]
> [**Explore Document Intelligence REST API 2023-02-28-preview**](https://westus.dev.cognitive.microsoft.com/docs/services/form-recognizer-api-2023-02-28-preview/operations/AnalyzeDocument)
