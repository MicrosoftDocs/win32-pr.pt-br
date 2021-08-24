---
description: Um aplicativo que dá suporte a contadores de desempenho deve ter uma Chave de desempenho na chave Serviços. O exemplo a seguir mostra os valores que você deve incluir para essa chave.
ms.assetid: b6cdf130-699f-49bd-97b6-a580818b3fab
title: Criando a chave de desempenho de aplicativos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c149e8142b892edeb43f5459fe68bc6ad4b7453118c64cb2e288bb334c054fff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144029"
---
# <a name="creating-the-applications-performance-key"></a>Criando a chave de desempenho do aplicativo

Um aplicativo que dá suporte a contadores de desempenho deve ter uma **Chave de** desempenho na **chave Serviços.** O exemplo a seguir mostra os valores que você deve incluir para essa chave.

```
HKEY_LOCAL_MACHINE
   \SYSTEM
      \CurrentControlSet
         \Services
            \application-name
               \Performance
                  Library = Name of your performance DLL
                  Open = Name of your Open function in your DLL
                  Collect = Name of your Collect function in your DLL
                  Close = Name of your Close function in your DLL
```

O **valor** biblioteca fornece o nome da DLL de  desempenho e os valores Abrir **,** Coletar e Fechar fornecem os nomes das funções exportadas da DLL de desempenho. O tipo de dados desses valores é **REG \_ SZ.** Quando um consumidor solicita dados de desempenho, o sistema usa esses valores para determinar quais DLLs de desempenho carregar e quais funções DLL chamar.

O **valor** biblioteca pode conter o nome da DLL ou um caminho completo para a DLL. Se você usar o tipo **de dados REG EXPAND \_ \_ SZ** para **Biblioteca**, poderá especificar variáveis de ambiente em seu caminho.

A chave de serviço do aplicativo deve existir antes que você possa executar **lodctr** para carregar seus nomes de contador e cadeias de caracteres de ajuda.

Para obter valores adicionais do Registro que você pode criar, como especificar valores de tempo limite para as funções [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) e [**CollectPerformanceData,**](/windows/win32/api/winperf/nc-winperf-pm_collect_proc) consulte Criando outras entradas [do Registro](creating-other-registry-entries.md).

 

 
