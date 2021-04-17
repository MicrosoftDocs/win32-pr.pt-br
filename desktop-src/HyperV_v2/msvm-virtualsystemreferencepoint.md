---
description: Representa um ponto de referência para um sistema virtual.
ms.assetid: b3ba4fa7-3b77-4a1d-ab8f-d38af12ab5dd
title: Classe Msvm_VirtualSystemReferencePoint
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePoint
- Msvm_VirtualSystemReferencePoint.InstanceID
- Msvm_VirtualSystemReferencePoint.ReferencePointType
- Msvm_VirtualSystemReferencePoint.ConsistencyLevel
- Msvm_VirtualSystemReferencePoint.VirtualSystemIdentifier
- Msvm_VirtualSystemReferencePoint.HasAssociatedData
- Msvm_VirtualSystemReferencePoint.VirtualDiskIdentifiers
- Msvm_VirtualSystemReferencePoint.ResilientChangeTrackingIdentifiers
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: add160cf44a592462634704ddf783cd8f4084068
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105755991"
---
# <a name="msvm_virtualsystemreferencepoint-class"></a><span data-ttu-id="c88db-103">\_Classe Msvm VirtualSystemReferencePoint</span><span class="sxs-lookup"><span data-stu-id="c88db-103">Msvm\_VirtualSystemReferencePoint class</span></span>

<span data-ttu-id="c88db-104">Representa um ponto de referência para um sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="c88db-104">Represents a reference point for a virtual system.</span></span>

