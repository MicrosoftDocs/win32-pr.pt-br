---
description: Esse evento notifica o instalador de que ele precisa verificar se o caminho selecionado pode ser escrito. Se o caminho não puder ser gravado, o evento bloqueará mais ControlEvents associados ao controle .
ms.assetid: 4672e2e4-a789-4050-81b9-92ec491745ac
title: CheckExistingTargetPath ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d523d04eba4ede88ca1382c17c5d40d48dadadbc9520d766b5cfca2b26b77fb5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119520186"
---
# <a name="checkexistingtargetpath-controlevent"></a>CheckExistingTargetPath ControlEvent

Esse evento notifica o instalador de que ele precisa verificar se o caminho selecionado pode ser escrito. Se o caminho não puder ser gravado, o evento bloqueará mais ControlEvents associados ao controle .

Esse evento pode ser publicado por um [controle PushButton ou](pushbutton-control.md)um [controle SelectionTree](selectiontree-control.md). Esse evento deve ser autor na [tabela ControlEvent](controlevent-table.md).

Esse ControlEvent exige que a interface do usuário seja executado no [*nível completo da interface do*](f-gly.md) usuário. Esse evento não funcionará com uma interface [*do usuário reduzida ou*](r-gly.md) interface do usuário [*básica.*](b-gly.md) Para obter informações, consulte [Interface do Usuário níveis](user-interface-levels.md).

## <a name="published-by"></a>Publicada por

Este ControlEvent é publicado pelo instalador.

## <a name="argument"></a>Argumento

O nome da propriedade que contém o caminho. Se a propriedade for indireta, o nome da propriedade será incluído entre colchetes.

## <a name="action-on-subscribers"></a>Ação em Assinantes

Este ControlEvent não executa uma ação em assinantes.

## <a name="typical-use"></a>Usos comum

Um [controle PushButton](pushbutton-control.md) em uma caixa de diálogo de navegação é vinculado a esse evento na tabela [ControlEvent](controlevent-table.md) para verificar o caminho selecionado antes de retornar à caixa de diálogo de seleção.

 

 



