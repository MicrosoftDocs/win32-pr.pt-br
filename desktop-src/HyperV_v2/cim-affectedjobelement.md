---
description: Representa uma associação entre um trabalho e os \_ objetos gerenciados CIM que podem ser afetados pela sua execução.
ms.assetid: 94c5e602-214c-4003-921c-8955c3859738
title: Classe CIM_AffectedJobElement
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AffectedJobElement
- CIM_AffectedJobElement.AffectedElement
- CIM_AffectedJobElement.AffectingElement
- CIM_AffectedJobElement.ElementEffects
- CIM_AffectedJobElement.OtherElementEffectsDescriptions
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 830e798ff12dc87c88126375736f116c044de731
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091404"
---
# <a name="cim_affectedjobelement-class"></a><span data-ttu-id="40e3f-103">\_Classe CIM AffectedJobElement</span><span class="sxs-lookup"><span data-stu-id="40e3f-103">CIM\_AffectedJobElement class</span></span>

<span data-ttu-id="40e3f-104">Representa uma associação entre um trabalho e os **objetos \_ gerenciados CIM** que podem ser afetados pela sua execução.</span><span class="sxs-lookup"><span data-stu-id="40e3f-104">Represents an association between a job and the **CIM\_ManagedElement** objects that may be affected by its execution.</span></span> <span data-ttu-id="40e3f-105">Talvez não seja possível que o trabalho Descreva todos os elementos afetados.</span><span class="sxs-lookup"><span data-stu-id="40e3f-105">It may not be feasible for the job to describe all of the affected elements.</span></span> <span data-ttu-id="40e3f-106">A principal finalidade dessa associação é fornecer informações quando um trabalho requer uso exclusivo dos elementos gerenciados afetados ou ao descrever os efeitos colaterais que podem resultar.</span><span class="sxs-lookup"><span data-stu-id="40e3f-106">The main purpose of this association is to provide information when a job requires exclusive use of the affected managed elements or when describing the side effects that may result.</span></span>

