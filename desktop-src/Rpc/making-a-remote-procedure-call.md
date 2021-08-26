---
title: Fazendo uma chamada de procedimento remoto
description: Depois que o programa cliente de aplicativos distribuídos que usa alças de associação explícita tiver um alçamento de associação, ele poderá executar procedimentos remotos.
ms.assetid: f424bb01-e562-49eb-abaf-cc2d76a6ad8f
keywords:
- RPC de Chamada de Procedimento Remoto , tarefas, fazendo uma chamada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8218fd99e11c65f15dbbe7a56c2ece1b93720839498352d610312a0f66f95bc5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120020076"
---
# <a name="making-a-remote-procedure-call"></a>Fazendo uma chamada de procedimento remoto

Depois que o programa cliente de aplicativos distribuídos que usa alças de associação explícita tiver um alçamento de associação, ele poderá executar procedimentos remotos.

O Microsoft RPC também oferece alças de associação personalizadas, alças de associação implícitas e alças de associação automática. Esses alças de associação oferecem programas de cliente e servidor diferentes níveis de controle sobre o processo de execução de procedimentos remotos. Para obter detalhes sobre diferentes tipos de alça e a flexibilidade que eles oferecem, consulte [Associação e alças.](binding-and-handles.md)

Para executar a chamada de procedimento remotamente, chame a função stub do lado do cliente da mesma maneira que qualquer função C é chamada.

 

 




