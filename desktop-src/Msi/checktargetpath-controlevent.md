---
description: Esse evento notifica o instalador que ele precisa verificar se o caminho selecionado é válido. Se o caminho não for válido, esse evento bloqueará ControlEvents adicionais associados ao controle.
ms.assetid: b7c1de6e-5738-4ecb-a033-9379d79dddb9
title: CheckTargetPath ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6d8ae179a3d6e0debba4cecfd620bc0cebf99361875517d944886b82ff4d55f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066056"
---
# <a name="checktargetpath-controlevent"></a>CheckTargetPath ControlEvent,

Esse evento notifica o instalador que ele precisa verificar se o caminho selecionado é válido. Se o caminho não for válido, esse evento bloqueará ControlEvents adicionais associados ao controle.

Esse evento pode ser publicado por um [controle de pressão](pushbutton-control.md)ou um [controle SelectionTree](selectiontree-control.md). Esse evento deve ser criado na [tabela ControlEvent,](controlevent-table.md).

Este ControlEvent, requer que a interface do usuário seja executada no nível [*completo da interface do*](f-gly.md) usuário. Esse evento não funcionará com uma interface [*do usuário reduzida*](r-gly.md) ou uma [*interface do usuário básica*](b-gly.md). Para obter informações, consulte [níveis de interface do usuário](user-interface-levels.md).

## <a name="published-by"></a>Publicada por

Esse ControlEvent, é publicado pelo instalador.

## <a name="argument"></a>Argumento

O nome da propriedade que contém o caminho. Se a propriedade for indireta, o nome da propriedade será colocado entre colchetes.

## <a name="action-on-subscribers"></a>Ação nos assinantes

Este ControlEvent, não executa uma ação nos assinantes.

## <a name="typical-use"></a>Usos comum

Um controle de [pressão](pushbutton-control.md) em uma caixa de diálogo de procura está vinculado a esse evento na tabela [ControlEvent,](controlevent-table.md) para verificar o caminho selecionado antes de retornar à caixa de diálogo de seleção.

 

 



