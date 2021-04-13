---
title: Propriedade IMsRdpClientTransportSettings2 GatewaySupportUrl
description: Especifica ou recupera o endereço Web do site que fornece suporte técnico para este servidor de Área de Trabalho Remota gateway (gateway de área de trabalho remota).
ms.assetid: e9c0f5ec-1b2f-4e09-8169-4316fd394443
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade GatewaySupportUrl
- Propriedade GatewaySupportUrl Serviços de Área de Trabalho Remota, interface IMsRdpClientTransportSettings2
- Serviços de Área de Trabalho Remota de interface IMsRdpClientTransportSettings2, Propriedade GatewaySupportUrl
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings2.GatewaySupportUrl
- IMsRdpClientTransportSettings2.get_GatewaySupportUrl
- IMsRdpClientTransportSettings2.put_GatewaySupportUrl
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4212dd03d5fb217753e14c2869973bda87476367
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369368"
---
# <a name="imsrdpclienttransportsettings2gatewaysupporturl-property"></a><span data-ttu-id="45847-106">Propriedade IMsRdpClientTransportSettings2:: GatewaySupportUrl</span><span class="sxs-lookup"><span data-stu-id="45847-106">IMsRdpClientTransportSettings2::GatewaySupportUrl property</span></span>

<span data-ttu-id="45847-107">Especifica ou recupera o endereço Web do site que fornece suporte técnico para este servidor de Área de Trabalho Remota gateway (gateway de área de trabalho remota).</span><span class="sxs-lookup"><span data-stu-id="45847-107">Specifies or retrieves the web address of the site that provides technical support for this Remote Desktop Gateway (RD Gateway) server.</span></span>

<span data-ttu-id="45847-108">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="45847-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="45847-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="45847-109">Syntax</span></span>


```C++
HRESULT put_GatewaySupportUrl(
  [in]  BSTR bstrProxySupportUrl
);

HRESULT get_GatewaySupportUrl(
  [out] BSTR *pbstrProxySupportUrl
);
```



## <a name="property-value"></a><span data-ttu-id="45847-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="45847-110">Property value</span></span>

<span data-ttu-id="45847-111">Especifica ou recupera o endereço Web do site que fornece suporte técnico para este servidor de gateway de área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="45847-111">Specifies or retrieves the web address of the site that provides technical support for this RD Gateway server.</span></span>

## <a name="requirements"></a><span data-ttu-id="45847-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="45847-112">Requirements</span></span>



| <span data-ttu-id="45847-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="45847-113">Requirement</span></span> | <span data-ttu-id="45847-114">Valor</span><span class="sxs-lookup"><span data-stu-id="45847-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45847-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="45847-115">Minimum supported client</span></span><br/> | <span data-ttu-id="45847-116">Windows Vista com SP1</span><span class="sxs-lookup"><span data-stu-id="45847-116">Windows Vista with SP1</span></span><br/>                                                                 |
| <span data-ttu-id="45847-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="45847-117">Minimum supported server</span></span><br/> | <span data-ttu-id="45847-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="45847-118">Windows Server 2008</span></span><br/>                                                                    |
| <span data-ttu-id="45847-119">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="45847-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="45847-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="45847-120"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="45847-121">DLL</span><span class="sxs-lookup"><span data-stu-id="45847-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="45847-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="45847-122"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="45847-123">IID</span><span class="sxs-lookup"><span data-stu-id="45847-123">IID</span></span><br/>                      | <span data-ttu-id="45847-124">IID \_ IMsRdpClientTransportSettings2 é definido como 67341688-D606-4C73-A5D2-2E0489009319</span><span class="sxs-lookup"><span data-stu-id="45847-124">IID\_IMsRdpClientTransportSettings2 is defined as 67341688-D606-4c73-A5D2-2E0489009319</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="45847-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="45847-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45847-126">**IMsRdpClientTransportSettings**</span><span class="sxs-lookup"><span data-stu-id="45847-126">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> <dt>

[<span data-ttu-id="45847-127">**IMsRdpClientTransportSettings2**</span><span class="sxs-lookup"><span data-stu-id="45847-127">**IMsRdpClientTransportSettings2**</span></span>](imsrdpclienttransportsettings2.md)
</dt> </dl>

 

 





