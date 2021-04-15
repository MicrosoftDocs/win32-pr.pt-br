---
description: A seguir estão as estruturas de DFS Sistema de Arquivos Distribuído
ms.assetid: f55ad3c0-0457-4d5a-a7d3-8eff744d573d
title: Estruturas de Sistema de Arquivos Distribuído
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42fc3351402c4721952cbfc4dc3fe3c6ac6d3a76
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457137"
---
# <a name="distributed-file-system-structures"></a><span data-ttu-id="0b5f2-103">Estruturas de Sistema de Arquivos Distribuído</span><span class="sxs-lookup"><span data-stu-id="0b5f2-103">Distributed File System Structures</span></span>

<span data-ttu-id="0b5f2-104">A seguir estão as estruturas de Sistema de Arquivos Distribuído (DFS):</span><span class="sxs-lookup"><span data-stu-id="0b5f2-104">The following are the Distributed File System (DFS) structures:</span></span>

## <a name="in-this-section"></a><span data-ttu-id="0b5f2-105">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="0b5f2-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="0b5f2-106">**DFS_GET_PKT_ENTRY_STATE_ARG**</span><span class="sxs-lookup"><span data-stu-id="0b5f2-106">**DFS_GET_PKT_ENTRY_STATE_ARG**</span></span>](/windows/win32/api/lmdfs/ns-lmdfs-dfs_get_pkt_entry_state_arg)
</dt> <dd>

<span data-ttu-id="0b5f2-107">Buffer de entrada usado com o código de controle de [**FSCTL_DFS_GET_PKT_ENTRY_STATE**](fsctl-dfs-get-pkt-entry-state.md)</span><span class="sxs-lookup"><span data-stu-id="0b5f2-107">Input buffer used with the [**FSCTL_DFS_GET_PKT_ENTRY_STATE**](fsctl-dfs-get-pkt-entry-state.md) control code</span></span>
</dd> <dt>

[<span data-ttu-id="0b5f2-108">Estrutura de _DFS_INFO_1</span><span class="sxs-lookup"><span data-stu-id="0b5f2-108">_DFS_INFO_1 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_1)
</dt> <dd>
<span data-ttu-id="0b5f2-109">Contém o nome de uma raiz ou um link de Sistema de Arquivos Distribuído (DFS).</span><span class="sxs-lookup"><span data-stu-id="0b5f2-109">Contains the name of a Distributed File System (DFS) root or link.</span></span>

</dd> <dt>

[<span data-ttu-id="0b5f2-110">Estrutura de _DFS_INFO_2</span><span class="sxs-lookup"><span data-stu-id="0b5f2-110">_DFS_INFO_2 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_2)
</dt> <dd>
<span data-ttu-id="0b5f2-111">Contém informações sobre um link ou uma raiz do Sistema de Arquivos Distribuído (DFS).</span><span class="sxs-lookup"><span data-stu-id="0b5f2-111">Contains information about a Distributed File System (DFS) root or link.</span></span> <span data-ttu-id="0b5f2-112">Essa estrutura contém o nome, o status e o número de destinos DFS para a raiz ou o link.</span><span class="sxs-lookup"><span data-stu-id="0b5f2-112">This structure contains the name, status, and number of DFS targets for the root or link.</span></span>

</dd> <dt>

[<span data-ttu-id="0b5f2-113">Estrutura de _DFS_INFO_3</span><span class="sxs-lookup"><span data-stu-id="0b5f2-113">_DFS_INFO_3 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_3)
</dt> <dd>
<span data-ttu-id="0b5f2-114">Contém informações sobre um link ou uma raiz do Sistema de Arquivos Distribuído (DFS).</span><span class="sxs-lookup"><span data-stu-id="0b5f2-114">Contains information about a Distributed File System (DFS) root or link.</span></span> <span data-ttu-id="0b5f2-115">Essa estrutura contém o nome, o status, o número de destinos do DFS e informações sobre cada destino da raiz ou do link.</span><span class="sxs-lookup"><span data-stu-id="0b5f2-115">This structure contains the name, status, number of DFS targets, and information about each target of the root or link.</span></span>

</dd> <dt>

[<span data-ttu-id="0b5f2-116">Estrutura de _DFS_INFO_4</span><span class="sxs-lookup"><span data-stu-id="0b5f2-116">_DFS_INFO_4 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_4)
</dt> <dd>
<span data-ttu-id="0b5f2-117">Contém informações sobre um link ou uma raiz do Sistema de Arquivos Distribuído (DFS).</span><span class="sxs-lookup"><span data-stu-id="0b5f2-117">Contains information about a Distributed File System (DFS) root or link.</span></span> <span data-ttu-id="0b5f2-118">Essa estrutura contém o nome, o status, o **GUID**, o tempo limite, o número de destinos e as informações sobre cada destino da raiz ou do link.</span><span class="sxs-lookup"><span data-stu-id="0b5f2-118">This structure contains the name, status, **GUID**, time-out, number of targets, and information about each target of the root or link.</span></span>

