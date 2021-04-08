---
description: A \_ classe WMI de associação PhysicalMemoryLocation do Win32 relaciona uma matriz de memória física e sua memória física.
ms.assetid: 40252428-77ca-4dfb-8048-c05096a114d8
ms.tgt_platform: multiple
title: Classe Win32_PhysicalMemoryLocation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PhysicalMemoryLocation
- Win32_PhysicalMemoryLocation.LocationWithinContainer
- Win32_PhysicalMemoryLocation.PartComponent
- Win32_PhysicalMemoryLocation.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: daa6d47b13cb5caa74a10f28ab5fcd6e66e1524f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920588"
---
# <a name="win32_physicalmemorylocation-class"></a><span data-ttu-id="cbe4c-103">\_Classe Win32 PhysicalMemoryLocation</span><span class="sxs-lookup"><span data-stu-id="cbe4c-103">Win32\_PhysicalMemoryLocation class</span></span>

<span data-ttu-id="cbe4c-104">A [classe WMI](../wmisdk/retrieving-a-class.md) de associação **\_ PhysicalMemoryLocation do Win32** relaciona uma matriz de memória física e sua memória física.</span><span class="sxs-lookup"><span data-stu-id="cbe4c-104">The **Win32\_PhysicalMemoryLocation** association [WMI class](../wmisdk/retrieving-a-class.md) relates an array of physical memory and its physical memory.</span></span>

<span data-ttu-id="cbe4c-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="cbe4c-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="cbe4c-106">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="cbe4c-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="cbe4c-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cbe4c-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{B24EF562-BBBE-11d2-ABFB-00805F538618}"), AMENDMENT]
class Win32_PhysicalMemoryLocation : CIM_PackagedComponent
{
  string                        LocationWithinContainer;
  Win32_PhysicalMemory      REF PartComponent;
  Win32_PhysicalMemoryArray REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="cbe4c-108">Membros</span><span class="sxs-lookup"><span data-stu-id="cbe4c-108">Members</span></span>

<span data-ttu-id="cbe4c-109">A classe **Win32 \_ PhysicalMemoryLocation** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="cbe4c-109">The **Win32\_PhysicalMemoryLocation** class has these types of members:</span></span>

-   [<span data-ttu-id="cbe4c-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="cbe4c-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cbe4c-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="cbe4c-111">Properties</span></span>

<span data-ttu-id="cbe4c-112">A classe **Win32 \_ PhysicalMemoryLocation** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="cbe4c-112">The **Win32\_PhysicalMemoryLocation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cbe4c-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="cbe4c-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cbe4c-114">Tipo de dados: **Win32 \_ PhysicalMemoryArray**</span><span class="sxs-lookup"><span data-stu-id="cbe4c-114">Data type: **Win32\_PhysicalMemoryArray**</span></span>
</dt> <dt>

<span data-ttu-id="cbe4c-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cbe4c-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cbe4c-116">Qualificadores: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ PhysicalMemoryArray")</span><span class="sxs-lookup"><span data-stu-id="cbe4c-116">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_PhysicalMemoryArray")</span></span>
</dt> </dl>

<span data-ttu-id="cbe4c-117">Um [**\_ PhysicalMemoryArray Win32**](win32-physicalmemoryarray.md) que representa a matriz de memória física que contém a memória física.</span><span class="sxs-lookup"><span data-stu-id="cbe4c-117">A [**Win32\_PhysicalMemoryArray**](win32-physicalmemoryarray.md) that represents the physical memory array that contains the physical memory.</span></span>

</dd> <dt>

<span data-ttu-id="cbe4c-118">**LocationWithinContainer**</span><span class="sxs-lookup"><span data-stu-id="cbe4c-118">**LocationWithinContainer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cbe4c-119">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="cbe4c-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cbe4c-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cbe4c-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cbe4c-121">Cadeia de caracteres de forma livre que representa o posicionamento do elemento físico dentro do pacote físico.</span><span class="sxs-lookup"><span data-stu-id="cbe4c-121">Free-form string that represents the positioning of the physical element within the physical package.</span></span> <span data-ttu-id="cbe4c-122">Informações relativas a elementos estacionários no contêiner (por exemplo, "segundo compartimento da unidade a partir da parte superior"), ângulos, altitudes e outros dados podem ser registrados nessa propriedade.</span><span class="sxs-lookup"><span data-stu-id="cbe4c-122">Information relative to stationary elements in the container (for example, "second drive bay from the top"), angles, altitudes, and other data can be recorded in this property.</span></span> <span data-ttu-id="cbe4c-123">Essa cadeia de caracteres pode complementar ou ser usada no lugar da instanciação do objeto de [**\_ local do CIM**](cim-location.md) .</span><span class="sxs-lookup"><span data-stu-id="cbe4c-123">This string could supplement or be used in place of instantiating the [**CIM\_Location**](cim-location.md) object.</span></span>

<span data-ttu-id="cbe4c-124">Essa propriedade é herdada [**do \_ contêiner CIM**](cim-container.md).</span><span class="sxs-lookup"><span data-stu-id="cbe4c-124">This property is inherited from [**CIM\_Container**](cim-container.md).</span></span>

</dd> <dt>

<span data-ttu-id="cbe4c-125">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="cbe4c-125">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cbe4c-126">Tipo de dados: **Win32 \_ PhysicalMemory**</span><span class="sxs-lookup"><span data-stu-id="cbe4c-126">Data type: **Win32\_PhysicalMemory**</span></span>
</dt> <dt>

<span data-ttu-id="cbe4c-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cbe4c-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cbe4c-128">Qualificadores: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ PhysicalMemory")</span><span class="sxs-lookup"><span data-stu-id="cbe4c-128">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_PhysicalMemory")</span></span>
</dt> </dl>

