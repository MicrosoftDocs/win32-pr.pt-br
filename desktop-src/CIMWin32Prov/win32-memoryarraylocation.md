---
description: A \_ classe WMI de associação do Win32 MemoryArrayLocation relaciona uma matriz de memória lógica e a matriz de memória física na qual ela existe.
ms.assetid: 455daeee-ad67-4599-84d6-fa3f4ac593aa
ms.tgt_platform: multiple
title: Classe Win32_MemoryArrayLocation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_MemoryArrayLocation
- Win32_MemoryArrayLocation.Dependent
- Win32_MemoryArrayLocation.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 62aae3bf672b12bdb947ff8ce6b76f919eaa11b7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501063"
---
# <a name="win32_memoryarraylocation-class"></a><span data-ttu-id="a0d31-103">\_Classe Win32 MemoryArrayLocation</span><span class="sxs-lookup"><span data-stu-id="a0d31-103">Win32\_MemoryArrayLocation class</span></span>

<span data-ttu-id="a0d31-104">A [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) de associação do **Win32 \_ MemoryArrayLocation** relaciona uma matriz de memória lógica e a matriz de memória física na qual ela existe.</span><span class="sxs-lookup"><span data-stu-id="a0d31-104">The **Win32\_MemoryArrayLocation** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a logical memory array and the physical memory array on which it exists.</span></span>

<span data-ttu-id="a0d31-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="a0d31-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="a0d31-106">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="a0d31-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0d31-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a0d31-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{B24EF561-BBBE-11d2-ABFB-00805F538618}"), AMENDMENT]
class Win32_MemoryArrayLocation : CIM_Realizes
{
  Win32_MemoryArray         REF Dependent;
  Win32_PhysicalMemoryArray REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="a0d31-108">Membros</span><span class="sxs-lookup"><span data-stu-id="a0d31-108">Members</span></span>

<span data-ttu-id="a0d31-109">A classe **Win32 \_ MemoryArrayLocation** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="a0d31-109">The **Win32\_MemoryArrayLocation** class has these types of members:</span></span>

-   [<span data-ttu-id="a0d31-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a0d31-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a0d31-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a0d31-111">Properties</span></span>

<span data-ttu-id="a0d31-112">A classe **Win32 \_ MemoryArrayLocation** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="a0d31-112">The **Win32\_MemoryArrayLocation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a0d31-113">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="a0d31-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0d31-114">Tipo de dados: **Win32 \_ PhysicalMemoryArray**</span><span class="sxs-lookup"><span data-stu-id="a0d31-114">Data type: **Win32\_PhysicalMemoryArray**</span></span>
</dt> <dt>

<span data-ttu-id="a0d31-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a0d31-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0d31-116">Qualificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ PhysicalMemoryArray")</span><span class="sxs-lookup"><span data-stu-id="a0d31-116">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_PhysicalMemoryArray")</span></span>
</dt> </dl>

<span data-ttu-id="a0d31-117">Um [**\_ PhysicalMemoryArray Win32**](win32-physicalmemoryarray.md) que descreve a matriz de memória física que implementa a matriz de memória lógica.</span><span class="sxs-lookup"><span data-stu-id="a0d31-117">A [**Win32\_PhysicalMemoryArray**](win32-physicalmemoryarray.md) that describes the physical memory array that implements the logical memory array.</span></span>

</dd> <dt>

<span data-ttu-id="a0d31-118">**Depende**</span><span class="sxs-lookup"><span data-stu-id="a0d31-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0d31-119">Tipo de dados: **Win32 \_ MemoryArray**</span><span class="sxs-lookup"><span data-stu-id="a0d31-119">Data type: **Win32\_MemoryArray**</span></span>
</dt> <dt>

<span data-ttu-id="a0d31-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a0d31-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0d31-121">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**substituição**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ MemoryArray")</span><span class="sxs-lookup"><span data-stu-id="a0d31-121">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_MemoryArray")</span></span>
</dt> </dl>

<span data-ttu-id="a0d31-122">Um [**\_ MemoryArray Win32**](win32-memoryarray.md) que descreve a matriz de memória lógica implementada pela matriz de memória física.</span><span class="sxs-lookup"><span data-stu-id="a0d31-122">A [**Win32\_MemoryArray**](win32-memoryarray.md) that describes the logical memory array implemented by the physical memory array.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a0d31-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="a0d31-123">Remarks</span></span>

<span data-ttu-id="a0d31-124">A classe **Win32 \_ MemoryArrayLocation** é derivada do [**CIM \_**](cim-realizes.md).</span><span class="sxs-lookup"><span data-stu-id="a0d31-124">The **Win32\_MemoryArrayLocation** class is derived from [**CIM\_Realizes**](cim-realizes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a0d31-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a0d31-125">Requirements</span></span>



| <span data-ttu-id="a0d31-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0d31-126">Requirement</span></span> | <span data-ttu-id="a0d31-127">Valor</span><span class="sxs-lookup"><span data-stu-id="a0d31-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a0d31-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a0d31-128">Minimum supported client</span></span><br/> | <span data-ttu-id="a0d31-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a0d31-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a0d31-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a0d31-130">Minimum supported server</span></span><br/> | <span data-ttu-id="a0d31-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a0d31-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a0d31-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="a0d31-132">Namespace</span></span><br/>                | <span data-ttu-id="a0d31-133">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="a0d31-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a0d31-134">MOF</span><span class="sxs-lookup"><span data-stu-id="a0d31-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a0d31-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a0d31-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a0d31-136">DLL</span><span class="sxs-lookup"><span data-stu-id="a0d31-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a0d31-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a0d31-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0d31-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="a0d31-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0d31-139">**O CIM \_ percebe**</span><span class="sxs-lookup"><span data-stu-id="a0d31-139">**CIM\_Realizes**</span></span>](cim-realizes.md)
</dt> <dt>

[<span data-ttu-id="a0d31-140">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="a0d31-140">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

