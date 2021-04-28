---
description: Msvm_CollectedVirtualSystems classe – associa os \_ VirtualSystemCollection Msvm aos \_ objetos Msvm ComputerSystem contidos.
ms.assetid: ad783188-b60a-4271-aa2d-8050c36e70eb
title: Classe Msvm_CollectedVirtualSystems
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectedVirtualSystems
- Msvm_CollectedVirtualSystems.Collection
- Msvm_CollectedVirtualSystems.Member
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d6775f41a6e2ae7e45bac642fcd32b8deaec3fda
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119274"
---
# <a name="msvm_collectedvirtualsystems-class"></a><span data-ttu-id="efc47-103">\_Classe Msvm CollectedVirtualSystems</span><span class="sxs-lookup"><span data-stu-id="efc47-103">Msvm\_CollectedVirtualSystems class</span></span>

<span data-ttu-id="efc47-104">Associa o [**Msvm \_ VirtualSystemCollection**](msvm-virtualsystemcollection.md) aos objetos [**Msvm \_ ComputerSystem**](msvm-computersystem.md) contidos.</span><span class="sxs-lookup"><span data-stu-id="efc47-104">Associates the [**Msvm\_VirtualSystemCollection**](msvm-virtualsystemcollection.md) to the contained [**Msvm\_ComputerSystem**](msvm-computersystem.md) objects.</span></span>

<span data-ttu-id="efc47-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="efc47-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="efc47-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="efc47-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectedVirtualSystems : CIM_CollectedMSEs
{
  Msvm_VirtualSystemCollection REF Collection;
  Msvm_ComputerSystem          REF Member;
};
```

## <a name="members"></a><span data-ttu-id="efc47-107">Membros</span><span class="sxs-lookup"><span data-stu-id="efc47-107">Members</span></span>

<span data-ttu-id="efc47-108">A classe **Msvm \_ CollectedVirtualSystems** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="efc47-108">The **Msvm\_CollectedVirtualSystems** class has these types of members:</span></span>

-   [<span data-ttu-id="efc47-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="efc47-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="efc47-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="efc47-110">Properties</span></span>

<span data-ttu-id="efc47-111">A classe **Msvm \_ CollectedVirtualSystems** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="efc47-111">The **Msvm\_CollectedVirtualSystems** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="efc47-112">**Coleção**</span><span class="sxs-lookup"><span data-stu-id="efc47-112">**Collection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efc47-113">Tipo de dados: **Msvm \_ VirtualSystemCollection**</span><span class="sxs-lookup"><span data-stu-id="efc47-113">Data type: **Msvm\_VirtualSystemCollection**</span></span>
</dt> <dt>

<span data-ttu-id="efc47-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="efc47-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="efc47-115">Qualificadores: [**agregação**](/windows/desktop/WmiSdk/standard-qualifiers), [**substituição**](/windows/desktop/WmiSdk/standard-qualifiers) ("coleção")</span><span class="sxs-lookup"><span data-stu-id="efc47-115">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Collection")</span></span>
</dt> </dl>

<span data-ttu-id="efc47-116">Um [**Msvm \_ VirtualSystemCollection**](msvm-virtualsystemcollection.md) GROUPING ou um objeto ' recipiente ' que representa a coleção.</span><span class="sxs-lookup"><span data-stu-id="efc47-116">An [**Msvm\_VirtualSystemCollection**](msvm-virtualsystemcollection.md) grouping or 'bag' object that represents the collection.</span></span>

</dd> <dt>

<span data-ttu-id="efc47-117">**Membro**</span><span class="sxs-lookup"><span data-stu-id="efc47-117">**Member**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efc47-118">Tipo de dados: **Msvm \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="efc47-118">Data type: **Msvm\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="efc47-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="efc47-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="efc47-120">Qualificadores: [**substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("membro")</span><span class="sxs-lookup"><span data-stu-id="efc47-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Member")</span></span>
</dt> </dl>

<span data-ttu-id="efc47-121">Um objeto de [**\_ ComputerSystem Msvm**](msvm-computersystem.md) que contém os membros da coleção.</span><span class="sxs-lookup"><span data-stu-id="efc47-121">An [**Msvm\_ComputerSystem**](msvm-computersystem.md) object containing the members of the collection.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="efc47-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="efc47-122">Requirements</span></span>



| <span data-ttu-id="efc47-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="efc47-123">Requirement</span></span> | <span data-ttu-id="efc47-124">Valor</span><span class="sxs-lookup"><span data-stu-id="efc47-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="efc47-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="efc47-125">Minimum supported client</span></span><br/> | <span data-ttu-id="efc47-126">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="efc47-126">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="efc47-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="efc47-127">Minimum supported server</span></span><br/> | <span data-ttu-id="efc47-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="efc47-128">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="efc47-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="efc47-129">Namespace</span></span><br/>                | <span data-ttu-id="efc47-130">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="efc47-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="efc47-131">MOF</span><span class="sxs-lookup"><span data-stu-id="efc47-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="efc47-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="efc47-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="efc47-133">DLL</span><span class="sxs-lookup"><span data-stu-id="efc47-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="efc47-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="efc47-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="efc47-135">Consulte também</span><span class="sxs-lookup"><span data-stu-id="efc47-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="efc47-136">**\_COLLECTEDMSES CIM**</span><span class="sxs-lookup"><span data-stu-id="efc47-136">**CIM\_CollectedMSEs**</span></span>](cim-collectedmses.md)
</dt> </dl>

 

