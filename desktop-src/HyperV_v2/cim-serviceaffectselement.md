---
description: Representa uma associação entre um serviço e um elemento gerenciado que pode ser afetado pela sua execução.
ms.assetid: 2fd9199f-9ab0-4c42-9708-d6cd6911f77a
title: Classe CIM_ServiceAffectsElement
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ServiceAffectsElement
- CIM_ServiceAffectsElement.AffectedElement
- CIM_ServiceAffectsElement.AffectingElement
- CIM_ServiceAffectsElement.ElementEffects
- CIM_ServiceAffectsElement.OtherElementEffectsDescriptions
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 2e4dd4fe00d1ee4a537741ce69240413e78aca85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756772"
---
# <a name="cim_serviceaffectselement-class"></a><span data-ttu-id="4da40-103">\_Classe CIM Imafetaelement</span><span class="sxs-lookup"><span data-stu-id="4da40-103">CIM\_ServiceAffectsElement class</span></span>

<span data-ttu-id="4da40-104">Representa uma associação entre um serviço e um elemento gerenciado que pode ser afetado pela sua execução.</span><span class="sxs-lookup"><span data-stu-id="4da40-104">Represents an association between a service and a managed element that might be affected by its execution.</span></span>

## <a name="syntax"></a><span data-ttu-id="4da40-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4da40-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.14.0"), UMLPackagePath("CIM::Core::Service"), AMENDMENT]
class CIM_ServiceAffectsElement
{
  CIM_ManagedElement REF AffectedElement;
  CIM_Service        REF AffectingElement;
  uint16                 ElementEffects[];
  string                 OtherElementEffectsDescriptions[];
};
```

## <a name="members"></a><span data-ttu-id="4da40-106">Membros</span><span class="sxs-lookup"><span data-stu-id="4da40-106">Members</span></span>

<span data-ttu-id="4da40-107">A classe **CIM \_ fileafetelement** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="4da40-107">The **CIM\_ServiceAffectsElement** class has these types of members:</span></span>

-   [<span data-ttu-id="4da40-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="4da40-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4da40-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="4da40-109">Properties</span></span>

<span data-ttu-id="4da40-110">A classe **CIM \_ fileafetelement** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="4da40-110">The **CIM\_ServiceAffectsElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4da40-111">**Afetadoselement**</span><span class="sxs-lookup"><span data-stu-id="4da40-111">**AffectedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4da40-112">Tipo de dados: **CIM \_ managedelement**</span><span class="sxs-lookup"><span data-stu-id="4da40-112">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="4da40-113">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4da40-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4da40-114">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="4da40-114">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="4da40-115">O elemento gerenciado que é afetado pelo serviço.</span><span class="sxs-lookup"><span data-stu-id="4da40-115">The managed element that is affected by the service.</span></span>

</dd> <dt>

<span data-ttu-id="4da40-116">**Afetando**</span><span class="sxs-lookup"><span data-stu-id="4da40-116">**AffectingElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4da40-117">Tipo de dados **: \_ serviço CIM**</span><span class="sxs-lookup"><span data-stu-id="4da40-117">Data type: **CIM\_Service**</span></span>
</dt> <dt>

<span data-ttu-id="4da40-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4da40-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4da40-119">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="4da40-119">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="4da40-120">O serviço que está afetando o elemento gerenciado.</span><span class="sxs-lookup"><span data-stu-id="4da40-120">The service that is affecting the managed element.</span></span>

</dd> <dt>

<span data-ttu-id="4da40-121">**ElementEffects**</span><span class="sxs-lookup"><span data-stu-id="4da40-121">**ElementEffects**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4da40-122">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4da40-122">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="4da40-123">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4da40-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4da40-124">Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (**" \_ CIM imafetaelement**.**OtherElementEffectsDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="4da40-124">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ServiceAffectsElement**.**OtherElementEffectsDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="4da40-125">O efeito no elemento gerenciado.</span><span class="sxs-lookup"><span data-stu-id="4da40-125">The effect on the managed element.</span></span> <span data-ttu-id="4da40-126">Essa matriz corresponde à matriz **OtherElementEffectsDescriptions** .</span><span class="sxs-lookup"><span data-stu-id="4da40-126">This array corresponds to the **OtherElementEffectsDescriptions** array.</span></span>

<span data-ttu-id="4da40-127">\- Uso exclusivo (2): nenhum outro serviço pode ter essa associação com o elemento.</span><span class="sxs-lookup"><span data-stu-id="4da40-127">\- Exclusive Use (2): No other Service may have this association to the element.</span></span>

<span data-ttu-id="4da40-128">\- Impacto no desempenho (3): preterido em favor de "consumir", "aprimorar o desempenho" ou "degradar o desempenho".</span><span class="sxs-lookup"><span data-stu-id="4da40-128">\- Performance Impact (3): Deprecated in favor of "Consumes", "Enhances Performance", or "Degrades Performance".</span></span> <span data-ttu-id="4da40-129">A execução do serviço pode aprimorar ou degradar o desempenho do elemento.</span><span class="sxs-lookup"><span data-stu-id="4da40-129">Execution of the Service may enhance or degrade the performance of the element.</span></span> <span data-ttu-id="4da40-130">Isso pode ser um efeito colateral de execução ou como uma conseqüência pretendida de métodos fornecidos pelo serviço.</span><span class="sxs-lookup"><span data-stu-id="4da40-130">This may be as a side-effect of execution or as an intended consequence of methods provided by the Service.</span></span>

<span data-ttu-id="4da40-131">\- Integridade do elemento (4): preterida em favor de "consumir", "aprimorar a integridade" ou "degradar a integridade".</span><span class="sxs-lookup"><span data-stu-id="4da40-131">\- Element Integrity (4): Deprecated in favor of "Consumes", "Enhances Integrity", or "Degrades Integrity".</span></span> <span data-ttu-id="4da40-132">A execução do serviço pode aprimorar ou degradar a integridade do elemento.</span><span class="sxs-lookup"><span data-stu-id="4da40-132">Execution of the Service may enhance or degrade the integrity of the element.</span></span> <span data-ttu-id="4da40-133">Isso pode ser um efeito colateral de execução ou como uma conseqüência pretendida de métodos fornecidos pelo serviço.</span><span class="sxs-lookup"><span data-stu-id="4da40-133">This may be as a side-effect of execution or as an intended consequence of methods provided by the Service.</span></span>

<span data-ttu-id="4da40-134">\- Gerencia (5): o serviço gerencia o elemento.</span><span class="sxs-lookup"><span data-stu-id="4da40-134">\- Manages (5): The Service manages the element.</span></span>

<span data-ttu-id="4da40-135">\- Consome (6): a execução do serviço consome parte ou todos os elementos associados como consequência da execução do serviço.</span><span class="sxs-lookup"><span data-stu-id="4da40-135">\- Consumes (6): Execution of the Service consumes some or all of the associated element as a consequence of running the Service.</span></span> <span data-ttu-id="4da40-136">Por exemplo, o serviço pode consumir ciclos de CPU, o que pode afetar o desempenho ou o armazenamento que pode afetar o desempenho e a integridade.</span><span class="sxs-lookup"><span data-stu-id="4da40-136">For example, the Service may consume CPU cycles, which may affect performance, or Storage which may affect both performance and integrity.</span></span> <span data-ttu-id="4da40-137">(Por exemplo, a falta de armazenamento livre pode prejudicar a integridade, reduzindo a capacidade de salvar o estado.</span><span class="sxs-lookup"><span data-stu-id="4da40-137">(For instance, the lack of free storage can degrade integrity by reducing the ability to save state.</span></span> <span data-ttu-id="4da40-138">) "Consuma" pode ser usado sozinha ou em conjunto com outros valores, em particular, "degradar o desempenho" e "degradar a integridade".</span><span class="sxs-lookup"><span data-stu-id="4da40-138">) "Consumes" may be used alone or in conjunction with other values, in particular, "Degrades Performance" and "Degrades Integrity".</span></span>

<span data-ttu-id="4da40-139">"Gerencia" e não "consome" devem ser usados para refletir os serviços de alocação que podem ser fornecidos por um serviço.</span><span class="sxs-lookup"><span data-stu-id="4da40-139">"Manages" and not "Consumes" should be used to reflect allocation services that may be provided by a Service.</span></span>

<span data-ttu-id="4da40-140">\- Aprimora a integridade (7): o serviço pode aprimorar a integridade do elemento associado.</span><span class="sxs-lookup"><span data-stu-id="4da40-140">\- Enhances Integrity (7): The Service may enhance integrity of the associated element.</span></span>

<span data-ttu-id="4da40-141">\- Degrada a integridade (8): o serviço pode prejudicar a integridade do elemento associado.</span><span class="sxs-lookup"><span data-stu-id="4da40-141">\- Degrades Integrity (8): The Service may degrade integrity of the associated element.</span></span>

<span data-ttu-id="4da40-142">\- Aprimora o desempenho (9): o serviço pode melhorar o desempenho do elemento associado.</span><span class="sxs-lookup"><span data-stu-id="4da40-142">\- Enhances Performance (9): The Service may enhance performance of the associated element.</span></span>

<span data-ttu-id="4da40-143">\- Degrada o desempenho (10): o serviço pode prejudicar o desempenho do elemento associado.</span><span class="sxs-lookup"><span data-stu-id="4da40-143">\- Degrades Performance (10): The Service may degrade performance of the associated element.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4da40-144">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="4da40-144">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="4da40-145">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="4da40-145">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Exclusive_Use"></span><span id="exclusive_use"></span><span id="EXCLUSIVE_USE"></span>

<span data-ttu-id="4da40-146">**Uso exclusivo** (2)</span><span class="sxs-lookup"><span data-stu-id="4da40-146">**Exclusive Use** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Performance_Impact"></span><span id="performance_impact"></span><span id="PERFORMANCE_IMPACT"></span>

<span data-ttu-id="4da40-147">**Impacto no desempenho** (3)</span><span class="sxs-lookup"><span data-stu-id="4da40-147">**Performance Impact** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Element_Integrity"></span><span id="element_integrity"></span><span id="ELEMENT_INTEGRITY"></span>

<span data-ttu-id="4da40-148">**Integridade do elemento** (4)</span><span class="sxs-lookup"><span data-stu-id="4da40-148">**Element Integrity** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Manages"></span><span id="manages"></span><span id="MANAGES"></span>

<span data-ttu-id="4da40-149">**Gerencia** (5)</span><span class="sxs-lookup"><span data-stu-id="4da40-149">**Manages** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Consumes"></span><span id="consumes"></span><span id="CONSUMES"></span>

<span data-ttu-id="4da40-150">**Consumo** (6)</span><span class="sxs-lookup"><span data-stu-id="4da40-150">**Consumes** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Enhances_Integrity"></span><span id="enhances_integrity"></span><span id="ENHANCES_INTEGRITY"></span>

<span data-ttu-id="4da40-151">**Aprimora a integridade** (7)</span><span class="sxs-lookup"><span data-stu-id="4da40-151">**Enhances Integrity** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Degrades_Integrity"></span><span id="degrades_integrity"></span><span id="DEGRADES_INTEGRITY"></span>

<span data-ttu-id="4da40-152">**Degradação da integridade** (8)</span><span class="sxs-lookup"><span data-stu-id="4da40-152">**Degrades Integrity** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Enhances_Performance"></span><span id="enhances_performance"></span><span id="ENHANCES_PERFORMANCE"></span>

<span data-ttu-id="4da40-153">**Melhora o desempenho** (9)</span><span class="sxs-lookup"><span data-stu-id="4da40-153">**Enhances Performance** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degrades_Performance"></span><span id="degrades_performance"></span><span id="DEGRADES_PERFORMANCE"></span>

<span data-ttu-id="4da40-154">**Degrada o desempenho** (10)</span><span class="sxs-lookup"><span data-stu-id="4da40-154">**Degrades Performance** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="4da40-155">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="4da40-155">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="4da40-156">**Fornecedor reservado** (0x8000.. 0xFFFF</span><span class="sxs-lookup"><span data-stu-id="4da40-156">**Vendor Reserved** (0x8000..0xFFFF)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4da40-157">**OtherElementEffectsDescriptions**</span><span class="sxs-lookup"><span data-stu-id="4da40-157">**OtherElementEffectsDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4da40-158">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="4da40-158">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="4da40-159">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4da40-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4da40-160">Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (**" \_ CIM imafetaelement**.**ElementEffects**")</span><span class="sxs-lookup"><span data-stu-id="4da40-160">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ServiceAffectsElement**.**ElementEffects**")</span></span>
</dt> </dl>

<span data-ttu-id="4da40-161">Cada item na matriz fornece informações adicionais para o item correspondente na matriz **ElementEffects** .</span><span class="sxs-lookup"><span data-stu-id="4da40-161">Each item in the array provides additional information for the corresponding item in the **ElementEffects** array.</span></span> <span data-ttu-id="4da40-162">Uma descrição é necessária para qualquer item na matriz **ElementEffects** que está definida como **Other** ("1").</span><span class="sxs-lookup"><span data-stu-id="4da40-162">A description is required for any item in the **ElementEffects** array that is set to **Other** ("1").</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4da40-163">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4da40-163">Requirements</span></span>



| <span data-ttu-id="4da40-164">Requisito</span><span class="sxs-lookup"><span data-stu-id="4da40-164">Requirement</span></span> | <span data-ttu-id="4da40-165">Valor</span><span class="sxs-lookup"><span data-stu-id="4da40-165">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4da40-166">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4da40-166">Minimum supported client</span></span><br/> | <span data-ttu-id="4da40-167">Windows 8</span><span class="sxs-lookup"><span data-stu-id="4da40-167">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="4da40-168">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4da40-168">Minimum supported server</span></span><br/> | <span data-ttu-id="4da40-169">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4da40-169">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="4da40-170">Namespace</span><span class="sxs-lookup"><span data-stu-id="4da40-170">Namespace</span></span><br/>                | <span data-ttu-id="4da40-171">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="4da40-171">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="4da40-172">MOF</span><span class="sxs-lookup"><span data-stu-id="4da40-172">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4da40-173"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4da40-173"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4da40-174">DLL</span><span class="sxs-lookup"><span data-stu-id="4da40-174">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4da40-175"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4da40-175"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

