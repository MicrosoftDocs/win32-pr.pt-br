---
description: Define as configurações para a migração de sistema virtual que é gerenciada por uma instância da \_ classe CIM VirtualSystemMigrationService.
ms.assetid: c28ed48b-bacc-49c8-9131-2543c0edb3fd
title: Classe CIM_VirtualSystemMigrationSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemMigrationSettingData
- CIM_VirtualSystemMigrationSettingData.MigrationType
- CIM_VirtualSystemMigrationSettingData.Priority
- CIM_VirtualSystemMigrationSettingData.Bandwidth
- CIM_VirtualSystemMigrationSettingData.BandwidthUnit
- CIM_VirtualSystemMigrationSettingData.OtherTransportType
- CIM_VirtualSystemMigrationSettingData.TransportType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0d33479d0148bc4004fbbbda216e508c276c7ee9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103662079"
---
# <a name="cim_virtualsystemmigrationsettingdata-class"></a><span data-ttu-id="d8e70-103">\_Classe CIM VirtualSystemMigrationSettingData</span><span class="sxs-lookup"><span data-stu-id="d8e70-103">CIM\_VirtualSystemMigrationSettingData class</span></span>

<span data-ttu-id="d8e70-104">Define as configurações para a migração de sistema virtual que é gerenciada por uma instância da classe [**CIM \_ VirtualSystemMigrationService**](cim-virtualsystemmigrationservice.md) .</span><span class="sxs-lookup"><span data-stu-id="d8e70-104">Defines the settings for virtual system migration that is managed by an instance of the [**CIM\_VirtualSystemMigrationService**](cim-virtualsystemmigrationservice.md) class.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8e70-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d8e70-105">Syntax</span></span>

``` syntax
[Experimental, Abstract, Version("2.20.0"), UMLPackagePath("CIM::System::Virtualization"), AMENDMENT]
class CIM_VirtualSystemMigrationSettingData : CIM_SettingData
{
  uint16 MigrationType;
  uint16 Priority;
  uint16 Bandwidth;
  string BandwidthUnit;
  string OtherTransportType;
  uint16 TransportType;
};
```

## <a name="members"></a><span data-ttu-id="d8e70-106">Membros</span><span class="sxs-lookup"><span data-stu-id="d8e70-106">Members</span></span>

<span data-ttu-id="d8e70-107">A classe **CIM \_ VirtualSystemMigrationSettingData** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="d8e70-107">The **CIM\_VirtualSystemMigrationSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="d8e70-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d8e70-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d8e70-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d8e70-109">Properties</span></span>

<span data-ttu-id="d8e70-110">A classe **CIM \_ VirtualSystemMigrationSettingData** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="d8e70-110">The **CIM\_VirtualSystemMigrationSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d8e70-111">**Largura de banda**</span><span class="sxs-lookup"><span data-stu-id="d8e70-111">**Bandwidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8e70-112">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d8e70-112">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d8e70-113">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d8e70-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8e70-114">Qualificadores: [**medidor**](/windows/desktop/WmiSdk/standard-qualifiers), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ VirtualSystemMigrationSettingData**.**BandwidthUnit**")</span><span class="sxs-lookup"><span data-stu-id="d8e70-114">Qualifiers: [**Gauge**](/windows/desktop/WmiSdk/standard-qualifiers), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_VirtualSystemMigrationSettingData**.**BandwidthUnit**")</span></span>
</dt> </dl>

<span data-ttu-id="d8e70-115">A largura de banda atribuída ou solicitada para uma operação de migração do sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="d8e70-115">The bandwidth assigned to or requested for a virtual system migration operation.</span></span> <span data-ttu-id="d8e70-116">"0" é a largura de banda padrão para solicitações de migração.</span><span class="sxs-lookup"><span data-stu-id="d8e70-116">"0" is default bandwidth for migration requests.</span></span>

<span data-ttu-id="d8e70-117">A **largura de banda** e as propriedades de **prioridade** podem ser usadas em conjunto.</span><span class="sxs-lookup"><span data-stu-id="d8e70-117">The **Bandwidth** and **Priority** properties may be used in conjunction.</span></span> <span data-ttu-id="d8e70-118">Os processos de migração que têm os valores de **prioridade** mais altos compartilham a largura de banda disponível com base na largura de banda solicitada.</span><span class="sxs-lookup"><span data-stu-id="d8e70-118">Migration processes that have the highest equal **Priority** values share the available bandwidth based on their requested bandwidth.</span></span> <span data-ttu-id="d8e70-119">Se nem toda a largura de banda for consumida por esse conjunto de processos, os processos de migração com os próximos valores de **prioridade** mais baixos compartilharão a largura de banda restante.</span><span class="sxs-lookup"><span data-stu-id="d8e70-119">If not all bandwidth is consumed by this set of processes, migration processes with the next lower equal **Priority** values share the remaining bandwidth.</span></span> <span data-ttu-id="d8e70-120">Se ainda houver mais largura de banda, os processos de migração com os próximos valores de **prioridade** menor menores serão considerados.</span><span class="sxs-lookup"><span data-stu-id="d8e70-120">If more bandwidth remains, migration processes with the next lower equal **Priority** values are considered.</span></span>

