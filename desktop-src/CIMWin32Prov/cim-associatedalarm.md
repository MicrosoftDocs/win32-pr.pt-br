---
description: A dependência do CIM \_ AssociatedAlarm associa um alarme a um dispositivo lógico.
ms.assetid: ed0ccc81-6d1b-45b0-abf0-7a2bd9a50193
ms.tgt_platform: multiple
title: Classe CIM_AssociatedAlarm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AssociatedAlarm
- CIM_AssociatedAlarm.Dependent
- CIM_AssociatedAlarm.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: fe6a637482526feecc7528eadc70dc695dafca9b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646451"
---
# <a name="cim_associatedalarm-class"></a><span data-ttu-id="e21e1-103">\_Classe CIM AssociatedAlarm</span><span class="sxs-lookup"><span data-stu-id="e21e1-103">CIM\_AssociatedAlarm class</span></span>

<span data-ttu-id="e21e1-104">A dependência do **CIM \_ AssociatedAlarm** associa um alarme a um dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="e21e1-104">The **CIM\_AssociatedAlarm** dependency associates an alarm with a logical device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e21e1-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="e21e1-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="e21e1-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="e21e1-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="e21e1-107">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="e21e1-107">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e21e1-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e21e1-108">Syntax</span></span>

``` syntax
[Abstract, UUID("{2280CB02-DB35-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_AssociatedAlarm : CIM_Dependency
{
  CIM_LogicalDevice REF Dependent;
  CIM_AlarmDevice   REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="e21e1-109">Membros</span><span class="sxs-lookup"><span data-stu-id="e21e1-109">Members</span></span>

<span data-ttu-id="e21e1-110">A classe **CIM \_ AssociatedAlarm** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="e21e1-110">The **CIM\_AssociatedAlarm** class has these types of members:</span></span>

-   [<span data-ttu-id="e21e1-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e21e1-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e21e1-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e21e1-112">Properties</span></span>

<span data-ttu-id="e21e1-113">A classe **CIM \_ AssociatedAlarm** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="e21e1-113">The **CIM\_AssociatedAlarm** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e21e1-114">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="e21e1-114">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e21e1-115">Tipo de dados: **CIM \_ AlarmDevice**</span><span class="sxs-lookup"><span data-stu-id="e21e1-115">Data type: **CIM\_AlarmDevice**</span></span>
</dt> <dt>

<span data-ttu-id="e21e1-116">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e21e1-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e21e1-117">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="e21e1-117">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="e21e1-118">Um [**\_ AlarmDevice CIM**](cim-alarmdevice.md) que contém o dispositivo de alarme.</span><span class="sxs-lookup"><span data-stu-id="e21e1-118">A [**CIM\_AlarmDevice**](cim-alarmdevice.md) that contains the alarm device.</span></span>

</dd> <dt>

<span data-ttu-id="e21e1-119">**Depende**</span><span class="sxs-lookup"><span data-stu-id="e21e1-119">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e21e1-120">Tipo de dados **: \_ LogicalDevice CIM**</span><span class="sxs-lookup"><span data-stu-id="e21e1-120">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="e21e1-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e21e1-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e21e1-122">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")</span><span class="sxs-lookup"><span data-stu-id="e21e1-122">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="e21e1-123">Um [**\_ LogicalDevice CIM**](cim-logicaldevice.md) que contém o dispositivo lógico que é despertado.</span><span class="sxs-lookup"><span data-stu-id="e21e1-123">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that contains the logical device that is alarmed.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e21e1-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="e21e1-124">Remarks</span></span>

<span data-ttu-id="e21e1-125">A classe **CIM \_ AssociatedAlarm** é derivada da [**\_ dependência CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="e21e1-125">The **CIM\_AssociatedAlarm** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="e21e1-126">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="e21e1-126">WMI does not implement this class.</span></span>

<span data-ttu-id="e21e1-127">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="e21e1-127">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="e21e1-128">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="e21e1-128">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="e21e1-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e21e1-129">Requirements</span></span>



| <span data-ttu-id="e21e1-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="e21e1-130">Requirement</span></span> | <span data-ttu-id="e21e1-131">Valor</span><span class="sxs-lookup"><span data-stu-id="e21e1-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e21e1-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e21e1-132">Minimum supported client</span></span><br/> | <span data-ttu-id="e21e1-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e21e1-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e21e1-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e21e1-134">Minimum supported server</span></span><br/> | <span data-ttu-id="e21e1-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e21e1-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e21e1-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="e21e1-136">Namespace</span></span><br/>                | <span data-ttu-id="e21e1-137">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="e21e1-137">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e21e1-138">MOF</span><span class="sxs-lookup"><span data-stu-id="e21e1-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e21e1-139"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e21e1-139"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e21e1-140">DLL</span><span class="sxs-lookup"><span data-stu-id="e21e1-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e21e1-141"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e21e1-141"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e21e1-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="e21e1-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e21e1-143">**\_Dependência CIM**</span><span class="sxs-lookup"><span data-stu-id="e21e1-143">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

