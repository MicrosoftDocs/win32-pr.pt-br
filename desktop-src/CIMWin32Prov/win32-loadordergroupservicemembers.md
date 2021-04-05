---
description: A \_ classe WMI de associação do Win32 LoadOrderGroupServiceMembers relaciona um grupo de ordem de carregamento e um serviço base.
ms.assetid: 60fa8292-b9d1-48f2-bd26-e5c9276006fc
ms.tgt_platform: multiple
title: Classe Win32_LoadOrderGroupServiceMembers
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LoadOrderGroupServiceMembers
- Win32_LoadOrderGroupServiceMembers.GroupComponent
- Win32_LoadOrderGroupServiceMembers.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 557e9b029dcbdac06e24d1630f00488696792e25
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826655"
---
# <a name="win32_loadordergroupservicemembers-class"></a><span data-ttu-id="55c1d-103">\_Classe Win32 LoadOrderGroupServiceMembers</span><span class="sxs-lookup"><span data-stu-id="55c1d-103">Win32\_LoadOrderGroupServiceMembers class</span></span>

<span data-ttu-id="55c1d-104">A [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) de associação do **Win32 \_ LoadOrderGroupServiceMembers** relaciona um grupo de ordem de carregamento e um serviço base.</span><span class="sxs-lookup"><span data-stu-id="55c1d-104">The **Win32\_LoadOrderGroupServiceMembers** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a load order group and a base service.</span></span>

> [!Note]  
> <span data-ttu-id="55c1d-105">[**Win32 \_**](win32-systemdriver.md) Os objetos do SystemDriver são membros desse grupo de ordem de carregamento.</span><span class="sxs-lookup"><span data-stu-id="55c1d-105">[**Win32\_SystemDriver**](win32-systemdriver.md) objects are members of that load order group.</span></span> <span data-ttu-id="55c1d-106">Nem todos os serviços são membros de grupos e nem todos os grupos têm serviços dentro deles.</span><span class="sxs-lookup"><span data-stu-id="55c1d-106">Not all services are members of groups, and not all groups have services within them.</span></span>

 

<span data-ttu-id="55c1d-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="55c1d-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="55c1d-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="55c1d-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="55c1d-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="55c1d-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4EF-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_LoadOrderGroupServiceMembers : CIM_Component
{
  Win32_LoadOrderGroup REF GroupComponent;
  Win32_BaseService    REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="55c1d-110">Membros</span><span class="sxs-lookup"><span data-stu-id="55c1d-110">Members</span></span>

<span data-ttu-id="55c1d-111">A classe **Win32 \_ LoadOrderGroupServiceMembers** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="55c1d-111">The **Win32\_LoadOrderGroupServiceMembers** class has these types of members:</span></span>

-   [<span data-ttu-id="55c1d-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="55c1d-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="55c1d-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="55c1d-113">Properties</span></span>

<span data-ttu-id="55c1d-114">A classe **Win32 \_ LoadOrderGroupServiceMembers** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="55c1d-114">The **Win32\_LoadOrderGroupServiceMembers** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="55c1d-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="55c1d-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55c1d-116">Tipo de dados: **Win32 \_ loadordergroup**</span><span class="sxs-lookup"><span data-stu-id="55c1d-116">Data type: **Win32\_LoadOrderGroup**</span></span>
</dt> <dt>

<span data-ttu-id="55c1d-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="55c1d-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55c1d-118">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**substituição**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ loadorder OrderGroup")</span><span class="sxs-lookup"><span data-stu-id="55c1d-118">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_LoadOrderGroup")</span></span>
</dt> </dl>

<span data-ttu-id="55c1d-119">Referência à instância que representa as propriedades do grupo de ordens de carga associadas ao serviço base.</span><span class="sxs-lookup"><span data-stu-id="55c1d-119">Reference to the instance representing the load order group properties associated with the base service.</span></span>

</dd> <dt>

<span data-ttu-id="55c1d-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="55c1d-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55c1d-121">Tipo de dados: **Win32 \_ BaseService**</span><span class="sxs-lookup"><span data-stu-id="55c1d-121">Data type: **Win32\_BaseService**</span></span>
</dt> <dt>

<span data-ttu-id="55c1d-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="55c1d-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55c1d-123">Qualificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ BaseService")</span><span class="sxs-lookup"><span data-stu-id="55c1d-123">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_BaseService")</span></span>
</dt> </dl>

<span data-ttu-id="55c1d-124">Referência à instância que representa o serviço que é membro de um grupo de ordem de carregamento.</span><span class="sxs-lookup"><span data-stu-id="55c1d-124">Reference to the instance representing the service that is a member of a load order group.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="55c1d-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="55c1d-125">Remarks</span></span>

<span data-ttu-id="55c1d-126">A classe **Win32 \_ LoadOrderGroupServiceMembers** é derivada do [**\_ componente CIM**](cim-component.md).</span><span class="sxs-lookup"><span data-stu-id="55c1d-126">The **Win32\_LoadOrderGroupServiceMembers** class is derived from [**CIM\_Component**](cim-component.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="55c1d-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="55c1d-127">Requirements</span></span>



| <span data-ttu-id="55c1d-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="55c1d-128">Requirement</span></span> | <span data-ttu-id="55c1d-129">Valor</span><span class="sxs-lookup"><span data-stu-id="55c1d-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="55c1d-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="55c1d-130">Minimum supported client</span></span><br/> | <span data-ttu-id="55c1d-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="55c1d-131">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="55c1d-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="55c1d-132">Minimum supported server</span></span><br/> | <span data-ttu-id="55c1d-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="55c1d-133">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="55c1d-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="55c1d-134">Namespace</span></span><br/>                | <span data-ttu-id="55c1d-135">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="55c1d-135">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="55c1d-136">MOF</span><span class="sxs-lookup"><span data-stu-id="55c1d-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="55c1d-137"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="55c1d-137"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="55c1d-138">DLL</span><span class="sxs-lookup"><span data-stu-id="55c1d-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="55c1d-139"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="55c1d-139"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55c1d-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="55c1d-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55c1d-141">**\_Componente CIM**</span><span class="sxs-lookup"><span data-stu-id="55c1d-141">**CIM\_Component**</span></span>](cim-component.md)
</dt> <dt>

<span data-ttu-id="55c1d-142">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="55c1d-142">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

