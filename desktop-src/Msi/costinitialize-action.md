---
description: A ação CostInitialize inicia o processo de custos de instalação.
ms.assetid: be9a8382-c892-44ae-8b59-c665b5cca2d2
title: Ação CostInitialize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 251bb0ae7508c87cd0af7ab81196c5d739e923a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105768475"
---
# <a name="costinitialize-action"></a>Ação CostInitialize

A ação CostInitialize inicia o processo de [*custos*](c-gly.md) de instalação.

## <a name="sequence-restrictions"></a>Restrições de sequência

Todas as ações padrão ou [personalizadas](custom-actions.md) que afetam o custo devem ser sequenciadas antes da ação CostInitialize. Chame a ação [filecost](filecost-action.md) imediatamente após a ação CostInitialize. Em seguida, chame a ação [CostFinalize](costfinalize-action.md) seguindo a ação de ação CostInitialize para disponibilizar todos os cálculos de custo final para o instalador por meio da tabela de [componentes](component-table.md) .

## <a name="actiondata-messages"></a>Mensagens ActionData

Não há nenhuma mensagem ActionData.

## <a name="remarks"></a>Comentários

A ação CostInitialize carrega a tabela de componentes e a tabela de [recursos](feature-table.md) na memória.

Para obter mais informações sobre o processo de [*custos*](c-gly.md) no instalador, consulte [custos de arquivo](file-costing.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Custo do arquivo](file-costing.md)
</dt> </dl>

 

 



