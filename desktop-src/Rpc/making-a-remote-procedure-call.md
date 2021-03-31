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
# <a name="making-a-remote-procedure-call"></a><span data-ttu-id="5cfef-104">Fazendo uma chamada de procedimento remoto</span><span class="sxs-lookup"><span data-stu-id="5cfef-104">Making a Remote Procedure Call</span></span>

<span data-ttu-id="5cfef-105">Depois que o programa cliente de aplicativos distribuídos que usa identificadores de ligação explícitos tem um identificador de associação, ele pode executar procedimentos remotos.</span><span class="sxs-lookup"><span data-stu-id="5cfef-105">Once the client program of distributed applications that uses explicit binding handles has a binding handle, it can execute remote procedures.</span></span>

<span data-ttu-id="5cfef-106">O Microsoft RPC também oferece identificadores de ligação personalizados, identificadores de associação implícitos e identificadores de ligação automática.</span><span class="sxs-lookup"><span data-stu-id="5cfef-106">Microsoft RPC also offers custom binding handles, implicit binding handles, and automatic binding handles.</span></span> <span data-ttu-id="5cfef-107">Esses identificadores de ligação oferecem aos programas cliente e servidor diferentes níveis de controle sobre o processo de execução de procedimentos remotos.</span><span class="sxs-lookup"><span data-stu-id="5cfef-107">These binding handles offer client and server programs different levels of control over the process of executing remote procedures.</span></span> <span data-ttu-id="5cfef-108">Para obter detalhes sobre os diferentes tipos de identificador e a flexibilidade que eles oferecem, consulte [associação e identificadores](binding-and-handles.md).</span><span class="sxs-lookup"><span data-stu-id="5cfef-108">For details on different handle types and the flexibility they offer, see [Binding and Handles](binding-and-handles.md).</span></span>

<span data-ttu-id="5cfef-109">Para executar a chamada de procedimento remotamente, chame a função de stub do lado do cliente da mesma maneira que qualquer função de C é chamada.</span><span class="sxs-lookup"><span data-stu-id="5cfef-109">To execute the procedure call remotely, call the client-side stub function in the same manner any C function is called.</span></span>

 

 




