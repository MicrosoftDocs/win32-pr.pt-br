---
description: A \_ classe CIM ErrorCountersForDevice associa a \_ classe CIM DeviceErrorCounts ao dispositivo lógico ao qual se aplica.
ms.assetid: 200971ab-df85-4a45-beb3-4ffe11ce92dc
ms.tgt_platform: multiple
title: Classe CIM_ErrorCountersForDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ErrorCountersForDevice
- CIM_ErrorCountersForDevice.Element
- CIM_ErrorCountersForDevice.Stats
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7c4e11b1f58cae7b544b251044657bb737525b37
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826462"
---
# <a name="cim_errorcountersfordevice-class"></a><span data-ttu-id="0151f-103">\_Classe CIM ErrorCountersForDevice</span><span class="sxs-lookup"><span data-stu-id="0151f-103">CIM\_ErrorCountersForDevice class</span></span>

<span data-ttu-id="0151f-104">A classe **CIM \_ ErrorCountersForDevice** associa a classe [**CIM \_ DeviceErrorCounts**](cim-deviceerrorcounts.md) ao dispositivo lógico ao qual se aplica.</span><span class="sxs-lookup"><span data-stu-id="0151f-104">The **CIM\_ErrorCountersForDevice** class associates the [**CIM\_DeviceErrorCounts**](cim-deviceerrorcounts.md) class to the logical device to which it applies.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0151f-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="0151f-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="0151f-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="0151f-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="0151f-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="0151f-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="0151f-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="0151f-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="0151f-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0151f-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{2D79F3A0-D025-11d2-85F5-0000F8102E5F}"), AMENDMENT]
class CIM_ErrorCountersForDevice : CIM_Statistics
{
  CIM_LogicalDevice     REF Element;
  CIM_DeviceErrorCounts REF Stats;
};
```

## <a name="members"></a><span data-ttu-id="0151f-110">Membros</span><span class="sxs-lookup"><span data-stu-id="0151f-110">Members</span></span>

<span data-ttu-id="0151f-111">A classe **CIM \_ ErrorCountersForDevice** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="0151f-111">The **CIM\_ErrorCountersForDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="0151f-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0151f-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0151f-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0151f-113">Properties</span></span>

<span data-ttu-id="0151f-114">A classe **CIM \_ ErrorCountersForDevice** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="0151f-114">The **CIM\_ErrorCountersForDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0151f-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="0151f-115">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0151f-116">Tipo de dados **: \_ LogicalDevice CIM**</span><span class="sxs-lookup"><span data-stu-id="0151f-116">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="0151f-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0151f-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0151f-118">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("element"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="0151f-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Element"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="0151f-119">Um [**\_ LogicalDevice CIM**](cim-logicaldevice.md) que descreve o dispositivo ao qual os contadores de erro se aplicam.</span><span class="sxs-lookup"><span data-stu-id="0151f-119">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that describes the device to which the error counters apply.</span></span>

</dd> <dt>

<span data-ttu-id="0151f-120">**Estatísticas**</span><span class="sxs-lookup"><span data-stu-id="0151f-120">**Stats**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0151f-121">Tipo de dados: **CIM \_ DeviceErrorCounts**</span><span class="sxs-lookup"><span data-stu-id="0151f-121">Data type: **CIM\_DeviceErrorCounts**</span></span>
</dt> <dt>

<span data-ttu-id="0151f-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0151f-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0151f-123">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("stats"), [**fraca**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="0151f-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Stats"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="0151f-124">Um [**\_ DeviceErrorCounts CIM**](cim-deviceerrorcounts.md) que descreve o objeto estatístico – nesse caso, a classe do contador de erros.</span><span class="sxs-lookup"><span data-stu-id="0151f-124">A [**CIM\_DeviceErrorCounts**](cim-deviceerrorcounts.md) describing the statistical object - in this case, the error counter class.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0151f-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="0151f-125">Remarks</span></span>

<span data-ttu-id="0151f-126">A classe **CIM \_ ErrorCountersForDevice** é herdada [**de \_ estatísticas CIM**](cim-statistics.md).</span><span class="sxs-lookup"><span data-stu-id="0151f-126">The **CIM\_ErrorCountersForDevice** class is inherited from [**CIM\_Statistics**](cim-statistics.md).</span></span>

<span data-ttu-id="0151f-127">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="0151f-127">WMI does not implement this class.</span></span>

<span data-ttu-id="0151f-128">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="0151f-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="0151f-129">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="0151f-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="0151f-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0151f-130">Requirements</span></span>



| <span data-ttu-id="0151f-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="0151f-131">Requirement</span></span> | <span data-ttu-id="0151f-132">Valor</span><span class="sxs-lookup"><span data-stu-id="0151f-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0151f-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0151f-133">Minimum supported client</span></span><br/> | <span data-ttu-id="0151f-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0151f-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0151f-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0151f-135">Minimum supported server</span></span><br/> | <span data-ttu-id="0151f-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0151f-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0151f-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="0151f-137">Namespace</span></span><br/>                | <span data-ttu-id="0151f-138">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="0151f-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0151f-139">MOF</span><span class="sxs-lookup"><span data-stu-id="0151f-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0151f-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0151f-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0151f-141">DLL</span><span class="sxs-lookup"><span data-stu-id="0151f-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0151f-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0151f-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0151f-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="0151f-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0151f-144">**Estatísticas de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="0151f-144">**CIM\_Statistics**</span></span>](cim-statistics.md)
</dt> </dl>

 

