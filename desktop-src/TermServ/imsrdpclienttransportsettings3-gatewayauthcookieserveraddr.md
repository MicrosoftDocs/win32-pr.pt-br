---
title: Propriedade IMsRdpClientTransportSettings3 GatewayAuthCookieServerAddr
description: O endereço do servidor para autenticação baseada em cookie.
ms.assetid: e00480cd-2133-42ff-8447-6c4234b56bf9
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade GatewayAuthCookieServerAddr
- Propriedade GatewayAuthCookieServerAddr Serviços de Área de Trabalho Remota, interface IMsRdpClientTransportSettings3
- Serviços de Área de Trabalho Remota de interface IMsRdpClientTransportSettings3, Propriedade GatewayAuthCookieServerAddr
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings3.GatewayAuthCookieServerAddr
- IMsRdpClientTransportSettings3.get_GatewayAuthCookieServerAddr
- IMsRdpClientTransportSettings3.put_GatewayAuthCookieServerAddr
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc238129d0bb9f698e90fc5e1de85e7257a4d16e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455921"
---
# <a name="imsrdpclienttransportsettings3gatewayauthcookieserveraddr-property"></a><span data-ttu-id="593eb-106">Propriedade IMsRdpClientTransportSettings3:: GatewayAuthCookieServerAddr</span><span class="sxs-lookup"><span data-stu-id="593eb-106">IMsRdpClientTransportSettings3::GatewayAuthCookieServerAddr property</span></span>

<span data-ttu-id="593eb-107">O endereço do servidor para autenticação baseada em cookie.</span><span class="sxs-lookup"><span data-stu-id="593eb-107">The server address for cookie-based authentication.</span></span>

<span data-ttu-id="593eb-108">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="593eb-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="593eb-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="593eb-109">Syntax</span></span>


```C++
HRESULT put_GatewayAuthCookieServerAddr(
  [in]          BSTR bstrProxyAuthCookieServerAddr
);

HRESULT get_GatewayAuthCookieServerAddr(
  [out, retval] BSTR *pbstrProxyAuthCookieServerAddr
);
```



## <a name="property-value"></a><span data-ttu-id="593eb-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="593eb-110">Property value</span></span>

<span data-ttu-id="593eb-111">O novo endereço do servidor para autenticação baseada em cookie.</span><span class="sxs-lookup"><span data-stu-id="593eb-111">The new server address for cookie-based authentication.</span></span>

## <a name="requirements"></a><span data-ttu-id="593eb-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="593eb-112">Requirements</span></span>



| <span data-ttu-id="593eb-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="593eb-113">Requirement</span></span> | <span data-ttu-id="593eb-114">Valor</span><span class="sxs-lookup"><span data-stu-id="593eb-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="593eb-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="593eb-115">Minimum supported client</span></span><br/> | <span data-ttu-id="593eb-116">Windows 7</span><span class="sxs-lookup"><span data-stu-id="593eb-116">Windows 7</span></span><br/>                                                                   |
| <span data-ttu-id="593eb-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="593eb-117">Minimum supported server</span></span><br/> | <span data-ttu-id="593eb-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="593eb-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="593eb-119">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="593eb-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="593eb-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="593eb-120"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="593eb-121">DLL</span><span class="sxs-lookup"><span data-stu-id="593eb-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="593eb-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="593eb-122"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="593eb-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="593eb-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="593eb-124">**IMsRdpClientTransportSettings3**</span><span class="sxs-lookup"><span data-stu-id="593eb-124">**IMsRdpClientTransportSettings3**</span></span>](imsrdpclienttransportsettings3.md)
</dt> </dl>

 

 





