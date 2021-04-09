---
description: O filecustoaction inicia as ações de instalação padrão do Dynamic costingof.
ms.assetid: 1b3f2baf-6191-452e-955d-8ac903edc1b7
title: Ação de custo de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b9d87cb73353ef80f956ce13ec1940f1a4adee2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011875"
---
# <a name="filecost-action"></a>Ação de custo de

O filecustaaction inicia o [*custo*](c-gly.md)dinâmico das ações de instalação padrão.

## <a name="actiondata-messages"></a>Mensagens ActionData

Não há nenhuma mensagem ActionData.

## <a name="sequence-restrictions"></a>Restrições de sequência

Todas as ações padrão ou [personalizadas](custom-actions.md) que afetam o custo devem ser sequenciadas antes da ação [CostInitialize](costinitialize-action.md) . Chame a ação filecost imediatamente após a ação CostInitialize. Em seguida, chame a ação [CostFinalize](costfinalize-action.md) após a ação CostInitialize para disponibilizar todos os cálculos de custo final para o instalador por meio da tabela de [componentes](component-table.md) .

A ação [CostInitialize](costinitialize-action.md) deve ser executada antes da ação filecost. Em seguida, o instalador determina o custo de espaço em disco de cada arquivo na tabela de [arquivos](file-table.md) , em uma base por componente (consulte a [tabela de componentes](component-table.md)), levando o clustering de [*volume*](v-gly.md) e a presença de arquivos existentes que talvez precisem ser substituídos em conta. Todas as ações que consomem ou liberam espaço em disco também são consideradas. Se um arquivo existente for encontrado, uma verificação de versão de arquivo será executada para determinar se o novo arquivo realmente precisa ser instalado ou não. Se o arquivo existente for de um número de versão igual ou maior, o arquivo existente não será substituído e nenhum custo de espaço em disco será incorrido. Em todos os casos, o instalador usa os resultados da verificação de número de versão para definir o estado de instalação de cada arquivo.

A ação filecusto Inicializa o cálculo de custos com o instalador. O [*custo*](c-gly.md) dinâmico real não ocorre até que a ação [CostFinalize](costfinalize-action.md) seja executada.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Custo do arquivo](file-costing.md)
</dt> </dl>

 

 



