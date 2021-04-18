---
title: Constantes de HTTP_RESPONSE_FLAG_ (http. h)
description: Defina opções para configurar as respostas na API do servidor HTTP.
ms.assetid: bcb59457-fd22-4166-8a72-ba85209ec8c7
topic_type:
- apiref
api_name:
- HTTP_RESPONSE_FLAG_MULTIPLE_ENCODINGS_AVAILABLE
api_location:
- http.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96b7c34d453c1b9bbe45cf2c85ad268b414f3439
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105764696"
---
# <a name="http_response_flag_-constants"></a><span data-ttu-id="11294-103">\_Constantes de \_ sinalizador de resposta http \_</span><span class="sxs-lookup"><span data-stu-id="11294-103">HTTP\_RESPONSE\_FLAG\_ Constants</span></span>

<span data-ttu-id="11294-104">As constantes do **\_ \_ sinalizador \_ de resposta http** definem opções para configurar as respostas na API do servidor http.</span><span class="sxs-lookup"><span data-stu-id="11294-104">The **HTTP\_RESPONSE\_FLAG\_** constants define options to configure responses in the HTTP Server API.</span></span>

<span data-ttu-id="11294-105">Essas constantes são usadas no membro **flags** da estrutura [**http \_ Response \_ v1**](/windows/desktop/api/Http/ns-http-http_response_v1) .</span><span class="sxs-lookup"><span data-stu-id="11294-105">These constants are used in the **Flags** member of the [**HTTP\_RESPONSE\_V1**](/windows/desktop/api/Http/ns-http-http_response_v1) structure.</span></span>

<dl> <dt>

<span data-ttu-id="11294-106"><span id="HTTP_RESPONSE_FLAG_MULTIPLE_ENCODINGS_AVAILABLE"></span><span id="http_response_flag_multiple_encodings_available"></span>**\_ \_ \_ várias codificações de sinalizador de resposta http \_ \_ disponíveis**</span><span class="sxs-lookup"><span data-stu-id="11294-106"><span id="HTTP_RESPONSE_FLAG_MULTIPLE_ENCODINGS_AVAILABLE"></span><span id="http_response_flag_multiple_encodings_available"></span>**HTTP\_RESPONSE\_FLAG\_MULTIPLE\_ENCODINGS\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="11294-107">Codificações diferentes do formulário de identidade estão disponíveis para este recurso.</span><span class="sxs-lookup"><span data-stu-id="11294-107">Encodings other than identity form are available for this resource.</span></span> <span data-ttu-id="11294-108">Esse sinalizador será ignorado se o aplicativo não tiver solicitado que a resposta seja armazenada em cache.</span><span class="sxs-lookup"><span data-stu-id="11294-108">This flag is ignored if the application has not asked for the response to be cached.</span></span> <span data-ttu-id="11294-109">Ele é usado como uma dica à API do servidor HTTP para negociação de conteúdo ao servir do cache de resposta do kernel.</span><span class="sxs-lookup"><span data-stu-id="11294-109">It's used as a hint to the HTTP Server API for content negotiation when serving from the kernel response cache.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="11294-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="11294-110">Requirements</span></span>



| <span data-ttu-id="11294-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="11294-111">Requirement</span></span> | <span data-ttu-id="11294-112">Valor</span><span class="sxs-lookup"><span data-stu-id="11294-112">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="11294-113">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="11294-113">Minimum supported client</span></span><br/> | <span data-ttu-id="11294-114">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="11294-114">Windows 7 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="11294-115">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="11294-115">Minimum supported server</span></span><br/> | <span data-ttu-id="11294-116">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="11294-116">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="11294-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="11294-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="11294-118"><dt>Http. h</dt></span><span class="sxs-lookup"><span data-stu-id="11294-118"><dt>Http.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11294-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="11294-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11294-120">Constantes da API do servidor HTTP versão 2,0</span><span class="sxs-lookup"><span data-stu-id="11294-120">HTTP Server API Version 2.0 Constants</span></span>](http-server-api-version-2-0-constants.md)
</dt> <dt>

[<span data-ttu-id="11294-121">**\_Resposta http \_ v1**</span><span class="sxs-lookup"><span data-stu-id="11294-121">**HTTP\_RESPONSE\_V1**</span></span>](/windows/desktop/api/Http/ns-http-http_response_v1)
</dt> </dl>

 

 





