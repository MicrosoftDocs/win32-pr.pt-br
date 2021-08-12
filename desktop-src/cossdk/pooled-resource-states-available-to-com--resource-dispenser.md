---
description: Estados de recursos em pool disponíveis para o Com+ Resource Dispenser
ms.assetid: 5037f11c-d113-49b0-b26f-0e3bc59ae8b3
title: Estados de recursos em pool disponíveis para o Com+ Resource Dispenser
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b0f28a54a85ed134bf95a8150b5bb4b9cb0d2fda15a16b0b96238ac8c2da18f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118305615"
---
# <a name="pooled-resource-states-available-to-com-resource-dispenser"></a>Estados de recursos em pool disponíveis para o Com+ Resource Dispenser

A qualquer momento, um recurso está em uso ou não está em uso e está inscrito ou não está inscrito em uma transação. Isso gera quatro estados de recursos possíveis, da seguinte maneira:

-   **Recursos no inventário não listado.** Um recurso que não está em uso por um objeto e não está inscrito em uma transação está em inventário não listado. Um recurso em inventário geral está disponível para atribuição.

-   **Recursos no inventário inscrito.** Um recurso que não está em uso por um objeto, mas está inscrito em uma transação, está no inventário inscrito. Esse recurso está disponível para atribuição somente para objetos em execução na mesma transação. Um recurso passa do inventário inscrito para o inventário não inscrito quando o COM+ notifica o gerenciador de distribuidores de que a transação foi concluída.

-   **Recursos em uso não listado.** Se um recurso for atribuído a um objeto e a instância não estiver em execução em uma transação ou o distribuidor de recursos tiver identificado o recurso como não transacional, esse recurso está em uso não na lista.

-   **Recursos em uso inscrito.** Se um recurso for atribuído a um objeto, a instância será em execução em uma transação e o distribuidor de recursos tiver inscrito com êxito o recurso na transação, esse recurso está em uso inscrito.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Conceitos do Com+ Resource Dispenser](com--resource-dispenser-concepts.md)
</dt> <dt>

[Inscrever um recurso em uma transação](enlisting-a-resource-in-a-transaction.md)
</dt> </dl>

 

 



