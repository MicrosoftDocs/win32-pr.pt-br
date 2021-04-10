---
title: DS-execute-intenções-script estendido à direita
description: Controle o direito de acesso, que deve ser concedido ao contêiner partições, que permite que a operação de Rendom.exe ou preparação seja usada em uma renomeação de domínio.
ms.assetid: 39e9e76c-55c5-4514-ad4d-102844bcbc5a
ms.tgt_platform: multiple
keywords:
- DS-execute-intenções-script de esquema do AD estendido à direita
topic_type:
- apiref
api_name:
- DS-Execute-Intentions-Script
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b34765db2063688ccc8fced0a1e25cac23b98ded
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104087140"
---
# <a name="ds-execute-intentions-script-extended-right"></a><span data-ttu-id="7c484-104">DS-execute-intenções-script estendido à direita</span><span class="sxs-lookup"><span data-stu-id="7c484-104">DS-Execute-Intentions-Script extended right</span></span>

<span data-ttu-id="7c484-105">Controle o direito de acesso, que deve ser concedido ao contêiner partições, que permite que a operação de Rendom.exe ou preparação seja usada em uma renomeação de domínio.</span><span class="sxs-lookup"><span data-stu-id="7c484-105">Control access right, which should be granted to the partitions container, that allows the Rendom.exe or prepare operation to be used in a domain rename.</span></span> <span data-ttu-id="7c484-106">Esse direito de acesso de controle também aparece como um direito somente de auditoria quando a operação de Rendom.exe ou executar etapa é executada.</span><span class="sxs-lookup"><span data-stu-id="7c484-106">This control access right also appears as an audit-only right when the Rendom.exe or execute step operation is performed.</span></span>



| <span data-ttu-id="7c484-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="7c484-107">Entry</span></span> | <span data-ttu-id="7c484-108">Valor</span><span class="sxs-lookup"><span data-stu-id="7c484-108">Value</span></span> |
|--------------|--------------------------------------|
| <span data-ttu-id="7c484-109">CN</span><span class="sxs-lookup"><span data-stu-id="7c484-109">CN</span></span>           | <span data-ttu-id="7c484-110">DS-execute-intenções-script</span><span class="sxs-lookup"><span data-stu-id="7c484-110">DS-Execute-Intentions-Script</span></span>         |
| <span data-ttu-id="7c484-111">Display-Name</span><span class="sxs-lookup"><span data-stu-id="7c484-111">Display-Name</span></span> | <span data-ttu-id="7c484-112">Executar script de atualização de floresta</span><span class="sxs-lookup"><span data-stu-id="7c484-112">Execute Forest Update Script</span></span>         |
| <span data-ttu-id="7c484-113">GUID de direitos</span><span class="sxs-lookup"><span data-stu-id="7c484-113">Rights-GUID</span></span>  | <span data-ttu-id="7c484-114">2f16c4a5-b98e-432c-952a-cb388ba33f2e</span><span class="sxs-lookup"><span data-stu-id="7c484-114">2f16c4a5-b98e-432c-952a-cb388ba33f2e</span></span> |



## <a name="implementations"></a><span data-ttu-id="7c484-115">Implementações</span><span class="sxs-lookup"><span data-stu-id="7c484-115">Implementations</span></span>

