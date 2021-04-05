---
description: A \_ classe WMI de associação LogicalDiskRootDirectory do Win32 relaciona um disco lógico e sua estrutura de diretórios.
ms.assetid: 860cd28a-2a59-4ce3-be26-8fdc869c70d1
ms.tgt_platform: multiple
title: Classe Win32_LogicalDiskRootDirectory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogicalDiskRootDirectory
- Win32_LogicalDiskRootDirectory.GroupComponent
- Win32_LogicalDiskRootDirectory.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e4b015891a37c5cc92bbf102482f48306d537bb6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826142"
---
# <a name="win32_logicaldiskrootdirectory-class"></a><span data-ttu-id="bdc7a-103">\_Classe Win32 LogicalDiskRootDirectory</span><span class="sxs-lookup"><span data-stu-id="bdc7a-103">Win32\_LogicalDiskRootDirectory class</span></span>

<span data-ttu-id="bdc7a-104">A [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) de associação **\_ LogicalDiskRootDirectory do Win32** relaciona um disco lógico e sua estrutura de diretórios.</span><span class="sxs-lookup"><span data-stu-id="bdc7a-104">The **Win32\_LogicalDiskRootDirectory** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a logical disk and its directory structure.</span></span>

<span data-ttu-id="bdc7a-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="bdc7a-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="bdc7a-106">As propriedades e os métodos estão em ordem alfabética, não em ordem de MOF.</span><span class="sxs-lookup"><span data-stu-id="bdc7a-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="bdc7a-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bdc7a-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{F25FE468-783E-11d2-90BF-0060081A46FD}"), AMENDMENT]
class Win32_LogicalDiskRootDirectory : CIM_Component
{
  Win32_LogicalDisk REF GroupComponent;
  Win32_Directory   REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="bdc7a-108">Membros</span><span class="sxs-lookup"><span data-stu-id="bdc7a-108">Members</span></span>

<span data-ttu-id="bdc7a-109">A classe **Win32 \_ LogicalDiskRootDirectory** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="bdc7a-109">The **Win32\_LogicalDiskRootDirectory** class has these types of members:</span></span>

-   [<span data-ttu-id="bdc7a-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="bdc7a-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bdc7a-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="bdc7a-111">Properties</span></span>

<span data-ttu-id="bdc7a-112">A classe **Win32 \_ LogicalDiskRootDirectory** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="bdc7a-112">The **Win32\_LogicalDiskRootDirectory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bdc7a-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="bdc7a-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bdc7a-114">Tipo de dados: disco **\_ lógico do Win32**</span><span class="sxs-lookup"><span data-stu-id="bdc7a-114">Data type: **Win32\_LogicalDisk**</span></span>
</dt> <dt>

<span data-ttu-id="bdc7a-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bdc7a-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bdc7a-116">Qualificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ LogicalDisk")</span><span class="sxs-lookup"><span data-stu-id="bdc7a-116">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_LogicalDisk")</span></span>
</dt> </dl>

<span data-ttu-id="bdc7a-117">Referência à instância que representa as propriedades do disco lógico.</span><span class="sxs-lookup"><span data-stu-id="bdc7a-117">Reference to the instance representing the properties of the logical disk.</span></span>

</dd> <dt>

<span data-ttu-id="bdc7a-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="bdc7a-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bdc7a-119">Tipo de dados **: \_ diretório Win32**</span><span class="sxs-lookup"><span data-stu-id="bdc7a-119">Data type: **Win32\_Directory**</span></span>
</dt> <dt>

<span data-ttu-id="bdc7a-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bdc7a-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bdc7a-121">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**substituição**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| diretório WMI Win32 \_ ")</span><span class="sxs-lookup"><span data-stu-id="bdc7a-121">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_Directory")</span></span>
</dt> </dl>

<span data-ttu-id="bdc7a-122">Referência à instância que representa as propriedades da estrutura do diretório de arquivos.</span><span class="sxs-lookup"><span data-stu-id="bdc7a-122">Reference to the instance representing the properties of the file directory structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bdc7a-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="bdc7a-123">Remarks</span></span>

<span data-ttu-id="bdc7a-124">A classe **Win32 \_ LogicalDiskRootDirectory** é derivada do [**\_ componente CIM**](cim-component.md).</span><span class="sxs-lookup"><span data-stu-id="bdc7a-124">The **Win32\_LogicalDiskRootDirectory** class is derived from [**CIM\_Component**](cim-component.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bdc7a-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bdc7a-125">Requirements</span></span>



| <span data-ttu-id="bdc7a-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="bdc7a-126">Requirement</span></span> | <span data-ttu-id="bdc7a-127">Valor</span><span class="sxs-lookup"><span data-stu-id="bdc7a-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bdc7a-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bdc7a-128">Minimum supported client</span></span><br/> | <span data-ttu-id="bdc7a-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bdc7a-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="bdc7a-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bdc7a-130">Minimum supported server</span></span><br/> | <span data-ttu-id="bdc7a-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bdc7a-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="bdc7a-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="bdc7a-132">Namespace</span></span><br/>                | <span data-ttu-id="bdc7a-133">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="bdc7a-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="bdc7a-134">MOF</span><span class="sxs-lookup"><span data-stu-id="bdc7a-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bdc7a-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bdc7a-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="bdc7a-136">DLL</span><span class="sxs-lookup"><span data-stu-id="bdc7a-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bdc7a-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bdc7a-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bdc7a-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="bdc7a-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bdc7a-139">**\_Componente CIM**</span><span class="sxs-lookup"><span data-stu-id="bdc7a-139">**CIM\_Component**</span></span>](cim-component.md)
</dt> <dt>

<span data-ttu-id="bdc7a-140">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="bdc7a-140">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

