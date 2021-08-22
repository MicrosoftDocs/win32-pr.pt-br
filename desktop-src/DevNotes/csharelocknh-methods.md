---
description: Um grupo de métodos que é usado para manipular bloqueios.
ms.assetid: ba4cc37c-bd2f-446f-8b3d-bc2a2e2e4de4
title: Métodos CShareLockNH
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97234d65a3be75ffc1eb679db31360aa6ce6c416d879c67c0ffc5385e10bdb49
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119654646"
---
# <a name="csharelocknh-methods"></a>Métodos CShareLockNH

Um grupo de métodos que é usado para manipular bloqueios.

## <a name="methods"></a>Métodos

Os métodos a seguir são exportados por Rwnh.dll.



| Método                                                                   | Descrição                                                     |
|--------------------------------------------------------------------------|-----------------------------------------------------------------|
| [**ExclusiveLock**](csharelocknh--exclusivelock.md)                     | Adquire um bloqueio de leitor/gravador.                                  |
| [**ExclusiveToPartial**](csharelocknh--exclusivetopartial.md)           | Altera o estado.                                              |
| [**ExclusiveUnlock**](csharelocknh--exclusiveunlock.md)                 | Libera um bloqueio.                                                |
| [**FirstPartialToExclusive**](csharelocknh--firstpartialtoexclusive.md) | Usado na conversão de um bloqueio parcial para um bloqueio exclusivo.         |
| [**PartialLock**](csharelocknh--partiallock.md)                         | Impede que mais de um thread conclua a aquisição de um bloqueio. |
| [**PartialUnlock**](csharelocknh--partialunlock.md)                     | Libera um bloqueio parcial.                                        |
| [**ShareLock**](csharelocknh--sharelock.md)                             | Obtém um bloqueio para o modo compartilhado.                                 |
| [**ShareUnlock**](csharelocknh--shareunlock.md)                         | Libera um bloqueio do modo compartilhado.                               |
| [**SharedToPartial**](csharelocknh--sharedtopartial.md)                 | Obtém um bloqueio parcial.                                         |
| [**TryExclusiveLock**](csharelocknh--tryexclusivelock.md)               | Obtém um bloqueio exclusivamente.                                     |



 

 

 



