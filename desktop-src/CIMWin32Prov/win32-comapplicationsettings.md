---
description: A \_ classe WMI de associação COMApplicationSettings do Win32 relaciona um aplicativo DCOM e suas definições de configuração.
ms.assetid: b08eaff1-b42a-42f3-abf7-3664b6195acd
ms.tgt_platform: multiple
title: Classe Win32_COMApplicationSettings
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_COMApplicationSettings
- Win32_COMApplicationSettings.Setting
- Win32_COMApplicationSettings.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8f2fd5953d770d541e704b7dc7fe8580e98b3066
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104163930"
---
# <a name="win32_comapplicationsettings-class"></a><span data-ttu-id="5cebb-103">\_Classe Win32 COMApplicationSettings</span><span class="sxs-lookup"><span data-stu-id="5cebb-103">Win32\_COMApplicationSettings class</span></span>

<span data-ttu-id="5cebb-104">A [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) de associação **\_ COMApplicationSettings do Win32** relaciona um aplicativo DCOM e suas definições de configuração.</span><span class="sxs-lookup"><span data-stu-id="5cebb-104">The **Win32\_COMApplicationSettings** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a DCOM application and its configuration settings.</span></span>

<span data-ttu-id="5cebb-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="5cebb-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="5cebb-106">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="5cebb-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="5cebb-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5cebb-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{E5D8A563-F6C0-11d2-B35E-00105A1F8569}"), AMENDMENT]
class Win32_COMApplicationSettings : CIM_ElementSetting
{
  Win32_DCOMApplicationSetting REF Setting;
  Win32_DCOMApplication        REF Element;
};
```

## <a name="members"></a><span data-ttu-id="5cebb-108">Membros</span><span class="sxs-lookup"><span data-stu-id="5cebb-108">Members</span></span>

<span data-ttu-id="5cebb-109">A classe **Win32 \_ COMApplicationSettings** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="5cebb-109">The **Win32\_COMApplicationSettings** class has these types of members:</span></span>

-   [<span data-ttu-id="5cebb-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5cebb-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5cebb-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5cebb-111">Properties</span></span>

<span data-ttu-id="5cebb-112">A classe **Win32 \_ COMApplicationSettings** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="5cebb-112">The **Win32\_COMApplicationSettings** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5cebb-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="5cebb-113">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cebb-114">Tipo de dados: **Win32 \_ DCOMApplication**</span><span class="sxs-lookup"><span data-stu-id="5cebb-114">Data type: **Win32\_DCOMApplication**</span></span>
</dt> <dt>

<span data-ttu-id="5cebb-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5cebb-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5cebb-116">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**substituição**](/windows/desktop/WmiSdk/standard-qualifiers) ("elemento"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ DCOMApplication")</span><span class="sxs-lookup"><span data-stu-id="5cebb-116">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Element"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_DCOMApplication")</span></span>
</dt> </dl>

<span data-ttu-id="5cebb-117">Um [**\_ DCOMApplication Win32**](win32-dcomapplication.md) que representa o aplicativo DCOM no qual as configurações são aplicadas.</span><span class="sxs-lookup"><span data-stu-id="5cebb-117">A [**Win32\_DCOMApplication**](win32-dcomapplication.md) that represents the DCOM application where the settings are applied.</span></span>

</dd> <dt>

<span data-ttu-id="5cebb-118">**Configuração**</span><span class="sxs-lookup"><span data-stu-id="5cebb-118">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cebb-119">Tipo de dados: **Win32 \_ DCOMApplicationSetting**</span><span class="sxs-lookup"><span data-stu-id="5cebb-119">Data type: **Win32\_DCOMApplicationSetting**</span></span>
</dt> <dt>

<span data-ttu-id="5cebb-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5cebb-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5cebb-121">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**substituição**](/windows/desktop/WmiSdk/standard-qualifiers) ("configuração"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ DCOMApplicationSetting")</span><span class="sxs-lookup"><span data-stu-id="5cebb-121">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Setting"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_DCOMApplicationSetting")</span></span>
</dt> </dl>

<span data-ttu-id="5cebb-122">Um [**\_ DCOMApplicationSetting Win32**](win32-dcomapplicationsetting.md) que representa os parâmetros de configuração associados ao aplicativo DCOM.</span><span class="sxs-lookup"><span data-stu-id="5cebb-122">A [**Win32\_DCOMApplicationSetting**](win32-dcomapplicationsetting.md) that represents the configuration settings associated with the DCOM application.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5cebb-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="5cebb-123">Remarks</span></span>

<span data-ttu-id="5cebb-124">A classe **Win32 \_ COMApplicationSettings** é derivada de [**CIM \_ ElementSetting**](cim-elementsetting.md).</span><span class="sxs-lookup"><span data-stu-id="5cebb-124">The **Win32\_COMApplicationSettings** class is derived from [**CIM\_ElementSetting**](cim-elementsetting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5cebb-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5cebb-125">Requirements</span></span>



| <span data-ttu-id="5cebb-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="5cebb-126">Requirement</span></span> | <span data-ttu-id="5cebb-127">Valor</span><span class="sxs-lookup"><span data-stu-id="5cebb-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5cebb-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5cebb-128">Minimum supported client</span></span><br/> | <span data-ttu-id="5cebb-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5cebb-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5cebb-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5cebb-130">Minimum supported server</span></span><br/> | <span data-ttu-id="5cebb-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5cebb-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5cebb-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="5cebb-132">Namespace</span></span><br/>                | <span data-ttu-id="5cebb-133">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="5cebb-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5cebb-134">MOF</span><span class="sxs-lookup"><span data-stu-id="5cebb-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5cebb-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5cebb-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5cebb-136">DLL</span><span class="sxs-lookup"><span data-stu-id="5cebb-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5cebb-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5cebb-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5cebb-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="5cebb-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5cebb-139">**\_ELEMENTSETTING CIM**</span><span class="sxs-lookup"><span data-stu-id="5cebb-139">**CIM\_ElementSetting**</span></span>](cim-elementsetting.md)
</dt> <dt>

<span data-ttu-id="5cebb-140">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5cebb-140">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

