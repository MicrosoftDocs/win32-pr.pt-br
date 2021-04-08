---
title: Propriedades de controle do agente
description: Propriedades de controle do agente
ms.assetid: e6a5b2db-9abf-4988-be41-fc7f4530507f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f5e80b10469e7e256b1b2bf3bcf55fb5a8a08b5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005077"
---
# <a name="agent-control-properties"></a><span data-ttu-id="72dc1-103">Propriedades de controle do agente</span><span class="sxs-lookup"><span data-stu-id="72dc1-103">Agent Control Properties</span></span>

<span data-ttu-id="72dc1-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="72dc1-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="72dc1-105">As propriedades a seguir são acessadas diretamente do controle do agente:</span><span class="sxs-lookup"><span data-stu-id="72dc1-105">The following properties are directly accessed from the Agent control:</span></span>

-   [<span data-ttu-id="72dc1-106">**Conectado**</span><span class="sxs-lookup"><span data-stu-id="72dc1-106">**Connected**</span></span>](connected-property.md)
-   [<span data-ttu-id="72dc1-107">**Nome**</span><span class="sxs-lookup"><span data-stu-id="72dc1-107">**Name**</span></span>](name-property-a.md)
-   [<span data-ttu-id="72dc1-108">**RaiseRequestErrors**</span><span class="sxs-lookup"><span data-stu-id="72dc1-108">**RaiseRequestErrors**</span></span>](raiserequesterrors-property.md)

<span data-ttu-id="72dc1-109">Além disso, alguns ambientes de programação podem atribuir propriedades adicionais em tempo de design ou em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="72dc1-109">In addition, some programming environments may assign additional design-time or run-time properties.</span></span> <span data-ttu-id="72dc1-110">Por exemplo, Visual Basic adiciona as propriedades Left, index, Tag e Top que definem o local do controle em um formulário, mesmo que o controle não apareça na página do formulário em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="72dc1-110">For example, Visual Basic adds Left, Index, Tag, and Top properties that define the location of the control on a form even though the control does not appear on the form's page at run time.</span></span>

<span data-ttu-id="72dc1-111">A propriedade suspensa ainda tem suporte para compatibilidade com versões anteriores, mas sempre retorna **false** porque o servidor não dá mais suporte a um estado suspenso.</span><span class="sxs-lookup"><span data-stu-id="72dc1-111">The Suspended property is still supported for backward compatibility, but always returns **False** because the server no longer supports a suspended state.</span></span>

 

 