## <a name="syntax"></a><span data-ttu-id="40e3f-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="40e3f-107">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.15.0"), UMLPackagePath("CIM::System::Processing"), AMENDMENT]
class CIM_AffectedJobElement
{
  CIM_ManagedElement REF AffectedElement;
  CIM_Job            REF AffectingElement;
  uint16                 ElementEffects[];
  string                 OtherElementEffectsDescriptions[];
};
```

## <a name="members"></a><span data-ttu-id="40e3f-108">Membros</span><span class="sxs-lookup"><span data-stu-id="40e3f-108">Members</span></span>

<span data-ttu-id="40e3f-109">A classe **CIM \_ AffectedJobElement** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="40e3f-109">The **CIM\_AffectedJobElement** class has these types of members:</span></span>

-   [<span data-ttu-id="40e3f-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="40e3f-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="40e3f-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="40e3f-111">Properties</span></span>

<span data-ttu-id="40e3f-112">A classe **CIM \_ AffectedJobElement** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="40e3f-112">The **CIM\_AffectedJobElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="40e3f-113">**Afetadoselement**</span><span class="sxs-lookup"><span data-stu-id="40e3f-113">**AffectedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40e3f-114">Tipo de dados: **CIM \_ managedelement**</span><span class="sxs-lookup"><span data-stu-id="40e3f-114">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="40e3f-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="40e3f-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="40e3f-116">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="40e3f-116">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="40e3f-117">O elemento gerenciado afetado pela execução do trabalho.</span><span class="sxs-lookup"><span data-stu-id="40e3f-117">The managed element affected by the execution of the job.</span></span>

</dd> <dt>

<span data-ttu-id="40e3f-118">**Afetando**</span><span class="sxs-lookup"><span data-stu-id="40e3f-118">**AffectingElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40e3f-119">Tipo de dados **: \_ trabalho do CIM**</span><span class="sxs-lookup"><span data-stu-id="40e3f-119">Data type: **CIM\_Job**</span></span>
</dt> <dt>

<span data-ttu-id="40e3f-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="40e3f-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="40e3f-121">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="40e3f-121">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="40e3f-122">O trabalho que está afetando o elemento gerenciado.</span><span class="sxs-lookup"><span data-stu-id="40e3f-122">The job that is affecting the managed element.</span></span>

</dd> <dt>

<span data-ttu-id="40e3f-123">**ElementEffects**</span><span class="sxs-lookup"><span data-stu-id="40e3f-123">**ElementEffects**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40e3f-124">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="40e3f-124">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="40e3f-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="40e3f-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="40e3f-126">Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (**" \_ CIM AffectedJobElement**.**OtherElementEffectsDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="40e3f-126">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AffectedJobElement**.**OtherElementEffectsDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="40e3f-127">O efeito que o trabalho tem no elemento gerenciado.</span><span class="sxs-lookup"><span data-stu-id="40e3f-127">The effect the job has on the managed element.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="40e3f-128">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="40e3f-128">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="40e3f-129">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="40e3f-129">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Exclusive_Use"></span><span id="exclusive_use"></span><span id="EXCLUSIVE_USE"></span>

<span data-ttu-id="40e3f-130">**Uso exclusivo** (2)</span><span class="sxs-lookup"><span data-stu-id="40e3f-130">**Exclusive Use** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Performance_Impact"></span><span id="performance_impact"></span><span id="PERFORMANCE_IMPACT"></span>

<span data-ttu-id="40e3f-131">**Impacto no desempenho** (3)</span><span class="sxs-lookup"><span data-stu-id="40e3f-131">**Performance Impact** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Element_Integrity"></span><span id="element_integrity"></span><span id="ELEMENT_INTEGRITY"></span>

<span data-ttu-id="40e3f-132">**Integridade do elemento** (4)</span><span class="sxs-lookup"><span data-stu-id="40e3f-132">**Element Integrity** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Create"></span><span id="create"></span><span id="CREATE"></span>

<span data-ttu-id="40e3f-133">**Criar** (5)</span><span class="sxs-lookup"><span data-stu-id="40e3f-133">**Create** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="40e3f-134">**OtherElementEffectsDescriptions**</span><span class="sxs-lookup"><span data-stu-id="40e3f-134">**OtherElementEffectsDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40e3f-135">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="40e3f-135">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="40e3f-136">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="40e3f-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="40e3f-137">Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (**" \_ CIM AffectedJobElement**.**ElementEffects**")</span><span class="sxs-lookup"><span data-stu-id="40e3f-137">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AffectedJobElement**.**ElementEffects**")</span></span>
</dt> </dl>

<span data-ttu-id="40e3f-138">Detalhes adicionais para os valores "1" (outros) correspondentes na matriz **ElementEffects** .</span><span class="sxs-lookup"><span data-stu-id="40e3f-138">Additional details for corresponding "1" (Other) values in the **ElementEffects** array.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="40e3f-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="40e3f-139">Requirements</span></span>



| <span data-ttu-id="40e3f-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="40e3f-140">Requirement</span></span> | <span data-ttu-id="40e3f-141">Valor</span><span class="sxs-lookup"><span data-stu-id="40e3f-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="40e3f-142">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="40e3f-142">Minimum supported client</span></span><br/> | <span data-ttu-id="40e3f-143">Windows 8</span><span class="sxs-lookup"><span data-stu-id="40e3f-143">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="40e3f-144">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="40e3f-144">Minimum supported server</span></span><br/> | <span data-ttu-id="40e3f-145">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="40e3f-145">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="40e3f-146">Namespace</span><span class="sxs-lookup"><span data-stu-id="40e3f-146">Namespace</span></span><br/>                | <span data-ttu-id="40e3f-147">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="40e3f-147">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="40e3f-148">MOF</span><span class="sxs-lookup"><span data-stu-id="40e3f-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="40e3f-149"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="40e3f-149"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="40e3f-150">DLL</span><span class="sxs-lookup"><span data-stu-id="40e3f-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="40e3f-151"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="40e3f-151"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

