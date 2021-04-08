---
description: A \_ classe CIM DeviceServiceImplementation representa uma associação entre um serviço e como ele é implementado.
ms.assetid: 5e2e3975-8338-4bf4-8c73-5be4b93fa2c8
ms.tgt_platform: multiple
title: Classe CIM_DeviceServiceImplementation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceServiceImplementation
- CIM_DeviceServiceImplementation.Dependent
- CIM_DeviceServiceImplementation.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ae96d94c95ddda684dbb4d17a2d8eb52fc6ffd4b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920458"
---
# <a name="cim_deviceserviceimplementation-class"></a><span data-ttu-id="a641b-103">\_Classe CIM DeviceServiceImplementation</span><span class="sxs-lookup"><span data-stu-id="a641b-103">CIM\_DeviceServiceImplementation class</span></span>

<span data-ttu-id="a641b-104">A classe **CIM \_ DeviceServiceImplementation** representa uma associação entre um serviço e como ele é implementado.</span><span class="sxs-lookup"><span data-stu-id="a641b-104">The **CIM\_DeviceServiceImplementation** class represents an association between a service and how it is implemented.</span></span> <span data-ttu-id="a641b-105">Quando vários dispositivos são associados a um serviço, os elementos operam em conjunto para fornecer o serviço.</span><span class="sxs-lookup"><span data-stu-id="a641b-105">When multiple devices are associated with one service, the elements operate in conjunction to provide the service.</span></span> <span data-ttu-id="a641b-106">Se houver implementações diferentes de um serviço, cada implementação resultará em instanciações individuais do objeto de serviço.</span><span class="sxs-lookup"><span data-stu-id="a641b-106">If different implementations of a service exist, each implementation results in individual instantiations of the service object.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a641b-107">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="a641b-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="a641b-108">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="a641b-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="a641b-109">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="a641b-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="a641b-110">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="a641b-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a641b-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a641b-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{290FC242-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_DeviceServiceImplementation : CIM_Dependency
{
  CIM_Service       REF Dependent;
  CIM_LogicalDevice REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="a641b-112">Membros</span><span class="sxs-lookup"><span data-stu-id="a641b-112">Members</span></span>

<span data-ttu-id="a641b-113">A classe **CIM \_ DeviceServiceImplementation** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="a641b-113">The **CIM\_DeviceServiceImplementation** class has these types of members:</span></span>

-   [<span data-ttu-id="a641b-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a641b-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a641b-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a641b-115">Properties</span></span>

<span data-ttu-id="a641b-116">A classe **CIM \_ DeviceServiceImplementation** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="a641b-116">The **CIM\_DeviceServiceImplementation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a641b-117">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="a641b-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a641b-118">Tipo de dados **: \_ LogicalDevice CIM**</span><span class="sxs-lookup"><span data-stu-id="a641b-118">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="a641b-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a641b-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a641b-120">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="a641b-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="a641b-121">Um [**\_ LogicalDevice CIM**](cim-logicaldevice.md) que descreve o dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="a641b-121">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that describes the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="a641b-122">**Depende**</span><span class="sxs-lookup"><span data-stu-id="a641b-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a641b-123">Tipo de dados **: \_ serviço CIM**</span><span class="sxs-lookup"><span data-stu-id="a641b-123">Data type: **CIM\_Service**</span></span>
</dt> <dt>

<span data-ttu-id="a641b-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a641b-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a641b-125">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")</span><span class="sxs-lookup"><span data-stu-id="a641b-125">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="a641b-126">Um [**\_ serviço CIM**](cim-service.md) que descreve o serviço implementado usando o dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="a641b-126">A [**CIM\_Service**](cim-service.md) that describes the service implemented using the logical device.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a641b-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="a641b-127">Remarks</span></span>

<span data-ttu-id="a641b-128">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="a641b-128">WMI does not implement this class.</span></span>

<span data-ttu-id="a641b-129">A classe **CIM \_ DeviceServiceImplementation** é derivada da [**\_ dependência CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="a641b-129">The **CIM\_DeviceServiceImplementation** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="a641b-130">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="a641b-130">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="a641b-131">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="a641b-131">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="a641b-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a641b-132">Requirements</span></span>



| <span data-ttu-id="a641b-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="a641b-133">Requirement</span></span> | <span data-ttu-id="a641b-134">Valor</span><span class="sxs-lookup"><span data-stu-id="a641b-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a641b-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a641b-135">Minimum supported client</span></span><br/> | <span data-ttu-id="a641b-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a641b-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a641b-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a641b-137">Minimum supported server</span></span><br/> | <span data-ttu-id="a641b-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a641b-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a641b-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="a641b-139">Namespace</span></span><br/>                | <span data-ttu-id="a641b-140">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="a641b-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a641b-141">MOF</span><span class="sxs-lookup"><span data-stu-id="a641b-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a641b-142"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a641b-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a641b-143">DLL</span><span class="sxs-lookup"><span data-stu-id="a641b-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a641b-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a641b-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a641b-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="a641b-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a641b-146">**\_Dependência CIM**</span><span class="sxs-lookup"><span data-stu-id="a641b-146">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

