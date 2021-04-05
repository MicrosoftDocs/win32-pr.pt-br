---
description: A \_ classe WMI de associação ShareToDirectory do Win32 relaciona um recurso compartilhado no sistema de computador e o diretório no qual ele está mapeado.
ms.assetid: f8562539-2cb4-4661-8ef9-8b665e76a292
ms.tgt_platform: multiple
title: Classe Win32_ShareToDirectory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ShareToDirectory
- Win32_ShareToDirectory.Share
- Win32_ShareToDirectory.SharedElement
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: f02e5e1ce125a2c8495327a08c14c94ac9f48567
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646230"
---
# <a name="win32_sharetodirectory-class"></a><span data-ttu-id="ab661-103">\_Classe Win32 ShareToDirectory</span><span class="sxs-lookup"><span data-stu-id="ab661-103">Win32\_ShareToDirectory class</span></span>

<span data-ttu-id="ab661-104">A [classe WMI](../wmisdk/retrieving-a-class.md) de associação **\_ ShareToDirectory do Win32** relaciona um recurso compartilhado no sistema de computador e o diretório no qual ele está mapeado.</span><span class="sxs-lookup"><span data-stu-id="ab661-104">The **Win32\_ShareToDirectory** association [WMI class](../wmisdk/retrieving-a-class.md) relates a shared resource on the computer system and the directory to which it is mapped.</span></span>

<span data-ttu-id="ab661-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="ab661-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="ab661-106">As propriedades e os métodos estão em ordem alfabética, não em ordem de MOF.</span><span class="sxs-lookup"><span data-stu-id="ab661-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab661-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ab661-107">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("CIMWin32"), UUID("{8502C511-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_ShareToDirectory
{
  Win32_Share   REF Share;
  CIM_Directory REF SharedElement;
};
```

## <a name="members"></a><span data-ttu-id="ab661-108">Membros</span><span class="sxs-lookup"><span data-stu-id="ab661-108">Members</span></span>

<span data-ttu-id="ab661-109">A classe **Win32 \_ ShareToDirectory** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="ab661-109">The **Win32\_ShareToDirectory** class has these types of members:</span></span>

-   [<span data-ttu-id="ab661-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ab661-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ab661-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ab661-111">Properties</span></span>

<span data-ttu-id="ab661-112">A classe **Win32 \_ ShareToDirectory** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="ab661-112">The **Win32\_ShareToDirectory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ab661-113">**Compartilhe**</span><span class="sxs-lookup"><span data-stu-id="ab661-113">**Share**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab661-114">Tipo de dados **: \_ compartilhamento do Win32**</span><span class="sxs-lookup"><span data-stu-id="ab661-114">Data type: **Win32\_Share**</span></span>
</dt> <dt>

<span data-ttu-id="ab661-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ab661-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ab661-116">Qualificadores: [**chave**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| compartilhamento WMI Win32 \_ ")</span><span class="sxs-lookup"><span data-stu-id="ab661-116">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_Share")</span></span>
</dt> </dl>

<span data-ttu-id="ab661-117">Referência à instância que representa as propriedades de um recurso compartilhado disponível por meio do diretório.</span><span class="sxs-lookup"><span data-stu-id="ab661-117">Reference to the instance representing the properties of a shared resource available through the directory.</span></span>

</dd> <dt>

<span data-ttu-id="ab661-118">**Sharedelement**</span><span class="sxs-lookup"><span data-stu-id="ab661-118">**SharedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab661-119">Tipo de dados **: \_ diretório CIM**</span><span class="sxs-lookup"><span data-stu-id="ab661-119">Data type: **CIM\_Directory**</span></span>
</dt> <dt>

<span data-ttu-id="ab661-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ab661-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ab661-121">Qualificadores: [**chave**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("diretório CIM CIM \| \_ ")</span><span class="sxs-lookup"><span data-stu-id="ab661-121">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM\|CIM\_Directory")</span></span>
</dt> </dl>

<span data-ttu-id="ab661-122">Referência à instância que representa as propriedades do diretório que foi mapeado para um recurso compartilhado.</span><span class="sxs-lookup"><span data-stu-id="ab661-122">Reference to the instance representing the properties of the directory that has been mapped to a shared resource.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ab661-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ab661-123">Requirements</span></span>



| <span data-ttu-id="ab661-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab661-124">Requirement</span></span> | <span data-ttu-id="ab661-125">Valor</span><span class="sxs-lookup"><span data-stu-id="ab661-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ab661-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ab661-126">Minimum supported client</span></span><br/> | <span data-ttu-id="ab661-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ab661-127">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ab661-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ab661-128">Minimum supported server</span></span><br/> | <span data-ttu-id="ab661-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ab661-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ab661-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="ab661-130">Namespace</span></span><br/>                | <span data-ttu-id="ab661-131">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="ab661-131">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ab661-132">MOF</span><span class="sxs-lookup"><span data-stu-id="ab661-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ab661-133"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ab661-133"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ab661-134">DLL</span><span class="sxs-lookup"><span data-stu-id="ab661-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ab661-135"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ab661-135"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab661-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="ab661-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab661-137">Classes do sistema operacional</span><span class="sxs-lookup"><span data-stu-id="ab661-137">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
