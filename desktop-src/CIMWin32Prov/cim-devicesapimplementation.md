---
description: A \_ classe CIM DeviceSAPImplementation representa uma associação entre um ponto de acesso de serviço (SAP) e como ele é implementado.
ms.assetid: 6c059507-bfc0-4630-9b39-9c4bae2bf138
ms.tgt_platform: multiple
title: Classe CIM_DeviceSAPImplementation (provedores WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceSAPImplementation
- CIM_DeviceSAPImplementation.Dependent
- CIM_DeviceSAPImplementation.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: eadc1e42427c06717c7b0d7a13aba8a2a71ccddb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646449"
---
# <a name="cim_devicesapimplementation-class-cimwin32-wmi-providers"></a><span data-ttu-id="cadc0-103">Classe CIM_DeviceSAPImplementation (provedores WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="cadc0-103">CIM_DeviceSAPImplementation class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="cadc0-104">A classe **CIM \_ DeviceSAPImplementation** representa uma associação entre um ponto de acesso de serviço (SAP) e como ele é implementado.</span><span class="sxs-lookup"><span data-stu-id="cadc0-104">The **CIM\_DeviceSAPImplementation** class represents an association between a service access point (SAP) and how it is implemented.</span></span> <span data-ttu-id="cadc0-105">Quando muitos dispositivos lógicos são associados a um SAP, os elementos operam em conjunto para fornecer o ponto de acesso.</span><span class="sxs-lookup"><span data-stu-id="cadc0-105">When many logical devices are associated with one SAP, the elements operate in conjunction to provide the access point.</span></span> <span data-ttu-id="cadc0-106">Se houver implementações diferentes de um SAP, cada implementação resultará em instanciações individuais do objeto SAP.</span><span class="sxs-lookup"><span data-stu-id="cadc0-106">If different implementations of a SAP exist, each implementation results in individual instantiations of the SAP object.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cadc0-107">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="cadc0-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="cadc0-108">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="cadc0-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="cadc0-109">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="cadc0-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="cadc0-110">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="cadc0-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="cadc0-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cadc0-111">Syntax</span></span>

``` syntax
[UUID("{1BE949DA-DB36-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_DeviceSAPImplementation : CIM_Dependency
{
  CIM_ServiceAccessPoint REF Dependent;
  CIM_LogicalDevice      REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="cadc0-112">Membros</span><span class="sxs-lookup"><span data-stu-id="cadc0-112">Members</span></span>

<span data-ttu-id="cadc0-113">A classe **CIM \_ DeviceSAPImplementation** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="cadc0-113">The **CIM\_DeviceSAPImplementation** class has these types of members:</span></span>

-   [<span data-ttu-id="cadc0-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="cadc0-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cadc0-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="cadc0-115">Properties</span></span>

<span data-ttu-id="cadc0-116">A classe **CIM \_ DeviceSAPImplementation** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="cadc0-116">The **CIM\_DeviceSAPImplementation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cadc0-117">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="cadc0-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cadc0-118">Tipo de dados **: \_ LogicalDevice CIM**</span><span class="sxs-lookup"><span data-stu-id="cadc0-118">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="cadc0-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cadc0-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cadc0-120">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="cadc0-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="cadc0-121">Um [**\_ LogicalDevice CIM**](cim-logicaldevice.md) que descreve o dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="cadc0-121">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that describes the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="cadc0-122">**Depende**</span><span class="sxs-lookup"><span data-stu-id="cadc0-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cadc0-123">Tipo de dados: **CIM \_ ServiceAccessPoint**</span><span class="sxs-lookup"><span data-stu-id="cadc0-123">Data type: **CIM\_ServiceAccessPoint**</span></span>
</dt> <dt>

<span data-ttu-id="cadc0-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cadc0-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cadc0-125">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")</span><span class="sxs-lookup"><span data-stu-id="cadc0-125">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="cadc0-126">Um [**\_ ServiceAccessPoint CIM**](cim-serviceaccesspoint.md) que descreve o ponto de acesso de serviço implementado usando o dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="cadc0-126">A [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md) that describes the service access point implemented using the logical device.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cadc0-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="cadc0-127">Remarks</span></span>

<span data-ttu-id="cadc0-128">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="cadc0-128">WMI does not implement this class.</span></span>

<span data-ttu-id="cadc0-129">A classe **CIM \_ DeviceSAPImplementation** é derivada da [**\_ dependência CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="cadc0-129">The **CIM\_DeviceSAPImplementation** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="cadc0-130">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="cadc0-130">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="cadc0-131">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="cadc0-131">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="cadc0-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cadc0-132">Requirements</span></span>



| <span data-ttu-id="cadc0-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="cadc0-133">Requirement</span></span> | <span data-ttu-id="cadc0-134">Valor</span><span class="sxs-lookup"><span data-stu-id="cadc0-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cadc0-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cadc0-135">Minimum supported client</span></span><br/> | <span data-ttu-id="cadc0-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cadc0-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="cadc0-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cadc0-137">Minimum supported server</span></span><br/> | <span data-ttu-id="cadc0-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cadc0-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="cadc0-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="cadc0-139">Namespace</span></span><br/>                | <span data-ttu-id="cadc0-140">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="cadc0-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="cadc0-141">MOF</span><span class="sxs-lookup"><span data-stu-id="cadc0-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cadc0-142"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cadc0-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="cadc0-143">DLL</span><span class="sxs-lookup"><span data-stu-id="cadc0-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cadc0-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cadc0-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cadc0-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="cadc0-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cadc0-146">**\_Dependência CIM**</span><span class="sxs-lookup"><span data-stu-id="cadc0-146">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

