---
description: A \_ classe CIM OperatingSystemSoftwareFeature representa os recursos de software que compõem o sistema operacional.
ms.assetid: 9ffc709c-213e-4252-9662-76f01e1685e5
ms.tgt_platform: multiple
title: Classe CIM_OperatingSystemSoftwareFeature
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_OperatingSystemSoftwareFeature
- CIM_OperatingSystemSoftwareFeature.PartComponent
- CIM_OperatingSystemSoftwareFeature.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b9d74478f211b23e103854cedb09a1e0186618b8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105754826"
---
# <a name="cim_operatingsystemsoftwarefeature-class"></a><span data-ttu-id="aec2c-103">\_Classe CIM OperatingSystemSoftwareFeature</span><span class="sxs-lookup"><span data-stu-id="aec2c-103">CIM\_OperatingSystemSoftwareFeature class</span></span>

<span data-ttu-id="aec2c-104">A classe **CIM \_ OperatingSystemSoftwareFeature** representa os recursos de software que compõem o sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="aec2c-104">The **CIM\_OperatingSystemSoftwareFeature** class represents the software features that make up the operating system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="aec2c-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="aec2c-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="aec2c-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="aec2c-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="aec2c-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="aec2c-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="aec2c-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="aec2c-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="aec2c-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="aec2c-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{96B4C734-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_OperatingSystemSoftwareFeature : CIM_Component
{
  CIM_SoftwareFeature REF PartComponent;
  CIM_OperatingSystem REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="aec2c-110">Membros</span><span class="sxs-lookup"><span data-stu-id="aec2c-110">Members</span></span>

<span data-ttu-id="aec2c-111">A classe **CIM \_ OperatingSystemSoftwareFeature** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="aec2c-111">The **CIM\_OperatingSystemSoftwareFeature** class has these types of members:</span></span>

-   [<span data-ttu-id="aec2c-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="aec2c-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="aec2c-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="aec2c-113">Properties</span></span>

<span data-ttu-id="aec2c-114">A classe **CIM \_ OperatingSystemSoftwareFeature** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="aec2c-114">The **CIM\_OperatingSystemSoftwareFeature** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="aec2c-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="aec2c-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aec2c-116">Tipo de dados: sistema **\_ operacional CIM**</span><span class="sxs-lookup"><span data-stu-id="aec2c-116">Data type: **CIM\_OperatingSystem**</span></span>
</dt> <dt>

<span data-ttu-id="aec2c-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="aec2c-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aec2c-118">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="aec2c-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="aec2c-119">Um [**\_ OperatingSystem CIM**](cim-operatingsystem.md) que descreve o sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="aec2c-119">A [**CIM\_OperatingSystem**](cim-operatingsystem.md) describing the operating system.</span></span>

</dd> <dt>

<span data-ttu-id="aec2c-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="aec2c-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aec2c-121">Tipo de dados: **CIM \_ SoftwareFeature**</span><span class="sxs-lookup"><span data-stu-id="aec2c-121">Data type: **CIM\_SoftwareFeature**</span></span>
</dt> <dt>

<span data-ttu-id="aec2c-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="aec2c-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aec2c-123">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="aec2c-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="aec2c-124">Um [**\_ SoftwareFeature CIM**](cim-softwarefeature.md) que descreve os recursos de software que compõem o sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="aec2c-124">A [**CIM\_SoftwareFeature**](cim-softwarefeature.md) describing the software features that make up the operating system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="aec2c-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="aec2c-125">Remarks</span></span>

<span data-ttu-id="aec2c-126">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="aec2c-126">WMI does not implement this class.</span></span>

<span data-ttu-id="aec2c-127">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="aec2c-127">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="aec2c-128">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="aec2c-128">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="aec2c-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aec2c-129">Requirements</span></span>



| <span data-ttu-id="aec2c-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="aec2c-130">Requirement</span></span> | <span data-ttu-id="aec2c-131">Valor</span><span class="sxs-lookup"><span data-stu-id="aec2c-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="aec2c-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="aec2c-132">Minimum supported client</span></span><br/> | <span data-ttu-id="aec2c-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="aec2c-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="aec2c-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="aec2c-134">Minimum supported server</span></span><br/> | <span data-ttu-id="aec2c-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="aec2c-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="aec2c-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="aec2c-136">Namespace</span></span><br/>                | <span data-ttu-id="aec2c-137">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="aec2c-137">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="aec2c-138">MOF</span><span class="sxs-lookup"><span data-stu-id="aec2c-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="aec2c-139"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="aec2c-139"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="aec2c-140">DLL</span><span class="sxs-lookup"><span data-stu-id="aec2c-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aec2c-141"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aec2c-141"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aec2c-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="aec2c-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aec2c-143">**\_Componente CIM**</span><span class="sxs-lookup"><span data-stu-id="aec2c-143">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 

