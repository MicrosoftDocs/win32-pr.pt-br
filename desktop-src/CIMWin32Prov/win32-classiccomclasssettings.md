---
description: A \_ classe WMI de associação ClassicCOMClassSettings do Win32 relaciona uma classe com (Component Object Model) e as configurações usadas para configurar instâncias da classe com.
ms.assetid: 50f253cc-b8ae-41ac-b01f-ea816f5ca3d4
ms.tgt_platform: multiple
title: Classe Win32_ClassicCOMClassSettings
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ClassicCOMClassSettings
- Win32_ClassicCOMClassSettings.Setting
- Win32_ClassicCOMClassSettings.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: fb9c190157742aeca7c1ba6008a784005d054ca6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826179"
---
# <a name="win32_classiccomclasssettings-class"></a><span data-ttu-id="5072d-103">\_Classe Win32 ClassicCOMClassSettings</span><span class="sxs-lookup"><span data-stu-id="5072d-103">Win32\_ClassicCOMClassSettings class</span></span>

<span data-ttu-id="5072d-104">A [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) de associação **\_ ClassicCOMClassSettings do Win32** relaciona uma classe com (Component Object Model) e as configurações usadas para configurar instâncias da classe com.</span><span class="sxs-lookup"><span data-stu-id="5072d-104">The **Win32\_ClassicCOMClassSettings** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a Component Object Model (COM) class and the settings used to configure instances of the COM class.</span></span>

<span data-ttu-id="5072d-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="5072d-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="5072d-106">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="5072d-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="5072d-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5072d-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{E5D8A564-F6C0-11d2-B35E-00105A1F8569}"), AMENDMENT]
class Win32_ClassicCOMClassSettings : CIM_ElementSetting
{
  Win32_ClassicCOMClassSetting REF Setting;
  Win32_ClassicCOMClass        REF Element;
};
```

## <a name="members"></a><span data-ttu-id="5072d-108">Membros</span><span class="sxs-lookup"><span data-stu-id="5072d-108">Members</span></span>

<span data-ttu-id="5072d-109">A classe **Win32 \_ ClassicCOMClassSettings** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="5072d-109">The **Win32\_ClassicCOMClassSettings** class has these types of members:</span></span>

-   [<span data-ttu-id="5072d-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5072d-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5072d-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5072d-111">Properties</span></span>

<span data-ttu-id="5072d-112">A classe **Win32 \_ ClassicCOMClassSettings** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="5072d-112">The **Win32\_ClassicCOMClassSettings** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5072d-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="5072d-113">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5072d-114">Tipo de dados: **Win32 \_ ClassicCOMClass**</span><span class="sxs-lookup"><span data-stu-id="5072d-114">Data type: **Win32\_ClassicCOMClass**</span></span>
</dt> <dt>

<span data-ttu-id="5072d-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5072d-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5072d-116">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**substituição**](/windows/desktop/WmiSdk/standard-qualifiers) ("elemento"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ ClassicCOMClass")</span><span class="sxs-lookup"><span data-stu-id="5072d-116">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Element"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_ClassicCOMClass")</span></span>
</dt> </dl>

<span data-ttu-id="5072d-117">Um [**\_ ClassicCOMClass Win32**](win32-classiccomclass.md) que representa a classe com onde as configurações são aplicadas.</span><span class="sxs-lookup"><span data-stu-id="5072d-117">A [**Win32\_ClassicCOMClass**](win32-classiccomclass.md) that represents the COM class where the settings are applied.</span></span>

</dd> <dt>

<span data-ttu-id="5072d-118">**Configuração**</span><span class="sxs-lookup"><span data-stu-id="5072d-118">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5072d-119">Tipo de dados: **Win32 \_ ClassicCOMClassSetting**</span><span class="sxs-lookup"><span data-stu-id="5072d-119">Data type: **Win32\_ClassicCOMClassSetting**</span></span>
</dt> <dt>

<span data-ttu-id="5072d-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5072d-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5072d-121">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**substituição**](/windows/desktop/WmiSdk/standard-qualifiers) ("configuração"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ ClassicCOMClassSetting")</span><span class="sxs-lookup"><span data-stu-id="5072d-121">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Setting"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_ClassicCOMClassSetting")</span></span>
</dt> </dl>

<span data-ttu-id="5072d-122">Um [**\_ ClassicCOMClassSetting Win32**](win32-classiccomclasssetting.md) que representa as definições de configuração associadas à classe com.</span><span class="sxs-lookup"><span data-stu-id="5072d-122">A [**Win32\_ClassicCOMClassSetting**](win32-classiccomclasssetting.md) that represents configuration settings associated with the COM class.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5072d-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="5072d-123">Remarks</span></span>

<span data-ttu-id="5072d-124">A classe **Win32 \_ ClassicCOMClassSettings** é derivada de [**CIM \_ ElementSetting**](cim-elementsetting.md).</span><span class="sxs-lookup"><span data-stu-id="5072d-124">The **Win32\_ClassicCOMClassSettings** class is derived from [**CIM\_ElementSetting**](cim-elementsetting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5072d-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5072d-125">Requirements</span></span>



| <span data-ttu-id="5072d-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="5072d-126">Requirement</span></span> | <span data-ttu-id="5072d-127">Valor</span><span class="sxs-lookup"><span data-stu-id="5072d-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5072d-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5072d-128">Minimum supported client</span></span><br/> | <span data-ttu-id="5072d-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5072d-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5072d-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5072d-130">Minimum supported server</span></span><br/> | <span data-ttu-id="5072d-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5072d-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5072d-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="5072d-132">Namespace</span></span><br/>                | <span data-ttu-id="5072d-133">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="5072d-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5072d-134">MOF</span><span class="sxs-lookup"><span data-stu-id="5072d-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5072d-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5072d-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5072d-136">DLL</span><span class="sxs-lookup"><span data-stu-id="5072d-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5072d-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5072d-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5072d-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="5072d-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5072d-139">**\_ELEMENTSETTING CIM**</span><span class="sxs-lookup"><span data-stu-id="5072d-139">**CIM\_ElementSetting**</span></span>](cim-elementsetting.md)
</dt> <dt>

<span data-ttu-id="5072d-140">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5072d-140">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

