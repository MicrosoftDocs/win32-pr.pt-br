---
description: A \_ classe CIM AssociatedProcessorMemory associa o processador e a memória do sistema ou o cache de um processador.
ms.assetid: a4c28a0a-e4cc-4db2-bd77-b7b5023eace6
ms.tgt_platform: multiple
title: Classe CIM_AssociatedProcessorMemory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AssociatedProcessorMemory
- CIM_AssociatedProcessorMemory.Antecedent
- CIM_AssociatedProcessorMemory.Dependent
- CIM_AssociatedProcessorMemory.BusSpeed
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: f35cdca92cb15e1c6fff215ff1363844e0d47012
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920464"
---
# <a name="cim_associatedprocessormemory-class"></a><span data-ttu-id="5e991-103">\_Classe CIM AssociatedProcessorMemory</span><span class="sxs-lookup"><span data-stu-id="5e991-103">CIM\_AssociatedProcessorMemory class</span></span>

<span data-ttu-id="5e991-104">A classe **CIM \_ AssociatedProcessorMemory** associa o processador e a memória do sistema ou o cache de um processador.</span><span class="sxs-lookup"><span data-stu-id="5e991-104">The **CIM\_AssociatedProcessorMemory** class associates the processor and system memory, or a processor's cache.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5e991-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="5e991-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="5e991-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="5e991-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="5e991-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="5e991-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="5e991-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="5e991-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e991-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5e991-109">Syntax</span></span>

``` syntax
[abstract, UUID("{464FFAB1-946F-11d2-AAE2-006008C78BC7}"), AMENDMENT]
class CIM_AssociatedProcessorMemory : CIM_AssociatedMemory
{
  CIM_Memory    REF Antecedent;
  CIM_Processor REF Dependent;
  uint32            BusSpeed;
};
```

## <a name="members"></a><span data-ttu-id="5e991-110">Membros</span><span class="sxs-lookup"><span data-stu-id="5e991-110">Members</span></span>

<span data-ttu-id="5e991-111">A classe **CIM \_ AssociatedProcessorMemory** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="5e991-111">The **CIM\_AssociatedProcessorMemory** class has these types of members:</span></span>

-   [<span data-ttu-id="5e991-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5e991-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5e991-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5e991-113">Properties</span></span>

<span data-ttu-id="5e991-114">A classe **CIM \_ AssociatedProcessorMemory** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="5e991-114">The **CIM\_AssociatedProcessorMemory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5e991-115">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="5e991-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e991-116">Tipo de dados **: \_ memória CIM**</span><span class="sxs-lookup"><span data-stu-id="5e991-116">Data type: **CIM\_Memory**</span></span>
</dt> <dt>

<span data-ttu-id="5e991-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5e991-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e991-118">Uma [**\_ memória CIM**](cim-memory.md) que descreve a memória instalada ou associada a um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5e991-118">A [**CIM\_Memory**](cim-memory.md) that describes the memory installed on or associated with a device.</span></span>

<span data-ttu-id="5e991-119">Essa propriedade é herdada do [**CIM \_ AssociatedMemory**](cim-associatedmemory.md).</span><span class="sxs-lookup"><span data-stu-id="5e991-119">This property is inherited from [**CIM\_AssociatedMemory**](cim-associatedmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="5e991-120">**BusSpeed**</span><span class="sxs-lookup"><span data-stu-id="5e991-120">**BusSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e991-121">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5e991-121">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5e991-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5e991-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e991-123">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("megahertz")</span><span class="sxs-lookup"><span data-stu-id="5e991-123">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("megahertz")</span></span>
</dt> </dl>

<span data-ttu-id="5e991-124">Velocidade do barramento, em megahertz (MHz), entre o processador e a memória.</span><span class="sxs-lookup"><span data-stu-id="5e991-124">Speed of the bus, in megahertz (MHz), between the processor and memory.</span></span>

</dd> <dt>

<span data-ttu-id="5e991-125">**Depende**</span><span class="sxs-lookup"><span data-stu-id="5e991-125">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e991-126">Tipo de dados **: \_ processador CIM**</span><span class="sxs-lookup"><span data-stu-id="5e991-126">Data type: **CIM\_Processor**</span></span>
</dt> <dt>

<span data-ttu-id="5e991-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5e991-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e991-128">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")</span><span class="sxs-lookup"><span data-stu-id="5e991-128">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="5e991-129">Um [**\_ processador CIM**](cim-processor.md) que descreve o processador que acessa a memória ou usa o cache.</span><span class="sxs-lookup"><span data-stu-id="5e991-129">A [**CIM\_Processor**](cim-processor.md) describing the processor that accesses the memory or uses the cache.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5e991-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="5e991-130">Remarks</span></span>

<span data-ttu-id="5e991-131">A classe **CIM \_ AssociatedProcessorMemory** é derivada de [**\_ AssociatedMemory CIM**](cim-associatedmemory.md).</span><span class="sxs-lookup"><span data-stu-id="5e991-131">The **CIM\_AssociatedProcessorMemory** class is derived from [**CIM\_AssociatedMemory**](cim-associatedmemory.md).</span></span>

<span data-ttu-id="5e991-132">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="5e991-132">WMI does not implement this class.</span></span> <span data-ttu-id="5e991-133">Para obter mais informações sobre classes derivadas de **CIM \_ AssociatedProcessorMemory**, consulte [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="5e991-133">For more information about classes derived from **CIM\_AssociatedProcessorMemory**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="5e991-134">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="5e991-134">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="5e991-135">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="5e991-135">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e991-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5e991-136">Requirements</span></span>



| <span data-ttu-id="5e991-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e991-137">Requirement</span></span> | <span data-ttu-id="5e991-138">Valor</span><span class="sxs-lookup"><span data-stu-id="5e991-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5e991-139">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5e991-139">Minimum supported client</span></span><br/> | <span data-ttu-id="5e991-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5e991-140">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5e991-141">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5e991-141">Minimum supported server</span></span><br/> | <span data-ttu-id="5e991-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5e991-142">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5e991-143">Namespace</span><span class="sxs-lookup"><span data-stu-id="5e991-143">Namespace</span></span><br/>                | <span data-ttu-id="5e991-144">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="5e991-144">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5e991-145">MOF</span><span class="sxs-lookup"><span data-stu-id="5e991-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5e991-146"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5e991-146"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5e991-147">DLL</span><span class="sxs-lookup"><span data-stu-id="5e991-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5e991-148"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5e991-148"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e991-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="5e991-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e991-150">**\_ASSOCIATEDMEMORY CIM**</span><span class="sxs-lookup"><span data-stu-id="5e991-150">**CIM\_AssociatedMemory**</span></span>](cim-associatedmemory.md)
</dt> </dl>

 

