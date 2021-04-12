---
title: Funções de Sistema de Arquivos Distribuído
description: A seguir estão as funções de Sistema de Arquivos Distribuído (DFS).
ms.assetid: 8f86b717-fe26-4550-8b71-8f7df5ca6022
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 463c085115f6d3e88f9a3be80a890caa0aacb340
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457136"
---
# <a name="distributed-file-system-functions"></a><span data-ttu-id="f3ac1-103">Funções de Sistema de Arquivos Distribuído</span><span class="sxs-lookup"><span data-stu-id="f3ac1-103">Distributed File System Functions</span></span>

<span data-ttu-id="f3ac1-104">A seguir estão as funções de Sistema de Arquivos Distribuído (DFS).</span><span class="sxs-lookup"><span data-stu-id="f3ac1-104">The following are the Distributed File System (DFS) functions.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="f3ac1-105">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="f3ac1-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="f3ac1-106">NetDfsAdd</span><span class="sxs-lookup"><span data-stu-id="f3ac1-106">NetDfsAdd</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsadd)
</dt> <dd>
<span data-ttu-id="f3ac1-107">Cria um novo link de Sistema de Arquivos Distribuído (DFS) ou adiciona destinos a um link existente em um namespace do DFS.</span><span class="sxs-lookup"><span data-stu-id="f3ac1-107">Creates a new Distributed File System (DFS) link or adds targets to an existing link in a DFS namespace.</span></span>

</dd> <dt>

[<span data-ttu-id="f3ac1-108">NetDfsAddFtRoot</span><span class="sxs-lookup"><span data-stu-id="f3ac1-108">NetDfsAddFtRoot</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsaddftroot)
</dt> <dd>
<span data-ttu-id="f3ac1-109">Cria um novo namespace do Sistema de Arquivos Distribuído (DFS) baseado em domínio.</span><span class="sxs-lookup"><span data-stu-id="f3ac1-109">Creates a new domain-based Distributed File System (DFS) namespace.</span></span> <span data-ttu-id="f3ac1-110">Se o namespace já existir, a função adicionará o destino de raiz especificado a ele.</span><span class="sxs-lookup"><span data-stu-id="f3ac1-110">If the namespace already exists, the function adds the specified root target to it.</span></span>

</dd> <dt>

[<span data-ttu-id="f3ac1-111">NetDfsAddRootTarget</span><span class="sxs-lookup"><span data-stu-id="f3ac1-111">NetDfsAddRootTarget</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsaddroottarget)
</dt> <dd>
<span data-ttu-id="f3ac1-112">Cria um namespace DFS baseado em domínio ou autônomo ou adiciona um novo destino de raiz a um namespace baseado em domínio existente.</span><span class="sxs-lookup"><span data-stu-id="f3ac1-112">Creates a domain-based or stand-alone DFS namespace or adds a new root target to an existing domain-based namespace.</span></span>

</dd> <dt>

[<span data-ttu-id="f3ac1-113">NetDfsAddStdRoot</span><span class="sxs-lookup"><span data-stu-id="f3ac1-113">NetDfsAddStdRoot</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsaddstdroot)
</dt> <dd>
<span data-ttu-id="f3ac1-114">Cria um novo namespace de Sistema de Arquivos Distribuído autônomo (DFS).</span><span class="sxs-lookup"><span data-stu-id="f3ac1-114">Creates a new stand-alone Distributed File System (DFS) namespace.</span></span>

</dd> <dt>

[<span data-ttu-id="f3ac1-115">NetDfsEnum</span><span class="sxs-lookup"><span data-stu-id="f3ac1-115">NetDfsEnum</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsenum)
</dt> <dd>
<span data-ttu-id="f3ac1-116">Enumera os namespaces de Sistema de Arquivos Distribuído (DFS) hospedados em um servidor ou links DFS de um namespace hospedado por um servidor.</span><span class="sxs-lookup"><span data-stu-id="f3ac1-116">Enumerates the Distributed File System (DFS) namespaces hosted on a server or DFS links of a namespace hosted by a server.</span></span>

</dd> <dt>

[<span data-ttu-id="f3ac1-117">NetDfsGetClientInfo</span><span class="sxs-lookup"><span data-stu-id="f3ac1-117">NetDfsGetClientInfo</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetclientinfo)
</dt> <dd>
<span data-ttu-id="f3ac1-118">Recupera informações sobre uma raiz do Sistema de Arquivos Distribuído (DFS) ou o link do cache mantido pelo cliente do DFS.</span><span class="sxs-lookup"><span data-stu-id="f3ac1-118">Retrieves information about a Distributed File System (DFS) root or link from the cache maintained by the DFS client.</span></span>

