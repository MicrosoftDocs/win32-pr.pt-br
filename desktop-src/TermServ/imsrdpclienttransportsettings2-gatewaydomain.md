---
title: Propriedade IMsRdpClientTransportSettings2 GatewayDomain
description: Especifica ou recupera o nome de domínio de um usuário que é fornecido para o servidor de gateway de Área de Trabalho Remota (gateway de área de trabalho remota).
ms.assetid: 792ff7c6-afeb-4a2a-86b4-7722513a08e0
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade GatewayDomain
- Propriedade GatewayDomain Serviços de Área de Trabalho Remota, interface IMsRdpClientTransportSettings2
- Serviços de Área de Trabalho Remota de interface IMsRdpClientTransportSettings2, Propriedade GatewayDomain
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings2.GatewayDomain
- IMsRdpClientTransportSettings2.get_GatewayDomain
- IMsRdpClientTransportSettings2.put_GatewayDomain
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5088780fbbaa4ab86fc416a3e9aa353920cc25e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369370"
---
# <a name="imsrdpclienttransportsettings2gatewaydomain-property"></a><span data-ttu-id="11811-106">Propriedade IMsRdpClientTransportSettings2:: GatewayDomain</span><span class="sxs-lookup"><span data-stu-id="11811-106">IMsRdpClientTransportSettings2::GatewayDomain property</span></span>

<span data-ttu-id="11811-107">Especifica ou recupera o nome de domínio de um usuário que é fornecido para o servidor de gateway de Área de Trabalho Remota (gateway de área de trabalho remota).</span><span class="sxs-lookup"><span data-stu-id="11811-107">Specifies or retrieves the domain name of a user that is provided to the Remote Desktop Gateway (RD Gateway) server.</span></span>

<span data-ttu-id="11811-108">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="11811-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="11811-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="11811-109">Syntax</span></span>


```C++
HRESULT put_GatewayDomain(
  [in]  BSTR proxyDomain
);

HRESULT get_GatewayDomain(
  [out] BSTR *pProxyDomain
);
```



## <a name="property-value"></a><span data-ttu-id="11811-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="11811-110">Property value</span></span>

<span data-ttu-id="11811-111">O nome de domínio que é fornecido para se conectar ao servidor de gateway de área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="11811-111">The domain name that is provided to connect to the RD Gateway server.</span></span>

## <a name="error-codes"></a><span data-ttu-id="11811-112">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="11811-112">Error codes</span></span>

<span data-ttu-id="11811-113">Retornará **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="11811-113">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="11811-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="11811-114">Requirements</span></span>



| <span data-ttu-id="11811-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="11811-115">Requirement</span></span> | <span data-ttu-id="11811-116">Valor</span><span class="sxs-lookup"><span data-stu-id="11811-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11811-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="11811-117">Minimum supported client</span></span><br/> | <span data-ttu-id="11811-118">Windows Vista com SP1</span><span class="sxs-lookup"><span data-stu-id="11811-118">Windows Vista with SP1</span></span><br/>                                                                 |
| <span data-ttu-id="11811-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="11811-119">Minimum supported server</span></span><br/> | <span data-ttu-id="11811-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="11811-120">Windows Server 2008</span></span><br/>                                                                    |
| <span data-ttu-id="11811-121">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="11811-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="11811-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="11811-122"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="11811-123">DLL</span><span class="sxs-lookup"><span data-stu-id="11811-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="11811-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="11811-124"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="11811-125">IID</span><span class="sxs-lookup"><span data-stu-id="11811-125">IID</span></span><br/>                      | <span data-ttu-id="11811-126">IID \_ IMsRdpClientTransportSettings2 é definido como 67341688-D606-4C73-A5D2-2E0489009319</span><span class="sxs-lookup"><span data-stu-id="11811-126">IID\_IMsRdpClientTransportSettings2 is defined as 67341688-D606-4c73-A5D2-2E0489009319</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="11811-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="11811-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11811-128">**IMsRdpClientTransportSettings**</span><span class="sxs-lookup"><span data-stu-id="11811-128">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> <dt>

[<span data-ttu-id="11811-129">**IMsRdpClientTransportSettings2**</span><span class="sxs-lookup"><span data-stu-id="11811-129">**IMsRdpClientTransportSettings2**</span></span>](imsrdpclienttransportsettings2.md)
</dt> </dl>

 

 





