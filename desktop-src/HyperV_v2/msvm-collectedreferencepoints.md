---
description: Associa o Msvm \_ ReferencePointCollection aos \_ objetos Msvm VirtualSystemReferencePoint contidos.
ms.assetid: 826125c3-0a89-4573-ac28-88588eac248d
title: Classe Msvm_CollectedReferencePoints
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectedReferencePoints
- Msvm_CollectedReferencePoints.Collection
- Msvm_CollectedReferencePoints.Member
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 4891d4ec4c613c92c3b5d5a090f2683bfc77dc5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647530"
---
# <a name="msvm_collectedreferencepoints-class"></a><span data-ttu-id="7234a-103">\_Classe Msvm CollectedReferencePoints</span><span class="sxs-lookup"><span data-stu-id="7234a-103">Msvm\_CollectedReferencePoints class</span></span>

<span data-ttu-id="7234a-104">Associa o [**Msvm \_ ReferencePointCollection**](msvm-referencepointcollection.md) aos objetos [**Msvm \_ VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md) contidos.</span><span class="sxs-lookup"><span data-stu-id="7234a-104">Associates the [**Msvm\_ReferencePointCollection**](msvm-referencepointcollection.md) to the contained [**Msvm\_VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md) objects.</span></span>

<span data-ttu-id="7234a-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="7234a-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7234a-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7234a-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectedReferencePoints : CIM_CollectedMSEs
{
  Msvm_ReferencePointCollection    REF Collection;
  Msvm_VirtualSystemReferencePoint REF Member;
};
```

## <a name="members"></a><span data-ttu-id="7234a-107">Membros</span><span class="sxs-lookup"><span data-stu-id="7234a-107">Members</span></span>

<span data-ttu-id="7234a-108">A classe **Msvm \_ CollectedReferencePoints** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="7234a-108">The **Msvm\_CollectedReferencePoints** class has these types of members:</span></span>

-   [<span data-ttu-id="7234a-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="7234a-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7234a-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="7234a-110">Properties</span></span>

<span data-ttu-id="7234a-111">A classe **Msvm \_ CollectedReferencePoints** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="7234a-111">The **Msvm\_CollectedReferencePoints** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7234a-112">**Coleção**</span><span class="sxs-lookup"><span data-stu-id="7234a-112">**Collection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7234a-113">Tipo de dados: **Msvm \_ ReferencePointCollection**</span><span class="sxs-lookup"><span data-stu-id="7234a-113">Data type: **Msvm\_ReferencePointCollection**</span></span>
</dt> <dt>

<span data-ttu-id="7234a-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7234a-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7234a-115">Qualificadores: [**agregação**](/windows/desktop/WmiSdk/standard-qualifiers), [**substituição**](/windows/desktop/WmiSdk/standard-qualifiers) ("coleção")</span><span class="sxs-lookup"><span data-stu-id="7234a-115">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Collection")</span></span>
</dt> </dl>

<span data-ttu-id="7234a-116">Um [**Msvm \_ ReferencePointCollection**](msvm-referencepointcollection.md) GROUPING ou um objeto ' recipiente ' que representa a coleção.</span><span class="sxs-lookup"><span data-stu-id="7234a-116">An [**Msvm\_ReferencePointCollection**](msvm-referencepointcollection.md) grouping or 'bag' object that represents the collection.</span></span>

</dd> <dt>

<span data-ttu-id="7234a-117">**Membro**</span><span class="sxs-lookup"><span data-stu-id="7234a-117">**Member**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7234a-118">Tipo de dados: **Msvm \_ VirtualSystemReferencePoint**</span><span class="sxs-lookup"><span data-stu-id="7234a-118">Data type: **Msvm\_VirtualSystemReferencePoint**</span></span>
</dt> <dt>

<span data-ttu-id="7234a-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7234a-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7234a-120">Qualificadores: [**substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("membro")</span><span class="sxs-lookup"><span data-stu-id="7234a-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Member")</span></span>
</dt> </dl>

<span data-ttu-id="7234a-121">Um [**Msvm \_ VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md) que contém os membros da coleção.</span><span class="sxs-lookup"><span data-stu-id="7234a-121">An [**Msvm\_VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md) containing the members of the collection.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7234a-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7234a-122">Requirements</span></span>



| <span data-ttu-id="7234a-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="7234a-123">Requirement</span></span> | <span data-ttu-id="7234a-124">Valor</span><span class="sxs-lookup"><span data-stu-id="7234a-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7234a-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7234a-125">Minimum supported client</span></span><br/> | <span data-ttu-id="7234a-126">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="7234a-126">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="7234a-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7234a-127">Minimum supported server</span></span><br/> | <span data-ttu-id="7234a-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="7234a-128">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="7234a-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="7234a-129">Namespace</span></span><br/>                | <span data-ttu-id="7234a-130">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="7234a-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="7234a-131">MOF</span><span class="sxs-lookup"><span data-stu-id="7234a-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7234a-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7234a-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7234a-133">DLL</span><span class="sxs-lookup"><span data-stu-id="7234a-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7234a-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7234a-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7234a-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="7234a-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7234a-136">**\_COLLECTEDMSES CIM**</span><span class="sxs-lookup"><span data-stu-id="7234a-136">**CIM\_CollectedMSEs**</span></span>](cim-collectedmses.md)
</dt> </dl>

 

