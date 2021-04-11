---
description: A dependência do CIM \_ AssociatedBattery associa uma bateria a um dispositivo lógico. Use essa associação para modelar baterias individuais que compõem uma fonte de alimentação ininterrupta (UPS).
ms.assetid: f8d8b3d3-edc5-438a-8be6-3ea4d765085b
ms.tgt_platform: multiple
title: Classe CIM_AssociatedBattery
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AssociatedBattery
- CIM_AssociatedBattery.Dependent
- CIM_AssociatedBattery.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 98c6394df79e53698ab6394f8572768f3728c503
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164110"
---
# <a name="cim_associatedbattery-class"></a><span data-ttu-id="9c57d-104">\_Classe CIM AssociatedBattery</span><span class="sxs-lookup"><span data-stu-id="9c57d-104">CIM\_AssociatedBattery class</span></span>

<span data-ttu-id="9c57d-105">A dependência do **CIM \_ AssociatedBattery** associa uma bateria a um dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="9c57d-105">The **CIM\_AssociatedBattery** dependency associates a battery with a logical device.</span></span> <span data-ttu-id="9c57d-106">Use essa associação para modelar baterias individuais que compõem uma fonte de alimentação ininterrupta (UPS).</span><span class="sxs-lookup"><span data-stu-id="9c57d-106">Use this association to model individual batteries that make up an uninterruptible power supply (UPS).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9c57d-107">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="9c57d-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="9c57d-108">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="9c57d-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="9c57d-109">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="9c57d-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="9c57d-110">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="9c57d-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c57d-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9c57d-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C578-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_AssociatedBattery : CIM_Dependency
{
  CIM_LogicalDevice REF Dependent;
  CIM_Battery       REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="9c57d-112">Membros</span><span class="sxs-lookup"><span data-stu-id="9c57d-112">Members</span></span>

<span data-ttu-id="9c57d-113">A classe **CIM \_ AssociatedBattery** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="9c57d-113">The **CIM\_AssociatedBattery** class has these types of members:</span></span>

-   [<span data-ttu-id="9c57d-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="9c57d-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9c57d-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="9c57d-115">Properties</span></span>

<span data-ttu-id="9c57d-116">A classe **CIM \_ AssociatedBattery** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="9c57d-116">The **CIM\_AssociatedBattery** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9c57d-117">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="9c57d-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c57d-118">Tipo de dados **: \_ bateria CIM**</span><span class="sxs-lookup"><span data-stu-id="9c57d-118">Data type: **CIM\_Battery**</span></span>
</dt> <dt>

<span data-ttu-id="9c57d-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9c57d-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c57d-120">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="9c57d-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="9c57d-121">Uma [**\_ bateria CIM**](cim-battery.md) que descreve a bateria.</span><span class="sxs-lookup"><span data-stu-id="9c57d-121">A [**CIM\_Battery**](cim-battery.md) that describes the battery.</span></span>

</dd> <dt>

<span data-ttu-id="9c57d-122">**Depende**</span><span class="sxs-lookup"><span data-stu-id="9c57d-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c57d-123">Tipo de dados **: \_ LogicalDevice CIM**</span><span class="sxs-lookup"><span data-stu-id="9c57d-123">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="9c57d-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9c57d-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c57d-125">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")</span><span class="sxs-lookup"><span data-stu-id="9c57d-125">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="9c57d-126">Um [**\_ LogicalDevice CIM**](cim-logicaldevice.md) que contém o dispositivo lógico que precisa ou está associado à bateria.</span><span class="sxs-lookup"><span data-stu-id="9c57d-126">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that contains the logical device needing or associated with the battery.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9c57d-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="9c57d-127">Remarks</span></span>

<span data-ttu-id="9c57d-128">A classe **CIM \_ AssociatedBattery** é derivada da [**\_ dependência CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="9c57d-128">The **CIM\_AssociatedBattery** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="9c57d-129">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="9c57d-129">WMI does not implement this class.</span></span> <span data-ttu-id="9c57d-130">Para obter mais informações sobre classes derivadas de **CIM \_ AssociatedBattery**, consulte [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="9c57d-130">For more information about classes derived from **CIM\_AssociatedBattery**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="9c57d-131">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="9c57d-131">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="9c57d-132">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="9c57d-132">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c57d-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9c57d-133">Requirements</span></span>



| <span data-ttu-id="9c57d-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="9c57d-134">Requirement</span></span> | <span data-ttu-id="9c57d-135">Valor</span><span class="sxs-lookup"><span data-stu-id="9c57d-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9c57d-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9c57d-136">Minimum supported client</span></span><br/> | <span data-ttu-id="9c57d-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9c57d-137">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9c57d-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9c57d-138">Minimum supported server</span></span><br/> | <span data-ttu-id="9c57d-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9c57d-139">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9c57d-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="9c57d-140">Namespace</span></span><br/>                | <span data-ttu-id="9c57d-141">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="9c57d-141">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9c57d-142">MOF</span><span class="sxs-lookup"><span data-stu-id="9c57d-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9c57d-143"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9c57d-143"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9c57d-144">DLL</span><span class="sxs-lookup"><span data-stu-id="9c57d-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9c57d-145"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9c57d-145"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9c57d-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="9c57d-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c57d-147">**\_Dependência CIM**</span><span class="sxs-lookup"><span data-stu-id="9c57d-147">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

