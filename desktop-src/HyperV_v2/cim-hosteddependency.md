---
description: Representa uma associação em que um elemento gerenciado é hospedado por outro.
ms.assetid: ae8476f7-38a4-4d08-a7dc-21e120d3cbe1
title: Classe CIM_HostedDependency
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_HostedDependency
- CIM_HostedDependency.Antecedent
- CIM_HostedDependency.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 551931fd88fac88f85bcc8ffd51423538de3bb5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105759884"
---
# <a name="cim_hosteddependency-class"></a><span data-ttu-id="25299-103">\_Classe CIM HostedDependency</span><span class="sxs-lookup"><span data-stu-id="25299-103">CIM\_HostedDependency class</span></span>

<span data-ttu-id="25299-104">Representa uma associação em que um elemento gerenciado é hospedado por outro.</span><span class="sxs-lookup"><span data-stu-id="25299-104">Represents an association where a managed element is hosted by another.</span></span>

## <a name="syntax"></a><span data-ttu-id="25299-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="25299-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.8.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_HostedDependency : CIM_Dependency
{
  CIM_ManagedElement REF Antecedent;
  CIM_ManagedElement REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="25299-106">Membros</span><span class="sxs-lookup"><span data-stu-id="25299-106">Members</span></span>

<span data-ttu-id="25299-107">A classe **CIM \_ HostedDependency** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="25299-107">The **CIM\_HostedDependency** class has these types of members:</span></span>

-   [<span data-ttu-id="25299-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="25299-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="25299-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="25299-109">Properties</span></span>

<span data-ttu-id="25299-110">A classe **CIM \_ HostedDependency** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="25299-110">The **CIM\_HostedDependency** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="25299-111">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="25299-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25299-112">Tipo de dados: **CIM \_ managedelement**</span><span class="sxs-lookup"><span data-stu-id="25299-112">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="25299-113">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="25299-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="25299-114">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="25299-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="25299-115">O elemento gerenciado pelo host.</span><span class="sxs-lookup"><span data-stu-id="25299-115">The host managed element.</span></span>

</dd> <dt>

<span data-ttu-id="25299-116">**Depende**</span><span class="sxs-lookup"><span data-stu-id="25299-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25299-117">Tipo de dados: **CIM \_ managedelement**</span><span class="sxs-lookup"><span data-stu-id="25299-117">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="25299-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="25299-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="25299-119">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")</span><span class="sxs-lookup"><span data-stu-id="25299-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="25299-120">O elemento gerenciado hospedado.</span><span class="sxs-lookup"><span data-stu-id="25299-120">The hosted managed element.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="25299-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="25299-121">Requirements</span></span>



| <span data-ttu-id="25299-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="25299-122">Requirement</span></span> | <span data-ttu-id="25299-123">Valor</span><span class="sxs-lookup"><span data-stu-id="25299-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="25299-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="25299-124">Minimum supported client</span></span><br/> | <span data-ttu-id="25299-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="25299-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="25299-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="25299-126">Minimum supported server</span></span><br/> | <span data-ttu-id="25299-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="25299-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="25299-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="25299-128">Namespace</span></span><br/>                | <span data-ttu-id="25299-129">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="25299-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="25299-130">MOF</span><span class="sxs-lookup"><span data-stu-id="25299-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="25299-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="25299-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="25299-132">DLL</span><span class="sxs-lookup"><span data-stu-id="25299-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="25299-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="25299-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="25299-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="25299-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25299-135">**\_Dependência CIM**</span><span class="sxs-lookup"><span data-stu-id="25299-135">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

