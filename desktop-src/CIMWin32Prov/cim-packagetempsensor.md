---
description: A \_ associação CIM PackageTempSensor representa a relação na qual um sensor de temperatura é frequentemente instalado em um pacote, como um chassi ou um rack, para monitorar o ambiente do pacote.
ms.assetid: 79f2c4d1-5e1a-4c5f-9ef4-0c8bc3926a13
ms.tgt_platform: multiple
title: Classe CIM_PackageTempSensor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PackageTempSensor
- CIM_PackageTempSensor.Dependent
- CIM_PackageTempSensor.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 28c3fa3ba569a2bf3101d62734bb9e4d5372fcf0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089263"
---
# <a name="cim_packagetempsensor-class"></a><span data-ttu-id="b3c1e-103">\_Classe CIM PackageTempSensor</span><span class="sxs-lookup"><span data-stu-id="b3c1e-103">CIM\_PackageTempSensor class</span></span>

<span data-ttu-id="b3c1e-104">A associação **CIM \_ PackageTempSensor** representa a relação na qual um sensor de temperatura é frequentemente instalado em um pacote, como um chassi ou um rack, para monitorar o ambiente do pacote.</span><span class="sxs-lookup"><span data-stu-id="b3c1e-104">The **CIM\_PackageTempSensor** association represents the relationship in which a temperature sensor is often installed in a package, such as a chassis or a rack, to monitor the package's environment.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b3c1e-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="b3c1e-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="b3c1e-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="b3c1e-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="b3c1e-107">A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="b3c1e-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="b3c1e-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="b3c1e-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3c1e-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b3c1e-109">Syntax</span></span>

``` syntax
[Abstract, Aggregation, UUID("{FAF76B8F-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PackageTempSensor : CIM_Dependency
{
  CIM_PhysicalPackage   REF Dependent;
  CIM_TemperatureSensor REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="b3c1e-110">Membros</span><span class="sxs-lookup"><span data-stu-id="b3c1e-110">Members</span></span>

<span data-ttu-id="b3c1e-111">A classe **CIM \_ PackageTempSensor** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="b3c1e-111">The **CIM\_PackageTempSensor** class has these types of members:</span></span>

-   [<span data-ttu-id="b3c1e-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b3c1e-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b3c1e-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b3c1e-113">Properties</span></span>

<span data-ttu-id="b3c1e-114">A classe **CIM \_ PackageTempSensor** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="b3c1e-114">The **CIM\_PackageTempSensor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b3c1e-115">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="b3c1e-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3c1e-116">Tipo de dados: **CIM \_ sensor**</span><span class="sxs-lookup"><span data-stu-id="b3c1e-116">Data type: **CIM\_TemperatureSensor**</span></span>
</dt> <dt>

<span data-ttu-id="b3c1e-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b3c1e-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b3c1e-118">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="b3c1e-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="b3c1e-119">Um [**\_ sensor CIM**](cim-temperaturesensor.md) que descreve o sensor de temperatura para o pacote.</span><span class="sxs-lookup"><span data-stu-id="b3c1e-119">A [**CIM\_TemperatureSensor**](cim-temperaturesensor.md) describing the temperature sensor for the package.</span></span>

</dd> <dt>

<span data-ttu-id="b3c1e-120">**Depende**</span><span class="sxs-lookup"><span data-stu-id="b3c1e-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3c1e-121">Tipo de dados: **CIM \_ PhysicalPackage**</span><span class="sxs-lookup"><span data-stu-id="b3c1e-121">Data type: **CIM\_PhysicalPackage**</span></span>
</dt> <dt>

<span data-ttu-id="b3c1e-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b3c1e-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b3c1e-123">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")</span><span class="sxs-lookup"><span data-stu-id="b3c1e-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="b3c1e-124">Um [**\_ PhysicalPackage CIM**](cim-physicalpackage.md) que descreve o pacote físico cujo ambiente é monitorado.</span><span class="sxs-lookup"><span data-stu-id="b3c1e-124">A [**CIM\_PhysicalPackage**](cim-physicalpackage.md) describing the physical package whose environment is monitored.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b3c1e-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="b3c1e-125">Remarks</span></span>

<span data-ttu-id="b3c1e-126">**CIM \_ PackageTempSensor** é derivado da [**\_ dependência CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="b3c1e-126">**CIM\_PackageTempSensor** is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="b3c1e-127">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="b3c1e-127">WMI does not implement this class.</span></span>

<span data-ttu-id="b3c1e-128">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="b3c1e-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="b3c1e-129">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="b3c1e-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3c1e-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b3c1e-130">Requirements</span></span>



| <span data-ttu-id="b3c1e-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3c1e-131">Requirement</span></span> | <span data-ttu-id="b3c1e-132">Valor</span><span class="sxs-lookup"><span data-stu-id="b3c1e-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b3c1e-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b3c1e-133">Minimum supported client</span></span><br/> | <span data-ttu-id="b3c1e-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b3c1e-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b3c1e-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b3c1e-135">Minimum supported server</span></span><br/> | <span data-ttu-id="b3c1e-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b3c1e-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b3c1e-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="b3c1e-137">Namespace</span></span><br/>                | <span data-ttu-id="b3c1e-138">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="b3c1e-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b3c1e-139">MOF</span><span class="sxs-lookup"><span data-stu-id="b3c1e-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b3c1e-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b3c1e-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b3c1e-141">DLL</span><span class="sxs-lookup"><span data-stu-id="b3c1e-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b3c1e-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b3c1e-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3c1e-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="b3c1e-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3c1e-144">**\_Dependência CIM**</span><span class="sxs-lookup"><span data-stu-id="b3c1e-144">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

