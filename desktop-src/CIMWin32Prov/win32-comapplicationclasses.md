---
description: A \_ classe WMI de associação abstrata COMApplicationClasses do Win32 relaciona um componente com (Component Object Model) e o aplicativo com onde ele reside.
ms.assetid: 7c188199-86fb-45ba-b318-9d9529b831b8
ms.tgt_platform: multiple
title: Classe Win32_COMApplicationClasses
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_COMApplicationClasses
- Win32_COMApplicationClasses.PartComponent
- Win32_COMApplicationClasses.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 01413128f7457049a4383c1148938e2136645337
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089470"
---
# <a name="win32_comapplicationclasses-class"></a><span data-ttu-id="38ade-103">\_Classe Win32 COMApplicationClasses</span><span class="sxs-lookup"><span data-stu-id="38ade-103">Win32\_COMApplicationClasses class</span></span>

<span data-ttu-id="38ade-104">A [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) de associação abstrata **\_ COMApplicationClasses do Win32** relaciona um componente com (Component Object Model) e o aplicativo com onde ele reside.</span><span class="sxs-lookup"><span data-stu-id="38ade-104">The **Win32\_COMApplicationClasses** abstract association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a Component Object Model (COM) component and the COM application where it resides.</span></span>

<span data-ttu-id="38ade-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="38ade-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="38ade-106">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="38ade-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="38ade-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="38ade-107">Syntax</span></span>

``` syntax
[abstract, UUID("{0F73ED51-8ED9-11d2-B340-00105A1F8569}"), AMENDMENT]
class Win32_COMApplicationClasses : CIM_Component
{
  Win32_COMClass       REF PartComponent;
  Win32_COMApplication REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="38ade-108">Membros</span><span class="sxs-lookup"><span data-stu-id="38ade-108">Members</span></span>

<span data-ttu-id="38ade-109">A classe **Win32 \_ COMApplicationClasses** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="38ade-109">The **Win32\_COMApplicationClasses** class has these types of members:</span></span>

-   [<span data-ttu-id="38ade-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="38ade-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="38ade-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="38ade-111">Properties</span></span>

<span data-ttu-id="38ade-112">A classe **Win32 \_ COMApplicationClasses** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="38ade-112">The **Win32\_COMApplicationClasses** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="38ade-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="38ade-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38ade-114">Tipo de dados **: \_ aplicativo Win32**</span><span class="sxs-lookup"><span data-stu-id="38ade-114">Data type: **Win32\_COMApplication**</span></span>
</dt> <dt>

<span data-ttu-id="38ade-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="38ade-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="38ade-116">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**substituição**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| aplicativo WMI Win32 \_ ")</span><span class="sxs-lookup"><span data-stu-id="38ade-116">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_COMApplication")</span></span>
</dt> </dl>

<span data-ttu-id="38ade-117">Um [**\_ aplicativo do Win32**](win32-comapplication.md) que representa o aplicativo com que contém o componente com.</span><span class="sxs-lookup"><span data-stu-id="38ade-117">A [**Win32\_COMApplication**](win32-comapplication.md) that represents the COM application containing the COM component.</span></span>

</dd> <dt>

<span data-ttu-id="38ade-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="38ade-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38ade-119">Tipo de dados: **Win32 \_ COMClass**</span><span class="sxs-lookup"><span data-stu-id="38ade-119">Data type: **Win32\_COMClass**</span></span>
</dt> <dt>

<span data-ttu-id="38ade-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="38ade-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="38ade-121">Qualificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ COMClass")</span><span class="sxs-lookup"><span data-stu-id="38ade-121">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_COMClass")</span></span>
</dt> </dl>

<span data-ttu-id="38ade-122">Um [**\_ COMClass do Win32**](win32-comclass.md) que representa o componente com agrupado sob o aplicativo com.</span><span class="sxs-lookup"><span data-stu-id="38ade-122">A [**Win32\_COMClass**](win32-comclass.md) that represents the COM component grouped under the COM application.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="38ade-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="38ade-123">Remarks</span></span>

<span data-ttu-id="38ade-124">A classe **Win32 \_ COMApplicationClasses** é derivada do [**\_ componente CIM**](cim-component.md).</span><span class="sxs-lookup"><span data-stu-id="38ade-124">The **Win32\_COMApplicationClasses** class is derived from [**CIM\_Component**](cim-component.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="38ade-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="38ade-125">Requirements</span></span>



| <span data-ttu-id="38ade-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="38ade-126">Requirement</span></span> | <span data-ttu-id="38ade-127">Valor</span><span class="sxs-lookup"><span data-stu-id="38ade-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="38ade-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="38ade-128">Minimum supported client</span></span><br/> | <span data-ttu-id="38ade-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="38ade-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="38ade-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="38ade-130">Minimum supported server</span></span><br/> | <span data-ttu-id="38ade-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="38ade-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="38ade-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="38ade-132">Namespace</span></span><br/>                | <span data-ttu-id="38ade-133">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="38ade-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="38ade-134">MOF</span><span class="sxs-lookup"><span data-stu-id="38ade-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="38ade-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="38ade-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="38ade-136">DLL</span><span class="sxs-lookup"><span data-stu-id="38ade-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="38ade-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="38ade-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38ade-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="38ade-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38ade-139">**\_Componente CIM**</span><span class="sxs-lookup"><span data-stu-id="38ade-139">**CIM\_Component**</span></span>](cim-component.md)
</dt> <dt>

<span data-ttu-id="38ade-140">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="38ade-140">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

