---
title: Resolução do temporizador
description: Resolução do temporizador
ms.assetid: 2e5e94fe-8175-417f-8c59-9d5cf052ea89
keywords:
- temporizadores de multimídia, resolução
- temporizadores, resolução
- resolução mínima do timer
- resolução máxima do timer
- temporizadores de multimídia, resolução máxima
- temporizadores, resolução máxima
- temporizadores de multimídia, resolução mínima
- temporizadores, resolução mínima
- função timeGetDevCaps
- função timeBeginPeriod
- função timeEndPeriod
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89e96f1b410f2e18203af794ea124bb6b83bccce
ms.sourcegitcommit: a0b531d335bc691100149830b256d5af7e136c24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/28/2019
ms.locfileid: "103634732"
---
# <a name="timer-resolution"></a>Resolução do temporizador

Para determinar as resoluções de temporizador mínimo e máximo com suporte nos serviços de timer, use a função [**timeGetDevCaps**](/windows/desktop/api/TimeAPI/nf-timeapi-timegetdevcaps) . Essa função preenche os membros **wPeriodMin** e **wPeriodMax** da estrutura [**timecaps**](/windows/desktop/api/TimeAPI/ns-timeapi-timecaps) com as resoluções mínima e máxima. Esse intervalo pode variar entre computadores e plataformas Windows.

Depois de determinar as resoluções de temporizador mínimo e máximo disponíveis, você deve estabelecer a resolução mínima que deseja que seu aplicativo use. Use as funções [**timeBeginPeriod**](/windows/desktop/api/TimeAPI/nf-timeapi-timebeginperiod) e [**timeEndPeriod**](/windows/desktop/api/TimeAPI/nf-timeapi-timeendperiod) para definir e limpar essa resolução. Você deve corresponder a cada chamada para **timeBeginPeriod** com uma chamada para **timeEndPeriod**, especificando a mesma resolução mínima em ambas as chamadas. Um aplicativo pode fazer várias chamadas **timeBeginPeriod** , contanto que cada chamada seja correspondida com uma chamada para **timeEndPeriod**.

Em [**timeBeginPeriod**](/windows/desktop/api/TimeAPI/nf-timeapi-timebeginperiod) e [**timeEndPeriod**](/windows/desktop/api/TimeAPI/nf-timeapi-timeendperiod), o parâmetro *uPeriod* indica a resolução mínima do timer, em milissegundos. Você pode especificar qualquer valor de resolução do temporizador dentro do intervalo com suporte pelo temporizador.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre timers de multimídia](about-multimedia-timers.md)
</dt> </dl>

 

 