</dd> <dt>

[<span data-ttu-id="0b5f2-119">Estrutura de _DFS_INFO_5</span><span class="sxs-lookup"><span data-stu-id="0b5f2-119">_DFS_INFO_5 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_5)
</dt> <dd>
<span data-ttu-id="0b5f2-120">Contém informações sobre um link ou uma raiz do Sistema de Arquivos Distribuído (DFS).</span><span class="sxs-lookup"><span data-stu-id="0b5f2-120">Contains information about a Distributed File System (DFS) root or link.</span></span> <span data-ttu-id="0b5f2-121">Essa estrutura contém o nome, o status, o **GUID**, o tempo limite, as propriedades de namespace/raiz/link, o tamanho dos metadados e o número de destinos para a raiz ou o link.</span><span class="sxs-lookup"><span data-stu-id="0b5f2-121">This structure contains the name, status, **GUID**, time-out, namespace/root/link properties, metadata size, and number of targets for the root or link.</span></span>

</dd> <dt>

[<span data-ttu-id="0b5f2-122">Estrutura de _DFS_INFO_6</span><span class="sxs-lookup"><span data-stu-id="0b5f2-122">_DFS_INFO_6 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_6)
</dt> <dd>
<span data-ttu-id="0b5f2-123">Contém informações sobre um link ou uma raiz do Sistema de Arquivos Distribuído (DFS).</span><span class="sxs-lookup"><span data-stu-id="0b5f2-123">Contains information about a Distributed File System (DFS) root or link.</span></span> <span data-ttu-id="0b5f2-124">Essa estrutura contém o nome, o status, o **GUID**, o tempo limite, as propriedades de namespace/raiz/link, o tamanho dos metadados, o número de destinos e as informações sobre cada destino da raiz ou do link.</span><span class="sxs-lookup"><span data-stu-id="0b5f2-124">This structure contains the name, status, **GUID**, time-out, namespace/root/link properties, metadata size, number of targets, and information about each target of the root or link.</span></span>

</dd> <dt>

[<span data-ttu-id="0b5f2-125">Estrutura de _DFS_INFO_7</span><span class="sxs-lookup"><span data-stu-id="0b5f2-125">_DFS_INFO_7 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_7)
</dt> <dd>
<span data-ttu-id="0b5f2-126">Contém informações sobre um namespace do DFS.</span><span class="sxs-lookup"><span data-stu-id="0b5f2-126">Contains information about a DFS namespace.</span></span> <span data-ttu-id="0b5f2-127">Essa estrutura contém o **GUID** de versão para os metadados do namespace.</span><span class="sxs-lookup"><span data-stu-id="0b5f2-127">This structure contains the version **GUID** for the metadata for the namespace.</span></span>

</dd> <dt>

[<span data-ttu-id="0b5f2-128">Estrutura de _DFS_INFO_8</span><span class="sxs-lookup"><span data-stu-id="0b5f2-128">_DFS_INFO_8 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_8)
</dt> <dd>
<span data-ttu-id="0b5f2-129">Contém o nome, o status, o **GUID**, o tempo limite, os sinalizadores de propriedade, o tamanho dos metadados, as informações de destino do DFS e o descritor de segurança do ponto de nova análise de link para uma raiz ou link.</span><span class="sxs-lookup"><span data-stu-id="0b5f2-129">Contains the name, status, **GUID**, time-out, property flags, metadata size, DFS target information, and link reparse point security descriptor for a root or link.</span></span>

</dd> <dt>

[<span data-ttu-id="0b5f2-130">Estrutura de _DFS_INFO_9</span><span class="sxs-lookup"><span data-stu-id="0b5f2-130">_DFS_INFO_9 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_9)
</dt> <dd>
<span data-ttu-id="0b5f2-131">Contém o nome, o status, o **GUID**, o tempo limite, os sinalizadores de propriedade, o tamanho dos metadados, as informações de destino do DFS, o descritor de segurança do ponto de nova análise de link e uma lista de destinos do DFS para uma raiz ou link.</span><span class="sxs-lookup"><span data-stu-id="0b5f2-131">Contains the name, status, **GUID**, time-out, property flags, metadata size, DFS target information, link reparse point security descriptor, and a list of DFS targets for a root or link.</span></span>

</dd> <dt>

