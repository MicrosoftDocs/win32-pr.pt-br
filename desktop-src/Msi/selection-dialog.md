---
description: Essa caixa de diálogo modal permite que os usuários selecionem itens específicos.
ms.assetid: 76e0f369-839e-4dc0-bb42-c48dbf1511f3
title: Caixa de diálogo de seleção
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9d5a6b8700bbbdefe2bd1b2270797b34b0cebfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105751631"
---
# <a name="selection-dialog"></a>Caixa de diálogo de seleção

Essa caixa de diálogo modal permite que os usuários selecionem itens específicos.

Uma caixa de diálogo de seleção contém um [controle SelectionTree](selectiontree-control.md) que publica vários ControlEvents. Normalmente, esses ControlEvents são assinados por [texto](text-control.md), [ícone](icon-control.md)ou controles de [bitmap](bitmap-control.md) que exibem uma descrição, o tamanho, o caminho e o ícone do item realçado.

Há um [controle de pressão](pushbutton-control.md) na caixa de diálogo que publica o [SelectionBrowse ControlEvent,](selectionbrowse-controlevent.md) e gera uma caixa de [diálogo de procura](browse-dialog.md). O controle procurar permite que o usuário selecione um diretório.

A árvore de seleção é preenchida somente depois que a [ação CostInitialize](costinitialize-action.md) e a [ação CostFinalize](costfinalize-action.md) são chamadas.

Uma caixa de diálogo de seleção é normalmente usada para selecionar recursos. Os recursos são listados como itens em um controle SelectionTree e rotulados com a cadeia de caracteres curta do texto que aparece na coluna título da [tabela de recursos](feature-table.md). A cadeia de texto na coluna Descrição da tabela de recursos é publicada como uma [SelectionDescription ControlEvent,](selectiondescription-controlevent.md) e exibida por um [controle de texto](text-control.md) na caixa de diálogo seleção. O controle de árvore de seleção também publica o identificador para o ícone do item realçado.

 

 



