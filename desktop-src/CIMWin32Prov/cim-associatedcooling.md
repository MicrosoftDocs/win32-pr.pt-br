---
description: A \_ associação CIM AssociatedCooling indica quando ventiladores ou outros dispositivos de resfriamento são específicos para um dispositivo (em vez de fornecer resfriamento de compartimento ou de gabinete).
ms.assetid: 7b20e429-593c-4365-a340-1aef9b0fadf5
ms.tgt_platform: multiple
title: Classe CIM_AssociatedCooling
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AssociatedCooling
- CIM_AssociatedCooling.Dependent
- CIM_AssociatedCooling.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: bb838129226b225f024917e8f8e77ddc92ddf2ff
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089403"
---
# <a name="cim_associatedcooling-class"></a><span data-ttu-id="c6d08-103">\_Classe CIM AssociatedCooling</span><span class="sxs-lookup"><span data-stu-id="c6d08-103">CIM\_AssociatedCooling class</span></span>

<span data-ttu-id="c6d08-104">A associação **CIM \_ AssociatedCooling** indica quando ventiladores ou outros dispositivos de resfriamento são específicos para um dispositivo (em vez de fornecer resfriamento de compartimento ou de gabinete).</span><span class="sxs-lookup"><span data-stu-id="c6d08-104">The **CIM\_AssociatedCooling** association indicates when fans or other cooling devices are specific to a device (versus providing enclosure or cabinet cooling).</span></span>

<span data-ttu-id="c6d08-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="c6d08-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="c6d08-106">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="c6d08-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6d08-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c6d08-107">Syntax</span></span>

``` syntax
[Abstract, UUID("{306F88F2-DB35-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_AssociatedCooling : CIM_Dependency
{
  CIM_LogicalDevice REF Dependent;
  CIM_CoolingDevice REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="c6d08-108">Membros</span><span class="sxs-lookup"><span data-stu-id="c6d08-108">Members</span></span>

<span data-ttu-id="c6d08-109">A classe **CIM \_ AssociatedCooling** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="c6d08-109">The **CIM\_AssociatedCooling** class has these types of members:</span></span>

-   [<span data-ttu-id="c6d08-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c6d08-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c6d08-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c6d08-111">Properties</span></span>

<span data-ttu-id="c6d08-112">A classe **CIM \_ AssociatedCooling** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="c6d08-112">The **CIM\_AssociatedCooling** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c6d08-113">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="c6d08-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6d08-114">Tipo de dados: **CIM \_ CoolingDevice**</span><span class="sxs-lookup"><span data-stu-id="c6d08-114">Data type: **CIM\_CoolingDevice**</span></span>
</dt> <dt>

<span data-ttu-id="c6d08-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c6d08-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c6d08-116">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="c6d08-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="c6d08-117">Um [**\_ LogicalDevice CIM**](cim-logicaldevice.md) que descreve o dispositivo de resfriamento.</span><span class="sxs-lookup"><span data-stu-id="c6d08-117">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that describes the cooling device.</span></span>

</dd> <dt>

<span data-ttu-id="c6d08-118">**Depende**</span><span class="sxs-lookup"><span data-stu-id="c6d08-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6d08-119">Tipo de dados **: \_ LogicalDevice CIM**</span><span class="sxs-lookup"><span data-stu-id="c6d08-119">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="c6d08-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c6d08-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c6d08-121">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")</span><span class="sxs-lookup"><span data-stu-id="c6d08-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="c6d08-122">Um [**\_ LogicalDevice CIM**](cim-logicaldevice.md) que faz referência ao dispositivo lógico que está sendo resfriado.</span><span class="sxs-lookup"><span data-stu-id="c6d08-122">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that references the logical device being cooled.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c6d08-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="c6d08-123">Remarks</span></span>

<span data-ttu-id="c6d08-124">A classe **CIM \_ AssociatedCooling** é derivada da [**\_ dependência CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="c6d08-124">The **CIM\_AssociatedCooling** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="c6d08-125">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="c6d08-125">WMI does not implement this class.</span></span>

<span data-ttu-id="c6d08-126">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="c6d08-126">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="c6d08-127">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="c6d08-127">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6d08-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c6d08-128">Requirements</span></span>



| <span data-ttu-id="c6d08-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="c6d08-129">Requirement</span></span> | <span data-ttu-id="c6d08-130">Valor</span><span class="sxs-lookup"><span data-stu-id="c6d08-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c6d08-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c6d08-131">Minimum supported client</span></span><br/> | <span data-ttu-id="c6d08-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c6d08-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c6d08-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c6d08-133">Minimum supported server</span></span><br/> | <span data-ttu-id="c6d08-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c6d08-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c6d08-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="c6d08-135">Namespace</span></span><br/>                | <span data-ttu-id="c6d08-136">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="c6d08-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c6d08-137">MOF</span><span class="sxs-lookup"><span data-stu-id="c6d08-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c6d08-138"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c6d08-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c6d08-139">DLL</span><span class="sxs-lookup"><span data-stu-id="c6d08-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c6d08-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c6d08-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6d08-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="c6d08-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6d08-142">**\_Dependência CIM**</span><span class="sxs-lookup"><span data-stu-id="c6d08-142">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

