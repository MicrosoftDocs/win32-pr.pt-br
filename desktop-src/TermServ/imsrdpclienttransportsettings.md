---
title: Interface IMsRdpClientTransportSettings
description: Gerencia as configurações de transporte do cliente para o servidor de gateway de Área de Trabalho Remota (gateway de área de trabalho remota). | Interface IMsRdpClientTransportSettings
ms.assetid: d2573727-1dcc-4d4d-af5c-038e9467ba84
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de interface IMsRdpClientTransportSettings
- Serviços de Área de Trabalho Remota da interface IMsRdpClientTransportSettings, descrita
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec240d008ef2f9469fb67f4041cfb33c08383079
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105813031"
---
# <a name="imsrdpclienttransportsettings-interface"></a><span data-ttu-id="950b1-106">Interface IMsRdpClientTransportSettings</span><span class="sxs-lookup"><span data-stu-id="950b1-106">IMsRdpClientTransportSettings interface</span></span>

<span data-ttu-id="950b1-107">Gerencia as configurações de transporte do cliente para o servidor de gateway de Área de Trabalho Remota (gateway de área de trabalho remota).</span><span class="sxs-lookup"><span data-stu-id="950b1-107">Manages client transport settings for the Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="members"></a><span data-ttu-id="950b1-108">Membros</span><span class="sxs-lookup"><span data-stu-id="950b1-108">Members</span></span>

<span data-ttu-id="950b1-109">A interface **IMsRdpClientTransportSettings** herda da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="950b1-109">The **IMsRdpClientTransportSettings** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="950b1-110">**IMsRdpClientTransportSettings** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="950b1-110">**IMsRdpClientTransportSettings** also has these types of members:</span></span>

