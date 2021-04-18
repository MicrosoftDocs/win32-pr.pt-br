---
description: Em alguns casos, os soquetes ingressados em uma sessão do MultiPoint podem ter algumas diferenças no comportamento de soquetes ponto a ponto.
ms.assetid: e59b701f-f85f-4fd6-8d6d-e46199250c22
title: Marcar bits para WSASocket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51fede5d160d89b08064d8dff1c1a901c048526f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105807887"
---
# <a name="flag-bits-for-wsasocket"></a><span data-ttu-id="7084a-103">Marcar bits para WSASocket</span><span class="sxs-lookup"><span data-stu-id="7084a-103">Flag Bits for WSASocket</span></span>

<span data-ttu-id="7084a-104">Em alguns casos, os soquetes ingressados em uma sessão do MultiPoint podem ter algumas diferenças no comportamento de soquetes ponto a ponto.</span><span class="sxs-lookup"><span data-stu-id="7084a-104">In some instances sockets joined to a multipoint session may have some differences in behavior from point-to-point sockets.</span></span> <span data-ttu-id="7084a-105">Por exemplo, um \_ soquete de folha d em um esquema de plano de dados com raiz só pode enviar informações para o \_ participante da raiz d.</span><span class="sxs-lookup"><span data-stu-id="7084a-105">For example, a d\_leaf socket in a rooted data plane scheme can only send information to the d\_root participant.</span></span> <span data-ttu-id="7084a-106">Isso cria uma necessidade de o aplicativo ser capaz de indicar o uso pretendido de um soquete coincidente com sua criação.</span><span class="sxs-lookup"><span data-stu-id="7084a-106">This creates a need for the application to be able to indicate the intended use of a socket coincident with its creation.</span></span> <span data-ttu-id="7084a-107">Isso é feito por meio de bits de quatro sinalizadores que podem ser definidos no parâmetro *dwFlags* para [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa):</span><span class="sxs-lookup"><span data-stu-id="7084a-107">This is done through four-flag bits that can be set in the *dwFlags* parameter to [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa):</span></span>

-   <span data-ttu-id="7084a-108">\_O sinalizador \_ WSA \_ \_ raiz do MultiPoint C, para a criação de um soquete agindo como uma \_ raiz C e permitido somente se um plano de controle com raiz for indicado na entrada de [**\_ informações de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) correspondente.</span><span class="sxs-lookup"><span data-stu-id="7084a-108">WSA\_FLAG\_MULTIPOINT\_C\_ROOT, for the creation of a socket acting as a c\_root, and only allowed if a rooted control plane is indicated in the corresponding [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) entry.</span></span>
-   <span data-ttu-id="7084a-109">\_O sinalizador WSA do \_ MultiPoint \_ C \_ folha, para a criação de um soquete agindo como uma \_ folha C e permitido somente se o XP1 \_ oferecer suporte ao \_ MultiPoint for indicado na entrada de [**\_ informações de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) correspondente.</span><span class="sxs-lookup"><span data-stu-id="7084a-109">WSA\_FLAG\_MULTIPOINT\_C\_LEAF, for the creation of a socket acting as a c\_leaf, and only allowed if XP1\_SUPPORT\_MULTIPOINT is indicated in the corresponding [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) entry.</span></span>
-   <span data-ttu-id="7084a-110">\_O sinalizador WSA da \_ \_ raiz do MultiPoint D \_ , para a criação de um soquete agindo como uma \_ raiz D e permitido somente se um plano de dados com raiz for indicado na entrada de [**\_ informações de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) correspondente.</span><span class="sxs-lookup"><span data-stu-id="7084a-110">WSA\_FLAG\_MULTIPOINT\_D\_ROOT, for the creation of a socket acting as a d\_root, and only allowed if a rooted data plane is indicated in the corresponding [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) entry.</span></span>
-   <span data-ttu-id="7084a-111">\_O sinalizador WSA do \_ MultiPoint \_ D \_ folha, para a criação de um soquete agindo como uma \_ folha d e permitido somente se \_ o XP1 oferecer suporte ao \_ MultiPoint for indicado na entrada de [**\_ informações de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) correspondente.</span><span class="sxs-lookup"><span data-stu-id="7084a-111">WSA\_FLAG\_MULTIPOINT\_D\_LEAF, for the creation of a socket acting as a d\_leaf, and only allowed if XP1\_SUPPORT\_MULTIPOINT is indicated in the corresponding [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) entry.</span></span>

<span data-ttu-id="7084a-112">Observe que, ao criar um soquete do MultiPoint, exatamente um dos dois sinalizadores de plano de controle e um dos dois sinalizadores de plano de dados devem ser definidos no parâmetro *dwFlags* de [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa).</span><span class="sxs-lookup"><span data-stu-id="7084a-112">Note that when creating a multipoint socket, exactly one of the two control-plane flags, and one of the two data-plane flags must be set in [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa)'s *dwFlags* parameter.</span></span> <span data-ttu-id="7084a-113">Portanto, as quatro possibilidades para criar soquetes do MultiPoint são:</span><span class="sxs-lookup"><span data-stu-id="7084a-113">Thus, the four possibilities for creating multipoint sockets are:</span></span>

-   <span data-ttu-id="7084a-114">" \_ raiz c raiz/d \_ "</span><span class="sxs-lookup"><span data-stu-id="7084a-114">"c\_root/d\_root"</span></span>
-   <span data-ttu-id="7084a-115">"c \_ raiz/d \_ folha"</span><span class="sxs-lookup"><span data-stu-id="7084a-115">"c\_root/d\_leaf"</span></span>
-   <span data-ttu-id="7084a-116">"c \_ folha/d \_ raiz"</span><span class="sxs-lookup"><span data-stu-id="7084a-116">"c\_leaf/d\_root"</span></span>
-   <span data-ttu-id="7084a-117">"c \_ folha/d \_ folha"</span><span class="sxs-lookup"><span data-stu-id="7084a-117">"c\_leaf /d\_leaf"</span></span>

 

 
