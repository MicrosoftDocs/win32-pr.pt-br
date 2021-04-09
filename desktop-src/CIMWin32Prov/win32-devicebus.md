---
description: A \_ classe WMI de associação do Win32 DeviceBus relaciona um barramento do sistema e um dispositivo lógico usando o barramento. Essa classe é usada para descobrir quais dispositivos estão em qual barramento.
ms.assetid: 2d7d83a5-c058-40c0-aab3-7700f4067a16
ms.tgt_platform: multiple
title: Classe Win32_DeviceBus
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DeviceBus
- Win32_DeviceBus.Dependent
- Win32_DeviceBus.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2dde01ee6b3f3be026dbc19f8c4b8e2c238f4ff2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089657"
---
# <a name="win32_devicebus-class"></a><span data-ttu-id="6a65d-104">\_Classe Win32 DeviceBus</span><span class="sxs-lookup"><span data-stu-id="6a65d-104">Win32\_DeviceBus class</span></span>

<span data-ttu-id="6a65d-105">A [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) de associação do **Win32 \_ DeviceBus** relaciona um barramento do sistema e um dispositivo lógico usando o barramento.</span><span class="sxs-lookup"><span data-stu-id="6a65d-105">The **Win32\_DeviceBus** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a system bus and a logical device using the bus.</span></span> <span data-ttu-id="6a65d-106">Essa classe é usada para descobrir quais dispositivos estão em qual barramento.</span><span class="sxs-lookup"><span data-stu-id="6a65d-106">This class is used to discover which devices are on which bus.</span></span>

<span data-ttu-id="6a65d-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="6a65d-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="6a65d-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="6a65d-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a65d-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6a65d-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C50F-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_DeviceBus : CIM_Dependency
{
  CIM_LogicalDevice REF Dependent;
  Win32_Bus         REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="6a65d-110">Membros</span><span class="sxs-lookup"><span data-stu-id="6a65d-110">Members</span></span>

<span data-ttu-id="6a65d-111">A classe **Win32 \_ DeviceBus** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="6a65d-111">The **Win32\_DeviceBus** class has these types of members:</span></span>

-   [<span data-ttu-id="6a65d-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="6a65d-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6a65d-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="6a65d-113">Properties</span></span>

<span data-ttu-id="6a65d-114">A classe **Win32 \_ DeviceBus** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="6a65d-114">The **Win32\_DeviceBus** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6a65d-115">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="6a65d-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a65d-116">Tipo de dados **: \_ barramento Win32**</span><span class="sxs-lookup"><span data-stu-id="6a65d-116">Data type: **Win32\_Bus**</span></span>
</dt> <dt>

<span data-ttu-id="6a65d-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6a65d-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6a65d-118">Qualificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecessor"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ Bus")</span><span class="sxs-lookup"><span data-stu-id="6a65d-118">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_Bus")</span></span>
</dt> </dl>

<span data-ttu-id="6a65d-119">Um [**\_ barramento Win32**](win32-bus.md) que descreve as propriedades do barramento do sistema que é usado pelo dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="6a65d-119">A [**Win32\_Bus**](win32-bus.md) that describes the properties of the system bus that is used by the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="6a65d-120">**Depende**</span><span class="sxs-lookup"><span data-stu-id="6a65d-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a65d-121">Tipo de dados **: \_ LogicalDevice CIM**</span><span class="sxs-lookup"><span data-stu-id="6a65d-121">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="6a65d-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6a65d-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6a65d-123">Qualificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \| CIM \_ LogicalDevice")</span><span class="sxs-lookup"><span data-stu-id="6a65d-123">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\|CIM\_LogicalDevice")</span></span>
</dt> </dl>

<span data-ttu-id="6a65d-124">Um [**\_ LogicalDevice CIM**](cim-logicaldevice.md) que descreve as propriedades do dispositivo lógico que está usando o barramento do sistema.</span><span class="sxs-lookup"><span data-stu-id="6a65d-124">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that describes the properties of the logical device that is using the system bus.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6a65d-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="6a65d-125">Remarks</span></span>

<span data-ttu-id="6a65d-126">A classe **Win32 \_ DeviceBus** é derivada da [**\_ dependência CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="6a65d-126">The **Win32\_DeviceBus** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6a65d-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6a65d-127">Requirements</span></span>



| <span data-ttu-id="6a65d-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a65d-128">Requirement</span></span> | <span data-ttu-id="6a65d-129">Valor</span><span class="sxs-lookup"><span data-stu-id="6a65d-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6a65d-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6a65d-130">Minimum supported client</span></span><br/> | <span data-ttu-id="6a65d-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6a65d-131">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6a65d-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6a65d-132">Minimum supported server</span></span><br/> | <span data-ttu-id="6a65d-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6a65d-133">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6a65d-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="6a65d-134">Namespace</span></span><br/>                | <span data-ttu-id="6a65d-135">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="6a65d-135">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6a65d-136">MOF</span><span class="sxs-lookup"><span data-stu-id="6a65d-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6a65d-137"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6a65d-137"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6a65d-138">DLL</span><span class="sxs-lookup"><span data-stu-id="6a65d-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6a65d-139"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6a65d-139"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a65d-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="6a65d-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a65d-141">**\_Dependência CIM**</span><span class="sxs-lookup"><span data-stu-id="6a65d-141">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> <dt>

[<span data-ttu-id="6a65d-142">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="6a65d-142">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

