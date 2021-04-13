---
description: Funções de depuração de seção crítica
ms.assetid: 2e58ff06-d9b2-45fe-bd40-d637aa434339
title: Funções de depuração de seção crítica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 098558a97e38168595dc89c3c81175c9d6635c5d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500285"
---
# <a name="critical-section-debugging-functions"></a>Funções de depuração de seção crítica

Essas funções ajudam a depurar seções críticas em seu código, o que pode facilitar a localização da causa de um deadlock. Essas funções usam a classe auxiliar [**CCritSec**](ccritsec.md) .



| Função                             | Descrição                                                                  |
|--------------------------------------|------------------------------------------------------------------------------|
| [**CritCheckIn**](critcheckin.md)   | Retornará **true** se o thread atual possuir a seção crítica especificada.  |
| [**CritCheckOut**](critcheckout.md) | Retorna **false** se o thread atual possui a seção crítica especificada. |
| [**DbgLockTrace**](dbglocktrace.md) | Habilita ou desabilita o log de depuração para uma determinada seção crítica.              |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Utilitários de depuração](debugging-utilities.md)
</dt> </dl>

 

 



