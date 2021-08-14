---
description: A ação CostFinalize encerra o processo de custo de instalação interno iniciado pela ação CostInitialize.
ms.assetid: ae69ad03-5acc-4a62-ba71-3a4e477d34ab
title: Ação CostFinalize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24f6b8fb49218925d3f517a9d198a638bc9dff5a1184beef24a487de0112830f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118638350"
---
# <a name="costfinalize-action"></a>Ação CostFinalize

A ação CostFinalize encerra o processo [*de*](c-gly.md) custo de instalação interno iniciado pela [ação CostInitialize.](costinitialize-action.md)

## <a name="sequence-restrictions"></a>Restrições de sequência

Qualquer ação padrão [ou personalizada](custom-actions.md) que afete o custo deve ser sequenciada antes da [ação CostInitialize.](costinitialize-action.md) Chame a [ação FileCost](filecost-action.md) imediatamente após a ação CostInitialize e, em seguida, chame a ação CostFinalize para disponibilizar todos os cálculos de custo finais para o instalador por meio da [tabela Componente.](component-table.md)

A ação CostFinalize deve ser executada antes de iniciar qualquer sequência [](feature-table.md) de interface do usuário que permita ao usuário exibir ou modificar diretórios ou seleções de tabela de recursos.

## <a name="actiondata-messages"></a>Mensagens ActionData

Não há mensagens ActionData.

## <a name="remarks"></a>Comentários

A ação CostFinalize consulta a [tabela Condição](condition-table.md) para determinar quais recursos estão agendados para serem instalados. O custo é feito para cada componente na [tabela Componente.](component-table.md)

A ação CostFinalize também verifica se todos os diretórios de destino podem ser escritos antes de permitir que a instalação continue.

> [!Note]  
> Durante uma [instalação administrativa,](administrative-installation.md)CostFinalize define todos os recursos para instalação, exceto recursos que têm 0 autor na coluna Nível da [tabela Recurso](feature-table.md).

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Custo do arquivo](file-costing.md)
</dt> </dl>

 

 



