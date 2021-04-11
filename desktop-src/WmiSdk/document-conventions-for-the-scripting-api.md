---
description: Descreve as convenções de documento para a leitura de tópicos da API de script do WMI.
ms.assetid: 889e6322-96f6-4a24-a084-e3b7bfa94a40
ms.tgt_platform: multiple
title: Convenções de documento para a API de script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 33335982672472fa9924a6e250305a3630628b21
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104296997"
---
# <a name="document-conventions-for-the-scripting-api"></a>Convenções de documento para a API de script

A [API de script para referência de WMI](scripting-api-for-wmi.md) usa as seguintes convenções de documento:

-   Os tipos de parâmetro são definidos usando um prefixo: b (booliano), Str (String), I (Integer), obj (Automation Object), var (Variant).
-   Os parâmetros opcionais são colocados entre colchetes com seus valores padrão mostrados pela atribuição.
-   No caso de parâmetros de objeto, os caracteres após o prefixo "obj" indicam o tipo de objeto esperado.



| Parâmetro de objeto      | Tipo de objeto                                          |
|-----------------------|------------------------------------------------------|
| *WbemDatetime*        | [**SWbemDateTime**](swbemdatetime.md)               |
| *WbemEventSource*     | [**SWbemEventSource**](swbemeventsource.md)         |
| *WbemLocator*         | [**SWbemLocator**](swbemlocator.md)                 |
| *WbemMethod*          | [**SWbemMethod**](swbemmethod.md)                   |
| *WbemMethodSet*       | [**SWbemMethodSet**](swbemmethodset.md)             |
| *WbemNamedValueSet*   | [**SWbemNamedValueSet**](swbemnamedvalueset.md)     |
| *WbemObject*          | [**SWbemObject**](swbemobject.md)                   |
| *WbemObjectEx*        | [**SWbemObjectEx**](swbemobjectex.md)               |
| *WbemObjectPath*      | [**SWbemObjectPath**](swbemobjectpath.md)           |
| *WbemObjectSet*       | [**SWbemObjectSet**](swbemobjectset.md)             |
| *WbemPrivilege*       | [**SWbemPrivilege**](swbemprivilege.md)             |
| *WbemPrivilegeSet*    | [**SWbemPrivilegeSet**](swbemprivilegeset.md)       |
| *WbemProperty*        | [**SWbemProperty**](swbemproperty.md)               |
| *WbemPropertySet*     | [**SWbemPropertySet**](swbempropertyset.md)         |
| *WbemQualifier*       | [**SWbemQualifier**](swbemqualifier.md)             |
| *WbemQualifierSet*    | [**SWbemQualifierSet**](swbemqualifierset.md)       |
| *WbemRefreshableItem* | [**SWbemRefreshableItem**](swbemrefreshableitem.md) |
| *WbemRefresher*       | [**SWbemRefresher**](swbemrefresher.md)             |
| *WbemServices*        | [**SWbemServices**](swbemservices.md)               |
| *WbemServicesEx*      | [**SWbemServicesEx**](swbemservicesex.md)           |



 

Por exemplo, o código a seguir mostra como nomear variáveis para diferentes tipos de objetos:


```VB
strComputerName  ' a string value for a computer name
bStatusFlag  ' a boolean value used for a status
objServices  ' an object value used to store an SWbemServices value
```



 

 



