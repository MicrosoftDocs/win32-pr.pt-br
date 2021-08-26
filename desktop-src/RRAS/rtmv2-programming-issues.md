---
title: Problemas de programação RTMv2
description: As funções RTMv2 são escritas com as suposições a seguir.
ms.assetid: c8c6f553-57cc-4eec-bbc0-b6b50897cc75
keywords:
- Problemas de programação, RTMv2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 584568fc3c4e7a46a2a2114781b81465d893b80978471aa3149d93d38f0c8c5d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120035586"
---
# <a name="rtmv2-programming-issues"></a>Problemas de programação RTMv2

As funções RTMv2 são escritas com as suposições a seguir.

-   As funções RTMv2 não alocam memória para o cliente. O cliente sempre deve alocar memória.
-   Quando um cliente está sendo anuado, ele deve executar operações de limpeza em si, como liberar toda a memória alocada.
-   Os clientes devem liberar os alças corretamente; vazamentos de memória podem ocorrer se um cliente não observar essa prática.

 

 




