---
description: Representa uma associação genérica usada para estabelecer relações de dependência entre elementos gerenciados.
ms.assetid: a81beedc-5473-49a6-8e7f-67e831d3e8bc
title: Classe CIM_Dependency (gerenciamento do Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Dependency
- CIM_Dependency.Antecedent
- CIM_Dependency.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 4e85f59b190e0024fc34489315fa2fae1c0d6b34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105764693"
---
# <a name="cim_dependency-class-hyper-v-management"></a><span data-ttu-id="f7a44-103">Classe CIM_Dependency (gerenciamento do Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="f7a44-103">CIM_Dependency class (Hyper-V management)</span></span>

<span data-ttu-id="f7a44-104">Representa uma associação genérica usada para estabelecer relações de dependência entre elementos gerenciados.</span><span class="sxs-lookup"><span data-stu-id="f7a44-104">Represents a generic association used to establish dependency relationships between managed elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7a44-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f7a44-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_Dependency
{
  CIM_ManagedElement REF Antecedent;
  CIM_ManagedElement REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="f7a44-106">Membros</span><span class="sxs-lookup"><span data-stu-id="f7a44-106">Members</span></span>

<span data-ttu-id="f7a44-107">A classe de **\_ dependência CIM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="f7a44-107">The **CIM\_Dependency** class has these types of members:</span></span>

-   [<span data-ttu-id="f7a44-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f7a44-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f7a44-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f7a44-109">Properties</span></span>

<span data-ttu-id="f7a44-110">A classe de **\_ dependência CIM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="f7a44-110">The **CIM\_Dependency** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f7a44-111">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="f7a44-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7a44-112">Tipo de dados: **CIM \_ managedelement**</span><span class="sxs-lookup"><span data-stu-id="f7a44-112">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="f7a44-113">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f7a44-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f7a44-114">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f7a44-114">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f7a44-115">O objeto independente nesta associação.</span><span class="sxs-lookup"><span data-stu-id="f7a44-115">The independent object in this association.</span></span>

</dd> <dt>

<span data-ttu-id="f7a44-116">**Depende**</span><span class="sxs-lookup"><span data-stu-id="f7a44-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7a44-117">Tipo de dados: **CIM \_ managedelement**</span><span class="sxs-lookup"><span data-stu-id="f7a44-117">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="f7a44-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f7a44-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f7a44-119">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f7a44-119">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f7a44-120">O objeto dependente na associação.</span><span class="sxs-lookup"><span data-stu-id="f7a44-120">The dependent object in the association.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f7a44-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f7a44-121">Requirements</span></span>



| <span data-ttu-id="f7a44-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="f7a44-122">Requirement</span></span> | <span data-ttu-id="f7a44-123">Valor</span><span class="sxs-lookup"><span data-stu-id="f7a44-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7a44-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f7a44-124">Minimum supported client</span></span><br/> | <span data-ttu-id="f7a44-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="f7a44-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="f7a44-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f7a44-126">Minimum supported server</span></span><br/> | <span data-ttu-id="f7a44-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f7a44-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="f7a44-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="f7a44-128">Namespace</span></span><br/>                | <span data-ttu-id="f7a44-129">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="f7a44-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="f7a44-130">MOF</span><span class="sxs-lookup"><span data-stu-id="f7a44-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f7a44-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f7a44-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f7a44-132">DLL</span><span class="sxs-lookup"><span data-stu-id="f7a44-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f7a44-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f7a44-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

