---
description: Representa as configurações de migração para migrar um sistema virtual e o armazenamento anexado a um sistema virtual.
ms.assetid: 2d632fe2-31ee-4e4d-b2a6-c1d1f3b4d624
title: Classe Msvm_VirtualSystemMigrationSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationSettingData
- Msvm_VirtualSystemMigrationSettingData.InstanceID
- Msvm_VirtualSystemMigrationSettingData.Caption
- Msvm_VirtualSystemMigrationSettingData.Description
- Msvm_VirtualSystemMigrationSettingData.ElementName
- Msvm_VirtualSystemMigrationSettingData.MigrationType
- Msvm_VirtualSystemMigrationSettingData.Priority
- Msvm_VirtualSystemMigrationSettingData.Bandwidth
- Msvm_VirtualSystemMigrationSettingData.BandwidthUnit
- Msvm_VirtualSystemMigrationSettingData.OtherTransportType
- Msvm_VirtualSystemMigrationSettingData.TransportType
- Msvm_VirtualSystemMigrationSettingData.RemoveSourceUnmanagedVhds
- Msvm_VirtualSystemMigrationSettingData.AvoidRemovingVHDs
- Msvm_VirtualSystemMigrationSettingData.CPUCappingMagnitude
- Msvm_VirtualSystemMigrationSettingData.CancelIfBlackoutThresholdExceeded
- Msvm_VirtualSystemMigrationSettingData.AllowOverwriteExistingFile
- Msvm_VirtualSystemMigrationSettingData.UnmanagedVhds
- Msvm_VirtualSystemMigrationSettingData.DestinationPlannedVirtualSystemId
- Msvm_VirtualSystemMigrationSettingData.DestinationIPAddressList
- Msvm_VirtualSystemMigrationSettingData.RetainVhdCopiesOnSource
- Msvm_VirtualSystemMigrationSettingData.EnableCompression
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 254884153b3f733691b1103a6eb57f204b5d1764
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826857"
---
# <a name="msvm_virtualsystemmigrationsettingdata-class"></a><span data-ttu-id="fa123-103">\_Classe Msvm VirtualSystemMigrationSettingData</span><span class="sxs-lookup"><span data-stu-id="fa123-103">Msvm\_VirtualSystemMigrationSettingData class</span></span>

<span data-ttu-id="fa123-104">Representa as configurações de migração para migrar um sistema virtual e o armazenamento anexado a um sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="fa123-104">Represents the migration settings for migrating a virtual system and the storage attached to a virtual system.</span></span>

