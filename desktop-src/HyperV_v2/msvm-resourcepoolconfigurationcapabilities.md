---
description: Descreve os recursos da \_ classe Msvm ResourcePoolConfigurationService associada.
ms.assetid: 3e6857f9-62a0-420b-8f1d-8aad685a7ff7
title: Classe Msvm_ResourcePoolConfigurationCapabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourcePoolConfigurationCapabilities
- Msvm_ResourcePoolConfigurationCapabilities.InstanceID
- Msvm_ResourcePoolConfigurationCapabilities.Caption
- Msvm_ResourcePoolConfigurationCapabilities.Description
- Msvm_ResourcePoolConfigurationCapabilities.ElementName
- Msvm_ResourcePoolConfigurationCapabilities.AsynchronousMethodsSupported
- Msvm_ResourcePoolConfigurationCapabilities.SynchronousMethodsSupported
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b70d9e84e2c85d4c5b702a638982df0b47d62193
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828885"
---
# <a name="msvm_resourcepoolconfigurationcapabilities-class"></a><span data-ttu-id="09476-103">\_Classe Msvm ResourcePoolConfigurationCapabilities</span><span class="sxs-lookup"><span data-stu-id="09476-103">Msvm\_ResourcePoolConfigurationCapabilities class</span></span>

<span data-ttu-id="09476-104">Descreve os recursos da classe [**Msvm \_ ResourcePoolConfigurationService**](msvm-resourcepoolconfigurationservice.md) associada.</span><span class="sxs-lookup"><span data-stu-id="09476-104">Describes the capabilities of the associated [**Msvm\_ResourcePoolConfigurationService**](msvm-resourcepoolconfigurationservice.md) class.</span></span> <span data-ttu-id="09476-105">Os clientes podem usar instâncias dessa classe para determinar quais métodos têm suporte de forma síncrona ou assíncrona.</span><span class="sxs-lookup"><span data-stu-id="09476-105">Clients can use instances of this class to determine which methods are supported synchronously or asynchronously.</span></span> <span data-ttu-id="09476-106">O mesmo método não deve estar em ambas as listas.</span><span class="sxs-lookup"><span data-stu-id="09476-106">The same method must not be in both lists.</span></span> <span data-ttu-id="09476-107">Implementações de método devem ser síncronas ou assíncronas.</span><span class="sxs-lookup"><span data-stu-id="09476-107">Method implementations must either be synchronous or asynchronous.</span></span>

