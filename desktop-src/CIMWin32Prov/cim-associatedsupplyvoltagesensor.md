---
description: Associa uma fonte de energia a um sensor de tensão que monitora sua tensão de entrada.
ms.assetid: 4164320e-8362-4ce2-9949-f14669278bd8
ms.tgt_platform: multiple
title: Classe CIM_AssociatedSupplyVoltageSensor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AssociatedSupplyVoltageSensor
- CIM_AssociatedSupplyVoltageSensor.Dependent
- CIM_AssociatedSupplyVoltageSensor.Antecedent
- CIM_AssociatedSupplyVoltageSensor.MonitoringRange
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ce597fb9e170b63335c56e30f8f8c4ddb30af66c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089399"
---
# <a name="cim_associatedsupplyvoltagesensor-class"></a><span data-ttu-id="b050a-103">\_Classe CIM AssociatedSupplyVoltageSensor</span><span class="sxs-lookup"><span data-stu-id="b050a-103">CIM\_AssociatedSupplyVoltageSensor class</span></span>

<span data-ttu-id="b050a-104">A classe **CIM \_ AssociatedSupplyVoltageSensor** associa uma fonte de energia a um sensor de tensão que monitora sua tensão de entrada.</span><span class="sxs-lookup"><span data-stu-id="b050a-104">The **CIM\_AssociatedSupplyVoltageSensor** class associates a power supply with a voltage sensor that monitors its input voltage.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b050a-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="b050a-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="b050a-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="b050a-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="b050a-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="b050a-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="b050a-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="b050a-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b050a-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b050a-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{327ABD78-E3D3-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_AssociatedSupplyVoltageSensor : CIM_AssociatedSensor
{
  CIM_PowerSupply   REF Dependent;
  CIM_VoltageSensor REF Antecedent;
  uint16                MonitoringRange;
};
```

## <a name="members"></a><span data-ttu-id="b050a-110">Membros</span><span class="sxs-lookup"><span data-stu-id="b050a-110">Members</span></span>

<span data-ttu-id="b050a-111">A classe **CIM \_ AssociatedSupplyVoltageSensor** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="b050a-111">The **CIM\_AssociatedSupplyVoltageSensor** class has these types of members:</span></span>

-   [<span data-ttu-id="b050a-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b050a-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b050a-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b050a-113">Properties</span></span>

<span data-ttu-id="b050a-114">A classe **CIM \_ AssociatedSupplyVoltageSensor** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="b050a-114">The **CIM\_AssociatedSupplyVoltageSensor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b050a-115">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="b050a-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b050a-116">Tipo de dados: **CIM \_ voltagem**</span><span class="sxs-lookup"><span data-stu-id="b050a-116">Data type: **CIM\_VoltageSensor**</span></span>
</dt> <dt>

<span data-ttu-id="b050a-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b050a-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b050a-118">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="b050a-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="b050a-119">Um [**\_ voltagem CIM**](cim-voltagesensor.md) que descreve o sensor de tensão.</span><span class="sxs-lookup"><span data-stu-id="b050a-119">A [**CIM\_VoltageSensor**](cim-voltagesensor.md) that describes the voltage sensor.</span></span>

</dd> <dt>

<span data-ttu-id="b050a-120">**Depende**</span><span class="sxs-lookup"><span data-stu-id="b050a-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b050a-121">Tipo de dados: fonte de alimentação **CIM \_**</span><span class="sxs-lookup"><span data-stu-id="b050a-121">Data type: **CIM\_PowerSupply**</span></span>
</dt> <dt>

<span data-ttu-id="b050a-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b050a-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b050a-123">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")</span><span class="sxs-lookup"><span data-stu-id="b050a-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="b050a-124">Um [**\_ powersupply CIM**](cim-powersupply.md) que descreve a fonte de alimentação associada ao sensor de tensão.</span><span class="sxs-lookup"><span data-stu-id="b050a-124">A [**CIM\_PowerSupply**](cim-powersupply.md) that describes the power supply associated with the voltage sensor.</span></span>

</dd> <dt>

<span data-ttu-id="b050a-125">**MonitoringRange**</span><span class="sxs-lookup"><span data-stu-id="b050a-125">**MonitoringRange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b050a-126">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b050a-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b050a-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b050a-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b050a-128">Indica o intervalo de voltagem de entrada da fonte de energia medido pelo sensor associado.</span><span class="sxs-lookup"><span data-stu-id="b050a-128">Indicates the power supply's input voltage range measured by the associated sensor.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b050a-129"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="b050a-129"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b050a-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="b050a-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Range_1"></span><span id="range_1"></span><span id="RANGE_1"></span>

<span data-ttu-id="b050a-131"><span id="Range_1"></span><span id="range_1"></span><span id="RANGE_1"></span>**Intervalo 1** (2)</span><span class="sxs-lookup"><span data-stu-id="b050a-131"><span id="Range_1"></span><span id="range_1"></span><span id="RANGE_1"></span>**Range 1** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Range_2"></span><span id="range_2"></span><span id="RANGE_2"></span>

<span data-ttu-id="b050a-132"><span id="Range_2"></span><span id="range_2"></span><span id="RANGE_2"></span>**Intervalo 2** (3)</span><span class="sxs-lookup"><span data-stu-id="b050a-132"><span id="Range_2"></span><span id="range_2"></span><span id="RANGE_2"></span>**Range 2** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Both_Range_1_and_2"></span><span id="both_range_1_and_2"></span><span id="BOTH_RANGE_1_AND_2"></span>

<span data-ttu-id="b050a-133"><span id="Both_Range_1_and_2"></span><span id="both_range_1_and_2"></span><span id="BOTH_RANGE_1_AND_2"></span>**Intervalo 1 e 2** (4)</span><span class="sxs-lookup"><span data-stu-id="b050a-133"><span id="Both_Range_1_and_2"></span><span id="both_range_1_and_2"></span><span id="BOTH_RANGE_1_AND_2"></span>**Both Range 1 and 2** (4)</span></span>


</dt> <dd>

<span data-ttu-id="b050a-134">Intervalo 1 e 2</span><span class="sxs-lookup"><span data-stu-id="b050a-134">Range 1 and 2</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b050a-135">Comentários</span><span class="sxs-lookup"><span data-stu-id="b050a-135">Remarks</span></span>

<span data-ttu-id="b050a-136">A classe **CIM \_ AssociatedSupplyVoltageSensor** é derivada de [**\_ AssociatedSensor CIM**](cim-associatedsensor.md).</span><span class="sxs-lookup"><span data-stu-id="b050a-136">The **CIM\_AssociatedSupplyVoltageSensor** class is derived from [**CIM\_AssociatedSensor**](cim-associatedsensor.md).</span></span>

<span data-ttu-id="b050a-137">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="b050a-137">WMI does not implement this class.</span></span>

<span data-ttu-id="b050a-138">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="b050a-138">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="b050a-139">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="b050a-139">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="b050a-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b050a-140">Requirements</span></span>



| <span data-ttu-id="b050a-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="b050a-141">Requirement</span></span> | <span data-ttu-id="b050a-142">Valor</span><span class="sxs-lookup"><span data-stu-id="b050a-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b050a-143">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b050a-143">Minimum supported client</span></span><br/> | <span data-ttu-id="b050a-144">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b050a-144">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b050a-145">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b050a-145">Minimum supported server</span></span><br/> | <span data-ttu-id="b050a-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b050a-146">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b050a-147">Namespace</span><span class="sxs-lookup"><span data-stu-id="b050a-147">Namespace</span></span><br/>                | <span data-ttu-id="b050a-148">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="b050a-148">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b050a-149">MOF</span><span class="sxs-lookup"><span data-stu-id="b050a-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b050a-150"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b050a-150"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b050a-151">DLL</span><span class="sxs-lookup"><span data-stu-id="b050a-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b050a-152"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b050a-152"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b050a-153">Confira também</span><span class="sxs-lookup"><span data-stu-id="b050a-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b050a-154">**\_ASSOCIATEDSENSOR CIM**</span><span class="sxs-lookup"><span data-stu-id="b050a-154">**CIM\_AssociatedSensor**</span></span>](cim-associatedsensor.md)
</dt> </dl>

 

