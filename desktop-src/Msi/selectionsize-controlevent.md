---
description: O controle SelectionTree usa o evento SelectionSize para publicar o tamanho do item realçado.
ms.assetid: 1ef161b6-f127-45ad-a312-d2adcb5124ef
title: SelectionSize ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c11829661f0120fa5906a04f081e6c979b37180
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169841"
---
# <a name="selectionsize-controlevent"></a>SelectionSize ControlEvent,

O [controle SelectionTree](selectiontree-control.md) usa o evento SelectionSize para publicar o tamanho do item realçado. Se for um item pai, o número de filhos selecionados também será publicado. A cadeia de caracteres é uma das cadeias de **SelChildCostPos**, **SelChildCostNeg**, **SelParentCostPosPos**, **SelParentCostPosNeg**, **SelParentCostNegPos** ou **SelParentCostNegNeg** da [tabela UIText](uitext-table.md). Esse evento deve ser criado na [tabela EventMappings](eventmapping-table.md).

Este ControlEvent, requer que a interface do usuário seja executada no nível [*completo da interface do*](f-gly.md) usuário. Esse evento não funcionará com uma interface [*do usuário reduzida*](r-gly.md) ou uma [*interface do usuário básica*](b-gly.md). Para obter informações, consulte [níveis de interface do usuário](user-interface-levels.md).

Esse evento só pode afetar controles que estão localizados na mesma caixa de diálogo que o controle SelectionTree.

## <a name="published-by"></a>Publicada por

[SelectionTree](selectiontree-control.md)

## <a name="argument"></a>Argumento

Nenhum.

## <a name="action-on-subscribers"></a>Ação nos assinantes

Nenhum.

## <a name="typical-use"></a>Usos comum

Um controle de [texto](text-control.md) na mesma caixa de diálogo modal que o controle SelectionTree por meio da [tabela EventMappings](eventmapping-table.md). O controle de texto usa esse evento para exibir o tamanho do item realçado.

 

 



