---
description: Um thread pode, a qualquer momento, chamar WSAIsBlocking para determinar se uma chamada de bloqueio está em andamento no momento.
ms.assetid: 6213ded4-feab-404f-86a0-3db9a0a42769
title: Cancelando operações de bloqueio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5064948fe7c1c1262acb9f4f8ef25a3ad3e721e77a188f313541595ef75f9ce9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120030686"
---
# <a name="canceling-blocking-operations"></a>Cancelando operações de bloqueio

Um thread pode, a qualquer momento, chamar [WSAIsBlocking](/windows/desktop/api/winsock2/nf-winsock2-wsaisblocking) para determinar se uma chamada de bloqueio está em andamento no momento. (essa função é implementada dentro dos shims de compatibilidade do Windows sockets 1,1 e, portanto, não tem uma contraparte SPI.) É claro que isso só é possível quando o pseudo bloqueio, ao contrário do bloqueio verdadeiro, está sendo empregado pelo provedor de serviços. Quando necessário, [**WSPCancelBlockingCall**](/previous-versions/windows/desktop/legacy/ms742269(v=vs.85)) pode ser chamado a qualquer momento para cancelar qualquer operação de pseudo-bloqueio atual.

 

 
