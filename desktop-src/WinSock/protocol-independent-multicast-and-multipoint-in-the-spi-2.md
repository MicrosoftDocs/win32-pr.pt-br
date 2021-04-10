---
description: Recursos de transmissão e multicast do Windows Sockets (Winsock) e de protocolos de transporte independentes.
ms.assetid: 861f457c-fe7e-4128-a3f3-786424a96ea5
title: Protocol-Independent multicast e MultiPoint no SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bda9e5cab1b790a1e2d2c64c4451063a94dd8bc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091384"
---
# <a name="protocol-independent-multicast-and-multipoint-in-the-spi"></a><span data-ttu-id="d736e-103">Protocol-Independent multicast e MultiPoint no SPI</span><span class="sxs-lookup"><span data-stu-id="d736e-103">Protocol-Independent Multicast and Multipoint in the SPI</span></span>

<span data-ttu-id="d736e-104">Assim como o Windows Sockets 2 permite que os recursos básicos de transporte de dados de vários protocolos de transporte sejam acessados de maneira genérica, ele também fornece uma maneira genérica de usar os recursos de MultiPoint e multicast de transportes que implementam esses recursos.</span><span class="sxs-lookup"><span data-stu-id="d736e-104">Just as Windows Sockets 2 allows the basic data transport capabilities of numerous transport protocols to be accessed in a generic manner, it also provides a generic way to use multipoint and multicast capabilities of transports that implement these features.</span></span> <span data-ttu-id="d736e-105">Para simplificar, o termo *MultiPoint* é usado daqui em diante para se referir a comunicações de multicast e de MultiPoint.</span><span class="sxs-lookup"><span data-stu-id="d736e-105">To simplify, the term *multipoint* is used hereafter to refer to both multicast and multipoint communications.</span></span>

<span data-ttu-id="d736e-106">As implementações atuais do MultiPoint (por exemplo, multicast de IP, ST-II, T. 120, ATM UNI) variam muito em relação ao modo como os nós ingressam em uma sessão do MultiPoint, se um nó específico é designado como um nó central ou raiz e se os dados são trocados entre todos os nós ou somente entre um nó raiz e vários nós folha.</span><span class="sxs-lookup"><span data-stu-id="d736e-106">Current multipoint implementations (for example, IP multicast, ST-II, T.120, ATM UNI) vary widely with respect to how nodes join a multipoint session, whether a particular node is designated as a central or root node, and whether data is exchanged between all nodes or only between a root node and various leaf nodes.</span></span> <span data-ttu-id="d736e-107">A estrutura de [**\_ informações WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) do Windows Sockets 2 é usada para declarar os atributos do MultiPoint de um protocolo.</span><span class="sxs-lookup"><span data-stu-id="d736e-107">The Windows Sockets 2 [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure is used to declare the multipoint attributes of a protocol.</span></span> <span data-ttu-id="d736e-108">Examinando esses atributos, o programador saberá quais convenções seguir no uso das funções Winsock aplicáveis para configurar, usar e subdividir as sessões do MultiPoint.</span><span class="sxs-lookup"><span data-stu-id="d736e-108">By examining these attributes the programmer will know what conventions to follow in using the applicable Winsock functions to set up, use, and tear down multipoint sessions.</span></span>

<span data-ttu-id="d736e-109">Os recursos do Windows Sockets 2 que oferecem suporte a multicast podem ser resumidos da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="d736e-109">The features of Windows Sockets 2 that support multicast can be summarized as follows:</span></span>

-   <span data-ttu-id="d736e-110">Três bits de atributo na estrutura de [**\_ informações de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) .</span><span class="sxs-lookup"><span data-stu-id="d736e-110">Three attribute bits in the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure.</span></span>
-   <span data-ttu-id="d736e-111">Quatro sinalizadores definidos para o parâmetro *dwFlags* de [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket)</span><span class="sxs-lookup"><span data-stu-id="d736e-111">Four flags defined for the *dwFlags* parameter of [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket)</span></span>
-   <span data-ttu-id="d736e-112">Uma função, [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf), para adicionar nós folha em uma sessão do MultiPoint.</span><span class="sxs-lookup"><span data-stu-id="d736e-112">One function, [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf), for adding leaf nodes into a multipoint session.</span></span>
-   <span data-ttu-id="d736e-113">Dois códigos de comando [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) para controlar o loopback do MultiPoint e estabelecer o escopo para transmissões multicast.</span><span class="sxs-lookup"><span data-stu-id="d736e-113">Two [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) command codes for controlling multipoint loopback and establishing the scope for multicast transmissions.</span></span> <span data-ttu-id="d736e-114">(O último corresponde ao parâmetro de tempo de vida ou TTL do IP multicast.)</span><span class="sxs-lookup"><span data-stu-id="d736e-114">(The latter corresponds to the IP multicast time-to-live or TTL parameter.)</span></span>

> [!Note]  
> <span data-ttu-id="d736e-115">A inclusão desses recursos do MultiPoint no Windows Sockets 2 não impede que um provedor de serviços também dê suporte a uma interface dependente de protocolo existente, como as opções de Soquete Deering para multicast de IP.</span><span class="sxs-lookup"><span data-stu-id="d736e-115">The inclusion of these multipoint features in Windows Sockets 2 does not preclude a service provider from also supporting an existing protocol-dependent interface, such as the Deering socket options for IP multicast.</span></span>

 

 

 
