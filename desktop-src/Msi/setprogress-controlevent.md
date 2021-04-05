---
description: O instalador usa o evento setProgress para publicar informações sobre o progresso da instalação.
ms.assetid: be597c90-7222-4542-b0f7-e9f4cdfc08b9
title: ControlEvent, de reprogress
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acd7523f03dd8fc8216991ae16b05a731e9f38f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922133"
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

 

 



