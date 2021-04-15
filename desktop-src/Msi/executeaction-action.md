---
description: A ação ExecuteAction inicia a sequência de execução usando a propriedade EXECUTEaction para determinar qual tipo de instalação deve ser executada.
ms.assetid: 61878317-ac87-4f6e-9375-12a78969e29e
title: Ação ExecuteAction
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2970a0fb4e9297264071769ac7415cd2acf866b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104461226"
---
# <a name="executeaction-action"></a>Ação ExecuteAction

A ação ExecuteAction inicia a sequência de execução usando a propriedade [**ExecuteAction**](executeaction.md) para determinar qual tipo de instalação deve ser executada.

## <a name="sequence-restrictions"></a>Restrições de sequência

Essa ação deve ser sequenciada depois de todas as coletas de informações necessárias para começar a instalação ser concluída. Ações adicionais podem ser sequenciadas após a ação ExecuteAction na [tabela InstallUISequence](installuisequence-table.md)e a [tabela AdminUISequence](adminuisequence-table.md). Normalmente, uma sequência começará com ações de [*custo*](c-gly.md) , como a [ação CostInitialize](costinitialize-action.md), seguida pelas ações da interface do usuário e a ação ExecuteAction.

## <a name="actiondata-messages"></a>Mensagens ActionData

Não há nenhuma mensagem ActionData.

## <a name="remarks"></a>Comentários

A ação ExecuteAction é executada com privilégios de sistema se o serviço do instalador estiver habilitado. As ações de nível superior, como a ação de [instalação](install-action.md), a [ação de anúncio](advertise-action.md)e a ação de [administrador](admin-action.md) incluem lógica interna que determina se a chamada da ação ExecuteAction exige que a sequência de execução ou a sequência da interface do usuário seja executada.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tabela InstallUISequence](installuisequence-table.md)
</dt> <dt>

[Tabela AdminUISequence](adminuisequence-table.md)
</dt> <dt>

[Ação CostInitialize](costinitialize-action.md)
</dt> </dl>

 

 



