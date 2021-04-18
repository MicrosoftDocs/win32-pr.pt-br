---
description: O instalador é notificado por esse evento quando um recurso ou todos os recursos são selecionados para remoção enquanto mantém a caixa de diálogo presente em execução.
ms.assetid: dabe44f7-97dd-4037-80e5-f289bab6d4b3
title: Remover ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f214330fc16704fd4eef50bc8c75fc10fc2823d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105780945"
---
# <a name="remove-controlevent"></a>Remover ControlEvent,

O instalador é notificado por esse evento quando um recurso ou todos os recursos são selecionados para remoção enquanto mantém a caixa de diálogo presente em execução.

Esse evento pode ser publicado por um [controle de pressão](pushbutton-control.md), [controle de caixa de seleção](checkbox-control.md)ou um [controle SelectionTree](selectiontree-control.md). Esse evento deve ser criado na [tabela ControlEvent,](controlevent-table.md).

Este ControlEvent, requer que a interface do usuário seja executada no nível [*completo da interface do*](f-gly.md) usuário. Esse evento não funcionará com uma interface [*do usuário reduzida*](r-gly.md) ou uma [*interface do usuário básica*](b-gly.md). Para obter informações, consulte [níveis de interface do usuário](user-interface-levels.md).

## <a name="published-by"></a>Publicada por

Esse ControlEvent, é publicado pelo instalador.

## <a name="argument"></a>Argumento

Uma cadeia de caracteres que é o nome do recurso ou "todos".

## <a name="action-on-subscribers"></a>Ação nos assinantes

Este ControlEvent, não executa uma ação nos assinantes.

## <a name="action-by-publisher-when-subscriber-activated"></a>Ação pelo Publicador quando o assinante foi ativado

O instalador mantém a caixa de diálogo presente em execução e notifica o instalador.

## <a name="typical-use"></a>Usos comum

Um controle de [pressão](pushbutton-control.md) em uma caixa de diálogo modal vinculada a este evento.

 

 



