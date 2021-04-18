---
description: O SpawnDialog ControlEvent, notifica o instalador para criar um filho de uma caixa de diálogo modal enquanto mantém a caixa de diálogo presente em execução.
ms.assetid: 2a341039-60dd-4e6c-9ef3-bf482ca53917
title: SpawnDialog ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71aec632332a87d047913b618aa2c39843849e5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105758761"
---
# <a name="spawndialog-controlevent"></a>SpawnDialog ControlEvent,

O SpawnDialog ControlEvent, notifica o instalador para criar um filho de uma caixa de diálogo modal enquanto mantém a caixa de diálogo presente em execução.

Esse evento pode ser publicado por um [controle de pressão](pushbutton-control.md)ou um [controle SelectionTree](selectiontree-control.md). Esse evento deve ser criado na [tabela ControlEvent,](controlevent-table.md).

Este ControlEvent, requer que a interface do usuário seja executada no nível [*completo da interface do*](f-gly.md) usuário. Esse evento não funcionará com uma interface [*do usuário reduzida*](r-gly.md) ou uma [*interface do usuário básica*](b-gly.md). Para obter informações, consulte [níveis de interface do usuário](user-interface-levels.md).

## <a name="published-by"></a>Publicada por

Esse ControlEvent, é publicado pelo instalador.

## <a name="argument"></a>Argumento

Uma cadeia de caracteres que é o nome da nova caixa de diálogo.

## <a name="action-on-subscribers"></a>Ação nos assinantes

Nenhum.

## <a name="typical-use"></a>Usos comum

Um controle de [pressão](pushbutton-control.md) em uma caixa de diálogo modal está vinculado a esse evento na tabela [ControlEvent,](controlevent-table.md) para criar uma caixa de diálogo filho, como "tem certeza de que deseja cancelar?" .

 

 