</dd> <dt>

[<span data-ttu-id="f3ac1-119">NetDfsGetFtContainerSecurity</span><span class="sxs-lookup"><span data-stu-id="f3ac1-119">NetDfsGetFtContainerSecurity</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetftcontainersecurity)
</dt> <dd>
<span data-ttu-id="f3ac1-120">Recupera o descritor de segurança do objeto de contêiner para os namespaces do DFS baseados em domínio no domínio de Active Directory especificado.</span><span class="sxs-lookup"><span data-stu-id="f3ac1-120">Retrieves the security descriptor of the container object for the domain-based DFS namespaces in the specified Active Directory domain.</span></span>

</dd> <dt>

[<span data-ttu-id="f3ac1-121">NetDfsGetInfo</span><span class="sxs-lookup"><span data-stu-id="f3ac1-121">NetDfsGetInfo</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetinfo)
</dt> <dd>
<span data-ttu-id="f3ac1-122">Recupera informações sobre uma raiz do Sistema de Arquivos Distribuído (DFS) especificada ou um link em um namespace do DFS.</span><span class="sxs-lookup"><span data-stu-id="f3ac1-122">Retrieves information about a specified Distributed File System (DFS) root or link in a DFS namespace.</span></span>

</dd> <dt>

[<span data-ttu-id="f3ac1-123">NetDfsGetSecurity</span><span class="sxs-lookup"><span data-stu-id="f3ac1-123">NetDfsGetSecurity</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetsecurity)
</dt> <dd>
<span data-ttu-id="f3ac1-124">Recupera o descritor de segurança para o objeto raiz do namespace do DFS especificado.</span><span class="sxs-lookup"><span data-stu-id="f3ac1-124">Retrieves the security descriptor for the root object of the specified DFS namespace.</span></span>

</dd> <dt>

[<span data-ttu-id="f3ac1-125">NetDfsGetStdContainerSecurity</span><span class="sxs-lookup"><span data-stu-id="f3ac1-125">NetDfsGetStdContainerSecurity</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetstdcontainersecurity)
</dt> <dd>
<span data-ttu-id="f3ac1-126">Recupera o descritor de segurança para o objeto de contêiner do namespace DFS autônomo especificado.</span><span class="sxs-lookup"><span data-stu-id="f3ac1-126">Retrieves the security descriptor for the container object of the specified stand-alone DFS namespace.</span></span>

</dd> <dt>

[<span data-ttu-id="f3ac1-127">NetDfsGetSupportedNamespaceVersion</span><span class="sxs-lookup"><span data-stu-id="f3ac1-127">NetDfsGetSupportedNamespaceVersion</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetsupportednamespaceversion)
</dt> <dd>
<span data-ttu-id="f3ac1-128">Determina o número de versão de metadados com suporte.</span><span class="sxs-lookup"><span data-stu-id="f3ac1-128">Determines the supported metadata version number.</span></span>

</dd> <dt>

[<span data-ttu-id="f3ac1-129">NetDfsMove</span><span class="sxs-lookup"><span data-stu-id="f3ac1-129">NetDfsMove</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsmove)
</dt> <dd>
<span data-ttu-id="f3ac1-130">Renomeia ou move um link DFS.</span><span class="sxs-lookup"><span data-stu-id="f3ac1-130">Renames or moves a DFS link.</span></span>

</dd> <dt>

[<span data-ttu-id="f3ac1-131">NetDfsRemove</span><span class="sxs-lookup"><span data-stu-id="f3ac1-131">NetDfsRemove</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsremove)
</dt> <dd>
<span data-ttu-id="f3ac1-132">Remove um link de Sistema de Arquivos Distribuído (DFS) ou um destino de link específico de um link DFS em um namespace DFS.</span><span class="sxs-lookup"><span data-stu-id="f3ac1-132">Removes a Distributed File System (DFS) link or a specific link target of a DFS link in a DFS namespace.</span></span> <span data-ttu-id="f3ac1-133">Ao remover um destino de link específico, o link em si será removido se o último destino de link do link for removido.</span><span class="sxs-lookup"><span data-stu-id="f3ac1-133">When removing a specific link target, the link itself is removed if the last link target of the link is removed.</span></span>