<span data-ttu-id="c88db-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="c88db-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c88db-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c88db-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemReferencePoint : CIM_ManagedElement
{
  string  InstanceID;
  uint16  ReferencePointType;
  uint16  ConsistencyLevel;
  string  VirtualSystemIdentifier;
  boolean HasAssociatedData;
  string  VirtualDiskIdentifiers[];
  string  ResilientChangeTrackingIdentifiers[];
};
```

## <a name="members"></a><span data-ttu-id="c88db-107">Membros</span><span class="sxs-lookup"><span data-stu-id="c88db-107">Members</span></span>

<span data-ttu-id="c88db-108">A classe **Msvm \_ VirtualSystemReferencePoint** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="c88db-108">The **Msvm\_VirtualSystemReferencePoint** class has these types of members:</span></span>

-   [<span data-ttu-id="c88db-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c88db-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c88db-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c88db-110">Properties</span></span>

<span data-ttu-id="c88db-111">A classe **Msvm \_ VirtualSystemReferencePoint** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="c88db-111">The **Msvm\_VirtualSystemReferencePoint** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c88db-112">**ConsistencyLevel**</span><span class="sxs-lookup"><span data-stu-id="c88db-112">**ConsistencyLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c88db-113">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c88db-113">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c88db-114">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="c88db-114">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="c88db-115">O nível de consistência do ponto de referência.</span><span class="sxs-lookup"><span data-stu-id="c88db-115">The consistency level of the reference point.</span></span>

<dt>

<span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>

<span data-ttu-id="c88db-116"><span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>**Consistente** com o aplicativo (1)</span><span class="sxs-lookup"><span data-stu-id="c88db-116"><span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>**Application Consistent** (1)</span></span>


</dt> <dd>

<span data-ttu-id="c88db-117">O ponto de referência indica um ponto no tempo em que o sistema virtual estava no estado consistente do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c88db-117">The reference point indicates a point in time when the virtual system was in application consistent state.</span></span>

</dd> <dt>

<span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>

<span data-ttu-id="c88db-118"><span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>**Falha consistente** (2)</span><span class="sxs-lookup"><span data-stu-id="c88db-118"><span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>**Crash Consistent** (2)</span></span>


</dt> <dd>

<span data-ttu-id="c88db-119">O ponto de referência indica um ponto no tempo em que o sistema virtual estava em estado de falha consistente.</span><span class="sxs-lookup"><span data-stu-id="c88db-119">The reference point indicates a point in time when the virtual system was in crash consistent state.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c88db-120">**HasAssociatedData**</span><span class="sxs-lookup"><span data-stu-id="c88db-120">**HasAssociatedData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c88db-121">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="c88db-121">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c88db-122">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="c88db-122">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="c88db-123">Defina como **true** se o ponto de referência tiver dados associados.</span><span class="sxs-lookup"><span data-stu-id="c88db-123">Set to **true** if the reference point has associated data.</span></span> <span data-ttu-id="c88db-124">Isso é válido somente para pontos de referência baseados em log.</span><span class="sxs-lookup"><span data-stu-id="c88db-124">This is valid only for log based reference points.</span></span> <span data-ttu-id="c88db-125">Para pontos de referência baseados em RCT, **HasAssociatedData** é definido como **false**.</span><span class="sxs-lookup"><span data-stu-id="c88db-125">For RCT-based reference points, **HasAssociatedData** is set to **false**.</span></span> <span data-ttu-id="c88db-126">Para pontos de referência baseados em log, uma vez que o log é Descartado, o **HasAssociatedData** se torna **falso**.</span><span class="sxs-lookup"><span data-stu-id="c88db-126">For log based reference points, once the log is discarded **HasAssociatedData** becomes **false**.</span></span>

</dd> <dt>

<span data-ttu-id="c88db-127">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="c88db-127">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c88db-128">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c88db-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c88db-129">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c88db-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c88db-130">Qualificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceId"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="c88db-130">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceID"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="c88db-131">Identificação exclusiva de um objeto de ponto de referência.</span><span class="sxs-lookup"><span data-stu-id="c88db-131">Unique identification of a reference point object.</span></span>

</dd> <dt>

<span data-ttu-id="c88db-132">**ReferencePointType**</span><span class="sxs-lookup"><span data-stu-id="c88db-132">**ReferencePointType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c88db-133">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c88db-133">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c88db-134">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="c88db-134">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="c88db-135">Indica o tipo do ponto de referência.</span><span class="sxs-lookup"><span data-stu-id="c88db-135">Indicates the type of the reference point.</span></span>

<dt>

<span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>

<span data-ttu-id="c88db-136"><span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>**Baseado em log** (1)</span><span class="sxs-lookup"><span data-stu-id="c88db-136"><span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>**Log based** (1)</span></span>


</dt> <dd>

<span data-ttu-id="c88db-137">Rastreamento de log de réplica do Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="c88db-137">Hyper-V replica log tracking.</span></span>

</dd> <dt>

<span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>

<span data-ttu-id="c88db-138"><span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>**Baseado em RCT** (2)</span><span class="sxs-lookup"><span data-stu-id="c88db-138"><span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>**RCT based** (2)</span></span>


</dt> <dd>

<span data-ttu-id="c88db-139">Com base em Controle de Alterações resilientes de discos virtuais.</span><span class="sxs-lookup"><span data-stu-id="c88db-139">Based on Resilient Change Tracking of virtual disks.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c88db-140">**ResilientChangeTrackingIdentifiers**</span><span class="sxs-lookup"><span data-stu-id="c88db-140">**ResilientChangeTrackingIdentifiers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c88db-141">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c88db-141">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c88db-142">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c88db-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c88db-143">Uma matriz de IDs de RCT correspondente aos discos virtuais da VM no momento em que esse ponto de referência foi criado.</span><span class="sxs-lookup"><span data-stu-id="c88db-143">An array of RCT IDs corresponding to the virtual disks of the VM at the time this reference point was created.</span></span> <span data-ttu-id="c88db-144">Este campo é válido somente para pontos de referência baseados em RCT.</span><span class="sxs-lookup"><span data-stu-id="c88db-144">This field is valid only for RCT-based reference points.</span></span>

</dd> <dt>

<span data-ttu-id="c88db-145">**VirtualDiskIdentifiers**</span><span class="sxs-lookup"><span data-stu-id="c88db-145">**VirtualDiskIdentifiers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c88db-146">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c88db-146">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c88db-147">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c88db-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c88db-148">Uma matriz de IDs de instância do WMI correspondente aos discos virtuais da VM no momento em que esse ponto de referência foi criado.</span><span class="sxs-lookup"><span data-stu-id="c88db-148">An array of WMI instance IDs corresponding to the virtual disks of the VM at the time this reference point was created.</span></span> <span data-ttu-id="c88db-149">Esses discos virtuais têm IDs RCT associadas a eles.</span><span class="sxs-lookup"><span data-stu-id="c88db-149">These virtual disks have RCT IDs associated with them.</span></span>

</dd> <dt>

<span data-ttu-id="c88db-150">**VirtualSystemIdentifier**</span><span class="sxs-lookup"><span data-stu-id="c88db-150">**VirtualSystemIdentifier**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c88db-151">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c88db-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c88db-152">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c88db-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c88db-153">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema de ComputerSystem CIM**](cim-computersystem.md).**Nome**")</span><span class="sxs-lookup"><span data-stu-id="c88db-153">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**")</span></span>
</dt> </dl>

<span data-ttu-id="c88db-154">O nome do [**sistema de \_ ComputerSystem CIM**](cim-computersystem.md) ao qual este ponto de referência pertence</span><span class="sxs-lookup"><span data-stu-id="c88db-154">The name of the [**CIM\_ComputerSystem**](cim-computersystem.md) to which this reference point belongs</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c88db-155">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c88db-155">Requirements</span></span>



| <span data-ttu-id="c88db-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="c88db-156">Requirement</span></span> | <span data-ttu-id="c88db-157">Valor</span><span class="sxs-lookup"><span data-stu-id="c88db-157">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c88db-158">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c88db-158">Minimum supported client</span></span><br/> | <span data-ttu-id="c88db-159">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="c88db-159">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="c88db-160">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c88db-160">Minimum supported server</span></span><br/> | <span data-ttu-id="c88db-161">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="c88db-161">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="c88db-162">Namespace</span><span class="sxs-lookup"><span data-stu-id="c88db-162">Namespace</span></span><br/>                | <span data-ttu-id="c88db-163">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="c88db-163">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="c88db-164">MOF</span><span class="sxs-lookup"><span data-stu-id="c88db-164">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c88db-165"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c88db-165"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c88db-166">DLL</span><span class="sxs-lookup"><span data-stu-id="c88db-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c88db-167"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c88db-167"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c88db-168">Confira também</span><span class="sxs-lookup"><span data-stu-id="c88db-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c88db-169">**\_Managedelement do CIM**</span><span class="sxs-lookup"><span data-stu-id="c88db-169">**CIM\_ManagedElement**</span></span>](cim-managedelement.md)
</dt> </dl>

 

