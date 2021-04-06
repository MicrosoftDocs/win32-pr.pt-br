---
description: As funções auxiliares a seguir só podem ser chamadas por especialistas que exportam a função executar ou configurar.
ms.assetid: 6890087c-7c94-41ff-bb5c-4bf88a4e07cc
title: Funções de especialista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7441289008c7dcd647775c2932e210ccd09b24bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826843"
---
# <a name="expert-functions"></a>Funções de especialista

As funções auxiliares a seguir só podem ser chamadas por especialistas que exportam a função [executar](run.md) ou [Configurar](configure.md) .



| Função                                         | Descrição                                                                             |
|--------------------------------------------------|-----------------------------------------------------------------------------------------|
| [ExpertGetFrame](expertgetframe.md)             | Recupera um determinado quadro da captura.                                               |
| [ExpertIndicateStatus](expertindicatestatus.md) | Indica a porcentagem de conclusão da análise de captura do especialista.             |
| [ExpertGetStartupInfo](expertgetstartupinfo.md) | Recupera as informações de inicialização para o especialista.                                       |
| [ExpertMemorySize](expertmemorysize.md)         | Recupera o tamanho da memória alocada por uma chamada para a função **ExpertAllocMemory** . |
| [ExpertSubmitEvent](expertsubmitevent.md)       | Indica um problema e recupera informações sobre o problema, se houver.          |
| [ExpertAllocMemory](expertallocmemory.md)       | Aloca memória para o especialista.                                                        |
| [ExpertReallocMemory](expertreallocmemory.md)   | Altera o tamanho da memória alocada pela função **ExpertAllocMemory** .         |
| [ExpertFreeMemory](expertfreememory.md)         | Libera memória alocada pelo especialista.                                                   |



 

Para obter informações sobre funções de exportação, funções auxiliares que podem ser chamadas por especialistas e analisadores, estruturas e enumerações, consulte os seguintes tópicos:



| Para obter informações sobre                                             | Consulte                                                                          |
|-------------------------------------------------------------------|------------------------------------------------------------------------------|
| Funções exportadas por especialistas                            | [Funções de exportação de DLL de especialista](expert-dll-export-functions.md)               |
| Estruturas que são usadas por funções de especialista                      | [Estruturas de especialistas](expert-structures.md)                                   |
| Enumerações usadas por estruturas e funções de especialistas              | [Enumerações de especialistas](expert-enumerations.md)                               |
| Funções auxiliares comuns que podem ser chamadas por especialistas e analisadores | [Funções comuns de expert e parser](expert-and-parser-common-functions.md) |



 

 

 



