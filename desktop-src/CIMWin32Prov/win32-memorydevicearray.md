---
description: A \_ classe WMI de associação MemoryDeviceArray do Win32 relaciona um dispositivo de memória e a matriz de memória na qual ele reside.
ms.assetid: 39ea6333-2352-488b-99e4-97594bea7dcd
ms.tgt_platform: multiple
title: Classe Win32_MemoryDeviceArray
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_MemoryDeviceArray
- Win32_MemoryDeviceArray.GroupComponent
- Win32_MemoryDeviceArray.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1e527f77183c3bdc09d464f6fed4808e45adefa5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826178"
---
# <a name="win32_memorydevicearray-class"></a><span data-ttu-id="10595-103">\_Classe Win32 MemoryDeviceArray</span><span class="sxs-lookup"><span data-stu-id="10595-103">Win32\_MemoryDeviceArray class</span></span>

<span data-ttu-id="10595-104">A [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) de associação **\_ MemoryDeviceArray do Win32** relaciona um dispositivo de memória e a matriz de memória na qual ele reside.</span><span class="sxs-lookup"><span data-stu-id="10595-104">The **Win32\_MemoryDeviceArray** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a memory device and the memory array in which it resides.</span></span>

<span data-ttu-id="10595-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="10595-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="10595-106">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="10595-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="10595-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="10595-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{B24EF563-BBBE-11d2-ABFB-00805F538618}"), AMENDMENT]
class Win32_MemoryDeviceArray : CIM_Component
{
  Win32_MemoryArray  REF GroupComponent;
  Win32_MemoryDevice REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="10595-108">Membros</span><span class="sxs-lookup"><span data-stu-id="10595-108">Members</span></span>

<span data-ttu-id="10595-109">A classe **Win32 \_ MemoryDeviceArray** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="10595-109">The **Win32\_MemoryDeviceArray** class has these types of members:</span></span>

-   [<span data-ttu-id="10595-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="10595-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="10595-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="10595-111">Properties</span></span>

<span data-ttu-id="10595-112">A classe **Win32 \_ MemoryDeviceArray** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="10595-112">The **Win32\_MemoryDeviceArray** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="10595-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="10595-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10595-114">Tipo de dados: **Win32 \_ MemoryArray**</span><span class="sxs-lookup"><span data-stu-id="10595-114">Data type: **Win32\_MemoryArray**</span></span>
</dt> <dt>

<span data-ttu-id="10595-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="10595-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10595-116">Qualificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ MemoryArray")</span><span class="sxs-lookup"><span data-stu-id="10595-116">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_MemoryArray")</span></span>
</dt> </dl>

<span data-ttu-id="10595-117">Um [**\_ MemoryArray Win32**](win32-memoryarray.md) que representa a parte da matriz de memória da \_ Associação Win32 MemoryDeviceArray.</span><span class="sxs-lookup"><span data-stu-id="10595-117">A [**Win32\_MemoryArray**](win32-memoryarray.md) that represents the memory array part of the Win32\_MemoryDeviceArray association.</span></span>

</dd> <dt>

<span data-ttu-id="10595-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="10595-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10595-119">Tipo de dados: **Win32 \_ MemoryDevice**</span><span class="sxs-lookup"><span data-stu-id="10595-119">Data type: **Win32\_MemoryDevice**</span></span>
</dt> <dt>

<span data-ttu-id="10595-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="10595-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10595-121">Qualificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ MemoryDevice")</span><span class="sxs-lookup"><span data-stu-id="10595-121">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_MemoryDevice")</span></span>
</dt> </dl>

<span data-ttu-id="10595-122">Um [**\_ MemoryDevice Win32**](win32-memorydevice.md) que representa uma parte do dispositivo de memória da \_ Associação Win32 MemoryDeviceArray.</span><span class="sxs-lookup"><span data-stu-id="10595-122">A [**Win32\_MemoryDevice**](win32-memorydevice.md) that represents a memory device part of the Win32\_MemoryDeviceArray association.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="10595-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="10595-123">Remarks</span></span>

<span data-ttu-id="10595-124">A classe **Win32 \_ MemoryDeviceArray** é derivada do [**\_ componente CIM**](cim-component.md).</span><span class="sxs-lookup"><span data-stu-id="10595-124">The **Win32\_MemoryDeviceArray** class is derived from [**CIM\_Component**](cim-component.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="10595-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="10595-125">Requirements</span></span>



| <span data-ttu-id="10595-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="10595-126">Requirement</span></span> | <span data-ttu-id="10595-127">Valor</span><span class="sxs-lookup"><span data-stu-id="10595-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="10595-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="10595-128">Minimum supported client</span></span><br/> | <span data-ttu-id="10595-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="10595-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="10595-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="10595-130">Minimum supported server</span></span><br/> | <span data-ttu-id="10595-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="10595-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="10595-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="10595-132">Namespace</span></span><br/>                | <span data-ttu-id="10595-133">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="10595-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="10595-134">MOF</span><span class="sxs-lookup"><span data-stu-id="10595-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="10595-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="10595-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="10595-136">DLL</span><span class="sxs-lookup"><span data-stu-id="10595-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="10595-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="10595-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10595-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="10595-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10595-139">**\_Componente CIM**</span><span class="sxs-lookup"><span data-stu-id="10595-139">**CIM\_Component**</span></span>](cim-component.md)
</dt> <dt>

[<span data-ttu-id="10595-140">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="10595-140">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

