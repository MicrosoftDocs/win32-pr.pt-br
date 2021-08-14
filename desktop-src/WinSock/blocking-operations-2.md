---
description: A noção de bloqueio em um Windows ambiente tem sido historicamente muito importante.
ms.assetid: bd2ede96-34a4-4912-b9d2-ef11d37d2292
title: Operações de bloqueio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d130de2322e10de15bc73e9901b7d55764b34cfbb609e2e25942fb55a3cf445
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118322431"
---
# <a name="blocking-operations"></a>Operações de bloqueio

A noção de bloqueio em um Windows ambiente tem sido historicamente muito importante. No Windows soquetes 1.1, as chamadas de bloqueio não eram desacentadas, pois elas tendiam a desabilitar a interação contínua com o sistema. Além disso, eles empregam uma técnica de pseudobloco que, por vários motivos, nem sempre funciona conforme o esperado. No entanto, em ambientes pré-agendados Windows, chamadas de bloqueio fazem muito mais sentido, podem ser implementadas por serviços nativos do sistema operacional e, na verdade, são um mecanismo geralmente preferencial. A API winsock 2 não dá mais suporte ao psuedoblocking, mas como os shims de compatibilidade do Windows Sockets 1.1 devem continuar a emular esse comportamento, os provedores de serviços devem dar suporte a isso, conforme descrito a seguir.

 

 



