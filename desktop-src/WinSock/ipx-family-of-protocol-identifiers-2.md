---
description: O parâmetro de protocolo em Socket e WSASocket é um identificador que estabelece um tipo de rede e um método para identificar os vários protocolos de transporte executados na rede.
ms.assetid: cb4d99d5-3ae0-4bfc-b521-122dd9d4f1c2
title: Família IPX de identificadores de protocolo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7fc808a04f1cf10bb099cd7d923bf471e9bd8d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090379"
---
# <a name="ipx-family-of-protocol-identifiers"></a><span data-ttu-id="567f8-103">Família IPX de identificadores de protocolo</span><span class="sxs-lookup"><span data-stu-id="567f8-103">IPX Family of Protocol Identifiers</span></span>

<span data-ttu-id="567f8-104">O parâmetro de *protocolo* em [**Socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) e [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) é um identificador que estabelece um tipo de rede e um método para identificar os vários protocolos de transporte executados na rede.</span><span class="sxs-lookup"><span data-stu-id="567f8-104">The *protocol* parameter in [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) and [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) is an identifier that establishes a network type and a method for identifying the various transport protocols that run on the network.</span></span> <span data-ttu-id="567f8-105">Ao contrário do IP, o IPX não usa um valor de protocolo único para selecionar uma pilha de transporte.</span><span class="sxs-lookup"><span data-stu-id="567f8-105">Unlike IP, IPX does not use a single protocol value for selecting a transport stack.</span></span> <span data-ttu-id="567f8-106">Como não há nenhum requisito de rede para usar um valor específico para cada protocolo de transporte, estamos livres para atribuí-los de maneira conveniente para aplicativos Winsock.</span><span class="sxs-lookup"><span data-stu-id="567f8-106">Since there is no network requirement to use a specific value for each transport protocol, we are free to assign them in a manner convenient for Winsock applications.</span></span> <span data-ttu-id="567f8-107">Evitamos valores de 0 a 255 para evitar colisões com os valores de protocolo de PF \_ inet correspondentes.</span><span class="sxs-lookup"><span data-stu-id="567f8-107">We avoid values 0–255 in order to avoid collisions with the corresponding PF\_INET protocol values.</span></span>



| <span data-ttu-id="567f8-108">Nome</span><span class="sxs-lookup"><span data-stu-id="567f8-108">Name</span></span>         | <span data-ttu-id="567f8-109">Valor</span><span class="sxs-lookup"><span data-stu-id="567f8-109">Value</span></span>       | <span data-ttu-id="567f8-110">Tipos de soquete</span><span class="sxs-lookup"><span data-stu-id="567f8-110">Socket types</span></span>              | <span data-ttu-id="567f8-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="567f8-111">Description</span></span>                                         |
|--------------|-------------|---------------------------|-----------------------------------------------------|
| <span data-ttu-id="567f8-112">Reservado</span><span class="sxs-lookup"><span data-stu-id="567f8-112">Reserved</span></span>     | <span data-ttu-id="567f8-113">0-255</span><span class="sxs-lookup"><span data-stu-id="567f8-113">0-255</span></span>       |                           | <span data-ttu-id="567f8-114">Reservado para valores de protocolo de PF \_ inet.</span><span class="sxs-lookup"><span data-stu-id="567f8-114">Reserved for PF\_INET protocol values.</span></span>              |
| <span data-ttu-id="567f8-115">NSPROTO \_ IPX</span><span class="sxs-lookup"><span data-stu-id="567f8-115">NSPROTO\_IPX</span></span> | <span data-ttu-id="567f8-116">1000-1255</span><span class="sxs-lookup"><span data-stu-id="567f8-116">1000 - 1255</span></span> | <span data-ttu-id="567f8-117">SOCK \_ DGRAM Sock \_ RAW</span><span class="sxs-lookup"><span data-stu-id="567f8-117">SOCK\_DGRAM SOCK\_RAW</span></span>     | <span data-ttu-id="567f8-118">Serviço de datagrama para IPX.</span><span class="sxs-lookup"><span data-stu-id="567f8-118">Datagram service for IPX.</span></span>                           |
| <span data-ttu-id="567f8-119">NSPROTO \_ SPX</span><span class="sxs-lookup"><span data-stu-id="567f8-119">NSPROTO\_SPX</span></span> | <span data-ttu-id="567f8-120">1256</span><span class="sxs-lookup"><span data-stu-id="567f8-120">1256</span></span>        | <span data-ttu-id="567f8-121">SOCK \_ Stream Sock \_ SEQPKT</span><span class="sxs-lookup"><span data-stu-id="567f8-121">SOCK\_STREAM SOCK\_SEQPKT</span></span> | <span data-ttu-id="567f8-122">Troca de pacotes confiável usando pacotes de tamanho fixo.</span><span class="sxs-lookup"><span data-stu-id="567f8-122">Reliable packet exchange using fixed-sized packets.</span></span> |



 

> [!Note]  
> <span data-ttu-id="567f8-123">Quando NSPROTO \_ SPX for especificado, o protocolo SPX II será automaticamente utilizado se ambos os pontos de extremidade forem capazes de fazer isso.</span><span class="sxs-lookup"><span data-stu-id="567f8-123">When NSPROTO\_SPX is specified, the SPX II protocol is automatically utilized if both endpoints are capable of doing so.</span></span>

 

 

 



