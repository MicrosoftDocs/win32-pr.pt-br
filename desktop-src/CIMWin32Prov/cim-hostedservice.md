---
description: A \_ classe CIM HostedService representa uma associação entre um serviço e o sistema no qual a funcionalidade reside.
ms.assetid: 23bb385d-dd22-4126-aea9-d2f22527223e
ms.tgt_platform: multiple
title: Classe CIM_HostedService (provedores WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_HostedService
- CIM_HostedService.Dependent
- CIM_HostedService.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c63b28fed7977c9fce78fe1030afbe66d5b2d75e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105752965"
---
# <a name="cim_hostedservice-class-cimwin32-wmi-providers"></a><span data-ttu-id="e4db0-103">Classe CIM_HostedService (provedores WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="e4db0-103">CIM_HostedService class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="e4db0-104">A classe **CIM \_ HostedService** representa uma associação entre um serviço e o sistema no qual a funcionalidade reside.</span><span class="sxs-lookup"><span data-stu-id="e4db0-104">The **CIM\_HostedService** class represents an association between a service and the system on which the functionality resides.</span></span> <span data-ttu-id="e4db0-105">Um sistema pode hospedar muitos serviços, o que adia para o sistema de hospedagem.</span><span class="sxs-lookup"><span data-stu-id="e4db0-105">A system may host many services, which defer to the hosting system.</span></span> <span data-ttu-id="e4db0-106">O modelo não representa serviços hospedados em vários sistemas.</span><span class="sxs-lookup"><span data-stu-id="e4db0-106">The model does not represent services hosted across multiple systems.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e4db0-107">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="e4db0-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="e4db0-108">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="e4db0-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="e4db0-109">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="e4db0-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="e4db0-110">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="e4db0-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4db0-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e4db0-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{83B2A7AA-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_HostedService : CIM_Dependency
{
  CIM_Service REF Dependent;
  CIM_System  REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="e4db0-112">Membros</span><span class="sxs-lookup"><span data-stu-id="e4db0-112">Members</span></span>

<span data-ttu-id="e4db0-113">A classe **CIM \_ HostedService** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="e4db0-113">The **CIM\_HostedService** class has these types of members:</span></span>

-   [<span data-ttu-id="e4db0-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e4db0-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e4db0-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e4db0-115">Properties</span></span>

<span data-ttu-id="e4db0-116">A classe **CIM \_ HostedService** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="e4db0-116">The **CIM\_HostedService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e4db0-117">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="e4db0-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4db0-118">Tipo de dados **: \_ sistema CIM**</span><span class="sxs-lookup"><span data-stu-id="e4db0-118">Data type: **CIM\_System**</span></span>
</dt> <dt>

<span data-ttu-id="e4db0-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e4db0-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e4db0-120">Qualificadores: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="e4db0-120">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="e4db0-121">Um [**\_ sistema CIM**](cim-system.md) que descreve o sistema de hospedagem.</span><span class="sxs-lookup"><span data-stu-id="e4db0-121">A [**CIM\_System**](cim-system.md) that describes the hosting system.</span></span>

</dd> <dt>

<span data-ttu-id="e4db0-122">**Depende**</span><span class="sxs-lookup"><span data-stu-id="e4db0-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4db0-123">Tipo de dados **: \_ serviço CIM**</span><span class="sxs-lookup"><span data-stu-id="e4db0-123">Data type: **CIM\_Service**</span></span>
</dt> <dt>

<span data-ttu-id="e4db0-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e4db0-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e4db0-125">Qualificadores: [**substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente"), [**fraco**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="e4db0-125">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="e4db0-126">Um [**\_ serviço CIM**](cim-service.md) que descreve o serviço hospedado no sistema.</span><span class="sxs-lookup"><span data-stu-id="e4db0-126">A [**CIM\_Service**](cim-service.md) that describes the service hosted on the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e4db0-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="e4db0-127">Remarks</span></span>

<span data-ttu-id="e4db0-128">**CIM \_ O HostedService** é derivado [**da \_ dependência CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="e4db0-128">**CIM\_HostedService** is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="e4db0-129">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="e4db0-129">WMI does not implement this class.</span></span>

<span data-ttu-id="e4db0-130">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="e4db0-130">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="e4db0-131">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="e4db0-131">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4db0-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e4db0-132">Requirements</span></span>



| <span data-ttu-id="e4db0-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4db0-133">Requirement</span></span> | <span data-ttu-id="e4db0-134">Valor</span><span class="sxs-lookup"><span data-stu-id="e4db0-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e4db0-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e4db0-135">Minimum supported client</span></span><br/> | <span data-ttu-id="e4db0-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e4db0-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e4db0-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e4db0-137">Minimum supported server</span></span><br/> | <span data-ttu-id="e4db0-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e4db0-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e4db0-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="e4db0-139">Namespace</span></span><br/>                | <span data-ttu-id="e4db0-140">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="e4db0-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e4db0-141">MOF</span><span class="sxs-lookup"><span data-stu-id="e4db0-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e4db0-142"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e4db0-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e4db0-143">DLL</span><span class="sxs-lookup"><span data-stu-id="e4db0-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e4db0-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e4db0-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4db0-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="e4db0-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4db0-146">**\_Dependência CIM**</span><span class="sxs-lookup"><span data-stu-id="e4db0-146">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