[<span data-ttu-id="0b5f2-132">Estrutura de _DFS_INFO_50</span><span class="sxs-lookup"><span data-stu-id="0b5f2-132">_DFS_INFO_50 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_50)
</dt> <dd>
<span data-ttu-id="0b5f2-133">Contém a versão de metadados do DFS e os recursos de um namespace do DFS existente.</span><span class="sxs-lookup"><span data-stu-id="0b5f2-133">Contains the DFS metadata version and capabilities of an existing DFS namespace.</span></span>

</dd> <dt>

[<span data-ttu-id="0b5f2-134">Estrutura de _DFS_INFO_100</span><span class="sxs-lookup"><span data-stu-id="0b5f2-134">_DFS_INFO_100 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_100)
</dt> <dd>
<span data-ttu-id="0b5f2-135">Contém um comentário associado a uma raiz ou link de Sistema de Arquivos Distribuído (DFS).</span><span class="sxs-lookup"><span data-stu-id="0b5f2-135">Contains a comment associated with a Distributed File System (DFS) root or link.</span></span>

</dd> <dt>

[<span data-ttu-id="0b5f2-136">Estrutura de _DFS_INFO_101</span><span class="sxs-lookup"><span data-stu-id="0b5f2-136">_DFS_INFO_101 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_101)
</dt> <dd>
<span data-ttu-id="0b5f2-137">Descreve o estado de armazenamento em uma raiz DFS, link, destino raiz ou destino de link.</span><span class="sxs-lookup"><span data-stu-id="0b5f2-137">Describes the state of storage on a DFS root, link, root target, or link target.</span></span>

</dd> <dt>

[<span data-ttu-id="0b5f2-138">Estrutura de _DFS_INFO_102</span><span class="sxs-lookup"><span data-stu-id="0b5f2-138">_DFS_INFO_102 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_102)
</dt> <dd>
<span data-ttu-id="0b5f2-139">Contém um valor de tempo limite para associar a uma raiz de Sistema de Arquivos Distribuído (DFS) ou a um link em uma raiz DFS nomeada.</span><span class="sxs-lookup"><span data-stu-id="0b5f2-139">Contains a time-out value to associate with a Distributed File System (DFS) root or a link in a named DFS root.</span></span>

</dd> <dt>

[<span data-ttu-id="0b5f2-140">Estrutura de _DFS_INFO_103</span><span class="sxs-lookup"><span data-stu-id="0b5f2-140">_DFS_INFO_103 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_103)
</dt> <dd>
<span data-ttu-id="0b5f2-141">Contém propriedades que definem comportamentos específicos para uma raiz ou link do DFS.</span><span class="sxs-lookup"><span data-stu-id="0b5f2-141">Contains properties that set specific behaviors for a DFS root or link.</span></span>

</dd> <dt>

[<span data-ttu-id="0b5f2-142">Estrutura de _DFS_INFO_104</span><span class="sxs-lookup"><span data-stu-id="0b5f2-142">_DFS_INFO_104 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_104)
</dt> <dd>
<span data-ttu-id="0b5f2-143">Contém a prioridade de um destino de raiz de DFS ou destino de link.</span><span class="sxs-lookup"><span data-stu-id="0b5f2-143">Contains the priority of a DFS root target or link target.</span></span>

</dd> <dt>

[<span data-ttu-id="0b5f2-144">Estrutura de _DFS_INFO_105</span><span class="sxs-lookup"><span data-stu-id="0b5f2-144">_DFS_INFO_105 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_105)
</dt> <dd>
<span data-ttu-id="0b5f2-145">Contém informações sobre uma raiz ou link do DFS, incluindo comentários, estado, tempo limite e comportamentos de DFS especificados por sinalizadores de propriedade.</span><span class="sxs-lookup"><span data-stu-id="0b5f2-145">Contains information about a DFS root or link, including comment, state, time-out, and DFS behaviors specified by property flags.</span></span>

</dd> <dt>

