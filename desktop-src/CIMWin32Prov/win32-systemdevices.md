---
description: A \_ classe WMI de associação SystemDevices do Win32 relaciona um sistema de computador e um dispositivo lógico instalado nesse sistema.
ms.assetid: 84dfcb75-3b44-4b27-8eee-779be522eb1f
ms.tgt_platform: multiple
title: Classe Win32_SystemDevices
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDevices
- Win32_SystemDevices.GroupComponent
- Win32_SystemDevices.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b2b28c11e10318e3bca562baf93bc20df9b756cf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826616"
---
# <a name="win32_systemdevices-class"></a><span data-ttu-id="b33a5-103">\_Classe Win32 SystemDevices</span><span class="sxs-lookup"><span data-stu-id="b33a5-103">Win32\_SystemDevices class</span></span>

<span data-ttu-id="b33a5-104">A [classe WMI](../wmisdk/retrieving-a-class.md) de associação **\_ SystemDevices do Win32** relaciona um sistema de computador e um dispositivo lógico instalado nesse sistema.</span><span class="sxs-lookup"><span data-stu-id="b33a5-104">The **Win32\_SystemDevices** association [WMI class](../wmisdk/retrieving-a-class.md) relates a computer system and a logical device installed on that system.</span></span>

<span data-ttu-id="b33a5-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="b33a5-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="b33a5-106">As propriedades e os métodos estão em ordem alfabética, não em ordem de MOF.</span><span class="sxs-lookup"><span data-stu-id="b33a5-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b33a5-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b33a5-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4F4-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemDevices : CIM_SystemDevice
{
  Win32_ComputerSystem REF GroupComponent;
  CIM_LogicalDevice    REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="b33a5-108">Membros</span><span class="sxs-lookup"><span data-stu-id="b33a5-108">Members</span></span>

<span data-ttu-id="b33a5-109">A classe **Win32 \_ SystemDevices** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="b33a5-109">The **Win32\_SystemDevices** class has these types of members:</span></span>

-   [<span data-ttu-id="b33a5-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b33a5-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b33a5-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b33a5-111">Properties</span></span>

<span data-ttu-id="b33a5-112">A classe **Win32 \_ SystemDevices** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="b33a5-112">The **Win32\_SystemDevices** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b33a5-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="b33a5-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b33a5-114">Tipo de dados **: \_ sistema de ComputerSystem Win32**</span><span class="sxs-lookup"><span data-stu-id="b33a5-114">Data type: **Win32\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="b33a5-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b33a5-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b33a5-116">Qualificadores: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ ComputerSystem")</span><span class="sxs-lookup"><span data-stu-id="b33a5-116">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_ComputerSystem")</span></span>
</dt> </dl>

<span data-ttu-id="b33a5-117">Referência à instância que representa as propriedades do sistema de computador onde o dispositivo lógico existe.</span><span class="sxs-lookup"><span data-stu-id="b33a5-117">Reference to the instance representing the properties of the computer system where the logical device exists.</span></span>

</dd> <dt>

<span data-ttu-id="b33a5-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="b33a5-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b33a5-119">Tipo de dados **: \_ LogicalDevice CIM**</span><span class="sxs-lookup"><span data-stu-id="b33a5-119">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="b33a5-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b33a5-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b33a5-121">Qualificadores: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM \| CIM \_ LogicalDevice")</span><span class="sxs-lookup"><span data-stu-id="b33a5-121">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM\|CIM\_LogicalDevice")</span></span>
</dt> </dl>

<span data-ttu-id="b33a5-122">Referência à instância que representa as propriedades de um dispositivo lógico que existe no sistema de computador.</span><span class="sxs-lookup"><span data-stu-id="b33a5-122">Reference to the instance representing the properties of a logical device that exists on the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b33a5-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="b33a5-123">Remarks</span></span>

<span data-ttu-id="b33a5-124">A classe **Win32 \_ SystemDevices** é derivada de [**CIM \_ SystemDevice**](cim-systemdevice.md).</span><span class="sxs-lookup"><span data-stu-id="b33a5-124">The **Win32\_SystemDevices** class is derived from [**CIM\_SystemDevice**](cim-systemdevice.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b33a5-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b33a5-125">Requirements</span></span>



| <span data-ttu-id="b33a5-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="b33a5-126">Requirement</span></span> | <span data-ttu-id="b33a5-127">Valor</span><span class="sxs-lookup"><span data-stu-id="b33a5-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b33a5-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b33a5-128">Minimum supported client</span></span><br/> | <span data-ttu-id="b33a5-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b33a5-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b33a5-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b33a5-130">Minimum supported server</span></span><br/> | <span data-ttu-id="b33a5-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b33a5-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b33a5-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="b33a5-132">Namespace</span></span><br/>                | <span data-ttu-id="b33a5-133">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="b33a5-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b33a5-134">MOF</span><span class="sxs-lookup"><span data-stu-id="b33a5-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b33a5-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b33a5-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b33a5-136">DLL</span><span class="sxs-lookup"><span data-stu-id="b33a5-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b33a5-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b33a5-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b33a5-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="b33a5-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b33a5-139">**\_SYSTEMDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="b33a5-139">**CIM\_SystemDevice**</span></span>](cim-systemdevice.md)
</dt> <dt>

[<span data-ttu-id="b33a5-140">Classes do sistema operacional</span><span class="sxs-lookup"><span data-stu-id="b33a5-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
