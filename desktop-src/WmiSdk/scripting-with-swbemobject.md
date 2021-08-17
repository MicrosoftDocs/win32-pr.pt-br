---
description: O objeto de script SWbemObject é o objeto WMI genérico, definindo propriedades e métodos que podem ser usados independentemente do objeto WMI específico ao qual o objeto SWbemObject está vinculado.
ms.assetid: 33252b49-00d4-4c43-8abe-9368ed82f34b
ms.tgt_platform: multiple
title: Script com SWbemObject
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d6ba0cccca8fcd62af490aa91ab1cc965fdad4d3682d99a8fda52151135500ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117739692"
---
# <a name="scripting-with-swbemobject"></a>Script com SWbemObject

O objeto de script [**SWbemObject**](swbemobject.md) é o objeto WMI genérico, definindo propriedades e métodos que podem ser usados independentemente do objeto WMI específico ao qual o objeto **SWbemObject** está vinculado. Todos os objetos WMI, como uma instância do [**Processo Win32 \_**](/windows/desktop/CIMWin32Prov/win32-process) ou qualquer outra classe de dados WMI, são representados por [**SWbemObject**](swbemobject.md) e podem usar as propriedades e métodos comuns **SWbemObject,** além de suas próprias propriedades e métodos específicos.

Por exemplo, use o script a seguir para obter todas as instâncias de um [**Processo \_ Win32**](/windows/desktop/CIMWin32Prov/win32-process) chamando o [**método SWbemObject.Instances. \_**](swbemobject-instances-.md) O clsobjProcess representa a definição da classe **\_ Win32 Process** e um [**SWbemObject.**](swbemobject.md)


```VB
strComputer = "."
Set objWMIServices = GetObject("winmgmts:\\" & strComputer & "\root\CIMV2") 
Set clsobjProcess = objWMIServices.Get("Win32_Process")
Set colProcesses = clsobjProcess.Instances_()
For Each Process in colProcesses
    WScript.Echo Process.Name
Next
```



O exemplo a seguir obtém uma instância específica do [**Serviço Win32 \_**](/windows/desktop/CIMWin32Prov/win32-service) que representa o serviço do Alerter e o armazena em objAlerter. Em seguida, você pode chamar métodos [**SWbemObject,**](swbemobject.md) como WScript.Echo objAlerter.Path ou métodos definidos pela classe de dados, como \_ WScript.Echo objAlerter.State. objAlerter que representa uma instância do Serviço Win32 \_ e um **SWbemObject.**


```VB
strComputer = "." 
Set objWMIServices = GetObject("winmgmts:\\" & strComputer & "\root\CIMV2") 
Set objAlerter = objWMIServices.Get("Win32_Service.Name='Alerter'")
WScript.Echo objAlerter.Path_
objAlerter.StopService()
WScript.Echo objAlerter.State
```




```VB
For each Prop in myObject.Properties_
    Wscript.Echo Prop.Name
Next
```



A chamada para [**SWbemObject.Instances \_**](swbemobject-instances-.md) obtém outro objeto de script WMI genérico, [**SWbemObjectSet**](swbemobjectset.md). Conforme mostrado, o **objeto SWbemObjectSet** pode ser tratado como uma [coleção](accessing-a-collection.md).


```VB
Set clsobjProcess = objWMIServices.Get("Win32_Process")
```



Você pode identificar os [**métodos SWbemObject**](swbemobject.md) porque todos terminam com um sublinhado ( ), por \_ exemplo, [**SWbemObject.Instances \_**](swbemobject-instances-.md).

[**SWbemObjectEx**](swbemobjectex.md) estende as propriedades de [**SWbemObject**](swbemobject.md). Por exemplo, agora você pode atualizar os dados de qualquer objeto WMI, como uma instância do [**Processo \_ Win32,**](/windows/desktop/CIMWin32Prov/win32-process)por uma chamada para [**SWbemObjectEx.Refresh \_**](swbemobjectex-refresh-.md).

O exemplo a seguir mostra como os dados de falha da página de processo do sistema podem ser atualizados a cada cinco segundos.


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\root\CIMV2")
Set colProcesses = objWMIService.ExecQuery("SELECT * FROM Win32_Process WHERE Name = 'System'",,48) 
For Each Process in colProcesses
        i = 0
        Do Until i = 5
            i = i + 1
            Wscript.Echo "PageFaults = " & Process.PageFaults 
            Wscript.Sleep 10000
            Process.Refresh_
        Loop
Next
```



Para obter mais informações sobre como atualizar dados usando um [**objeto SWbemRefresher,**](swbemrefresher.md) consulte Atualizar dados [WMI em scripts](refreshing-wmi-data-in-scripts.md).

O [**SWbemObject.Put \_**](swbemobject-put-.md) e o [**PutAsync \_**](swbemobject-putasync-.md) permitem que você escreva alterações novamente em qualquer objeto WMI. Esses métodos só confirmam alterações em um objeto no namespace em que o objeto foi criado. Você pode gravar o objeto em um namespace diferente [**usando SWbemServicesEx.Put**](swbemservicesex-put.md) ou [**SWbemServicesEx.PutAsync**](swbemservicesex-putasync.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[API de script para WMI](scripting-api-for-wmi.md)
</dt> <dt>

[Criando um script WMI](creating-a-wmi-script.md)
</dt> <dt>

[Atualizando uma instância inteira](updating-an-entire-instance.md)
</dt> <dt>

[Chamando um método](calling-a-method.md)
</dt> </dl>

 

 
