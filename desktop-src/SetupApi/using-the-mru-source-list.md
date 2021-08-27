---
description: A função SetupSetSourceList será aberta ou criará uma lista de origem no sistema de usuários.
ms.assetid: cda632cf-6c92-48fb-aef1-25b320affd3e
title: Usando a lista de origem MRU
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ada1fa55a1c0defea2f344200eb331b8031dedfa66336510fb55b6fb77213a24
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100626"
---
# <a name="using-the-mru-source-list"></a>Usando a lista de origem MRU

A função [**SetupSetSourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupsetsourcelista) será aberta ou criará uma lista de origem no sistema do usuário. Você pode especificar para definir a lista de usuários, a lista do sistema, uma combinação das listas de usuários e do sistema ou uma lista temporária como a lista de origem do MRU. Se uma lista temporária for usada, ela será a única lista disponível para o aplicativo de instalação até que [**SetupCancelTemporarySourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupcanceltemporarysourcelist) seja chamado ou **SetupSetSourceList** seja chamado uma segunda vez.

Depois que uma lista é definida, você pode consultar a lista de origem usando [**SetupQuerySourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupquerysourcelista) para obter uma matriz dos caminhos de origem. Quando a matriz da lista de origem não for mais necessária, você deverá chamar a função [**SetupFreeSourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupfreesourcelista) para liberar os recursos alocados pelo [**SetupQuerySourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupquerysourcelista).

Para adicionar um caminho a uma lista de origem, seja um que seja residente no sistema do usuário ou uma lista temporária, chame [**SetupAddToSourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddtosourcelista). Se a lista de origem especificada não for temporária, essa fonte permanecerá no sistema do usuário e poderá ser acessada por instalações subsequentes.

Para remover um caminho do caminho de origem, chame a função [**SetupRemoveFromSourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupremovefromsourcelista) .

 

 



