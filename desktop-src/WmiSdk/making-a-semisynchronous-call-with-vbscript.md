---
description: Fornece a funcionalidade de acesso do semisynchronous e um exemplo de código para fazer uma chamada de método semisynchronous.
ms.assetid: 3eae38e8-6a63-45c0-99b0-94e25ddbc5a8
ms.tgt_platform: multiple
title: Fazendo uma chamada Semisynchronous com o VBScript
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e875a269d2cf1cd4e3b40d5c84d42ffb97dc35a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105790478"
---
# <a name="making-a-semisynchronous-call-with-vbscript"></a>Fazendo uma chamada Semisynchronous com o VBScript

Alguns métodos WMI podem retornar grandes coleções, fazendo com que os scripts parem de responder. No script, o acesso semisynchronous é o padrão, e instrumentação de gerenciamento do Windows (WMI) define **wbemFlagReturnImmediately** para chamadas que podem retornar grandes coleções de objetos, como os seguintes métodos [**SWbemServices**](swbemservices.md) : [**InstancesOf**](swbemservices-instancesof.md), [**SubclassesOf**](swbemservices-subclassesof.md), [**ExecQuery**](swbemservices-execquery.md), [**AssociatorsOf**](swbemservices-associatorsof.md)e [**References**](swbemservices-referencesto.md).

O acesso Semisynchronous que usa **wbemFlagReturnImmediately** definido no parâmetro *iFlags* também é o padrão para chamadas que podem retornar grandes conjuntos de objetos para os seguintes métodos [**SWbemObject**](swbemobject.md) : [**instâncias \_**](swbemobject-instances-.md), [**subclasses \_**](swbemobject-subclasses-.md), [**ASSOCIADORES \_**](swbemobject-associators-.md)e [**referências \_**](swbemobject-references-.md).

Para reduzir o uso de recursos de memória WMI ao processar uma grande coleção de objetos, inclua o valor de **wbemFlagForwardOnly** no parâmetro *iFlags* . O uso de **wbemFlagForwardOnly** faz com que o WMI crie um enumerador somente de encaminhamento que não permite rebobinar a coleção e acessar itens novamente.

O WMI elimina a memória de cada objeto, uma vez que a instrução **for each** processa um objeto. Você não pode chamar o método **Count** para uma coleção quando o sinalizador **wbemFlagForwardOnly** foi definido na chamada que obteve a coleção. Observe que o parâmetro *iFlags* tem **wbemFlagReturnImmediately** e **wbemFlagForwardOnly** definidos por padrão para o método [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) .

O procedimento a seguir descreve como usar o VBScript para fazer uma chamada semisynchronous.

**Para fazer uma chamada semisynchronous no VBScript**

1.  Defina o parâmetro *iFlags* para o valor de [wbemFlagReturnImmediately](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum).
2.  Faça a chamada síncrona normal para [**SWbemServices.ExecQuery**](swbemservices-execquery.md) ou [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) com o valor *iFlags* .
3.  Se você quiser tratar os objetos retornados pela chamada como uma coleção, use uma sintaxe de enumeração como VBScript **para cada** um. À medida que cada objeto é retornado, ele é processado como o próximo item da coleção.
4.  Crie um enumerador somente encaminhamento combinando o valor de **wbemFlagReturnImmediately** com o valor de **wbemFlagForwardOnly**. O valor decimal dessa operação ou é 48. Essas constantes são definidas na biblioteca de tipos wbemdisp. tlb para Visual Basic. A maioria das linguagens de script usa o valor numérico ou define uma constante. Para obter mais informações, consulte [WbemFlagEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum).

O exemplo de código a seguir mostra como fazer uma chamada de método semisynchronous. Para obter mais informações, consulte [chamando um método](calling-a-method.md).


```VB
wbemFlagReturnImmediately = 16
wbemFlagForwardOnly = 32
IFlags = wbemFlagReturnImmediately + wbemFlagForwardOnly
WScript.Echo IFlags
Set objWMIService = GetObject("winmgmts:root\cimv2")
' Query for all the Win32_Process objects on the 
'     local computer and use forward-only enumerator
Set colProcesses = objWMIService.ExecQuery("SELECT Name FROM Win32_Process",,IFlags)
' Receive each object as it arrives
For Each objProcess in colProcesses
    WScript.Echo objProcess.Name
Next
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Chamando um método](calling-a-method.md)
</dt> </dl>

 

 



