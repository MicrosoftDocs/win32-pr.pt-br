---
description: A \_ classe WMI de associação SystemUsers do Win32 relaciona um sistema de computador e uma conta de usuário nesse sistema.
ms.assetid: 0f6cba69-86f7-4795-a47d-6fb8ed0a00b8
ms.tgt_platform: multiple
title: Classe Win32_SystemUsers
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemUsers
- Win32_SystemUsers.GroupComponent
- Win32_SystemUsers.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a2239983d5b9c080c60d301a557b5487f8cf7fcf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920551"
---
# <a name="win32_systemusers-class"></a><span data-ttu-id="b682e-103">\_Classe Win32 SystemUsers</span><span class="sxs-lookup"><span data-stu-id="b682e-103">Win32\_SystemUsers class</span></span>

<span data-ttu-id="b682e-104">A [classe WMI](../wmisdk/retrieving-a-class.md) de associação **\_ SystemUsers do Win32** relaciona um sistema de computador e uma conta de usuário nesse sistema.</span><span class="sxs-lookup"><span data-stu-id="b682e-104">The **Win32\_SystemUsers** association [WMI class](../wmisdk/retrieving-a-class.md) relates a computer system and a user account on that system.</span></span>

<span data-ttu-id="b682e-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="b682e-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="b682e-106">As propriedades e os métodos estão em ordem alfabética, não em ordem de MOF.</span><span class="sxs-lookup"><span data-stu-id="b682e-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b682e-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b682e-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4F2-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemUsers : CIM_SystemComponent
{
  Win32_ComputerSystem REF GroupComponent;
  Win32_UserAccount    REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="b682e-108">Membros</span><span class="sxs-lookup"><span data-stu-id="b682e-108">Members</span></span>

<span data-ttu-id="b682e-109">A classe **Win32 \_ SystemUsers** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="b682e-109">The **Win32\_SystemUsers** class has these types of members:</span></span>

-   [<span data-ttu-id="b682e-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b682e-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b682e-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b682e-111">Properties</span></span>

<span data-ttu-id="b682e-112">A classe **Win32 \_ SystemUsers** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="b682e-112">The **Win32\_SystemUsers** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b682e-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="b682e-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b682e-114">Tipo de dados **: \_ sistema de ComputerSystem Win32**</span><span class="sxs-lookup"><span data-stu-id="b682e-114">Data type: **Win32\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="b682e-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b682e-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b682e-116">Qualificadores: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ ComputerSystem")</span><span class="sxs-lookup"><span data-stu-id="b682e-116">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_ComputerSystem")</span></span>
</dt> </dl>

<span data-ttu-id="b682e-117">Referência à instância que representa o sistema de computador que contém a conta de usuário.</span><span class="sxs-lookup"><span data-stu-id="b682e-117">Reference to the instance representing the computer system containing the user account.</span></span>

</dd> <dt>

<span data-ttu-id="b682e-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="b682e-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b682e-119">Tipo de dados **: \_ conta de userwin32**</span><span class="sxs-lookup"><span data-stu-id="b682e-119">Data type: **Win32\_UserAccount**</span></span>
</dt> <dt>

<span data-ttu-id="b682e-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b682e-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b682e-121">Qualificadores: [**chave**](../wmisdk/key-qualifier.md), [**substituição**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("conta de userwmi \| Win32 \_ ")</span><span class="sxs-lookup"><span data-stu-id="b682e-121">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_UserAccount")</span></span>
</dt> </dl>

<span data-ttu-id="b682e-122">Referência à instância que representa a conta de usuário no sistema de computador.</span><span class="sxs-lookup"><span data-stu-id="b682e-122">Reference to the instance representing the user account on the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b682e-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="b682e-123">Remarks</span></span>

<span data-ttu-id="b682e-124">A classe **Win32 \_ SystemUsers** é derivada de [**CIM \_ Systemcomponent**](cim-systemcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="b682e-124">The **Win32\_SystemUsers** class is derived from [**CIM\_SystemComponent**](cim-systemcomponent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b682e-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b682e-125">Requirements</span></span>



| <span data-ttu-id="b682e-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="b682e-126">Requirement</span></span> | <span data-ttu-id="b682e-127">Valor</span><span class="sxs-lookup"><span data-stu-id="b682e-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b682e-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b682e-128">Minimum supported client</span></span><br/> | <span data-ttu-id="b682e-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b682e-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b682e-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b682e-130">Minimum supported server</span></span><br/> | <span data-ttu-id="b682e-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b682e-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b682e-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="b682e-132">Namespace</span></span><br/>                | <span data-ttu-id="b682e-133">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="b682e-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b682e-134">MOF</span><span class="sxs-lookup"><span data-stu-id="b682e-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b682e-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b682e-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b682e-136">DLL</span><span class="sxs-lookup"><span data-stu-id="b682e-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b682e-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b682e-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b682e-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="b682e-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b682e-139">**\_SYSTEMCOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="b682e-139">**CIM\_SystemComponent**</span></span>](cim-systemcomponent.md)
</dt> <dt>

[<span data-ttu-id="b682e-140">Classes do sistema operacional</span><span class="sxs-lookup"><span data-stu-id="b682e-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
