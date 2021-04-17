---
description: O Windows Sockets 2 fornece um método genérico para utilizar os recursos multiponto e multicast dos transportes.
ms.assetid: 75cd8f21-a391-4626-b909-0760d12db995
title: Protocol-Independent multicast e MultiPoint
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e409c18752b32af7cf65b4a55862ec75cec7a3e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105811524"
---
# <a name="protocol-independent-multicast-and-multipoint"></a><span data-ttu-id="db0f5-103">Protocol-Independent multicast e MultiPoint</span><span class="sxs-lookup"><span data-stu-id="db0f5-103">Protocol-Independent Multicast and Multipoint</span></span>

<span data-ttu-id="db0f5-104">O Windows Sockets 2 fornece um método genérico para utilizar os recursos multiponto e multicast dos transportes.</span><span class="sxs-lookup"><span data-stu-id="db0f5-104">Windows Sockets 2 provides a generic method for utilizing the multipoint and multicast capabilities of transports.</span></span> <span data-ttu-id="db0f5-105">Esse método genérico implementa esses recursos da mesma forma que permite que os recursos básicos de transporte de dados de vários protocolos de transporte sejam acessados.</span><span class="sxs-lookup"><span data-stu-id="db0f5-105">This generic method implements these features just as it allows the basic data transport capabilities of numerous transport protocols to be accessed.</span></span> <span data-ttu-id="db0f5-106">O termo MultiPoint, é usado daqui em diante para se referir a comunicações de multicast e de MultiPoint.</span><span class="sxs-lookup"><span data-stu-id="db0f5-106">The term, multipoint, is used hereafter to refer to both multicast and multipoint communications.</span></span>

<span data-ttu-id="db0f5-107">As implementações atuais do MultiPoint (por exemplo, multicast de IP, ST-II, T. 120 e ATM UNI) variam muito.</span><span class="sxs-lookup"><span data-stu-id="db0f5-107">Current multipoint implementations (for example, IP multicast, ST-II, T.120, and ATM UNI) vary widely.</span></span> <span data-ttu-id="db0f5-108">Como os nós ingressam em uma sessão do MultiPoint, se um nó específico é designado como um nó central ou raiz e se os dados são trocados entre todos os nós ou somente entre um nó raiz e os vários nós folha diferem entre as implementações.</span><span class="sxs-lookup"><span data-stu-id="db0f5-108">How nodes join a multipoint session, whether a particular node is designated as a central or root node, and whether data is exchanged between all nodes or only between a root node and the various leaf nodes differ among implementations.</span></span> <span data-ttu-id="db0f5-109">A estrutura de [**\_ informações do WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) para Windows Sockets 2 é usada para declarar os vários atributos do MultiPoint de um protocolo.</span><span class="sxs-lookup"><span data-stu-id="db0f5-109">The [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure for Windows Sockets 2 is used to declare the various multipoint attributes of a protocol.</span></span> <span data-ttu-id="db0f5-110">Examinando esses atributos, o programador sabe quais convenções seguir com as funções aplicáveis do Windows Sockets 2 para configurar, utilizar e subdividir as sessões do MultiPoint.</span><span class="sxs-lookup"><span data-stu-id="db0f5-110">By examining these attributes, the programmer knows what conventions to follow with the applicable Windows Sockets 2 functions to set up, utilize, and tear down multipoint sessions.</span></span>

<span data-ttu-id="db0f5-111">O seguinte resume os recursos do Winsock que dão suporte ao MultiPoint:</span><span class="sxs-lookup"><span data-stu-id="db0f5-111">The following summarizes Winsock features that support multipoint:</span></span>

-   <span data-ttu-id="db0f5-112">Bits de dois atributos na estrutura [**de \_ informações de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) .</span><span class="sxs-lookup"><span data-stu-id="db0f5-112">Two-attribute bits in the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure.</span></span>
-   <span data-ttu-id="db0f5-113">Quatro sinalizadores definidos para o parâmetro *dwFlags* da função [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) .</span><span class="sxs-lookup"><span data-stu-id="db0f5-113">Four flags defined for the *dwFlags* parameter of the [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) function.</span></span>
-   <span data-ttu-id="db0f5-114">Uma função, [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf), para adicionar nós folha em uma sessão do MultiPoint</span><span class="sxs-lookup"><span data-stu-id="db0f5-114">One function, [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf), for adding leaf nodes into a multipoint session</span></span>
-   <span data-ttu-id="db0f5-115">Dois códigos de comando [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) para controlar o loopback do MultiPoint e estabelecer o escopo para transmissões multicast.</span><span class="sxs-lookup"><span data-stu-id="db0f5-115">Two [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) command codes for controlling multipoint loopback and establishing the scope for multicast transmissions.</span></span> <span data-ttu-id="db0f5-116">(O último corresponde ao parâmetro de tempo de vida ou TTL do IP multicast.)</span><span class="sxs-lookup"><span data-stu-id="db0f5-116">(The latter corresponds to the IP multicast time-to-live or TTL parameter.)</span></span>

> [!Note]  
> <span data-ttu-id="db0f5-117">A inclusão desses recursos do MultiPoint no Windows Sockets 2 não impede que um aplicativo use uma interface dependente de protocolo existente, como as opções de Soquete Deering para multicast de IP.</span><span class="sxs-lookup"><span data-stu-id="db0f5-117">The inclusion of these multipoint features in Windows Sockets 2 does not preclude an application from using an existing protocol-dependent interface, such as the Deering socket options for IP multicast.</span></span>

 

<span data-ttu-id="db0f5-118">Consulte [semântica do MultiPoint e multicast](multipoint-and-multicast-semantics-2.md) para obter informações detalhadas sobre como os vários esquemas do MultiPoint são caracterizados e como os recursos aplicáveis do Windows Sockets 2 são utilizados.</span><span class="sxs-lookup"><span data-stu-id="db0f5-118">See [Multipoint and Multicast Semantics](multipoint-and-multicast-semantics-2.md) for detailed information on how the various multipoint schemes are characterized and how the applicable features of Windows Sockets 2 are utilized.</span></span>

 

 
