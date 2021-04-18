---
description: Antes que um soquete possa ser usado para configurar uma conexão ou receber uma solicitação de conexão, ele precisa estar associado a um endereço local.
ms.assetid: 8767a209-e293-47cd-b503-ff4cffbf6fb4
title: Associação a um endereço local
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39aa022d17a8862e6092c52b18edd1539f2d95ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105771355"
---
# <a name="binding-to-a-local-address"></a><span data-ttu-id="5d84b-103">Associação a um endereço local</span><span class="sxs-lookup"><span data-stu-id="5d84b-103">Binding to a Local Address</span></span>

<span data-ttu-id="5d84b-104">Antes que um soquete possa ser usado para configurar uma conexão ou receber uma solicitação de conexão, ele precisa estar associado a um endereço local.</span><span class="sxs-lookup"><span data-stu-id="5d84b-104">Before a socket can be used to set up a connection or receive a connection request, it needs to be bound to a local address.</span></span> <span data-ttu-id="5d84b-105">Isso pode ser feito explicitamente chamando [**WSPBind**](/previous-versions/windows/hardware/network/ff566268(v=vs.85))ou implicitamente por [**WSPConnect**](/previous-versions/windows/hardware/network/ff566275(v=vs.85)) se o soquete estiver desassociado quando essa função for chamada.</span><span class="sxs-lookup"><span data-stu-id="5d84b-105">This could be done explicitly by calling [**WSPBind**](/previous-versions/windows/hardware/network/ff566268(v=vs.85)), or implicitly by [**WSPConnect**](/previous-versions/windows/hardware/network/ff566275(v=vs.85)) if the socket is unbound when this function is called.</span></span>

 

 
