---
title: Propriedade IMsRdpClientTransportSettings2 GatewayPreAuthServerAddr
description: Especifica ou recupera o endereço Web do servidor de pré-autenticação, que é usado para o recurso de senha única (OTP) do gateway de Área de Trabalho Remota (Gateway RD).
ms.assetid: 14edad82-ab19-46fe-b878-d34298763c56
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade GatewayPreAuthServerAddr
- Propriedade GatewayPreAuthServerAddr Serviços de Área de Trabalho Remota, interface IMsRdpClientTransportSettings2
- Serviços de Área de Trabalho Remota de interface IMsRdpClientTransportSettings2, Propriedade GatewayPreAuthServerAddr
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings2.GatewayPreAuthServerAddr
- IMsRdpClientTransportSettings2.get_GatewayPreAuthServerAddr
- IMsRdpClientTransportSettings2.put_GatewayPreAuthServerAddr
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95d6fe2f397b0d445a6300d68a89b210debd449a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369369"
---
# <a name="imsrdpclienttransportsettings2gatewaypreauthserveraddr-property"></a><span data-ttu-id="a1756-106">Propriedade IMsRdpClientTransportSettings2:: GatewayPreAuthServerAddr</span><span class="sxs-lookup"><span data-stu-id="a1756-106">IMsRdpClientTransportSettings2::GatewayPreAuthServerAddr property</span></span>

<span data-ttu-id="a1756-107">Especifica ou recupera o endereço Web do servidor de pré-autenticação, que é usado para o recurso de senha única (OTP) do gateway de Área de Trabalho Remota (Gateway RD).</span><span class="sxs-lookup"><span data-stu-id="a1756-107">Specifies or retrieves the web address of the pre-authentication server, which is used for the Remote Desktop Gateway (RD Gateway) one-time password (OTP) feature.</span></span>

<span data-ttu-id="a1756-108">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="a1756-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1756-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="a1756-109">Syntax</span></span>


```C++
HRESULT put_GatewayPreAuthServerAddr(
  [in]  BSTR bstrProxyPreAuthServerAddr
);

HRESULT get_GatewayPreAuthServerAddr(
  [out] BSTR *pbstrProxyPreAuthServerAddr
);
```



## <a name="property-value"></a><span data-ttu-id="a1756-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="a1756-110">Property value</span></span>

<span data-ttu-id="a1756-111">O endereço Web do servidor de pré-autenticação; por exemplo, o endereço Web do Microsoft Internet Security and Acceleration (ISA) Server.</span><span class="sxs-lookup"><span data-stu-id="a1756-111">The web address of the pre-authentication server; for example, the web address of the Microsoft Internet Security and Acceleration (ISA) server.</span></span> <span data-ttu-id="a1756-112">Especifique o endereço Web usando o formato "https://*hostname*. *Nomedodomínio*. com/*WebSiteName*"ou"*nome do host* https://. *Nomedodomínio*. com/*WebSiteName*".</span><span class="sxs-lookup"><span data-stu-id="a1756-112">Specify the web address by using the format "https://*HostName*.*DomainName*.com/*WebsiteName*" or "https://*HostName*.*DomainName*.com/*WebsiteName*".</span></span>

## <a name="error-codes"></a><span data-ttu-id="a1756-113">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="a1756-113">Error codes</span></span>

<span data-ttu-id="a1756-114">Retornará **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="a1756-114">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1756-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a1756-115">Requirements</span></span>



| <span data-ttu-id="a1756-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="a1756-116">Requirement</span></span> | <span data-ttu-id="a1756-117">Valor</span><span class="sxs-lookup"><span data-stu-id="a1756-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1756-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a1756-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a1756-119">Windows Vista com SP1</span><span class="sxs-lookup"><span data-stu-id="a1756-119">Windows Vista with SP1</span></span><br/>                                                                 |
| <span data-ttu-id="a1756-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a1756-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a1756-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a1756-121">Windows Server 2008</span></span><br/>                                                                    |
| <span data-ttu-id="a1756-122">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="a1756-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="a1756-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a1756-123"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="a1756-124">DLL</span><span class="sxs-lookup"><span data-stu-id="a1756-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a1756-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a1756-125"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="a1756-126">IID</span><span class="sxs-lookup"><span data-stu-id="a1756-126">IID</span></span><br/>                      | <span data-ttu-id="a1756-127">IID \_ IMsRdpClientTransportSettings2 é definido como 67341688-D606-4C73-A5D2-2E0489009319</span><span class="sxs-lookup"><span data-stu-id="a1756-127">IID\_IMsRdpClientTransportSettings2 is defined as 67341688-D606-4c73-A5D2-2E0489009319</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a1756-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="a1756-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1756-129">**IMsRdpClientTransportSettings**</span><span class="sxs-lookup"><span data-stu-id="a1756-129">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> <dt>

[<span data-ttu-id="a1756-130">**IMsRdpClientTransportSettings2**</span><span class="sxs-lookup"><span data-stu-id="a1756-130">**IMsRdpClientTransportSettings2**</span></span>](imsrdpclienttransportsettings2.md)
</dt> </dl>

 

 





