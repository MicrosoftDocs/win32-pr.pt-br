---
description: 'Você pode consumir dados de desempenho usando uma das seguintes interfaces: a interface do auxiliar de dados de desempenho (PDH), que fornece acesso de alto nível aos dados dos provedores de contador de desempenho da versão 1 e da versão 2. A interface do registro, que fornece acesso de baixo nível aos dados de provedores de contador de desempenho. A interface de biblioteca de desempenho, que fornece acesso direto aos dados dos provedores de contador de desempenho da versão 2. A interface PDH é mais fácil de usar do que a interface do registro e é recomendada para a maioria das tarefas de coleta de dados de desempenho. A interface PDH é essencialmente uma abstração de nível superior da funcionalidade fornecida pela interface do registro. Use a interface de biblioteca de desempenho somente se você não puder usar as funções de camada de abstração de PDH.'
ms.assetid: a42f6cdd-47e9-4f43-aeaf-37a5abb0fa36
title: Consumindo dados do contador
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: f3abcc6dd5a385ebffdc887516613efb76b53359e5f8995bc28ba7f6239187b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119775676"
---
# <a name="consuming-counter-data"></a>Consumindo dados do contador

os programas que desejam ler e usar Windows dados do contador de desempenho podem usar uma das várias interfaces conforme apropriado para o cenário.

- Os scripts podem usar as [classes do contador de desempenho WMI](/windows/desktop/WmiSdk/monitoring-performance-data) ou a ferramenta [TypePerf](/windows-server/administration/windows-commands/typeperf) .
- Os programas .NET podem usar a [classe PerformanceCounter](/dotnet/api/system.diagnostics.performancecounter).
- A [biblioteca do auxiliar de dados de desempenho (PDH)](using-the-pdh-functions-to-consume-counter-data.md) fornece acesso de alto nível aos dados de provedores de contador de desempenho v1 e v2 por meio de uma API Win32 (C/C++).
- A [interface do registro](using-the-registry-functions-to-consume-counter-data.md) fornece acesso a dados de provedores de contador de desempenho v1 e v2 por meio da `HKEY_PERFORMANCE_DATA` chave do registro especial.
- As [funções de consumidor do PerfLib v2](using-the-perflib-functions-to-consume-counter-data.md) fornecem acesso de baixo nível aos dados de provedores de contador de desempenho v2 por meio de uma API Win32 (C/C++).

A interface PDH é recomendada para a maioria das tarefas de coleta de dados de desempenho do C/C++, pois é mais fácil de usar do que as interfaces do registro e do PerfLib.