<span data-ttu-id="09476-108">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="09476-108">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="09476-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="09476-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider")]
class Msvm_ResourcePoolConfigurationCapabilities : CIM_Capabilities
{
  string InstanceID;
  string Caption = "Resource Pool Configuration Capabilities";
  string Description = "Microsoft Resource Pool Configuration Capabilities";
  string ElementName = "Resource Pool Configuration Capabilities";
  uint32 AsynchronousMethodsSupported[];
  uint32 SynchronousMethodsSupported[];
};
```

## <a name="members"></a><span data-ttu-id="09476-110">Membros</span><span class="sxs-lookup"><span data-stu-id="09476-110">Members</span></span>

<span data-ttu-id="09476-111">A classe **Msvm \_ ResourcePoolConfigurationCapabilities** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="09476-111">The **Msvm\_ResourcePoolConfigurationCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="09476-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="09476-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="09476-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="09476-113">Properties</span></span>

<span data-ttu-id="09476-114">A classe **Msvm \_ ResourcePoolConfigurationCapabilities** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="09476-114">The **Msvm\_ResourcePoolConfigurationCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="09476-115">**AsynchronousMethodsSupported**</span><span class="sxs-lookup"><span data-stu-id="09476-115">**AsynchronousMethodsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09476-116">Tipo de dados: matriz **UInt32**</span><span class="sxs-lookup"><span data-stu-id="09476-116">Data type: **uint32** array</span></span>
</dt> <dt>

<span data-ttu-id="09476-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="09476-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09476-118">Uma matriz de identificadores de método, cada um identificando um método da classe [**Msvm \_ ResourcePoolConfigurationService**](msvm-resourcepoolconfigurationservice.md) que tem suporte de forma assíncrona pela implementação.</span><span class="sxs-lookup"><span data-stu-id="09476-118">An array of method identifiers, each identifying a method of the [**Msvm\_ResourcePoolConfigurationService**](msvm-resourcepoolconfigurationservice.md) class that is supported asynchronously by the implementation.</span></span>

<dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="09476-119">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="09476-119">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="CreatePool_is_supported"></span><span id="createpool_is_supported"></span><span id="CREATEPOOL_IS_SUPPORTED"></span>

<span data-ttu-id="09476-120">**Createpool tem suporte** (32768)</span><span class="sxs-lookup"><span data-stu-id="09476-120">**CreatePool is supported** (32768)</span></span>


</dt> <dd></dd> <dt>

<span id="ChangePoolResources_is_supported"></span><span id="changepoolresources_is_supported"></span><span id="CHANGEPOOLRESOURCES_IS_SUPPORTED"></span>

<span data-ttu-id="09476-121">**ChangePoolResources tem suporte** (32769)</span><span class="sxs-lookup"><span data-stu-id="09476-121">**ChangePoolResources is supported** (32769)</span></span>


</dt> <dd></dd> <dt>

<span id="ChangePoolSettings_is_supported"></span><span id="changepoolsettings_is_supported"></span><span id="CHANGEPOOLSETTINGS_IS_SUPPORTED"></span>

<span data-ttu-id="09476-122">**ChangePoolSettings tem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="09476-122">**ChangePoolSettings is supported** (32770)</span></span>


</dt> <dd></dd> <dt>

<span id="DeletePool_is_supported"></span><span id="deletepool_is_supported"></span><span id="DELETEPOOL_IS_SUPPORTED"></span>

<span data-ttu-id="09476-123">**DeletePool tem suporte** (32771)</span><span class="sxs-lookup"><span data-stu-id="09476-123">**DeletePool is supported** (32771)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="09476-124">**Fornecedor reservado** (32772.. 65535)</span><span class="sxs-lookup"><span data-stu-id="09476-124">**Vendor Reserved** (32772..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="09476-125">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="09476-125">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09476-126">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="09476-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="09476-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="09476-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09476-128">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="09476-128">A short description of the object.</span></span> <span data-ttu-id="09476-129">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "recursos de configuração do pool de recursos".</span><span class="sxs-lookup"><span data-stu-id="09476-129">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Resource Pool Configuration Capabilities".</span></span>

</dd> <dt>

<span data-ttu-id="09476-130">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="09476-130">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09476-131">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="09476-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="09476-132">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="09476-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09476-133">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="09476-133">A description of the object.</span></span> <span data-ttu-id="09476-134">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "recursos de configuração do pool de recursos da Microsoft".</span><span class="sxs-lookup"><span data-stu-id="09476-134">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Microsoft Resource Pool Configuration Capabilities".</span></span>

</dd> <dt>

<span data-ttu-id="09476-135">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="09476-135">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09476-136">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="09476-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="09476-137">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="09476-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09476-138">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="09476-138">A display name for the object.</span></span> <span data-ttu-id="09476-139">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "recursos de configuração do pool de recursos".</span><span class="sxs-lookup"><span data-stu-id="09476-139">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Resource Pool Configuration Capabilities".</span></span>

</dd> <dt>

<span data-ttu-id="09476-140">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="09476-140">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09476-141">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="09476-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="09476-142">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="09476-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="09476-143">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="09476-143">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="09476-144">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="09476-144">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="09476-145">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="09476-145">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="09476-146">**SynchronousMethodsSupported**</span><span class="sxs-lookup"><span data-stu-id="09476-146">**SynchronousMethodsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09476-147">Tipo de dados: matriz **UInt32**</span><span class="sxs-lookup"><span data-stu-id="09476-147">Data type: **uint32** array</span></span>
</dt> <dt>

<span data-ttu-id="09476-148">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="09476-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09476-149">Uma matriz de identificadores de método, cada um identificando um método da classe [**Msvm \_ ResourcePoolConfigurationService**](msvm-resourcepoolconfigurationservice.md) que tem suporte de forma síncrona pela implementação.</span><span class="sxs-lookup"><span data-stu-id="09476-149">An array of method identifiers, each identifying a method of the [**Msvm\_ResourcePoolConfigurationService**](msvm-resourcepoolconfigurationservice.md) class that is supported synchronously by the implementation.</span></span>

<dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="09476-150">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="09476-150">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="CreatePool_is_supported"></span><span id="createpool_is_supported"></span><span id="CREATEPOOL_IS_SUPPORTED"></span>

<span data-ttu-id="09476-151">**Createpool tem suporte** (32768)</span><span class="sxs-lookup"><span data-stu-id="09476-151">**CreatePool is supported** (32768)</span></span>


</dt> <dd></dd> <dt>

<span id="ChangePoolResources_is_supported"></span><span id="changepoolresources_is_supported"></span><span id="CHANGEPOOLRESOURCES_IS_SUPPORTED"></span>

<span data-ttu-id="09476-152">**ChangePoolResources tem suporte** (32769)</span><span class="sxs-lookup"><span data-stu-id="09476-152">**ChangePoolResources is supported** (32769)</span></span>


</dt> <dd></dd> <dt>

<span id="ChangePoolSettings_is_supported"></span><span id="changepoolsettings_is_supported"></span><span id="CHANGEPOOLSETTINGS_IS_SUPPORTED"></span>

<span data-ttu-id="09476-153">**ChangePoolSettings tem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="09476-153">**ChangePoolSettings is supported** (32770)</span></span>


</dt> <dd></dd> <dt>

<span id="DeletePool_is_supported"></span><span id="deletepool_is_supported"></span><span id="DELETEPOOL_IS_SUPPORTED"></span>

<span data-ttu-id="09476-154">**DeletePool tem suporte** (32771)</span><span class="sxs-lookup"><span data-stu-id="09476-154">**DeletePool is supported** (32771)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="09476-155">**Fornecedor reservado** (32772.. 65535)</span><span class="sxs-lookup"><span data-stu-id="09476-155">**Vendor Reserved** (32772..65535)</span></span>


<span data-ttu-id="09476-156"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="09476-156"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="09476-157">Requisitos</span><span class="sxs-lookup"><span data-stu-id="09476-157">Requirements</span></span>



| <span data-ttu-id="09476-158">Requisito</span><span class="sxs-lookup"><span data-stu-id="09476-158">Requirement</span></span> | <span data-ttu-id="09476-159">Valor</span><span class="sxs-lookup"><span data-stu-id="09476-159">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09476-160">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="09476-160">Minimum supported client</span></span><br/> | <span data-ttu-id="09476-161">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="09476-161">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="09476-162">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="09476-162">Minimum supported server</span></span><br/> | <span data-ttu-id="09476-163">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="09476-163">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="09476-164">Namespace</span><span class="sxs-lookup"><span data-stu-id="09476-164">Namespace</span></span><br/>                | <span data-ttu-id="09476-165">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="09476-165">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="09476-166">MOF</span><span class="sxs-lookup"><span data-stu-id="09476-166">MOF</span></span><br/>                      | <dl> <span data-ttu-id="09476-167"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="09476-167"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="09476-168">DLL</span><span class="sxs-lookup"><span data-stu-id="09476-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="09476-169"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="09476-169"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

