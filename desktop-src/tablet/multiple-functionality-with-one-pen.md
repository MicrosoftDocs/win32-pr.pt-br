---
description: Uma caneta tablet pc pode ter mais de uma extremidade que pode interagir com o digitalizador.
ms.assetid: c1aa0d65-cfea-4720-ad09-7add724e03c7
title: Várias funcionalidades com uma caneta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22cbba4c95ef215b8ae1e0c94cbe1d43eaceb966fd775284c57a365bbba2f7fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118449667"
---
# <a name="multiple-functionality-with-one-pen"></a>Várias funcionalidades com uma caneta

Uma caneta tablet pc pode ter mais de uma extremidade que pode interagir com o digitalizador. Se ambas as extremidades da caneta puderem gerar eventos, uma extremidade poderá ser usada para colocar tinta, selecionar e apontar e a outra extremidade pode ser usada para outras funções, como apagamento.

Para implementar essa funcionalidade, seu aplicativo deve ser capaz de determinar qual extremidade da caneta está sendo usada e, portanto, quando alterar a aparência do cursor. Ele pode fazer isso procurando o estado da propriedade [**Invertida**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_inverted) no [**objeto Cursor.**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)

Para obter detalhes específicos sobre como usar a parte traseira da caneta para apagar, consulte [Apagando tinta com a caneta](erasing-ink-with-the-pen.md). Além disso, o [exemplo de apagamento de](ink-erasing-sample.md) tinta demonstra como usar a parte traseira da caneta para apagar a tinta.

 

 



