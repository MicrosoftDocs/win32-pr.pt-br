---
description: Representa uma coleção de pontos de referência do sistema virtual.
ms.assetid: dc293f94-a683-468f-af05-ba99824d773e
title: Classe Msvm_ReferencePointCollection
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReferencePointCollection
- Msvm_ReferencePointCollection.CollectionID
- Msvm_ReferencePointCollection.ElementName
- Msvm_ReferencePointCollection.ReferencePointType
- Msvm_ReferencePointCollection.ConsistencyLevel
- Msvm_ReferencePointCollection.VirtualSystemCollectionId
- Msvm_ReferencePointCollection.HasAssociatedLog
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 570590221ee8568d78e150fec3c359365c8434cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828592"
---
# <a name="msvm_referencepointcollection-class"></a><span data-ttu-id="0953a-103">\_Classe Msvm ReferencePointCollection</span><span class="sxs-lookup"><span data-stu-id="0953a-103">Msvm\_ReferencePointCollection class</span></span>

<span data-ttu-id="0953a-104">Representa uma coleção de pontos de referência do sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="0953a-104">Represents a collection of virtual system reference points.</span></span>

<span data-ttu-id="0953a-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="0953a-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0953a-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0953a-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ReferencePointCollection : CIM_Collection
{
  string  CollectionID;
  string  ElementName;
  uint16  ReferencePointType;
  uint16  ConsistencyLevel;
  string  VirtualSystemCollectionId;
  boolean HasAssociatedLog;
};
```

## <a name="members"></a><span data-ttu-id="0953a-107">Membros</span><span class="sxs-lookup"><span data-stu-id="0953a-107">Members</span></span>

<span data-ttu-id="0953a-108">A classe **Msvm \_ ReferencePointCollection** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="0953a-108">The **Msvm\_ReferencePointCollection** class has these types of members:</span></span>

-   [<span data-ttu-id="0953a-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0953a-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0953a-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0953a-110">Properties</span></span>

<span data-ttu-id="0953a-111">A classe **Msvm \_ ReferencePointCollection** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="0953a-111">The **Msvm\_ReferencePointCollection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0953a-112">**CollectionID**</span><span class="sxs-lookup"><span data-stu-id="0953a-112">**CollectionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0953a-113">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0953a-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0953a-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0953a-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0953a-115">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**substituição**](/windows/desktop/WmiSdk/standard-qualifiers) ("CollectionId"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="0953a-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CollectionID"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="0953a-116">A identificação exclusiva do objeto de coleção.</span><span class="sxs-lookup"><span data-stu-id="0953a-116">The unique identification of the collection object.</span></span>

</dd> <dt>

<span data-ttu-id="0953a-117">**ConsistencyLevel**</span><span class="sxs-lookup"><span data-stu-id="0953a-117">**ConsistencyLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0953a-118">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0953a-118">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0953a-119">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0953a-119">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0953a-120">Nível de consistência do ponto de referência.</span><span class="sxs-lookup"><span data-stu-id="0953a-120">Consistency level of the reference point.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0953a-121"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="0953a-121"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>

<span data-ttu-id="0953a-122"><span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>Com **consistência de falha** (1)</span><span class="sxs-lookup"><span data-stu-id="0953a-122"><span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>**Crash Consistent** (1)</span></span>


</dt> <dd>

<span data-ttu-id="0953a-123">O ponto de referência indica um ponto no tempo em que o sistema virtual estava em estado de falha consistente.</span><span class="sxs-lookup"><span data-stu-id="0953a-123">The reference point indicates a point in time when the virtual system was in crash consistent state.</span></span>

</dd> <dt>

<span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>

<span data-ttu-id="0953a-124"><span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>**Consistente** com o aplicativo (2)</span><span class="sxs-lookup"><span data-stu-id="0953a-124"><span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>**Application Consistent** (2)</span></span>


</dt> <dd>

<span data-ttu-id="0953a-125">O ponto de referência indica um ponto no tempo em que o sistema virtual estava no estado consistente do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0953a-125">The reference point indicates a point in time when the virtual system was in application consistent state.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0953a-126">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="0953a-126">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0953a-127">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0953a-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0953a-128">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0953a-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0953a-129">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ElementName")</span><span class="sxs-lookup"><span data-stu-id="0953a-129">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ElementName")</span></span>
</dt> </dl>

<span data-ttu-id="0953a-130">Um nome definido pelo usuário para a coleção.</span><span class="sxs-lookup"><span data-stu-id="0953a-130">An user-defined name for the collection.</span></span> <span data-ttu-id="0953a-131">Observe que isso não é garantido como exclusivo.</span><span class="sxs-lookup"><span data-stu-id="0953a-131">Note this is not guaranteed to be unique.</span></span>

</dd> <dt>

<span data-ttu-id="0953a-132">**HasAssociatedLog**</span><span class="sxs-lookup"><span data-stu-id="0953a-132">**HasAssociatedLog**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0953a-133">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="0953a-133">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0953a-134">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0953a-134">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0953a-135">**true** se todos os pontos de referência de membro tiverem logs associados.</span><span class="sxs-lookup"><span data-stu-id="0953a-135">**true** if all the member reference points have associated logs.</span></span> <span data-ttu-id="0953a-136">Isso é válido somente para pontos de referência baseados em log.</span><span class="sxs-lookup"><span data-stu-id="0953a-136">This is valid only for log based reference points.</span></span> <span data-ttu-id="0953a-137">Para pontos de referência baseados em RCT, **HasAssociatedLog** é definido como **false**.</span><span class="sxs-lookup"><span data-stu-id="0953a-137">For RCT based reference points, **HasAssociatedLog** is set to **false**.</span></span> <span data-ttu-id="0953a-138">Para pontos de referência baseados em log, uma vez que o log é Descartado, o **HasAssociatedLog** se torna **falso**.</span><span class="sxs-lookup"><span data-stu-id="0953a-138">For log based reference points, once the log is discarded **HasAssociatedLog** becomes **false**.</span></span>

</dd> <dt>

<span data-ttu-id="0953a-139">**ReferencePointType**</span><span class="sxs-lookup"><span data-stu-id="0953a-139">**ReferencePointType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0953a-140">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0953a-140">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0953a-141">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0953a-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0953a-142">Qualificadores: [ **in**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="0953a-142">Qualifiers: [**In**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="0953a-143">Indica o tipo do ponto de referência.</span><span class="sxs-lookup"><span data-stu-id="0953a-143">Indicates the type of the reference point.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0953a-144"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="0953a-144"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>

<span data-ttu-id="0953a-145"><span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>**Baseado em log** (1)</span><span class="sxs-lookup"><span data-stu-id="0953a-145"><span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>**Log based** (1)</span></span>


</dt> <dd>

<span data-ttu-id="0953a-146">Rastreamento de log de réplica do Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="0953a-146">Hyper-V replica log tracking.</span></span>

</dd> <dt>

<span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>

<span data-ttu-id="0953a-147"><span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>**Baseado em RCT** (2)</span><span class="sxs-lookup"><span data-stu-id="0953a-147"><span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>**RCT based** (2)</span></span>


</dt> <dd>

<span data-ttu-id="0953a-148">Com base em Controle de Alterações resilientes de discos virtuais.</span><span class="sxs-lookup"><span data-stu-id="0953a-148">Based on Resilient Change Tracking of virtual disks.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="0953a-149"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="0953a-149"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

<span data-ttu-id="0953a-150"><span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>**Específico do fornecedor** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="0953a-150"><span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>**Vendor Specific** (32768..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0953a-151">**VirtualSystemCollectionId**</span><span class="sxs-lookup"><span data-stu-id="0953a-151">**VirtualSystemCollectionId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0953a-152">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0953a-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0953a-153">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0953a-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0953a-154">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**Msvm \_ VirtualSystemCollection**](msvm-virtualsystemcollection.md).**CollectionId**")</span><span class="sxs-lookup"><span data-stu-id="0953a-154">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**Msvm\_VirtualSystemCollection**](msvm-virtualsystemcollection.md).**CollectionID**")</span></span>
</dt> </dl>

<span data-ttu-id="0953a-155">O identificador do [**\_ VirtualSystemCollection Msvm**](msvm-virtualsystemcollection.md) ao qual esse ponto de referência pertence.</span><span class="sxs-lookup"><span data-stu-id="0953a-155">The identifier of the [**Msvm\_VirtualSystemCollection**](msvm-virtualsystemcollection.md) to which this reference point belongs.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0953a-156">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0953a-156">Requirements</span></span>



| <span data-ttu-id="0953a-157">Requisito</span><span class="sxs-lookup"><span data-stu-id="0953a-157">Requirement</span></span> | <span data-ttu-id="0953a-158">Valor</span><span class="sxs-lookup"><span data-stu-id="0953a-158">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0953a-159">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0953a-159">Minimum supported client</span></span><br/> | <span data-ttu-id="0953a-160">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="0953a-160">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="0953a-161">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0953a-161">Minimum supported server</span></span><br/> | <span data-ttu-id="0953a-162">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="0953a-162">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="0953a-163">Namespace</span><span class="sxs-lookup"><span data-stu-id="0953a-163">Namespace</span></span><br/>                | <span data-ttu-id="0953a-164">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="0953a-164">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="0953a-165">MOF</span><span class="sxs-lookup"><span data-stu-id="0953a-165">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0953a-166"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0953a-166"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0953a-167">DLL</span><span class="sxs-lookup"><span data-stu-id="0953a-167">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0953a-168"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0953a-168"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0953a-169">Confira também</span><span class="sxs-lookup"><span data-stu-id="0953a-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0953a-170">**\_Coleção CIM**</span><span class="sxs-lookup"><span data-stu-id="0953a-170">**CIM\_Collection**</span></span>](cim-collection.md)
</dt> </dl>

 

