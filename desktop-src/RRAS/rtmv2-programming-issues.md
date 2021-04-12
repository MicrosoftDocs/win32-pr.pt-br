---
title: Problemas de programação do RTMv2
description: As funções RTMv2 são escritas com as seguintes suposições.
ms.assetid: c8c6f553-57cc-4eec-bbc0-b6b50897cc75
keywords:
- Problemas de programação, RTMv2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b607adc939ff72a4d9fee99c15f6aa5192fa4c6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292150"
---
# <a name="rtmv2-programming-issues"></a>Problemas de programação do RTMv2

As funções RTMv2 são escritas com as seguintes suposições.

-   As funções RTMv2 não alocam memória para o cliente. O cliente deve sempre alocar memória.
-   Quando um cliente está cancelando o registro, ele deve executar operações de limpeza em si, como liberar toda a memória alocada.
-   Os clientes devem liberar identificadores corretamente; podem ocorrer vazamentos de memória se um cliente não observar essa prática.

 

 




