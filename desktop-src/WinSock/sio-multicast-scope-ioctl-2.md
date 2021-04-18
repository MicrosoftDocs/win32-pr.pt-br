---
description: Usando o \_ código de comando do escopo multicast sio \_ para especificar o escopo no qual o multicast deve ocorrer.
ms.assetid: 3acec987-9cb4-446c-af6e-ea0e6a96e70c
title: SIO_MULTICAST_SCOPE IOCTL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90d1fd6f2bea76d095ea88d66c0ac029fb9168ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105763197"
---
# <a name="sio_multicast_scope-ioctl"></a><span data-ttu-id="52e88-103">\_IOCTL do \_ escopo multicast sio</span><span class="sxs-lookup"><span data-stu-id="52e88-103">SIO\_MULTICAST\_SCOPE Ioctl</span></span>

<span data-ttu-id="52e88-104">Quando o multicast é empregado, geralmente é necessário especificar o escopo sobre o qual a difusão seletiva deve ocorrer.</span><span class="sxs-lookup"><span data-stu-id="52e88-104">When multicasting is employed, it is usually necessary to specify the scope over which the multicast should occur.</span></span> <span data-ttu-id="52e88-105">Aqui, o escopo é definido como o número de segmentos de rede roteados a serem cobertos.</span><span class="sxs-lookup"><span data-stu-id="52e88-105">Here scope is defined to be the number of routed network segments to be covered.</span></span> <span data-ttu-id="52e88-106">O \_ \_ código de comando do escopo multicast sio para [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) é usado para controlar isso.</span><span class="sxs-lookup"><span data-stu-id="52e88-106">The SIO\_MULTICAST\_SCOPE command code for [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) is used to control this.</span></span> <span data-ttu-id="52e88-107">Um escopo de zero indicaria que a transmissão multicast não seria colocada na conexão, mas poderia ser disseminada entre os soquetes no host local.</span><span class="sxs-lookup"><span data-stu-id="52e88-107">A scope of zero would indicate that the multicast transmission would not be placed on the wire but could be disseminated across sockets within the local host.</span></span> <span data-ttu-id="52e88-108">Um valor de escopo de um (o padrão) indica que a transmissão será colocada na conexão, mas não vai cruzar nenhum roteador.</span><span class="sxs-lookup"><span data-stu-id="52e88-108">A scope value of one (the default) indicates that the transmission will be placed on the wire, but will not cross any routers.</span></span> <span data-ttu-id="52e88-109">Valores de escopo mais altos determinam o número de roteadores que podem ser cruzados.</span><span class="sxs-lookup"><span data-stu-id="52e88-109">Higher scope values determine the number of routers that may be crossed.</span></span> <span data-ttu-id="52e88-110">Observe que isso corresponde ao parâmetro time-to-Live (TTL) no multicast de IP.</span><span class="sxs-lookup"><span data-stu-id="52e88-110">Note that this corresponds to the time-to-live (TTL) parameter in IP multicasting.</span></span>

 

 
