---
description: O instalador usa esse evento para publicar o nome da ação atual. O nome pode ser exibido em uma caixa de diálogo por um controle de texto que assina esse ControlEvent,. Esse evento deve ser criado na tabela EventMappings.
ms.assetid: 2b4928fe-2d5c-46c1-8a31-cbebbc78d304
title: ActionText ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: caf03829818ea7ce7732ca5f51f1710a11e8d07f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921532"
---
# <a name="actiontext-controlevent"></a>ActionText ControlEvent,

O instalador usa esse evento para publicar o nome da ação atual. O nome pode ser exibido em uma caixa de diálogo por um [controle de texto](text-control.md) que assina esse ControlEvent,. Esse evento deve ser criado na [tabela EventMappings](eventmapping-table.md).

Esse ControlEvent, pode ser manipulado por uma interface do usuário executada na [*interface da usuário básica*](b-gly.md), na [*IU reduzida*](r-gly.md)ou em níveis [*completos da interface*](f-gly.md) de usuários. Para obter informações sobre níveis de interface do usuário, consulte [níveis de interface de usuários](user-interface-levels.md).

## <a name="published-by"></a>Publicada por

Esse ControlEvent, é publicado pelo instalador.

## <a name="argument"></a>Argumento

Este ControlEvent, não usa um argumento.

## <a name="action-on-subscribers"></a>Ação nos assinantes

Os assinantes são mostrados quando novos dados de progresso chegam do instalador.

## <a name="typical-use"></a>Usos comum

Um [controle de texto](text-control.md) em uma caixa de diálogo sem janela restrita assina esse evento por meio da [tabela EventMappings](eventmapping-table.md). O [atributo de controle de texto](text-control-attribute.md) deve estar listado no campo atributos desta tabela para receber o nome da ação atual.

 

 



