---
description: Um grupo de métodos que é usado para manipular bloqueios.
ms.assetid: ba4cc37c-bd2f-446f-8b3d-bc2a2e2e4de4
title: Métodos CShareLockNH
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b16a979c5d1f111c92a64376c48f4c0ed1a165ca
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756008"
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



 

 

 



