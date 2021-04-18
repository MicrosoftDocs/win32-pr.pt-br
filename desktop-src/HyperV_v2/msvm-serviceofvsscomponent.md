---
description: Uma associação entre uma instância de Msvm \_ VssComponent e uma instância de Msvm \_ VssService que representa um serviço para executar operações no componente do VSS.
ms.assetid: 19fdf2e3-48c4-452b-89d0-ec0b8681fca2
title: Classe Msvm_ServiceOfVssComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ServiceOfVssComponent
- Msvm_ServiceOfVssComponent.Antecedent
- Msvm_ServiceOfVssComponent.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 5787dcdd4d8ce1aeefdc1fbafb2c156aec4d467a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105770213"
---
# <a name="msvm_serviceofvsscomponent-class"></a><span data-ttu-id="12d91-103">\_Classe Msvm ServiceOfVssComponent</span><span class="sxs-lookup"><span data-stu-id="12d91-103">Msvm\_ServiceOfVssComponent class</span></span>

<span data-ttu-id="12d91-104">Uma associação entre uma instância de [**Msvm \_ VssComponent**](msvm-vsscomponent.md) e uma instância de [**Msvm \_ VssService**](msvm-vssservice.md) que representa um serviço para executar operações no componente do VSS.</span><span class="sxs-lookup"><span data-stu-id="12d91-104">An association between an instance of [**Msvm\_VssComponent**](msvm-vsscomponent.md) and an instance of [**Msvm\_VssService**](msvm-vssservice.md) that represents a service for performing operations on the VSS component.</span></span>

<span data-ttu-id="12d91-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="12d91-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="12d91-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="12d91-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ServiceOfVssComponent : CIM_Dependency
{
  Msvm_VssComponent REF Antecedent;
  Msvm_VssService   REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="12d91-107">Membros</span><span class="sxs-lookup"><span data-stu-id="12d91-107">Members</span></span>

<span data-ttu-id="12d91-108">A classe **Msvm \_ ServiceOfVssComponent** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="12d91-108">The **Msvm\_ServiceOfVssComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="12d91-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="12d91-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="12d91-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="12d91-110">Properties</span></span>

<span data-ttu-id="12d91-111">A classe **Msvm \_ ServiceOfVssComponent** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="12d91-111">The **Msvm\_ServiceOfVssComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="12d91-112">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="12d91-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12d91-113">Tipo de dados: **Msvm \_ VssComponent**</span><span class="sxs-lookup"><span data-stu-id="12d91-113">Data type: **Msvm\_VssComponent**</span></span>
</dt> <dt>

<span data-ttu-id="12d91-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="12d91-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12d91-115">Qualificadores: [**substituir**](/windows/desktop/WmiSdk/standard-qualifiers) (" \_ dependência CIM. Antecedent")</span><span class="sxs-lookup"><span data-stu-id="12d91-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_Dependency.Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="12d91-116">A, [**Msvm \_ VssComponent**](msvm-vsscomponent.md) que representa o componente do VSS.</span><span class="sxs-lookup"><span data-stu-id="12d91-116">A, [**Msvm\_VssComponent**](msvm-vsscomponent.md) that represents the VSS component.</span></span>

</dd> <dt>

<span data-ttu-id="12d91-117">**Depende**</span><span class="sxs-lookup"><span data-stu-id="12d91-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12d91-118">Tipo de dados: **Msvm \_ VssService**</span><span class="sxs-lookup"><span data-stu-id="12d91-118">Data type: **Msvm\_VssService**</span></span>
</dt> <dt>

<span data-ttu-id="12d91-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="12d91-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12d91-120">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (" \_ dependência CIM. dependent")</span><span class="sxs-lookup"><span data-stu-id="12d91-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_Dependency.Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="12d91-121">Um [**\_ VssService Msvm**](msvm-vssservice.md) que representa o serviço VSS IC.</span><span class="sxs-lookup"><span data-stu-id="12d91-121">An [**Msvm\_VssService**](msvm-vssservice.md) that represents the VSS IC service.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="12d91-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="12d91-122">Requirements</span></span>



| <span data-ttu-id="12d91-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="12d91-123">Requirement</span></span> | <span data-ttu-id="12d91-124">Valor</span><span class="sxs-lookup"><span data-stu-id="12d91-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12d91-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="12d91-125">Minimum supported client</span></span><br/> | <span data-ttu-id="12d91-126">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="12d91-126">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="12d91-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="12d91-127">Minimum supported server</span></span><br/> | <span data-ttu-id="12d91-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="12d91-128">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="12d91-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="12d91-129">Namespace</span></span><br/>                | <span data-ttu-id="12d91-130">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="12d91-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="12d91-131">MOF</span><span class="sxs-lookup"><span data-stu-id="12d91-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="12d91-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="12d91-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="12d91-133">DLL</span><span class="sxs-lookup"><span data-stu-id="12d91-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="12d91-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="12d91-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="12d91-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="12d91-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12d91-136">**\_Dependência CIM**</span><span class="sxs-lookup"><span data-stu-id="12d91-136">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

