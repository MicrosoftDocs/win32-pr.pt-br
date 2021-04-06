---
description: A \_ classe WMI de associação SystemBootConfiguration do Win32 relaciona um sistema de computador e sua configuração de inicialização.
ms.assetid: 1c6bce81-84d9-4949-92da-6111b4ecc939
ms.tgt_platform: multiple
title: Classe Win32_SystemBootConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemBootConfiguration
- Win32_SystemBootConfiguration.Element
- Win32_SystemBootConfiguration.Setting
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 863e4103f7e87681e25ccf53679bfe006ed3ff75
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826413"
---
# <a name="win32_systembootconfiguration-class"></a><span data-ttu-id="ae9be-103">\_Classe Win32 SystemBootConfiguration</span><span class="sxs-lookup"><span data-stu-id="ae9be-103">Win32\_SystemBootConfiguration class</span></span>

<span data-ttu-id="ae9be-104">A [classe WMI](../wmisdk/retrieving-a-class.md) de associação **\_ SystemBootConfiguration do Win32** relaciona um sistema de computador e sua configuração de inicialização.</span><span class="sxs-lookup"><span data-stu-id="ae9be-104">The **Win32\_SystemBootConfiguration** association [WMI class](../wmisdk/retrieving-a-class.md) relates a computer system and its boot configuration.</span></span>

<span data-ttu-id="ae9be-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="ae9be-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="ae9be-106">As propriedades e os métodos estão em ordem alfabética, não em ordem de MOF.</span><span class="sxs-lookup"><span data-stu-id="ae9be-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae9be-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ae9be-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C507-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemBootConfiguration : Win32_SystemSetting
{
  Win32_ComputerSystem    REF Element;
  Win32_BootConfiguration REF Setting;
};
```

## <a name="members"></a><span data-ttu-id="ae9be-108">Membros</span><span class="sxs-lookup"><span data-stu-id="ae9be-108">Members</span></span>

<span data-ttu-id="ae9be-109">A classe **Win32 \_ SystemBootConfiguration** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="ae9be-109">The **Win32\_SystemBootConfiguration** class has these types of members:</span></span>

-   [<span data-ttu-id="ae9be-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ae9be-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ae9be-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ae9be-111">Properties</span></span>

<span data-ttu-id="ae9be-112">A classe **Win32 \_ SystemBootConfiguration** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="ae9be-112">The **Win32\_SystemBootConfiguration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ae9be-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="ae9be-113">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae9be-114">Tipo de dados **: \_ sistema de ComputerSystem Win32**</span><span class="sxs-lookup"><span data-stu-id="ae9be-114">Data type: **Win32\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="ae9be-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ae9be-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae9be-116">Qualificadores: [**override**](../wmisdk/standard-qualifiers.md) ("element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ ComputerSystem")</span><span class="sxs-lookup"><span data-stu-id="ae9be-116">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_ComputerSystem")</span></span>
</dt> </dl>

<span data-ttu-id="ae9be-117">Referência à instância que representa o sistema de computador usando a configuração de inicialização.</span><span class="sxs-lookup"><span data-stu-id="ae9be-117">Reference to the instance representing the computer system using the boot configuration.</span></span>

</dd> <dt>

<span data-ttu-id="ae9be-118">**Configuração**</span><span class="sxs-lookup"><span data-stu-id="ae9be-118">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae9be-119">Tipo de dados: **Win32 \_ BootConfiguration**</span><span class="sxs-lookup"><span data-stu-id="ae9be-119">Data type: **Win32\_BootConfiguration**</span></span>
</dt> <dt>

<span data-ttu-id="ae9be-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ae9be-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae9be-121">Qualificadores: [**override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ BootConfiguration")</span><span class="sxs-lookup"><span data-stu-id="ae9be-121">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_BootConfiguration")</span></span>
</dt> </dl>

<span data-ttu-id="ae9be-122">Referência à instância que representa a configuração de inicialização do sistema de computador.</span><span class="sxs-lookup"><span data-stu-id="ae9be-122">Reference to the instance representing the boot configuration for the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ae9be-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="ae9be-123">Remarks</span></span>

<span data-ttu-id="ae9be-124">A classe **Win32 \_ SystemBootConfiguration** é derivada de [**Win32 \_ SystemSetting**](win32-systemsetting.md).</span><span class="sxs-lookup"><span data-stu-id="ae9be-124">The **Win32\_SystemBootConfiguration** class is derived from [**Win32\_SystemSetting**](win32-systemsetting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ae9be-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ae9be-125">Requirements</span></span>



| <span data-ttu-id="ae9be-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="ae9be-126">Requirement</span></span> | <span data-ttu-id="ae9be-127">Valor</span><span class="sxs-lookup"><span data-stu-id="ae9be-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ae9be-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ae9be-128">Minimum supported client</span></span><br/> | <span data-ttu-id="ae9be-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ae9be-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ae9be-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ae9be-130">Minimum supported server</span></span><br/> | <span data-ttu-id="ae9be-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ae9be-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ae9be-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="ae9be-132">Namespace</span></span><br/>                | <span data-ttu-id="ae9be-133">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="ae9be-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ae9be-134">MOF</span><span class="sxs-lookup"><span data-stu-id="ae9be-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ae9be-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ae9be-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ae9be-136">DLL</span><span class="sxs-lookup"><span data-stu-id="ae9be-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ae9be-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ae9be-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae9be-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="ae9be-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae9be-139">**\_SystemSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="ae9be-139">**Win32\_SystemSetting**</span></span>](win32-systemsetting.md)
</dt> <dt>

[<span data-ttu-id="ae9be-140">Classes do sistema operacional</span><span class="sxs-lookup"><span data-stu-id="ae9be-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
