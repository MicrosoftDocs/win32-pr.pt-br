---
description: A tabela a seguir lista os
ms.assetid: 3f47a52c-2d36-4a74-9d7f-df37645b8e72
title: Ferramentas de contadores de desempenho
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: dc40dd5dfe640e09ac6f7258856389f04d60215f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921729"
---
# <a name="performance-counters-tools"></a>Ferramentas de contadores de desempenho

## <a name="data-collection-tools"></a>Ferramentas de coleta de dados

As ferramentas a seguir são úteis ao consumir ou manipular dados do contador de desempenho do Windows.

|Ferramenta|Descrição
|----|-----------
| [PerfMon](/windows-server/administration/windows-commands/perfmon) | Ferramenta de GUI para coletar e exibir dados do contador de desempenho. `perfmon.exe` inicia o MMC com o snap-in Monitor de desempenho, que fornece acesso ao monitor de desempenho, conjuntos de coletores de dados e ferramentas de relatórios.
| [TypePerf](/windows-server/administration/windows-commands/typeperf) |Ferramenta de linha de comando para coletar e imprimir dados do contador de desempenho. Pode ser usado para listar os conjuntos de linhas disponíveis, listar os contadores disponíveis, imprimir dados do contador no console ou coletar dados do contador para um arquivo de log (CSV, TDF, BLG).
| [Relog](/windows-server/administration/windows-commands/relog) |Ferramenta de linha de comando para transformar e mesclar arquivos de log (CSV, TDF, BLG) capturados via `typeperf.exe` ou por meio das `PDH.dll` APIs.
| [LogMan](/windows-server/administration/windows-commands/logman) |Ferramenta de linha de comando para controlar conjuntos de coletores de dados.

## <a name="data-provider-tools"></a>Ferramentas de provedor de dados

As ferramentas a seguir são úteis ao publicar dados do contador de desempenho do Windows.

|Ferramenta|Descrição
|----|-----------
| [CtrPP](ctrpp.md) | Ferramenta de criação de linha de comando do SDK do Windows que valida e compila seu manifesto de provedor de contadores de desempenho v2. Essa ferramenta gera os `.h` cabeçalhos e os `.rc` scripts de recursos necessários para criar um provedor v2.
| [LodCtr](/windows-server/administration/windows-commands/lodctr) | Ferramenta de linha de comando usada para instalar seu provedor em um sistema.
| [UnlodCtr](/windows-server/administration/windows-commands/unlodctr_1) | Ferramenta de linha de comando usada para desinstalar seu provedor de um sistema.
