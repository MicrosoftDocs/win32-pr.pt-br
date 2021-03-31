---
description: Representa um identificador para uma resposta OCSP associada a uma cadeia de certificados de servidor.
ms.assetid: baf173f1-99dc-49f9-9a17-fee79b393db7
title: HCERT_SERVER_OCSP_RESPONSE (Wincrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ceab319b5d8370dd15ef3dcd288124e4f2adf9ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829537"
---
# <a name="hcert_server_ocsp_response"></a><span data-ttu-id="157f8-103">\_resposta OCSP do servidor HCERT \_ \_</span><span class="sxs-lookup"><span data-stu-id="157f8-103">HCERT\_SERVER\_OCSP\_RESPONSE</span></span>

<span data-ttu-id="157f8-104">O tipo de dados de **\_ \_ \_ resposta OCSP do servidor HCERT** representa um identificador para uma resposta OCSP associada a uma cadeia de certificados de servidor.</span><span class="sxs-lookup"><span data-stu-id="157f8-104">The **HCERT\_SERVER\_OCSP\_RESPONSE** data type represents a handle to an OCSP response associated with a server certificate chain.</span></span>

<span data-ttu-id="157f8-105">Esse tipo é usado pelas APIs a seguir.</span><span class="sxs-lookup"><span data-stu-id="157f8-105">This type is used by the following APIs.</span></span>

-   [<span data-ttu-id="157f8-106">**CertOpenServerOcspResponse**</span><span class="sxs-lookup"><span data-stu-id="157f8-106">**CertOpenServerOcspResponse**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenserverocspresponse)
-   [<span data-ttu-id="157f8-107">**CertAddRefServerOcspResponse**</span><span class="sxs-lookup"><span data-stu-id="157f8-107">**CertAddRefServerOcspResponse**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddrefserverocspresponse)
-   [<span data-ttu-id="157f8-108">**CertCloseServerOcspResponse**</span><span class="sxs-lookup"><span data-stu-id="157f8-108">**CertCloseServerOcspResponse**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certcloseserverocspresponse)
-   [<span data-ttu-id="157f8-109">**CertGetServerOcspResponseContext**</span><span class="sxs-lookup"><span data-stu-id="157f8-109">**CertGetServerOcspResponseContext**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetserverocspresponsecontext)


```C++
typedef VOID* HCERT_SERVER_OCSP_RESPONSE;
```



## <a name="requirements"></a><span data-ttu-id="157f8-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="157f8-110">Requirements</span></span>



| <span data-ttu-id="157f8-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="157f8-111">Requirement</span></span> | <span data-ttu-id="157f8-112">Valor</span><span class="sxs-lookup"><span data-stu-id="157f8-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="157f8-113">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="157f8-113">Minimum supported client</span></span><br/> | <span data-ttu-id="157f8-114">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="157f8-114">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="157f8-115">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="157f8-115">Minimum supported server</span></span><br/> | <span data-ttu-id="157f8-116">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="157f8-116">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="157f8-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="157f8-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="157f8-118"><dt>Wincrypt. h</dt></span><span class="sxs-lookup"><span data-stu-id="157f8-118"><dt>Wincrypt.h</dt></span></span> </dl> |



 

 




