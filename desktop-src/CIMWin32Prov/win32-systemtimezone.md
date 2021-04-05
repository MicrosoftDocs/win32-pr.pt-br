---
description: A \_ classe WMI de associação SystemTimeZone do Win32 relaciona um sistema de computador e um fuso horário.
ms.assetid: 53c74a61-c91d-4daa-933e-4cc7b9583d98
ms.tgt_platform: multiple
title: Classe Win32_SystemTimeZone
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemTimeZone
- Win32_SystemTimeZone.Element
- Win32_SystemTimeZone.Setting
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9ec294600fdc81f085bf29f5e664bcbec961417c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826408"
---
# <a name="win32_systemtimezone-class"></a><span data-ttu-id="76851-103">\_Classe Win32 SystemTimeZone</span><span class="sxs-lookup"><span data-stu-id="76851-103">Win32\_SystemTimeZone class</span></span>

<span data-ttu-id="76851-104">A [classe WMI](../wmisdk/retrieving-a-class.md) de associação **\_ SystemTimeZone do Win32** relaciona um sistema de computador e um fuso horário.</span><span class="sxs-lookup"><span data-stu-id="76851-104">The **Win32\_SystemTimeZone** association [WMI class](../wmisdk/retrieving-a-class.md) relates a computer system and a time zone.</span></span>

<span data-ttu-id="76851-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="76851-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="76851-106">As propriedades e os métodos estão em ordem alfabética, não em ordem de MOF.</span><span class="sxs-lookup"><span data-stu-id="76851-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="76851-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="76851-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C504-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemTimeZone : Win32_SystemSetting
{
  Win32_ComputerSystem REF Element;
  Win32_TimeZone       REF Setting;
};
```

## <a name="members"></a><span data-ttu-id="76851-108">Membros</span><span class="sxs-lookup"><span data-stu-id="76851-108">Members</span></span>

<span data-ttu-id="76851-109">A classe **Win32 \_ SystemTimeZone** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="76851-109">The **Win32\_SystemTimeZone** class has these types of members:</span></span>

-   [<span data-ttu-id="76851-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="76851-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="76851-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="76851-111">Properties</span></span>

<span data-ttu-id="76851-112">A classe **Win32 \_ SystemTimeZone** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="76851-112">The **Win32\_SystemTimeZone** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="76851-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="76851-113">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76851-114">Tipo de dados **: \_ sistema de ComputerSystem Win32**</span><span class="sxs-lookup"><span data-stu-id="76851-114">Data type: **Win32\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="76851-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="76851-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="76851-116">Qualificadores: [**override**](../wmisdk/standard-qualifiers.md) ("element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ ComputerSystem")</span><span class="sxs-lookup"><span data-stu-id="76851-116">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_ComputerSystem")</span></span>
</dt> </dl>

<span data-ttu-id="76851-117">Referência à instância que representa o sistema de computador mantendo o controle do fuso horário do sistema.</span><span class="sxs-lookup"><span data-stu-id="76851-117">Reference to the instance representing the computer system keeping track of the system time zone.</span></span>

</dd> <dt>

<span data-ttu-id="76851-118">**Configuração**</span><span class="sxs-lookup"><span data-stu-id="76851-118">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76851-119">Tipo de dados **: \_ fuso horário do Win32**</span><span class="sxs-lookup"><span data-stu-id="76851-119">Data type: **Win32\_TimeZone**</span></span>
</dt> <dt>

<span data-ttu-id="76851-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="76851-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="76851-121">Qualificadores: [**override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ timezone")</span><span class="sxs-lookup"><span data-stu-id="76851-121">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_TimeZone")</span></span>
</dt> </dl>

<span data-ttu-id="76851-122">Referência à instância que representa as propriedades de fuso horário rastreadas pelo sistema de computador.</span><span class="sxs-lookup"><span data-stu-id="76851-122">Reference to the instance representing the time zone properties tracked by the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="76851-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="76851-123">Remarks</span></span>

<span data-ttu-id="76851-124">A classe **Win32 \_ SystemTimeZone** é derivada de [**Win32 \_ SystemSetting**](win32-systemsetting.md).</span><span class="sxs-lookup"><span data-stu-id="76851-124">The **Win32\_SystemTimeZone** class is derived from [**Win32\_SystemSetting**](win32-systemsetting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="76851-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="76851-125">Requirements</span></span>



| <span data-ttu-id="76851-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="76851-126">Requirement</span></span> | <span data-ttu-id="76851-127">Valor</span><span class="sxs-lookup"><span data-stu-id="76851-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="76851-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="76851-128">Minimum supported client</span></span><br/> | <span data-ttu-id="76851-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="76851-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="76851-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="76851-130">Minimum supported server</span></span><br/> | <span data-ttu-id="76851-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="76851-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="76851-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="76851-132">Namespace</span></span><br/>                | <span data-ttu-id="76851-133">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="76851-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="76851-134">MOF</span><span class="sxs-lookup"><span data-stu-id="76851-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="76851-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="76851-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="76851-136">DLL</span><span class="sxs-lookup"><span data-stu-id="76851-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="76851-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="76851-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76851-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="76851-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76851-139">**\_SystemSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="76851-139">**Win32\_SystemSetting**</span></span>](win32-systemsetting.md)
</dt> <dt>

[<span data-ttu-id="76851-140">Classes do sistema operacional</span><span class="sxs-lookup"><span data-stu-id="76851-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
