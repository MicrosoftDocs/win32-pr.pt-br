---
description: A \_ classe WMI de associação do Win32 AssociatedProcessorMemory relaciona um processador e sua memória de cache.
ms.assetid: 23da2a9d-772e-4258-9489-07d47801b2d8
ms.tgt_platform: multiple
title: Classe Win32_AssociatedProcessorMemory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_AssociatedProcessorMemory
- Win32_AssociatedProcessorMemory.BusSpeed
- Win32_AssociatedProcessorMemory.Dependent
- Win32_AssociatedProcessorMemory.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3737dca869c539d1414c4399f35fb8f107697b70
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920527"
---
# <a name="win32_associatedprocessormemory-class"></a><span data-ttu-id="889a7-103">\_Classe Win32 AssociatedProcessorMemory</span><span class="sxs-lookup"><span data-stu-id="889a7-103">Win32\_AssociatedProcessorMemory class</span></span>

<span data-ttu-id="889a7-104">A [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) de associação do **Win32 \_ AssociatedProcessorMemory** relaciona um processador e sua memória de cache.</span><span class="sxs-lookup"><span data-stu-id="889a7-104">The **Win32\_AssociatedProcessorMemory** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a processor and its cache memory.</span></span>

<span data-ttu-id="889a7-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="889a7-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="889a7-106">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="889a7-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="889a7-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="889a7-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{074737F0-ACBC-11d2-ABF6-00805F538618}"), AMENDMENT]
class Win32_AssociatedProcessorMemory : CIM_AssociatedProcessorMemory
{
  uint32                BusSpeed;
  Win32_Processor   REF Dependent;
  Win32_CacheMemory REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="889a7-108">Membros</span><span class="sxs-lookup"><span data-stu-id="889a7-108">Members</span></span>

<span data-ttu-id="889a7-109">A classe **Win32 \_ AssociatedProcessorMemory** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="889a7-109">The **Win32\_AssociatedProcessorMemory** class has these types of members:</span></span>

-   [<span data-ttu-id="889a7-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="889a7-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="889a7-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="889a7-111">Properties</span></span>

<span data-ttu-id="889a7-112">A classe **Win32 \_ AssociatedProcessorMemory** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="889a7-112">The **Win32\_AssociatedProcessorMemory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="889a7-113">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="889a7-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="889a7-114">Tipo de dados: **Win32 \_ CacheMemory**</span><span class="sxs-lookup"><span data-stu-id="889a7-114">Data type: **Win32\_CacheMemory**</span></span>
</dt> <dt>

<span data-ttu-id="889a7-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="889a7-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="889a7-116">Qualificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ CacheMemory")</span><span class="sxs-lookup"><span data-stu-id="889a7-116">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_CacheMemory")</span></span>
</dt> </dl>

<span data-ttu-id="889a7-117">Um [**\_ CacheMemory Win32**](win32-cachememory.md) que descreve a memória de cache disponível para o processador.</span><span class="sxs-lookup"><span data-stu-id="889a7-117">A [**Win32\_CacheMemory**](win32-cachememory.md) that describes the cache memory available to the processor.</span></span>

</dd> <dt>

<span data-ttu-id="889a7-118">**BusSpeed**</span><span class="sxs-lookup"><span data-stu-id="889a7-118">**BusSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="889a7-119">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="889a7-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="889a7-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="889a7-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="889a7-121">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("megahertz")</span><span class="sxs-lookup"><span data-stu-id="889a7-121">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("megahertz")</span></span>
</dt> </dl>

<span data-ttu-id="889a7-122">Velocidade do barramento, em megahertz (MHz), entre o processador e a memória.</span><span class="sxs-lookup"><span data-stu-id="889a7-122">Speed of the bus, in megahertz (MHz), between the processor and memory.</span></span>

<span data-ttu-id="889a7-123">Essa propriedade é herdada do [**CIM \_ AssociatedProcessorMemory**](cim-associatedprocessormemory.md).</span><span class="sxs-lookup"><span data-stu-id="889a7-123">This property is inherited from [**CIM\_AssociatedProcessorMemory**](cim-associatedprocessormemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="889a7-124">**Depende**</span><span class="sxs-lookup"><span data-stu-id="889a7-124">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="889a7-125">Tipo de dados **: \_ processador Win32**</span><span class="sxs-lookup"><span data-stu-id="889a7-125">Data type: **Win32\_Processor**</span></span>
</dt> <dt>

<span data-ttu-id="889a7-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="889a7-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="889a7-127">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**substituição**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| processador WMI Win32 \_ ")</span><span class="sxs-lookup"><span data-stu-id="889a7-127">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_Processor")</span></span>
</dt> </dl>

<span data-ttu-id="889a7-128">Um [**\_ processador Win32**](win32-processor.md) que descreve o processador que está usando a memória cache.</span><span class="sxs-lookup"><span data-stu-id="889a7-128">A [**Win32\_Processor**](win32-processor.md) that describes the processor that is using the cache memory.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="889a7-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="889a7-129">Remarks</span></span>

<span data-ttu-id="889a7-130">A classe **Win32 \_ AssociatedProcessorMemory** é derivada de [**CIM \_ AssociatedProcessorMemory**](cim-associatedprocessormemory.md).</span><span class="sxs-lookup"><span data-stu-id="889a7-130">The **Win32\_AssociatedProcessorMemory** class is derived from [**CIM\_AssociatedProcessorMemory**](cim-associatedprocessormemory.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="889a7-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="889a7-131">Requirements</span></span>



| <span data-ttu-id="889a7-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="889a7-132">Requirement</span></span> | <span data-ttu-id="889a7-133">Valor</span><span class="sxs-lookup"><span data-stu-id="889a7-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="889a7-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="889a7-134">Minimum supported client</span></span><br/> | <span data-ttu-id="889a7-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="889a7-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="889a7-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="889a7-136">Minimum supported server</span></span><br/> | <span data-ttu-id="889a7-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="889a7-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="889a7-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="889a7-138">Namespace</span></span><br/>                | <span data-ttu-id="889a7-139">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="889a7-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="889a7-140">MOF</span><span class="sxs-lookup"><span data-stu-id="889a7-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="889a7-141"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="889a7-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="889a7-142">DLL</span><span class="sxs-lookup"><span data-stu-id="889a7-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="889a7-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="889a7-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="889a7-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="889a7-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="889a7-145">**\_ASSOCIATEDPROCESSORMEMORY CIM**</span><span class="sxs-lookup"><span data-stu-id="889a7-145">**CIM\_AssociatedProcessorMemory**</span></span>](cim-associatedprocessormemory.md)
</dt> <dt>

[<span data-ttu-id="889a7-146">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="889a7-146">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

