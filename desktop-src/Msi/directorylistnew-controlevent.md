---
description: Esse evento notifica o controle DirectoryList de que uma nova pasta deve ser criada; ele cria a nova pasta e seleciona o campo de nome da pasta para edição.
ms.assetid: dc5859b9-f4b4-4ed7-93d5-369a3d2b9805
title: DirectoryListNew ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 281835954c947e4bcaaf6e4e2019cbd422151e6cca39b83fa84a0abe0db010cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118378896"
---
# <a name="directorylistnew-controlevent"></a>DirectoryListNew ControlEvent

Esse evento notifica o controle [DirectoryList de](directorylist-control.md) que uma nova pasta deve ser criada; ele cria a nova pasta e seleciona o campo de nome da pasta para edição. O nome padrão da nova pasta pode ser autor na [tabela UIText](uitext-table.md). Insira "NewFolder" na coluna Chave. Insira o valor do nome padrão da nova pasta na coluna Texto. Esse valor deve estar na forma de um tipo de dados de coluna [Filename](filename.md) e usar a sintaxe LFN do \| SFN. Se esse valor não estiver presente na tabela UIText ou for um valor inválido, o instalador usará um valor padrão de "Fldr \| New Folder". Para obter informações relacionadas, consulte [Caixa de diálogo Procurar](browse-dialog.md).

Esse evento deve ser publicado por um [Controle PushButton](pushbutton-control.md) localizado na mesma caixa de diálogo que o controle que assina esse evento. O evento deve ser autor na [tabela ControlEvent](controlevent-table.md).

Esse ControlEvent exige que a interface do usuário seja executado no [*nível completo da interface do*](f-gly.md) usuário. Esse evento não funcionará com uma interface [*do usuário reduzida ou*](r-gly.md) interface do usuário [*básica.*](b-gly.md) Para obter informações, consulte [Interface do Usuário níveis de dados](user-interface-levels.md).

Observe que, se esse ControlEvent for chamado novamente quando uma nova pasta já existir, uma segunda pasta não será criada. Nesse caso, chamar DirectoryListNew seleciona o nome da nova pasta existente para edição.

## <a name="published-by"></a>Publicada por

[DirectoryList](directorylist-control.md)

## <a name="argument"></a>Argumento

Este ControlEvent não usa um argumento .

## <a name="action-on-subscribers"></a>Ação em Assinantes

Este ControlEvent não executa uma ação em assinantes.

## <a name="typical-use"></a>Usos comum

Um [controle PushButton](pushbutton-control.md) na mesma caixa de diálogo modal que a DirectoryList é usado para disparar a criação de uma nova pasta.

 

 



