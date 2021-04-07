---
description: A \_ classe WMI de associação SystemResources do Win32 relaciona um recurso do sistema e o sistema de computador no qual ele reside.
ms.assetid: 90bff0b0-7c1d-44bf-b67e-aefeaa4b4a83
ms.tgt_platform: multiple
title: Classe Win32_SystemResources
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemResources
- Win32_SystemResources.GroupComponent
- Win32_SystemResources.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: fe96467e4bc609fa9426edd3c977b5596ea95fe7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920357"
---
# <a name="win32_systemresources-class"></a><span data-ttu-id="16f73-103">\_Classe Win32 SystemResources</span><span class="sxs-lookup"><span data-stu-id="16f73-103">Win32\_SystemResources class</span></span>

<span data-ttu-id="16f73-104">A [classe WMI](../wmisdk/retrieving-a-class.md) de associação **\_ SystemResources do Win32** relaciona um recurso do sistema e o sistema de computador no qual ele reside.</span><span class="sxs-lookup"><span data-stu-id="16f73-104">The **Win32\_SystemResources** association [WMI class](../wmisdk/retrieving-a-class.md) relates a system resource and the computer system it resides on.</span></span>

<span data-ttu-id="16f73-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="16f73-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="16f73-106">As propriedades e os métodos estão em ordem alfabética, não em ordem de MOF.</span><span class="sxs-lookup"><span data-stu-id="16f73-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="16f73-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="16f73-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4F8-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemResources : CIM_ComputerSystemResource
{
  Win32_ComputerSystem REF GroupComponent;
  CIM_SystemResource   REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="16f73-108">Membros</span><span class="sxs-lookup"><span data-stu-id="16f73-108">Members</span></span>

<span data-ttu-id="16f73-109">A classe **Win32 \_ SystemResources** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="16f73-109">The **Win32\_SystemResources** class has these types of members:</span></span>

-   [<span data-ttu-id="16f73-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="16f73-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="16f73-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="16f73-111">Properties</span></span>

<span data-ttu-id="16f73-112">A classe **Win32 \_ SystemResources** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="16f73-112">The **Win32\_SystemResources** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="16f73-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="16f73-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16f73-114">Tipo de dados **: \_ sistema de ComputerSystem Win32**</span><span class="sxs-lookup"><span data-stu-id="16f73-114">Data type: **Win32\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="16f73-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="16f73-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="16f73-116">Qualificadores: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ ComputerSystem")</span><span class="sxs-lookup"><span data-stu-id="16f73-116">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_ComputerSystem")</span></span>
</dt> </dl>

<span data-ttu-id="16f73-117">Referência à instância que representa o sistema de computador no qual o recurso está localizado.</span><span class="sxs-lookup"><span data-stu-id="16f73-117">Reference to the instance representing the computer system where the resource is located.</span></span>

</dd> <dt>

<span data-ttu-id="16f73-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="16f73-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16f73-119">Tipo de dados: **CIM \_ SystemResource**</span><span class="sxs-lookup"><span data-stu-id="16f73-119">Data type: **CIM\_SystemResource**</span></span>
</dt> <dt>

<span data-ttu-id="16f73-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="16f73-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="16f73-121">Qualificadores: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM \| CIM \_ SystemResource")</span><span class="sxs-lookup"><span data-stu-id="16f73-121">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM\|CIM\_SystemResource")</span></span>
</dt> </dl>

<span data-ttu-id="16f73-122">Referência à instância que representa o recurso (como serviços de e/s e recursos de memória) disponíveis no sistema de computador.</span><span class="sxs-lookup"><span data-stu-id="16f73-122">Reference to the instance representing the resource (such as I/O services and memory resources) available on the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="16f73-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="16f73-123">Remarks</span></span>

<span data-ttu-id="16f73-124">A classe **Win32 \_ SystemResources** é derivada de [**CIM \_ ComputerSystemResource**](cim-computersystemresource.md).</span><span class="sxs-lookup"><span data-stu-id="16f73-124">The **Win32\_SystemResources** class is derived from [**CIM\_ComputerSystemResource**](cim-computersystemresource.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="16f73-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="16f73-125">Requirements</span></span>



| <span data-ttu-id="16f73-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="16f73-126">Requirement</span></span> | <span data-ttu-id="16f73-127">Valor</span><span class="sxs-lookup"><span data-stu-id="16f73-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="16f73-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="16f73-128">Minimum supported client</span></span><br/> | <span data-ttu-id="16f73-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="16f73-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="16f73-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="16f73-130">Minimum supported server</span></span><br/> | <span data-ttu-id="16f73-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="16f73-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="16f73-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="16f73-132">Namespace</span></span><br/>                | <span data-ttu-id="16f73-133">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="16f73-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="16f73-134">MOF</span><span class="sxs-lookup"><span data-stu-id="16f73-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="16f73-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="16f73-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="16f73-136">DLL</span><span class="sxs-lookup"><span data-stu-id="16f73-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="16f73-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="16f73-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16f73-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="16f73-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16f73-139">**\_COMPUTERSYSTEMRESOURCE CIM**</span><span class="sxs-lookup"><span data-stu-id="16f73-139">**CIM\_ComputerSystemResource**</span></span>](cim-computersystemresource.md)
</dt> <dt>

[<span data-ttu-id="16f73-140">Classes do sistema operacional</span><span class="sxs-lookup"><span data-stu-id="16f73-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
