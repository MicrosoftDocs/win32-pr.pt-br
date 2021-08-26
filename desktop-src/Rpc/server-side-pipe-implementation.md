---
title: Implementação de pipe de Server-Side
description: Os programas de servidor para aplicativos distribuídos que usam pipes não precisam implementar nenhuma função Push, pull ou Alloc.
ms.assetid: de733075-5767-4d46-b294-089c7e3cc695
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf5cf7a928c58890e618c9a62cf1df77fe3d00a7ef9d013240d66e57e88a1584
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120017686"
---
# <a name="server-side-pipe-implementation"></a>Implementação de pipe de Server-Side

Os programas de servidor para aplicativos distribuídos que usam pipes não precisam implementar nenhuma função Push, pull ou Alloc. Eles precisam conter procedimentos que os clientes podem invocar remotamente para iniciar transferências de dados. Nos tópicos a seguir, esta seção explica como os procedimentos remotos do servidor podem ser implementados.

-   [Implementando pipes de entrada no servidor](implementing-input-pipes-on-the-server.md)
-   [Implementando os pipes de saída no servidor](implementing-output-pipes-on-the-server.md)

 

 