-   [<span data-ttu-id="950b1-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="950b1-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="950b1-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="950b1-112">Properties</span></span>

<span data-ttu-id="950b1-113">A interface **IMsRdpClientTransportSettings** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="950b1-113">The **IMsRdpClientTransportSettings** interface has these properties.</span></span>



| <span data-ttu-id="950b1-114">Propriedade</span><span class="sxs-lookup"><span data-stu-id="950b1-114">Property</span></span>                                                                                                          | <span data-ttu-id="950b1-115">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="950b1-115">Access type</span></span>           | <span data-ttu-id="950b1-116">Description</span><span class="sxs-lookup"><span data-stu-id="950b1-116">Description</span></span>                                                 |
|:------------------------------------------------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------|
| [<span data-ttu-id="950b1-117">**GatewayCredsSource**</span><span class="sxs-lookup"><span data-stu-id="950b1-117">**GatewayCredsSource**</span></span>](imsrdpclienttransportsettings-gatewaycredssource.md)<br/>                         | <span data-ttu-id="950b1-118">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="950b1-118">Read/write</span></span><br/> | <span data-ttu-id="950b1-119">O método de autenticação do servidor de gateway de área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="950b1-119">The RD Gateway server authentication method.</span></span><br/>     |
| [<span data-ttu-id="950b1-120">**GatewayDefaultUsageMethod**</span><span class="sxs-lookup"><span data-stu-id="950b1-120">**GatewayDefaultUsageMethod**</span></span>](imsrdpclienttransportsettings-gatewaydefaultusagemethod.md)<br/>           | <span data-ttu-id="950b1-121">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="950b1-121">Read-only</span></span><br/>  | <span data-ttu-id="950b1-122">O método de uso do gateway RD padrão.</span><span class="sxs-lookup"><span data-stu-id="950b1-122">The default RD Gateway usage method.</span></span><br/>             |
| [<span data-ttu-id="950b1-123">**GatewayHostname**</span><span class="sxs-lookup"><span data-stu-id="950b1-123">**GatewayHostname**</span></span>](imsrdpclienttransportsettings-gatewayhostname.md)<br/>                               | <span data-ttu-id="950b1-124">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="950b1-124">Read/write</span></span><br/> | <span data-ttu-id="950b1-125">Nome do host do servidor de gateway de área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="950b1-125">Host name of the RD Gateway server.</span></span><br/>              |
| [<span data-ttu-id="950b1-126">**GatewayIsSupported**</span><span class="sxs-lookup"><span data-stu-id="950b1-126">**GatewayIsSupported**</span></span>](imsrdpclienttransportsettings-gatewayissupported.md)<br/>                         | <span data-ttu-id="950b1-127">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="950b1-127">Read-only</span></span><br/>  | <span data-ttu-id="950b1-128">Indica se há suporte para o Gateway RD.</span><span class="sxs-lookup"><span data-stu-id="950b1-128">Indicates whether RD Gateway is supported.</span></span><br/>       |
| [<span data-ttu-id="950b1-129">**GatewayProfileUsageMethod**</span><span class="sxs-lookup"><span data-stu-id="950b1-129">**GatewayProfileUsageMethod**</span></span>](imsrdpclienttransportsettings-gatewayprofileusagemethod.md)<br/>           | <span data-ttu-id="950b1-130">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="950b1-130">Read/write</span></span><br/> | <span data-ttu-id="950b1-131">O método de uso de perfil de gateway de área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="950b1-131">The RD Gateway profile usage method.</span></span><br/>             |
| [<span data-ttu-id="950b1-132">**GatewayUsageMethod**</span><span class="sxs-lookup"><span data-stu-id="950b1-132">**GatewayUsageMethod**</span></span>](imsrdpclienttransportsettings-gatewayusagemethod.md)<br/>                         | <span data-ttu-id="950b1-133">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="950b1-133">Read/write</span></span><br/> | <span data-ttu-id="950b1-134">O método de uso do servidor de gateway de área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="950b1-134">The RD Gateway server usage method.</span></span><br/>              |
| [<span data-ttu-id="950b1-135">**GatewayUserSelectedCredsSource**</span><span class="sxs-lookup"><span data-stu-id="950b1-135">**GatewayUserSelectedCredsSource**</span></span>](imsrdpclienttransportsettings-gatewayuserselectedcredssource.md)<br/> | <span data-ttu-id="950b1-136">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="950b1-136">Read/write</span></span><br/> | <span data-ttu-id="950b1-137">A origem da credencial do gateway de área de trabalho remota especificada pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="950b1-137">The user-specified RD Gateway credential source.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="950b1-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="950b1-138">Requirements</span></span>



| <span data-ttu-id="950b1-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="950b1-139">Requirement</span></span> | <span data-ttu-id="950b1-140">Valor</span><span class="sxs-lookup"><span data-stu-id="950b1-140">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="950b1-141">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="950b1-141">Minimum supported client</span></span><br/> | <span data-ttu-id="950b1-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="950b1-142">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="950b1-143">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="950b1-143">Minimum supported server</span></span><br/> | <span data-ttu-id="950b1-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="950b1-144">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="950b1-145">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="950b1-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="950b1-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="950b1-146"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="950b1-147">DLL</span><span class="sxs-lookup"><span data-stu-id="950b1-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="950b1-148"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="950b1-148"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="950b1-149">IID</span><span class="sxs-lookup"><span data-stu-id="950b1-149">IID</span></span><br/>                      | <span data-ttu-id="950b1-150">IID \_ IMsRdpClientTransportSettings é definido como 720298C0-A099-46f5-9F82-96921BAE4701</span><span class="sxs-lookup"><span data-stu-id="950b1-150">IID\_IMsRdpClientTransportSettings is defined as 720298C0-A099-46f5-9F82-96921BAE4701</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="950b1-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="950b1-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="950b1-152">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="950b1-152">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[<span data-ttu-id="950b1-153">Referência de Conexão Web de Área de Trabalho Remota</span><span class="sxs-lookup"><span data-stu-id="950b1-153">Remote Desktop Web Connection Reference</span></span>](remote-desktop-web-connection-reference.md)
</dt> <dt>

[<span data-ttu-id="950b1-154">**IMsRdpClientTransportSettings2**</span><span class="sxs-lookup"><span data-stu-id="950b1-154">**IMsRdpClientTransportSettings2**</span></span>](imsrdpclienttransportsettings2.md)
</dt> </dl>

 

