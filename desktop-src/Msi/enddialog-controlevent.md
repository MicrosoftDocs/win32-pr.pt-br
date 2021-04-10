---
description: Esse evento notifica o instalador para remover uma caixa de diálogo modal. Em todos os casos, o instalador remove a caixa de diálogo atual.
ms.assetid: 74a28696-6387-4d62-8955-4708ba5872bb
title: EndDialog ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f08449bffe29093e32066e92e1b8fc739efa02d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169862"
---
# <a name="enddialog-controlevent"></a>EndDialog ControlEvent,

Esse evento notifica o instalador para remover uma caixa de diálogo modal. Em todos os casos, o instalador remove a caixa de diálogo atual.

Esse evento pode ser publicado por um [controle de pressão](pushbutton-control.md)ou um [controle SelectionTree](selectiontree-control.md). Esse evento deve ser criado na [tabela ControlEvent,](controlevent-table.md).

Este ControlEvent, requer que a interface do usuário seja executada no nível [*completo da interface do*](f-gly.md) usuário. Esse evento não funcionará com uma interface [*do usuário reduzida*](r-gly.md) ou uma [*interface do usuário básica*](b-gly.md). Para obter informações, consulte [níveis de interface do usuário](user-interface-levels.md).

A tabela a seguir lista a ação do evento resultante de diferentes argumentos inseridos na [tabela ControlEvent,](controlevent-table.md).



| Argumento | Ação do instalador                                                                                                                                                             |
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Fechar     | A sequência do assistente é fechada e o controle retorna para o instalador com o valor UserExit. Esse argumento não pode ser usado em uma caixa de diálogo que seja filho de outra caixa de diálogo. |
| Tentar novamente    | A sequência do assistente é fechada e o controle retorna ao instalador com o valor de suspensão. Esse argumento não pode ser usado em uma caixa de diálogo que seja filho de outra caixa de diálogo.  |
| Ignorar   | A sequência do assistente é fechada e o controle retorna ao instalador com o valor concluído. Esse argumento não pode ser usado em uma caixa de diálogo que seja filho de outra caixa de diálogo. |
| Retorno   | O controle retorna ao pai da caixa de diálogo atual ou, se não houver nenhum pai, o controle retornará ao instalador com o valor de êxito.                                 |



 

## <a name="published-by"></a>Publicada por

Esse ControlEvent, é publicado pelo instalador.

## <a name="argument"></a>Argumento

Em caixas de diálogo normais, a coluna Argument da [tabela ControlEvent,](controlevent-table.md) pode ser "Return", "Exit", "retry" ou "ignore".

Nas caixas de diálogo de erro, a coluna Argument da [tabela ControlEvent,](controlevent-table.md) pode ser "ErrorOk", "ErrorCancel", "ErrorAbort", "ErrorRetry", "ErrorIgnore", "ErrorYes" ou "ErrorNo".

## <a name="action-on-subscribers"></a>Ação nos assinantes

Nenhum.

## <a name="typical-use"></a>Usos comum

Um controle de [supressão](pushbutton-control.md) em uma caixa de diálogo modal está vinculado a esse evento na tabela [ControlEvent,](controlevent-table.md) para fechar um diálogo.

 

 



