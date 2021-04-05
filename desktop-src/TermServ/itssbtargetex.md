---
title: Interface ITsSbTargetEx
description: Expõe propriedades que armazenam informações de configuração e estado sobre um destino.
ms.assetid: 3f0f26fb-e8bc-47eb-8038-e51792ad4376
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de interface ITsSbTargetEx
- Serviços de Área de Trabalho Remota da interface ITsSbTargetEx, descrita
topic_type:
- apiref
api_name:
- ITsSbTargetEx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d53d126d9419f87d91b027b0d69847f67de84be6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919110"
---
# <a name="itssbtargetex-interface"></a><span data-ttu-id="4051a-105">Interface ITsSbTargetEx</span><span class="sxs-lookup"><span data-stu-id="4051a-105">ITsSbTargetEx interface</span></span>

<span data-ttu-id="4051a-106">Expõe propriedades que armazenam informações de configuração e estado sobre um destino.</span><span class="sxs-lookup"><span data-stu-id="4051a-106">Exposes properties that store configuration and state information about a target.</span></span>

<span data-ttu-id="4051a-107">Essa interface só está disponível no Windows Server 2012 R2 com o [KB3091411](https://support.microsoft.com/kb/3091411) instalado.</span><span class="sxs-lookup"><span data-stu-id="4051a-107">This interface is only available on Windows Server 2012 R2 with [KB3091411](https://support.microsoft.com/kb/3091411) installed.</span></span> <span data-ttu-id="4051a-108">A propriedade [**TargetLoad**](itssbtarget-targetload.md) da interface [**ITsSbTarget**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget) está disponível a partir do Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="4051a-108">The [**TargetLoad**](itssbtarget-targetload.md) property of the [**ITsSbTarget**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget) interface is available starting with Windows Server 2016.</span></span>

## <a name="members"></a><span data-ttu-id="4051a-109">Membros</span><span class="sxs-lookup"><span data-stu-id="4051a-109">Members</span></span>

<span data-ttu-id="4051a-110">A interface **ITsSbTargetEx** herda de [**ITsSbTarget**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget).</span><span class="sxs-lookup"><span data-stu-id="4051a-110">The **ITsSbTargetEx** interface inherits from [**ITsSbTarget**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget).</span></span> <span data-ttu-id="4051a-111">**ITsSbTargetEx** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="4051a-111">**ITsSbTargetEx** also has these types of members:</span></span>

-   [<span data-ttu-id="4051a-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="4051a-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4051a-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="4051a-113">Properties</span></span>

<span data-ttu-id="4051a-114">A interface **ITsSbTargetEx** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="4051a-114">The **ITsSbTargetEx** interface has these properties.</span></span>



| <span data-ttu-id="4051a-115">Propriedade</span><span class="sxs-lookup"><span data-stu-id="4051a-115">Property</span></span>                                                                      | <span data-ttu-id="4051a-116">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="4051a-116">Access type</span></span>           | <span data-ttu-id="4051a-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="4051a-117">Description</span></span>                                                                               |
|:------------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4051a-118">**EnvironmentName**</span><span class="sxs-lookup"><span data-stu-id="4051a-118">**EnvironmentName**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtarget-get_environmentname)<br/>             | <span data-ttu-id="4051a-119">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="4051a-119">Read/write</span></span><br/> | <span data-ttu-id="4051a-120">Recupera ou especifica o nome do ambiente associado ao destino.</span><span class="sxs-lookup"><span data-stu-id="4051a-120">Retrieves or specifies the name of the environment associated with the target.</span></span><br/> |
| [<span data-ttu-id="4051a-121">**Farmname**</span><span class="sxs-lookup"><span data-stu-id="4051a-121">**FarmName**</span></span>](itssbtarget-farmname.md)<br/>                           | <span data-ttu-id="4051a-122">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="4051a-122">Read/write</span></span><br/> | <span data-ttu-id="4051a-123">Especifica ou recupera o nome do farm ao qual esse destino está associado.</span><span class="sxs-lookup"><span data-stu-id="4051a-123">Specifies or retrieves the name of the farm to which this target is joined.</span></span><br/>    |
| [<span data-ttu-id="4051a-124">**IpAddresses**</span><span class="sxs-lookup"><span data-stu-id="4051a-124">**IpAddresses**</span></span>](itssbtarget-ipaddresses.md)<br/>                     | <span data-ttu-id="4051a-125">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="4051a-125">Read/write</span></span><br/> | <span data-ttu-id="4051a-126">Recupera ou especifica os endereços IP externos do destino.</span><span class="sxs-lookup"><span data-stu-id="4051a-126">Retrieves or specifies the external IP addresses of the target.</span></span><br/>                |
| [<span data-ttu-id="4051a-127">**NumPendingConnections**</span><span class="sxs-lookup"><span data-stu-id="4051a-127">**NumPendingConnections**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtarget-get_numpendingconnections)<br/> | <span data-ttu-id="4051a-128">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4051a-128">Read-only</span></span><br/>  | <span data-ttu-id="4051a-129">Recupera o número de conexões de usuário pendentes para o destino.</span><span class="sxs-lookup"><span data-stu-id="4051a-129">Retrieves the number of pending user connections for the target.</span></span><br/>               |
| [<span data-ttu-id="4051a-130">**NumSessions**</span><span class="sxs-lookup"><span data-stu-id="4051a-130">**NumSessions**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtarget-get_numsessions)<br/>                     | <span data-ttu-id="4051a-131">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4051a-131">Read-only</span></span><br/>  | <span data-ttu-id="4051a-132">Recupera o número de sessões mantidas pelo Broker para o destino.</span><span class="sxs-lookup"><span data-stu-id="4051a-132">Retrieves the number of sessions maintained by broker for the target.</span></span><br/>          |
| [<span data-ttu-id="4051a-133">**TargetFQDN**</span><span class="sxs-lookup"><span data-stu-id="4051a-133">**TargetFQDN**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtarget-get_targetfqdn)<br/>                       | <span data-ttu-id="4051a-134">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="4051a-134">Read/write</span></span><br/> | <span data-ttu-id="4051a-135">Especifica ou recupera o nome de domínio totalmente qualificado do destino.</span><span class="sxs-lookup"><span data-stu-id="4051a-135">Specifies or retrieves the fully qualified domain name of the target.</span></span><br/>          |
| <span data-ttu-id="4051a-136">[**TargetLoad**](/previous-versions/windows/desktop/legacy/mt703468(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4051a-136">[**TargetLoad**](/previous-versions/windows/desktop/legacy/mt703468(v=vs.85))</span></span><br/>                     | <span data-ttu-id="4051a-137">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4051a-137">Read-only</span></span><br/>  | <span data-ttu-id="4051a-138">Recupera a carga relativa em um destino.</span><span class="sxs-lookup"><span data-stu-id="4051a-138">Retrieves the relative load on a target.</span></span><br/>                                       |
| [<span data-ttu-id="4051a-139">**TargetName**</span><span class="sxs-lookup"><span data-stu-id="4051a-139">**TargetName**</span></span>](itssbtarget-targetname.md)<br/>                       | <span data-ttu-id="4051a-140">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="4051a-140">Read/write</span></span><br/> | <span data-ttu-id="4051a-141">Especifica ou recupera o nome do destino.</span><span class="sxs-lookup"><span data-stu-id="4051a-141">Specifies or retrieves the name of the target.</span></span><br/>                                 |
| [<span data-ttu-id="4051a-142">**TargetNetbios**</span><span class="sxs-lookup"><span data-stu-id="4051a-142">**TargetNetbios**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtarget-get_targetnetbios)<br/>                 | <span data-ttu-id="4051a-143">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="4051a-143">Read/write</span></span><br/> | <span data-ttu-id="4051a-144">Especifica ou recupera o nome NetBIOS do destino.</span><span class="sxs-lookup"><span data-stu-id="4051a-144">Specifies or retrieves the NetBIOS name of the target.</span></span><br/>                         |
| [<span data-ttu-id="4051a-145">**TargetSet**</span><span class="sxs-lookup"><span data-stu-id="4051a-145">**TargetPropertySet**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtarget-get_targetpropertyset)<br/>         | <span data-ttu-id="4051a-146">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="4051a-146">Read/write</span></span><br/> | <span data-ttu-id="4051a-147">Especifica ou recupera o conjunto de propriedades para o destino.</span><span class="sxs-lookup"><span data-stu-id="4051a-147">Specifies or retrieves the property set for the target.</span></span><br/>                        |
| [<span data-ttu-id="4051a-148">**Destinostate**</span><span class="sxs-lookup"><span data-stu-id="4051a-148">**TargetState**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtarget-get_targetstate)<br/>                     | <span data-ttu-id="4051a-149">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="4051a-149">Read/write</span></span><br/> | <span data-ttu-id="4051a-150">Especifica ou recupera o estado de destino.</span><span class="sxs-lookup"><span data-stu-id="4051a-150">Specifies or retrieves the target state.</span></span><br/>                                       |



 

## <a name="requirements"></a><span data-ttu-id="4051a-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4051a-151">Requirements</span></span>



| <span data-ttu-id="4051a-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="4051a-152">Requirement</span></span> | <span data-ttu-id="4051a-153">Valor</span><span class="sxs-lookup"><span data-stu-id="4051a-153">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="4051a-154">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4051a-154">Minimum supported client</span></span><br/> | <span data-ttu-id="4051a-155">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="4051a-155">None supported</span></span><br/>                                                        |
| <span data-ttu-id="4051a-156">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4051a-156">Minimum supported server</span></span><br/> | <span data-ttu-id="4051a-157">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="4051a-157">Windows Server 2012 R2</span></span><br/>                                                |
| <span data-ttu-id="4051a-158">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="4051a-158">End of server support</span></span><br/>    | <span data-ttu-id="4051a-159">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="4051a-159">Windows Server 2012 R2</span></span><br/>                                                |
| <span data-ttu-id="4051a-160">IID</span><span class="sxs-lookup"><span data-stu-id="4051a-160">IID</span></span><br/>                      | <span data-ttu-id="4051a-161">IID \_ ITsSbTargetEx é definido como 74f99987-625d-11e5-bea1-a0481c7e9064</span><span class="sxs-lookup"><span data-stu-id="4051a-161">IID\_ITsSbTargetEx is defined as 74f99987-625d-11e5-bea1-a0481c7e9064</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4051a-162">Confira também</span><span class="sxs-lookup"><span data-stu-id="4051a-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4051a-163">**ITsSbTarget**</span><span class="sxs-lookup"><span data-stu-id="4051a-163">**ITsSbTarget**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget)
</dt> <dt>

[<span data-ttu-id="4051a-164">Interfaces de virtualização Área de Trabalho Remota</span><span class="sxs-lookup"><span data-stu-id="4051a-164">Remote Desktop Virtualization Interfaces</span></span>](remote-desktop-virtualization-interfaces.md)
</dt> </dl>

 

