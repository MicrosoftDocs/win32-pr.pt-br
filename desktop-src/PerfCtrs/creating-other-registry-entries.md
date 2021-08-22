---
description: A função OpenPerformanceData de DLLs de desempenho recebe um argumento de cadeia de caracteres como entrada.
ms.assetid: 8ec0ea45-5789-4801-b486-555779a7303e
title: Criando outras entradas do Registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5ad9fe960713a481ba5a9b8f4b73e11bdbdd4d9fe9474b04b994e373ce8e1bd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119683966"
---
# <a name="creating-other-registry-entries"></a>Criando outras entradas do Registro

A função [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) da DLL de desempenho recebe um argumento de cadeia de caracteres como entrada. Para fornecer uma cadeia de caracteres de entrada para sua função aberta, inclua uma **chave de vinculação** em sua **chave de** Serviços. A **chave De vinculação** contém um **valor exportar.** De definir os dados de valor **para Exportar** para a cadeia de caracteres de entrada que você deseja passar para a função aberta. O tipo de dados **Export** é **REG MULTI \_ \_ SZ.**

Se **Exportar** não estiver definido (**Exportar** é opcional), o sistema passará **NULL** para sua [**função OpenPerformanceData.**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85))

Normalmente, se mais de um aplicativo compartilhar **a** mesma DLL de  desempenho, cada aplicativo incluirá uma chave de vinculação e um valor exportar para fornecer contexto sobre qual aplicativo está chamando a DLL.

O seguinte mostra as entradas do Registro:

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

Por padrão, as funções [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) e [**CollectPerformanceData**](/windows/win32/api/winperf/nc-winperf-pm_collect_proc) da DLL de desempenho devem retornar dentro de 10.000 milissegundos. Caso não seja, o sistema não usará os dados que a DLL retorna. O aplicativo pode aumentar ou diminuir o valor de  tempo-máximo especificando um  valor de Registro de TempoOut aberto ou Coletar TempoOut em sua chave de desempenho, conforme mostrado no exemplo a seguir. 

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

Para obter os dados de desempenho de alguns aplicativos (aqueles que retornam contadores usando a função [**DeviceIoControl),**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) é necessário usar a [**função CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) para abrir o dispositivo associado ao aplicativo. Nesse caso, o nome especificado em **CreateFile** também deve ser instalado no nó Dispositivos DOS do registro, conforme mostrado aqui:

```
HKEY_LOCAL_MACHINE
   \SYSTEM
      \CurrentControlSet
         \Control
            \Session Manager
               \DOS Devices
```

 

 
