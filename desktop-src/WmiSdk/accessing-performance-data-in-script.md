---
description: Os scripts WMI podem acessar as classes de contador de desempenho do WMI pré-instalado, seja no computador local ou remotamente.
ms.assetid: 79e47173-c8b6-452d-9400-93e2bd6e9da5
ms.tgt_platform: multiple
title: Acessando dados de desempenho no script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 42fe1ecdbaf5cdc5cbafc53117ad7c8f370dae2b4e1a3adcee3a4fcf719c995a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118320439"
---
# <a name="accessing-performance-data-in-script"></a>Acessando dados de desempenho no script

Os scripts WMI podem acessar as [classes de contador de desempenho](/windows/desktop/CIMWin32Prov/performance-counter-classes)do WMI pré-instalado, seja no computador local ou remotamente. Embora os scripts possam obter dados de classes não calculadas, como [**Win32 \_ PerfRawData \_ PerfOS \_ Memory**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data)ou classes formatadas, [**a \_ \_ \_ memória Win32 PerfFormattedData PerfOS**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data), as classes de dados formatadas podem ser mais fáceis de usar.

O monitoramento de dados de desempenho com as classes do contador de desempenho requer o uso de um [*atualizador*](gloss-r.md). Use o objeto [**SWbemRefresher**](swbemrefresher.md) para armazenar um ou mais objetos de desempenho para atualizar ou atualizar um único objeto pela chamada [**SWbemObjectEx. Refresh**](swbemobjectex-refresh-.md) . Para obter mais informações, consulte [atualizando dados do WMI em scripts](refreshing-wmi-data-in-scripts.md).

Ao definir a propriedade [**SWbemRefresher. falha**](swbemrefresher-autoreconnect.md) como **true**, o WMI se reconectará automaticamente a um provedor remoto se a conexão for interrompida para que você não precise verificar o status da conexão.

Conforme mostrado no script de exemplo de código de script a seguir, você deve fazer uma chamada de atualização inicial para obter um valor inicial para o objeto que você está atualizando. Em seguida, as chamadas de atualização subsequentes contêm dados.

> [!Note]  
> Quando um script está acessando dados do contador de desempenho do WMI de um computador remoto, o script só pode ser executado sob a conta de usuário conectada no momento. O WMI não dá suporte a uma chamada [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md) que passa credenciais de usuário diferentes. Portanto, a conta que está chamando o computador remoto já deve ter os privilégios apropriados no computador.

 

O exemplo de código de script a seguir mostra como usar um objeto [**SWbemRefresher**](swbemrefresher.md) para atualizar os dados em objetos de contador de desempenho. Para obter mais informações sobre como usar contadores de desempenho no WMI, consulte [acessando classes de desempenho pré-instalado do WMI](accessing-wmi-preinstalled-performance-classes.md).


```VB
' Get raw and cooked data performance counter instances for the
" wscript process running this script

set RawProc = GetObject("winmgmts:Win32_PerfRawdata_Perfproc_process.name='wscript'")
set CookedProc = GetObject("winmgmts:Win32_Perfformatteddata_Perfproc_process.name='wscript'")

' Display the same property in raw and cooked form in a loop
for I = 1 to 6
    Wscript.Echo "wscript process raw PageFaultsPerSec = & RawProc.PageFaultsPerSec _
                 & " cooked PageFaultsPerSec= " & CookedProc.PageFaultsPerSec 

' Wait 2 seconds
    Wscript.Sleep 2000
    
    ' Refresh the object
    RawProc.Refresh_
    CookedProc.Refresh_
next
```



## <a name="example"></a>Exemplo

O exemplo de código de script a seguir mostra que você deve fazer uma chamada de atualização inicial para obter um valor inicial para o objeto atualizado. Em seguida, as chamadas de atualização subsequentes contêm dados.

O exemplo de código de script a seguir mostra como usar um objeto [**SWbemRefresher**](swbemrefresher.md) para atualizar os dados em objetos de contador de desempenho. Para obter mais informações sobre como usar contadores de desempenho no WMI, consulte [acessando classes de desempenho pré-instalado do WMI](accessing-wmi-preinstalled-performance-classes.md).


```VB
' Get raw and cooked data performance counter instances for the
" wscript process running this script

set RawProc = GetObject("winmgmts:" _
                        & "Win32_PerfRawdata_Perfproc_process." _
                        & "name='wscript'")
set CookedProc = GetObject("winmgmts:" _ 
                & "Win32_Perfformatteddata_Perfproc_process." _
                & "name='wscript'")

' Display the same property in raw and cooked form in a loop
for I = 1 to 6
    Wscript.Echo "wscript process raw PageFaultsPerSec = " _
                 & RawProc.PageFaultsPerSec _
                 & " cooked PageFaultsPerSec= " _
                 & CookedProc.PageFaultsPerSec 

' Wait 2 seconds
    Wscript.Sleep 2000
    
    ' Refresh the object
    RawProc.Refresh_
    CookedProc.Refresh_
next
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Classes de contador de desempenho](/windows/desktop/CIMWin32Prov/performance-counter-classes)
</dt> <dt>

[Tarefas do WMI: monitoramento de desempenho](wmi-tasks--performance-monitoring.md)
</dt> <dt>

[Monitorando dados de desempenho](monitoring-performance-data.md)
</dt> </dl>

 

 
