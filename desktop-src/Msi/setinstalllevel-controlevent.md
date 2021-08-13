---
description: O evento SetInstallLevel altera o nível de instalação para o valor especificado pelo argumento .
ms.assetid: 71cfd516-4a92-446c-bd8f-a3a04dba0bb2
title: SetInstallLevel ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3e7632e666dc169318e04cbcaf979aa82432d028cc6b7230e6a5e711350ef35
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118625104"
---
# <a name="setinstalllevel-controlevent"></a>SetInstallLevel ControlEvent

O evento SetInstallLevel altera o nível de instalação para o valor especificado pelo argumento .

Esse evento pode ser publicado por um [controle PushButton ou](pushbutton-control.md)um [controle SelectionTree](selectiontree-control.md). Esse evento deve ser autor na [tabela ControlEvent](controlevent-table.md).

Esse ControlEvent exige que a interface do usuário seja executado no [*nível completo da interface do*](f-gly.md) usuário. Esse evento não funcionará com uma interface [*do usuário reduzida ou*](r-gly.md) interface do usuário [*básica.*](b-gly.md) Para obter informações, consulte [Interface do Usuário níveis .](user-interface-levels.md)

## <a name="published-by"></a>Publicada por

Este ControlEvent é publicado pelo instalador.

## <a name="argument"></a>Argumento

Um inteiro que é o novo valor do nível de instalação.

## <a name="action-on-subscribers"></a>Ação em Assinantes

Nenhum.

## <a name="typical-use"></a>Usos comum

Um [controle PushButton](pushbutton-control.md) em uma caixa de diálogo modal é vinculado a esse evento na tabela [ControlEvent](controlevent-table.md) para alterar o nível de instalação.

 

 



