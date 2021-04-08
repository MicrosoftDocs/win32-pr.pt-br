---
description: A \_ classe WMI de associação ComClassEmulator do Win32 relaciona duas versões de uma classe com (Component Object Model).
ms.assetid: 33899c1e-911d-49ad-be25-355dcdb8f0c7
ms.tgt_platform: multiple
title: Classe Win32_ComClassEmulator
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ComClassEmulator
- Win32_ComClassEmulator.NewVersion
- Win32_ComClassEmulator.OldVersion
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9966ed85b0e0b4eeb25073e13ad679759f1d460b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104088974"
---
# <a name="win32_comclassemulator-class"></a><span data-ttu-id="a485d-103">\_Classe Win32 ComClassEmulator</span><span class="sxs-lookup"><span data-stu-id="a485d-103">Win32\_ComClassEmulator class</span></span>

<span data-ttu-id="a485d-104">A [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) de associação **\_ ComClassEmulator do Win32** relaciona duas versões de uma classe com (Component Object Model).</span><span class="sxs-lookup"><span data-stu-id="a485d-104">The **Win32\_ComClassEmulator** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates two versions of a Component Object Model (COM) class.</span></span>

<span data-ttu-id="a485d-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="a485d-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="a485d-106">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="a485d-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a485d-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a485d-107">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("CIMWin32"), UUID("{0F73ED5C-8ED9-11d2-B340-00105A1F8569}"), AMENDMENT]
class Win32_ComClassEmulator
{
  Win32_ClassicCOMClass REF NewVersion;
  Win32_ClassicCOMClass REF OldVersion;
};
```

## <a name="members"></a><span data-ttu-id="a485d-108">Membros</span><span class="sxs-lookup"><span data-stu-id="a485d-108">Members</span></span>

<span data-ttu-id="a485d-109">A classe **Win32 \_ ComClassEmulator** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="a485d-109">The **Win32\_ComClassEmulator** class has these types of members:</span></span>

-   [<span data-ttu-id="a485d-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a485d-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a485d-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a485d-111">Properties</span></span>

<span data-ttu-id="a485d-112">A classe **Win32 \_ ComClassEmulator** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="a485d-112">The **Win32\_ComClassEmulator** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a485d-113">**NewVersion**</span><span class="sxs-lookup"><span data-stu-id="a485d-113">**NewVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a485d-114">Tipo de dados: **Win32 \_ ClassicCOMClass**</span><span class="sxs-lookup"><span data-stu-id="a485d-114">Data type: **Win32\_ClassicCOMClass**</span></span>
</dt> <dt>

<span data-ttu-id="a485d-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a485d-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a485d-116">Qualificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ ClassicCOMClass")</span><span class="sxs-lookup"><span data-stu-id="a485d-116">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_ClassicCOMClass")</span></span>
</dt> </dl>

<span data-ttu-id="a485d-117">Referência à instância que representa o componente COM que contém interfaces que emulam a versão mais antiga do componente.</span><span class="sxs-lookup"><span data-stu-id="a485d-117">Reference to the instance representing the COM component that contains interfaces emulating the older version of the component.</span></span>

</dd> <dt>

<span data-ttu-id="a485d-118">**OldVersion**</span><span class="sxs-lookup"><span data-stu-id="a485d-118">**OldVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a485d-119">Tipo de dados: **Win32 \_ ClassicCOMClass**</span><span class="sxs-lookup"><span data-stu-id="a485d-119">Data type: **Win32\_ClassicCOMClass**</span></span>
</dt> <dt>

<span data-ttu-id="a485d-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a485d-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a485d-121">Qualificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ ClassicCOMClass")</span><span class="sxs-lookup"><span data-stu-id="a485d-121">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_ClassicCOMClass")</span></span>
</dt> </dl>

<span data-ttu-id="a485d-122">Referência à instância que representa o componente com com interfaces que podem ser emuladas pela nova versão do componente.</span><span class="sxs-lookup"><span data-stu-id="a485d-122">Reference to the instance representing the COM component with interfaces that can be emulated by the new version of the component.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a485d-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a485d-123">Requirements</span></span>



| <span data-ttu-id="a485d-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="a485d-124">Requirement</span></span> | <span data-ttu-id="a485d-125">Valor</span><span class="sxs-lookup"><span data-stu-id="a485d-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a485d-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a485d-126">Minimum supported client</span></span><br/> | <span data-ttu-id="a485d-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a485d-127">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a485d-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a485d-128">Minimum supported server</span></span><br/> | <span data-ttu-id="a485d-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a485d-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a485d-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="a485d-130">Namespace</span></span><br/>                | <span data-ttu-id="a485d-131">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="a485d-131">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a485d-132">MOF</span><span class="sxs-lookup"><span data-stu-id="a485d-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a485d-133"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a485d-133"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a485d-134">DLL</span><span class="sxs-lookup"><span data-stu-id="a485d-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a485d-135"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a485d-135"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a485d-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="a485d-136">See also</span></span>

<dl> <dt>

<span data-ttu-id="a485d-137">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a485d-137">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

