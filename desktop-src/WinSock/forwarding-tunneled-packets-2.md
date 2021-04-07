---
description: Há uma limitação no código que recebe pacotes encapsulados (encapsulados) e os desmultiplexa para uma interface específica.
ms.assetid: 6148fca7-adf4-460d-afd6-79c43285af6c
title: Pacotes de túnel de encaminhamento IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f95f88a90a358317cf46516808a96f93b792dd5d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827114"
---
# <a name="ipv6-forwarding-tunneled-packets"></a><span data-ttu-id="a5f38-103">Pacotes de túnel de encaminhamento IPv6</span><span class="sxs-lookup"><span data-stu-id="a5f38-103">IPv6 Forwarding Tunneled Packets</span></span>

<span data-ttu-id="a5f38-104">Há uma limitação no código que recebe pacotes encapsulados (encapsulados) e os desmultiplexa para uma interface específica.</span><span class="sxs-lookup"><span data-stu-id="a5f38-104">There is a limitation in the code that receives encapsulated (tunneled) packets and demultiplexes them to a specific interface.</span></span> <span data-ttu-id="a5f38-105">Se você quiser encaminhar pacotes encapsulados recebidos por meio de um túnel configurado, será necessário habilitar o encaminhamento em qualquer interface 6-over-4, bem como na interfaces \# 2.</span><span class="sxs-lookup"><span data-stu-id="a5f38-105">If you want to forward tunneled packets received through a configured tunnel, then it is necessary to enable forwarding on any 6-over-4 interfaces as well as interface \#2.</span></span> <span data-ttu-id="a5f38-106">Apenas habilitar o encaminhamento na interface \# 2 não funcionará.</span><span class="sxs-lookup"><span data-stu-id="a5f38-106">Just enabling forwarding on interface \#2 will not work.</span></span> <span data-ttu-id="a5f38-107">Normalmente, ao configurar um roteador, você permitiria o encaminhamento em todas as interfaces, exceto loopback.</span><span class="sxs-lookup"><span data-stu-id="a5f38-107">Typically when configuring a router, you would enable forwarding on all interfaces except loopback.</span></span>

 

 



