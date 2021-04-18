---
description: Usado no método QueryGuestClusterInformation na \_ classe VssService Msvm para recuperar informações sobre o cluster de convidado do qual a VM faz parte.
ms.assetid: c484b38d-9137-44da-a368-a2a673b94ef8
title: Classe Msvm_GuestClusterInformation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestClusterInformation
- Msvm_GuestClusterInformation.ClusterId
- Msvm_GuestClusterInformation.ClusterSize
- Msvm_GuestClusterInformation.SharedVirtualHardDisks
- Msvm_GuestClusterInformation.SharedVirtualHardDiskPaths
- Msvm_GuestClusterInformation.IsClustered
- Msvm_GuestClusterInformation.IsOnline
- Msvm_GuestClusterInformation.IsOwned
- Msvm_GuestClusterInformation.IsActiveActive
- Msvm_GuestClusterInformation.LastResourceMoveTime
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ee7fa33f142e47b9493e53aa5bc4779623d6ef40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105770217"
---
# <a name="msvm_guestclusterinformation-class"></a><span data-ttu-id="95f74-103">\_Classe Msvm GuestClusterInformation</span><span class="sxs-lookup"><span data-stu-id="95f74-103">Msvm\_GuestClusterInformation class</span></span>

<span data-ttu-id="95f74-104">Usado no método [**QueryGuestClusterInformation**](msvm-vssservice-queryguestclusterinformation.md) na classe [**\_ VssService Msvm**](msvm-vssservice.md) para recuperar informações sobre o cluster de convidado do qual a VM faz parte.</span><span class="sxs-lookup"><span data-stu-id="95f74-104">Used in the [**QueryGuestClusterInformation**](msvm-vssservice-queryguestclusterinformation.md) method in the [**Msvm\_VssService**](msvm-vssservice.md) class to retrieve information about the guest cluster the VM is part of.</span></span>

