---
description: Esse evento seleciona e realça um diretório no controle DirectoryList que o usuário optou por abrir. Para obter informações relacionadas, consulte Caixa de diálogo Procurar.
ms.assetid: 95cdf345-e1bb-41d8-b1e0-2acf97e33110
title: DirectoryListOpen ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b1453ffd42e0763ec747f02f7030818eaba3d533e5dfcca4570c13596efdcb1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118947320"
---
# <a name="directorylistopen-controlevent"></a>DirectoryListOpen ControlEvent

Esse evento seleciona e realça um diretório no controle [DirectoryList](directorylist-control.md) que o usuário optou por abrir. Para obter informações relacionadas, consulte [Caixa de diálogo Procurar](browse-dialog.md).

Esse evento deve ser publicado por um [Controle PushButton](pushbutton-control.md) localizado na mesma caixa de diálogo que o controle que assina esse evento. O evento deve ser autor na [tabela ControlEvent](controlevent-table.md).

Esse ControlEvent exige que a interface do usuário seja executado no [*nível completo da interface do*](f-gly.md) usuário. Esse evento não funcionará com uma interface [*do usuário reduzida ou*](r-gly.md) interface do usuário [*básica.*](b-gly.md) Para obter informações, consulte [Interface do Usuário níveis](user-interface-levels.md).

Se nenhum diretório tiver sido selecionado no controle [DirectoryList](directorylist-control.md), um evento DirectoryListOpen desabilitará todos os outros controles que publicam um evento DirectoryListOpen.

## <a name="published-by"></a>Publicada por

[DirectoryList](directorylist-control.md)

## <a name="argument"></a>Argumento

Este ControlEvent não usa um argumento .

## <a name="action-on-subscribers"></a>Ação em Assinantes

Este ControlEvent não executa nenhuma ação em assinantes.

## <a name="typical-use"></a>Usos comum

Um [controle PushButton](pushbutton-control.md) na mesma caixa de diálogo modal que a DirectoryList é usado para disparar a reação no caminho.

 

 



