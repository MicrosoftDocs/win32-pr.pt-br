---
title: Fazendo uma chamada de procedimento remoto
description: Depois que o programa cliente de aplicativos distribuídos que usa identificadores de ligação explícitos tem um identificador de associação, ele pode executar procedimentos remotos.
ms.assetid: f424bb01-e562-49eb-abaf-cc2d76a6ad8f
keywords:
- Chamada de procedimento remoto RPC, tarefas, fazendo uma chamada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a97095d7eda8227f2369f5e3776faf8ce04c22f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103634796"
---
# <a name="making-a-remote-procedure-call"></a>Fazendo uma chamada de procedimento remoto

Depois que o programa cliente de aplicativos distribuídos que usa identificadores de ligação explícitos tem um identificador de associação, ele pode executar procedimentos remotos.

O Microsoft RPC também oferece identificadores de ligação personalizados, identificadores de associação implícitos e identificadores de ligação automática. Esses identificadores de ligação oferecem aos programas cliente e servidor diferentes níveis de controle sobre o processo de execução de procedimentos remotos. Para obter detalhes sobre os diferentes tipos de identificador e a flexibilidade que eles oferecem, consulte [associação e identificadores](binding-and-handles.md).

Para executar a chamada de procedimento remotamente, chame a função de stub do lado do cliente da mesma maneira que qualquer função de C é chamada.

 

 