<span data-ttu-id="fa123-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="fa123-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa123-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fa123-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemMigrationSettingData : CIM_VirtualSystemMigrationSettingData
{
  string  InstanceID;
  string  Caption = "Migration Setting Data";
  string  Description = "Virtual System Migration Setting Data";
  string  ElementName;
  uint16  MigrationType;
  uint16  Priority;
  uint16  Bandwidth;
  string  BandwidthUnit;
  string  OtherTransportType;
  uint16  TransportType;
  boolean RemoveSourceUnmanagedVhds;
  boolean AvoidRemovingVHDs;
  uint16  CPUCappingMagnitude;
  boolean CancelIfBlackoutThresholdExceeded;
  boolean AllowOverwriteExistingFile;
  string  UnmanagedVhds[];
  string  DestinationPlannedVirtualSystemId;
  string  DestinationIPAddressList[];
  boolean RetainVhdCopiesOnSource;
  boolean EnableCompression;
};
```

## <a name="members"></a><span data-ttu-id="fa123-107">Membros</span><span class="sxs-lookup"><span data-stu-id="fa123-107">Members</span></span>

<span data-ttu-id="fa123-108">A classe **Msvm \_ VirtualSystemMigrationSettingData** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="fa123-108">The **Msvm\_VirtualSystemMigrationSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="fa123-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="fa123-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fa123-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="fa123-110">Properties</span></span>

<span data-ttu-id="fa123-111">A classe **Msvm \_ VirtualSystemMigrationSettingData** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="fa123-111">The **Msvm\_VirtualSystemMigrationSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fa123-112">**AllowOverwriteExistingFile**</span><span class="sxs-lookup"><span data-stu-id="fa123-112">**AllowOverwriteExistingFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa123-113">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="fa123-113">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fa123-114">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="fa123-114">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="fa123-115">Permitir que a operação de migração de armazenamento substitua arquivos. vhdx existentes.</span><span class="sxs-lookup"><span data-stu-id="fa123-115">Allow the storage migration operation to overwrite existing .vhdx files.</span></span>

> [!Note]  
> <span data-ttu-id="fa123-116">Essa propriedade foi adicionada no Windows 10, versão 1703.</span><span class="sxs-lookup"><span data-stu-id="fa123-116">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="fa123-117">**AvoidRemovingVHDs**</span><span class="sxs-lookup"><span data-stu-id="fa123-117">**AvoidRemovingVHDs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa123-118">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="fa123-118">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fa123-119">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="fa123-119">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="fa123-120">Não remova nenhum VHDs durante a migração, ou seja, VHDs na origem em VHDs successand no destino em caso de falha.</span><span class="sxs-lookup"><span data-stu-id="fa123-120">Do not remove any VHDs during the migration, i.e. VHDs on the source in successand VHDs on the destination in failure.</span></span>

> [!Note]  
> <span data-ttu-id="fa123-121">Adicionado no Windows 10, versão 1703 e Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="fa123-121">Added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="fa123-122">**Largura de banda**</span><span class="sxs-lookup"><span data-stu-id="fa123-122">**Bandwidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa123-123">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fa123-123">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fa123-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fa123-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fa123-125">Especifica a largura de banda atribuída ou solicitada para uma operação de migração de sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="fa123-125">Specifies the bandwidth assigned to or requested for a virtual system migration operation.</span></span> <span data-ttu-id="fa123-126">As unidades de largura de banda são especificadas pela propriedade **BandwidthUnit** .</span><span class="sxs-lookup"><span data-stu-id="fa123-126">The bandwidth units are specified by the **BandwidthUnit** property.</span></span> <span data-ttu-id="fa123-127">Em uma migração, um valor de 0 indica a largura de banda padrão.</span><span class="sxs-lookup"><span data-stu-id="fa123-127">Within a migration, a value of 0 indicates the default bandwidth.</span></span> <span data-ttu-id="fa123-128">Caso contrário, um valor de 0 indica que não há suporte para larguras de banda.</span><span class="sxs-lookup"><span data-stu-id="fa123-128">Otherwise, a value of 0 indicates that bandwidths are not supported.</span></span>

<span data-ttu-id="fa123-129">A **largura de banda** e a **prioridade** podem ser usadas em conjunto.</span><span class="sxs-lookup"><span data-stu-id="fa123-129">**Bandwidth** and **Priority** can be used in conjunction.</span></span> <span data-ttu-id="fa123-130">Os processos de migração que têm o maior valor de prioridade igual compartilham a largura de banda disponível com base na largura de banda solicitada.</span><span class="sxs-lookup"><span data-stu-id="fa123-130">Migration processes that have the highest equal priority value share the available bandwidth based on their requested bandwidth.</span></span> <span data-ttu-id="fa123-131">Se nem toda a largura de banda for consumida por esse conjunto de processos, os processos de migração com a próxima prioridade inferior menor compartilharão a largura de banda restante.</span><span class="sxs-lookup"><span data-stu-id="fa123-131">If not all bandwidth is consumed by this set of processes, migration processes with the next lower equal priority share the remaining bandwidth.</span></span> <span data-ttu-id="fa123-132">Se ainda houver mais largura de banda restante, os processos de migração com a próxima prioridade menor inferior serão considerados e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="fa123-132">If still more bandwidth remains, migration processes with the next lower equal priority are considered, and so forth.</span></span>

<span data-ttu-id="fa123-133">Essa propriedade é herdada do **CIM \_ VirtualSystemMigrationSettingData**.</span><span class="sxs-lookup"><span data-stu-id="fa123-133">This property is inherited from **CIM\_VirtualSystemMigrationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="fa123-134">**BandwidthUnit**</span><span class="sxs-lookup"><span data-stu-id="fa123-134">**BandwidthUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa123-135">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="fa123-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fa123-136">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fa123-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fa123-137">Especifica as unidades usadas pela propriedade **Bandwidth** .</span><span class="sxs-lookup"><span data-stu-id="fa123-137">Specifies the units used by the **Bandwidth** property.</span></span> <span data-ttu-id="fa123-138">O valor dessa propriedade deve ser um valor válido do qualificador de unidades programáticas, conforme definido no Apêndice C. 1 de DSP0004 V 2.4 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="fa123-138">The value of this property must be a legal value of the Programmatic Units qualifier as defined in Appendix C.1 of DSP0004 V2.4 or later.</span></span>

<span data-ttu-id="fa123-139">Se o valor dessa propriedade for "percent", o valor da propriedade **Bandwidth** deverá estar entre 0 e 100, com valores mais altos indicando uma maior largura de banda.</span><span class="sxs-lookup"><span data-stu-id="fa123-139">If the value of this property is "percent", the value of the **Bandwidth** property must be between 0 and 100, with higher values indicating a higher bandwidth.</span></span> <span data-ttu-id="fa123-140">Um valor de 100 indica a largura de banda total disponível para executar operações de migração de sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="fa123-140">A value of 100 indicates the total available bandwidth for performing virtual system migration operations.</span></span> <span data-ttu-id="fa123-141">Os valores entre 1 e 100 devem correlacionar linearmente com o intervalo de largura de banda disponível.</span><span class="sxs-lookup"><span data-stu-id="fa123-141">Values between 1 and 100 should linearly correlate with the available bandwidth range.</span></span> <span data-ttu-id="fa123-142">Por exemplo, um valor de 50 deve solicitar metade da largura de banda disponível.</span><span class="sxs-lookup"><span data-stu-id="fa123-142">For example, a value of 50 should request half of the available bandwidth.</span></span>

<span data-ttu-id="fa123-143">Essa propriedade é herdada do **CIM \_ VirtualSystemMigrationSettingData**.</span><span class="sxs-lookup"><span data-stu-id="fa123-143">This property is inherited from **CIM\_VirtualSystemMigrationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="fa123-144">**CancelIfBlackoutThresholdExceeded**</span><span class="sxs-lookup"><span data-stu-id="fa123-144">**CancelIfBlackoutThresholdExceeded**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa123-145">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="fa123-145">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fa123-146">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="fa123-146">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="fa123-147">Cancelará a migração se o tempo limite de blecaute for excedido.</span><span class="sxs-lookup"><span data-stu-id="fa123-147">Cancels migration if the blackout threshold time is exceeded.</span></span>

> [!Note]  
> <span data-ttu-id="fa123-148">Adicionado no Windows 10, versão 1709.</span><span class="sxs-lookup"><span data-stu-id="fa123-148">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="fa123-149">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="fa123-149">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa123-150">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="fa123-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fa123-151">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fa123-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fa123-152">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="fa123-152">A short description of the object.</span></span> <span data-ttu-id="fa123-153">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="fa123-153">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="fa123-154">**CPUCappingMagnitude**</span><span class="sxs-lookup"><span data-stu-id="fa123-154">**CPUCappingMagnitude**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa123-155">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fa123-155">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fa123-156">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="fa123-156">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="fa123-157">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CPUCappingMagnitude")</span><span class="sxs-lookup"><span data-stu-id="fa123-157">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CPUCappingMagnitude")</span></span>
</dt> </dl>

<span data-ttu-id="fa123-158">Grau de limitação de CPU durante a migração.</span><span class="sxs-lookup"><span data-stu-id="fa123-158">Degree of CPU capping during migration.</span></span>

> [!Note]  
> <span data-ttu-id="fa123-159">Adicionado no Windows 10, versão 1709.</span><span class="sxs-lookup"><span data-stu-id="fa123-159">Added in Windows 10, version 1709.</span></span>

 

<dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span data-ttu-id="fa123-160">**Normal** (0)</span><span class="sxs-lookup"><span data-stu-id="fa123-160">**Normal** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>

<span data-ttu-id="fa123-161">**Baixo** (1)</span><span class="sxs-lookup"><span data-stu-id="fa123-161">**Low** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="High"></span><span id="high"></span><span id="HIGH"></span>

<span data-ttu-id="fa123-162">**Alta** (2)</span><span class="sxs-lookup"><span data-stu-id="fa123-162">**High** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="fa123-163">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="fa123-163">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa123-164">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="fa123-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fa123-165">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fa123-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fa123-166">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="fa123-166">A description of the object.</span></span> <span data-ttu-id="fa123-167">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="fa123-167">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="fa123-168">**DestinationIPAddressList**</span><span class="sxs-lookup"><span data-stu-id="fa123-168">**DestinationIPAddressList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa123-169">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="fa123-169">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="fa123-170">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="fa123-170">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="fa123-171">Isso será **nulo** para migração de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="fa123-171">This will be **Null** for storage migration.</span></span> <span data-ttu-id="fa123-172">Para a migração do sistema virtual, isso pode conter uma lista de endereços IP do host de destino.</span><span class="sxs-lookup"><span data-stu-id="fa123-172">For virtual system migration, this can contain a list of IP addresses of the destination host.</span></span>

</dd> <dt>

<span data-ttu-id="fa123-173">**DestinationPlannedVirtualSystemId**</span><span class="sxs-lookup"><span data-stu-id="fa123-173">**DestinationPlannedVirtualSystemId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa123-174">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="fa123-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fa123-175">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="fa123-175">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="fa123-176">Se uma máquina virtual planejada existir no destino de migração, essa propriedade será definida como o GUID da máquina virtual planejada de destino onde a máquina virtual precisa ser migrada.</span><span class="sxs-lookup"><span data-stu-id="fa123-176">If a planned virtual machine exists at the migration destination, this property will be set to the GUID of the destination planned virtual machine where the virtual machine needs to migrate.</span></span> <span data-ttu-id="fa123-177">Isso é útil para casos em que um usuário criou uma máquina virtual planejada no destino, juntamente com a configuração do recurso, e quer que uma máquina virtual da origem seja migrada para essa máquina virtual planejada.</span><span class="sxs-lookup"><span data-stu-id="fa123-177">This is useful for cases where a user has created a planned virtual machine at the destination, along with resource setup, and wants a virtual machine from the source to migrate into this planned virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="fa123-178">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="fa123-178">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa123-179">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="fa123-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fa123-180">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fa123-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fa123-181">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="fa123-181">A display name for the object.</span></span> <span data-ttu-id="fa123-182">Essa propriedade é herdada do [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="fa123-182">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="fa123-183">**EnableCompression**</span><span class="sxs-lookup"><span data-stu-id="fa123-183">**EnableCompression**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa123-184">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="fa123-184">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fa123-185">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="fa123-185">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="fa123-186">Indica se o tráfego de migração ao vivo deve ser compactado.</span><span class="sxs-lookup"><span data-stu-id="fa123-186">Indicates whether to compress the live migration traffic.</span></span> <span data-ttu-id="fa123-187">**Verdadeiro** indica compactar; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="fa123-187">**True** indicates to compress; otherwise **False**.</span></span>

<span data-ttu-id="fa123-188">**Windows 8.1:** Não há suporte para esse valor até Windows 8.1 e Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="fa123-188">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="fa123-189">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="fa123-189">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa123-190">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="fa123-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fa123-191">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fa123-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fa123-192">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="fa123-192">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="fa123-193">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="fa123-193">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="fa123-194">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="fa123-194">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="fa123-195">**MigrationType**</span><span class="sxs-lookup"><span data-stu-id="fa123-195">**MigrationType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa123-196">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fa123-196">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fa123-197">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="fa123-197">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="fa123-198">Qualificadores: [**substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("MigrationType")</span><span class="sxs-lookup"><span data-stu-id="fa123-198">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("MigrationType")</span></span>
</dt> </dl>

<span data-ttu-id="fa123-199">Especifica o tipo de operação de migração a ser executada.</span><span class="sxs-lookup"><span data-stu-id="fa123-199">Specifies the type of migration operation to be performed.</span></span> <span data-ttu-id="fa123-200">Essa propriedade é herdada do **CIM \_ VirtualSystemMigrationSettingData**.</span><span class="sxs-lookup"><span data-stu-id="fa123-200">This property is inherited from **CIM\_VirtualSystemMigrationSettingData**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="fa123-201"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="fa123-201"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="VirtualSystem"></span><span id="virtualsystem"></span><span id="VIRTUALSYSTEM"></span>

<span data-ttu-id="fa123-202"><span id="VirtualSystem"></span><span id="virtualsystem"></span><span id="VIRTUALSYSTEM"></span>**VirtualSystem** (32768)</span><span class="sxs-lookup"><span data-stu-id="fa123-202"><span id="VirtualSystem"></span><span id="virtualsystem"></span><span id="VIRTUALSYSTEM"></span>**VirtualSystem** (32768)</span></span>


</dt> <dd>

<span data-ttu-id="fa123-203">Migra o sistema virtual para o host de destino.</span><span class="sxs-lookup"><span data-stu-id="fa123-203">Migrates the virtual system to the destination host.</span></span>

</dd> <dt>

<span id="Storage"></span><span id="storage"></span><span id="STORAGE"></span>

<span data-ttu-id="fa123-204"><span id="Storage"></span><span id="storage"></span><span id="STORAGE"></span>**Armazenamento** (32769)</span><span class="sxs-lookup"><span data-stu-id="fa123-204"><span id="Storage"></span><span id="storage"></span><span id="STORAGE"></span>**Storage** (32769)</span></span>


</dt> <dd>

<span data-ttu-id="fa123-205">Migra somente os recursos de armazenamento do sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="fa123-205">Migrates only the storage resources of the virtual system.</span></span>

</dd> <dt>

<span id="Staged"></span><span id="staged"></span><span id="STAGED"></span>

<span data-ttu-id="fa123-206"><span id="Staged"></span><span id="staged"></span><span id="STAGED"></span>**Preparado** (32770)</span><span class="sxs-lookup"><span data-stu-id="fa123-206"><span id="Staged"></span><span id="staged"></span><span id="STAGED"></span>**Staged** (32770)</span></span>


</dt> <dd>

<span data-ttu-id="fa123-207">Usando a configuração do sistema virtual, o cria um sistema virtual planejado no host de destino.</span><span class="sxs-lookup"><span data-stu-id="fa123-207">Using the virtual system configuration, creates a planned virtual system at the destination host.</span></span>

</dd> <dt>

<span id="VirtualSystemAndStorage"></span><span id="virtualsystemandstorage"></span><span id="VIRTUALSYSTEMANDSTORAGE"></span>

<span data-ttu-id="fa123-208"><span id="VirtualSystemAndStorage"></span><span id="virtualsystemandstorage"></span><span id="VIRTUALSYSTEMANDSTORAGE"></span>**VirtualSystemAndStorage** (32771)</span><span class="sxs-lookup"><span data-stu-id="fa123-208"><span id="VirtualSystemAndStorage"></span><span id="virtualsystemandstorage"></span><span id="VIRTUALSYSTEMANDSTORAGE"></span>**VirtualSystemAndStorage** (32771)</span></span>


</dt> <dd>

<span data-ttu-id="fa123-209">Migra o sistema virtual e seu armazenamento para o host de destino.</span><span class="sxs-lookup"><span data-stu-id="fa123-209">Migrates the virtual system and its storage to the destination host.</span></span>

</dd> <dt>

<span id="StorageDeepCheck"></span><span id="storagedeepcheck"></span><span id="STORAGEDEEPCHECK"></span>

<span data-ttu-id="fa123-210"><span id="StorageDeepCheck"></span><span id="storagedeepcheck"></span><span id="STORAGEDEEPCHECK"></span>**StorageDeepCheck** (32772)</span><span class="sxs-lookup"><span data-stu-id="fa123-210"><span id="StorageDeepCheck"></span><span id="storagedeepcheck"></span><span id="STORAGEDEEPCHECK"></span>**StorageDeepCheck** (32772)</span></span>


</dt> <dd>

<span data-ttu-id="fa123-211">Executa uma verificação de capacidade de migração de recursos de armazenamento de sistema virtual no host de destino.</span><span class="sxs-lookup"><span data-stu-id="fa123-211">Performs a virtual system storage resource migration ability check at the destination host.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="fa123-212">**OtherTransportType**</span><span class="sxs-lookup"><span data-stu-id="fa123-212">**OtherTransportType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa123-213">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="fa123-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fa123-214">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fa123-214">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fa123-215">Especifica o tipo de transporte a ser aplicado se o valor de **TransportType** for 1 (outro).</span><span class="sxs-lookup"><span data-stu-id="fa123-215">Specifies the type of transport to be applied if the value of **TransportType** is 1 (Other).</span></span> <span data-ttu-id="fa123-216">Essa propriedade é herdada do **CIM \_ VirtualSystemMigrationSettingData**.</span><span class="sxs-lookup"><span data-stu-id="fa123-216">This property is inherited from **CIM\_VirtualSystemMigrationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="fa123-217">**Prioridade**</span><span class="sxs-lookup"><span data-stu-id="fa123-217">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa123-218">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fa123-218">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fa123-219">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fa123-219">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fa123-220">Especifica uma importância de migração relativa, que o sistema de migração pode usar para ordenar ou, de outra forma, dar preferência entre várias solicitações de migração pendentes.</span><span class="sxs-lookup"><span data-stu-id="fa123-220">Specifies a relative migration importance, which the migration system may use to order or otherwise give preference among multiple pending migration requests.</span></span> <span data-ttu-id="fa123-221">Quanto menor o valor, maior a prioridade.</span><span class="sxs-lookup"><span data-stu-id="fa123-221">The lower the value, the higher the priority.</span></span> <span data-ttu-id="fa123-222">Em uma migração, um valor de 0 indica a prioridade padrão.</span><span class="sxs-lookup"><span data-stu-id="fa123-222">Within a migration, a value of 0 indicates the default priority.</span></span> <span data-ttu-id="fa123-223">Caso contrário, um valor de 0 indica que não há suporte para as prioridades.</span><span class="sxs-lookup"><span data-stu-id="fa123-223">Otherwise, a value of 0 indicates that priorities are not supported.</span></span>

<span data-ttu-id="fa123-224">Essa propriedade é herdada do **CIM \_ VirtualSystemMigrationSettingData**.</span><span class="sxs-lookup"><span data-stu-id="fa123-224">This property is inherited from **CIM\_VirtualSystemMigrationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="fa123-225">**RemoveSourceUnmanagedVhds**</span><span class="sxs-lookup"><span data-stu-id="fa123-225">**RemoveSourceUnmanagedVhds**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa123-226">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="fa123-226">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fa123-227">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="fa123-227">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="fa123-228">Remover VHDs não gerenciados de origem.</span><span class="sxs-lookup"><span data-stu-id="fa123-228">Remove source unmanaged VHDs.</span></span>

> [!Note]  
> <span data-ttu-id="fa123-229">Adicionado ao Windows 10 e ao Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="fa123-229">Added in Windows 10 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="fa123-230">**RetainVhdCopiesOnSource**</span><span class="sxs-lookup"><span data-stu-id="fa123-230">**RetainVhdCopiesOnSource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa123-231">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="fa123-231">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fa123-232">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="fa123-232">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="fa123-233">Para uma migração de armazenamento, isso especifica se os VHDs somente leitura no host de origem devem ser removidos após a conclusão da migração.</span><span class="sxs-lookup"><span data-stu-id="fa123-233">For a storage migration, this specifies whether the read-only VHDs on the source host should be removed after the migration is completed.</span></span>

</dd> <dt>

<span data-ttu-id="fa123-234">**TransportType**</span><span class="sxs-lookup"><span data-stu-id="fa123-234">**TransportType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa123-235">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fa123-235">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fa123-236">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="fa123-236">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="fa123-237">Qualificadores: [**substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("TransportType")</span><span class="sxs-lookup"><span data-stu-id="fa123-237">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("TransportType")</span></span>
</dt> </dl>

<span data-ttu-id="fa123-238">Especifica o tipo de transporte a ser aplicado a uma operação de migração de sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="fa123-238">Specifies the type of transport to be applied for a virtual system migration operation.</span></span> <span data-ttu-id="fa123-239">Essa propriedade é herdada do **CIM \_ VirtualSystemMigrationSettingData**.</span><span class="sxs-lookup"><span data-stu-id="fa123-239">This property is inherited from **CIM\_VirtualSystemMigrationSettingData**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="fa123-240">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="fa123-240">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="fa123-241">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="fa123-241">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="SSH"></span><span id="ssh"></span>

<span data-ttu-id="fa123-242">**SSH** (2)</span><span class="sxs-lookup"><span data-stu-id="fa123-242">**SSH** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="TLS"></span><span id="tls"></span>

<span data-ttu-id="fa123-243">**TLS** (3)</span><span class="sxs-lookup"><span data-stu-id="fa123-243">**TLS** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="TLS_Strict"></span><span id="tls_strict"></span><span id="TLS_STRICT"></span>

<span data-ttu-id="fa123-244">**TLS estrito** (4)</span><span class="sxs-lookup"><span data-stu-id="fa123-244">**TLS Strict** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="TCP"></span><span id="tcp"></span>

<span data-ttu-id="fa123-245">**TCP** (5)</span><span class="sxs-lookup"><span data-stu-id="fa123-245">**TCP** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="IPC"></span><span id="ipc"></span>

<span data-ttu-id="fa123-246">**IPC** (6)</span><span class="sxs-lookup"><span data-stu-id="fa123-246">**IPC** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="fa123-247">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="fa123-247">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="fa123-248">**Fornecedor reservado** (32768..)</span><span class="sxs-lookup"><span data-stu-id="fa123-248">**Vendor Reserved** (32768..)</span></span>


<span data-ttu-id="fa123-249"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="fa123-249"></dt> <dd></dd> </dl></span></span>

<span data-ttu-id="fa123-250">Para a migração dinâmica, essa propriedade especifica o tipo de transporte a ser usado para transferir o estado do sistema virtual para o host de destino.</span><span class="sxs-lookup"><span data-stu-id="fa123-250">For live migration, this property specifies the transport type to be used for transferring virtual system state to the destination host.</span></span> <span data-ttu-id="fa123-251">Os valores com suporte são:</span><span class="sxs-lookup"><span data-stu-id="fa123-251">The supported values are:</span></span>

<dt>

<span id="TCP"></span><span id="tcp"></span>

<span data-ttu-id="fa123-252"><span id="TCP"></span><span id="tcp"></span>**TCP** (5)</span><span class="sxs-lookup"><span data-stu-id="fa123-252"><span id="TCP"></span><span id="tcp"></span>**TCP** (5)</span></span>


</dt> <dd>

<span data-ttu-id="fa123-253">Indica o tipo de transporte TCP.</span><span class="sxs-lookup"><span data-stu-id="fa123-253">Indicates the TCP transport type.</span></span>

</dd> <dt>

<span id="SMB"></span><span id="smb"></span>

<span data-ttu-id="fa123-254"><span id="SMB"></span><span id="smb"></span>**SMB** (32768)</span><span class="sxs-lookup"><span data-stu-id="fa123-254"><span id="SMB"></span><span id="smb"></span>**SMB** (32768)</span></span>


</dt> <dd>

<span data-ttu-id="fa123-255">Indica que o tipo de transporte para transferência do estado da máquina virtual é SMB.</span><span class="sxs-lookup"><span data-stu-id="fa123-255">Indicates the transport type for transferring the virtual machine state is SMB.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="fa123-256">**UnmanagedVhds**</span><span class="sxs-lookup"><span data-stu-id="fa123-256">**UnmanagedVhds**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa123-257">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="fa123-257">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="fa123-258">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="fa123-258">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="fa123-259">Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), **HyperVEmbeddedInstance** ("Msvm \_ MoveUnmanagedVhd")</span><span class="sxs-lookup"><span data-stu-id="fa123-259">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), **HyperVEmbeddedInstance** ("Msvm\_MoveUnmanagedVhd")</span></span>
</dt> </dl>

<span data-ttu-id="fa123-260">Uma matriz de instâncias [**Msvm \_ MoveUnmanagedVhd**](msvm-moveunmanagedvhd.md) inseridas que contêm informações de VHDs não gerenciados.</span><span class="sxs-lookup"><span data-stu-id="fa123-260">An array of embedded [**Msvm\_MoveUnmanagedVhd**](msvm-moveunmanagedvhd.md) instances which contain unmanaged VHDs information.</span></span>

> [!Note]  
> <span data-ttu-id="fa123-261">Adicionado ao Windows 10 e ao Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="fa123-261">Added in Windows 10 and Windows Server 2016.</span></span>

 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fa123-262">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fa123-262">Requirements</span></span>



| <span data-ttu-id="fa123-263">Requisito</span><span class="sxs-lookup"><span data-stu-id="fa123-263">Requirement</span></span> | <span data-ttu-id="fa123-264">Valor</span><span class="sxs-lookup"><span data-stu-id="fa123-264">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa123-265">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fa123-265">Minimum supported client</span></span><br/> | <span data-ttu-id="fa123-266">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="fa123-266">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="fa123-267">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fa123-267">Minimum supported server</span></span><br/> | <span data-ttu-id="fa123-268">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="fa123-268">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fa123-269">Namespace</span><span class="sxs-lookup"><span data-stu-id="fa123-269">Namespace</span></span><br/>                | <span data-ttu-id="fa123-270">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="fa123-270">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="fa123-271">MOF</span><span class="sxs-lookup"><span data-stu-id="fa123-271">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fa123-272"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fa123-272"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="fa123-273">DLL</span><span class="sxs-lookup"><span data-stu-id="fa123-273">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fa123-274"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="fa123-274"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="fa123-275">Confira também</span><span class="sxs-lookup"><span data-stu-id="fa123-275">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa123-276">**\_VIRTUALSYSTEMMIGRATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="fa123-276">**CIM\_VirtualSystemMigrationSettingData**</span></span>](cim-virtualsystemmigrationsettingdata.md)
</dt> <dt>

[<span data-ttu-id="fa123-277">**MigrateVirtualSystemToHost**</span><span class="sxs-lookup"><span data-stu-id="fa123-277">**MigrateVirtualSystemToHost**</span></span>](migratevirtualsystemtohost-msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

