---
description: Representa uma associação genérica entre dois elementos gerenciados que representam diferentes aspectos da mesma entidade subjacente.
ms.assetid: 28d153de-ce9c-4cd3-8995-0d959846be4d
title: Classe CIM_LogicalIdentity (gerenciamento do Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalIdentity
- CIM_LogicalIdentity.SystemElement
- CIM_LogicalIdentity.SameElement
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 71382910dc195c0fa6ef2456e1811d66d90a41e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105778765"
---
# <a name="cim_logicalidentity-class-hyper-v-management"></a><span data-ttu-id="222bb-103">Classe CIM_LogicalIdentity (gerenciamento do Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="222bb-103">CIM_LogicalIdentity class (Hyper-V management)</span></span>

<span data-ttu-id="222bb-104">Representa uma associação genérica entre dois elementos gerenciados que representam diferentes aspectos da mesma entidade subjacente.</span><span class="sxs-lookup"><span data-stu-id="222bb-104">Represents a generic association between two managed elements that represent different aspects of the same underlying entity.</span></span>

## <a name="syntax"></a><span data-ttu-id="222bb-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="222bb-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_LogicalIdentity
{
  CIM_ManagedElement REF SystemElement;
  CIM_ManagedElement REF SameElement;
};
```

## <a name="members"></a><span data-ttu-id="222bb-106">Membros</span><span class="sxs-lookup"><span data-stu-id="222bb-106">Members</span></span>

<span data-ttu-id="222bb-107">A classe **CIM \_ LogicalIdentity** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="222bb-107">The **CIM\_LogicalIdentity** class has these types of members:</span></span>

-   [<span data-ttu-id="222bb-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="222bb-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="222bb-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="222bb-109">Properties</span></span>

<span data-ttu-id="222bb-110">A classe **CIM \_ LogicalIdentity** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="222bb-110">The **CIM\_LogicalIdentity** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="222bb-111">**Mesmoelement**</span><span class="sxs-lookup"><span data-stu-id="222bb-111">**SameElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="222bb-112">Tipo de dados: **CIM \_ managedelement**</span><span class="sxs-lookup"><span data-stu-id="222bb-112">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="222bb-113">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="222bb-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="222bb-114">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="222bb-114">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="222bb-115">O segundo aspecto na associação.</span><span class="sxs-lookup"><span data-stu-id="222bb-115">The second aspect in the association.</span></span>

</dd> <dt>

<span data-ttu-id="222bb-116">**Sistema de**</span><span class="sxs-lookup"><span data-stu-id="222bb-116">**SystemElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="222bb-117">Tipo de dados: **CIM \_ managedelement**</span><span class="sxs-lookup"><span data-stu-id="222bb-117">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="222bb-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="222bb-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="222bb-119">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="222bb-119">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="222bb-120">O primeiro aspecto na associação.</span><span class="sxs-lookup"><span data-stu-id="222bb-120">The first aspect in the association.</span></span> <span data-ttu-id="222bb-121">O uso do sistema no nome da propriedade não limita o escopo da associação.</span><span class="sxs-lookup"><span data-stu-id="222bb-121">The use of System in the property name does not limit the scope of the association.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="222bb-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="222bb-122">Requirements</span></span>



| <span data-ttu-id="222bb-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="222bb-123">Requirement</span></span> | <span data-ttu-id="222bb-124">Valor</span><span class="sxs-lookup"><span data-stu-id="222bb-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="222bb-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="222bb-125">Minimum supported client</span></span><br/> | <span data-ttu-id="222bb-126">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="222bb-126">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="222bb-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="222bb-127">Minimum supported server</span></span><br/> | <span data-ttu-id="222bb-128">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="222bb-128">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="222bb-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="222bb-129">Namespace</span></span><br/>                | <span data-ttu-id="222bb-130">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="222bb-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="222bb-131">MOF</span><span class="sxs-lookup"><span data-stu-id="222bb-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="222bb-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="222bb-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="222bb-133">DLL</span><span class="sxs-lookup"><span data-stu-id="222bb-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="222bb-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="222bb-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