<span data-ttu-id="cbe4c-129">Um [**\_ PhysicalMemory Win32**](win32-physicalmemory.md) que representa a memória física contida na matriz de memória física.</span><span class="sxs-lookup"><span data-stu-id="cbe4c-129">A [**Win32\_PhysicalMemory**](win32-physicalmemory.md) that represents the physical memory contained in the physical memory array.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cbe4c-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="cbe4c-130">Remarks</span></span>

<span data-ttu-id="cbe4c-131">A classe **Win32 \_ PhysicalMemoryLocation** é derivada de [**CIM \_ PackagedComponent**](cim-packagedcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="cbe4c-131">The **Win32\_PhysicalMemoryLocation** class is derived from [**CIM\_PackagedComponent**](cim-packagedcomponent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cbe4c-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cbe4c-132">Requirements</span></span>



| <span data-ttu-id="cbe4c-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="cbe4c-133">Requirement</span></span> | <span data-ttu-id="cbe4c-134">Valor</span><span class="sxs-lookup"><span data-stu-id="cbe4c-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cbe4c-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cbe4c-135">Minimum supported client</span></span><br/> | <span data-ttu-id="cbe4c-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cbe4c-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="cbe4c-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cbe4c-137">Minimum supported server</span></span><br/> | <span data-ttu-id="cbe4c-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cbe4c-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="cbe4c-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="cbe4c-139">Namespace</span></span><br/>                | <span data-ttu-id="cbe4c-140">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="cbe4c-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="cbe4c-141">MOF</span><span class="sxs-lookup"><span data-stu-id="cbe4c-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cbe4c-142"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cbe4c-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="cbe4c-143">DLL</span><span class="sxs-lookup"><span data-stu-id="cbe4c-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cbe4c-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cbe4c-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cbe4c-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="cbe4c-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbe4c-146">**\_PACKAGEDCOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="cbe4c-146">**CIM\_PackagedComponent**</span></span>](cim-packagedcomponent.md)
</dt> <dt>

[<span data-ttu-id="cbe4c-147">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="cbe4c-147">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
