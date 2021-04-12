---
description: Em scripts de monitoramento, você pode evitar chamadas sucessivas para GetObject usando um objeto SWbemRefresher. O objeto SWbemRefresher é um contêiner que pode conter vários objetos WMI cujos dados podem ser atualizados em uma chamada.
ms.assetid: b34567f5-9349-4580-97d5-723759805d88
ms.tgt_platform: multiple
title: Atualizando dados do WMI em scripts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae0f17ce718fcf5b57e4f3204337634af4129d24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170382"
---
# <a name="refreshing-wmi-data-in-scripts"></a>Atualizando dados do WMI em scripts

Em scripts de monitoramento, você pode evitar chamadas sucessivas para **GetObject** usando um objeto [**SWbemRefresher**](swbemrefresher.md) . O objeto **SWbemRefresher** é um contêiner que pode conter vários objetos WMI cujos dados podem ser atualizados em uma chamada.

O uso de um objeto [**SWbemRefresher**](swbemrefresher.md) é necessário para obter dados precisos de classes de desempenho do WMI, como [**Win32 \_ PerfFormattedData \_ perfdisk \_ LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md) ou outras classes pré-instalados derivadas do [**Win32 \_ perf**](/windows/desktop/CIMWin32Prov/win32-perf).

O procedimento a seguir descreve como atualizar dados em scripts.

**Para atualizar dados em scripts**

1.  Chame **CreateObject** para criar um objeto de atualizador [**SWbemRefresher**](swbemrefresher.md) .

    ```VB
    Set objRefresher = CreateObject("WbemScripting.SWbemRefresher")
    ```

    

2.  Conecte-se ao namespace do WMI. Para usar as classes de [**desempenho \_ do Win32**](/windows/desktop/CIMWin32Prov/win32-perf) pré-instalado, conecte-se à **\\ cimv2 raiz**.

    ```VB
    Set objServicesCimv2 = GetObject("winmgmts:\\" _
        & strComputer & "\root\cimv2")
    ```

    

3.  Adicione um único objeto (chame [**SWbemRefresher. Add**](swbemrefresher-add.md)) ou uma coleção (chame [**SWbemRefresher. AddEnum**](swbemrefresher-addenum.md)) ao atualizador.

    Use as classes de dados precalculadas derivadas do [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata), por exemplo, o [**PerfFormattedData de \_ \_ perfdisk \_**](./retrieving-raw-and-formatted-performance-data.md) do Win32, em vez do [**Win32 \_ PerfRawData \_ perfdisk \_**](./retrieving-raw-and-formatted-performance-data.md). Caso contrário, você deve calcular os valores para todas as propriedades que não sejam contadores simples.

    ```VB
    Set objRefreshableItem = _
        objRefresher.AddEnum(objServicesCimv2 , _
        "Win32_PerfFormattedData_PerfProc_Process")
    ```

    

4.  Atualize os dados uma vez para obter os dados de desempenho iniciais.

    Chame o método [**SWbemRefresher. Refresh**](swbemrefresher-refresh.md) ou o método [**SWbemObjectEx. Refresh \_**](swbemobjectex-refresh-.md) genérico.

    ```VB
    objRefresher.Refresh
    ```

    

5.  Se você estiver monitorando o desempenho e tiver uma coleção no objeto do atualizador, faça um loop pelos objetos da coleção.

    ```VB
    For Each Process in objRefreshableItem.ObjectSet
        If Process.PercentProcessorTime > 1 then
            WScript.Echo Process.Name & vbnewLine _
                & Process.PercentProcessorTime & "%"
        End If
    Next
    ```

    

6.  Limpe os itens do atualizador chamando [**SWbemRefresher. DeleteAll**](swbemrefresher-deleteall.md) ou remova itens específicos chamando [**SWbemRefresher. Remove**](swbemrefresher-remove.md).

O exemplo de código VBScript a seguir mostra como atualizar um único objeto no computador local. O script cria um contêiner de atualização e adiciona uma instância de um enumerador para instâncias de [**processo do Win32 \_ PerfFormattedData \_ PerfProc \_**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) . A chamada de [**atualização**](swbemrefresher-refresh.md) é feita três vezes para demonstrar as alterações na propriedade **PercentProcessorTime** para processos usando mais de uma porcentagem do tempo do processador.


```VB
On Error Resume Next
strComputer = "."
Set objRefresher = CreateObject("WbemScripting.SWbemRefresher")
Set objServicesCimv2 = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
If Err = 0 Then 
Set objRefreshableItem = _
    objRefresher.AddEnum(objServicesCimv2 ,"Win32_PerfFormattedData_PerfProc_Process")
objRefresher.Refresh
' Loop through the processes three times to locate  
'    and display all the process currently using 
'    more than 1 % of the process time. Refresh on each pass.
For i = 1 to 3
    Wscript.Echo "Refresh number " & i 
    objRefresher.Refresh 
    For Each Process in objRefreshableItem.ObjectSet
        If Process.PercentProcessorTime > 1 then
            WScript.Echo Process.Name & vbnewLine & Process.PercentProcessorTime & "%"
        End If
    Next
Next
Else
    WScript.Echo Err.Description
End If
```



A propriedade [**index**](swbemrefreshableitem-index.md) do [**SWbemRefreshableItem**](swbemrefreshableitem.md) retornado representa o índice do objeto na coleção de atualizadores. Você pode chamar a propriedade [**SWbemRefreshableItem. IsSet**](swbemrefreshableitem-isset.md) para determinar se um item em um atualizador é um único item ou uma coleção. Para acessar um único item, use a propriedade [**SWbemRefreshableItem. Object**](swbemrefreshableitem-object.md) . Se você não fizer a chamada para **SWbemRefreshableItem. Object**, o script falhará quando você tentar acessar o objeto. Para acessar uma coleção, use a propriedade [**SWbemRefreshableItem. ObjectSet**](swbemrefreshableitem-objectset.md) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Classes de contador de desempenho](/windows/desktop/CIMWin32Prov/performance-counter-classes)
</dt> <dt>

[Acessando dados de desempenho no script](accessing-performance-data-in-script.md)
</dt> <dt>

[Tarefas do WMI: monitoramento de desempenho](wmi-tasks--performance-monitoring.md)
</dt> <dt>

[Monitorando dados de desempenho](monitoring-performance-data.md)
</dt> </dl>

 

 
