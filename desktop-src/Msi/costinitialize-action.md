---
description: A ação CostInitialize inicia o processo de custo de instalação.
ms.assetid: be9a8382-c892-44ae-8b59-c665b5cca2d2
title: Ação CostInitialize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 959e9e250292a44050c1f4b9feb3fb29f7530fe2a1f53aa77a62bf3680ea9eeb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118948363"
---
# <a name="costinitialize-action"></a>Ação CostInitialize

A ação CostInitialize inicia o processo de [*custo de*](c-gly.md) instalação.

## <a name="sequence-restrictions"></a>Restrições de sequência

Qualquer ação padrão [ou](custom-actions.md) personalizada que afete o custo deve ser sequenciada antes da ação CostInitialize. Chame a [ação FileCost](filecost-action.md) imediatamente após a ação CostInitialize. Em seguida, chame a ação [CostFinalize](costfinalize-action.md) após a ação CostInitialize para disponibilizar todos os cálculos de custo finais para o instalador por meio da [tabela Componente.](component-table.md)

## <a name="actiondata-messages"></a>Mensagens ActionData

Não há mensagens ActionData.

## <a name="remarks"></a>Comentários

A ação CostInitialize carrega a tabela Componente e a [Tabela de](feature-table.md) recursos na memória.

Para obter mais informações sobre [*o processo de*](c-gly.md) custo no instalador, consulte Custo do [arquivo](file-costing.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Custo do arquivo](file-costing.md)
</dt> </dl>

 

 



