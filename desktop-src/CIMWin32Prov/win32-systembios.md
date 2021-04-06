---
description: A \_ classe WMI de associação SystemBIOS do Win32 relaciona um sistema de computador (incluindo dados como propriedades de inicialização, fusos horários, configurações de inicialização ou senhas administrativas) e um BIOS do sistema (serviços, linguagens e propriedades de gerenciamento do sistema).
ms.assetid: 92747b1b-ef28-40ab-868a-6755aee8c723
ms.tgt_platform: multiple
title: Classe Win32_SystemBIOS
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemBIOS
- Win32_SystemBIOS.PartComponent
- Win32_SystemBIOS.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: bc8ec1f3526e2faefe0e63c9dea357accd025c13
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826617"
---
# <a name="win32_systembios-class"></a><span data-ttu-id="bb111-103">\_Classe Win32 SystemBIOS</span><span class="sxs-lookup"><span data-stu-id="bb111-103">Win32\_SystemBIOS class</span></span>

<span data-ttu-id="bb111-104">A [classe WMI](../wmisdk/retrieving-a-class.md) de associação **\_ SystemBIOS do Win32** relaciona um sistema de computador (incluindo dados como propriedades de inicialização, fusos horários, configurações de inicialização ou senhas administrativas) e um BIOS do sistema (serviços, linguagens e propriedades de gerenciamento do sistema).</span><span class="sxs-lookup"><span data-stu-id="bb111-104">The **Win32\_SystemBIOS** association [WMI class](../wmisdk/retrieving-a-class.md) relates a computer system (including data such as startup properties, time zones, boot configurations, or administrative passwords), and a system BIOS (services, languages, and system management properties).</span></span>

<span data-ttu-id="bb111-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="bb111-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="bb111-106">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="bb111-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb111-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bb111-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4EE-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemBIOS : CIM_SystemComponent
{
  Win32_BIOS           REF PartComponent;
  Win32_ComputerSystem REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="bb111-108">Membros</span><span class="sxs-lookup"><span data-stu-id="bb111-108">Members</span></span>

<span data-ttu-id="bb111-109">A classe **Win32 \_ SystemBIOS** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="bb111-109">The **Win32\_SystemBIOS** class has these types of members:</span></span>

-   [<span data-ttu-id="bb111-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="bb111-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bb111-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="bb111-111">Properties</span></span>

<span data-ttu-id="bb111-112">A classe **Win32 \_ SystemBIOS** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="bb111-112">The **Win32\_SystemBIOS** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bb111-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="bb111-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb111-114">Tipo de dados **: \_ sistema de ComputerSystem Win32**</span><span class="sxs-lookup"><span data-stu-id="bb111-114">Data type: **Win32\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="bb111-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bb111-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bb111-116">Qualificadores: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ ComputerSystem")</span><span class="sxs-lookup"><span data-stu-id="bb111-116">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_ComputerSystem")</span></span>
</dt> </dl>

<span data-ttu-id="bb111-117">O [**\_ sistema de ComputerSystem do Win32**](win32-computersystemprocessor.md) que contém o BIOS da associação.</span><span class="sxs-lookup"><span data-stu-id="bb111-117">The [**Win32\_ComputerSystem**](win32-computersystemprocessor.md) containing the BIOS of the association.</span></span>

</dd> <dt>

<span data-ttu-id="bb111-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="bb111-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb111-119">Tipo de dados **: \_ BIOS Win32**</span><span class="sxs-lookup"><span data-stu-id="bb111-119">Data type: **Win32\_BIOS**</span></span>
</dt> <dt>

<span data-ttu-id="bb111-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bb111-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bb111-121">Qualificadores: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ BIOS")</span><span class="sxs-lookup"><span data-stu-id="bb111-121">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_BIOS")</span></span>
</dt> </dl>

<span data-ttu-id="bb111-122">Um [**\_ BIOS Win32**](win32-bios.md) contido no sistema de computador dessa associação.</span><span class="sxs-lookup"><span data-stu-id="bb111-122">A [**Win32\_BIOS**](win32-bios.md) contained in the computer system of this association.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bb111-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="bb111-123">Remarks</span></span>

<span data-ttu-id="bb111-124">A classe **Win32 \_ SystemBIOS** é derivada de [**CIM \_ Systemcomponent**](cim-systemcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="bb111-124">The **Win32\_SystemBIOS** class is derived from [**CIM\_SystemComponent**](cim-systemcomponent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bb111-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bb111-125">Requirements</span></span>



| <span data-ttu-id="bb111-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb111-126">Requirement</span></span> | <span data-ttu-id="bb111-127">Valor</span><span class="sxs-lookup"><span data-stu-id="bb111-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bb111-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bb111-128">Minimum supported client</span></span><br/> | <span data-ttu-id="bb111-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bb111-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="bb111-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bb111-130">Minimum supported server</span></span><br/> | <span data-ttu-id="bb111-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bb111-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="bb111-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="bb111-132">Namespace</span></span><br/>                | <span data-ttu-id="bb111-133">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="bb111-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="bb111-134">MOF</span><span class="sxs-lookup"><span data-stu-id="bb111-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bb111-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bb111-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="bb111-136">DLL</span><span class="sxs-lookup"><span data-stu-id="bb111-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bb111-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bb111-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb111-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="bb111-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb111-139">**\_SYSTEMCOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="bb111-139">**CIM\_SystemComponent**</span></span>](cim-systemcomponent.md)
</dt> <dt>

[<span data-ttu-id="bb111-140">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="bb111-140">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
