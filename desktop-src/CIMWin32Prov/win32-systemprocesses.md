---
description: A \_ classe WMI de associação SystemProcesses do Win32 relaciona um sistema de computador e um processo em execução nesse sistema.
ms.assetid: 0d8c3ec6-265e-4486-8e94-f5acd2845cf5
ms.tgt_platform: multiple
title: Classe Win32_SystemProcesses
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemProcesses
- Win32_SystemProcesses.GroupComponent
- Win32_SystemProcesses.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1b963aea5d9c651e27dc4380200e40dd3dcb9a77
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010199"
---
# <a name="win32_systemprocesses-class"></a><span data-ttu-id="de4b6-103">\_Classe Win32 SystemProcesses</span><span class="sxs-lookup"><span data-stu-id="de4b6-103">Win32\_SystemProcesses class</span></span>

<span data-ttu-id="de4b6-104">A [classe WMI](../wmisdk/retrieving-a-class.md) de associação **\_ SystemProcesses do Win32** relaciona um sistema de computador e um processo em execução nesse sistema.</span><span class="sxs-lookup"><span data-stu-id="de4b6-104">The **Win32\_SystemProcesses** association [WMI class](../wmisdk/retrieving-a-class.md) relates a computer system and a process running on that system.</span></span>

<span data-ttu-id="de4b6-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="de4b6-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="de4b6-106">As propriedades e os métodos estão em ordem alfabética, não em ordem de MOF.</span><span class="sxs-lookup"><span data-stu-id="de4b6-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="de4b6-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="de4b6-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4F3-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemProcesses : CIM_SystemComponent
{
  Win32_ComputerSystem REF GroupComponent;
  Win32_Process        REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="de4b6-108">Membros</span><span class="sxs-lookup"><span data-stu-id="de4b6-108">Members</span></span>

<span data-ttu-id="de4b6-109">A classe **Win32 \_ SystemProcesses** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="de4b6-109">The **Win32\_SystemProcesses** class has these types of members:</span></span>

-   [<span data-ttu-id="de4b6-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="de4b6-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="de4b6-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="de4b6-111">Properties</span></span>

<span data-ttu-id="de4b6-112">A classe **Win32 \_ SystemProcesses** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="de4b6-112">The **Win32\_SystemProcesses** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="de4b6-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="de4b6-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de4b6-114">Tipo de dados **: \_ sistema de ComputerSystem Win32**</span><span class="sxs-lookup"><span data-stu-id="de4b6-114">Data type: **Win32\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="de4b6-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="de4b6-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="de4b6-116">Qualificadores: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ ComputerSystem")</span><span class="sxs-lookup"><span data-stu-id="de4b6-116">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_ComputerSystem")</span></span>
</dt> </dl>

<span data-ttu-id="de4b6-117">Referência à instância que representa o sistema de computador no qual o processo está em execução.</span><span class="sxs-lookup"><span data-stu-id="de4b6-117">Reference to the instance representing the computer system upon which the process is running.</span></span>

</dd> <dt>

<span data-ttu-id="de4b6-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="de4b6-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de4b6-119">Tipo de dados **: \_ processo Win32**</span><span class="sxs-lookup"><span data-stu-id="de4b6-119">Data type: **Win32\_Process**</span></span>
</dt> <dt>

<span data-ttu-id="de4b6-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="de4b6-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="de4b6-121">Qualificadores: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| processo WMI Win32 \_ ")</span><span class="sxs-lookup"><span data-stu-id="de4b6-121">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_Process")</span></span>
</dt> </dl>

<span data-ttu-id="de4b6-122">Referência à instância que representa o processo em execução no sistema de computador.</span><span class="sxs-lookup"><span data-stu-id="de4b6-122">Reference to the instance representing the process running on the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="de4b6-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="de4b6-123">Remarks</span></span>

<span data-ttu-id="de4b6-124">A classe **Win32 \_ SystemProcesses** é derivada de [**CIM \_ Systemcomponent**](cim-systemcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="de4b6-124">The **Win32\_SystemProcesses** class is derived from [**CIM\_SystemComponent**](cim-systemcomponent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="de4b6-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="de4b6-125">Requirements</span></span>



| <span data-ttu-id="de4b6-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="de4b6-126">Requirement</span></span> | <span data-ttu-id="de4b6-127">Valor</span><span class="sxs-lookup"><span data-stu-id="de4b6-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="de4b6-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="de4b6-128">Minimum supported client</span></span><br/> | <span data-ttu-id="de4b6-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="de4b6-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="de4b6-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="de4b6-130">Minimum supported server</span></span><br/> | <span data-ttu-id="de4b6-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="de4b6-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="de4b6-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="de4b6-132">Namespace</span></span><br/>                | <span data-ttu-id="de4b6-133">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="de4b6-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="de4b6-134">MOF</span><span class="sxs-lookup"><span data-stu-id="de4b6-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="de4b6-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="de4b6-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="de4b6-136">DLL</span><span class="sxs-lookup"><span data-stu-id="de4b6-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="de4b6-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="de4b6-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de4b6-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="de4b6-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de4b6-139">**\_SYSTEMCOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="de4b6-139">**CIM\_SystemComponent**</span></span>](cim-systemcomponent.md)
</dt> <dt>

[<span data-ttu-id="de4b6-140">Classes do sistema operacional</span><span class="sxs-lookup"><span data-stu-id="de4b6-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
