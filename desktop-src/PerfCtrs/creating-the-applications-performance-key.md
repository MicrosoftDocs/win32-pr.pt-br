---
description: Um aplicativo que dá suporte a contadores de desempenho deve ter uma chave de desempenho sob a chave de serviços. O exemplo a seguir mostra os valores que você deve incluir para essa chave.
ms.assetid: b6cdf130-699f-49bd-97b6-a580818b3fab
title: Criando a chave de desempenho de aplicativos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d39fb89f7f5feb4e34284b541775b5c093a6bfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105753242"
---
# <a name="creating-the-applications-performance-key"></a>Criando a chave de desempenho do aplicativo

Um aplicativo que dá suporte a contadores de desempenho deve ter uma chave de **desempenho** sob a chave de **Serviços** . O exemplo a seguir mostra os valores que você deve incluir para essa chave.

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

O valor da **biblioteca** fornece o nome da DLL de desempenho e os valores de **abrir**, **coletar** e **fechar** fornecem os nomes das funções exportadas da DLL de desempenho. O tipo de dados desses valores é **reg \_ sz**. Quando um consumidor solicita dados de desempenho, o sistema usa esses valores para determinar quais DLLs de desempenho carregar e quais funções de DLL chamar.

O valor da **biblioteca** pode conter o nome da dll ou um caminho completo para a dll. Se você usar o tipo de dados **reg \_ expande \_ sz** para a **biblioteca**, poderá especificar variáveis de ambiente em seu caminho.

A chave de serviço do aplicativo deve existir antes que você possa executar o **lodctr** para carregar os nomes de contadores e as cadeias de caracteres de ajuda.

Para obter valores de registro adicionais que você pode criar, como especificar valores de tempo limite para as funções [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) e [**CollectPerformanceData**](/windows/win32/api/winperf/nc-winperf-pm_collect_proc) , consulte [criando outras entradas de registro](creating-other-registry-entries.md).

 

 
