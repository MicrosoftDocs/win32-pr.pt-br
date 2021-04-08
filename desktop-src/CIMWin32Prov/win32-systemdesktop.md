---
description: A \_ classe WMI de associação SystemDesktop do Win32 relaciona um sistema de computador e sua configuração de desktop.
ms.assetid: 2b024660-d707-4463-8207-73df74bfa7d6
ms.tgt_platform: multiple
title: Classe Win32_SystemDesktop
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDesktop
- Win32_SystemDesktop.Element
- Win32_SystemDesktop.Setting
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3e14cab58a445fd645b9d59c1aea713bf6c40ac0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920553"
---
# <a name="win32_systemdesktop-class"></a><span data-ttu-id="d7dd5-103">\_Classe Win32 SystemDesktop</span><span class="sxs-lookup"><span data-stu-id="d7dd5-103">Win32\_SystemDesktop class</span></span>

<span data-ttu-id="d7dd5-104">A [classe WMI](../wmisdk/retrieving-a-class.md) de associação **\_ SystemDesktop do Win32** relaciona um sistema de computador e sua configuração de desktop.</span><span class="sxs-lookup"><span data-stu-id="d7dd5-104">The **Win32\_SystemDesktop** association [WMI class](../wmisdk/retrieving-a-class.md) relates a computer system and its desktop configuration.</span></span>

<span data-ttu-id="d7dd5-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="d7dd5-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="d7dd5-106">As propriedades e os métodos estão em ordem alfabética, não em ordem de MOF.</span><span class="sxs-lookup"><span data-stu-id="d7dd5-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7dd5-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d7dd5-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C506-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemDesktop : Win32_SystemSetting
{
  Win32_ComputerSystem REF Element;
  Win32_Desktop        REF Setting;
};
```

## <a name="members"></a><span data-ttu-id="d7dd5-108">Membros</span><span class="sxs-lookup"><span data-stu-id="d7dd5-108">Members</span></span>

<span data-ttu-id="d7dd5-109">A classe **Win32 \_ SystemDesktop** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="d7dd5-109">The **Win32\_SystemDesktop** class has these types of members:</span></span>

-   [<span data-ttu-id="d7dd5-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d7dd5-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d7dd5-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d7dd5-111">Properties</span></span>

<span data-ttu-id="d7dd5-112">A classe **Win32 \_ SystemDesktop** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="d7dd5-112">The **Win32\_SystemDesktop** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d7dd5-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="d7dd5-113">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7dd5-114">Tipo de dados **: \_ sistema de ComputerSystem Win32**</span><span class="sxs-lookup"><span data-stu-id="d7dd5-114">Data type: **Win32\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="d7dd5-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d7dd5-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d7dd5-116">Qualificadores: [**override**](../wmisdk/standard-qualifiers.md) ("element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ ComputerSystem")</span><span class="sxs-lookup"><span data-stu-id="d7dd5-116">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_ComputerSystem")</span></span>
</dt> </dl>

<span data-ttu-id="d7dd5-117">Referência à instância que representa o sistema de computador no qual a configuração da área de trabalho existe.</span><span class="sxs-lookup"><span data-stu-id="d7dd5-117">Reference to the instance representing the computer system where the desktop configuration exists.</span></span>

</dd> <dt>

<span data-ttu-id="d7dd5-118">**Configuração**</span><span class="sxs-lookup"><span data-stu-id="d7dd5-118">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7dd5-119">Tipo de dados **: \_ Desktop Win32**</span><span class="sxs-lookup"><span data-stu-id="d7dd5-119">Data type: **Win32\_Desktop**</span></span>
</dt> <dt>

<span data-ttu-id="d7dd5-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d7dd5-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d7dd5-121">Qualificadores: [**override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ Desktop")</span><span class="sxs-lookup"><span data-stu-id="d7dd5-121">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_Desktop")</span></span>
</dt> </dl>

<span data-ttu-id="d7dd5-122">Referência à instância que representa a configuração existente no sistema de computador.</span><span class="sxs-lookup"><span data-stu-id="d7dd5-122">Reference to the instance representing the configuration existing on the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d7dd5-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="d7dd5-123">Remarks</span></span>

<span data-ttu-id="d7dd5-124">A classe **Win32 \_ SystemDesktop** é derivada de [**Win32 \_ SystemSetting**](win32-systemsetting.md).</span><span class="sxs-lookup"><span data-stu-id="d7dd5-124">The **Win32\_SystemDesktop** class is derived from [**Win32\_SystemSetting**](win32-systemsetting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d7dd5-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d7dd5-125">Requirements</span></span>



| <span data-ttu-id="d7dd5-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7dd5-126">Requirement</span></span> | <span data-ttu-id="d7dd5-127">Valor</span><span class="sxs-lookup"><span data-stu-id="d7dd5-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d7dd5-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d7dd5-128">Minimum supported client</span></span><br/> | <span data-ttu-id="d7dd5-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d7dd5-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d7dd5-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d7dd5-130">Minimum supported server</span></span><br/> | <span data-ttu-id="d7dd5-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d7dd5-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d7dd5-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="d7dd5-132">Namespace</span></span><br/>                | <span data-ttu-id="d7dd5-133">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="d7dd5-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d7dd5-134">MOF</span><span class="sxs-lookup"><span data-stu-id="d7dd5-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d7dd5-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d7dd5-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d7dd5-136">DLL</span><span class="sxs-lookup"><span data-stu-id="d7dd5-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d7dd5-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d7dd5-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7dd5-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="d7dd5-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7dd5-139">**\_SystemSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="d7dd5-139">**Win32\_SystemSetting**</span></span>](win32-systemsetting.md)
</dt> <dt>

[<span data-ttu-id="d7dd5-140">Classes do sistema operacional</span><span class="sxs-lookup"><span data-stu-id="d7dd5-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
