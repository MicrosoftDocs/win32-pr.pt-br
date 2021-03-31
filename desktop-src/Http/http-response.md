---
title: HTTP_RESPONSE (http. h)
description: A versão da estrutura de \_ resposta http é dependente da versão da fila de solicitações usada como a seguir fila de solicitação da API do servidor http versão 1,0 Esta é uma \_ estrutura de solicitação HTTP \_ v1. Fila de solicitações da API do servidor HTTP versão 2,0 Esta é uma \_ estrutura de solicitação HTTP \_ v2.
ms.assetid: F94646C0-7293-4543-842B-F08D8C7E2247
keywords:
- HTTP_RESPONSE
- HTTP_RESPONSE
- PHTTP_RESPONSE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a8445021aa61b94ae83a55937b1db5ca4e3c577
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369486"
---
# <a name="http_response"></a><span data-ttu-id="c7988-106">\_resposta http</span><span class="sxs-lookup"><span data-stu-id="c7988-106">HTTP\_RESPONSE</span></span>

<span data-ttu-id="c7988-107">A versão da estrutura **de \_ resposta http** depende da versão da fila de solicitações usada da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="c7988-107">The version of the **HTTP\_RESPONSE** structure is dependent on the version of the request queue used as follows:</span></span>

-   <span data-ttu-id="c7988-108">Fila de solicitações da API do servidor HTTP versão 1,0: esta é uma estrutura de [**\_ solicitação HTTP \_ v1**](/windows/desktop/api/Http/ns-http-http_request_v1) .</span><span class="sxs-lookup"><span data-stu-id="c7988-108">HTTP Server API Version 1.0 request queue: This is an [**HTTP\_REQUEST\_V1**](/windows/desktop/api/Http/ns-http-http_request_v1) structure.</span></span>
-   <span data-ttu-id="c7988-109">Fila de solicitações da API do servidor HTTP versão 2,0: esta é uma estrutura de [**\_ solicitação HTTP \_ v2**](/windows/desktop/api/Http/ns-http-http_request_v2) .</span><span class="sxs-lookup"><span data-stu-id="c7988-109">HTTP Server API Version 2.0 request queue: This is an [**HTTP\_REQUEST\_V2**](/windows/desktop/api/Http/ns-http-http_request_v2) structure.</span></span>

<span data-ttu-id="c7988-110">Não use a [**solicitação \_ http \_ v1**](/windows/desktop/api/Http/ns-http-http_request_v1) e a [**\_ solicitação HTTP \_ v2**](/windows/desktop/api/Http/ns-http-http_request_v2) diretamente em seu código; usar **\_ resposta http** , em vez disso, garante que a versão apropriada da estrutura seja usada com base na versão da fila de solicitações.</span><span class="sxs-lookup"><span data-stu-id="c7988-110">Do not use [**HTTP\_REQUEST\_V1**](/windows/desktop/api/Http/ns-http-http_request_v1) and [**HTTP\_REQUEST\_V2**](/windows/desktop/api/Http/ns-http-http_request_v2) directly in your code; using **HTTP\_RESPONSE** instead ensures the proper version of the structure is used based on the version of the request queue.</span></span>


```C++
typedef HTTP_REQUEST_V1 HTTP_RESPONSE;
typedef HTTP_REQUEST_V2 HTTP_RESPONSE;
typedef HTTP_RESPONSE* PHTTP_RESPONSE;
```



<dl> <dt>

<span data-ttu-id="c7988-111">**\_resposta http**</span><span class="sxs-lookup"><span data-stu-id="c7988-111">**HTTP\_RESPONSE**</span></span>
</dt> <dd>

<span data-ttu-id="c7988-112">A solicitação foi de uma fila de solicitações v1.</span><span class="sxs-lookup"><span data-stu-id="c7988-112">Request was from a v1 request queue.</span></span>

</dd> <dt>

<span data-ttu-id="c7988-113">**\_resposta http**</span><span class="sxs-lookup"><span data-stu-id="c7988-113">**HTTP\_RESPONSE**</span></span>
</dt> <dd>

<span data-ttu-id="c7988-114">A solicitação foi de uma fila de solicitações v2.</span><span class="sxs-lookup"><span data-stu-id="c7988-114">Request was from a v2 request queue.</span></span>

</dd> <dt>

<span data-ttu-id="c7988-115">**resposta do PHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="c7988-115">**PHTTP\_RESPONSE**</span></span>
</dt> <dd>

<span data-ttu-id="c7988-116">Ponteiro para uma estrutura de **\_ resposta http** .</span><span class="sxs-lookup"><span data-stu-id="c7988-116">Pointer to an **HTTP\_RESPONSE** structure.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c7988-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c7988-117">Requirements</span></span>



| <span data-ttu-id="c7988-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="c7988-118">Requirement</span></span> | <span data-ttu-id="c7988-119">Valor</span><span class="sxs-lookup"><span data-stu-id="c7988-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="c7988-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c7988-120">Minimum supported client</span></span><br/> | <span data-ttu-id="c7988-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c7988-121">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c7988-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c7988-122">Minimum supported server</span></span><br/> | <span data-ttu-id="c7988-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c7988-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="c7988-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c7988-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="c7988-125"><dt>Http. h</dt></span><span class="sxs-lookup"><span data-stu-id="c7988-125"><dt>Http.h</dt></span></span> </dl> |



 

 





