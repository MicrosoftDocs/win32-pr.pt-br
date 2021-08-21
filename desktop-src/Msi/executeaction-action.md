---
description: A ação ExecuteAction inicia a sequência de execução usando a propriedade EXECUTEACTION para determinar qual tipo de instalação executar.
ms.assetid: 61878317-ac87-4f6e-9375-12a78969e29e
title: Ação ExecuteAction
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20555af337f8774aec6c58769f2235da97ae763e044665e407a8dc29e75de750
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118636883"
---
# <a name="executeaction-action"></a>Ação ExecuteAction

A ação ExecuteAction inicia a sequência de execução usando a [**propriedade EXECUTEACTION**](executeaction.md) para determinar qual tipo de instalação executar.

## <a name="sequence-restrictions"></a>Restrições de sequência

Essa ação deve ser sequenciada depois que toda a coleta de informações necessária para iniciar a instalação for concluída. Ações adicionais podem ser sequenciadas após a ação ExecuteAction na tabela [InstallUISequence](installuisequence-table.md)e [na tabela AdminUISequence](adminuisequence-table.md). Uma sequência normalmente começará [](c-gly.md) com ações de custo, como a ação [CostInitialize](costinitialize-action.md), seguida pelas ações da interface do usuário e, em seguida, pela ação ExecuteAction.

## <a name="actiondata-messages"></a>Mensagens ActionData

Não há mensagens ActionData.

## <a name="remarks"></a>Comentários

A ação ExecuteAction será executada com privilégios do sistema se o serviço do instalador estiver habilitado. As ações de nível superior, como a ação [INSTALL](install-action.md), a ação [ADVERTISE](advertise-action.md)e a ação [ADMIN](admin-action.md) incluem lógica interna que determina se chamar a ação ExecuteAction requer que a sequência de execução ou a sequência de interface do usuário seja executada.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tabela InstallUISequence](installuisequence-table.md)
</dt> <dt>

[Tabela AdminUISequence](adminuisequence-table.md)
</dt> <dt>

[Ação CostInitialize](costinitialize-action.md)
</dt> </dl>

 

 



