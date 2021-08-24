---
description: O evento ValidateProductID define a propriedade ProductID como a ID do produto completo. Se a validação não for bem-sucedida, esse evento colocará uma mensagem de erro e uma caixa de diálogo modal para uma entrada de usuário da ID do produto.
ms.assetid: 44002cae-154a-4938-a15c-456c293e94fb
title: ValidateProductID ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68ae9ae5747deb9995c2e33a5c44541793442be8844b224c28c8a91e412cb188
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119786656"
---
# <a name="validateproductid-controlevent"></a>ValidateProductID ControlEvent,

O evento ValidateProductID define a propriedade [**ProductID**](productid.md) como a ID do produto completo. Se a validação não for bem-sucedida, esse evento colocará uma mensagem de erro e uma caixa de diálogo modal para uma entrada de usuário da ID do produto.

Esse evento pode ser publicado por um [controle de pressão](pushbutton-control.md)ou um [controle SelectionTree](selectiontree-control.md). Esse evento deve ser criado na [tabela ControlEvent,](controlevent-table.md).

Este ControlEvent, requer que a interface do usuário seja executada no nível [*completo da interface do*](f-gly.md) usuário. Esse evento não funcionará com uma interface [*do usuário reduzida*](r-gly.md) ou uma [*interface do usuário básica*](b-gly.md). Para obter informações, consulte [níveis de interface do usuário](user-interface-levels.md).

## <a name="published-by"></a>Publicada por

Esse ControlEvent, é publicado pelo instalador.

## <a name="argument"></a>Argumento

Nenhum.

## <a name="action-on-subscribers"></a>Ação nos assinantes

Nenhum.

## <a name="typical-use"></a>Usos comum

Um controle de [pressão](pushbutton-control.md) em uma caixa de diálogo modal está vinculado a esse evento e é usado para verificar a entrada do usuário da ID do produto. Se a entrada do usuário for válida, a próxima caixa de diálogo será aberta.

 

 



