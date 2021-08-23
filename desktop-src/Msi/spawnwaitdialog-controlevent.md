---
description: O ControlEvent, SpawnWaitDialog aciona a caixa de diálogo especificada pela coluna Argument da tabela ControlEvent,, se a expressão na coluna condição for avaliada como FALSE.
ms.assetid: 38a5d896-2c11-4ce9-b829-104a882723b6
title: SpawnWaitDialog ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffeddfcb46f67d292de81a5a8195ba17c2a63b305be229ae96b2133448d41f00
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119628006"
---
# <a name="spawnwaitdialog-controlevent"></a>SpawnWaitDialog ControlEvent,

O ControlEvent, SpawnWaitDialog aciona a caixa de diálogo especificada pela coluna Argument da [tabela ControlEvent,](controlevent-table.md), se a expressão na coluna condição for avaliada como false. A caixa de diálogo permanece ativa por enquanto a expressão condicional permanece falsa e é removida assim que a condição é avaliada como TRUE.

Esse evento pode ser publicado por um [controle de pressão](pushbutton-control.md)ou um [controle SelectionTree](selectiontree-control.md). Esse evento deve ser criado na [tabela ControlEvent,](controlevent-table.md).

Este ControlEvent, requer que a interface do usuário seja executada no nível [*completo da interface do*](f-gly.md) usuário. Esse evento não funcionará com uma interface [*do usuário reduzida*](r-gly.md) ou uma [*interface do usuário básica*](b-gly.md). Para obter informações, consulte [níveis de interface do usuário](user-interface-levels.md).

## <a name="published-by"></a>Publicada por

Esse ControlEvent, é publicado pelo instalador.

## <a name="argument"></a>Argumento

Uma caixa de diálogo na [tabela de diálogo](dialog-table.md).

## <a name="action-on-subscribers"></a>Ação nos assinantes

Nenhum.

## <a name="typical-use"></a>Usos comum

O SpawnWaitDialog ControlEvent, pode ser usado para aguardar qualquer tarefa em segundo plano a conclusão do que pode ser testada usando uma expressão condicional, como o estado de uma propriedade. Para obter um exemplo de como usar o SpawnWaitDialog ControlEvent,, consulte a seção [criando uma condicional "Aguarde...". Caixa de mensagem](authoring-a-conditional-please-wait-------message-box.md).

 

 



