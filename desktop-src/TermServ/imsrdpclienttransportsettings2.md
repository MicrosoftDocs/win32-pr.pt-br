---
title: Interface IMsRdpClientTransportSettings2
description: Gerencia as configurações de transporte do cliente para o servidor de gateway de Área de Trabalho Remota (gateway de área de trabalho remota). | Interface IMsRdpClientTransportSettings2
ms.assetid: 4f9f1905-2693-4666-9f6f-6e00b1eb6a0f
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de interface IMsRdpClientTransportSettings2
- Serviços de Área de Trabalho Remota da interface IMsRdpClientTransportSettings2, descrita
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings2
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f2f4887c6a4f55f3b9c97c389e9afd702d2ffab
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105780100"
---
# <a name="imsrdpclienttransportsettings2-interface"></a><span data-ttu-id="afdf7-106">Interface IMsRdpClientTransportSettings2</span><span class="sxs-lookup"><span data-stu-id="afdf7-106">IMsRdpClientTransportSettings2 interface</span></span>

<span data-ttu-id="afdf7-107">Gerencia as configurações de transporte do cliente para o servidor de gateway de Área de Trabalho Remota (gateway de área de trabalho remota).</span><span class="sxs-lookup"><span data-stu-id="afdf7-107">Manages client transport settings for the Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="members"></a><span data-ttu-id="afdf7-108">Membros</span><span class="sxs-lookup"><span data-stu-id="afdf7-108">Members</span></span>

<span data-ttu-id="afdf7-109">A interface **IMsRdpClientTransportSettings2** herda de [**IMsRdpClientTransportSettings**](imsrdpclienttransportsettings.md).</span><span class="sxs-lookup"><span data-stu-id="afdf7-109">The **IMsRdpClientTransportSettings2** interface inherits from [**IMsRdpClientTransportSettings**](imsrdpclienttransportsettings.md).</span></span> <span data-ttu-id="afdf7-110">**IMsRdpClientTransportSettings2** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="afdf7-110">**IMsRdpClientTransportSettings2** also has these types of members:</span></span>

