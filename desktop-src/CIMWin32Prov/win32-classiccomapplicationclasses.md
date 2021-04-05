---
description: A \_ classe WMI de associação ClassicCOMApplicationClasses do Win32 relaciona um aplicativo com e um componente com agrupados sob ele.
ms.assetid: 77f24461-9ca0-4fc3-8728-4a4b9a1edbc3
ms.tgt_platform: multiple
title: Classe Win32_ClassicCOMApplicationClasses
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ClassicCOMApplicationClasses
- Win32_ClassicCOMApplicationClasses.PartComponent
- Win32_ClassicCOMApplicationClasses.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: dfd451c1c5d4819f1ec1d21f890b207a06d6fb82
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826589"
---
# <a name="win32_classiccomapplicationclasses-class"></a><span data-ttu-id="23500-103">\_Classe Win32 ClassicCOMApplicationClasses</span><span class="sxs-lookup"><span data-stu-id="23500-103">Win32\_ClassicCOMApplicationClasses class</span></span>

<span data-ttu-id="23500-104">A [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) de associação **\_ ClassicCOMApplicationClasses do Win32** relaciona um aplicativo com e um componente com agrupados sob ele.</span><span class="sxs-lookup"><span data-stu-id="23500-104">The **Win32\_ClassicCOMApplicationClasses** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a COM application and a COM component grouped under it.</span></span>

<span data-ttu-id="23500-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="23500-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="23500-106">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="23500-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="23500-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="23500-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{0F73ED54-8ED9-11d2-B340-00105A1F8569}"), AMENDMENT]
class Win32_ClassicCOMApplicationClasses : Win32_COMApplicationClasses
{
  Win32_ClassicCOMClass REF PartComponent;
  Win32_DCOMApplication REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="23500-108">Membros</span><span class="sxs-lookup"><span data-stu-id="23500-108">Members</span></span>

<span data-ttu-id="23500-109">A classe **Win32 \_ ClassicCOMApplicationClasses** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="23500-109">The **Win32\_ClassicCOMApplicationClasses** class has these types of members:</span></span>

-   [<span data-ttu-id="23500-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="23500-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="23500-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="23500-111">Properties</span></span>

<span data-ttu-id="23500-112">A classe **Win32 \_ ClassicCOMApplicationClasses** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="23500-112">The **Win32\_ClassicCOMApplicationClasses** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="23500-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="23500-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23500-114">Tipo de dados: **Win32 \_ DCOMApplication**</span><span class="sxs-lookup"><span data-stu-id="23500-114">Data type: **Win32\_DCOMApplication**</span></span>
</dt> <dt>

<span data-ttu-id="23500-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="23500-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="23500-116">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ DCOMApplication")</span><span class="sxs-lookup"><span data-stu-id="23500-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_DCOMApplication")</span></span>
</dt> </dl>

<span data-ttu-id="23500-117">Um [**\_ DCOMApplication Win32**](win32-dcomapplication.md) que representa um aplicativo DCOM que contém ou usa o componente com.</span><span class="sxs-lookup"><span data-stu-id="23500-117">A [**Win32\_DCOMApplication**](win32-dcomapplication.md) that represents a DCOM application containing or using the COM component.</span></span>

</dd> <dt>

<span data-ttu-id="23500-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="23500-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23500-119">Tipo de dados: **Win32 \_ ClassicCOMClass**</span><span class="sxs-lookup"><span data-stu-id="23500-119">Data type: **Win32\_ClassicCOMClass**</span></span>
</dt> <dt>

<span data-ttu-id="23500-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="23500-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="23500-121">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ ClassicCOMClass")</span><span class="sxs-lookup"><span data-stu-id="23500-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_ClassicCOMClass")</span></span>
</dt> </dl>

<span data-ttu-id="23500-122">Um [**\_ ClassicCOMClass Win32**](win32-classiccomclass.md) que representa o componente com existente ou usado pelo aplicativo DCOM.</span><span class="sxs-lookup"><span data-stu-id="23500-122">A [**Win32\_ClassicCOMClass**](win32-classiccomclass.md) that represents the COM component existing in or used by the DCOM application.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="23500-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="23500-123">Remarks</span></span>

<span data-ttu-id="23500-124">A classe **Win32 \_ ClassicCOMApplicationClasses** é derivada de [**Win32 \_ COMApplicationClasses**](win32-comapplicationclasses.md).</span><span class="sxs-lookup"><span data-stu-id="23500-124">The **Win32\_ClassicCOMApplicationClasses** class is derived from [**Win32\_COMApplicationClasses**](win32-comapplicationclasses.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="23500-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="23500-125">Requirements</span></span>



| <span data-ttu-id="23500-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="23500-126">Requirement</span></span> | <span data-ttu-id="23500-127">Valor</span><span class="sxs-lookup"><span data-stu-id="23500-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="23500-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="23500-128">Minimum supported client</span></span><br/> | <span data-ttu-id="23500-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="23500-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="23500-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="23500-130">Minimum supported server</span></span><br/> | <span data-ttu-id="23500-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="23500-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="23500-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="23500-132">Namespace</span></span><br/>                | <span data-ttu-id="23500-133">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="23500-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="23500-134">MOF</span><span class="sxs-lookup"><span data-stu-id="23500-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="23500-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="23500-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="23500-136">DLL</span><span class="sxs-lookup"><span data-stu-id="23500-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="23500-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="23500-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23500-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="23500-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23500-139">**\_COMApplicationClasses Win32**</span><span class="sxs-lookup"><span data-stu-id="23500-139">**Win32\_COMApplicationClasses**</span></span>](win32-comapplicationclasses.md)
</dt> <dt>

<span data-ttu-id="23500-140">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="23500-140">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

