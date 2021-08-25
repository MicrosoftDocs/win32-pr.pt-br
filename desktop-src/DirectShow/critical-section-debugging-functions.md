---
description: Funções críticas de depuração de seção
ms.assetid: 2e58ff06-d9b2-45fe-bd40-d637aa434339
title: Funções críticas de depuração de seção
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65834d84900ad3ac893cb75493a59902629fec15523cfaca8974a6684ba9c409
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119908066"
---
# <a name="critical-section-debugging-functions"></a>Funções críticas de depuração de seção

Essas funções ajudam a depurar seções críticas em seu código, o que pode facilitar a encontrar a causa de um deadlock. Essas funções usam a [**classe auxiliar CCritSec.**](ccritsec.md)



| Função                             | Descrição                                                                  |
|--------------------------------------|------------------------------------------------------------------------------|
| [**CritCheckIn**](critcheckin.md)   | Retornará **TRUE** se o thread atual possuir a seção crítica especificada.  |
| [**CritCheckOut**](critcheckout.md) | Retornará **FALSE** se o thread atual possuir a seção crítica especificada. |
| [**DbgLockTrace**](dbglocktrace.md) | Habilita ou desabilita o registro em log de depuração para uma determinada seção crítica.              |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Utilitários de depuração](debugging-utilities.md)
</dt> </dl>

 

 



