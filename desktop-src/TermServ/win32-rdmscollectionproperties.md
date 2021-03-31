---
title: Classe Win32_RDMSCollectionProperties
description: Gerencia as propriedades de uma coleção de áreas de trabalho virtuais.
ms.assetid: 8c533284-aa7b-4c47-b0a3-33307c4c805b
ms.tgt_platform: multiple
keywords:
- Classe de Win32_RDMSCollectionProperties Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_RDMSCollectionProperties classe, descrita
topic_type:
- apiref
api_name:
- Win32_RDMSCollectionProperties
- Win32_RDMSCollectionProperties.Alias
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopName
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopMachineName
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopHost
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopGuid
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopOsversion
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopRamsizeMB
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopArchitecture
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopRemoteFX
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopAdapters
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb7397ccc1afd350689ac1eeb984a62177140f50
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369511"
---
# <a name="win32_rdmscollectionproperties-class"></a><span data-ttu-id="05d0a-105">\_Classe Win32 RDMSCollectionProperties</span><span class="sxs-lookup"><span data-stu-id="05d0a-105">Win32\_RDMSCollectionProperties class</span></span>

<span data-ttu-id="05d0a-106">Gerencia as propriedades de uma coleção de áreas de trabalho virtuais.</span><span class="sxs-lookup"><span data-stu-id="05d0a-106">Manages the properties of a virtual desktop collection.</span></span>

