---
description: O controle SelectionTree usa o evento SelectionNoItems para excluir o texto de descrição do item obsoleto ou para desabilitar botões que se tornaram inúteis. Esse evento deve ser autor na tabela EventMapping.
ms.assetid: a79abd77-a6e5-4a1f-8a63-51644151404a
title: SelectionNoItems ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17220849c6bf50a28a0a0596bcd347e2f0a4c5af77cb53c9d9fa0041ced59abe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040456"
---
# <a name="selectionnoitems-controlevent"></a>SelectionNoItems ControlEvent

O [controle SelectionTree](selectiontree-control.md) usa o evento SelectionNoItems para excluir o texto de descrição do item obsoleto ou para desabilitar botões que se tornaram inúteis. Esse evento deve ser autor na [tabela EventMapping](eventmapping-table.md).

Esse ControlEvent exige que a interface do usuário seja executado no [*nível completo da interface do*](f-gly.md) usuário. Esse evento não funcionará com uma interface [*do usuário reduzida ou*](r-gly.md) interface do usuário [*básica.*](b-gly.md) Para obter informações, consulte [Interface do Usuário níveis .](user-interface-levels.md)

Esse evento só pode afetar controles localizados na mesma caixa de diálogo que o controle SelectionTree.

## <a name="published-by"></a>Publicada por

[Controle SelectionTree](selectiontree-control.md) se a seleção não tiver nós.

## <a name="argument"></a>Argumento

Nenhum.

## <a name="action-on-subscribers"></a>Ação em Assinantes

Exclui o texto de descrição do item obsoleto ou desabilita botões obsoletos.

## <a name="typical-use"></a>Usos comum

Pode ser usado para desabilitar os botões Next, [](selection-dialog.md) Reset e DiskCost na Caixa de Diálogo de Seleção quando uma seleção não tem nós e esses botões se tornam inúteis.

 

 



