---
description: Constantes do VDS
ms.assetid: a3a8b549-51bc-48eb-9215-04c7311e03a3
title: Constantes do VDS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9979cd4416b5305c61f6275612422b1f4cfe43a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105787027"
---
# <a name="vds-constants"></a><span data-ttu-id="b6831-103">Constantes do VDS</span><span class="sxs-lookup"><span data-stu-id="b6831-103">VDS Constants</span></span>

<span data-ttu-id="b6831-104">\[A partir do Windows 8 e do Windows Server 2012, a interface com do [serviço de disco virtual](virtual-disk-service-portal.md) é substituída pela [API de gerenciamento de armazenamento do Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="b6831-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="b6831-105">As constantes do VDS são categorizadas da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="b6831-105">VDS constants are categorized as follows:</span></span>

-   [<span data-ttu-id="b6831-106">Constantes de status do objeto</span><span class="sxs-lookup"><span data-stu-id="b6831-106">Object Status Constants</span></span>](#object-status-constants)
-   [<span data-ttu-id="b6831-107">Constantes de dicas do automagic</span><span class="sxs-lookup"><span data-stu-id="b6831-107">Automagic Hints Constants</span></span>](#automagic-hints-constants)
-   [<span data-ttu-id="b6831-108">Constantes diversas</span><span class="sxs-lookup"><span data-stu-id="b6831-108">Miscellaneous Constants</span></span>](#miscellaneous-constants)

### <a name="object-status-constants"></a><span data-ttu-id="b6831-109">Constantes de status do objeto</span><span class="sxs-lookup"><span data-stu-id="b6831-109">Object Status Constants</span></span>



| <span data-ttu-id="b6831-110">Constante</span><span class="sxs-lookup"><span data-stu-id="b6831-110">Constant</span></span>           | <span data-ttu-id="b6831-111">Valor</span><span class="sxs-lookup"><span data-stu-id="b6831-111">Value</span></span> |
|--------------------|-------|
| <span data-ttu-id="b6831-112">STATUS \_ desconhecido</span><span class="sxs-lookup"><span data-stu-id="b6831-112">STATUS\_UNKNOWN</span></span>    | <span data-ttu-id="b6831-113">0</span><span class="sxs-lookup"><span data-stu-id="b6831-113">0</span></span>     |
| <span data-ttu-id="b6831-114">STATUS \_ online</span><span class="sxs-lookup"><span data-stu-id="b6831-114">STATUS\_ONLINE</span></span>     | <span data-ttu-id="b6831-115">1</span><span class="sxs-lookup"><span data-stu-id="b6831-115">1</span></span>     |
| <span data-ttu-id="b6831-116">o STATUS \_ não \_ está pronto</span><span class="sxs-lookup"><span data-stu-id="b6831-116">STATUS\_NOT\_READY</span></span> | <span data-ttu-id="b6831-117">2</span><span class="sxs-lookup"><span data-stu-id="b6831-117">2</span></span>     |
| <span data-ttu-id="b6831-118">STATUS \_ sem \_ mídia</span><span class="sxs-lookup"><span data-stu-id="b6831-118">STATUS\_NO\_MEDIA</span></span>  | <span data-ttu-id="b6831-119">3</span><span class="sxs-lookup"><span data-stu-id="b6831-119">3</span></span>     |
| <span data-ttu-id="b6831-120">STATUS \_ offline</span><span class="sxs-lookup"><span data-stu-id="b6831-120">STATUS\_OFFLINE</span></span>    | <span data-ttu-id="b6831-121">4</span><span class="sxs-lookup"><span data-stu-id="b6831-121">4</span></span>     |
| <span data-ttu-id="b6831-122">\_falha no status</span><span class="sxs-lookup"><span data-stu-id="b6831-122">STATUS\_FAILED</span></span>     | <span data-ttu-id="b6831-123">5</span><span class="sxs-lookup"><span data-stu-id="b6831-123">5</span></span>     |
| <span data-ttu-id="b6831-124">STATUS \_ ausente</span><span class="sxs-lookup"><span data-stu-id="b6831-124">STATUS\_MISSING</span></span>    | <span data-ttu-id="b6831-125">6</span><span class="sxs-lookup"><span data-stu-id="b6831-125">6</span></span>     |



 

### <a name="automagic-hints-constants"></a><span data-ttu-id="b6831-126">Constantes de dicas do automagic</span><span class="sxs-lookup"><span data-stu-id="b6831-126">Automagic Hints Constants</span></span>



| <span data-ttu-id="b6831-127">Constante</span><span class="sxs-lookup"><span data-stu-id="b6831-127">Constant</span></span>                               | <span data-ttu-id="b6831-128">Valor</span><span class="sxs-lookup"><span data-stu-id="b6831-128">Value</span></span>   |
|----------------------------------------|---------|
| <span data-ttu-id="b6831-129">Dica de VDS \_ \_ MOSTLYREADS</span><span class="sxs-lookup"><span data-stu-id="b6831-129">VDS\_HINT\_MOSTLYREADS</span></span>                 | <span data-ttu-id="b6831-130">0x0002L</span><span class="sxs-lookup"><span data-stu-id="b6831-130">0x0002L</span></span> |
| <span data-ttu-id="b6831-131">Dica de VDS \_ \_ OPTIMIZEFORSEQUENTIALREADS</span><span class="sxs-lookup"><span data-stu-id="b6831-131">VDS\_HINT\_OPTIMIZEFORSEQUENTIALREADS</span></span>  | <span data-ttu-id="b6831-132">0x0004L</span><span class="sxs-lookup"><span data-stu-id="b6831-132">0x0004L</span></span> |
| <span data-ttu-id="b6831-133">Dica de VDS \_ \_ OPTIMIZEFORSEQUENTIALWRITES</span><span class="sxs-lookup"><span data-stu-id="b6831-133">VDS\_HINT\_OPTIMIZEFORSEQUENTIALWRITES</span></span> | <span data-ttu-id="b6831-134">0x0008L</span><span class="sxs-lookup"><span data-stu-id="b6831-134">0x0008L</span></span> |
| <span data-ttu-id="b6831-135">Dica de VDS \_ \_ REMAPENABLED</span><span class="sxs-lookup"><span data-stu-id="b6831-135">VDS\_HINT\_REMAPENABLED</span></span>                | <span data-ttu-id="b6831-136">0x0020L</span><span class="sxs-lookup"><span data-stu-id="b6831-136">0x0020L</span></span> |
| <span data-ttu-id="b6831-137">Dica de VDS \_ \_ WRITETHROUGHCACHINGENABLED</span><span class="sxs-lookup"><span data-stu-id="b6831-137">VDS\_HINT\_WRITETHROUGHCACHINGENABLED</span></span>  | <span data-ttu-id="b6831-138">0x0040L</span><span class="sxs-lookup"><span data-stu-id="b6831-138">0x0040L</span></span> |
| <span data-ttu-id="b6831-139">Dica de VDS \_ \_ HARDWARECHECKSUMENABLED</span><span class="sxs-lookup"><span data-stu-id="b6831-139">VDS\_HINT\_HARDWARECHECKSUMENABLED</span></span>     | <span data-ttu-id="b6831-140">0x0080L</span><span class="sxs-lookup"><span data-stu-id="b6831-140">0x0080L</span></span> |
| <span data-ttu-id="b6831-141">Dica de VDS \_ \_ ISYANKABLE</span><span class="sxs-lookup"><span data-stu-id="b6831-141">VDS\_HINT\_ISYANKABLE</span></span>                  | <span data-ttu-id="b6831-142">0x0100L</span><span class="sxs-lookup"><span data-stu-id="b6831-142">0x0100L</span></span> |



 

### <a name="miscellaneous-constants"></a><span data-ttu-id="b6831-143">Constantes diversas</span><span class="sxs-lookup"><span data-stu-id="b6831-143">Miscellaneous Constants</span></span>



| <span data-ttu-id="b6831-144">Constante</span><span class="sxs-lookup"><span data-stu-id="b6831-144">Constant</span></span>                     | <span data-ttu-id="b6831-145">Valor</span><span class="sxs-lookup"><span data-stu-id="b6831-145">Value</span></span>      |
|------------------------------|------------|
| <span data-ttu-id="b6831-146">\_ \_ prioridade mínima da recompilação do VDS \_</span><span class="sxs-lookup"><span data-stu-id="b6831-146">VDS\_REBUILD\_PRIORITY\_MIN</span></span>  | <span data-ttu-id="b6831-147">0x0001L</span><span class="sxs-lookup"><span data-stu-id="b6831-147">0x0001L</span></span>    |
| <span data-ttu-id="b6831-148">\_informações de \_ LUN do VDS da versão \_</span><span class="sxs-lookup"><span data-stu-id="b6831-148">VER\_VDS\_LUN\_INFORMATION</span></span>   | <span data-ttu-id="b6831-149">1</span><span class="sxs-lookup"><span data-stu-id="b6831-149">1</span></span>          |
| <span data-ttu-id="b6831-150">comprimento máximo de \_ ComputerName \_</span><span class="sxs-lookup"><span data-stu-id="b6831-150">MAX\_COMPUTERNAME\_LENGTH</span></span>    | <span data-ttu-id="b6831-151">15</span><span class="sxs-lookup"><span data-stu-id="b6831-151">15</span></span>         |
| <span data-ttu-id="b6831-152">comprimento máximo de \_ PROVIDERNAME \_</span><span class="sxs-lookup"><span data-stu-id="b6831-152">MAX\_PROVIDERNAME\_LENGTH</span></span>    | <span data-ttu-id="b6831-153">200</span><span class="sxs-lookup"><span data-stu-id="b6831-153">200</span></span>        |
| <span data-ttu-id="b6831-154">comprimento máximo de \_ VersionString \_</span><span class="sxs-lookup"><span data-stu-id="b6831-154">MAX\_VERSIONSTRING\_LENGTH</span></span>   | <span data-ttu-id="b6831-155">16</span><span class="sxs-lookup"><span data-stu-id="b6831-155">16</span></span>         |
| <span data-ttu-id="b6831-156">letra da unidade \_ \_ prop</span><span class="sxs-lookup"><span data-stu-id="b6831-156">DRIVE\_LETTER\_PROP</span></span>          | <span data-ttu-id="b6831-157">N/D</span><span class="sxs-lookup"><span data-stu-id="b6831-157">N/A</span></span>        |
| <span data-ttu-id="b6831-158">tamanho máximo do \_ \_ nome FS \_</span><span class="sxs-lookup"><span data-stu-id="b6831-158">MAX\_FS\_NAME\_SIZE</span></span>          | <span data-ttu-id="b6831-159">8</span><span class="sxs-lookup"><span data-stu-id="b6831-159">8</span></span>          |
| <span data-ttu-id="b6831-160">\_membro \_ IDX inválido</span><span class="sxs-lookup"><span data-stu-id="b6831-160">INVALID\_MEMBER\_IDX</span></span>         | <span data-ttu-id="b6831-161">0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="b6831-161">0xFFFFFFFF</span></span> |
| <span data-ttu-id="b6831-162">\_comprimento do \_ nome da partição GPT \_</span><span class="sxs-lookup"><span data-stu-id="b6831-162">GPT\_PARTITION\_NAME\_LENGTH</span></span> | <span data-ttu-id="b6831-163">36</span><span class="sxs-lookup"><span data-stu-id="b6831-163">36</span></span>         |
| <span data-ttu-id="b6831-164">\_caminho máximo</span><span class="sxs-lookup"><span data-stu-id="b6831-164">MAX\_PATH</span></span>                    | <span data-ttu-id="b6831-165">260</span><span class="sxs-lookup"><span data-stu-id="b6831-165">260</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="b6831-166">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b6831-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b6831-167">Referência do VDS</span><span class="sxs-lookup"><span data-stu-id="b6831-167">VDS Reference</span></span>](vds-reference.md)
</dt> </dl>

 

 
