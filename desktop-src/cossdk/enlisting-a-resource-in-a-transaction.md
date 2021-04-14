---
description: Inlistando um recurso em uma transação
ms.assetid: b41fe0aa-a4cf-4d4a-9543-8eb0b38f07a2
title: Inlistando um recurso em uma transação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db0a0bf93f373872c8be79054899dea4199dda7e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370505"
---
# <a name="enlisting-a-resource-in-a-transaction"></a>Inlistando um recurso em uma transação

Depois que um recurso é alocado, mas antes de retornar o recurso para o dispensador de recurso, o Gerenciador do dispensador verifica com COM+ para ver se o objeto de chamada está sendo executado dentro de uma transação. Se o objeto de chamada estiver sendo executado em uma transação, o Gerenciador do dispensador chamará de volta para o dispensador de recursos e solicitará que ele inscreva o recurso na transação. Em seguida, o recurso é retornado para o dispensador de recursos, que o retorna para a instância de chamada.

O dispensador de recursos deve ser capaz de se inscrever em uma transação OLE com o Coordenador de Transações Distribuídas (DTC).

> [!Note]  
> A inscrição de transação é opcional quando um dispensador de recurso dispensa recursos não transacionais, como memória ou threads.

 

Quando uma transação é concluída, o COM+ notifica o Gerenciador do dispensador sobre se ele foi confirmado ou anulado. Em seguida, o Gerenciador do dispensador notifica o detentor de cada dispensador de recursos de que todos os recursos inscritos nesta transação agora podem ser movidos para o inventário geral.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Conceitos do dispensador de recursos COM+](com--resource-dispenser-concepts.md)
</dt> <dt>

[Estados de recursos em pool disponíveis para o dispensador de recursos COM+](pooled-resource-states-available-to-com--resource-dispenser.md)
</dt> <dt>

[Processo de alocação de recursos do dispensador de recursos](resource-dispenser-resource-allocation-process.md)
</dt> </dl>

 

 



