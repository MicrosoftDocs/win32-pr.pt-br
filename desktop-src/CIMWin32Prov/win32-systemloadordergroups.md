---
description: A \_ classe WMI de associação SystemLoadOrderGroups do Win32 relaciona um sistema de computador e um grupo de ordem de carregamento.
ms.assetid: fb637300-0f70-465a-a72b-f0ab3f246790
ms.tgt_platform: multiple
title: Classe Win32_SystemLoadOrderGroups
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemLoadOrderGroups
- Win32_SystemLoadOrderGroups.GroupComponent
- Win32_SystemLoadOrderGroups.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 510acfbde2f562493a454abe80a4f7788377e556
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105750946"
---
# <a name="win32_systemloadordergroups-class"></a><span data-ttu-id="bcbad-103">\_Classe Win32 SystemLoadOrderGroups</span><span class="sxs-lookup"><span data-stu-id="bcbad-103">Win32\_SystemLoadOrderGroups class</span></span>

<span data-ttu-id="bcbad-104">A [classe WMI](../wmisdk/retrieving-a-class.md) de associação **\_ SystemLoadOrderGroups do Win32** relaciona um sistema de computador e um grupo de ordem de carregamento.</span><span class="sxs-lookup"><span data-stu-id="bcbad-104">The **Win32\_SystemLoadOrderGroups** association [WMI class](../wmisdk/retrieving-a-class.md) relates a computer system and a load order group.</span></span>

<span data-ttu-id="bcbad-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="bcbad-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="bcbad-106">As propriedades e os métodos estão em ordem alfabética, não em ordem de MOF.</span><span class="sxs-lookup"><span data-stu-id="bcbad-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="bcbad-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bcbad-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C503-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemLoadOrderGroups : CIM_SystemComponent
{
  Win32_ComputerSystem REF GroupComponent;
  Win32_LoadOrderGroup REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="bcbad-108">Membros</span><span class="sxs-lookup"><span data-stu-id="bcbad-108">Members</span></span>

<span data-ttu-id="bcbad-109">A classe **Win32 \_ SystemLoadOrderGroups** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="bcbad-109">The **Win32\_SystemLoadOrderGroups** class has these types of members:</span></span>

-   [<span data-ttu-id="bcbad-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="bcbad-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bcbad-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="bcbad-111">Properties</span></span>

<span data-ttu-id="bcbad-112">A classe **Win32 \_ SystemLoadOrderGroups** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="bcbad-112">The **Win32\_SystemLoadOrderGroups** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bcbad-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="bcbad-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bcbad-114">Tipo de dados **: \_ sistema de ComputerSystem Win32**</span><span class="sxs-lookup"><span data-stu-id="bcbad-114">Data type: **Win32\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="bcbad-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bcbad-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bcbad-116">Qualificadores: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ ComputerSystem")</span><span class="sxs-lookup"><span data-stu-id="bcbad-116">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_ComputerSystem")</span></span>
</dt> </dl>

<span data-ttu-id="bcbad-117">Referência à instância que representa o sistema de computador no qual o grupo de ordem de carregamento existe.</span><span class="sxs-lookup"><span data-stu-id="bcbad-117">Reference to the instance representing the computer system where the load order group exists.</span></span>

</dd> <dt>

<span data-ttu-id="bcbad-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="bcbad-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bcbad-119">Tipo de dados: **Win32 \_ loadordergroup**</span><span class="sxs-lookup"><span data-stu-id="bcbad-119">Data type: **Win32\_LoadOrderGroup**</span></span>
</dt> <dt>

<span data-ttu-id="bcbad-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bcbad-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bcbad-121">Qualificadores: [**chave**](../wmisdk/key-qualifier.md), [**substituição**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ loadorder OrderGroup")</span><span class="sxs-lookup"><span data-stu-id="bcbad-121">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_LoadOrderGroup")</span></span>
</dt> </dl>

<span data-ttu-id="bcbad-122">Referência à instância que representa o grupo de ordem de carregamento existente no sistema de computador.</span><span class="sxs-lookup"><span data-stu-id="bcbad-122">Reference to the instance representing the load order group existing on the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bcbad-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="bcbad-123">Remarks</span></span>

<span data-ttu-id="bcbad-124">A classe **Win32 \_ SystemLoadOrderGroups** é derivada de [**CIM \_ Systemcomponent**](cim-systemcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="bcbad-124">The **Win32\_SystemLoadOrderGroups** class is derived from [**CIM\_SystemComponent**](cim-systemcomponent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bcbad-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bcbad-125">Requirements</span></span>



| <span data-ttu-id="bcbad-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="bcbad-126">Requirement</span></span> | <span data-ttu-id="bcbad-127">Valor</span><span class="sxs-lookup"><span data-stu-id="bcbad-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bcbad-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bcbad-128">Minimum supported client</span></span><br/> | <span data-ttu-id="bcbad-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bcbad-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="bcbad-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bcbad-130">Minimum supported server</span></span><br/> | <span data-ttu-id="bcbad-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bcbad-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="bcbad-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="bcbad-132">Namespace</span></span><br/>                | <span data-ttu-id="bcbad-133">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="bcbad-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="bcbad-134">MOF</span><span class="sxs-lookup"><span data-stu-id="bcbad-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bcbad-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bcbad-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="bcbad-136">DLL</span><span class="sxs-lookup"><span data-stu-id="bcbad-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bcbad-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bcbad-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bcbad-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="bcbad-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bcbad-139">**\_SYSTEMCOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="bcbad-139">**CIM\_SystemComponent**</span></span>](cim-systemcomponent.md)
</dt> <dt>

[<span data-ttu-id="bcbad-140">Classes do sistema operacional</span><span class="sxs-lookup"><span data-stu-id="bcbad-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
