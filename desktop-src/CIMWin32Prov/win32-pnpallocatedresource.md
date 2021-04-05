---
description: A \_ classe WMI de associação do Win32 PnPAllocatedResource representa uma associação entre dispositivos lógicos e recursos do sistema.
ms.assetid: e3cef457-cf88-4df5-8db8-b0495f636904
ms.tgt_platform: multiple
title: Classe Win32_PnPAllocatedResource
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PnPAllocatedResource
- Win32_PnPAllocatedResource.Antecedent
- Win32_PnPAllocatedResource.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 353009016c8d4d54cdc92fb8f0ed062567dded6f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826685"
---
# <a name="win32_pnpallocatedresource-class"></a><span data-ttu-id="16066-103">\_Classe Win32 PnPAllocatedResource</span><span class="sxs-lookup"><span data-stu-id="16066-103">Win32\_PnPAllocatedResource class</span></span>

<span data-ttu-id="16066-104">A [classe WMI](../wmisdk/retrieving-a-class.md) de associação do **Win32 \_ PnPAllocatedResource** representa uma associação entre dispositivos lógicos e recursos do sistema.</span><span class="sxs-lookup"><span data-stu-id="16066-104">The **Win32\_PnPAllocatedResource** association [WMI class](../wmisdk/retrieving-a-class.md) represents an association between logical devices and system resources.</span></span> <span data-ttu-id="16066-105">Essa classe é usada para descobrir os recursos que estão sendo usados por um dispositivo específico, como uma IRQ (solicitação de interrupção) ou um canal de acesso direto à memória (DMA).</span><span class="sxs-lookup"><span data-stu-id="16066-105">This class is used to discover the resources that are in-use by a specific device, such as an Interrupt ReQuest (IRQ) or a Direct Memory Access (DMA) channel.</span></span>

<span data-ttu-id="16066-106">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="16066-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="16066-107">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="16066-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="16066-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="16066-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("970C0998-41FE-4275-B7D9-7DABAD3FBC4D"), AMENDMENT]
class Win32_PnPAllocatedResource : CIM_AllocatedResource
{
  CIM_SystemResource REF Antecedent;
  Win32_PnPEntity    REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="16066-109">Membros</span><span class="sxs-lookup"><span data-stu-id="16066-109">Members</span></span>

<span data-ttu-id="16066-110">A classe **Win32 \_ PnPAllocatedResource** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="16066-110">The **Win32\_PnPAllocatedResource** class has these types of members:</span></span>

-   [<span data-ttu-id="16066-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="16066-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="16066-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="16066-112">Properties</span></span>

<span data-ttu-id="16066-113">A classe **Win32 \_ PnPAllocatedResource** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="16066-113">The **Win32\_PnPAllocatedResource** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="16066-114">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="16066-114">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16066-115">Tipo de dados: **CIM \_ SystemResource**</span><span class="sxs-lookup"><span data-stu-id="16066-115">Data type: **CIM\_SystemResource**</span></span>
</dt> <dt>

<span data-ttu-id="16066-116">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="16066-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="16066-117">Qualificadores: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("Antecedent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM \| CIM \_ SystemResource")</span><span class="sxs-lookup"><span data-stu-id="16066-117">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Antecedent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM\|CIM\_SystemResource")</span></span>
</dt> </dl>

<span data-ttu-id="16066-118">Referência à instância [**de \_ SystemResource do CIM**](cim-systemresource.md) que representa as propriedades de um recurso do sistema disponível para o dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="16066-118">Reference to the [**CIM\_SystemResource**](cim-systemresource.md) instance that represents the properties of a system resource available to the logical device.</span></span> <span data-ttu-id="16066-119">Essa propriedade é herdada [**da \_ dependência CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="16066-119">This property is inherited from [**CIM\_Dependency**](cim-dependency.md).</span></span>

</dd> <dt>

<span data-ttu-id="16066-120">**Depende**</span><span class="sxs-lookup"><span data-stu-id="16066-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16066-121">Tipo de dados: **Win32 \_ PnPEntity**</span><span class="sxs-lookup"><span data-stu-id="16066-121">Data type: **Win32\_PnPEntity**</span></span>
</dt> <dt>

<span data-ttu-id="16066-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="16066-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="16066-123">Qualificadores: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("dependent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM \| CIM \_ LogicalDevice")</span><span class="sxs-lookup"><span data-stu-id="16066-123">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Dependent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM\|CIM\_LogicalDevice")</span></span>
</dt> </dl>

<span data-ttu-id="16066-124">Referência à instância do [**Win32 \_ PnPEntity**](win32-pnpentity.md) que representa as propriedades do dispositivo lógico usando os recursos do sistema atribuídos a ele.</span><span class="sxs-lookup"><span data-stu-id="16066-124">Reference to the [**Win32\_PnPEntity**](win32-pnpentity.md) instance that represents the properties of the logical device using the system resources assigned to it.</span></span> <span data-ttu-id="16066-125">Essa propriedade é herdada [**da \_ dependência CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="16066-125">This property is inherited from [**CIM\_Dependency**](cim-dependency.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="16066-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="16066-126">Remarks</span></span>

<span data-ttu-id="16066-127">A classe **Win32 \_ PnPAllocatedResource** é derivada de [**CIM \_ AllocatedResource**](cim-allocatedresource.md).</span><span class="sxs-lookup"><span data-stu-id="16066-127">The **Win32\_PnPAllocatedResource** class is derived from [**CIM\_AllocatedResource**](cim-allocatedresource.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="16066-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="16066-128">Requirements</span></span>



| <span data-ttu-id="16066-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="16066-129">Requirement</span></span> | <span data-ttu-id="16066-130">Valor</span><span class="sxs-lookup"><span data-stu-id="16066-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="16066-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="16066-131">Minimum supported client</span></span><br/> | <span data-ttu-id="16066-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="16066-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="16066-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="16066-133">Minimum supported server</span></span><br/> | <span data-ttu-id="16066-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="16066-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="16066-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="16066-135">Namespace</span></span><br/>                | <span data-ttu-id="16066-136">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="16066-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="16066-137">MOF</span><span class="sxs-lookup"><span data-stu-id="16066-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="16066-138"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="16066-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="16066-139">DLL</span><span class="sxs-lookup"><span data-stu-id="16066-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="16066-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="16066-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16066-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="16066-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16066-142">**\_ALLOCATEDRESOURCE CIM**</span><span class="sxs-lookup"><span data-stu-id="16066-142">**CIM\_AllocatedResource**</span></span>](cim-allocatedresource.md)
</dt> <dt>

[<span data-ttu-id="16066-143">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="16066-143">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
