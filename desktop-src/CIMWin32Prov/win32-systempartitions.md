---
description: A \_ classe WMI de associação SystemPartitions do Win32 relaciona um sistema de computador e uma partição de disco nesse sistema.
ms.assetid: e8f02cd0-9446-4258-b476-5dc6c72c80d4
ms.tgt_platform: multiple
title: Classe Win32_SystemPartitions
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemPartitions
- Win32_SystemPartitions.GroupComponent
- Win32_SystemPartitions.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: deae8129772e5d854f05b5b953ec66a12bd5bcaf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826411"
---
# <a name="win32_systempartitions-class"></a><span data-ttu-id="665be-103">\_Classe Win32 SystemPartitions</span><span class="sxs-lookup"><span data-stu-id="665be-103">Win32\_SystemPartitions class</span></span>

<span data-ttu-id="665be-104">A [classe WMI](../wmisdk/retrieving-a-class.md) de associação **\_ SystemPartitions do Win32** relaciona um sistema de computador e uma partição de disco nesse sistema.</span><span class="sxs-lookup"><span data-stu-id="665be-104">The **Win32\_SystemPartitions** association [WMI class](../wmisdk/retrieving-a-class.md) relates a computer system and a disk partition on that system.</span></span>

<span data-ttu-id="665be-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="665be-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="665be-106">As propriedades e os métodos estão em ordem alfabética, não em ordem de MOF.</span><span class="sxs-lookup"><span data-stu-id="665be-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="665be-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="665be-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4F5-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemPartitions : Win32_SystemDevices
{
  Win32_ComputerSystem REF GroupComponent;
  Win32_DiskPartition  REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="665be-108">Membros</span><span class="sxs-lookup"><span data-stu-id="665be-108">Members</span></span>

<span data-ttu-id="665be-109">A classe **Win32 \_ SystemPartitions** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="665be-109">The **Win32\_SystemPartitions** class has these types of members:</span></span>

-   [<span data-ttu-id="665be-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="665be-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="665be-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="665be-111">Properties</span></span>

<span data-ttu-id="665be-112">A classe **Win32 \_ SystemPartitions** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="665be-112">The **Win32\_SystemPartitions** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="665be-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="665be-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="665be-114">Tipo de dados **: \_ sistema de ComputerSystem Win32**</span><span class="sxs-lookup"><span data-stu-id="665be-114">Data type: **Win32\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="665be-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="665be-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="665be-116">Qualificadores: [**override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ ComputerSystem")</span><span class="sxs-lookup"><span data-stu-id="665be-116">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_ComputerSystem")</span></span>
</dt> </dl>

<span data-ttu-id="665be-117">Referência à instância que representa as propriedades do sistema de computador onde a partição de disco está localizada.</span><span class="sxs-lookup"><span data-stu-id="665be-117">Reference to the instance representing the properties of the computer system where the disk partition is located.</span></span>

</dd> <dt>

<span data-ttu-id="665be-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="665be-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="665be-119">Tipo de dados: **Win32 \_ DiskPartition**</span><span class="sxs-lookup"><span data-stu-id="665be-119">Data type: **Win32\_DiskPartition**</span></span>
</dt> <dt>

<span data-ttu-id="665be-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="665be-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="665be-121">Qualificadores: [**override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ DiskPartition")</span><span class="sxs-lookup"><span data-stu-id="665be-121">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_DiskPartition")</span></span>
</dt> </dl>

<span data-ttu-id="665be-122">Referência à instância que representa as propriedades de uma partição de disco que existe no sistema de computador.</span><span class="sxs-lookup"><span data-stu-id="665be-122">Reference to the instance representing the properties of a disk partition that exists on the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="665be-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="665be-123">Remarks</span></span>

<span data-ttu-id="665be-124">A classe **Win32 \_ SystemPartitions** é derivada de [**Win32 \_ SystemDevices**](win32-systemdevices.md).</span><span class="sxs-lookup"><span data-stu-id="665be-124">The **Win32\_SystemPartitions** class is derived from [**Win32\_SystemDevices**](win32-systemdevices.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="665be-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="665be-125">Requirements</span></span>



| <span data-ttu-id="665be-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="665be-126">Requirement</span></span> | <span data-ttu-id="665be-127">Valor</span><span class="sxs-lookup"><span data-stu-id="665be-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="665be-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="665be-128">Minimum supported client</span></span><br/> | <span data-ttu-id="665be-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="665be-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="665be-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="665be-130">Minimum supported server</span></span><br/> | <span data-ttu-id="665be-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="665be-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="665be-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="665be-132">Namespace</span></span><br/>                | <span data-ttu-id="665be-133">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="665be-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="665be-134">MOF</span><span class="sxs-lookup"><span data-stu-id="665be-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="665be-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="665be-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="665be-136">DLL</span><span class="sxs-lookup"><span data-stu-id="665be-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="665be-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="665be-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="665be-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="665be-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="665be-139">**\_SystemDevices Win32**</span><span class="sxs-lookup"><span data-stu-id="665be-139">**Win32\_SystemDevices**</span></span>](win32-systemdevices.md)
</dt> <dt>

[<span data-ttu-id="665be-140">Classes do sistema operacional</span><span class="sxs-lookup"><span data-stu-id="665be-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