</dd> <dt>

[<span data-ttu-id="f3ac1-134">NetDfsRemoveFtRoot</span><span class="sxs-lookup"><span data-stu-id="f3ac1-134">NetDfsRemoveFtRoot</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsremoveftroot)
</dt> <dd>
<span data-ttu-id="f3ac1-135">Remove o destino raiz especificado de um namespace de Sistema de Arquivos Distribuído baseado em domínio (DFS).</span><span class="sxs-lookup"><span data-stu-id="f3ac1-135">Removes the specified root target from a domain-based Distributed File System (DFS) namespace.</span></span> <span data-ttu-id="f3ac1-136">Se o último destino raiz do namespace do DFS estiver sendo removido, a função também excluirá o namespace do DFS.</span><span class="sxs-lookup"><span data-stu-id="f3ac1-136">If the last root target of the DFS namespace is being removed, the function also deletes the DFS namespace.</span></span> <span data-ttu-id="f3ac1-137">Um namespace DFS pode ser excluído sem primeiro excluir todos os links nele.</span><span class="sxs-lookup"><span data-stu-id="f3ac1-137">A DFS namespace can be deleted without first deleting all the links in it.</span></span>

</dd> <dt>

[<span data-ttu-id="f3ac1-138">NetDfsRemoveFtRootForced</span><span class="sxs-lookup"><span data-stu-id="f3ac1-138">NetDfsRemoveFtRootForced</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsremoveftrootforced)
</dt> <dd>
<span data-ttu-id="f3ac1-139">Remove o destino raiz especificado de um namespace de Sistema de Arquivos Distribuído baseado em domínio (DFS), mesmo que o servidor de destino raiz esteja offline.</span><span class="sxs-lookup"><span data-stu-id="f3ac1-139">Removes the specified root target from a domain-based Distributed File System (DFS) namespace, even if the root target server is offline.</span></span> <span data-ttu-id="f3ac1-140">Se o último destino raiz do namespace do DFS estiver sendo removido, a função também excluirá o namespace do DFS.</span><span class="sxs-lookup"><span data-stu-id="f3ac1-140">If the last root target of the DFS namespace is being removed, the function also deletes the DFS namespace.</span></span> <span data-ttu-id="f3ac1-141">Um namespace DFS pode ser excluído sem primeiro excluir todos os links nele.</span><span class="sxs-lookup"><span data-stu-id="f3ac1-141">A DFS namespace can be deleted without first deleting all the links in it.</span></span>

> [!Note]
> <span data-ttu-id="f3ac1-142">A função [**NetDfsRemoveFtRootForced**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsremoveftrootforced) não atualiza o registro no servidor de destino raiz DFS.</span><span class="sxs-lookup"><span data-stu-id="f3ac1-142">The [**NetDfsRemoveFtRootForced**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsremoveftrootforced) function does not update the registry on the DFS root target server.</span></span> <span data-ttu-id="f3ac1-143">Para obter mais informações, consulte a seção Comentários.</span><span class="sxs-lookup"><span data-stu-id="f3ac1-143">For more information, see the Remarks section.</span></span>

</dd> <dt>

[<span data-ttu-id="f3ac1-144">NetDfsRemoveRootTarget</span><span class="sxs-lookup"><span data-stu-id="f3ac1-144">NetDfsRemoveRootTarget</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsremoveroottarget)
</dt> <dd>
<span data-ttu-id="f3ac1-145">Remove um destino raiz do DFS de um namespace DFS baseado em domínio.</span><span class="sxs-lookup"><span data-stu-id="f3ac1-145">Removes a DFS root target from a domain-based DFS namespace.</span></span> <span data-ttu-id="f3ac1-146">Se o destino raiz for o último destino raiz no namespace DFS, essa função removerá o namespace DFS.</span><span class="sxs-lookup"><span data-stu-id="f3ac1-146">If the root target is the last root target in the DFS namespace, this function removes the DFS namespace.</span></span> <span data-ttu-id="f3ac1-147">Essa função também pode ser usada para remover um namespace autônomo do DFS.</span><span class="sxs-lookup"><span data-stu-id="f3ac1-147">This function can also be used to remove a stand-alone DFS namespace.</span></span>

</dd> <dt>

