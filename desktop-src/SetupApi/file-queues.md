---
description: As funções de instalação incluem a funcionalidade de fila de arquivos.
ms.assetid: 628850ab-eb66-4b60-9298-1a44a7f6a390
title: Filas de arquivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1af071d059ea6862f79927da5321d027257bafb035bc81a3586ed34b8dcd9505
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117965642"
---
# <a name="file-queues"></a>Filas de arquivos

As funções de instalação incluem a funcionalidade de fila de arquivos. Uma fila de arquivos é uma lista de operações de cópia, renomeação e exclusão de arquivos. Essas operações podem ser enviadas para a fila em qualquer ordem. Quando a fila é comprometida, essas operações são processadas como um lote, na ordem do tipo de operação.

As seções a seguir explicam o que é uma fila e como usá-la ao criar um aplicativo de instalação. Também é discutida a ordem na qual as operações de arquivo enfileiradas são processadas à medida que a fila confirma e quais notificações a fila envia para uma rotina de retorno de chamada em cada estágio.

-   [Sobre filas de arquivos](about-file-queues.md)
-   [Usando filas de arquivos](using-file-queues.md)
-   [Referência da fila de arquivos](file-queue-reference.md)

 

 



