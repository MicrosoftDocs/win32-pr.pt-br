---
description: A \_ associação CIM PackageCooling representa a relação na qual um dispositivo de resfriamento é instalado em um pacote, como um chassi ou rack, para auxiliar na resfriamento do pacote.
ms.assetid: 0aaae8e1-6e70-4b26-8e56-dac5657e58c1
ms.tgt_platform: multiple
title: Classe CIM_PackageCooling
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PackageCooling
- CIM_PackageCooling.Dependent
- CIM_PackageCooling.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1f88cd3f07983870bed8fd2d740f3bf9051019b4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104500972"
---
# <a name="cim_packagecooling-class"></a><span data-ttu-id="03f9a-103">\_Classe CIM PackageCooling</span><span class="sxs-lookup"><span data-stu-id="03f9a-103">CIM\_PackageCooling class</span></span>

<span data-ttu-id="03f9a-104">A associação **CIM \_ PackageCooling** representa a relação na qual um dispositivo de resfriamento é instalado em um pacote, como um chassi ou rack, para auxiliar na resfriamento do pacote.</span><span class="sxs-lookup"><span data-stu-id="03f9a-104">The **CIM\_PackageCooling** association represents the relationship in which a cooling device is installed in a package, such as a chassis or rack, to assist with the package's cooling.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="03f9a-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="03f9a-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="03f9a-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="03f9a-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="03f9a-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="03f9a-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="03f9a-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="03f9a-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="03f9a-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="03f9a-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B8E-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PackageCooling : CIM_Dependency
{
  CIM_PhysicalPackage REF Dependent;
  CIM_CoolingDevice   REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="03f9a-110">Membros</span><span class="sxs-lookup"><span data-stu-id="03f9a-110">Members</span></span>

<span data-ttu-id="03f9a-111">A classe **CIM \_ PackageCooling** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="03f9a-111">The **CIM\_PackageCooling** class has these types of members:</span></span>

-   [<span data-ttu-id="03f9a-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="03f9a-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="03f9a-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="03f9a-113">Properties</span></span>

<span data-ttu-id="03f9a-114">A classe **CIM \_ PackageCooling** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="03f9a-114">The **CIM\_PackageCooling** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="03f9a-115">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="03f9a-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03f9a-116">Tipo de dados: **CIM \_ CoolingDevice**</span><span class="sxs-lookup"><span data-stu-id="03f9a-116">Data type: **CIM\_CoolingDevice**</span></span>
</dt> <dt>

<span data-ttu-id="03f9a-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="03f9a-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03f9a-118">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="03f9a-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="03f9a-119">Um [**\_ CoolingDevice CIM**](cim-coolingdevice.md) que descreve o dispositivo de resfriamento para o pacote.</span><span class="sxs-lookup"><span data-stu-id="03f9a-119">A [**CIM\_CoolingDevice**](cim-coolingdevice.md) that describes the cooling device for the package.</span></span>

</dd> <dt>

<span data-ttu-id="03f9a-120">**Depende**</span><span class="sxs-lookup"><span data-stu-id="03f9a-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03f9a-121">Tipo de dados: **CIM \_ PhysicalPackage**</span><span class="sxs-lookup"><span data-stu-id="03f9a-121">Data type: **CIM\_PhysicalPackage**</span></span>
</dt> <dt>

<span data-ttu-id="03f9a-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="03f9a-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03f9a-123">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")</span><span class="sxs-lookup"><span data-stu-id="03f9a-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="03f9a-124">Um [**\_ PhysicalPackage CIM**](cim-physicalpackage.md) que descreve o pacote físico cujo ambiente é resfriado.</span><span class="sxs-lookup"><span data-stu-id="03f9a-124">A [**CIM\_PhysicalPackage**](cim-physicalpackage.md) that describes the physical package whose environment is cooled.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="03f9a-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="03f9a-125">Remarks</span></span>

<span data-ttu-id="03f9a-126">**CIM \_ PackageCooling** é derivado da [**\_ dependência CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="03f9a-126">**CIM\_PackageCooling** is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="03f9a-127">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="03f9a-127">WMI does not implement this class.</span></span>

<span data-ttu-id="03f9a-128">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="03f9a-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="03f9a-129">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="03f9a-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="03f9a-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="03f9a-130">Requirements</span></span>



| <span data-ttu-id="03f9a-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="03f9a-131">Requirement</span></span> | <span data-ttu-id="03f9a-132">Valor</span><span class="sxs-lookup"><span data-stu-id="03f9a-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="03f9a-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="03f9a-133">Minimum supported client</span></span><br/> | <span data-ttu-id="03f9a-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="03f9a-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="03f9a-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="03f9a-135">Minimum supported server</span></span><br/> | <span data-ttu-id="03f9a-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="03f9a-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="03f9a-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="03f9a-137">Namespace</span></span><br/>                | <span data-ttu-id="03f9a-138">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="03f9a-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="03f9a-139">MOF</span><span class="sxs-lookup"><span data-stu-id="03f9a-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="03f9a-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="03f9a-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="03f9a-141">DLL</span><span class="sxs-lookup"><span data-stu-id="03f9a-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="03f9a-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="03f9a-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03f9a-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="03f9a-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03f9a-144">**\_Dependência CIM**</span><span class="sxs-lookup"><span data-stu-id="03f9a-144">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

