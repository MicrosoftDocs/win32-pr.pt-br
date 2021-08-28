---
description: As funções auxiliares a seguir só podem ser chamadas por especialistas que exportam a função Executar ou Configurar.
ms.assetid: 6890087c-7c94-41ff-bb5c-4bf88a4e07cc
title: Funções de especialista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b189f0af3b748bc6ad162342ae23d98cbf0e381232193c114d245fa6aadb77c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119779376"
---
# <a name="expert-functions"></a>Funções de especialista

As funções auxiliares a seguir só podem ser chamadas por especialistas que exportam a [função Executar](run.md) [ou](configure.md) Configurar.



| Função                                         | Descrição                                                                             |
|--------------------------------------------------|-----------------------------------------------------------------------------------------|
| [ExpertGetFrame](expertgetframe.md)             | Recupera um determinado quadro da captura.                                               |
| [ExpertIndicateStatus](expertindicatestatus.md) | Indica o percentual de conclusão da análise de captura do especialista.             |
| [ExpertGetStartupInfo](expertgetstartupinfo.md) | Recupera as informações de inicialização para o especialista.                                       |
| [ExpertMemorySize](expertmemorysize.md)         | Recupera o tamanho da memória alocada por uma chamada para a **função ExpertAllocMemory.** |
| [ExpertSubmitEvent](expertsubmitevent.md)       | Indica um problema e recupera informações sobre o problema se houver um.          |
| [ExpertAllocMemory](expertallocmemory.md)       | Aloca memória para o especialista.                                                        |
| [ExpertReallocMemory](expertreallocmemory.md)   | Altera o tamanho da memória alocada pela **função ExpertAllocMemory.**         |
| [ExpertFreeMemory](expertfreememory.md)         | Libera a memória alocada pelo especialista.                                                   |



 

Para obter informações sobre funções de exportação, funções auxiliares que podem ser chamadas por especialistas e analisadores, estruturas e enumerações, consulte os seguintes tópicos:



| Para obter informações sobre                                             | Consulte                                                                          |
|-------------------------------------------------------------------|------------------------------------------------------------------------------|
| Funções que são exportadas por especialistas                            | [Funções de exportação de DLL especialista](expert-dll-export-functions.md)               |
| Estruturas que são usadas por funções especializadas                      | [Estruturas de especialistas](expert-structures.md)                                   |
| Enumerações usadas por estruturas e funções especializadas              | [Enumerações de especialistas](expert-enumerations.md)                               |
| Funções auxiliares comuns que podem ser chamadas por especialistas e analisadores | [Funções comuns de especialista e analisador](expert-and-parser-common-functions.md) |



 

 

 



