---
description: Representa a rede na qual o serviço de migração de sistema virtual está escutando a migração de sistema virtual de entrada.
ms.assetid: 24458602-ff5c-45c2-8053-00315b59d3bb
title: Classe Msvm_VirtualSystemMigrationNetworkSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationNetworkSettingData
- Msvm_VirtualSystemMigrationNetworkSettingData.InstanceID
- Msvm_VirtualSystemMigrationNetworkSettingData.Caption
- Msvm_VirtualSystemMigrationNetworkSettingData.Description
- Msvm_VirtualSystemMigrationNetworkSettingData.ElementName
- Msvm_VirtualSystemMigrationNetworkSettingData.SubnetNumber
- Msvm_VirtualSystemMigrationNetworkSettingData.PrefixLength
- Msvm_VirtualSystemMigrationNetworkSettingData.Metric
- Msvm_VirtualSystemMigrationNetworkSettingData.Tags
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 4f7c24bb754148fa8ede12292f308164512af646
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826859"
---
# <a name="msvm_virtualsystemmigrationnetworksettingdata-class"></a><span data-ttu-id="dcdba-103">\_Classe Msvm VirtualSystemMigrationNetworkSettingData</span><span class="sxs-lookup"><span data-stu-id="dcdba-103">Msvm\_VirtualSystemMigrationNetworkSettingData class</span></span>

<span data-ttu-id="dcdba-104">Representa a rede na qual o serviço de migração de sistema virtual está escutando a migração de sistema virtual de entrada.</span><span class="sxs-lookup"><span data-stu-id="dcdba-104">Represents the network on which the virtual system migration service is listening for incoming virtual system migration.</span></span>

<span data-ttu-id="dcdba-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="dcdba-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="dcdba-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dcdba-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemMigrationNetworkSettingData : CIM_SettingData
{
  string InstanceID;
  string Caption;
  string Description;
  string ElementName;
  string SubnetNumber;
  uint8  PrefixLength;
  uint32 Metric;
  string Tags[];
};
```

## <a name="members"></a><span data-ttu-id="dcdba-107">Membros</span><span class="sxs-lookup"><span data-stu-id="dcdba-107">Members</span></span>

<span data-ttu-id="dcdba-108">A classe **Msvm \_ VirtualSystemMigrationNetworkSettingData** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="dcdba-108">The **Msvm\_VirtualSystemMigrationNetworkSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="dcdba-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="dcdba-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="dcdba-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="dcdba-110">Properties</span></span>

<span data-ttu-id="dcdba-111">A classe **Msvm \_ VirtualSystemMigrationNetworkSettingData** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="dcdba-111">The **Msvm\_VirtualSystemMigrationNetworkSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="dcdba-112">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="dcdba-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dcdba-113">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="dcdba-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dcdba-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dcdba-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dcdba-115">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="dcdba-115">A short description of the object.</span></span> <span data-ttu-id="dcdba-116">Essa propriedade é herdada da classe [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) .</span><span class="sxs-lookup"><span data-stu-id="dcdba-116">This property is inherited from the [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) class.</span></span>

</dd> <dt>

<span data-ttu-id="dcdba-117">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="dcdba-117">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dcdba-118">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="dcdba-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dcdba-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dcdba-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dcdba-120">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="dcdba-120">A description of the object.</span></span> <span data-ttu-id="dcdba-121">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="dcdba-121">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="dcdba-122">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="dcdba-122">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dcdba-123">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="dcdba-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dcdba-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dcdba-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dcdba-125">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="dcdba-125">A display name for the object.</span></span> <span data-ttu-id="dcdba-126">Essa propriedade é herdada do [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="dcdba-126">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="dcdba-127">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="dcdba-127">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dcdba-128">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="dcdba-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dcdba-129">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dcdba-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dcdba-130">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="dcdba-130">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="dcdba-131">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="dcdba-131">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="dcdba-132">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="dcdba-132">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="dcdba-133">**Métrica**</span><span class="sxs-lookup"><span data-stu-id="dcdba-133">**Metric**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dcdba-134">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dcdba-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dcdba-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dcdba-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dcdba-136">A métrica de prioridade desta rede para migração.</span><span class="sxs-lookup"><span data-stu-id="dcdba-136">The priority metric of this network for migration.</span></span> <span data-ttu-id="dcdba-137">Os valores mais baixos são maiores em prioridade.</span><span class="sxs-lookup"><span data-stu-id="dcdba-137">Lower values are higher in priority.</span></span>

</dd> <dt>

<span data-ttu-id="dcdba-138">**PrefixLength**</span><span class="sxs-lookup"><span data-stu-id="dcdba-138">**PrefixLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dcdba-139">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="dcdba-139">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="dcdba-140">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dcdba-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dcdba-141">O comprimento do prefixo da sub-rede da rede de migração.</span><span class="sxs-lookup"><span data-stu-id="dcdba-141">The migration network subnet prefix length.</span></span>

</dd> <dt>

<span data-ttu-id="dcdba-142">**SubnetNumber**</span><span class="sxs-lookup"><span data-stu-id="dcdba-142">**SubnetNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dcdba-143">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="dcdba-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dcdba-144">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dcdba-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dcdba-145">O número da sub-rede da rede de migração.</span><span class="sxs-lookup"><span data-stu-id="dcdba-145">The migration network subnet number.</span></span>

</dd> <dt>

<span data-ttu-id="dcdba-146">**Marcas**</span><span class="sxs-lookup"><span data-stu-id="dcdba-146">**Tags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dcdba-147">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="dcdba-147">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="dcdba-148">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dcdba-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dcdba-149">Uma matriz de marcas para representar qual sistema de gerenciamento definiu esta rede para o serviço de migração do sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="dcdba-149">An array of tags to represent which management system has set this network for virtual system migration service.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dcdba-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dcdba-150">Requirements</span></span>



| <span data-ttu-id="dcdba-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="dcdba-151">Requirement</span></span> | <span data-ttu-id="dcdba-152">Valor</span><span class="sxs-lookup"><span data-stu-id="dcdba-152">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dcdba-153">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dcdba-153">Minimum supported client</span></span><br/> | <span data-ttu-id="dcdba-154">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="dcdba-154">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="dcdba-155">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dcdba-155">Minimum supported server</span></span><br/> | <span data-ttu-id="dcdba-156">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="dcdba-156">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="dcdba-157">Namespace</span><span class="sxs-lookup"><span data-stu-id="dcdba-157">Namespace</span></span><br/>                | <span data-ttu-id="dcdba-158">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="dcdba-158">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="dcdba-159">MOF</span><span class="sxs-lookup"><span data-stu-id="dcdba-159">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dcdba-160"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dcdba-160"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="dcdba-161">DLL</span><span class="sxs-lookup"><span data-stu-id="dcdba-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dcdba-162"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="dcdba-162"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="dcdba-163">Confira também</span><span class="sxs-lookup"><span data-stu-id="dcdba-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dcdba-164">**CIM \_ SettingData**</span><span class="sxs-lookup"><span data-stu-id="dcdba-164">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> <dt>

[<span data-ttu-id="dcdba-165">**ModifyNetworkSettings**</span><span class="sxs-lookup"><span data-stu-id="dcdba-165">**ModifyNetworkSettings**</span></span>](modifynetworksettings-msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

