---
description: Quando o multicast é empregado, geralmente é necessário especificar o escopo sobre o qual a difusão seletiva deve ocorrer.
ms.assetid: 744b43a8-dd89-4e63-ae3c-5bee72864df7
title: SIO_MULTICAST_SCOPE o código de comando para WSAIoctl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 209a43e461907dcded8e59c6ffee9b1376989d6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010769"
---
# <a name="sio_multicast_scope-command-code-for-wsaioctl"></a><span data-ttu-id="70b9a-103">\_ \_ Código de comando do escopo multicast sio para WSAIoctl</span><span class="sxs-lookup"><span data-stu-id="70b9a-103">SIO\_MULTICAST\_SCOPE Command Code for WSAIoctl</span></span>

<span data-ttu-id="70b9a-104">Quando o multicast é empregado, geralmente é necessário especificar o *escopo* sobre o qual a difusão seletiva deve ocorrer.</span><span class="sxs-lookup"><span data-stu-id="70b9a-104">When multicasting is employed, it is usually necessary to specify the *scope* over which the multicast should occur.</span></span> <span data-ttu-id="70b9a-105">O escopo é definido como o número de segmentos de rede roteados a serem cobertos.</span><span class="sxs-lookup"><span data-stu-id="70b9a-105">Scope is defined as the number of routed network segments to be covered.</span></span> <span data-ttu-id="70b9a-106">Um escopo de zero indicaria que a transmissão multicast não seria colocada na conexão, mas poderia ser disseminada entre os soquetes no host local.</span><span class="sxs-lookup"><span data-stu-id="70b9a-106">A scope of zero would indicate that the multicast transmission would not be placed on the wire but could be disseminated across sockets within the local host.</span></span> <span data-ttu-id="70b9a-107">Um valor de escopo de 1 (o padrão) indica que a transmissão será colocada na conexão, mas não cruzará nenhum roteador.</span><span class="sxs-lookup"><span data-stu-id="70b9a-107">A scope value of 1 (the default) indicates that the transmission will be placed on the wire, but will not cross any routers.</span></span> <span data-ttu-id="70b9a-108">Valores de escopo mais altos determinam o número de roteadores que podem ser cruzados.</span><span class="sxs-lookup"><span data-stu-id="70b9a-108">Higher scope values determine the number of routers that may be crossed.</span></span> <span data-ttu-id="70b9a-109">Observe que isso corresponde ao parâmetro time-to-Live (TTL) no multicast de IP.</span><span class="sxs-lookup"><span data-stu-id="70b9a-109">Note that this corresponds to the time-to-live (TTL) parameter in IP multicasting.</span></span>

<span data-ttu-id="70b9a-110">A função [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) é usada para ingressar um nó folha na sessão do MultiPoint.</span><span class="sxs-lookup"><span data-stu-id="70b9a-110">The function [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) is used to join a leaf node into the multipoint session.</span></span> <span data-ttu-id="70b9a-111">Consulte o seguinte para obter uma discussão sobre como essa função é utilizada.</span><span class="sxs-lookup"><span data-stu-id="70b9a-111">See the following for a discussion on how this function is utilized.</span></span>

 

 