[<span data-ttu-id="f3ac1-148">NetDfsRemoveStdRoot</span><span class="sxs-lookup"><span data-stu-id="f3ac1-148">NetDfsRemoveStdRoot</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsremovestdroot)
</dt> <dd>
<span data-ttu-id="f3ac1-149">Exclui um namespace de Sistema de Arquivos Distribuído autônomo (DFS).</span><span class="sxs-lookup"><span data-stu-id="f3ac1-149">Deletes a stand-alone Distributed File System (DFS) namespace.</span></span>

</dd> <dt>

[<span data-ttu-id="f3ac1-150">NetDfsSetClientInfo</span><span class="sxs-lookup"><span data-stu-id="f3ac1-150">NetDfsSetClientInfo</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetclientinfo)
</dt> <dd>
<span data-ttu-id="f3ac1-151">Modifica informações sobre uma raiz de Sistema de Arquivos Distribuído (DFS) ou link no cache mantido pelo cliente DFS.</span><span class="sxs-lookup"><span data-stu-id="f3ac1-151">Modifies information about a Distributed File System (DFS) root or link in the cache maintained by the DFS client.</span></span>

</dd> <dt>

[<span data-ttu-id="f3ac1-152">NetDfsSetFtContainerSecurity</span><span class="sxs-lookup"><span data-stu-id="f3ac1-152">NetDfsSetFtContainerSecurity</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetftcontainersecurity)
</dt> <dd>
<span data-ttu-id="f3ac1-153">Define o descritor de segurança do objeto de contêiner para os namespaces DFS baseados em domínio no domínio de Active Directory especificado.</span><span class="sxs-lookup"><span data-stu-id="f3ac1-153">Sets the security descriptor of the container object for the domain-based DFS namespaces in the specified Active Directory domain.</span></span>

</dd> <dt>

[<span data-ttu-id="f3ac1-154">NetDfsSetInfo</span><span class="sxs-lookup"><span data-stu-id="f3ac1-154">NetDfsSetInfo</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetinfo)
</dt> <dd>
<span data-ttu-id="f3ac1-155">Define ou modifica informações sobre uma raiz Sistema de Arquivos Distribuído (DFS) específica, destino raiz, link ou destino de link.</span><span class="sxs-lookup"><span data-stu-id="f3ac1-155">Sets or modifies information about a specific Distributed File System (DFS) root, root target, link, or link target.</span></span>

</dd> <dt>

[<span data-ttu-id="f3ac1-156">NetDfsSetSecurity</span><span class="sxs-lookup"><span data-stu-id="f3ac1-156">NetDfsSetSecurity</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetsecurity)
</dt> <dd>
<span data-ttu-id="f3ac1-157">Define o descritor de segurança para o objeto raiz do namespace do DFS especificado.</span><span class="sxs-lookup"><span data-stu-id="f3ac1-157">Sets the security descriptor for the root object of the specified DFS namespace.</span></span>

</dd> <dt>

[<span data-ttu-id="f3ac1-158">NetDfsSetStdContainerSecurity</span><span class="sxs-lookup"><span data-stu-id="f3ac1-158">NetDfsSetStdContainerSecurity</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetstdcontainersecurity)
</dt> <dd>
<span data-ttu-id="f3ac1-159">Define o descritor de segurança para o objeto de contêiner do namespace DFS autônomo especificado.</span><span class="sxs-lookup"><span data-stu-id="f3ac1-159">Sets the security descriptor for the container object of the specified stand-alone DFS namespace.</span></span>

</dd> </dl>

<span data-ttu-id="f3ac1-160">Observe que um aplicativo que invoca qualquer uma das funções pode fazer com que o servidor de namespace do DFS local atenda à chamada de função para executar uma sincronização completa dos metadados de namespace relacionados do mestre do emulador PDC para esse domínio.</span><span class="sxs-lookup"><span data-stu-id="f3ac1-160">Note that an application invoking any of the functions may indirectly cause the local DFS Namespace server servicing the function call to perform a full synchronization of the related namespace metadata from the PDC emulator master for that domain.</span></span> <span data-ttu-id="f3ac1-161">Essa sincronização completa pode ocorrer mesmo quando o modo de escalabilidade raiz está configurado para esse namespace.</span><span class="sxs-lookup"><span data-stu-id="f3ac1-161">This full synchronization could happen even when root scalability mode is configured for that namespace.</span></span>
