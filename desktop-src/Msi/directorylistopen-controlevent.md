---
description: Esse evento seleciona e realça um diretório no controle Directorylist que o usuário optou por abrir. Para obter informações relacionadas, consulte caixa de diálogo procurar.
ms.assetid: 95cdf345-e1bb-41d8-b1e0-2acf97e33110
title: DirectoryListOpen ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbeb3a570f49032adb0f5208514c26dd9cc16726
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104172338"
---
# <a name="directorylistopen-controlevent"></a>DirectoryListOpen ControlEvent,

Esse evento seleciona e realça um diretório no [controle directorylist](directorylist-control.md) que o usuário optou por abrir. Para obter informações relacionadas, consulte [caixa de diálogo Procurar](browse-dialog.md).

Esse evento deve ser publicado por um [controle de pressão](pushbutton-control.md) localizado na mesma caixa de diálogo que o controle assinando esse evento. O evento deve ser criado na [tabela ControlEvent,](controlevent-table.md).

Este ControlEvent, requer que a interface do usuário seja executada no nível [*completo da interface do*](f-gly.md) usuário. Esse evento não funcionará com uma interface [*do usuário reduzida*](r-gly.md) ou uma [*interface do usuário básica*](b-gly.md). Para obter informações, consulte [níveis de interface do usuário](user-interface-levels.md).

Se nenhum diretório tiver sido selecionado no [controle directorylist](directorylist-control.md), um evento DirectoryListOpen desabilitará quaisquer outros controles que publiquem um evento DirectoryListOpen.

## <a name="published-by"></a>Publicada por

[Directorylist](directorylist-control.md)

## <a name="argument"></a>Argumento

Este ControlEvent, não usa um argumento.

## <a name="action-on-subscribers"></a>Ação nos assinantes

Este ControlEvent, não executa nenhuma ação nos assinantes.

## <a name="typical-use"></a>Usos comum

Um controle de [pressão](pushbutton-control.md) na mesma caixa de diálogo modal que a directorylist é usado para disparar a depuração no caminho.

 

 



