---
description: O instalador usa o evento setProgress para publicar informações sobre o progresso da instalação.
ms.assetid: be597c90-7222-4542-b0f7-e9f4cdfc08b9
title: ControlEvent, de reprogress
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22e36ecf5851713d7460f8f249b77871439c628f2adfce516aea29db52ad7942
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118625076"
---
# <a name="setprogress-controlevent"></a>ControlEvent, de reprogress

O instalador usa o evento setProgress para publicar informações sobre o progresso da instalação. Um [controle ProgressBar](progressbar-control.md) ou um [controle de mensagem](billboard-control.md) deve assinar o evento por meio da [tabela EventMappings](eventmapping-table.md) , nomeando a ação cujo progresso está sendo indicado. Esse evento deve ser criado na [tabela EventMappings](eventmapping-table.md).

Esse ControlEvent, pode ser manipulado por uma interface do usuário executada na [*interface da usuário básica*](b-gly.md), na [*IU reduzida*](r-gly.md)ou em níveis [*completos da interface*](f-gly.md) de usuários. Para obter informações sobre níveis de interface do usuário, consulte [níveis de interface de usuários](user-interface-levels.md).

## <a name="published-by"></a>Publicada por

Esse ControlEvent, é publicado pelo instalador.

## <a name="argument"></a>Argumento

Nenhum.

## <a name="action-on-subscribers"></a>Ação nos assinantes

Nenhum.

## <a name="typical-use"></a>Usos comum

Um controle [ProgressBar](progressbar-control.md) em uma caixa de diálogo sem janela restrita assina esse evento usando o atributo [Progress](progress-control-attribute.md) para receber as informações de progresso.

 

 



