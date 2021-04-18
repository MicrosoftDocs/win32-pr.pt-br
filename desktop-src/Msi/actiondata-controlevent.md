---
description: O instalador usa esse evento para publicar dados na ação mais recente. Os dados podem ser exibidos em uma caixa de diálogo por um controle de texto que assina esse ControlEvent,. Esse evento deve ser criado na tabela EventMappings.
ms.assetid: 3c0ab7d0-35f2-4966-8eff-f9f0419d8eed
title: ActionData ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13bbfe27a59dbe0eda27e7a24e654711d1999188
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105780966"
---
# <a name="actiondata-controlevent"></a>ActionData ControlEvent,

O instalador usa esse evento para publicar dados na ação mais recente. Os dados podem ser exibidos em uma caixa de diálogo por um [controle de texto](text-control.md) que assina esse ControlEvent,. Esse evento deve ser criado na [tabela EventMappings](eventmapping-table.md).

Esse ControlEvent, pode ser manipulado por uma interface do usuário executada na [*interface da usuário básica*](b-gly.md), na [*IU reduzida*](r-gly.md)ou em níveis [*completos da interface*](f-gly.md) de usuários. Para obter informações sobre níveis de interface do usuário, consulte [níveis de interface de usuários](user-interface-levels.md).

## <a name="published-by"></a>Publicada por

Esse ControlEvent, é publicado pelo instalador.

## <a name="argument"></a>Argumento

Este ControlEvent, não usa um argumento.

## <a name="action-on-subscribers"></a>Ação nos assinantes

Os assinantes ficam ocultos quando uma nova ação é iniciada e mostrada quando novos dados de ação chegam do instalador.

## <a name="typical-use"></a>Usos comum

Um [controle de texto](text-control.md) em uma caixa de diálogo sem janela restrita assina esse evento por meio da [tabela EventMappings](eventmapping-table.md). O [atributo controle de texto](text-control-attribute.md) é listado no campo atributos desta tabela para receber os dados de ação atuais. Normalmente usado para exibir os nomes dos arquivos copiados durante a cópia do arquivo.

 

 



