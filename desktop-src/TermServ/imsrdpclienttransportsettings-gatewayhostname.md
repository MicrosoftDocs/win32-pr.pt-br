---
title: Propriedade IMsRdpClientTransportSettings GatewayHostname
description: Especifica o nome do host do servidor de gateway de Área de Trabalho Remota (gateway de área de trabalho remota).
ms.assetid: 34c4b3b7-3768-4d98-b1e8-7fcb8f9c758d
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade GatewayHostname
- Propriedade GatewayHostname Serviços de Área de Trabalho Remota, interface IMsRdpClientTransportSettings
- Serviços de Área de Trabalho Remota de interface IMsRdpClientTransportSettings, Propriedade GatewayHostname
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings.GatewayHostname
- IMsRdpClientTransportSettings.get_GatewayHostname
- IMsRdpClientTransportSettings.put_GatewayHostname
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03835faf48fa8aba557f82da158fdba827a84831
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104294773"
---
# <a name="imsrdpclienttransportsettingsgatewayhostname-property"></a><span data-ttu-id="955fe-106">Propriedade IMsRdpClientTransportSettings:: GatewayHostname</span><span class="sxs-lookup"><span data-stu-id="955fe-106">IMsRdpClientTransportSettings::GatewayHostname property</span></span>

<span data-ttu-id="955fe-107">Especifica o nome do host do servidor de gateway de Área de Trabalho Remota (gateway de área de trabalho remota).</span><span class="sxs-lookup"><span data-stu-id="955fe-107">Specifies the host name of the Remote Desktop Gateway (RD Gateway) server.</span></span>

<span data-ttu-id="955fe-108">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="955fe-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="955fe-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="955fe-109">Syntax</span></span>


```C++
HRESULT put_GatewayHostname(
  [in]  BSTR newVal
);

HRESULT get_GatewayHostname(
  [out] BSTR *pProxyHostname
);
```



## <a name="property-value"></a><span data-ttu-id="955fe-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="955fe-110">Property value</span></span>

<span data-ttu-id="955fe-111">Uma cadeia de caracteres que contém o nome do host do servidor de gateway RD.</span><span class="sxs-lookup"><span data-stu-id="955fe-111">A string that contains the RD Gateway server host name.</span></span>

## <a name="error-codes"></a><span data-ttu-id="955fe-112">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="955fe-112">Error codes</span></span>

<span data-ttu-id="955fe-113">Retornará **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="955fe-113">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="955fe-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="955fe-114">Requirements</span></span>



| <span data-ttu-id="955fe-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="955fe-115">Requirement</span></span> | <span data-ttu-id="955fe-116">Valor</span><span class="sxs-lookup"><span data-stu-id="955fe-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="955fe-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="955fe-117">Minimum supported client</span></span><br/> | <span data-ttu-id="955fe-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="955fe-118">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="955fe-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="955fe-119">Minimum supported server</span></span><br/> | <span data-ttu-id="955fe-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="955fe-120">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="955fe-121">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="955fe-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="955fe-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="955fe-122"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="955fe-123">DLL</span><span class="sxs-lookup"><span data-stu-id="955fe-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="955fe-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="955fe-124"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="955fe-125">IID</span><span class="sxs-lookup"><span data-stu-id="955fe-125">IID</span></span><br/>                      | <span data-ttu-id="955fe-126">IID \_ IMsRdpClientTransportSettings é definido como 720298C0-A099-46f5-9F82-96921BAE4701</span><span class="sxs-lookup"><span data-stu-id="955fe-126">IID\_IMsRdpClientTransportSettings is defined as 720298C0-A099-46f5-9F82-96921BAE4701</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="955fe-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="955fe-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="955fe-128">**IMsRdpClientTransportSettings**</span><span class="sxs-lookup"><span data-stu-id="955fe-128">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> </dl>

 

 





