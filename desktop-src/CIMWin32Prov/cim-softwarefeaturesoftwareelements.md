---
description: A \_ associação CIM SoftwareFeatureSoftwareElements identifica os elementos de software que compõem um recurso de software específico.
ms.assetid: 933586c5-b85e-4136-b557-5151a48abc32
ms.tgt_platform: multiple
title: Classe CIM_SoftwareFeatureSoftwareElements
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SoftwareFeatureSoftwareElements
- CIM_SoftwareFeatureSoftwareElements.PartComponent
- CIM_SoftwareFeatureSoftwareElements.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 71712ebb3f8bf2ab2067325f16cf31af7fb1dc38
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756048"
---
# <a name="cim_softwarefeaturesoftwareelements-class"></a><span data-ttu-id="68e9c-103">\_Classe CIM SoftwareFeatureSoftwareElements</span><span class="sxs-lookup"><span data-stu-id="68e9c-103">CIM\_SoftwareFeatureSoftwareElements class</span></span>

<span data-ttu-id="68e9c-104">A associação **CIM \_ SoftwareFeatureSoftwareElements** identifica os elementos de software que compõem um recurso de software específico.</span><span class="sxs-lookup"><span data-stu-id="68e9c-104">The **CIM\_SoftwareFeatureSoftwareElements** association identifies the software elements that make up a specific software feature.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="68e9c-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="68e9c-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="68e9c-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="68e9c-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="68e9c-107">A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="68e9c-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="68e9c-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="68e9c-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="68e9c-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="68e9c-109">Syntax</span></span>

``` syntax
[UUID("{A91081E2-DB37-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_SoftwareFeatureSoftwareElements : CIM_Component
{
  CIM_SoftwareElement REF PartComponent;
  CIM_SoftwareFeature REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="68e9c-110">Membros</span><span class="sxs-lookup"><span data-stu-id="68e9c-110">Members</span></span>

<span data-ttu-id="68e9c-111">A classe **CIM \_ SoftwareFeatureSoftwareElements** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="68e9c-111">The **CIM\_SoftwareFeatureSoftwareElements** class has these types of members:</span></span>

-   [<span data-ttu-id="68e9c-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="68e9c-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="68e9c-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="68e9c-113">Properties</span></span>

<span data-ttu-id="68e9c-114">A classe **CIM \_ SoftwareFeatureSoftwareElements** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="68e9c-114">The **CIM\_SoftwareFeatureSoftwareElements** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="68e9c-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="68e9c-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68e9c-116">Tipo de dados: **CIM \_ SoftwareFeature**</span><span class="sxs-lookup"><span data-stu-id="68e9c-116">Data type: **CIM\_SoftwareFeature**</span></span>
</dt> <dt>

<span data-ttu-id="68e9c-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="68e9c-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68e9c-118">Qualificadores: [ **agregação**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="68e9c-118">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="68e9c-119">O componente de grupo.</span><span class="sxs-lookup"><span data-stu-id="68e9c-119">The group component.</span></span>

<span data-ttu-id="68e9c-120">Esta propriedade é herdada [**do \_ componente CIM**](cim-component.md).</span><span class="sxs-lookup"><span data-stu-id="68e9c-120">This property is inherited from [**CIM\_Component**](cim-component.md).</span></span>

</dd> <dt>

<span data-ttu-id="68e9c-121">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="68e9c-121">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68e9c-122">Tipo de dados: **CIM \_ softwareelement**</span><span class="sxs-lookup"><span data-stu-id="68e9c-122">Data type: **CIM\_SoftwareElement**</span></span>
</dt> <dt>

<span data-ttu-id="68e9c-123">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="68e9c-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68e9c-124">O componente da parte.</span><span class="sxs-lookup"><span data-stu-id="68e9c-124">The part component.</span></span>

<span data-ttu-id="68e9c-125">Esta propriedade é herdada [**do \_ componente CIM**](cim-component.md).</span><span class="sxs-lookup"><span data-stu-id="68e9c-125">This property is inherited from [**CIM\_Component**](cim-component.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="68e9c-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="68e9c-126">Remarks</span></span>

<span data-ttu-id="68e9c-127">A associação **CIM \_ SoftwareFeatureSoftwareElements** é derivada do [**\_ componente CIM**](cim-component.md).</span><span class="sxs-lookup"><span data-stu-id="68e9c-127">The **CIM\_SoftwareFeatureSoftwareElements** association is derived from [**CIM\_Component**](cim-component.md).</span></span>

<span data-ttu-id="68e9c-128">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="68e9c-128">WMI does not implement this class.</span></span> <span data-ttu-id="68e9c-129">Para classes WMI derivadas do **CIM \_ SoftwareFeatureSoftwareElements**, consulte [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="68e9c-129">For WMI classes derived from **CIM\_SoftwareFeatureSoftwareElements**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="68e9c-130">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="68e9c-130">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="68e9c-131">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="68e9c-131">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="68e9c-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="68e9c-132">Requirements</span></span>



| <span data-ttu-id="68e9c-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="68e9c-133">Requirement</span></span> | <span data-ttu-id="68e9c-134">Valor</span><span class="sxs-lookup"><span data-stu-id="68e9c-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="68e9c-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="68e9c-135">Minimum supported client</span></span><br/> | <span data-ttu-id="68e9c-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="68e9c-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="68e9c-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="68e9c-137">Minimum supported server</span></span><br/> | <span data-ttu-id="68e9c-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="68e9c-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="68e9c-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="68e9c-139">Namespace</span></span><br/>                | <span data-ttu-id="68e9c-140">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="68e9c-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="68e9c-141">MOF</span><span class="sxs-lookup"><span data-stu-id="68e9c-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="68e9c-142"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="68e9c-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="68e9c-143">DLL</span><span class="sxs-lookup"><span data-stu-id="68e9c-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="68e9c-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68e9c-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68e9c-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="68e9c-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68e9c-146">**\_Componente CIM**</span><span class="sxs-lookup"><span data-stu-id="68e9c-146">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 

