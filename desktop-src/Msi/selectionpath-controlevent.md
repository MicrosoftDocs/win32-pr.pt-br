---
description: O controle SelectionTree usa o evento SelectionPath para publicar o caminho do item realçado.
ms.assetid: 755e5bf2-42c4-4213-9bb7-4f15ad22041f
title: SelectionPath ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f45dfcb017c18b026f03bf9fa9b89d7be33db49bafc3dd9f899846cbada1047
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040436"
---
# <a name="selectionpath-controlevent"></a>SelectionPath ControlEvent

O [controle SelectionTree](selectiontree-control.md) usa o evento SelectionPath para publicar o caminho do item realçado. Se o item for selecionado para ser executado da origem, esse será o caminho da origem. Se o item for selecionado como ausente, a cadeia de caracteres será a cadeia de caracteres **AbsentPath** da [tabela UIText](uitext-table.md). Esse evento deve ser autor na [tabela EventMapping](eventmapping-table.md).

Esse ControlEvent exige que a interface do usuário seja executado no [*nível completo da interface do*](f-gly.md) usuário. Esse evento não funcionará com uma interface [*do usuário reduzida ou*](r-gly.md) interface do usuário [*básica.*](b-gly.md) Para obter informações, consulte [Interface do Usuário níveis .](user-interface-levels.md)

Esse evento só pode afetar controles localizados na mesma caixa de diálogo que o controle SelectionTree.

## <a name="published-by"></a>Publicada por

[SelectionTree](selectiontree-control.md)

## <a name="argument"></a>Argumento

Nenhum.

## <a name="action-on-subscribers"></a>Ação em Assinantes

Nenhum.

## <a name="typical-use"></a>Usos comum

Um [controle](text-control.md) Texto na mesma caixa de diálogo modal que SelectionTree deve assinar o evento por meio da [tabela EventMapping](eventmapping-table.md). O Controle de Texto exibe o caminho do item realçado.

 

 



