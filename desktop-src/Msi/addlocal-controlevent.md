---
description: Esse evento notifica o instalador, mantendo a caixa de diálogo atual em execução, de que um recurso ou todos os recursos devem ser executados localmente.
ms.assetid: 074f347e-37d3-4365-a25d-caa0392a0dbc
title: AddLocal ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfb2db93bea39d167d5b8f08af2cdecfcb07194fb68d4c1e39f5511e2a09f8c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118639540"
---
# <a name="addlocal-controlevent"></a>AddLocal ControlEvent

Esse evento notifica o instalador, mantendo a caixa de diálogo atual em execução, de que um recurso ou todos os recursos devem ser executados localmente. Esse evento pode ser publicado por um [controle PushButton,](pushbutton-control.md)controle [checkbox](checkbox-control.md)ou um [controle SelectionTree](selectiontree-control.md). Esse evento deve ser autor na [tabela ControlEvent](controlevent-table.md).

Esse ControlEvent exige que a interface do usuário seja executado no [*nível completo da interface do*](f-gly.md) usuário. Esse evento não funcionará com uma interface [*do usuário reduzida ou*](r-gly.md) interface do usuário [*básica.*](b-gly.md) Para obter informações, consulte [Interface do Usuário níveis .](user-interface-levels.md)

## <a name="published-by"></a>Publicada por

Este ControlEvent é publicado pelo instalador.

## <a name="argument"></a>Argumento

Uma cadeia de caracteres, o nome do recurso ou "ALL".

## <a name="action-on-subscribers"></a>Ação em Assinantes

Este ControlEvent não executa uma ação em assinantes.

## <a name="typical-use"></a>Usos comum

Um [controle PushButton](pushbutton-control.md) em uma caixa de diálogo modal é vinculado a esse evento e usado para notificar o instalador sem interromper a caixa de diálogo.

 

 