[<span data-ttu-id="0b5f2-146">Estrutura de _DFS_INFO_106</span><span class="sxs-lookup"><span data-stu-id="0b5f2-146">_DFS_INFO_106 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_106)
</dt> <dd>
<span data-ttu-id="0b5f2-147">Contém o estado de armazenamento e a prioridade para um destino de raiz de DFS ou destino de link.</span><span class="sxs-lookup"><span data-stu-id="0b5f2-147">Contains the storage state and priority for a DFS root target or link target.</span></span> <span data-ttu-id="0b5f2-148">Essa estrutura é apenas para uso com a função [**NetDfsSetInfo**](netdfssetinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="0b5f2-148">This structure is only for use with the [**NetDfsSetInfo**](netdfssetinfo.md) function.</span></span>

</dd> <dt>

[<span data-ttu-id="0b5f2-149">Estrutura de _DFS_INFO_107</span><span class="sxs-lookup"><span data-stu-id="0b5f2-149">_DFS_INFO_107 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_107)
</dt> <dd>
<span data-ttu-id="0b5f2-150">Contém informações sobre uma raiz ou link do DFS, incluindo o comentário, o estado, o tempo limite, os sinalizadores de propriedade e o descritor de segurança do ponto de nova análise de link.</span><span class="sxs-lookup"><span data-stu-id="0b5f2-150">Contains information about a DFS root or link, including the comment, state, time-out, property flags, and link reparse point security descriptor.</span></span>

</dd> <dt>

[<span data-ttu-id="0b5f2-151">Estrutura de _DFS_INFO_150</span><span class="sxs-lookup"><span data-stu-id="0b5f2-151">_DFS_INFO_150 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_150)
</dt> <dd>
<span data-ttu-id="0b5f2-152">Contém o descritor de segurança para um ponto de nova análise do link do DFS.</span><span class="sxs-lookup"><span data-stu-id="0b5f2-152">Contains the security descriptor for a DFS link's reparse point.</span></span>

</dd> <dt>

[<span data-ttu-id="0b5f2-153">Estrutura de _DFS_INFO_200</span><span class="sxs-lookup"><span data-stu-id="0b5f2-153">_DFS_INFO_200 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_200)
</dt> <dd>
<span data-ttu-id="0b5f2-154">Contém o nome de um namespace de Sistema de Arquivos Distribuído baseado em domínio (DFS).</span><span class="sxs-lookup"><span data-stu-id="0b5f2-154">Contains the name of a domain-based Distributed File System (DFS) namespace.</span></span>

</dd> <dt>

[<span data-ttu-id="0b5f2-155">Estrutura de _DFS_INFO_300</span><span class="sxs-lookup"><span data-stu-id="0b5f2-155">_DFS_INFO_300 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_300)
</dt> <dd>
<span data-ttu-id="0b5f2-156">Contém o nome e o tipo (baseado em domínio ou autônomo) de um namespace do DFS.</span><span class="sxs-lookup"><span data-stu-id="0b5f2-156">Contains the name and type (domain-based or stand-alone) of a DFS namespace.</span></span>

</dd> <dt>

[<span data-ttu-id="0b5f2-157">Estrutura de _DFS_STORAGE_INFO</span><span class="sxs-lookup"><span data-stu-id="0b5f2-157">_DFS_STORAGE_INFO structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_storage_info)
</dt> <dd>
<span data-ttu-id="0b5f2-158">Contém informações sobre uma raiz DFS ou destino de link em um namespace DFS ou do cache mantido pelo cliente DFS.</span><span class="sxs-lookup"><span data-stu-id="0b5f2-158">Contains information about a DFS root or link target in a DFS namespace or from the cache maintained by the DFS client.</span></span>

</dd> <dt>

[<span data-ttu-id="0b5f2-159">Estrutura de _DFS_STORAGE_INFO_1</span><span class="sxs-lookup"><span data-stu-id="0b5f2-159">_DFS_STORAGE_INFO_1 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_storage_info_1)
</dt> <dd>
<span data-ttu-id="0b5f2-160">Contém informações sobre um destino DFS, incluindo o nome do servidor de destino DFS e o nome do compartilhamento, bem como o estado e a prioridade do destino.</span><span class="sxs-lookup"><span data-stu-id="0b5f2-160">Contains information about a DFS target, including the DFS target server name and share name as well as the target's state and priority.</span></span>

</dd> <dt>

[<span data-ttu-id="0b5f2-161">Estrutura de _DFS_SUPPORTED_NAMESPACE_VERSION_INFO</span><span class="sxs-lookup"><span data-stu-id="0b5f2-161">_DFS_SUPPORTED_NAMESPACE_VERSION_INFO structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_supported_namespace_version_info)
</dt> <dd>
<span data-ttu-id="0b5f2-162">Contém informações de versão para um namespace do DFS.</span><span class="sxs-lookup"><span data-stu-id="0b5f2-162">Contains version information for a DFS namespace.</span></span>

</dd> <dt>

[<span data-ttu-id="0b5f2-163">Estrutura de _DFS_TARGET_PRIORITY</span><span class="sxs-lookup"><span data-stu-id="0b5f2-163">_DFS_TARGET_PRIORITY structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_target_priority)
</dt> <dd>
<span data-ttu-id="0b5f2-164">Contém a classe de prioridade e a classificação de um destino DFS específico.</span><span class="sxs-lookup"><span data-stu-id="0b5f2-164">Contains the priority class and rank of a specific DFS target.</span></span>

</dd> </dl>
