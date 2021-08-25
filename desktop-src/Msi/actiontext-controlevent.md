---
description: O instalador usa esse evento para publicar o nome da ação atual. O nome pode ser exibido em uma caixa de diálogo por um Controle de Texto que assina este ControlEvent. Esse evento deve ser autor na tabela EventMapping.
ms.assetid: 2b4928fe-2d5c-46c1-8a31-cbebbc78d304
title: ActionText ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a216cb30dbcaa0be9972f12f7a83c8e45e5bb5686d93ce210bf96087aa3c4552
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119927376"
---
# <a name="actiontext-controlevent"></a>ActionText ControlEvent

O instalador usa esse evento para publicar o nome da ação atual. O nome pode ser exibido em uma caixa de diálogo por um [Controle de](text-control.md) Texto que assina este ControlEvent. Esse evento deve ser autor na [tabela EventMapping](eventmapping-table.md).

Esse ControlEvent pode ser tratado por uma interface [](r-gly.md)do usuário executado na interface do usuário [*básica,*](b-gly.md)na interface do usuário reduzida ou nos níveis de interface [*do usuário*](f-gly.md) completos. Para obter informações sobre níveis de interface do usuário, [consulte Interface do Usuário níveis de interface do usuário.](user-interface-levels.md)

## <a name="published-by"></a>Publicada por

Este ControlEvent é publicado pelo instalador.

## <a name="argument"></a>Argumento

Este ControlEvent não usa um argumento .

## <a name="action-on-subscribers"></a>Ação em Assinantes

Os assinantes são mostrados quando novos dados de progresso chegam do instalador.

## <a name="typical-use"></a>Usos comum

Um [Controle de Texto](text-control.md) em uma caixa de diálogo sem modo assina esse evento por meio da tabela [EventMapping](eventmapping-table.md). O [Atributo de Controle de](text-control-attribute.md) Texto deve ser listado no campo Atributos desta tabela para receber o nome da ação atual.

 

 



