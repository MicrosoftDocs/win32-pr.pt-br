---
description: A \_ classe WMI de associação do Win32 ProgramGroupContents relaciona uma ordem de grupo de programas e um grupo de programas individual ou item contido nele.
ms.assetid: 687794d1-acc1-498a-9886-0c9ac762ebf4
ms.tgt_platform: multiple
title: Classe Win32_ProgramGroupContents
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ProgramGroupContents
- Win32_ProgramGroupContents.GroupComponent
- Win32_ProgramGroupContents.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5f77a61052357f7c67009ee7a89da018abeadda8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010122"
---
# <a name="win32_programgroupcontents-class"></a><span data-ttu-id="992e2-103">\_Classe Win32 ProgramGroupContents</span><span class="sxs-lookup"><span data-stu-id="992e2-103">Win32\_ProgramGroupContents class</span></span>

<span data-ttu-id="992e2-104">A [classe WMI](../wmisdk/retrieving-a-class.md) de associação do **Win32 \_ ProgramGroupContents** relaciona uma ordem de grupo de programas e um grupo de programas individual ou item contido nele.</span><span class="sxs-lookup"><span data-stu-id="992e2-104">The **Win32\_ProgramGroupContents** association [WMI class](../wmisdk/retrieving-a-class.md) relates a program group order and an individual program group or item contained in it.</span></span>

<span data-ttu-id="992e2-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="992e2-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="992e2-106">As propriedades e os métodos estão em ordem alfabética, não em ordem de MOF.</span><span class="sxs-lookup"><span data-stu-id="992e2-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="992e2-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="992e2-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{86E30E83-7DB2-11d2-90CB-0060081A46FD}"), AMENDMENT]
class Win32_ProgramGroupContents : CIM_Component
{
  Win32_LogicalProgramGroup REF GroupComponent;
  Win32_ProgramGroupOrItem  REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="992e2-108">Membros</span><span class="sxs-lookup"><span data-stu-id="992e2-108">Members</span></span>

<span data-ttu-id="992e2-109">A classe **Win32 \_ ProgramGroupContents** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="992e2-109">The **Win32\_ProgramGroupContents** class has these types of members:</span></span>

-   [<span data-ttu-id="992e2-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="992e2-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="992e2-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="992e2-111">Properties</span></span>

<span data-ttu-id="992e2-112">A classe **Win32 \_ ProgramGroupContents** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="992e2-112">The **Win32\_ProgramGroupContents** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="992e2-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="992e2-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="992e2-114">Tipo de dados: **Win32 \_ LogicalProgramGroup**</span><span class="sxs-lookup"><span data-stu-id="992e2-114">Data type: **Win32\_LogicalProgramGroup**</span></span>
</dt> <dt>

<span data-ttu-id="992e2-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="992e2-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="992e2-116">Qualificadores: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ LogicalProgramGroup")</span><span class="sxs-lookup"><span data-stu-id="992e2-116">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_LogicalProgramGroup")</span></span>
</dt> </dl>

<span data-ttu-id="992e2-117">Referência à instância que representa o grupo de programas lógico para essa associação.</span><span class="sxs-lookup"><span data-stu-id="992e2-117">Reference to the instance representing the logical program group for this association.</span></span>

</dd> <dt>

<span data-ttu-id="992e2-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="992e2-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="992e2-119">Tipo de dados: **Win32 \_ ProgramGroupOrItem**</span><span class="sxs-lookup"><span data-stu-id="992e2-119">Data type: **Win32\_ProgramGroupOrItem**</span></span>
</dt> <dt>

<span data-ttu-id="992e2-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="992e2-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="992e2-121">Qualificadores: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ ProgramGroupOrItem")</span><span class="sxs-lookup"><span data-stu-id="992e2-121">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_ProgramGroupOrItem")</span></span>
</dt> </dl>

<span data-ttu-id="992e2-122">Referência à instância que representa o grupo do menu **Iniciar** ou item para essa associação.</span><span class="sxs-lookup"><span data-stu-id="992e2-122">Reference to the instance representing the **Start** menu group or item for this association.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="992e2-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="992e2-123">Remarks</span></span>

<span data-ttu-id="992e2-124">A classe **Win32 \_ ProgramGroupContents** é derivada do [**\_ componente CIM**](cim-component.md).</span><span class="sxs-lookup"><span data-stu-id="992e2-124">The **Win32\_ProgramGroupContents** class is derived from [**CIM\_Component**](cim-component.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="992e2-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="992e2-125">Requirements</span></span>



| <span data-ttu-id="992e2-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="992e2-126">Requirement</span></span> | <span data-ttu-id="992e2-127">Valor</span><span class="sxs-lookup"><span data-stu-id="992e2-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="992e2-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="992e2-128">Minimum supported client</span></span><br/> | <span data-ttu-id="992e2-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="992e2-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="992e2-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="992e2-130">Minimum supported server</span></span><br/> | <span data-ttu-id="992e2-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="992e2-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="992e2-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="992e2-132">Namespace</span></span><br/>                | <span data-ttu-id="992e2-133">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="992e2-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="992e2-134">MOF</span><span class="sxs-lookup"><span data-stu-id="992e2-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="992e2-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="992e2-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="992e2-136">DLL</span><span class="sxs-lookup"><span data-stu-id="992e2-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="992e2-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="992e2-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="992e2-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="992e2-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="992e2-139">**\_Componente CIM**</span><span class="sxs-lookup"><span data-stu-id="992e2-139">**CIM\_Component**</span></span>](cim-component.md)
</dt> <dt>

[<span data-ttu-id="992e2-140">Classes do sistema operacional</span><span class="sxs-lookup"><span data-stu-id="992e2-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