-   [<span data-ttu-id="afdf7-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="afdf7-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="afdf7-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="afdf7-112">Properties</span></span>

<span data-ttu-id="afdf7-113">A interface **IMsRdpClientTransportSettings2** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="afdf7-113">The **IMsRdpClientTransportSettings2** interface has these properties.</span></span>



| <span data-ttu-id="afdf7-114">Propriedade</span><span class="sxs-lookup"><span data-stu-id="afdf7-114">Property</span></span>                                                                                                    | <span data-ttu-id="afdf7-115">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="afdf7-115">Access type</span></span>           | <span data-ttu-id="afdf7-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="afdf7-116">Description</span></span>                                                                                       |
|:------------------------------------------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="afdf7-117">**GatewayCredSharing**</span><span class="sxs-lookup"><span data-stu-id="afdf7-117">**GatewayCredSharing**</span></span>](imsrdpclienttransportsettings2-gatewaycredsharing.md)<br/>                  | <span data-ttu-id="afdf7-118">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="afdf7-118">Read/write</span></span><br/> | <span data-ttu-id="afdf7-119">Indica se o recurso de logon único para o gateway de área de trabalho remota está habilitado.</span><span class="sxs-lookup"><span data-stu-id="afdf7-119">Indicates whether the single sign-on feature for RD Gateway is enabled.</span></span><br/>                |
| [<span data-ttu-id="afdf7-120">**GatewayDomain**</span><span class="sxs-lookup"><span data-stu-id="afdf7-120">**GatewayDomain**</span></span>](imsrdpclienttransportsettings2-gatewaydomain.md)<br/>                            | <span data-ttu-id="afdf7-121">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="afdf7-121">Read/write</span></span><br/> | <span data-ttu-id="afdf7-122">O nome de domínio que um usuário fornece para se conectar ao servidor de gateway de área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="afdf7-122">The domain name that a user provides to connect to the RD Gateway server.</span></span><br/>              |
| [<span data-ttu-id="afdf7-123">**GatewayEncryptedOtpCookie**</span><span class="sxs-lookup"><span data-stu-id="afdf7-123">**GatewayEncryptedOtpCookie**</span></span>](imsrdpclienttransportsettings2-gatewaypreauthserveraddr.md)<br/>     | <span data-ttu-id="afdf7-124">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="afdf7-124">Read/write</span></span><br/> | <span data-ttu-id="afdf7-125">O cookie de OTP criptografado.</span><span class="sxs-lookup"><span data-stu-id="afdf7-125">The encrypted OTP cookie.</span></span><br/>                                                              |
| [<span data-ttu-id="afdf7-126">**GatewayEncryptedOtpCookieSize**</span><span class="sxs-lookup"><span data-stu-id="afdf7-126">**GatewayEncryptedOtpCookieSize**</span></span>](imsrdpclienttransportsettings2-gatewaypreauthserveraddr.md)<br/> | <span data-ttu-id="afdf7-127">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="afdf7-127">Read/write</span></span><br/> | <span data-ttu-id="afdf7-128">O tamanho, em bytes, do cookie de OTP criptografado.</span><span class="sxs-lookup"><span data-stu-id="afdf7-128">The size, in bytes, of the encrypted OTP cookie.</span></span><br/>                                       |
| [<span data-ttu-id="afdf7-129">**GatewayPassword**</span><span class="sxs-lookup"><span data-stu-id="afdf7-129">**GatewayPassword**</span></span>](imsrdpclienttransportsettings2-gatewaypassword.md)<br/>                        | <span data-ttu-id="afdf7-130">Somente gravação</span><span class="sxs-lookup"><span data-stu-id="afdf7-130">Write-only</span></span><br/> | <span data-ttu-id="afdf7-131">A senha que um usuário fornece para se conectar ao servidor de gateway de área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="afdf7-131">The password that a user provides to connect to the RD Gateway server.</span></span><br/>                 |
| [<span data-ttu-id="afdf7-132">**GatewayPreAuthRequirement**</span><span class="sxs-lookup"><span data-stu-id="afdf7-132">**GatewayPreAuthRequirement**</span></span>](imsrdpclienttransportsettings2-gatewaypreauthrequirement.md)<br/>    | <span data-ttu-id="afdf7-133">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="afdf7-133">Read/write</span></span><br/> | <span data-ttu-id="afdf7-134">Indica se o recurso de senha de uso único (OTP) do gateway de área de trabalho remota está habilitado.</span><span class="sxs-lookup"><span data-stu-id="afdf7-134">Indicates whether the RD Gateway one-time password (OTP) feature is enabled.</span></span><br/>           |
| [<span data-ttu-id="afdf7-135">**GatewayPreAuthServerAddr**</span><span class="sxs-lookup"><span data-stu-id="afdf7-135">**GatewayPreAuthServerAddr**</span></span>](imsrdpclienttransportsettings2-gatewaypreauthserveraddr.md)<br/>      | <span data-ttu-id="afdf7-136">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="afdf7-136">Read/write</span></span><br/> | <span data-ttu-id="afdf7-137">O endereço Web do servidor de pré-autenticação.</span><span class="sxs-lookup"><span data-stu-id="afdf7-137">The web address of the pre-authentication server.</span></span><br/>                                      |
| [<span data-ttu-id="afdf7-138">**GatewaySupportUrl**</span><span class="sxs-lookup"><span data-stu-id="afdf7-138">**GatewaySupportUrl**</span></span>](imsrdpclienttransportsettings2-gatewaypreauthserveraddr.md)<br/>             | <span data-ttu-id="afdf7-139">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="afdf7-139">Read/write</span></span><br/> | <span data-ttu-id="afdf7-140">O endereço Web do site que fornece suporte técnico para o servidor de gateway de área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="afdf7-140">The web address of the site that provides technical support for the RD Gateway server.</span></span><br/> |
| [<span data-ttu-id="afdf7-141">**GatewayUsername**</span><span class="sxs-lookup"><span data-stu-id="afdf7-141">**GatewayUsername**</span></span>](imsrdpclienttransportsettings2-gatewayusername.md)<br/>                        | <span data-ttu-id="afdf7-142">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="afdf7-142">Read/write</span></span><br/> | <span data-ttu-id="afdf7-143">O nome de usuário que um usuário fornece para se conectar ao servidor de gateway de área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="afdf7-143">The user name that a user provides to connect to the RD Gateway server.</span></span><br/>                |



 

## <a name="requirements"></a><span data-ttu-id="afdf7-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="afdf7-144">Requirements</span></span>



| <span data-ttu-id="afdf7-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="afdf7-145">Requirement</span></span> | <span data-ttu-id="afdf7-146">Valor</span><span class="sxs-lookup"><span data-stu-id="afdf7-146">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="afdf7-147">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="afdf7-147">Minimum supported client</span></span><br/> | <span data-ttu-id="afdf7-148">Windows Vista com SP1</span><span class="sxs-lookup"><span data-stu-id="afdf7-148">Windows Vista with SP1</span></span><br/>                                                                 |
| <span data-ttu-id="afdf7-149">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="afdf7-149">Minimum supported server</span></span><br/> | <span data-ttu-id="afdf7-150">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="afdf7-150">Windows Server 2008</span></span><br/>                                                                    |
| <span data-ttu-id="afdf7-151">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="afdf7-151">Type library</span></span><br/>             | <dl> <span data-ttu-id="afdf7-152"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="afdf7-152"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="afdf7-153">DLL</span><span class="sxs-lookup"><span data-stu-id="afdf7-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="afdf7-154"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="afdf7-154"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="afdf7-155">IID</span><span class="sxs-lookup"><span data-stu-id="afdf7-155">IID</span></span><br/>                      | <span data-ttu-id="afdf7-156">IID \_ IMsRdpClientTransportSettings2 é definido como 67341688-D606-4C73-A5D2-2E0489009319</span><span class="sxs-lookup"><span data-stu-id="afdf7-156">IID\_IMsRdpClientTransportSettings2 is defined as 67341688-D606-4c73-A5D2-2E0489009319</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="afdf7-157">Confira também</span><span class="sxs-lookup"><span data-stu-id="afdf7-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="afdf7-158">**IMsRdpClientTransportSettings**</span><span class="sxs-lookup"><span data-stu-id="afdf7-158">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> </dl>

 

 





