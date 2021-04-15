---
title: Classe Win32_RdvhManagement
description: Descreve um serviço de gerenciamento de Área de Trabalho Remota host virtual (RDVH).
ms.assetid: 2a81786c-e772-4596-9846-a46828f9b48b
ms.tgt_platform: multiple
keywords:
- Classe de Win32_RdvhManagement Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_RdvhManagement classe, descrita
topic_type:
- apiref
api_name:
- Win32_RdvhManagement
api_location:
- TSVmHostWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b01e2cde81173035d00587782dc45d9ddeb66fcf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105753515"
---
# <a name="win32_rdvhmanagement-class"></a><span data-ttu-id="bf9ec-105">\_Classe Win32 RdvhManagement</span><span class="sxs-lookup"><span data-stu-id="bf9ec-105">Win32\_RdvhManagement class</span></span>

<span data-ttu-id="bf9ec-106">Descreve um serviço de gerenciamento de Área de Trabalho Remota host virtual (RDVH).</span><span class="sxs-lookup"><span data-stu-id="bf9ec-106">Describes a Remote Desktop Virtual Host (RDVH) management service.</span></span>

<span data-ttu-id="bf9ec-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="bf9ec-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf9ec-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bf9ec-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_TSVmHost_Prov"), AMENDMENT]
class Win32_RdvhManagement
{
};
```

## <a name="members"></a><span data-ttu-id="bf9ec-109">Membros</span><span class="sxs-lookup"><span data-stu-id="bf9ec-109">Members</span></span>

<span data-ttu-id="bf9ec-110">A classe **Win32 \_ RdvhManagement** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="bf9ec-110">The **Win32\_RdvhManagement** class has these types of members:</span></span>

-   [<span data-ttu-id="bf9ec-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="bf9ec-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="bf9ec-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="bf9ec-112">Methods</span></span>

<span data-ttu-id="bf9ec-113">A classe **Win32 \_ RdvhManagement** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="bf9ec-113">The **Win32\_RdvhManagement** class has these methods.</span></span>



| <span data-ttu-id="bf9ec-114">Método</span><span class="sxs-lookup"><span data-stu-id="bf9ec-114">Method</span></span>                                                                                  | <span data-ttu-id="bf9ec-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="bf9ec-115">Description</span></span>                                                                                                                                                             |
|:----------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bf9ec-116">**RdvCreateUserDiskTemplate**</span><span class="sxs-lookup"><span data-stu-id="bf9ec-116">**RdvCreateUserDiskTemplate**</span></span>](rdvcreateuserdisktemplate-win32-rdvhmanagement.md)     | <span data-ttu-id="bf9ec-117">Cria o modelo de disco do usuário de tamanho máximo especificado e no local especificado.</span><span class="sxs-lookup"><span data-stu-id="bf9ec-117">Creates User Disk Template of specified max size and at the specified location.</span></span> <span data-ttu-id="bf9ec-118">Todos os discos de usuário criados terão tamanhos máximos correspondentes ao tamanho máximo do modelo.</span><span class="sxs-lookup"><span data-stu-id="bf9ec-118">All User Disks created will have max sizes matching the Template's max size.</span></span><br/> |
| [<span data-ttu-id="bf9ec-119">**RdvMigrateVmToDifferentHost**</span><span class="sxs-lookup"><span data-stu-id="bf9ec-119">**RdvMigrateVmToDifferentHost**</span></span>](rdvmigratevmtodifferenthost-win32-rdvhmanagement.md) | <span data-ttu-id="bf9ec-120">Inicia uma migração dinâmica de máquina virtual em cenários de VDI</span><span class="sxs-lookup"><span data-stu-id="bf9ec-120">Initiates a live migration of virtual machine in VDI scenarios</span></span><br/>                                                                                               |
| [<span data-ttu-id="bf9ec-121">**RdvCopyBaseVmLocally**</span><span class="sxs-lookup"><span data-stu-id="bf9ec-121">**RdvCopyBaseVmLocally**</span></span>](rdvcopybasevmlocally-win32-rdvhmanagement.md)               | <span data-ttu-id="bf9ec-122">Copia o local da VM base localmente para o Host RDV Server</span><span class="sxs-lookup"><span data-stu-id="bf9ec-122">Copies Base VM location locally to RDV Host server</span></span><br/>                                                                                                           |
| [<span data-ttu-id="bf9ec-123">**RdvCreateUserDiskTemplate**</span><span class="sxs-lookup"><span data-stu-id="bf9ec-123">**RdvCreateUserDiskTemplate**</span></span>](rdvcreateuserdisktemplate-win32-rdvhmanagement.md)     | <span data-ttu-id="bf9ec-124">Cria o modelo de disco do usuário de tamanho máximo especificado e no local especificado.</span><span class="sxs-lookup"><span data-stu-id="bf9ec-124">Creates User Disk Template of specified max size and at the specified location.</span></span> <span data-ttu-id="bf9ec-125">Todos os discos de usuário criados terão tamanhos máximos correspondentes ao tamanho máximo do modelo.</span><span class="sxs-lookup"><span data-stu-id="bf9ec-125">All User Disks created will have max sizes matching the Template's max size.</span></span><br/> |
| [<span data-ttu-id="bf9ec-126">**RdvMigrateVmToDifferentHost**</span><span class="sxs-lookup"><span data-stu-id="bf9ec-126">**RdvMigrateVmToDifferentHost**</span></span>](rdvmigratevmtodifferenthost-win32-rdvhmanagement.md) | <span data-ttu-id="bf9ec-127">Inicia uma migração dinâmica de máquina virtual em cenários de VDI.</span><span class="sxs-lookup"><span data-stu-id="bf9ec-127">Initiates a live migration of virtual machine in VDI scenarios.</span></span><br/>                                                                                              |
| [<span data-ttu-id="bf9ec-128">**RdvSetupVMPermissions**</span><span class="sxs-lookup"><span data-stu-id="bf9ec-128">**RdvSetupVMPermissions**</span></span>](rdvsetupvmpermissions-win32-rdvhmanagement.md)             | <span data-ttu-id="bf9ec-129">Define permissões na VM para o chamador</span><span class="sxs-lookup"><span data-stu-id="bf9ec-129">Sets permissions in VM for the caller</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="bf9ec-130">**RdvUndoVMPermissions**</span><span class="sxs-lookup"><span data-stu-id="bf9ec-130">**RdvUndoVMPermissions**</span></span>](rdvundovmpermissions-win32-rdvhmanagement.md)               | <span data-ttu-id="bf9ec-131">Reverte as permissões na VM definida por RdvSetupVMPermissions</span><span class="sxs-lookup"><span data-stu-id="bf9ec-131">Reverts permissions in VM set by RdvSetupVMPermissions</span></span><br/>                                                                                                       |



 

## <a name="requirements"></a><span data-ttu-id="bf9ec-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bf9ec-132">Requirements</span></span>



| <span data-ttu-id="bf9ec-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf9ec-133">Requirement</span></span> | <span data-ttu-id="bf9ec-134">Valor</span><span class="sxs-lookup"><span data-stu-id="bf9ec-134">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf9ec-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bf9ec-135">Minimum supported client</span></span><br/> | <span data-ttu-id="bf9ec-136">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="bf9ec-136">None supported</span></span><br/>                                                                  |
| <span data-ttu-id="bf9ec-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bf9ec-137">Minimum supported server</span></span><br/> | <span data-ttu-id="bf9ec-138">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="bf9ec-138">Windows Server 2012</span></span><br/>                                                             |
| <span data-ttu-id="bf9ec-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="bf9ec-139">Namespace</span></span><br/>                | <span data-ttu-id="bf9ec-140">\\TerminalServices da cimv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="bf9ec-140">Root\\cimv2\\TerminalServices</span></span><br/>                                                   |
| <span data-ttu-id="bf9ec-141">MOF</span><span class="sxs-lookup"><span data-stu-id="bf9ec-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bf9ec-142"><dt>TSVmHost. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bf9ec-142"><dt>TSVmHost.mof</dt></span></span> </dl>    |
| <span data-ttu-id="bf9ec-143">DLL</span><span class="sxs-lookup"><span data-stu-id="bf9ec-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bf9ec-144"><dt>TSVmHostWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bf9ec-144"><dt>TSVmHostWmi.dll</dt></span></span> </dl> |



 

 





