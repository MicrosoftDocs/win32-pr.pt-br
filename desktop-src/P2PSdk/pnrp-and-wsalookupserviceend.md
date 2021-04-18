---
description: O PNRP usa a função WSALookupServiceEnd para fazer o seguinte.
ms.assetid: 0732929e-ca03-438f-80d9-48a3da0095f7
title: PNRP e WSALookupServiceEnd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1db499c9a736e26d630b623a29baa4c18dcfceeb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105787479"
---
# <a name="pnrp-and-wsalookupserviceend"></a><span data-ttu-id="d4f8c-103">PNRP e WSALookupServiceEnd</span><span class="sxs-lookup"><span data-stu-id="d4f8c-103">PNRP and WSALookupServiceEnd</span></span>

<span data-ttu-id="d4f8c-104">O PNRP usa a função [**WSALookupServiceEnd**](winsock-nsp-reference-links.md) para fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="d4f8c-104">PNRP uses the [**WSALookupServiceEnd**](winsock-nsp-reference-links.md) function to do the following:</span></span>

-   <span data-ttu-id="d4f8c-105">Encerrar uma consulta iniciada em uma chamada anterior para [ **WSALookupServiceBegin**](winsock-nsp-reference-links.md)</span><span class="sxs-lookup"><span data-stu-id="d4f8c-105">Terminate a query initiated in a previous call to [**WSALookupServiceBegin**](winsock-nsp-reference-links.md)</span></span>
-   <span data-ttu-id="d4f8c-106">Desbloquear uma chamada para [**WSALookupServiceNext**](winsock-nsp-reference-links.md) para interromper a pesquisa</span><span class="sxs-lookup"><span data-stu-id="d4f8c-106">Unblock a call to [**WSALookupServiceNext**](winsock-nsp-reference-links.md) to stop the search</span></span>

<span data-ttu-id="d4f8c-107">Uma chamada para [**WSALookupServiceEnd**](winsock-nsp-reference-links.md) encerra uma consulta e limpa o contexto.</span><span class="sxs-lookup"><span data-stu-id="d4f8c-107">A call to [**WSALookupServiceEnd**](winsock-nsp-reference-links.md) terminates a query and cleans up the context.</span></span> <span data-ttu-id="d4f8c-108">O identificador obtido de uma chamada para **WSALookupServiceBegin** deve ser passado como um parâmetro para **WSALookupServiceEnd**.</span><span class="sxs-lookup"><span data-stu-id="d4f8c-108">The handle obtained from a call to **WSALookupServiceBegin** must be passed as a parameter to **WSALookupServiceEnd**.</span></span>

<span data-ttu-id="d4f8c-109">Para obter mais informações sobre o PNRP e a função [**WSALookupServiceBegin**](winsock-nsp-reference-links.md) , consulte [PNRP e WSALookupServiceBegin](pnrp-and-wsalookupservicebegin.md).</span><span class="sxs-lookup"><span data-stu-id="d4f8c-109">For more information about PNRP and the [**WSALookupServiceBegin**](winsock-nsp-reference-links.md) function, see [PNRP and WSALookupServiceBegin](pnrp-and-wsalookupservicebegin.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d4f8c-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d4f8c-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d4f8c-111">PNRP e WSALookupServiceBegin</span><span class="sxs-lookup"><span data-stu-id="d4f8c-111">PNRP and WSALookupServiceBegin</span></span>](pnrp-and-wsalookupservicebegin.md)
</dt> <dt>

[<span data-ttu-id="d4f8c-112">Códigos de erro NSP PNRP</span><span class="sxs-lookup"><span data-stu-id="d4f8c-112">PNRP NSP Error Codes</span></span>](pnrp-nsp-error-codes.md)
</dt> <dt>

[<span data-ttu-id="d4f8c-113">**WSALookupServiceNext**</span><span class="sxs-lookup"><span data-stu-id="d4f8c-113">**WSALookupServiceNext**</span></span>](winsock-nsp-reference-links.md)
</dt> </dl>

 

 



