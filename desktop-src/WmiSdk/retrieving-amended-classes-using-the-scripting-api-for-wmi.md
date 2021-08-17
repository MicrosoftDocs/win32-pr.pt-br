---
description: Se você estiver usando a API de script para que o WMI recupere ou armazene informações de classe localizadas, especifique a localidade como parte de um moniker.
ms.assetid: 3c64047d-ce3a-4180-8f71-0e66c2e61627
ms.tgt_platform: multiple
title: Recuperando classes corrigidas usando a API de script para WMI
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 47d01af2515b26ca308a1b258aa40508f227a0c1d0eaa5b2b332c1e7b3200420
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130878"
---
# <a name="retrieving-amended-classes-using-the-scripting-api-for-wmi"></a>Recuperando classes corrigidas usando a API de script para WMI

Se você estiver usando a API de script para que o WMI recupere ou armazene informações de classe localizadas, especifique a localidade como parte de um moniker. Ou, você pode fornecer o nome da localidade no parâmetro *strLocale* para o método [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md) . Ao ler ou gravar classes corrigidas, indique que você deseja usar definições de classe localizadas especificando [wbemFlagUseAmendedQualifiers](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum) como um sinalizador para o parâmetro *iFlags* do método que você chama. Para o PowerShell, você pode usar o parâmetro *-locale* em [Get-WmiObject](/powershell/module/microsoft.powershell.management/get-wmiobject?view=powershell-5.1&preserve-view=true) para especificar a localidade.

O exemplo de código a seguir mostra como recuperar uma classe localizada usando um moniker scripting do WMI ou o parâmetro-locale.


```VB
Set objwbemobject = GetObject("winmgmts:[locale=ms_409]!root/test:myclass")
```


```PowerShell

Get-WmiObject myclass -Namespace &quot;root\test&quot; -Locale &quot;ms_409&quot;
```





O exemplo de código a seguir mostra como definir o parâmetro locale e usar o sinalizador [wbemFlagUseAmendedQualifiers](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum) .


```VB
Set Locator = CreateObject("WbemScripting.SWbemLocator")
Set service = Locator.ConnectServer(,"root\test", , , "ms_409")
Set objwbemobject = service.Get("myclass", wbemFlagUseAmendedQualifiers)
```



> [!Note]  
> Como o retorno de chamada para o coletor pode não ser retornado no mesmo nível de autenticação que o cliente requer, é recomendável que você use semisynchronous em vez de comunicação assíncrona. Para obter mais informações, consulte [chamando um método](calling-a-method.md).

 

A tabela a seguir lista os métodos que aceitam o sinalizador [wbemFlagUseAmendedQualifiers](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum) .



| Método síncrono                                                 | Método assíncrono                                                          |
|--------------------------------------------------------------------|------------------------------------------------------------------------------|
| [**SWbemServices. SubclassesOf**](swbemservices-subclassesof.md)   | [**SWbemServices. SubclassesOfAsync**](swbemservices-subclassesofasync.md)   |
| [**Subclasses de SWbemObject\_**](swbemobject-subclasses-.md)        | [**SWbemObject. SubclassesAsync\_**](swbemobject-subclassesasync-.md)        |
| [**SWbemServices. InstancesOf**](swbemservices-instancesof.md)     | [**SWbemServices. InstancesOfAsync**](swbemservices-instancesofasync.md)     |
| [**SWbemObject. instâncias\_**](swbemobject-instances-.md)          | [**SWbemObject. InstancesAsync\_**](swbemobject-instancesasync-.md)          |
| [**SWbemServices.ExecQuery**](swbemservices-execquery.md)         | [**SWbemServices.ExecQueryAsync**](swbemservices-execqueryasync.md)         |
| [**SWbemServices. Get**](swbemservices-get.md)                     | [**SWbemServices. getasync**](swbemservices-getasync.md)                     |
| [**SWbemObject. put\_**](swbemobject-put-.md)                      | [**SWbemObject. PutAsync\_**](swbemobject-putasync-.md)                      |
| [**SWbemServices. References**](swbemservices-referencesto.md)   | [**SWbemServices. ReferencesToAsync**](swbemservices-referencestoasync.md)   |
| [**SWbemObject. referências\_**](swbemobject-references-.md)        | [**SWbemObject. ReferencesAsync\_**](swbemobject-referencesasync-.md)        |
| [**SWbemServices. AssociatorsOf**](swbemservices-associatorsof.md) | [**SWbemServices. AssociatorsOfAsync**](swbemservices-associatorsofasync.md) |
| [**SWbemObject. ASSOCIATORS\_**](swbemobject-associators-.md)      | [**SWbemObject. AssociatorsAsync\_**](swbemobject-associatorsasync-.md)      |



 

 

 
