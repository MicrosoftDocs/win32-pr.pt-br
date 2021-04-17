---
description: Representa uma associação na qual um elemento gerenciado está em conformidade com o padrão de um perfil registrado.
ms.assetid: 9d5704b6-c764-4f68-bce3-384d5a244e28
title: Classe CIM_ElementConformsToProfile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ElementConformsToProfile
- CIM_ElementConformsToProfile.ConformantStandard
- CIM_ElementConformsToProfile.ManagedElement
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7034001641029099d1b52090b3cc518b6589dc50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105811881"
---
# <a name="cim_elementconformstoprofile-class"></a><span data-ttu-id="f1375-103">\_Classe CIM ElementConformsToProfile</span><span class="sxs-lookup"><span data-stu-id="f1375-103">CIM\_ElementConformsToProfile class</span></span>

<span data-ttu-id="f1375-104">Representa uma associação na qual um elemento gerenciado está em conformidade com o padrão de um perfil registrado.</span><span class="sxs-lookup"><span data-stu-id="f1375-104">Represents an association in which a managed element conforms to the standard of a registered profile.</span></span> <span data-ttu-id="f1375-105">Essa associação geralmente se aplica a uma instância de nível superior, como um sistema, namespace ou serviço.</span><span class="sxs-lookup"><span data-stu-id="f1375-105">This association usually applies to a higher level instance, such as a system, namespace, or service.</span></span> <span data-ttu-id="f1375-106">Quando aplicado a uma instância de nível superior, todas as partes constituintes devem se comportar adequadamente para dar suporte à conformidade do Managedelement com o RegisteredProfile nomeado.</span><span class="sxs-lookup"><span data-stu-id="f1375-106">When applied to a higher level instance, all constituent parts MUST behave appropriately in support of the ManagedElement's conformance to the named RegisteredProfile.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1375-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f1375-107">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.8.0"), UMLPackagePath("CIM::Interop")]
class CIM_ElementConformsToProfile
{
  CIM_RegisteredProfile REF ConformantStandard;
  CIM_ManagedElement    REF ManagedElement;
};
```

## <a name="members"></a><span data-ttu-id="f1375-108">Membros</span><span class="sxs-lookup"><span data-stu-id="f1375-108">Members</span></span>

<span data-ttu-id="f1375-109">A classe **CIM \_ ElementConformsToProfile** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="f1375-109">The **CIM\_ElementConformsToProfile** class has these types of members:</span></span>

-   [<span data-ttu-id="f1375-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f1375-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f1375-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f1375-111">Properties</span></span>

<span data-ttu-id="f1375-112">A classe **CIM \_ ElementConformsToProfile** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="f1375-112">The **CIM\_ElementConformsToProfile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f1375-113">**ConformantStandard**</span><span class="sxs-lookup"><span data-stu-id="f1375-113">**ConformantStandard**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1375-114">Tipo de dados: **CIM \_ RegisteredProfile**</span><span class="sxs-lookup"><span data-stu-id="f1375-114">Data type: **CIM\_RegisteredProfile**</span></span>
</dt> <dt>

<span data-ttu-id="f1375-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f1375-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1375-116">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f1375-116">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f1375-117">O perfil registrado no qual o elemento gerenciado está em conformidade.</span><span class="sxs-lookup"><span data-stu-id="f1375-117">The registered profile to which the managed element conforms.</span></span>

</dd> <dt>

<span data-ttu-id="f1375-118">**Managedelement**</span><span class="sxs-lookup"><span data-stu-id="f1375-118">**ManagedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1375-119">Tipo de dados: **CIM \_ managedelement**</span><span class="sxs-lookup"><span data-stu-id="f1375-119">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="f1375-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f1375-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1375-121">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f1375-121">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f1375-122">O elemento gerenciado que está de acordo com o perfil registrado.</span><span class="sxs-lookup"><span data-stu-id="f1375-122">The managed element that conforms to the registered profile.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f1375-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f1375-123">Requirements</span></span>



| <span data-ttu-id="f1375-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1375-124">Requirement</span></span> | <span data-ttu-id="f1375-125">Valor</span><span class="sxs-lookup"><span data-stu-id="f1375-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1375-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f1375-126">Minimum supported client</span></span><br/> | <span data-ttu-id="f1375-127">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="f1375-127">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="f1375-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f1375-128">Minimum supported server</span></span><br/> | <span data-ttu-id="f1375-129">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="f1375-129">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="f1375-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="f1375-130">Namespace</span></span><br/>                | <span data-ttu-id="f1375-131">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="f1375-131">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="f1375-132">MOF</span><span class="sxs-lookup"><span data-stu-id="f1375-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f1375-133"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f1375-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f1375-134">DLL</span><span class="sxs-lookup"><span data-stu-id="f1375-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f1375-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f1375-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

