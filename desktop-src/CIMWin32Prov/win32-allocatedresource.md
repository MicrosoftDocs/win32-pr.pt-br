---
description: A \_ classe WMI de associação AllocatedResource do Win32 relaciona um dispositivo lógico a um recurso do sistema. Essa classe é usada para descobrir quais recursos, como IRQs ou canais DMA, estão em uso por um dispositivo específico.
ms.assetid: cfac1209-1405-4fee-847c-8a61504bfac1
ms.tgt_platform: multiple
title: Classe Win32_AllocatedResource
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_AllocatedResource
- Win32_AllocatedResource.Dependent
- Win32_AllocatedResource.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 87a57e53a85e4433ae325fc2ed441211db75b79f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920528"
---
# <a name="win32_allocatedresource-class"></a><span data-ttu-id="5916b-104">\_Classe Win32 AllocatedResource</span><span class="sxs-lookup"><span data-stu-id="5916b-104">Win32\_AllocatedResource class</span></span>

<span data-ttu-id="5916b-105">A [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) de associação **\_ AllocatedResource do Win32** relaciona um dispositivo lógico a um recurso do sistema.</span><span class="sxs-lookup"><span data-stu-id="5916b-105">The **Win32\_AllocatedResource** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a logical device to a system resource.</span></span> <span data-ttu-id="5916b-106">Essa classe é usada para descobrir quais recursos, como IRQs ou canais DMA, estão em uso por um dispositivo específico.</span><span class="sxs-lookup"><span data-stu-id="5916b-106">This class is used to discover which resources, such as IRQs or DMA channels, are in use by a specific device.</span></span>

<span data-ttu-id="5916b-107">Essa classe está obsoleta.</span><span class="sxs-lookup"><span data-stu-id="5916b-107">This class is obsolete.</span></span> <span data-ttu-id="5916b-108">No lugar dessa classe, você deve usar as propriedades na classe [**Win32 \_ PNPAllocatedResource**](win32-pnpallocatedresource.md) .</span><span class="sxs-lookup"><span data-stu-id="5916b-108">In place of this class, you should use the properties in the [**Win32\_PNPAllocatedResource**](win32-pnpallocatedresource.md) class.</span></span>

<span data-ttu-id="5916b-109">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="5916b-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="5916b-110">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="5916b-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="5916b-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5916b-111">Syntax</span></span>

``` syntax
[DEPRECATED, Dynamic, Provider("CIMWin32"), UUID("{8502C50D-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_AllocatedResource : CIM_Dependency
{
  CIM_LogicalDevice  REF Dependent;
  CIM_SystemResource REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="5916b-112">Membros</span><span class="sxs-lookup"><span data-stu-id="5916b-112">Members</span></span>

<span data-ttu-id="5916b-113">A classe **Win32 \_ AllocatedResource** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="5916b-113">The **Win32\_AllocatedResource** class has these types of members:</span></span>

-   [<span data-ttu-id="5916b-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5916b-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5916b-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5916b-115">Properties</span></span>

<span data-ttu-id="5916b-116">A classe **Win32 \_ AllocatedResource** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="5916b-116">The **Win32\_AllocatedResource** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5916b-117">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="5916b-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5916b-118">Tipo de dados: **CIM \_ SystemResource**</span><span class="sxs-lookup"><span data-stu-id="5916b-118">Data type: **CIM\_SystemResource**</span></span>
</dt> <dt>

<span data-ttu-id="5916b-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5916b-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5916b-120">Qualificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \| CIM \_ SystemResource")</span><span class="sxs-lookup"><span data-stu-id="5916b-120">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\|CIM\_SystemResource")</span></span>
</dt> </dl>

<span data-ttu-id="5916b-121">Um [**\_ SystemResource CIM**](cim-systemresource.md) que descreve as propriedades de um recurso do sistema disponível para o dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="5916b-121">A [**CIM\_SystemResource**](cim-systemresource.md) that describes the properties of a system resource available to the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="5916b-122">**Depende**</span><span class="sxs-lookup"><span data-stu-id="5916b-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5916b-123">Tipo de dados **: \_ LogicalDevice CIM**</span><span class="sxs-lookup"><span data-stu-id="5916b-123">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="5916b-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5916b-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5916b-125">Qualificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \| CIM \_ LogicalDevice")</span><span class="sxs-lookup"><span data-stu-id="5916b-125">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\|CIM\_LogicalDevice")</span></span>
</dt> </dl>

<span data-ttu-id="5916b-126">Um [**\_ LogicalDevice CIM**](cim-logicaldevice.md) que representa as propriedades do dispositivo lógico que está usando os recursos do sistema atribuídos a ele.</span><span class="sxs-lookup"><span data-stu-id="5916b-126">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that represents the properties of the logical device that is using the system resources assigned to it.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5916b-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="5916b-127">Remarks</span></span>

<span data-ttu-id="5916b-128">A classe **Win32 \_ AllocatedResource** é derivada da [**\_ dependência CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="5916b-128">The **Win32\_AllocatedResource** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5916b-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5916b-129">Requirements</span></span>



| <span data-ttu-id="5916b-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="5916b-130">Requirement</span></span> | <span data-ttu-id="5916b-131">Valor</span><span class="sxs-lookup"><span data-stu-id="5916b-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5916b-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5916b-132">Minimum supported client</span></span><br/> | <span data-ttu-id="5916b-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5916b-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5916b-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5916b-134">Minimum supported server</span></span><br/> | <span data-ttu-id="5916b-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5916b-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5916b-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="5916b-136">Namespace</span></span><br/>                | <span data-ttu-id="5916b-137">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="5916b-137">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5916b-138">MOF</span><span class="sxs-lookup"><span data-stu-id="5916b-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5916b-139"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5916b-139"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5916b-140">DLL</span><span class="sxs-lookup"><span data-stu-id="5916b-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5916b-141"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5916b-141"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5916b-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="5916b-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5916b-143">**\_Dependência CIM**</span><span class="sxs-lookup"><span data-stu-id="5916b-143">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> <dt>

[<span data-ttu-id="5916b-144">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="5916b-144">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

