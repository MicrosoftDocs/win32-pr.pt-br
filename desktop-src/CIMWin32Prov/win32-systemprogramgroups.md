---
description: A \_ classe WMI de associação SystemProgramGroups do Win32 relaciona um sistema de computador e um grupo de programas lógico.
ms.assetid: cbf810c8-a967-4d60-889c-e47c43b039ea
ms.tgt_platform: multiple
title: Classe Win32_SystemProgramGroups
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemProgramGroups
- Win32_SystemProgramGroups.Element
- Win32_SystemProgramGroups.Setting
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1a8ca556c24295e2c4b04ab851610ef35ec9b715
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089594"
---
# <a name="win32_systemprogramgroups-class"></a><span data-ttu-id="1407c-103">\_Classe Win32 SystemProgramGroups</span><span class="sxs-lookup"><span data-stu-id="1407c-103">Win32\_SystemProgramGroups class</span></span>

<span data-ttu-id="1407c-104">A [classe WMI](../wmisdk/retrieving-a-class.md) de associação **\_ SystemProgramGroups do Win32** relaciona um sistema de computador e um grupo de programas lógico.</span><span class="sxs-lookup"><span data-stu-id="1407c-104">The **Win32\_SystemProgramGroups** association [WMI class](../wmisdk/retrieving-a-class.md) relates a computer system and a logical program group.</span></span>

<span data-ttu-id="1407c-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="1407c-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="1407c-106">As propriedades e os métodos estão em ordem alfabética, não em ordem de MOF.</span><span class="sxs-lookup"><span data-stu-id="1407c-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="1407c-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1407c-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C505-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemProgramGroups : Win32_SystemSetting
{
  Win32_ComputerSystem      REF Element;
  Win32_LogicalProgramGroup REF Setting;
};
```

## <a name="members"></a><span data-ttu-id="1407c-108">Membros</span><span class="sxs-lookup"><span data-stu-id="1407c-108">Members</span></span>

<span data-ttu-id="1407c-109">A classe **Win32 \_ SystemProgramGroups** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="1407c-109">The **Win32\_SystemProgramGroups** class has these types of members:</span></span>

-   [<span data-ttu-id="1407c-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1407c-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1407c-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1407c-111">Properties</span></span>

<span data-ttu-id="1407c-112">A classe **Win32 \_ SystemProgramGroups** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="1407c-112">The **Win32\_SystemProgramGroups** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1407c-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="1407c-113">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1407c-114">Tipo de dados **: \_ sistema de ComputerSystem Win32**</span><span class="sxs-lookup"><span data-stu-id="1407c-114">Data type: **Win32\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="1407c-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1407c-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1407c-116">Qualificadores: [**override**](../wmisdk/standard-qualifiers.md) ("element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ ComputerSystem")</span><span class="sxs-lookup"><span data-stu-id="1407c-116">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_ComputerSystem")</span></span>
</dt> </dl>

<span data-ttu-id="1407c-117">Referência à instância que representa o sistema de computador que contém o grupo de programas lógicos.</span><span class="sxs-lookup"><span data-stu-id="1407c-117">Reference to the instance representing the computer system containing the logical program group.</span></span>

</dd> <dt>

<span data-ttu-id="1407c-118">**Configuração**</span><span class="sxs-lookup"><span data-stu-id="1407c-118">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1407c-119">Tipo de dados: **Win32 \_ LogicalProgramGroup**</span><span class="sxs-lookup"><span data-stu-id="1407c-119">Data type: **Win32\_LogicalProgramGroup**</span></span>
</dt> <dt>

<span data-ttu-id="1407c-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1407c-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1407c-121">Qualificadores: [**override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ LogicalProgramGroup")</span><span class="sxs-lookup"><span data-stu-id="1407c-121">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_LogicalProgramGroup")</span></span>
</dt> </dl>

<span data-ttu-id="1407c-122">Referência à instância que representa o grupo de programas lógicos no sistema de computador.</span><span class="sxs-lookup"><span data-stu-id="1407c-122">Reference to the instance representing the logical program group on the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1407c-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="1407c-123">Remarks</span></span>

<span data-ttu-id="1407c-124">A classe **Win32 \_ SystemProgramGroups** é derivada de [**Win32 \_ SystemSetting**](win32-systemsetting.md).</span><span class="sxs-lookup"><span data-stu-id="1407c-124">The **Win32\_SystemProgramGroups** class is derived from [**Win32\_SystemSetting**](win32-systemsetting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1407c-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1407c-125">Requirements</span></span>



| <span data-ttu-id="1407c-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="1407c-126">Requirement</span></span> | <span data-ttu-id="1407c-127">Valor</span><span class="sxs-lookup"><span data-stu-id="1407c-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1407c-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1407c-128">Minimum supported client</span></span><br/> | <span data-ttu-id="1407c-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1407c-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1407c-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1407c-130">Minimum supported server</span></span><br/> | <span data-ttu-id="1407c-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1407c-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1407c-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="1407c-132">Namespace</span></span><br/>                | <span data-ttu-id="1407c-133">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="1407c-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1407c-134">MOF</span><span class="sxs-lookup"><span data-stu-id="1407c-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1407c-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1407c-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1407c-136">DLL</span><span class="sxs-lookup"><span data-stu-id="1407c-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1407c-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1407c-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1407c-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="1407c-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1407c-139">**\_SystemSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="1407c-139">**Win32\_SystemSetting**</span></span>](win32-systemsetting.md)
</dt> <dt>

[<span data-ttu-id="1407c-140">Classes do sistema operacional</span><span class="sxs-lookup"><span data-stu-id="1407c-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
