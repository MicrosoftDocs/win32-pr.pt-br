---
description: A \_ classe WMI de associação ComClassAutoEmulator do Win32 relaciona uma classe com (Component Object Model) e outra classe com que ela emula automaticamente.
ms.assetid: e060ba26-98e7-47cb-bf21-1ca80d0e8a07
ms.tgt_platform: multiple
title: Classe Win32_ComClassAutoEmulator
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ComClassAutoEmulator
- Win32_ComClassAutoEmulator.NewVersion
- Win32_ComClassAutoEmulator.OldVersion
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9442036d43859caa5fa277109c7e85553e7d42f0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089469"
---
# <a name="win32_comclassautoemulator-class"></a><span data-ttu-id="2472d-103">\_Classe Win32 ComClassAutoEmulator</span><span class="sxs-lookup"><span data-stu-id="2472d-103">Win32\_ComClassAutoEmulator class</span></span>

<span data-ttu-id="2472d-104">A [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) de associação **\_ ComClassAutoEmulator do Win32** relaciona uma classe com (Component Object Model) e outra classe com que ela emula automaticamente.</span><span class="sxs-lookup"><span data-stu-id="2472d-104">The **Win32\_ComClassAutoEmulator** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a Component Object Model (COM) class and another COM class that it automatically emulates.</span></span>

<span data-ttu-id="2472d-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="2472d-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="2472d-106">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="2472d-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="2472d-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2472d-107">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("CIMWin32"), UUID("{0F73ED5D-8ED9-11d2-B340-00105A1F8569}"), AMENDMENT]
class Win32_ComClassAutoEmulator
{
  Win32_ClassicCOMClass REF NewVersion;
  Win32_ClassicCOMClass REF OldVersion;
};
```

## <a name="members"></a><span data-ttu-id="2472d-108">Membros</span><span class="sxs-lookup"><span data-stu-id="2472d-108">Members</span></span>

<span data-ttu-id="2472d-109">A classe **Win32 \_ ComClassAutoEmulator** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="2472d-109">The **Win32\_ComClassAutoEmulator** class has these types of members:</span></span>

-   [<span data-ttu-id="2472d-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="2472d-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2472d-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="2472d-111">Properties</span></span>

<span data-ttu-id="2472d-112">A classe **Win32 \_ ComClassAutoEmulator** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="2472d-112">The **Win32\_ComClassAutoEmulator** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2472d-113">**NewVersion**</span><span class="sxs-lookup"><span data-stu-id="2472d-113">**NewVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2472d-114">Tipo de dados: **Win32 \_ ClassicCOMClass**</span><span class="sxs-lookup"><span data-stu-id="2472d-114">Data type: **Win32\_ClassicCOMClass**</span></span>
</dt> <dt>

<span data-ttu-id="2472d-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2472d-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2472d-116">Qualificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ ClassicCOMClass")</span><span class="sxs-lookup"><span data-stu-id="2472d-116">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_ClassicCOMClass")</span></span>
</dt> </dl>

<span data-ttu-id="2472d-117">Referência à instância que representa o componente COM que pode emular automaticamente o componente COM associado.</span><span class="sxs-lookup"><span data-stu-id="2472d-117">Reference to the instance representing the COM component that can automatically emulate the associated COM component.</span></span> <span data-ttu-id="2472d-118">Essas informações são obtidas por meio da entrada de registro autotratáas.</span><span class="sxs-lookup"><span data-stu-id="2472d-118">This information is obtained through the AutoTreatAs registry entry.</span></span>

</dd> <dt>

<span data-ttu-id="2472d-119">**OldVersion**</span><span class="sxs-lookup"><span data-stu-id="2472d-119">**OldVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2472d-120">Tipo de dados: **Win32 \_ ClassicCOMClass**</span><span class="sxs-lookup"><span data-stu-id="2472d-120">Data type: **Win32\_ClassicCOMClass**</span></span>
</dt> <dt>

<span data-ttu-id="2472d-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2472d-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2472d-122">Qualificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ ClassicCOMClass")</span><span class="sxs-lookup"><span data-stu-id="2472d-122">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_ClassicCOMClass")</span></span>
</dt> </dl>

<span data-ttu-id="2472d-123">Referência à instância que representa o componente COM que é emulado automaticamente por outro componente.</span><span class="sxs-lookup"><span data-stu-id="2472d-123">Reference to the instance representing the COM component that is automatically emulated by another component.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2472d-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2472d-124">Requirements</span></span>



| <span data-ttu-id="2472d-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="2472d-125">Requirement</span></span> | <span data-ttu-id="2472d-126">Valor</span><span class="sxs-lookup"><span data-stu-id="2472d-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2472d-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2472d-127">Minimum supported client</span></span><br/> | <span data-ttu-id="2472d-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2472d-128">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2472d-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2472d-129">Minimum supported server</span></span><br/> | <span data-ttu-id="2472d-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2472d-130">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2472d-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="2472d-131">Namespace</span></span><br/>                | <span data-ttu-id="2472d-132">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="2472d-132">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2472d-133">MOF</span><span class="sxs-lookup"><span data-stu-id="2472d-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2472d-134"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2472d-134"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2472d-135">DLL</span><span class="sxs-lookup"><span data-stu-id="2472d-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2472d-136"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2472d-136"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2472d-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="2472d-137">See also</span></span>

<dl> <dt>

<span data-ttu-id="2472d-138">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2472d-138">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

