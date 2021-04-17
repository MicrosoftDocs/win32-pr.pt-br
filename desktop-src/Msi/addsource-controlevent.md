---
description: Esse evento notifica o instalador, enquanto mantém a caixa de diálogo presente em execução, que um recurso ou todos os recursos devem ser executados da origem.
ms.assetid: fd8d6433-87cc-4544-9f4f-57a90e5f2ea5
title: ControlEvent, addsource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7441fb6cdf10abf25798c5e56405b6b4eab11b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105754651"
---
# <a name="addsource-controlevent"></a>ControlEvent, addsource

Esse evento notifica o instalador, enquanto mantém a caixa de diálogo presente em execução, que um recurso ou todos os recursos devem ser executados da origem. Esse evento pode ser publicado por um [controle de pressão](pushbutton-control.md), [controle de caixa de seleção](checkbox-control.md)ou um [controle SelectionTree](selectiontree-control.md). Esse evento deve ser criado na [tabela ControlEvent,](controlevent-table.md).

Este ControlEvent, requer que a interface do usuário seja executada no nível [*completo da interface do*](f-gly.md) usuário. Esse evento não funcionará com uma interface [*do usuário reduzida*](r-gly.md) ou uma [*interface do usuário básica*](b-gly.md). Para obter informações, consulte [níveis de interface do usuário](user-interface-levels.md).

## <a name="published-by"></a>Publicada por

Esse ControlEvent, é publicado pelo instalador.

## <a name="argument"></a>Argumento

Uma cadeia de caracteres, o nome do recurso ou "todos".

## <a name="action-on-subscribers"></a>Ação nos assinantes

Este ControlEvent, não executa uma ação nos assinantes.

## <a name="typical-use"></a>Usos comum

Um controle de [pressão](pushbutton-control.md) em uma caixa de diálogo modal está vinculado a esse evento e usado para notificar o instalador sem interromper a caixa de diálogo.

 

 



