---
description: A \_ classe WMI de associação ComputerSystemProcessor do Win32 relaciona um sistema de computador e um processador em execução nesse sistema.
ms.assetid: e630ebea-19bf-43c7-a8a0-7acfda3a752b
ms.tgt_platform: multiple
title: Classe Win32_ComputerSystemProcessor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ComputerSystemProcessor
- Win32_ComputerSystemProcessor.PartComponent
- Win32_ComputerSystemProcessor.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2f836d8f5e9053029763c38d2c4f2116987b08fe
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089028"
---
# <a name="win32_computersystemprocessor-class"></a><span data-ttu-id="e5951-103">\_Classe Win32 ComputerSystemProcessor</span><span class="sxs-lookup"><span data-stu-id="e5951-103">Win32\_ComputerSystemProcessor class</span></span>

<span data-ttu-id="e5951-104">A [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) de associação **\_ ComputerSystemProcessor do Win32** relaciona um sistema de computador e um processador em execução nesse sistema.</span><span class="sxs-lookup"><span data-stu-id="e5951-104">The **Win32\_ComputerSystemProcessor** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a computer system and a processor running on that system.</span></span>

<span data-ttu-id="e5951-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="e5951-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="e5951-106">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="e5951-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5951-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e5951-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{719A6839-C124-11d2-85E8-0000F8102E5F}"), AMENDMENT]
class Win32_ComputerSystemProcessor : Win32_SystemDevices
{
  Win32_Processor      REF PartComponent;
  Win32_ComputerSystem REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="e5951-108">Membros</span><span class="sxs-lookup"><span data-stu-id="e5951-108">Members</span></span>

<span data-ttu-id="e5951-109">A classe **Win32 \_ ComputerSystemProcessor** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="e5951-109">The **Win32\_ComputerSystemProcessor** class has these types of members:</span></span>

-   [<span data-ttu-id="e5951-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e5951-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e5951-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e5951-111">Properties</span></span>

<span data-ttu-id="e5951-112">A classe **Win32 \_ ComputerSystemProcessor** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="e5951-112">The **Win32\_ComputerSystemProcessor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e5951-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="e5951-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5951-114">Tipo de dados **: \_ sistema de ComputerSystem Win32**</span><span class="sxs-lookup"><span data-stu-id="e5951-114">Data type: **Win32\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="e5951-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e5951-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e5951-116">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ ComputerSystem")</span><span class="sxs-lookup"><span data-stu-id="e5951-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_ComputerSystem")</span></span>
</dt> </dl>

<span data-ttu-id="e5951-117">Um **\_ sistema** de computadores Win32 que descreve as propriedades do sistema de computador em que o processador está sendo executado.</span><span class="sxs-lookup"><span data-stu-id="e5951-117">A **Win32\_ComputerSystem** that describes the properties of the computer system on which the processor is running.</span></span>

</dd> <dt>

<span data-ttu-id="e5951-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="e5951-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5951-119">Tipo de dados **: \_ processador Win32**</span><span class="sxs-lookup"><span data-stu-id="e5951-119">Data type: **Win32\_Processor**</span></span>
</dt> <dt>

<span data-ttu-id="e5951-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e5951-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e5951-121">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| processador WMI Win32 \_ ")</span><span class="sxs-lookup"><span data-stu-id="e5951-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_Processor")</span></span>
</dt> </dl>

<span data-ttu-id="e5951-122">Um [**\_ processador Win32**](win32-processor.md) que descreve as propriedades de um processador que está executando o sistema de computador.</span><span class="sxs-lookup"><span data-stu-id="e5951-122">A [**Win32\_Processor**](win32-processor.md) that describes the properties of a processor which is running the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e5951-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="e5951-123">Remarks</span></span>

<span data-ttu-id="e5951-124">A classe **Win32 \_ ComputerSystemProcessor** é derivada de [**Win32 \_ SystemDevices**](win32-systemdevices.md).</span><span class="sxs-lookup"><span data-stu-id="e5951-124">The **Win32\_ComputerSystemProcessor** class is derived from [**Win32\_SystemDevices**](win32-systemdevices.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e5951-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e5951-125">Requirements</span></span>



| <span data-ttu-id="e5951-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="e5951-126">Requirement</span></span> | <span data-ttu-id="e5951-127">Valor</span><span class="sxs-lookup"><span data-stu-id="e5951-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e5951-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e5951-128">Minimum supported client</span></span><br/> | <span data-ttu-id="e5951-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e5951-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e5951-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e5951-130">Minimum supported server</span></span><br/> | <span data-ttu-id="e5951-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e5951-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e5951-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="e5951-132">Namespace</span></span><br/>                | <span data-ttu-id="e5951-133">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="e5951-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e5951-134">MOF</span><span class="sxs-lookup"><span data-stu-id="e5951-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e5951-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e5951-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e5951-136">DLL</span><span class="sxs-lookup"><span data-stu-id="e5951-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e5951-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e5951-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5951-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="e5951-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5951-139">**\_SystemDevices Win32**</span><span class="sxs-lookup"><span data-stu-id="e5951-139">**Win32\_SystemDevices**</span></span>](win32-systemdevices.md)
</dt> <dt>

<span data-ttu-id="e5951-140">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e5951-140">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

