---
description: O PNRP usa a estrutura WSAQUERYSET em conjunto com várias funções para facilitar a resolução de nomes e a enumeração de nomes e nuvens.
ms.assetid: 0ccf20c1-4c95-4caf-a8f3-82a9e0a9907b
title: PNRP e WSAQUERYSET (P2P. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d09d135d57af0922feb5a143c41696d85dac083
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105770362"
---
# <a name="pnrp-and-wsaqueryset"></a><span data-ttu-id="36029-103">PNRP e WSAQUERYSET</span><span class="sxs-lookup"><span data-stu-id="36029-103">PNRP and WSAQUERYSET</span></span>

<span data-ttu-id="36029-104">O PNRP usa a estrutura [**WSAQUERYSET**](winsock-nsp-reference-links.md) em conjunto com várias funções para facilitar a resolução de nomes e a enumeração de nomes e nuvens.</span><span class="sxs-lookup"><span data-stu-id="36029-104">PNRP uses the [**WSAQUERYSET**](winsock-nsp-reference-links.md) structure in conjunction with various functions to facilitate resolving names and enumerating names and clouds.</span></span>

<span data-ttu-id="36029-105">Para obter definições completas de funções do [**WSAQUERYSET**](winsock-nsp-reference-links.md) ou do Windows Sockets, consulte suas respectivas definições na documentação da API do Windows Sockets 2 no SDK da plataforma.</span><span class="sxs-lookup"><span data-stu-id="36029-105">For complete definitions of [**WSAQUERYSET**](winsock-nsp-reference-links.md) or Windows Sockets functions, see their respective definitions in the Windows Sockets 2 API documentation in the Platform SDK.</span></span>

## <a name="wsaqueryset-and-wsasetservice"></a><span data-ttu-id="36029-106">WSAQUERYSET e WSASetService</span><span class="sxs-lookup"><span data-stu-id="36029-106">WSAQUERYSET and WSASetService</span></span>

<span data-ttu-id="36029-107">A função [**WSASetService**](winsock-nsp-reference-links.md) usa a estrutura **WSAQUERYSET** para registrar ou remover nomes de par.</span><span class="sxs-lookup"><span data-stu-id="36029-107">The [**WSASetService**](winsock-nsp-reference-links.md) function uses the **WSAQUERYSET** structure to register or remove peer names.</span></span> <span data-ttu-id="36029-108">A página [PNRP e WSASetService](pnrp-and-wsasetservice.md) descreve como usar a estrutura **WSAQUERYSET** com essa função.</span><span class="sxs-lookup"><span data-stu-id="36029-108">The [PNRP and WSASetService](pnrp-and-wsasetservice.md) page outlines how to use the **WSAQUERYSET** structure with this function.</span></span>

## <a name="wsaqueryset-and-wsalookupservicebegin"></a><span data-ttu-id="36029-109">WSAQUERYSET e WSALookupServiceBegin</span><span class="sxs-lookup"><span data-stu-id="36029-109">WSAQUERYSET and WSALookupServiceBegin</span></span>

<span data-ttu-id="36029-110">A estrutura [**WSAQUERYSET**](winsock-nsp-reference-links.md) é usada extensivamente com as funções **WSALookupServiceBegin**, **WSALookupServiceNext** e **WSALookupServiceEnd** .</span><span class="sxs-lookup"><span data-stu-id="36029-110">The [**WSAQUERYSET**](winsock-nsp-reference-links.md) structure is used extensively with the **WSALookupServiceBegin**, **WSALookupServiceNext**, and **WSALookupServiceEnd** functions.</span></span> <span data-ttu-id="36029-111">Detalhes sobre como essas funções usam a estrutura **WSAQUERYSET** são detalhados nas seguintes páginas de referência:</span><span class="sxs-lookup"><span data-stu-id="36029-111">Details about how these functions use the **WSAQUERYSET** structure are detailed in the following reference pages:</span></span>

-   [<span data-ttu-id="36029-112">PNRP e WSALookupServiceBegin</span><span class="sxs-lookup"><span data-stu-id="36029-112">PNRP and WSALookupServiceBegin</span></span>](pnrp-and-wsalookupservicebegin.md)
-   [<span data-ttu-id="36029-113">PNRP e WSALookupServiceNext</span><span class="sxs-lookup"><span data-stu-id="36029-113">PNRP and WSALookupServiceNext</span></span>](pnrp-and-wsalookupservicenext.md)
-   [<span data-ttu-id="36029-114">PNRP e WSALookupServiceEnd</span><span class="sxs-lookup"><span data-stu-id="36029-114">PNRP and WSALookupServiceEnd</span></span>](pnrp-and-wsalookupserviceend.md)

## <a name="requirements"></a><span data-ttu-id="36029-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="36029-115">Requirements</span></span>



| <span data-ttu-id="36029-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="36029-116">Requirement</span></span> | <span data-ttu-id="36029-117">Valor</span><span class="sxs-lookup"><span data-stu-id="36029-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="36029-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="36029-118">Minimum supported client</span></span><br/> | <span data-ttu-id="36029-119">\[Somente aplicativos de área de trabalho do Windows XP com SP2\]</span><span class="sxs-lookup"><span data-stu-id="36029-119">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="36029-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="36029-120">Minimum supported server</span></span><br/> | <span data-ttu-id="36029-121">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="36029-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="36029-122">Versão</span><span class="sxs-lookup"><span data-stu-id="36029-122">Version</span></span><br/>                  | <span data-ttu-id="36029-123">Windows XP com SP1 com o Advanced Networking Pack para Windows XP</span><span class="sxs-lookup"><span data-stu-id="36029-123">Windows XP with SP1 with the Advanced Networking Pack for Windows XP</span></span><br/>  |
| <span data-ttu-id="36029-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="36029-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="36029-125"><dt>P2P. h</dt></span><span class="sxs-lookup"><span data-stu-id="36029-125"><dt>P2P.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36029-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="36029-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36029-127">PNRP e BLOB</span><span class="sxs-lookup"><span data-stu-id="36029-127">PNRP and BLOB</span></span>](pnrp-and-blob.md)
</dt> <dt>

[<span data-ttu-id="36029-128">PNRP e WSASetService</span><span class="sxs-lookup"><span data-stu-id="36029-128">PNRP and WSASetService</span></span>](pnrp-and-wsasetservice.md)
</dt> </dl>

 

 




