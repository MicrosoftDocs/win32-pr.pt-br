---
title: Propriedade IMsRdpClientTransportSettings2 GatewayPreAuthRequirement
description: Especifica ou recupera a configuração para se o recurso de senha de uso único (OTP) do gateway de Área de Trabalho Remota (Gateway RD) está habilitado.
ms.assetid: cc8f7ebb-16ba-45ed-ba66-de4a339946d0
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade GatewayPreAuthRequirement
- Propriedade GatewayPreAuthRequirement Serviços de Área de Trabalho Remota, interface IMsRdpClientTransportSettings2
- Serviços de Área de Trabalho Remota de interface IMsRdpClientTransportSettings2, Propriedade GatewayPreAuthRequirement
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings2.GatewayPreAuthRequirement
- IMsRdpClientTransportSettings2.get_GatewayPreAuthRequirement
- IMsRdpClientTransportSettings2.put_GatewayPreAuthRequirement
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 058ca92237a4f9729f526030f5f8a836ce1c739c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499762"
---
# <a name="imsrdpclienttransportsettings2gatewaypreauthrequirement-property"></a><span data-ttu-id="6f4a3-106">Propriedade IMsRdpClientTransportSettings2:: GatewayPreAuthRequirement</span><span class="sxs-lookup"><span data-stu-id="6f4a3-106">IMsRdpClientTransportSettings2::GatewayPreAuthRequirement property</span></span>

<span data-ttu-id="6f4a3-107">Especifica ou recupera a configuração para se o recurso de senha de uso único (OTP) do gateway de Área de Trabalho Remota (Gateway RD) está habilitado.</span><span class="sxs-lookup"><span data-stu-id="6f4a3-107">Specifies or retrieves the setting for whether the Remote Desktop Gateway (RD Gateway) one-time password (OTP) feature is enabled.</span></span>

<span data-ttu-id="6f4a3-108">Quando a OTP está habilitada, o **GatewayPreAuthRequirement** tenta consultar o cookie de OTP do armazenamento de cookies da Internet usando a propriedade [**GatewayPreAuthServerAddr**](imsrdpclienttransportsettings2-gatewaypreauthserveraddr.md) .</span><span class="sxs-lookup"><span data-stu-id="6f4a3-108">When OTP is enabled, **GatewayPreAuthRequirement** tries to query the OTP cookie from the Internet cookie store by using the [**GatewayPreAuthServerAddr**](imsrdpclienttransportsettings2-gatewaypreauthserveraddr.md) property.</span></span> <span data-ttu-id="6f4a3-109">Se for bem-sucedido, o **GatewayPreAuthRequirement** enviará o cookie de OTP para o servidor de firewall (como o Microsoft Internet Security and Acceleration \[ ISA \] Server) para pré-autenticação.</span><span class="sxs-lookup"><span data-stu-id="6f4a3-109">If successful, **GatewayPreAuthRequirement** sends the OTP cookie to the firewall server (such as Microsoft Internet Security and Acceleration \[ISA\] server) for pre-authentication.</span></span>

<span data-ttu-id="6f4a3-110">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="6f4a3-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f4a3-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="6f4a3-111">Syntax</span></span>


```C++
HRESULT put_GatewayPreAuthRequirement(
  [in]  ULONG ulProxyPreAuthRequirement
);

HRESULT get_GatewayPreAuthRequirement(
  [out] ULONG *pulProxyPreAuthRequirement
);
```



## <a name="property-value"></a><span data-ttu-id="6f4a3-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="6f4a3-112">Property value</span></span>

<span data-ttu-id="6f4a3-113">Se definido como 1, o recurso de OTP será habilitado.</span><span class="sxs-lookup"><span data-stu-id="6f4a3-113">If set to 1, the OTP feature is enabled.</span></span> <span data-ttu-id="6f4a3-114">Se definido como 0, o recurso de OTP será desabilitado.</span><span class="sxs-lookup"><span data-stu-id="6f4a3-114">If set to 0, the OTP feature is disabled.</span></span>

## <a name="error-codes"></a><span data-ttu-id="6f4a3-115">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="6f4a3-115">Error codes</span></span>

<span data-ttu-id="6f4a3-116">Retornará **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="6f4a3-116">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="6f4a3-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6f4a3-117">Requirements</span></span>



| <span data-ttu-id="6f4a3-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f4a3-118">Requirement</span></span> | <span data-ttu-id="6f4a3-119">Valor</span><span class="sxs-lookup"><span data-stu-id="6f4a3-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f4a3-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6f4a3-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6f4a3-121">Windows Vista com SP1</span><span class="sxs-lookup"><span data-stu-id="6f4a3-121">Windows Vista with SP1</span></span><br/>                                                                 |
| <span data-ttu-id="6f4a3-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6f4a3-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6f4a3-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6f4a3-123">Windows Server 2008</span></span><br/>                                                                    |
| <span data-ttu-id="6f4a3-124">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="6f4a3-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="6f4a3-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6f4a3-125"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="6f4a3-126">DLL</span><span class="sxs-lookup"><span data-stu-id="6f4a3-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6f4a3-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6f4a3-127"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="6f4a3-128">IID</span><span class="sxs-lookup"><span data-stu-id="6f4a3-128">IID</span></span><br/>                      | <span data-ttu-id="6f4a3-129">IID \_ IMsRdpClientTransportSettings2 é definido como 67341688-D606-4C73-A5D2-2E0489009319</span><span class="sxs-lookup"><span data-stu-id="6f4a3-129">IID\_IMsRdpClientTransportSettings2 is defined as 67341688-D606-4c73-A5D2-2E0489009319</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6f4a3-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="6f4a3-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f4a3-131">**IMsRdpClientTransportSettings**</span><span class="sxs-lookup"><span data-stu-id="6f4a3-131">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> <dt>

[<span data-ttu-id="6f4a3-132">**IMsRdpClientTransportSettings2**</span><span class="sxs-lookup"><span data-stu-id="6f4a3-132">**IMsRdpClientTransportSettings2**</span></span>](imsrdpclienttransportsettings2.md)
</dt> </dl>

 

 





