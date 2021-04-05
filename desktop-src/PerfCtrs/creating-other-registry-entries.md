---
description: A função OpenPerformanceData de DLLs de desempenho usa um argumento de cadeia de caracteres como entrada.
ms.assetid: 8ec0ea45-5789-4801-b486-555779a7303e
title: Criando outras entradas do registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dfc3b46ce642069210df5112eb41cac9a038797
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921748"
---
# <a name="creating-other-registry-entries"></a>Criando outras entradas do registro

A função [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) da DLL de desempenho usa um argumento de cadeia de caracteres como entrada. Para fornecer uma cadeia de caracteres de entrada para a função Open, inclua uma chave de **vinculação** em sua chave de **Serviços** . A chave de **vinculação** contém um valor de **exportação** . Defina os dados do valor para **Exportar** para a cadeia de caracteres de entrada que você deseja passar para a função Open. O tipo de dados de **exportação** é **reg \_ multi \_ sz**.

Se a **exportação** não for definida (**Exportar** é opcional), o sistema passará **nulo** para sua função [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) .

Normalmente, se mais de um aplicativo compartilhar a mesma DLL de desempenho, cada aplicativo incluirá uma chave de **vinculação** e um valor de **exportação** para fornecer contexto sobre o aplicativo que está chamando a dll.

O seguinte mostra as entradas do registro:

```
HKEY_LOCAL_MACHINE
   \SYSTEM
      \CurrentControlSet
         \Services
            \application-name-1
               \Linkage
                  Export = app-1 context strings
               \Performance
                  Library = perfctrs.dll
            \application-name-2
               \Linkage
                  Export = app-2 context strings
               \Performance
                  Library = perfctrs.dll
```

Por padrão, as funções [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) e [**CollectPerformanceData**](/windows/win32/api/winperf/nc-winperf-pm_collect_proc) da DLL de desempenho devem retornar dentro de 10.000 milissegundos. Caso contrário, o sistema não usa os dados retornados pela DLL. O aplicativo pode aumentar ou diminuir o valor de tempo limite especificando um valor de registro de tempo limite **aberto** ou **coletar tempo limite** em sua chave de **desempenho** , conforme mostrado no exemplo a seguir.

```
HKEY_LOCAL_MACHINE
   \SYSTEM
      \CurrentControlSet
         \Services
            \application-name
               \Performance
                  Open Timeout = Timeout value for your open function, in milliseconds
                  Collect Timeout = Timeout value for your collect function, in milliseconds
```

Para obter os dados de desempenho de alguns aplicativos (aqueles que retornam contadores usando a função [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) ), é necessário usar a função [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) para abrir o dispositivo associado ao aplicativo. Nesse caso, o nome especificado em **CreateFile** também deve ser instalado no nó dispositivos dos do registro, como mostrado aqui:

```
HKEY_LOCAL_MACHINE
   \SYSTEM
      \CurrentControlSet
         \Control
            \Session Manager
               \DOS Devices
```

 

 