<span data-ttu-id="d8e70-121">A unidade usada na propriedade **Bandwidth** é especificada pelo valor da propriedade **BandwidthUnit** .</span><span class="sxs-lookup"><span data-stu-id="d8e70-121">The unit used in **Bandwidth** property is specified by the value of the **BandwidthUnit** property.</span></span>

<span data-ttu-id="d8e70-122">Se o valor da propriedade **BandwidthUnit** for "percent", as seguintes regras se aplicarão:</span><span class="sxs-lookup"><span data-stu-id="d8e70-122">If the value of the **BandwidthUnit** property is "percent", the following rules apply:</span></span>

-   <span data-ttu-id="d8e70-123">O valor da propriedade **Bandwidth** deve estar entre "0" e "100", com valores mais altos indicando uma largura de banda maior.</span><span class="sxs-lookup"><span data-stu-id="d8e70-123">The value of the **Bandwidth** property must be between "0" and "100", with higher values indicating a higher bandwidth.</span></span>
-   <span data-ttu-id="d8e70-124">Um valor de "100" indica toda a largura de banda disponível para executar operações de migração de sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="d8e70-124">A value of "100" indicates all available bandwidth for performing virtual system migration operations.</span></span>
-   <span data-ttu-id="d8e70-125">Os valores entre "1" e "100" se correlacionam linearmente com o intervalo de largura de banda disponível.</span><span class="sxs-lookup"><span data-stu-id="d8e70-125">Values between "1" and "100" linearly correlate with the available bandwidth range.</span></span> <span data-ttu-id="d8e70-126">Por exemplo, um valor de 50 solicita metade da largura de banda disponível.</span><span class="sxs-lookup"><span data-stu-id="d8e70-126">For example, a value of 50 requests half of the available bandwidth.</span></span>

</dd> <dt>

<span data-ttu-id="d8e70-127">**BandwidthUnit**</span><span class="sxs-lookup"><span data-stu-id="d8e70-127">**BandwidthUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8e70-128">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d8e70-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8e70-129">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d8e70-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8e70-130">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ VirtualSystemMigrationSettingData**.**Largura de banda**"), **IsPUnit**</span><span class="sxs-lookup"><span data-stu-id="d8e70-130">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_VirtualSystemMigrationSettingData**.**Bandwidth**"), **IsPUnit**</span></span>
</dt> </dl>

<span data-ttu-id="d8e70-131">A unidade usada pela propriedade **Bandwidth** .</span><span class="sxs-lookup"><span data-stu-id="d8e70-131">The unit used by the **Bandwidth** property.</span></span> <span data-ttu-id="d8e70-132">O valor dessa propriedade deve ser um valor válido do qualificador de unidades programáticas definido no Apêndice C. 1 de DSP0004 V 2.4 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="d8e70-132">The value of this property should be a legal value of the Programmatic Units qualifier defined in Appendix C.1 of DSP0004 V2.4 or later.</span></span>

> [!Note]  
> <span data-ttu-id="d8e70-133">Perfis como o DMTF DSP1081 definem como os clientes podem descobrir o conjunto de unidades com suporte em uma implementação, e intervalos e incrementos para valores da propriedade **Bandwidth** .</span><span class="sxs-lookup"><span data-stu-id="d8e70-133">Profiles such as DMTF DSP1081 define how clients can discover the set of units supported by an implementation, and ranges and increments for values of the **Bandwidth** property.</span></span>

 

</dd> <dt>

<span data-ttu-id="d8e70-134">**MigrationType**</span><span class="sxs-lookup"><span data-stu-id="d8e70-134">**MigrationType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8e70-135">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d8e70-135">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d8e70-136">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d8e70-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d8e70-137">O tipo de operação de migração a ser executada.</span><span class="sxs-lookup"><span data-stu-id="d8e70-137">The type of migration operation to perform.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d8e70-138">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="d8e70-138">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="d8e70-139">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="d8e70-139">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Live"></span><span id="live"></span><span id="LIVE"></span>

<span data-ttu-id="d8e70-140">**Ao vivo** (2)</span><span class="sxs-lookup"><span data-stu-id="d8e70-140">**Live** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Resume"></span><span id="resume"></span><span id="RESUME"></span>

<span data-ttu-id="d8e70-141">**Retomar** (3)</span><span class="sxs-lookup"><span data-stu-id="d8e70-141">**Resume** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Restart"></span><span id="restart"></span><span id="RESTART"></span>

<span data-ttu-id="d8e70-142">**Reiniciar** (4)</span><span class="sxs-lookup"><span data-stu-id="d8e70-142">**Restart** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d8e70-143">**OtherTransportType**</span><span class="sxs-lookup"><span data-stu-id="d8e70-143">**OtherTransportType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8e70-144">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d8e70-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8e70-145">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d8e70-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8e70-146">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ VirtualSystemMigrationSettingData**.**TransportType**")</span><span class="sxs-lookup"><span data-stu-id="d8e70-146">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_VirtualSystemMigrationSettingData**.**TransportType**")</span></span>
</dt> </dl>

