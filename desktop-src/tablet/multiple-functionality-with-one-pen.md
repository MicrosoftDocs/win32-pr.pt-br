---
description: Uma caneta do Tablet PC pode ter mais de uma extremidade que possa interagir com o digitalizador.
ms.assetid: c1aa0d65-cfea-4720-ad09-7add724e03c7
title: Várias funcionalidades com uma caneta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8313e6a13cb48900e0c0d31c2e1e590e07df6c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297625"
---
# <a name="multiple-functionality-with-one-pen"></a>Várias funcionalidades com uma caneta

Uma caneta do Tablet PC pode ter mais de uma extremidade que possa interagir com o digitalizador. Se ambas as extremidades da caneta puderem gerar eventos, uma extremidade poderá ser usada para definir a tinta, selecionar e apontar, e a outra extremidade poderá ser usada para outras funções, como apagar.

Para implementar essa funcionalidade, seu aplicativo deve ser capaz de determinar qual extremidade da caneta está sendo usada e, portanto, quando alterar a aparência do cursor. Isso pode fazer isso procurando o estado da propriedade [**invertida**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_inverted) no objeto [**cursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) .

Para obter detalhes específicos sobre como usar a parte traseira da caneta para apagar, consulte [apagando a tinta com a caneta](erasing-ink-with-the-pen.md). Além disso, o [exemplo de apagamento de tinta](ink-erasing-sample.md) demonstra como usar a parte traseira da caneta para apagar a tinta.

 

 



