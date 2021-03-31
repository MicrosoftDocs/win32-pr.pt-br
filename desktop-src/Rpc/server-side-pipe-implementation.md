---
title: Implementação de pipe de Server-Side
description: Os programas de servidor para aplicativos distribuídos que usam pipes não precisam implementar nenhuma função Push, pull ou Alloc.
ms.assetid: de733075-5767-4d46-b294-089c7e3cc695
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6927350e10061850c5fac0ab0db7c18570dd2bab
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005776"
---
# <a name="server-side-pipe-implementation"></a>Implementação de pipe de Server-Side

Os programas de servidor para aplicativos distribuídos que usam pipes não precisam implementar nenhuma função Push, pull ou Alloc. Eles precisam conter procedimentos que os clientes podem invocar remotamente para iniciar transferências de dados. Nos tópicos a seguir, esta seção explica como os procedimentos remotos do servidor podem ser implementados.

-   [Implementando pipes de entrada no servidor](implementing-input-pipes-on-the-server.md)
-   [Implementando os pipes de saída no servidor](implementing-output-pipes-on-the-server.md)

 

 




