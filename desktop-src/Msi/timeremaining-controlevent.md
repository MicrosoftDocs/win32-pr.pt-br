---
description: O instalador usa o evento timecontinueing para publicar o tempo aproximado restante, em segundos, para a sequência de progresso atual.
ms.assetid: ec5fc2b3-13a9-4681-89f0-fd39bab1de5f
title: ControlEvent, do timecontinueing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4c8978dfb7ed3be855921ad66af8554ea50972a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011672"
---
# <a name="timeremaining-controlevent"></a>ControlEvent, do timecontinueing

O instalador usa o evento timecontinueing para publicar o tempo aproximado restante, em segundos, para a sequência de progresso atual. O tempo restante pode ser exibido em uma caixa de diálogo por um [controle de texto](text-control.md) que assina esse ControlEvent,. Esse evento deve ser criado na [tabela EventMappings](eventmapping-table.md).

Esse ControlEvent, pode ser manipulado por uma interface do usuário executada na [*interface da usuário básica*](b-gly.md), na [*IU reduzida*](r-gly.md)ou em níveis [*completos da interface*](f-gly.md) de usuários. Para obter informações sobre níveis de interface do usuário, consulte [níveis de interface de usuários](user-interface-levels.md).

## <a name="published-by"></a>Publicada por

Esse ControlEvent, é publicado pelo instalador.

## <a name="argument"></a>Argumento

Nenhum.

## <a name="action-on-subscribers"></a>Ação nos assinantes

Nenhum.

## <a name="typical-use"></a>Usos comum

Um [controle de texto](text-control.md) em uma caixa de diálogo sem janela restrita assina esse evento por meio da [tabela EventMappings](eventmapping-table.md) e usa o [atributo timecontinueing](timeremaining-control-attribute.md) para exibir o tempo restante.

O mesmo controle de texto que assina para o timestart ControlEvent, também pode assinar o [ScriptInProgress ControlEvent,](scriptinprogress-controlevent.md). Nesse caso, como a cadeia de caracteres de mensagem ScriptInProgress preliminar, ela é substituída pela cadeia de caracteres "tempo restante: XX minutos".

 

 



