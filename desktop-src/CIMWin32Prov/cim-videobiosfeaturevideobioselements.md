---
description: A \_ classe CIM VideoBIOSFeatureVideoBIOSElements associa um recurso de BIOS de vídeo e seus elementos de BIOS de vídeo agregados.
ms.assetid: f1419505-213f-450e-8c96-45f547dd71da
ms.tgt_platform: multiple
title: Classe CIM_VideoBIOSFeatureVideoBIOSElements
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VideoBIOSFeatureVideoBIOSElements
- CIM_VideoBIOSFeatureVideoBIOSElements.PartComponent
- CIM_VideoBIOSFeatureVideoBIOSElements.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 421b6814499240b3364ac1aed622e2b7c96e7313
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089156"
---
# <a name="cim_videobiosfeaturevideobioselements-class"></a><span data-ttu-id="54bfd-103">\_Classe CIM VideoBIOSFeatureVideoBIOSElements</span><span class="sxs-lookup"><span data-stu-id="54bfd-103">CIM\_VideoBIOSFeatureVideoBIOSElements class</span></span>

<span data-ttu-id="54bfd-104">A classe **CIM \_ VideoBIOSFeatureVideoBIOSElements** associa um recurso de BIOS de vídeo e seus elementos de BIOS de vídeo agregados.</span><span class="sxs-lookup"><span data-stu-id="54bfd-104">The **CIM\_VideoBIOSFeatureVideoBIOSElements** class associates a video BIOS feature and its aggregated video BIOS elements.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="54bfd-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="54bfd-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="54bfd-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="54bfd-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="54bfd-107">A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="54bfd-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="54bfd-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="54bfd-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="54bfd-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="54bfd-109">Syntax</span></span>

``` syntax
[UUID("{B3F86390-DB37-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_VideoBIOSFeatureVideoBIOSElements : CIM_SoftwareFeatureSoftwareElements
{
  CIM_VideoBIOSElement REF PartComponent;
  CIM_VideoBIOSFeature REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="54bfd-110">Membros</span><span class="sxs-lookup"><span data-stu-id="54bfd-110">Members</span></span>

<span data-ttu-id="54bfd-111">A classe **CIM \_ VideoBIOSFeatureVideoBIOSElements** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="54bfd-111">The **CIM\_VideoBIOSFeatureVideoBIOSElements** class has these types of members:</span></span>

-   [<span data-ttu-id="54bfd-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="54bfd-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="54bfd-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="54bfd-113">Properties</span></span>

<span data-ttu-id="54bfd-114">A classe **CIM \_ VideoBIOSFeatureVideoBIOSElements** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="54bfd-114">The **CIM\_VideoBIOSFeatureVideoBIOSElements** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="54bfd-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="54bfd-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54bfd-116">Tipo de dados: **CIM \_ VideoBIOSFeature**</span><span class="sxs-lookup"><span data-stu-id="54bfd-116">Data type: **CIM\_VideoBIOSFeature**</span></span>
</dt> <dt>

<span data-ttu-id="54bfd-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="54bfd-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="54bfd-118">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="54bfd-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="54bfd-119">Um [**\_ VideoBIOSFeature CIM**](cim-videobiosfeature.md) que descreve o recurso do BIOS de vídeo.</span><span class="sxs-lookup"><span data-stu-id="54bfd-119">A [**CIM\_VideoBIOSFeature**](cim-videobiosfeature.md) that describes the video BIOS feature.</span></span>

</dd> <dt>

<span data-ttu-id="54bfd-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="54bfd-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54bfd-121">Tipo de dados: **CIM \_ VideoBIOSElement**</span><span class="sxs-lookup"><span data-stu-id="54bfd-121">Data type: **CIM\_VideoBIOSElement**</span></span>
</dt> <dt>

<span data-ttu-id="54bfd-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="54bfd-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="54bfd-123">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="54bfd-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="54bfd-124">Um [**\_ VideoBIOSElement CIM**](cim-videobioselement.md) que descreve o elemento de BIOS de vídeo que implementa os recursos descritos pelo recurso de BIOS de vídeo.</span><span class="sxs-lookup"><span data-stu-id="54bfd-124">A [**CIM\_VideoBIOSElement**](cim-videobioselement.md) that describes the video BIOS element that implements the capabilities described by video BIOS feature.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="54bfd-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="54bfd-125">Remarks</span></span>

<span data-ttu-id="54bfd-126">A classe **CIM \_ VideoBIOSFeatureVideoBIOSElements** é derivada de [**\_ SoftwareFeatureSoftwareElements CIM**](cim-softwarefeaturesoftwareelements.md).</span><span class="sxs-lookup"><span data-stu-id="54bfd-126">The **CIM\_VideoBIOSFeatureVideoBIOSElements** class is derived from [**CIM\_SoftwareFeatureSoftwareElements**](cim-softwarefeaturesoftwareelements.md).</span></span>

<span data-ttu-id="54bfd-127">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="54bfd-127">WMI does not implement this class.</span></span>

<span data-ttu-id="54bfd-128">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="54bfd-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="54bfd-129">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="54bfd-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="54bfd-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="54bfd-130">Requirements</span></span>



| <span data-ttu-id="54bfd-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="54bfd-131">Requirement</span></span> | <span data-ttu-id="54bfd-132">Valor</span><span class="sxs-lookup"><span data-stu-id="54bfd-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="54bfd-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="54bfd-133">Minimum supported client</span></span><br/> | <span data-ttu-id="54bfd-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="54bfd-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="54bfd-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="54bfd-135">Minimum supported server</span></span><br/> | <span data-ttu-id="54bfd-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="54bfd-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="54bfd-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="54bfd-137">Namespace</span></span><br/>                | <span data-ttu-id="54bfd-138">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="54bfd-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="54bfd-139">MOF</span><span class="sxs-lookup"><span data-stu-id="54bfd-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="54bfd-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="54bfd-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="54bfd-141">DLL</span><span class="sxs-lookup"><span data-stu-id="54bfd-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="54bfd-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="54bfd-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54bfd-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="54bfd-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54bfd-144">**\_SOFTWAREFEATURESOFTWAREELEMENTS CIM**</span><span class="sxs-lookup"><span data-stu-id="54bfd-144">**CIM\_SoftwareFeatureSoftwareElements**</span></span>](cim-softwarefeaturesoftwareelements.md)
</dt> </dl>

 

