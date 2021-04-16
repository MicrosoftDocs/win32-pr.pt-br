---
description: Gerencia os recursos da \_ instância ResourcePoolConfigurationService do CIM para um \_ objeto RESOURCEPOOL do CIM.
ms.assetid: bd2eb4da-8ecd-4adb-b657-837c8da4dcdc
title: Classe CIM_ResourcePoolConfigurationCapabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourcePoolConfigurationCapabilities
- CIM_ResourcePoolConfigurationCapabilities.AsynchronousMethodsSupported
- CIM_ResourcePoolConfigurationCapabilities.SynchronousMethodsSupported
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 967b307049fa9c5f81b8deb6da96bcaa3be9acc8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105782365"
---
# <a name="cim_resourcepoolconfigurationcapabilities-class"></a><span data-ttu-id="54940-103">\_Classe CIM ResourcePoolConfigurationCapabilities</span><span class="sxs-lookup"><span data-stu-id="54940-103">CIM\_ResourcePoolConfigurationCapabilities class</span></span>

<span data-ttu-id="54940-104">Gerencia os recursos da instância [**\_ ResourcePoolConfigurationService do CIM**](cim-resourcepoolconfigurationservice.md) para um objeto [**\_ ResourcePool do CIM**](cim-resourcepool.md) .</span><span class="sxs-lookup"><span data-stu-id="54940-104">Manages the capabilities of the [**CIM\_ResourcePoolConfigurationService**](cim-resourcepoolconfigurationservice.md) instance for a [**CIM\_ResourcePool**](cim-resourcepool.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="54940-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="54940-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::Resource")]
class CIM_ResourcePoolConfigurationCapabilities : CIM_Capabilities
{
  uint32 AsynchronousMethodsSupported[];
  uint32 SynchronousMethodsSupported[];
};
```

## <a name="members"></a><span data-ttu-id="54940-106">Membros</span><span class="sxs-lookup"><span data-stu-id="54940-106">Members</span></span>

<span data-ttu-id="54940-107">A classe **CIM \_ ResourcePoolConfigurationCapabilities** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="54940-107">The **CIM\_ResourcePoolConfigurationCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="54940-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="54940-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="54940-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="54940-109">Properties</span></span>

<span data-ttu-id="54940-110">A classe **CIM \_ ResourcePoolConfigurationCapabilities** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="54940-110">The **CIM\_ResourcePoolConfigurationCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="54940-111">**AsynchronousMethodsSupported**</span><span class="sxs-lookup"><span data-stu-id="54940-111">**AsynchronousMethodsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54940-112">Tipo de dados: matriz **UInt32**</span><span class="sxs-lookup"><span data-stu-id="54940-112">Data type: **uint32** array</span></span>
</dt> <dt>

<span data-ttu-id="54940-113">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="54940-113">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="54940-114">Os métodos do serviço de configuração que têm suporte para operações assíncronas.</span><span class="sxs-lookup"><span data-stu-id="54940-114">The methods of the configuration service that are supported for asynchronous operations.</span></span>

<dt>

<span id="CreateResourcePool_is_supported"></span><span id="createresourcepool_is_supported"></span><span id="CREATERESOURCEPOOL_IS_SUPPORTED"></span>

<span data-ttu-id="54940-115">**CreateResourcePool tem suporte** (2)</span><span class="sxs-lookup"><span data-stu-id="54940-115">**CreateResourcePool is supported** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="CreateChild_ResourcePool_is_supported"></span><span id="createchild_resourcepool_is_supported"></span><span id="CREATECHILD_RESOURCEPOOL_IS_SUPPORTED"></span>

<span data-ttu-id="54940-116">**CreateChild ResourcePool tem suporte** (3)</span><span class="sxs-lookup"><span data-stu-id="54940-116">**CreateChild ResourcePool is supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DeleteResourcePool_is_supported"></span><span id="deleteresourcepool_is_supported"></span><span id="DELETERESOURCEPOOL_IS_SUPPORTED"></span>

<span data-ttu-id="54940-117">**DeleteResourcePool tem suporte** (4)</span><span class="sxs-lookup"><span data-stu-id="54940-117">**DeleteResourcePool is supported** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="AddResourcesToResourcePool_is_supported"></span><span id="addresourcestoresourcepool_is_supported"></span><span id="ADDRESOURCESTORESOURCEPOOL_IS_SUPPORTED"></span>

<span data-ttu-id="54940-118">**AddResourcesToResourcePool tem suporte** (5)</span><span class="sxs-lookup"><span data-stu-id="54940-118">**AddResourcesToResourcePool is supported** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="RemoveResourcesFromResourcePool_is_supported"></span><span id="removeresourcesfromresourcepool_is_supported"></span><span id="REMOVERESOURCESFROMRESOURCEPOOL_IS_SUPPORTED"></span>

<span data-ttu-id="54940-119">**RemoveResourcesFromResourcePool tem suporte** (6)</span><span class="sxs-lookup"><span data-stu-id="54940-119">**RemoveResourcesFromResourcePool is supported** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="ChangeParentResourcePool_is_supported"></span><span id="changeparentresourcepool_is_supported"></span><span id="CHANGEPARENTRESOURCEPOOL_IS_SUPPORTED"></span>

<span data-ttu-id="54940-120">**ChangeParentResourcePool tem suporte** (7)</span><span class="sxs-lookup"><span data-stu-id="54940-120">**ChangeParentResourcePool is supported** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="54940-121">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="54940-121">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="54940-122">**Fornecedor reservado** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="54940-122">**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="54940-123">**SynchronousMethodsSupported**</span><span class="sxs-lookup"><span data-stu-id="54940-123">**SynchronousMethodsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54940-124">Tipo de dados: matriz **UInt32**</span><span class="sxs-lookup"><span data-stu-id="54940-124">Data type: **uint32** array</span></span>
</dt> <dt>

<span data-ttu-id="54940-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="54940-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="54940-126">Os métodos do serviço de configuração que têm suporte para operações síncronas.</span><span class="sxs-lookup"><span data-stu-id="54940-126">The methods of the configuration service that are supported for synchronous operations.</span></span>

<dt>

<span id="CreateResourcePool_is_supported"></span><span id="createresourcepool_is_supported"></span><span id="CREATERESOURCEPOOL_IS_SUPPORTED"></span>

<span data-ttu-id="54940-127">**CreateResourcePool tem suporte** (2)</span><span class="sxs-lookup"><span data-stu-id="54940-127">**CreateResourcePool is supported** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="CreateChild_ResourcePool_is_supported"></span><span id="createchild_resourcepool_is_supported"></span><span id="CREATECHILD_RESOURCEPOOL_IS_SUPPORTED"></span>

<span data-ttu-id="54940-128">**CreateChild ResourcePool tem suporte** (3)</span><span class="sxs-lookup"><span data-stu-id="54940-128">**CreateChild ResourcePool is supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DeleteResourcePool_is_supported"></span><span id="deleteresourcepool_is_supported"></span><span id="DELETERESOURCEPOOL_IS_SUPPORTED"></span>

<span data-ttu-id="54940-129">**DeleteResourcePool tem suporte** (4)</span><span class="sxs-lookup"><span data-stu-id="54940-129">**DeleteResourcePool is supported** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="AddResourcesToResourcePool_is_supported"></span><span id="addresourcestoresourcepool_is_supported"></span><span id="ADDRESOURCESTORESOURCEPOOL_IS_SUPPORTED"></span>

<span data-ttu-id="54940-130">**AddResourcesToResourcePool tem suporte** (5)</span><span class="sxs-lookup"><span data-stu-id="54940-130">**AddResourcesToResourcePool is supported** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="RemoveResourcesFromResourcePool_is_supported"></span><span id="removeresourcesfromresourcepool_is_supported"></span><span id="REMOVERESOURCESFROMRESOURCEPOOL_IS_SUPPORTED"></span>

<span data-ttu-id="54940-131">**RemoveResourcesFromResourcePool tem suporte** (6)</span><span class="sxs-lookup"><span data-stu-id="54940-131">**RemoveResourcesFromResourcePool is supported** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="CIM_ChangeParentResourcePool_is_supported"></span><span id="cim_changeparentresourcepool_is_supported"></span><span id="CIM_CHANGEPARENTRESOURCEPOOL_IS_SUPPORTED"></span>

<span data-ttu-id="54940-132">**CIM \_ ChangeParentResourcePool tem suporte** (7)</span><span class="sxs-lookup"><span data-stu-id="54940-132">**CIM\_ChangeParentResourcePool is supported** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="54940-133">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="54940-133">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="54940-134">**Fornecedor reservado** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="54940-134">**Vendor Reserved** (32768..65535)</span></span>


<span data-ttu-id="54940-135"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="54940-135"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="54940-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="54940-136">Requirements</span></span>



| <span data-ttu-id="54940-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="54940-137">Requirement</span></span> | <span data-ttu-id="54940-138">Valor</span><span class="sxs-lookup"><span data-stu-id="54940-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="54940-139">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="54940-139">Minimum supported client</span></span><br/> | <span data-ttu-id="54940-140">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="54940-140">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="54940-141">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="54940-141">Minimum supported server</span></span><br/> | <span data-ttu-id="54940-142">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="54940-142">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="54940-143">Namespace</span><span class="sxs-lookup"><span data-stu-id="54940-143">Namespace</span></span><br/>                | <span data-ttu-id="54940-144">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="54940-144">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="54940-145">MOF</span><span class="sxs-lookup"><span data-stu-id="54940-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="54940-146"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="54940-146"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="54940-147">DLL</span><span class="sxs-lookup"><span data-stu-id="54940-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="54940-148"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="54940-148"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="54940-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="54940-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54940-150">**Recursos de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="54940-150">**CIM\_Capabilities**</span></span>](cim-capabilities.md)
</dt> </dl>

 

 




