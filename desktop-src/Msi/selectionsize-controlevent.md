---
description: O controle SelectionTree usa o evento SelectionSize para publicar o tamanho do item realçado.
ms.assetid: 1ef161b6-f127-45ad-a312-d2adcb5124ef
title: SelectionSize ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24c8733c0155adc085343c0a5db1a42e3aa219719babb5b342781c5bb9923ed0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040356"
---
# <a name="selectionsize-controlevent"></a>SelectionSize ControlEvent

O [controle SelectionTree](selectiontree-control.md) usa o evento SelectionSize para publicar o tamanho do item realçado. Se for um item pai, o número de filhos selecionados também será publicado. A cadeia de caracteres é uma das cadeias de caracteres **SelChildCostPos**, **SelChildCostNeg**, **SelParentCostPosPos ,** **SelParentCostNegPos** ou  **SelParentCostNegNeg da** tabela [UIText](uitext-table.md). Esse evento deve ser autor na [tabela EventMapping](eventmapping-table.md).

Esse ControlEvent exige que a interface do usuário seja executado no [*nível completo da interface do*](f-gly.md) usuário. Esse evento não funcionará com uma interface [*do usuário reduzida ou*](r-gly.md) interface do usuário [*básica.*](b-gly.md) Para obter informações, consulte [Interface do Usuário níveis .](user-interface-levels.md)

Esse evento só pode afetar controles localizados na mesma caixa de diálogo que o controle SelectionTree.

## <a name="published-by"></a>Publicada por

[SelectionTree](selectiontree-control.md)

## <a name="argument"></a>Argumento

Nenhum.

## <a name="action-on-subscribers"></a>Ação em Assinantes

Nenhum.

## <a name="typical-use"></a>Usos comum

Um [controle](text-control.md) Texto na mesma caixa de diálogo modal que o Controle SelectionTree por meio da [tabela EventMapping](eventmapping-table.md). O Controle de Texto usa esse evento para exibir o tamanho do item realçado.

 

 