-   [<span data-ttu-id="7c484-116">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="7c484-116">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="7c484-117">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="7c484-117">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="7c484-118">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="7c484-118">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="7c484-119">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="7c484-119">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="7c484-120">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="7c484-120">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="7c484-121">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="7c484-121">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="7c484-122">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7c484-122">Windows Server 2003</span></span>



| <span data-ttu-id="7c484-123">Entrada</span><span class="sxs-lookup"><span data-stu-id="7c484-123">Entry</span></span> | <span data-ttu-id="7c484-124">Valor</span><span class="sxs-lookup"><span data-stu-id="7c484-124">Value</span></span> |
|-------------------------|---------------------------------------------------------------|
| <span data-ttu-id="7c484-125">Applies-To</span><span class="sxs-lookup"><span data-stu-id="7c484-125">Applies-To</span></span>              | [<span data-ttu-id="7c484-126">**Entre referências-contêiner**</span><span class="sxs-lookup"><span data-stu-id="7c484-126">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |
| <span data-ttu-id="7c484-127">Localização-exibição-ID</span><span class="sxs-lookup"><span data-stu-id="7c484-127">Localization-Display-ID</span></span> | <span data-ttu-id="7c484-128">66</span><span class="sxs-lookup"><span data-stu-id="7c484-128">66</span></span>                                                            |



## <a name="adam"></a><span data-ttu-id="7c484-129">ADAM</span><span class="sxs-lookup"><span data-stu-id="7c484-129">ADAM</span></span>



| <span data-ttu-id="7c484-130">Entrada</span><span class="sxs-lookup"><span data-stu-id="7c484-130">Entry</span></span> | <span data-ttu-id="7c484-131">Valor</span><span class="sxs-lookup"><span data-stu-id="7c484-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------|
| <span data-ttu-id="7c484-132">Applies-To</span><span class="sxs-lookup"><span data-stu-id="7c484-132">Applies-To</span></span>              | [<span data-ttu-id="7c484-133">**Entre referências-contêiner**</span><span class="sxs-lookup"><span data-stu-id="7c484-133">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |
| <span data-ttu-id="7c484-134">Localização-exibição-ID</span><span class="sxs-lookup"><span data-stu-id="7c484-134">Localization-Display-ID</span></span> | <span data-ttu-id="7c484-135">66</span><span class="sxs-lookup"><span data-stu-id="7c484-135">66</span></span>                                                            |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="7c484-136">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="7c484-136">Windows Server 2003 R2</span></span>



| <span data-ttu-id="7c484-137">Entrada</span><span class="sxs-lookup"><span data-stu-id="7c484-137">Entry</span></span> | <span data-ttu-id="7c484-138">Valor</span><span class="sxs-lookup"><span data-stu-id="7c484-138">Value</span></span> |
|-------------------------|---------------------------------------------------------------|
| <span data-ttu-id="7c484-139">Applies-To</span><span class="sxs-lookup"><span data-stu-id="7c484-139">Applies-To</span></span>              | [<span data-ttu-id="7c484-140">**Entre referências-contêiner**</span><span class="sxs-lookup"><span data-stu-id="7c484-140">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |
| <span data-ttu-id="7c484-141">Localização-exibição-ID</span><span class="sxs-lookup"><span data-stu-id="7c484-141">Localization-Display-ID</span></span> | <span data-ttu-id="7c484-142">66</span><span class="sxs-lookup"><span data-stu-id="7c484-142">66</span></span>                                                            |



## <a name="windows-server-2008"></a><span data-ttu-id="7c484-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7c484-143">Windows Server 2008</span></span>



| <span data-ttu-id="7c484-144">Entrada</span><span class="sxs-lookup"><span data-stu-id="7c484-144">Entry</span></span> | <span data-ttu-id="7c484-145">Valor</span><span class="sxs-lookup"><span data-stu-id="7c484-145">Value</span></span> |
|-------------------------|---------------------------------------------------------------|
| <span data-ttu-id="7c484-146">Applies-To</span><span class="sxs-lookup"><span data-stu-id="7c484-146">Applies-To</span></span>              | [<span data-ttu-id="7c484-147">**Entre referências-contêiner**</span><span class="sxs-lookup"><span data-stu-id="7c484-147">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |
| <span data-ttu-id="7c484-148">Localização-exibição-ID</span><span class="sxs-lookup"><span data-stu-id="7c484-148">Localization-Display-ID</span></span> | <span data-ttu-id="7c484-149">66</span><span class="sxs-lookup"><span data-stu-id="7c484-149">66</span></span>                                                            |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="7c484-150">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7c484-150">Windows Server 2008 R2</span></span>



| <span data-ttu-id="7c484-151">Entrada</span><span class="sxs-lookup"><span data-stu-id="7c484-151">Entry</span></span> | <span data-ttu-id="7c484-152">Valor</span><span class="sxs-lookup"><span data-stu-id="7c484-152">Value</span></span> |
|-------------------------|---------------------------------------------------------------|
| <span data-ttu-id="7c484-153">Applies-To</span><span class="sxs-lookup"><span data-stu-id="7c484-153">Applies-To</span></span>              | [<span data-ttu-id="7c484-154">**Entre referências-contêiner**</span><span class="sxs-lookup"><span data-stu-id="7c484-154">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |
| <span data-ttu-id="7c484-155">Localização-exibição-ID</span><span class="sxs-lookup"><span data-stu-id="7c484-155">Localization-Display-ID</span></span> | <span data-ttu-id="7c484-156">66</span><span class="sxs-lookup"><span data-stu-id="7c484-156">66</span></span>                                                            |



## <a name="windows-server-2012"></a><span data-ttu-id="7c484-157">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7c484-157">Windows Server 2012</span></span>



| <span data-ttu-id="7c484-158">Entrada</span><span class="sxs-lookup"><span data-stu-id="7c484-158">Entry</span></span> | <span data-ttu-id="7c484-159">Valor</span><span class="sxs-lookup"><span data-stu-id="7c484-159">Value</span></span> |
|-------------------------|---------------------------------------------------------------|
| <span data-ttu-id="7c484-160">Applies-To</span><span class="sxs-lookup"><span data-stu-id="7c484-160">Applies-To</span></span>              | [<span data-ttu-id="7c484-161">**Entre referências-contêiner**</span><span class="sxs-lookup"><span data-stu-id="7c484-161">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |
| <span data-ttu-id="7c484-162">Localização-exibição-ID</span><span class="sxs-lookup"><span data-stu-id="7c484-162">Localization-Display-ID</span></span> | <span data-ttu-id="7c484-163">66</span><span class="sxs-lookup"><span data-stu-id="7c484-163">66</span></span>                                                            |



 

 





