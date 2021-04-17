---
description: O controle SelectionTree usa o evento SelectionNoItems para excluir texto de descrição de item obsoleto ou para desabilitar botões que se tornaram inúteis. Esse evento deve ser criado na tabela EventMappings.
ms.assetid: a79abd77-a6e5-4a1f-8a63-51644151404a
title: SelectionNoItems ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6544dfcaad3d22b63d71703ea95d1aa4f09a1efd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105749573"
---
# <a name="selectionnoitems-controlevent"></a>SelectionNoItems ControlEvent,

O [controle SelectionTree](selectiontree-control.md) usa o evento SelectionNoItems para excluir texto de descrição de item obsoleto ou para desabilitar botões que se tornaram inúteis. Esse evento deve ser criado na [tabela EventMappings](eventmapping-table.md).

Este ControlEvent, requer que a interface do usuário seja executada no nível [*completo da interface do*](f-gly.md) usuário. Esse evento não funcionará com uma interface [*do usuário reduzida*](r-gly.md) ou uma [*interface do usuário básica*](b-gly.md). Para obter informações, consulte [níveis de interface do usuário](user-interface-levels.md).

Esse evento só pode afetar controles que estão localizados na mesma caixa de diálogo que o controle SelectionTree.

## <a name="published-by"></a>Publicada por

[SelectionTree controle](selectiontree-control.md) se a seleção não tiver nós.

## <a name="argument"></a>Argumento

Nenhum.

## <a name="action-on-subscribers"></a>Ação nos assinantes

Exclui o texto de descrição do item obsoleto ou desabilita os botões obsoletos.

## <a name="typical-use"></a>Usos comum

Pode ser usado para desabilitar os botões Avançar, redefinir e DiskCost na caixa de [diálogo de seleção](selection-dialog.md) quando uma seleção não tem nós e esses botões se tornam inúteis.

 

 



