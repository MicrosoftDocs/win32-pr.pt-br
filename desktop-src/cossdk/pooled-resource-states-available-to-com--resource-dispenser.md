---
description: Estados de recursos em pool disponíveis para o dispensador de recursos COM+
ms.assetid: 5037f11c-d113-49b0-b26f-0e3bc59ae8b3
title: Estados de recursos em pool disponíveis para o dispensador de recursos COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff0bc59dcc2b7e95e060c0d6e96a5880d09d26e3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457052"
---
# <a name="pooled-resource-states-available-to-com-resource-dispenser"></a>Estados de recursos em pool disponíveis para o dispensador de recursos COM+

A qualquer momento, um recurso está em uso ou não está em uso e é inscrito ou não inscrito em uma transação. Isso produz quatro Estados de recursos possíveis, da seguinte maneira:

-   **Recursos no inventário não inscrito.** Um recurso que não está sendo usado por um objeto e que não está inscrito em uma transação está no inventário não inscrito. Um recurso no inventário geral está disponível para atribuição.

-   **Recursos no inventário inscrito.** Um recurso que não está sendo usado por um objeto, mas que está inscrito em uma transação está no estoque inscrito. Esse recurso está disponível para atribuição somente a objetos em execução na mesma transação. Um recurso passa do inventário inscrito para o inventário não inscrito quando o COM+ notifica o Gerenciador do dispensador de que a transação foi concluída.

-   **Recursos no uso não inscrito.** Se um recurso for atribuído a um objeto e a instância não estiver sendo executada em uma transação ou o dispensador de recurso tiver identificado o recurso como não transacional, esse recurso estará no uso não inscrito.

-   **Recursos no uso inscrito.** Se um recurso for atribuído a um objeto, a instância estiver sendo executada em uma transação e o dispensador de recursos tiver inscrito com êxito o recurso na transação, esse recurso estará no uso inscrito.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Conceitos do dispensador de recursos COM+](com--resource-dispenser-concepts.md)
</dt> <dt>

[Inlistando um recurso em uma transação](enlisting-a-resource-in-a-transaction.md)
</dt> </dl>

 

 



