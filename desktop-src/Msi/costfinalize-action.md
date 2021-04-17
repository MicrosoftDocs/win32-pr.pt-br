---
description: A ação CostFinalize encerra o processo de custo de instalação interno iniciado pela ação CostInitialize.
ms.assetid: ae69ad03-5acc-4a62-ba71-3a4e477d34ab
title: Ação CostFinalize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72a5423f1050f9c9d755d33e492b9b65cfcaa08b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105755087"
---
# <a name="costfinalize-action"></a>Ação CostFinalize

A ação CostFinalize encerra o processo de [*custo*](c-gly.md) de instalação interno iniciado pela ação [CostInitialize](costinitialize-action.md) .

## <a name="sequence-restrictions"></a>Restrições de sequência

Todas as ações padrão ou [personalizadas](custom-actions.md) que afetam o custo devem ser sequenciadas antes da ação [CostInitialize](costinitialize-action.md) . Chame a ação [filecost](filecost-action.md) imediatamente após a ação CostInitialize e, em seguida, chame a ação CostFinalize para disponibilizar todos os cálculos de custo final para o instalador por meio da tabela de [componentes](component-table.md) .

A ação CostFinalize deve ser executada antes de iniciar qualquer sequência de interface do usuário que permita ao usuário exibir ou modificar as seleções ou diretórios de tabela de [recursos](feature-table.md) .

## <a name="actiondata-messages"></a>Mensagens ActionData

Não há nenhuma mensagem ActionData.

## <a name="remarks"></a>Comentários

A ação CostFinalize consulta a tabela de [condição](condition-table.md) para determinar quais recursos estão agendados para instalação. O custo é feito para cada componente na tabela de [componentes](component-table.md) .

A ação CostFinalize também verifica se todos os diretórios de destino são graváveis antes de permitir que a instalação continue.

> [!Note]  
> Durante uma [instalação administrativa](administrative-installation.md), o CostFinalize define todos os recursos para instalação, exceto os recursos com 0 criados na coluna nível da [tabela de recursos](feature-table.md).

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Custo do arquivo](file-costing.md)
</dt> </dl>

 

 



