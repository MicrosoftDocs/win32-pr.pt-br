---
description: O objeto de script SWbemObject é o objeto WMI genérico, definindo propriedades e métodos que podem ser usados independentemente do objeto WMI específico ao qual o objeto SWbemObject está associado.
ms.assetid: 33252b49-00d4-4c43-8abe-9368ed82f34b
ms.tgt_platform: multiple
title: Criando scripts com SWbemObject
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3ce9a48779b13f1b1917ad189b2297b60329ba04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091300"
---
# <a name="scripting-with-swbemobject"></a>Criando scripts com SWbemObject

O objeto de script [**SWbemObject**](swbemobject.md) é o objeto WMI genérico, definindo propriedades e métodos que podem ser usados independentemente do objeto WMI específico ao qual o objeto **SWbemObject** está associado. Todos os objetos WMI, como uma instância do [**\_ processo Win32**](/windows/desktop/CIMWin32Prov/win32-process) ou qualquer outra classe de dados WMI, são representados por [**SWbemObject**](swbemobject.md) e podem usar os métodos e propriedades comuns de **SWbemObject** , além de suas próprias propriedades e métodos específicos.

Por exemplo, use o script a seguir para obter todas as instâncias de um [**\_ processo Win32**](/windows/desktop/CIMWin32Prov/win32-process) chamando o método [**SWbemObject. Instances \_**](swbemobject-instances-.md) . O clsobjProcess representa a definição de classe de **\_ processo do Win32** e um [**SWbemObject**](swbemobject.md).


```VB
strComputer = "."
Set objWMIServices = GetObject("winmgmts:\\" & strComputer & "\root\CIMV2") 
Set clsobjProcess = objWMIServices.Get("Win32_Process")
Set colProcesses = clsobjProcess.Instances_()
For Each Process in colProcesses
    WScript.Echo Process.Name
Next
```



O exemplo a seguir obtém uma instância específica do [**\_ serviço Win32**](/windows/desktop/CIMWin32Prov/win32-service) que representa o serviço de alerta e o armazena em objAlerter. Em seguida, você pode chamar os métodos [**SWbemObject**](swbemobject.md) , como WScript. Echo ObjAlerter. Path \_ , ou métodos definidos pela classe de dados, como WScript. Echo objAlerter. State. objAlerter que representa uma instância do serviço Win32 \_ e um **SWbemObject**.


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



A chamada para [**SWbemObject. Instances \_**](swbemobject-instances-.md) Obtém outro objeto de script WMI genérico, [**SWbemObjectSet**](swbemobjectset.md). Como mostrado, o objeto **SWbemObjectSet** pode ser tratado como uma [coleção](accessing-a-collection.md).


```VB
Set clsobjProcess = objWMIServices.Get("Win32_Process")
```



Você pode identificar os métodos [**SWbemObject**](swbemobject.md) porque todos eles terminam com um sublinhado ( \_ ), por exemplo, [**SWbemObject \_ . Instances**](swbemobject-instances-.md).

[**SWbemObjectEx**](swbemobjectex.md) estende as propriedades de [**SWbemObject**](swbemobject.md). Por exemplo, agora você pode atualizar os dados de qualquer objeto WMI, como uma instância do [**\_ processo do Win32**](/windows/desktop/CIMWin32Prov/win32-process), por uma chamada para [**SWbemObjectEx. Refresh \_**](swbemobjectex-refresh-.md).

O exemplo a seguir mostra como os dados de falha de página do processo do sistema podem ser atualizados a cada cinco segundos.


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



Para obter mais informações sobre como atualizar dados usando um objeto [**SWbemRefresher**](swbemrefresher.md) , consulte [atualizando dados do WMI em scripts](refreshing-wmi-data-in-scripts.md).

O [**SWbemObject. put \_**](swbemobject-put-.md) e [**o \_ PutAsync**](swbemobject-putasync-.md) permitem que você grave alterações de volta em qualquer objeto WMI. Esses métodos só confirmam alterações em um objeto no namespace em que o objeto foi criado. Você pode gravar o objeto em um namespace diferente usando [**SWbemServicesEx. put**](swbemservicesex-put.md) ou [**SWbemServicesEx. PutAsync**](swbemservicesex-putasync.md).

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

 

 
