---
title: Propriedade IMsRdpClientTransportSettings2 GatewayCredSharing
description: Especifica ou recupera a configuração para se o recurso de compartilhamento de credenciais do gateway de Área de Trabalho Remota (Gateway RD) está habilitado.
ms.assetid: 296dc578-376d-41f6-988a-286fe744959f
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade GatewayCredSharing
- Propriedade GatewayCredSharing Serviços de Área de Trabalho Remota, interface IMsRdpClientTransportSettings2
- Serviços de Área de Trabalho Remota de interface IMsRdpClientTransportSettings2, Propriedade GatewayCredSharing
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings2.GatewayCredSharing
- IMsRdpClientTransportSettings2.get_GatewayCredSharing
- IMsRdpClientTransportSettings2.put_GatewayCredSharing
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 329e425631b674e050f246c4105115bd4326be3d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454783"
---
# <a name="imsrdpclienttransportsettings2gatewaycredsharing-property"></a><span data-ttu-id="0e184-106">Propriedade IMsRdpClientTransportSettings2:: GatewayCredSharing</span><span class="sxs-lookup"><span data-stu-id="0e184-106">IMsRdpClientTransportSettings2::GatewayCredSharing property</span></span>

<span data-ttu-id="0e184-107">Especifica ou recupera a configuração para se o recurso de compartilhamento de credenciais do gateway de Área de Trabalho Remota (Gateway RD) está habilitado.</span><span class="sxs-lookup"><span data-stu-id="0e184-107">Specifies or retrieves the setting for whether the Remote Desktop Gateway (RD Gateway) credential sharing feature is enabled.</span></span> <span data-ttu-id="0e184-108">Quando o recurso está habilitado, o controle ActiveX Área de Trabalho Remota tenta usar as mesmas credenciais para autenticar o servidor de Host da Sessão da Área de Trabalho Remota (Host da Sessão RD) e o servidor de gateway de área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="0e184-108">When the feature is enabled, the Remote Desktop ActiveX control tries to use the same credentials to authenticate to the Remote Desktop Session Host (RD Session Host) server and to the RD Gateway server.</span></span>

<span data-ttu-id="0e184-109">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="0e184-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e184-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="0e184-110">Syntax</span></span>


```C++
HRESULT put_GatewayCredSharing(
  [in]  ULONG ulProxyCredSharing
);

HRESULT get_GatewayCredSharing(
  [out] ULONG *pulProxyCredSharing
);
```



## <a name="property-value"></a><span data-ttu-id="0e184-111">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="0e184-111">Property value</span></span>

<span data-ttu-id="0e184-112">Se definido como um, o compartilhamento de credenciais está habilitado.</span><span class="sxs-lookup"><span data-stu-id="0e184-112">If set to one, credential sharing is enabled.</span></span> <span data-ttu-id="0e184-113">Se definido como zero, o compartilhamento de credenciais será desabilitado.</span><span class="sxs-lookup"><span data-stu-id="0e184-113">If set to zero, credential sharing is disabled.</span></span>

## <a name="error-codes"></a><span data-ttu-id="0e184-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="0e184-114">Error codes</span></span>

<span data-ttu-id="0e184-115">Retornará **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="0e184-115">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="0e184-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="0e184-116">Remarks</span></span>

<span data-ttu-id="0e184-117">Essa propriedade é usada pelo controle ActiveX para implementar um único prompt para o compartilhamento de credenciais entre o servidor de Host da Sessão RD e o servidor de gateway de área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="0e184-117">This property is used by the ActiveX control to implement a single prompt for credential sharing between the RD Session Host server and the RD Gateway server.</span></span> <span data-ttu-id="0e184-118">O compartilhamento de credenciais não oferece suporte ao compartilhamento de senha baseado na Web com [**GatewayPassword**](imsrdpclienttransportsettings2-gatewaypassword.md) ou [**clearTextPassword**](imstscnonscriptable-cleartextpassword.md).</span><span class="sxs-lookup"><span data-stu-id="0e184-118">Credential sharing does not support web-based password sharing with [**GatewayPassword**](imsrdpclienttransportsettings2-gatewaypassword.md) or [**ClearTextPassword**](imstscnonscriptable-cleartextpassword.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0e184-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0e184-119">Requirements</span></span>



| <span data-ttu-id="0e184-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="0e184-120">Requirement</span></span> | <span data-ttu-id="0e184-121">Valor</span><span class="sxs-lookup"><span data-stu-id="0e184-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e184-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0e184-122">Minimum supported client</span></span><br/> | <span data-ttu-id="0e184-123">Windows Vista com SP1</span><span class="sxs-lookup"><span data-stu-id="0e184-123">Windows Vista with SP1</span></span><br/>                                                                 |
| <span data-ttu-id="0e184-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0e184-124">Minimum supported server</span></span><br/> | <span data-ttu-id="0e184-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0e184-125">Windows Server 2008</span></span><br/>                                                                    |
| <span data-ttu-id="0e184-126">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="0e184-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="0e184-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0e184-127"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="0e184-128">DLL</span><span class="sxs-lookup"><span data-stu-id="0e184-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0e184-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0e184-129"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="0e184-130">IID</span><span class="sxs-lookup"><span data-stu-id="0e184-130">IID</span></span><br/>                      | <span data-ttu-id="0e184-131">IID \_ IMsRdpClientTransportSettings2 é definido como 67341688-D606-4C73-A5D2-2E0489009319</span><span class="sxs-lookup"><span data-stu-id="0e184-131">IID\_IMsRdpClientTransportSettings2 is defined as 67341688-D606-4c73-A5D2-2E0489009319</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0e184-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="0e184-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e184-133">**IMsRdpClientTransportSettings**</span><span class="sxs-lookup"><span data-stu-id="0e184-133">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> <dt>

[<span data-ttu-id="0e184-134">**IMsRdpClientTransportSettings2**</span><span class="sxs-lookup"><span data-stu-id="0e184-134">**IMsRdpClientTransportSettings2**</span></span>](imsrdpclienttransportsettings2.md)
</dt> </dl>

 

 





