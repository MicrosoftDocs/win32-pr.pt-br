---
description: A \_ classe WMI de associação do Win32 LoadOrderGroupServiceDependencies relaciona um serviço base e um grupo de ordem de carregamento do qual o serviço depende para iniciar a execução.
ms.assetid: 56739b80-9028-4a2e-85ed-973a078860c1
ms.tgt_platform: multiple
title: Classe Win32_LoadOrderGroupServiceDependencies
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LoadOrderGroupServiceDependencies
- Win32_LoadOrderGroupServiceDependencies.Antecedent
- Win32_LoadOrderGroupServiceDependencies.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b95d1aa01def951802434e787931ce348d04ccb6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089537"
---
# <a name="win32_loadordergroupservicedependencies-class"></a><span data-ttu-id="ec7ee-103">\_Classe Win32 LoadOrderGroupServiceDependencies</span><span class="sxs-lookup"><span data-stu-id="ec7ee-103">Win32\_LoadOrderGroupServiceDependencies class</span></span>

<span data-ttu-id="ec7ee-104">A [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) de associação do **Win32 \_ LoadOrderGroupServiceDependencies** relaciona um serviço base e um grupo de ordem de carregamento do qual o serviço depende para iniciar a execução.</span><span class="sxs-lookup"><span data-stu-id="ec7ee-104">The **Win32\_LoadOrderGroupServiceDependencies** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a base service and a load order group that the service depends on to start running.</span></span>

<span data-ttu-id="ec7ee-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="ec7ee-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="ec7ee-106">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="ec7ee-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec7ee-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ec7ee-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4FC-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_LoadOrderGroupServiceDependencies : CIM_Dependency
{
  Win32_LoadOrderGroup REF Antecedent;
  Win32_BaseService    REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="ec7ee-108">Membros</span><span class="sxs-lookup"><span data-stu-id="ec7ee-108">Members</span></span>

<span data-ttu-id="ec7ee-109">A classe **Win32 \_ LoadOrderGroupServiceDependencies** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="ec7ee-109">The **Win32\_LoadOrderGroupServiceDependencies** class has these types of members:</span></span>

-   [<span data-ttu-id="ec7ee-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ec7ee-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ec7ee-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ec7ee-111">Properties</span></span>

<span data-ttu-id="ec7ee-112">A classe **Win32 \_ LoadOrderGroupServiceDependencies** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="ec7ee-112">The **Win32\_LoadOrderGroupServiceDependencies** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ec7ee-113">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="ec7ee-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec7ee-114">Tipo de dados: **Win32 \_ loadordergroup**</span><span class="sxs-lookup"><span data-stu-id="ec7ee-114">Data type: **Win32\_LoadOrderGroup**</span></span>
</dt> <dt>

<span data-ttu-id="ec7ee-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ec7ee-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ec7ee-116">Qualificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecessor"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ loadorder OrderGroup")</span><span class="sxs-lookup"><span data-stu-id="ec7ee-116">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_LoadOrderGroup")</span></span>
</dt> </dl>

<span data-ttu-id="ec7ee-117">A referência à instância que representa as propriedades do grupo de ordens de carga que deve iniciar antes que o serviço base dependente dessa classe possa ser iniciada.</span><span class="sxs-lookup"><span data-stu-id="ec7ee-117">Reference to the instance representing the properties of the load order group that must start before the dependent base service of this class can start.</span></span>

</dd> <dt>

<span data-ttu-id="ec7ee-118">**Depende**</span><span class="sxs-lookup"><span data-stu-id="ec7ee-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec7ee-119">Tipo de dados: **Win32 \_ BaseService**</span><span class="sxs-lookup"><span data-stu-id="ec7ee-119">Data type: **Win32\_BaseService**</span></span>
</dt> <dt>

<span data-ttu-id="ec7ee-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ec7ee-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ec7ee-121">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**substituição**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ BaseService")</span><span class="sxs-lookup"><span data-stu-id="ec7ee-121">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_BaseService")</span></span>
</dt> </dl>

<span data-ttu-id="ec7ee-122">Referência à instância que representa as propriedades do serviço de base dependente do grupo de ordem de carregamento para iniciar a execução.</span><span class="sxs-lookup"><span data-stu-id="ec7ee-122">Reference to the instance representing the properties of the base service that is dependent upon the load order group to start running.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ec7ee-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="ec7ee-123">Remarks</span></span>

<span data-ttu-id="ec7ee-124">A classe **Win32 \_ LoadOrderGroupServiceDependencies** é derivada da [**\_ dependência CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="ec7ee-124">The **Win32\_LoadOrderGroupServiceDependencies** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ec7ee-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ec7ee-125">Requirements</span></span>



| <span data-ttu-id="ec7ee-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="ec7ee-126">Requirement</span></span> | <span data-ttu-id="ec7ee-127">Valor</span><span class="sxs-lookup"><span data-stu-id="ec7ee-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ec7ee-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ec7ee-128">Minimum supported client</span></span><br/> | <span data-ttu-id="ec7ee-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ec7ee-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ec7ee-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ec7ee-130">Minimum supported server</span></span><br/> | <span data-ttu-id="ec7ee-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ec7ee-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ec7ee-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="ec7ee-132">Namespace</span></span><br/>                | <span data-ttu-id="ec7ee-133">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="ec7ee-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ec7ee-134">MOF</span><span class="sxs-lookup"><span data-stu-id="ec7ee-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ec7ee-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ec7ee-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ec7ee-136">DLL</span><span class="sxs-lookup"><span data-stu-id="ec7ee-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ec7ee-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ec7ee-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec7ee-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="ec7ee-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec7ee-139">**\_Dependência CIM**</span><span class="sxs-lookup"><span data-stu-id="ec7ee-139">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> <dt>

<span data-ttu-id="ec7ee-140">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ec7ee-140">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

