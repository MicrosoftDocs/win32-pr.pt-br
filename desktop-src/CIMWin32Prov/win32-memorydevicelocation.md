---
description: A \_ classe WMI de associação MemoryDeviceLocation do Win32 relaciona um dispositivo de memória e a memória física na qual ele existe.
ms.assetid: 6fef916e-44e2-4b9f-94b7-c7204259004a
ms.tgt_platform: multiple
title: Classe Win32_MemoryDeviceLocation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_MemoryDeviceLocation
- Win32_MemoryDeviceLocation.Dependent
- Win32_MemoryDeviceLocation.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5cf1ba93a2574810892443aefa43e1c7c501636c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920211"
---
# <a name="win32_memorydevicelocation-class"></a><span data-ttu-id="0cf96-103">\_Classe Win32 MemoryDeviceLocation</span><span class="sxs-lookup"><span data-stu-id="0cf96-103">Win32\_MemoryDeviceLocation class</span></span>

<span data-ttu-id="0cf96-104">A [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) de associação **\_ MemoryDeviceLocation do Win32** relaciona um dispositivo de memória e a memória física na qual ele existe.</span><span class="sxs-lookup"><span data-stu-id="0cf96-104">The **Win32\_MemoryDeviceLocation** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a memory device and the physical memory on which it exists.</span></span>

<span data-ttu-id="0cf96-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="0cf96-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="0cf96-106">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="0cf96-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="0cf96-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0cf96-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{FAF76B9C-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class Win32_MemoryDeviceLocation : CIM_Realizes
{
  Win32_MemoryDevice   REF Dependent;
  Win32_PhysicalMemory REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="0cf96-108">Membros</span><span class="sxs-lookup"><span data-stu-id="0cf96-108">Members</span></span>

<span data-ttu-id="0cf96-109">A classe **Win32 \_ MemoryDeviceLocation** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="0cf96-109">The **Win32\_MemoryDeviceLocation** class has these types of members:</span></span>

-   [<span data-ttu-id="0cf96-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0cf96-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0cf96-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0cf96-111">Properties</span></span>

<span data-ttu-id="0cf96-112">A classe **Win32 \_ MemoryDeviceLocation** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="0cf96-112">The **Win32\_MemoryDeviceLocation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0cf96-113">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="0cf96-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0cf96-114">Tipo de dados: **Win32 \_ PhysicalMemory**</span><span class="sxs-lookup"><span data-stu-id="0cf96-114">Data type: **Win32\_PhysicalMemory**</span></span>
</dt> <dt>

<span data-ttu-id="0cf96-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0cf96-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0cf96-116">Qualificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ PhysicalMemory")</span><span class="sxs-lookup"><span data-stu-id="0cf96-116">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_PhysicalMemory")</span></span>
</dt> </dl>

<span data-ttu-id="0cf96-117">Um [**\_ PhysicalMemory Win32**](win32-physicalmemory.md) que representa a memória física que contém o dispositivo de memória.</span><span class="sxs-lookup"><span data-stu-id="0cf96-117">A [**Win32\_PhysicalMemory**](win32-physicalmemory.md) that represents the physical memory containing the memory device.</span></span>

</dd> <dt>

<span data-ttu-id="0cf96-118">**Depende**</span><span class="sxs-lookup"><span data-stu-id="0cf96-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0cf96-119">Tipo de dados: **Win32 \_ MemoryDevice**</span><span class="sxs-lookup"><span data-stu-id="0cf96-119">Data type: **Win32\_MemoryDevice**</span></span>
</dt> <dt>

<span data-ttu-id="0cf96-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0cf96-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0cf96-121">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**substituição**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ MemoryDevice")</span><span class="sxs-lookup"><span data-stu-id="0cf96-121">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_MemoryDevice")</span></span>
</dt> </dl>

<span data-ttu-id="0cf96-122">Um **\_ MemoryDeviceLocation Win32** que representa o dispositivo de memória existente na memória física.</span><span class="sxs-lookup"><span data-stu-id="0cf96-122">A **Win32\_MemoryDeviceLocation** that represents the memory device existing in the physical memory.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0cf96-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="0cf96-123">Remarks</span></span>

<span data-ttu-id="0cf96-124">A classe **Win32 \_ MemoryDeviceLocation** é derivada do [**CIM \_**](cim-realizes.md).</span><span class="sxs-lookup"><span data-stu-id="0cf96-124">The **Win32\_MemoryDeviceLocation** class is derived from [**CIM\_Realizes**](cim-realizes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0cf96-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0cf96-125">Requirements</span></span>



| <span data-ttu-id="0cf96-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="0cf96-126">Requirement</span></span> | <span data-ttu-id="0cf96-127">Valor</span><span class="sxs-lookup"><span data-stu-id="0cf96-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0cf96-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0cf96-128">Minimum supported client</span></span><br/> | <span data-ttu-id="0cf96-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0cf96-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0cf96-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0cf96-130">Minimum supported server</span></span><br/> | <span data-ttu-id="0cf96-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0cf96-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0cf96-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="0cf96-132">Namespace</span></span><br/>                | <span data-ttu-id="0cf96-133">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="0cf96-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0cf96-134">MOF</span><span class="sxs-lookup"><span data-stu-id="0cf96-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0cf96-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0cf96-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0cf96-136">DLL</span><span class="sxs-lookup"><span data-stu-id="0cf96-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0cf96-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0cf96-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0cf96-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="0cf96-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0cf96-139">**O CIM \_ percebe**</span><span class="sxs-lookup"><span data-stu-id="0cf96-139">**CIM\_Realizes**</span></span>](cim-realizes.md)
</dt> <dt>

[<span data-ttu-id="0cf96-140">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="0cf96-140">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

