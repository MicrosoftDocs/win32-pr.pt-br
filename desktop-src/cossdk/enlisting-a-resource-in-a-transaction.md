---
description: Inscrever um recurso em uma transação
ms.assetid: b41fe0aa-a4cf-4d4a-9543-8eb0b38f07a2
title: Inscrever um recurso em uma transação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 327ef1ab34d32853be0ca7d4641958b4f57ab55577865aad8612821e98882c71
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119858956"
---
# <a name="enlisting-a-resource-in-a-transaction"></a>Inscrever um recurso em uma transação

Depois que um recurso é alocado, mas logo antes de retornar o recurso para o distribuidor de recursos, o gerenciador do distribuidor verifica com COM+ para ver se o objeto de chamada está em execução dentro de uma transação. Se o objeto de chamada estiver em execução em uma transação, o gerenciador do distribuidor chamará de volta o distribuidor de recursos e pedirá que ele insruia o recurso na transação. Em seguida, o recurso é retornado para o distribuidor de recursos, que, em seguida, o retorna para a instância de chamada.

O distribuidor de recursos deve ser capaz de se inscrever em uma transação OLE com o Coordenador de Transações Distribuídas (DTC).

> [!Note]  
> A inserção de transação é opcional quando um distribuidor de recursos libera recursos não transacionais, como memória ou threads.

 

Quando uma transação é concluída, o COM+ notifica o gerenciador do distribuidor sobre se ela foi comprometida ou anulada. Em seguida, o gerenciador do distribuidor notifica o titular de cada administrador de recursos de que todos os recursos inscritos nessa transação agora podem ser movidos para o inventário geral.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Conceitos do Com+ Resource Dispenser](com--resource-dispenser-concepts.md)
</dt> <dt>

[Estados de recursos em pool disponíveis para o Com+ Resource Dispenser](pooled-resource-states-available-to-com--resource-dispenser.md)
</dt> <dt>

[Processo de alocação de recursos do Alocador de Recursos](resource-dispenser-resource-allocation-process.md)
</dt> </dl>

 

 