<span data-ttu-id="95f74-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="95f74-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="95f74-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="95f74-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_GuestClusterInformation
{
  string  ClusterId;
  uint16  ClusterSize;
  string  SharedVirtualHardDisks[];
  string  SharedVirtualHardDiskPaths[];
  boolean IsClustered[];
  boolean IsOnline[];
  boolean IsOwned[];
  boolean IsActiveActive[];
  uint64  LastResourceMoveTime;
};
```

## <a name="members"></a><span data-ttu-id="95f74-107">Membros</span><span class="sxs-lookup"><span data-stu-id="95f74-107">Members</span></span>

<span data-ttu-id="95f74-108">A classe **Msvm \_ GuestClusterInformation** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="95f74-108">The **Msvm\_GuestClusterInformation** class has these types of members:</span></span>

-   [<span data-ttu-id="95f74-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="95f74-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="95f74-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="95f74-110">Properties</span></span>

<span data-ttu-id="95f74-111">A classe **Msvm \_ GuestClusterInformation** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="95f74-111">The **Msvm\_GuestClusterInformation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="95f74-112">**ClusterId**</span><span class="sxs-lookup"><span data-stu-id="95f74-112">**ClusterId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95f74-113">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="95f74-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="95f74-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="95f74-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="95f74-115">O identificador do cluster de failover do qual o sistema operacional convidado da VM faz parte.</span><span class="sxs-lookup"><span data-stu-id="95f74-115">The identifier of the failover cluster the VM's guest Operating System is a part of.</span></span>

</dd> <dt>

<span data-ttu-id="95f74-116">**ClusterSize**</span><span class="sxs-lookup"><span data-stu-id="95f74-116">**ClusterSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95f74-117">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="95f74-117">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="95f74-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="95f74-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="95f74-119">Número de nós no cluster do qual o sistema operacional convidado da VM faz parte.</span><span class="sxs-lookup"><span data-stu-id="95f74-119">Number of nodes in the cluster the VM's guest Operating System is a part of.</span></span>

</dd> <dt>

<span data-ttu-id="95f74-120">**IsActiveActive**</span><span class="sxs-lookup"><span data-stu-id="95f74-120">**IsActiveActive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95f74-121">Tipo de dados: matriz **booliana**</span><span class="sxs-lookup"><span data-stu-id="95f74-121">Data type: **boolean** array</span></span>
</dt> <dt>

<span data-ttu-id="95f74-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="95f74-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95f74-123">Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado")</span><span class="sxs-lookup"><span data-stu-id="95f74-123">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="95f74-124">Uma matriz de boolianos correspondente a cada disco rígido virtual compartilhado que indica se o recurso de disco correspondente no cluster de convidado é compartilhado entre VMs no modo ativo/ativo.</span><span class="sxs-lookup"><span data-stu-id="95f74-124">An array of booleans corresponding to each shared virtual hard disk indicating if the corresponding disk resource in the guest cluster is shared between VMs in active/active mode.</span></span>

</dd> <dt>

<span data-ttu-id="95f74-125">**IsClustered**</span><span class="sxs-lookup"><span data-stu-id="95f74-125">**IsClustered**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95f74-126">Tipo de dados: matriz **booliana**</span><span class="sxs-lookup"><span data-stu-id="95f74-126">Data type: **boolean** array</span></span>
</dt> <dt>

<span data-ttu-id="95f74-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="95f74-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95f74-128">Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado")</span><span class="sxs-lookup"><span data-stu-id="95f74-128">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="95f74-129">Uma matriz de boolianos correspondente a cada disco rígido virtual compartilhado que indica se o disco correspondente é um recurso de cluster no cluster de convidado.</span><span class="sxs-lookup"><span data-stu-id="95f74-129">An array of booleans corresponding to each shared virtual hard disk indicating if the corresponding disk is a cluster resource in the guest cluster.</span></span>

</dd> <dt>

<span data-ttu-id="95f74-130">**IsOnline**</span><span class="sxs-lookup"><span data-stu-id="95f74-130">**IsOnline**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95f74-131">Tipo de dados: matriz **booliana**</span><span class="sxs-lookup"><span data-stu-id="95f74-131">Data type: **boolean** array</span></span>
</dt> <dt>

<span data-ttu-id="95f74-132">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="95f74-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95f74-133">Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado")</span><span class="sxs-lookup"><span data-stu-id="95f74-133">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="95f74-134">Uma matriz de boolianos correspondente a cada disco rígido virtual compartilhado que indica se o recurso de disco correspondente no cluster de convidado está online.</span><span class="sxs-lookup"><span data-stu-id="95f74-134">An array of booleans corresponding to each shared virtual hard disk indicating if the corresponding disk resource in the guest cluster is online.</span></span>

</dd> <dt>

<span data-ttu-id="95f74-135">**Isdele**</span><span class="sxs-lookup"><span data-stu-id="95f74-135">**IsOwned**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95f74-136">Tipo de dados: matriz **booliana**</span><span class="sxs-lookup"><span data-stu-id="95f74-136">Data type: **boolean** array</span></span>
</dt> <dt>

<span data-ttu-id="95f74-137">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="95f74-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95f74-138">Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado")</span><span class="sxs-lookup"><span data-stu-id="95f74-138">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="95f74-139">Uma matriz de boolianos correspondente a cada disco rígido virtual compartilhado que indica se o recurso de disco correspondente no cluster de convidado é currenly pertencente a essa VM.</span><span class="sxs-lookup"><span data-stu-id="95f74-139">An array of booleans corresponding to each shared virtual hard disk indicating if the corresponding disk resource in the guest cluster is currenly owned by this VM.</span></span>

</dd> <dt>

<span data-ttu-id="95f74-140">**LastResourceMoveTime**</span><span class="sxs-lookup"><span data-stu-id="95f74-140">**LastResourceMoveTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95f74-141">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="95f74-141">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="95f74-142">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="95f74-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="95f74-143">A contagem de tiques de relógio quando um dos recursos de disco compartilhado foi movido pela última vez.</span><span class="sxs-lookup"><span data-stu-id="95f74-143">The clock tick count when one of the shared disk resources last moved.</span></span>

> [!Note]  
> <span data-ttu-id="95f74-144">Essa propriedade foi adicionada no Windows 10, versão 1703 e Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="95f74-144">This property was added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="95f74-145">**SharedVirtualHardDiskPaths**</span><span class="sxs-lookup"><span data-stu-id="95f74-145">**SharedVirtualHardDiskPaths**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95f74-146">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="95f74-146">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="95f74-147">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="95f74-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95f74-148">Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado")</span><span class="sxs-lookup"><span data-stu-id="95f74-148">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="95f74-149">Uma matriz de caminhos de disco rígido virtual compartilhados conectados à VM.</span><span class="sxs-lookup"><span data-stu-id="95f74-149">An array of shared virtual hard disk paths connected to the VM.</span></span>

</dd> <dt>

<span data-ttu-id="95f74-150">**SharedVirtualHardDisks**</span><span class="sxs-lookup"><span data-stu-id="95f74-150">**SharedVirtualHardDisks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95f74-151">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="95f74-151">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="95f74-152">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="95f74-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95f74-153">Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado")</span><span class="sxs-lookup"><span data-stu-id="95f74-153">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="95f74-154">Uma matriz de dados de configuração de alocação de recursos (RASD) que representa os discos rígidos virtuais compartilhados conectados à VM.</span><span class="sxs-lookup"><span data-stu-id="95f74-154">An array of Resource Allocation Setting Data (RASD) representing the shared virtual hard disks connected to the VM.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="95f74-155">Requisitos</span><span class="sxs-lookup"><span data-stu-id="95f74-155">Requirements</span></span>



| <span data-ttu-id="95f74-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="95f74-156">Requirement</span></span> | <span data-ttu-id="95f74-157">Valor</span><span class="sxs-lookup"><span data-stu-id="95f74-157">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95f74-158">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="95f74-158">Minimum supported client</span></span><br/> | <span data-ttu-id="95f74-159">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="95f74-159">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="95f74-160">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="95f74-160">Minimum supported server</span></span><br/> | <span data-ttu-id="95f74-161">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="95f74-161">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="95f74-162">Namespace</span><span class="sxs-lookup"><span data-stu-id="95f74-162">Namespace</span></span><br/>                | <span data-ttu-id="95f74-163">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="95f74-163">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="95f74-164">MOF</span><span class="sxs-lookup"><span data-stu-id="95f74-164">MOF</span></span><br/>                      | <dl> <span data-ttu-id="95f74-165"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="95f74-165"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="95f74-166">DLL</span><span class="sxs-lookup"><span data-stu-id="95f74-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="95f74-167"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="95f74-167"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

