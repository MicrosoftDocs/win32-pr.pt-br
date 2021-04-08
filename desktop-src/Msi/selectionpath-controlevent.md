---
description: O controle SelectionTree usa o evento SelectionPath para publicar o caminho para o item realçado.
ms.assetid: 755e5bf2-42c4-4213-9bb7-4f15ad22041f
title: SelectionPath ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8314b12d14e10ccf96c7db9db32e63172050c0bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103921906"
---
# <a name="selectionpath-controlevent"></a>SelectionPath ControlEvent,

O [controle SelectionTree](selectiontree-control.md) usa o evento SelectionPath para publicar o caminho para o item realçado. Se o item for selecionado para ser executado da origem, esse será o caminho da origem. Se o item estiver selecionado como ausente, a cadeia de caracteres será a cadeia de caracteres **AbsentPath** da [tabela UIText](uitext-table.md). Esse evento deve ser criado na [tabela EventMappings](eventmapping-table.md).

Este ControlEvent, requer que a interface do usuário seja executada no nível [*completo da interface do*](f-gly.md) usuário. Esse evento não funcionará com uma interface [*do usuário reduzida*](r-gly.md) ou uma [*interface do usuário básica*](b-gly.md). Para obter informações, consulte [níveis de interface do usuário](user-interface-levels.md).

Esse evento só pode afetar controles que estão localizados na mesma caixa de diálogo que o controle SelectionTree.

## <a name="published-by"></a>Publicada por

[SelectionTree](selectiontree-control.md)

## <a name="argument"></a>Argumento

Nenhum.

## <a name="action-on-subscribers"></a>Ação nos assinantes

Nenhum.

## <a name="typical-use"></a>Usos comum

Um controle de [texto](text-control.md) na mesma caixa de diálogo modal que o SelectionTree deve assinar o evento por meio da [tabela EventMappings](eventmapping-table.md). O controle de texto exibe o caminho do item realçado.

 

 



