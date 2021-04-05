---
description: Representa uma associação entre uma instância de Msvm \_ GuestServiceInterfaceComponent e uma instância de Msvm \_ GuestService, que representa um serviço em execução no convidado.
ms.assetid: 246CFAC1-7D83-4DE7-B9D3-96326511E08B
title: Classe Msvm_RegisteredGuestService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_RegisteredGuestService
- Msvm_RegisteredGuestService.Antecedent
- Msvm_RegisteredGuestService.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 850d7f081b070fd34ef11bc56e8cd1f914e498b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662286"
---
# <a name="msvm_registeredguestservice-class"></a><span data-ttu-id="48699-103">\_Classe Msvm RegisteredGuestService</span><span class="sxs-lookup"><span data-stu-id="48699-103">Msvm\_RegisteredGuestService class</span></span>

<span data-ttu-id="48699-104">Representa uma associação entre uma instância de [**Msvm \_ GuestServiceInterfaceComponent**](msvm-guestserviceinterfacecomponent.md) e uma instância de [**Msvm \_ GuestService**](msvm-guestservice.md), que representa um serviço em execução no convidado.</span><span class="sxs-lookup"><span data-stu-id="48699-104">Represents an association between an instance of [**Msvm\_GuestServiceInterfaceComponent**](msvm-guestserviceinterfacecomponent.md) and an instance of [**Msvm\_GuestService**](msvm-guestservice.md), which represents a service running in the guest.</span></span> <span data-ttu-id="48699-105">Essa classe deriva da classe de [**\_ dependência CIM**](/windows/desktop/CIMWin32Prov/cim-dependency) .</span><span class="sxs-lookup"><span data-stu-id="48699-105">This class derives from the [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency) class.</span></span>

<span data-ttu-id="48699-106">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="48699-106">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="48699-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="48699-107">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_RegisteredGuestService : CIM_Dependency
{
  Msvm_GuestServiceInterfaceComponent REF Antecedent;
  Msvm_GuestService                   REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="48699-108">Membros</span><span class="sxs-lookup"><span data-stu-id="48699-108">Members</span></span>

<span data-ttu-id="48699-109">A classe **Msvm \_ RegisteredGuestService** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="48699-109">The **Msvm\_RegisteredGuestService** class has these types of members:</span></span>

-   [<span data-ttu-id="48699-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="48699-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="48699-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="48699-111">Properties</span></span>

<span data-ttu-id="48699-112">A classe **Msvm \_ RegisteredGuestService** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="48699-112">The **Msvm\_RegisteredGuestService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="48699-113">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="48699-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48699-114">Tipo de dados: **[ **Msvm \_ GuestServiceInterfaceComponent**](msvm-guestserviceinterfacecomponent.md)**</span><span class="sxs-lookup"><span data-stu-id="48699-114">Data type: **[**Msvm\_GuestServiceInterfaceComponent**](msvm-guestserviceinterfacecomponent.md)**</span></span>
</dt> <dt>

<span data-ttu-id="48699-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="48699-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48699-116">Qualificadores: [**substituir**](/windows/desktop/WmiSdk/standard-qualifiers) (" \_ dependência CIM. Antecedent")</span><span class="sxs-lookup"><span data-stu-id="48699-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_Dependency.Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="48699-117">Referência ao componente de interface do serviço de convidado nesta associação.</span><span class="sxs-lookup"><span data-stu-id="48699-117">Reference to the guest service interface component in this association.</span></span>

</dd> <dt>

<span data-ttu-id="48699-118">**Depende**</span><span class="sxs-lookup"><span data-stu-id="48699-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48699-119">Tipo de dados: **[ **Msvm \_ GuestService**](msvm-guestservice.md)**</span><span class="sxs-lookup"><span data-stu-id="48699-119">Data type: **[**Msvm\_GuestService**](msvm-guestservice.md)**</span></span>
</dt> <dt>

<span data-ttu-id="48699-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="48699-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48699-121">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (" \_ dependência CIM. dependent")</span><span class="sxs-lookup"><span data-stu-id="48699-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_Dependency.Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="48699-122">Referência ao serviço convidado registrado que é dependente da propriedade **Antecedent** .</span><span class="sxs-lookup"><span data-stu-id="48699-122">Reference to the registered guest service that is dependent on the **Antecedent** property.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="48699-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="48699-123">Requirements</span></span>



| <span data-ttu-id="48699-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="48699-124">Requirement</span></span> | <span data-ttu-id="48699-125">Valor</span><span class="sxs-lookup"><span data-stu-id="48699-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48699-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="48699-126">Minimum supported client</span></span><br/> | <span data-ttu-id="48699-127">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="48699-127">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="48699-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="48699-128">Minimum supported server</span></span><br/> | <span data-ttu-id="48699-129">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="48699-129">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="48699-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="48699-130">Namespace</span></span><br/>                | <span data-ttu-id="48699-131">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="48699-131">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="48699-132">MOF</span><span class="sxs-lookup"><span data-stu-id="48699-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="48699-133"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="48699-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="48699-134">DLL</span><span class="sxs-lookup"><span data-stu-id="48699-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="48699-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="48699-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="48699-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="48699-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48699-137">**\_Dependência CIM**</span><span class="sxs-lookup"><span data-stu-id="48699-137">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> <dt>

[<span data-ttu-id="48699-138">**\_Dependência CIM**</span><span class="sxs-lookup"><span data-stu-id="48699-138">**CIM\_Dependency**</span></span>](/windows/desktop/CIMWin32Prov/cim-dependency)
</dt> </dl>

 

