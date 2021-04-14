---
title: Propriedade IMsRdpClientTransportSettings GatewayIsSupported
description: Especifica se há suporte para o gateway de Área de Trabalho Remota (Gateway RD).
ms.assetid: 31edd35b-251d-404d-bec8-e082bb2427b3
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade GatewayIsSupported
- Propriedade GatewayIsSupported Serviços de Área de Trabalho Remota, interface IMsRdpClientTransportSettings
- Serviços de Área de Trabalho Remota de interface IMsRdpClientTransportSettings, Propriedade GatewayIsSupported
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings.GatewayIsSupported
- IMsRdpClientTransportSettings.get_GatewayIsSupported
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de79033c2ab9bae73aae4213e72a54590170a184
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369229"
---
# <a name="imsrdpclienttransportsettingsgatewayissupported-property"></a><span data-ttu-id="67fa1-106">Propriedade IMsRdpClientTransportSettings:: GatewayIsSupported</span><span class="sxs-lookup"><span data-stu-id="67fa1-106">IMsRdpClientTransportSettings::GatewayIsSupported property</span></span>

<span data-ttu-id="67fa1-107">Especifica se há suporte para o gateway de Área de Trabalho Remota (Gateway RD).</span><span class="sxs-lookup"><span data-stu-id="67fa1-107">Specifies whether Remote Desktop Gateway (RD Gateway) is supported.</span></span>

<span data-ttu-id="67fa1-108">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="67fa1-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="67fa1-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="67fa1-109">Syntax</span></span>


```C++
HRESULT get_GatewayIsSupported(
  [out] BOOL *pfProxyIsSupported
);
```



## <a name="property-value"></a><span data-ttu-id="67fa1-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="67fa1-110">Property value</span></span>

<span data-ttu-id="67fa1-111">Especifica se o Gateway RD tem suporte.</span><span class="sxs-lookup"><span data-stu-id="67fa1-111">Specifies whether RD Gateway is supported.</span></span>

## <a name="error-codes"></a><span data-ttu-id="67fa1-112">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="67fa1-112">Error codes</span></span>

<span data-ttu-id="67fa1-113">Retornará **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="67fa1-113">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="67fa1-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="67fa1-114">Requirements</span></span>



| <span data-ttu-id="67fa1-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="67fa1-115">Requirement</span></span> | <span data-ttu-id="67fa1-116">Valor</span><span class="sxs-lookup"><span data-stu-id="67fa1-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67fa1-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="67fa1-117">Minimum supported client</span></span><br/> | <span data-ttu-id="67fa1-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="67fa1-118">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="67fa1-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="67fa1-119">Minimum supported server</span></span><br/> | <span data-ttu-id="67fa1-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="67fa1-120">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="67fa1-121">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="67fa1-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="67fa1-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="67fa1-122"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="67fa1-123">DLL</span><span class="sxs-lookup"><span data-stu-id="67fa1-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="67fa1-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="67fa1-124"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="67fa1-125">IID</span><span class="sxs-lookup"><span data-stu-id="67fa1-125">IID</span></span><br/>                      | <span data-ttu-id="67fa1-126">IID \_ IMsRdpClientTransportSettings é definido como 720298C0-A099-46f5-9F82-96921BAE4701</span><span class="sxs-lookup"><span data-stu-id="67fa1-126">IID\_IMsRdpClientTransportSettings is defined as 720298C0-A099-46f5-9F82-96921BAE4701</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="67fa1-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="67fa1-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67fa1-128">**IMsRdpClientTransportSettings**</span><span class="sxs-lookup"><span data-stu-id="67fa1-128">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> </dl>

 

 





