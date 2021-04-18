---
title: Propriedade IMsRdpClientTransportSettings3 GatewayCredSourceCookie
description: Especifica se a origem da credencial é baseada em cookie.
ms.assetid: 039459a3-7a83-444c-a0b4-46ef0dc5ddd0
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade GatewayCredSourceCookie
- Propriedade GatewayCredSourceCookie Serviços de Área de Trabalho Remota, interface IMsRdpClientTransportSettings3
- Serviços de Área de Trabalho Remota de interface IMsRdpClientTransportSettings3, Propriedade GatewayCredSourceCookie
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings3.GatewayCredSourceCookie
- IMsRdpClientTransportSettings3.get_GatewayCredSourceCookie
- IMsRdpClientTransportSettings3.put_GatewayCredSourceCookie
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9547df10ce9f528a4b52c526c970a82d0bd098c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105756809"
---
# <a name="imsrdpclienttransportsettings3gatewaycredsourcecookie-property"></a><span data-ttu-id="3c461-106">Propriedade IMsRdpClientTransportSettings3:: GatewayCredSourceCookie</span><span class="sxs-lookup"><span data-stu-id="3c461-106">IMsRdpClientTransportSettings3::GatewayCredSourceCookie property</span></span>

<span data-ttu-id="3c461-107">Especifica se a origem da credencial é baseada em cookie.</span><span class="sxs-lookup"><span data-stu-id="3c461-107">Specifies if the credential source is cookie based.</span></span> <span data-ttu-id="3c461-108">Contém um se a origem da credencial for baseada em cookie ou for zero caso contrário.</span><span class="sxs-lookup"><span data-stu-id="3c461-108">Contains one if the credential source is cookie-based or zero otherwise.</span></span>

<span data-ttu-id="3c461-109">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="3c461-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c461-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3c461-110">Syntax</span></span>


```C++
HRESULT put_GatewayCredSourceCookie(
  [in]          ULONG ulProxyCredSourceCookie
);

HRESULT get_GatewayCredSourceCookie(
  [out, retval] ULONG *pulProxyCredSourceCookie
);
```



## <a name="property-value"></a><span data-ttu-id="3c461-111">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="3c461-111">Property value</span></span>

<span data-ttu-id="3c461-112">Um valor **ULONG** que especifica se a origem da credencial é baseada em cookie.</span><span class="sxs-lookup"><span data-stu-id="3c461-112">A **ULONG** value that specifies if the credential source is cookie based.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c461-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3c461-113">Requirements</span></span>



| <span data-ttu-id="3c461-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c461-114">Requirement</span></span> | <span data-ttu-id="3c461-115">Valor</span><span class="sxs-lookup"><span data-stu-id="3c461-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3c461-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3c461-116">Minimum supported client</span></span><br/> | <span data-ttu-id="3c461-117">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3c461-117">Windows 7</span></span><br/>                                                                   |
| <span data-ttu-id="3c461-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3c461-118">Minimum supported server</span></span><br/> | <span data-ttu-id="3c461-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3c461-119">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="3c461-120">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="3c461-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="3c461-121"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3c461-121"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="3c461-122">DLL</span><span class="sxs-lookup"><span data-stu-id="3c461-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3c461-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3c461-123"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c461-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="3c461-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c461-125">**IMsRdpClientTransportSettings3**</span><span class="sxs-lookup"><span data-stu-id="3c461-125">**IMsRdpClientTransportSettings3**</span></span>](imsrdpclienttransportsettings3.md)
</dt> </dl>

 

 





