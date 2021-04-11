---
description: A \_ classe WMI de associação SystemOperatingSystem do Win32 relaciona um sistema de computador e seu sistema operacional.
ms.assetid: dc71f80b-6fbd-4bc8-8783-3922d8050518
ms.tgt_platform: multiple
title: Classe Win32_SystemOperatingSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemOperatingSystem
- Win32_SystemOperatingSystem.PrimaryOS
- Win32_SystemOperatingSystem.GroupComponent
- Win32_SystemOperatingSystem.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ba3f8ac94ec882ee1df96da51d93d2c24fde9b3f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089601"
---
# <a name="win32_systemoperatingsystem-class"></a><span data-ttu-id="a9ea7-103">\_Classe Win32 SystemOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="a9ea7-103">Win32\_SystemOperatingSystem class</span></span>

<span data-ttu-id="a9ea7-104">A [classe WMI](../wmisdk/retrieving-a-class.md) de associação **\_ SystemOperatingSystem do Win32** relaciona um sistema de computador e seu sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="a9ea7-104">The **Win32\_SystemOperatingSystem** association [WMI class](../wmisdk/retrieving-a-class.md) relates a computer system and its operating system.</span></span>

<span data-ttu-id="a9ea7-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="a9ea7-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="a9ea7-106">As propriedades e os métodos estão em ordem alfabética, não em ordem de MOF.</span><span class="sxs-lookup"><span data-stu-id="a9ea7-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9ea7-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a9ea7-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4F0-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemOperatingSystem : CIM_InstalledOS
{
  boolean                   PrimaryOS;
  Win32_ComputerSystem  REF GroupComponent;
  Win32_OperatingSystem REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="a9ea7-108">Membros</span><span class="sxs-lookup"><span data-stu-id="a9ea7-108">Members</span></span>

<span data-ttu-id="a9ea7-109">A classe **Win32 \_ SystemOperatingSystem** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="a9ea7-109">The **Win32\_SystemOperatingSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="a9ea7-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a9ea7-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a9ea7-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a9ea7-111">Properties</span></span>

<span data-ttu-id="a9ea7-112">A classe **Win32 \_ SystemOperatingSystem** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="a9ea7-112">The **Win32\_SystemOperatingSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a9ea7-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="a9ea7-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9ea7-114">Tipo de dados **: \_ sistema de ComputerSystem Win32**</span><span class="sxs-lookup"><span data-stu-id="a9ea7-114">Data type: **Win32\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="a9ea7-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a9ea7-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9ea7-116">Qualificadores: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ ComputerSystem")</span><span class="sxs-lookup"><span data-stu-id="a9ea7-116">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_ComputerSystem")</span></span>
</dt> </dl>

<span data-ttu-id="a9ea7-117">Um sistema de computadores [**Win32 \_**](win32-computersystemprocessor.md) que descreve as propriedades do sistema de computador no qual o sistema operacional está instalado.</span><span class="sxs-lookup"><span data-stu-id="a9ea7-117">A [**Win32\_ComputerSystem**](win32-computersystemprocessor.md) that describes the properties of the computer system upon which the operating system is installed.</span></span>

</dd> <dt>

<span data-ttu-id="a9ea7-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="a9ea7-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9ea7-119">Tipo de dados: sistema **\_ operacional Win32**</span><span class="sxs-lookup"><span data-stu-id="a9ea7-119">Data type: **Win32\_OperatingSystem**</span></span>
</dt> <dt>

<span data-ttu-id="a9ea7-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a9ea7-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9ea7-121">Qualificadores: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ OperatingSystem")</span><span class="sxs-lookup"><span data-stu-id="a9ea7-121">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_OperatingSystem")</span></span>
</dt> </dl>

<span data-ttu-id="a9ea7-122">Um [**\_ OperatingSystem do Win32**](win32-operatingsystem.md) que descreve as propriedades do sistema operacional em execução neste sistema de computador.</span><span class="sxs-lookup"><span data-stu-id="a9ea7-122">A [**Win32\_OperatingSystem**](win32-operatingsystem.md) that describes properties of the operating system running on this computer system.</span></span>

</dd> <dt>

<span data-ttu-id="a9ea7-123">**PrimaryOS**</span><span class="sxs-lookup"><span data-stu-id="a9ea7-123">**PrimaryOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9ea7-124">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="a9ea7-124">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a9ea7-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a9ea7-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9ea7-126">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Sistema operacional DMTF \| 1,4 ")</span><span class="sxs-lookup"><span data-stu-id="a9ea7-126">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operating System\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="a9ea7-127">Se for **true**, o sistema operacional instalado será o sistema operacional padrão do sistema de computador.</span><span class="sxs-lookup"><span data-stu-id="a9ea7-127">If **TRUE**, the installed operating system is the default operating system for the computer system.</span></span>

<span data-ttu-id="a9ea7-128">Essa propriedade é herdada do [**CIM \_ InstalledOS**](cim-installedos.md).</span><span class="sxs-lookup"><span data-stu-id="a9ea7-128">This property is inherited from [**CIM\_InstalledOS**](cim-installedos.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a9ea7-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="a9ea7-129">Remarks</span></span>

<span data-ttu-id="a9ea7-130">A classe **Win32 \_ SystemOperatingSystem** é derivada de [**CIM \_ InstalledOS**](cim-installedos.md).</span><span class="sxs-lookup"><span data-stu-id="a9ea7-130">The **Win32\_SystemOperatingSystem** class is derived from [**CIM\_InstalledOS**](cim-installedos.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a9ea7-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a9ea7-131">Requirements</span></span>



| <span data-ttu-id="a9ea7-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="a9ea7-132">Requirement</span></span> | <span data-ttu-id="a9ea7-133">Valor</span><span class="sxs-lookup"><span data-stu-id="a9ea7-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a9ea7-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a9ea7-134">Minimum supported client</span></span><br/> | <span data-ttu-id="a9ea7-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a9ea7-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a9ea7-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a9ea7-136">Minimum supported server</span></span><br/> | <span data-ttu-id="a9ea7-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a9ea7-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a9ea7-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="a9ea7-138">Namespace</span></span><br/>                | <span data-ttu-id="a9ea7-139">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="a9ea7-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a9ea7-140">MOF</span><span class="sxs-lookup"><span data-stu-id="a9ea7-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a9ea7-141"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a9ea7-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a9ea7-142">DLL</span><span class="sxs-lookup"><span data-stu-id="a9ea7-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a9ea7-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a9ea7-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9ea7-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="a9ea7-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9ea7-145">**\_INSTALLEDOS CIM**</span><span class="sxs-lookup"><span data-stu-id="a9ea7-145">**CIM\_InstalledOS**</span></span>](cim-installedos.md)
</dt> <dt>

[<span data-ttu-id="a9ea7-146">Classes do sistema operacional</span><span class="sxs-lookup"><span data-stu-id="a9ea7-146">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
