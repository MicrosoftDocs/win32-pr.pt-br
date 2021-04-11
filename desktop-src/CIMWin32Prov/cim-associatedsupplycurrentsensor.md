---
description: A \_ classe CIM AssociatedSupplyCurrentSensor associa uma fonte de energia a um sensor atual (amperagem) que monitora sua frequência de entrada.
ms.assetid: bed4714f-ecf4-4c53-b231-c8fac673371f
ms.tgt_platform: multiple
title: Classe CIM_AssociatedSupplyCurrentSensor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AssociatedSupplyCurrentSensor
- CIM_AssociatedSupplyCurrentSensor.Dependent
- CIM_AssociatedSupplyCurrentSensor.Antecedent
- CIM_AssociatedSupplyCurrentSensor.MonitoringRange
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 70a88d87c68b36db5bd44413e3c68940db44f29b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164108"
---
# <a name="cim_associatedsupplycurrentsensor-class"></a><span data-ttu-id="ae6dd-103">\_Classe CIM AssociatedSupplyCurrentSensor</span><span class="sxs-lookup"><span data-stu-id="ae6dd-103">CIM\_AssociatedSupplyCurrentSensor class</span></span>

<span data-ttu-id="ae6dd-104">A classe **CIM \_ AssociatedSupplyCurrentSensor** associa uma fonte de energia a um sensor atual (amperagem) que monitora sua frequência de entrada.</span><span class="sxs-lookup"><span data-stu-id="ae6dd-104">The **CIM\_AssociatedSupplyCurrentSensor** class associates a power supply with a current (amperage) sensor that monitors its input frequency.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ae6dd-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="ae6dd-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="ae6dd-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="ae6dd-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="ae6dd-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="ae6dd-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="ae6dd-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="ae6dd-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae6dd-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ae6dd-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{29B273F2-E3D3-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_AssociatedSupplyCurrentSensor : CIM_AssociatedSensor
{
  CIM_PowerSupply   REF Dependent;
  CIM_CurrentSensor REF Antecedent;
  uint16                MonitoringRange;
};
```

## <a name="members"></a><span data-ttu-id="ae6dd-110">Membros</span><span class="sxs-lookup"><span data-stu-id="ae6dd-110">Members</span></span>

<span data-ttu-id="ae6dd-111">A classe **CIM \_ AssociatedSupplyCurrentSensor** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="ae6dd-111">The **CIM\_AssociatedSupplyCurrentSensor** class has these types of members:</span></span>

-   [<span data-ttu-id="ae6dd-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ae6dd-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ae6dd-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ae6dd-113">Properties</span></span>

<span data-ttu-id="ae6dd-114">A classe **CIM \_ AssociatedSupplyCurrentSensor** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="ae6dd-114">The **CIM\_AssociatedSupplyCurrentSensor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ae6dd-115">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="ae6dd-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae6dd-116">Tipo de dados: **CIM \_ CurrentSensor**</span><span class="sxs-lookup"><span data-stu-id="ae6dd-116">Data type: **CIM\_CurrentSensor**</span></span>
</dt> <dt>

<span data-ttu-id="ae6dd-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ae6dd-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae6dd-118">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="ae6dd-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="ae6dd-119">Um [**\_ CurrentSensor CIM**](cim-currentsensor.md) que descreve o sensor atual.</span><span class="sxs-lookup"><span data-stu-id="ae6dd-119">A [**CIM\_CurrentSensor**](cim-currentsensor.md) that describes the current sensor.</span></span>

</dd> <dt>

<span data-ttu-id="ae6dd-120">**Depende**</span><span class="sxs-lookup"><span data-stu-id="ae6dd-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae6dd-121">Tipo de dados: fonte de alimentação **CIM \_**</span><span class="sxs-lookup"><span data-stu-id="ae6dd-121">Data type: **CIM\_PowerSupply**</span></span>
</dt> <dt>

<span data-ttu-id="ae6dd-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ae6dd-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae6dd-123">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")</span><span class="sxs-lookup"><span data-stu-id="ae6dd-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="ae6dd-124">Um [**\_ powersupply CIM**](cim-powersupply.md) que descreve a fonte de energia associada ao sensor atual.</span><span class="sxs-lookup"><span data-stu-id="ae6dd-124">A [**CIM\_PowerSupply**](cim-powersupply.md) that describes the power supply associated with the current sensor.</span></span>

</dd> <dt>

<span data-ttu-id="ae6dd-125">**MonitoringRange**</span><span class="sxs-lookup"><span data-stu-id="ae6dd-125">**MonitoringRange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae6dd-126">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ae6dd-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ae6dd-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ae6dd-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae6dd-128">Indica o intervalo de frequência de entrada da fonte de energia medido pelo sensor associado.</span><span class="sxs-lookup"><span data-stu-id="ae6dd-128">Indicates the power supply input frequency range measured by the associated sensor.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ae6dd-129"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="ae6dd-129"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="ae6dd-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="ae6dd-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Range_1"></span><span id="range_1"></span><span id="RANGE_1"></span>

<span data-ttu-id="ae6dd-131"><span id="Range_1"></span><span id="range_1"></span><span id="RANGE_1"></span>**Intervalo 1** (2)</span><span class="sxs-lookup"><span data-stu-id="ae6dd-131"><span id="Range_1"></span><span id="range_1"></span><span id="RANGE_1"></span>**Range 1** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Range_2"></span><span id="range_2"></span><span id="RANGE_2"></span>

<span data-ttu-id="ae6dd-132"><span id="Range_2"></span><span id="range_2"></span><span id="RANGE_2"></span>**Intervalo 2** (3)</span><span class="sxs-lookup"><span data-stu-id="ae6dd-132"><span id="Range_2"></span><span id="range_2"></span><span id="RANGE_2"></span>**Range 2** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Both_Range_1_and_2"></span><span id="both_range_1_and_2"></span><span id="BOTH_RANGE_1_AND_2"></span>

<span data-ttu-id="ae6dd-133"><span id="Both_Range_1_and_2"></span><span id="both_range_1_and_2"></span><span id="BOTH_RANGE_1_AND_2"></span>**Intervalo 1 e 2** (4)</span><span class="sxs-lookup"><span data-stu-id="ae6dd-133"><span id="Both_Range_1_and_2"></span><span id="both_range_1_and_2"></span><span id="BOTH_RANGE_1_AND_2"></span>**Both Range 1 and 2** (4)</span></span>


</dt> <dd>

<span data-ttu-id="ae6dd-134">Intervalo 1 e 2</span><span class="sxs-lookup"><span data-stu-id="ae6dd-134">Range 1 and 2</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ae6dd-135">Comentários</span><span class="sxs-lookup"><span data-stu-id="ae6dd-135">Remarks</span></span>

<span data-ttu-id="ae6dd-136">A classe **CIM \_ AssociatedSupplyCurrentSensor** é derivada de [**\_ AssociatedSensor CIM**](cim-associatedsensor.md).</span><span class="sxs-lookup"><span data-stu-id="ae6dd-136">The **CIM\_AssociatedSupplyCurrentSensor** class is derived from [**CIM\_AssociatedSensor**](cim-associatedsensor.md).</span></span>

<span data-ttu-id="ae6dd-137">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="ae6dd-137">WMI does not implement this class.</span></span>

<span data-ttu-id="ae6dd-138">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="ae6dd-138">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="ae6dd-139">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="ae6dd-139">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae6dd-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ae6dd-140">Requirements</span></span>



| <span data-ttu-id="ae6dd-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="ae6dd-141">Requirement</span></span> | <span data-ttu-id="ae6dd-142">Valor</span><span class="sxs-lookup"><span data-stu-id="ae6dd-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ae6dd-143">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ae6dd-143">Minimum supported client</span></span><br/> | <span data-ttu-id="ae6dd-144">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ae6dd-144">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ae6dd-145">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ae6dd-145">Minimum supported server</span></span><br/> | <span data-ttu-id="ae6dd-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ae6dd-146">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ae6dd-147">Namespace</span><span class="sxs-lookup"><span data-stu-id="ae6dd-147">Namespace</span></span><br/>                | <span data-ttu-id="ae6dd-148">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="ae6dd-148">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ae6dd-149">MOF</span><span class="sxs-lookup"><span data-stu-id="ae6dd-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ae6dd-150"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ae6dd-150"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ae6dd-151">DLL</span><span class="sxs-lookup"><span data-stu-id="ae6dd-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ae6dd-152"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ae6dd-152"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae6dd-153">Confira também</span><span class="sxs-lookup"><span data-stu-id="ae6dd-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae6dd-154">**\_ASSOCIATEDSENSOR CIM**</span><span class="sxs-lookup"><span data-stu-id="ae6dd-154">**CIM\_AssociatedSensor**</span></span>](cim-associatedsensor.md)
</dt> </dl>

 

