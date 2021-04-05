---
description: A \_ classe CIM AssociatedSensor associa um sensor instalado a um dispositivo lógico. O sensor mede as propriedades de entrada e saída críticas e pode ser incluído no dispositivo ou instalado no próximo.
ms.assetid: 8ccaa37f-b95f-4582-a694-23bdc15b8c8b
ms.tgt_platform: multiple
title: Classe CIM_AssociatedSensor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AssociatedSensor
- CIM_AssociatedSensor.Dependent
- CIM_AssociatedSensor.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 50eac6b8bd933762df0da0213c420f5895b74640
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826540"
---
# <a name="cim_associatedsensor-class"></a><span data-ttu-id="119e2-104">\_Classe CIM AssociatedSensor</span><span class="sxs-lookup"><span data-stu-id="119e2-104">CIM\_AssociatedSensor class</span></span>

<span data-ttu-id="119e2-105">A classe **CIM \_ AssociatedSensor** associa um sensor instalado a um dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="119e2-105">The **CIM\_AssociatedSensor** class associates an installed sensor with a logical device.</span></span> <span data-ttu-id="119e2-106">O sensor mede as propriedades de entrada e saída críticas e pode ser incluído no dispositivo ou instalado no próximo.</span><span class="sxs-lookup"><span data-stu-id="119e2-106">The sensor measures critical input and output properties, and can be included with the device or installed nearby.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="119e2-107">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="119e2-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="119e2-108">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="119e2-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="119e2-109">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="119e2-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="119e2-110">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="119e2-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="119e2-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="119e2-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{956597A0-7D80-11D2-AAD3-006008C78BC7}"), AMENDMENT]
class CIM_AssociatedSensor : CIM_Dependency
{
  CIM_LogicalDevice REF Dependent;
  CIM_Sensor        REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="119e2-112">Membros</span><span class="sxs-lookup"><span data-stu-id="119e2-112">Members</span></span>

<span data-ttu-id="119e2-113">A classe **CIM \_ AssociatedSensor** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="119e2-113">The **CIM\_AssociatedSensor** class has these types of members:</span></span>

-   [<span data-ttu-id="119e2-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="119e2-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="119e2-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="119e2-115">Properties</span></span>

<span data-ttu-id="119e2-116">A classe **CIM \_ AssociatedSensor** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="119e2-116">The **CIM\_AssociatedSensor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="119e2-117">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="119e2-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="119e2-118">Tipo de dados **: \_ sensor CIM**</span><span class="sxs-lookup"><span data-stu-id="119e2-118">Data type: **CIM\_Sensor**</span></span>
</dt> <dt>

<span data-ttu-id="119e2-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="119e2-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="119e2-120">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="119e2-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="119e2-121">Um [**\_ sensor CIM**](cim-sensor.md) que descreve o sensor.</span><span class="sxs-lookup"><span data-stu-id="119e2-121">A [**CIM\_Sensor**](cim-sensor.md) that describes the sensor.</span></span>

</dd> <dt>

<span data-ttu-id="119e2-122">**Depende**</span><span class="sxs-lookup"><span data-stu-id="119e2-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="119e2-123">Tipo de dados **: \_ LogicalDevice CIM**</span><span class="sxs-lookup"><span data-stu-id="119e2-123">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="119e2-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="119e2-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="119e2-125">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")</span><span class="sxs-lookup"><span data-stu-id="119e2-125">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="119e2-126">Um [**\_ LogicalDevice CIM**](cim-logicaldevice.md) que descreve o dispositivo lógico para o qual as informações são medidas pelo sensor.</span><span class="sxs-lookup"><span data-stu-id="119e2-126">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that describes the logical device for which information is measured by the sensor.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="119e2-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="119e2-127">Remarks</span></span>

<span data-ttu-id="119e2-128">A classe **CIM \_ AssociatedSensor** é derivada da [**\_ dependência CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="119e2-128">The **CIM\_AssociatedSensor** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="119e2-129">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="119e2-129">WMI does not implement this class.</span></span> <span data-ttu-id="119e2-130">Para obter mais informações sobre classes derivadas de **CIM \_ AssociatedSensor**, consulte [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="119e2-130">For more information about classes derived from **CIM\_AssociatedSensor**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="119e2-131">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="119e2-131">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="119e2-132">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="119e2-132">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="119e2-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="119e2-133">Requirements</span></span>



| <span data-ttu-id="119e2-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="119e2-134">Requirement</span></span> | <span data-ttu-id="119e2-135">Valor</span><span class="sxs-lookup"><span data-stu-id="119e2-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="119e2-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="119e2-136">Minimum supported client</span></span><br/> | <span data-ttu-id="119e2-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="119e2-137">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="119e2-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="119e2-138">Minimum supported server</span></span><br/> | <span data-ttu-id="119e2-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="119e2-139">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="119e2-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="119e2-140">Namespace</span></span><br/>                | <span data-ttu-id="119e2-141">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="119e2-141">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="119e2-142">MOF</span><span class="sxs-lookup"><span data-stu-id="119e2-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="119e2-143"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="119e2-143"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="119e2-144">DLL</span><span class="sxs-lookup"><span data-stu-id="119e2-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="119e2-145"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="119e2-145"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="119e2-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="119e2-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="119e2-147">**\_Dependência CIM**</span><span class="sxs-lookup"><span data-stu-id="119e2-147">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