<span data-ttu-id="05d0a-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="05d0a-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="05d0a-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="05d0a-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSCollectionProperties
{
  string  Alias;
  string  ReferenceVirtualDesktopName;
  string  ReferenceVirtualDesktopMachineName;
  string  ReferenceVirtualDesktopHost;
  string  ReferenceVirtualDesktopGuid;
  string  ReferenceVirtualDesktopOsversion;
  uint32  ReferenceVirtualDesktopRamsizeMB;
  string  ReferenceVirtualDesktopArchitecture;
  boolean ReferenceVirtualDesktopRemoteFX = false;
  string  ReferenceVirtualDesktopAdapters[];
};
```

## <a name="members"></a><span data-ttu-id="05d0a-109">Membros</span><span class="sxs-lookup"><span data-stu-id="05d0a-109">Members</span></span>

<span data-ttu-id="05d0a-110">A classe **Win32 \_ RDMSCollectionProperties** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="05d0a-110">The **Win32\_RDMSCollectionProperties** class has these types of members:</span></span>

-   [<span data-ttu-id="05d0a-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="05d0a-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="05d0a-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="05d0a-112">Properties</span></span>](/windows)

### <a name="methods"></a><span data-ttu-id="05d0a-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="05d0a-113">Methods</span></span>

<span data-ttu-id="05d0a-114">A classe **Win32 \_ RDMSCollectionProperties** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="05d0a-114">The **Win32\_RDMSCollectionProperties** class has these methods.</span></span>



| <span data-ttu-id="05d0a-115">Método</span><span class="sxs-lookup"><span data-stu-id="05d0a-115">Method</span></span>                                                                                        | <span data-ttu-id="05d0a-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="05d0a-116">Description</span></span>                                                                         |
|:----------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------|
| [<span data-ttu-id="05d0a-117">**GetProvisioningProperties**</span><span class="sxs-lookup"><span data-stu-id="05d0a-117">**GetProvisioningProperties**</span></span>](getprovisioningproperties-win32-rdmscollectionproperties.md) | <span data-ttu-id="05d0a-118">Recupera as propriedades de provisionamento da coleção de áreas de trabalho virtuais.</span><span class="sxs-lookup"><span data-stu-id="05d0a-118">Retrieves the provisioning properties of the virtual desktop collection.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="05d0a-119">Propriedades</span><span class="sxs-lookup"><span data-stu-id="05d0a-119">Properties</span></span>

<span data-ttu-id="05d0a-120">A classe **Win32 \_ RDMSCollectionProperties** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="05d0a-120">The **Win32\_RDMSCollectionProperties** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="05d0a-121">**Alias**</span><span class="sxs-lookup"><span data-stu-id="05d0a-121">**Alias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05d0a-122">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="05d0a-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05d0a-123">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="05d0a-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05d0a-124">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="05d0a-124">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="05d0a-125">Obtém o alias da coleção.</span><span class="sxs-lookup"><span data-stu-id="05d0a-125">Gets the alias of the collection.</span></span>

</dd> <dt>

<span data-ttu-id="05d0a-126">**ReferenceVirtualDesktopAdapters**</span><span class="sxs-lookup"><span data-stu-id="05d0a-126">**ReferenceVirtualDesktopAdapters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05d0a-127">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="05d0a-127">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="05d0a-128">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="05d0a-128">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="05d0a-129">Obtém e define os nomes dos adaptadores de rede virtual da VM mestre.</span><span class="sxs-lookup"><span data-stu-id="05d0a-129">Gets and sets the names of the virtual network adapters of the master VM.</span></span>

</dd> <dt>

<span data-ttu-id="05d0a-130">**ReferenceVirtualDesktopArchitecture**</span><span class="sxs-lookup"><span data-stu-id="05d0a-130">**ReferenceVirtualDesktopArchitecture**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05d0a-131">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="05d0a-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05d0a-132">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="05d0a-132">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="05d0a-133">Obtém e define a arquitetura do processador da VM mestre.</span><span class="sxs-lookup"><span data-stu-id="05d0a-133">Gets and sets the processor architecture of the master VM.</span></span>

</dd> <dt>

<span data-ttu-id="05d0a-134">**ReferenceVirtualDesktopGuid**</span><span class="sxs-lookup"><span data-stu-id="05d0a-134">**ReferenceVirtualDesktopGuid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05d0a-135">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="05d0a-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05d0a-136">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="05d0a-136">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="05d0a-137">Obtém e define o GUID da VM mestre.</span><span class="sxs-lookup"><span data-stu-id="05d0a-137">Gets and sets the GUID of the master VM.</span></span>

</dd> <dt>

<span data-ttu-id="05d0a-138">**ReferenceVirtualDesktopHost**</span><span class="sxs-lookup"><span data-stu-id="05d0a-138">**ReferenceVirtualDesktopHost**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05d0a-139">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="05d0a-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05d0a-140">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="05d0a-140">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="05d0a-141">Obtém e define o nome do servidor host da VM mestre.</span><span class="sxs-lookup"><span data-stu-id="05d0a-141">Gets and sets the host server name of the master VM.</span></span>

</dd> <dt>

<span data-ttu-id="05d0a-142">**ReferenceVirtualDesktopMachineName**</span><span class="sxs-lookup"><span data-stu-id="05d0a-142">**ReferenceVirtualDesktopMachineName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05d0a-143">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="05d0a-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05d0a-144">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="05d0a-144">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="05d0a-145">Obtém e define o nome do computador da VM mestre.</span><span class="sxs-lookup"><span data-stu-id="05d0a-145">Gets and sets the machine name of the master VM.</span></span>

</dd> <dt>

<span data-ttu-id="05d0a-146">**ReferenceVirtualDesktopName**</span><span class="sxs-lookup"><span data-stu-id="05d0a-146">**ReferenceVirtualDesktopName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05d0a-147">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="05d0a-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05d0a-148">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="05d0a-148">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="05d0a-149">Obtém e define o nome da VM mestra.</span><span class="sxs-lookup"><span data-stu-id="05d0a-149">Gets and sets the name of the master VM.</span></span>

</dd> <dt>

<span data-ttu-id="05d0a-150">**ReferenceVirtualDesktopOsversion**</span><span class="sxs-lookup"><span data-stu-id="05d0a-150">**ReferenceVirtualDesktopOsversion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05d0a-151">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="05d0a-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05d0a-152">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="05d0a-152">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="05d0a-153">Obtém e define a versão do sistema operacional da VM mestre.</span><span class="sxs-lookup"><span data-stu-id="05d0a-153">Gets and sets the OS version of the master VM.</span></span>

</dd> <dt>

<span data-ttu-id="05d0a-154">**ReferenceVirtualDesktopRamsizeMB**</span><span class="sxs-lookup"><span data-stu-id="05d0a-154">**ReferenceVirtualDesktopRamsizeMB**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05d0a-155">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="05d0a-155">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="05d0a-156">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="05d0a-156">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="05d0a-157">Obtém e define o tamanho da memória da VM mestre.</span><span class="sxs-lookup"><span data-stu-id="05d0a-157">Gets and sets the memory size of the master VM.</span></span>

</dd> <dt>

<span data-ttu-id="05d0a-158">**ReferenceVirtualDesktopRemoteFX**</span><span class="sxs-lookup"><span data-stu-id="05d0a-158">**ReferenceVirtualDesktopRemoteFX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05d0a-159">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="05d0a-159">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="05d0a-160">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="05d0a-160">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="05d0a-161">Obtém e define um valor que indica se o RemoteFX está habilitado para a VM mestre.</span><span class="sxs-lookup"><span data-stu-id="05d0a-161">Gets and sets a value that indicates whether RemoteFX is enabled for the master VM.</span></span> <span data-ttu-id="05d0a-162">**True** se o RemoteFX estiver habilitado; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="05d0a-162">**TRUE** if RemoteFX is enabled; otherwise, **FALSE**.</span></span> <span data-ttu-id="05d0a-163">O valor padrão dessa propriedade é **false**.</span><span class="sxs-lookup"><span data-stu-id="05d0a-163">The default value for this property is **FALSE**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="05d0a-164">Requisitos</span><span class="sxs-lookup"><span data-stu-id="05d0a-164">Requirements</span></span>



| <span data-ttu-id="05d0a-165">Requisito</span><span class="sxs-lookup"><span data-stu-id="05d0a-165">Requirement</span></span> | <span data-ttu-id="05d0a-166">Valor</span><span class="sxs-lookup"><span data-stu-id="05d0a-166">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="05d0a-167">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="05d0a-167">Minimum supported client</span></span><br/> | <span data-ttu-id="05d0a-168">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="05d0a-168">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="05d0a-169">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="05d0a-169">Minimum supported server</span></span><br/> | <span data-ttu-id="05d0a-170">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="05d0a-170">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="05d0a-171">Namespace</span><span class="sxs-lookup"><span data-stu-id="05d0a-171">Namespace</span></span><br/>                | <span data-ttu-id="05d0a-172">\\RDMs cimv2 \\ raiz</span><span class="sxs-lookup"><span data-stu-id="05d0a-172">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="05d0a-173">MOF</span><span class="sxs-lookup"><span data-stu-id="05d0a-173">MOF</span></span><br/>                      | <dl> <span data-ttu-id="05d0a-174"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="05d0a-174"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="05d0a-175">DLL</span><span class="sxs-lookup"><span data-stu-id="05d0a-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="05d0a-176"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="05d0a-176"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="05d0a-177">Consulte também</span><span class="sxs-lookup"><span data-stu-id="05d0a-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05d0a-178">Provedor de serviços de gerenciamento de Área de Trabalho Remota</span><span class="sxs-lookup"><span data-stu-id="05d0a-178">Remote Desktop Management Services Provider</span></span>](rdms-api-reference.md)
</dt> </dl>

 