<span data-ttu-id="d8e70-147">O tipo de transporte a ser aplicado se o valor de **TransportType** for "1" (outro).</span><span class="sxs-lookup"><span data-stu-id="d8e70-147">The type of transport to apply if the value of **TransportType** is "1" (other).</span></span>

</dd> <dt>

<span data-ttu-id="d8e70-148">**Prioridade**</span><span class="sxs-lookup"><span data-stu-id="d8e70-148">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8e70-149">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d8e70-149">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d8e70-150">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d8e70-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d8e70-151">A importância da migração relativa que a implementação da migração do sistema virtual pode usar para ordenar ou atribuir preferência entre várias solicitações de migração pendentes.</span><span class="sxs-lookup"><span data-stu-id="d8e70-151">The relative migration importance that the virtual system migration implementation may use to order or assign preference among multiple pending migration requests.</span></span> <span data-ttu-id="d8e70-152">Quanto menor o valor, maior a prioridade.</span><span class="sxs-lookup"><span data-stu-id="d8e70-152">The lower the value, the higher the priority.</span></span> <span data-ttu-id="d8e70-153">"0" é a largura de banda padrão para solicitações de migração.</span><span class="sxs-lookup"><span data-stu-id="d8e70-153">"0" is default bandwidth for migration requests.</span></span>

</dd> <dt>

<span data-ttu-id="d8e70-154">**TransportType**</span><span class="sxs-lookup"><span data-stu-id="d8e70-154">**TransportType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8e70-155">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d8e70-155">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d8e70-156">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d8e70-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8e70-157">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ VirtualSystemMigrationSettingData**.**OtherTransportType**")</span><span class="sxs-lookup"><span data-stu-id="d8e70-157">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_VirtualSystemMigrationSettingData**.**OtherTransportType**")</span></span>
</dt> </dl>

<span data-ttu-id="d8e70-158">O tipo de transporte a ser aplicado a uma operação de migração de sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="d8e70-158">The type of transport to apply to a virtual system migration operation.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d8e70-159">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="d8e70-159">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="d8e70-160">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="d8e70-160">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="SSH"></span><span id="ssh"></span>

<span data-ttu-id="d8e70-161">**SSH** (2)</span><span class="sxs-lookup"><span data-stu-id="d8e70-161">**SSH** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="TLS"></span><span id="tls"></span>

<span data-ttu-id="d8e70-162">**TLS** (3)</span><span class="sxs-lookup"><span data-stu-id="d8e70-162">**TLS** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="TLS_Strict"></span><span id="tls_strict"></span><span id="TLS_STRICT"></span>

<span data-ttu-id="d8e70-163">**TLS estrito** (4)</span><span class="sxs-lookup"><span data-stu-id="d8e70-163">**TLS Strict** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="TCP"></span><span id="tcp"></span>

<span data-ttu-id="d8e70-164">**TCP** (5)</span><span class="sxs-lookup"><span data-stu-id="d8e70-164">**TCP** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="IPC"></span><span id="ipc"></span>

<span data-ttu-id="d8e70-165">**IPC** (6)</span><span class="sxs-lookup"><span data-stu-id="d8e70-165">**IPC** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="d8e70-166">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="d8e70-166">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="d8e70-167">**Fornecedor reservado** (32768..)</span><span class="sxs-lookup"><span data-stu-id="d8e70-167">**Vendor Reserved** (32768..)</span></span>


<span data-ttu-id="d8e70-168"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="d8e70-168"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="d8e70-169">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d8e70-169">Requirements</span></span>



| <span data-ttu-id="d8e70-170">Requisito</span><span class="sxs-lookup"><span data-stu-id="d8e70-170">Requirement</span></span> | <span data-ttu-id="d8e70-171">Valor</span><span class="sxs-lookup"><span data-stu-id="d8e70-171">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8e70-172">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d8e70-172">Minimum supported client</span></span><br/> | <span data-ttu-id="d8e70-173">Windows 8</span><span class="sxs-lookup"><span data-stu-id="d8e70-173">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="d8e70-174">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d8e70-174">Minimum supported server</span></span><br/> | <span data-ttu-id="d8e70-175">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d8e70-175">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="d8e70-176">Namespace</span><span class="sxs-lookup"><span data-stu-id="d8e70-176">Namespace</span></span><br/>                | <span data-ttu-id="d8e70-177">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="d8e70-177">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="d8e70-178">MOF</span><span class="sxs-lookup"><span data-stu-id="d8e70-178">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d8e70-179"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d8e70-179"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d8e70-180">DLL</span><span class="sxs-lookup"><span data-stu-id="d8e70-180">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d8e70-181"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d8e70-181"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d8e70-182">Confira também</span><span class="sxs-lookup"><span data-stu-id="d8e70-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8e70-183">**CIM \_ SettingData**</span><span class="sxs-lookup"><span data-stu-id="d8e70-183">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> </dl>

 

