---
description: A \_ classe CIM SoftwareElementVersionCheck representa um tipo de elemento de software que deve existir no ambiente.
ms.assetid: a1c0f0d5-2586-499c-bd82-bbb107570d81
ms.tgt_platform: multiple
title: Classe CIM_SoftwareElementVersionCheck
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SoftwareElementVersionCheck
- CIM_SoftwareElementVersionCheck.Caption
- CIM_SoftwareElementVersionCheck.CheckID
- CIM_SoftwareElementVersionCheck.CheckMode
- CIM_SoftwareElementVersionCheck.Description
- CIM_SoftwareElementVersionCheck.LowerSoftwareElementVersion
- CIM_SoftwareElementVersionCheck.Name
- CIM_SoftwareElementVersionCheck.SoftwareElementID
- CIM_SoftwareElementVersionCheck.SoftwareElementName
- CIM_SoftwareElementVersionCheck.SoftwareElementState
- CIM_SoftwareElementVersionCheck.SoftwareElementStateDesired
- CIM_SoftwareElementVersionCheck.TargetOperatingSystem
- CIM_SoftwareElementVersionCheck.TargetOperatingSystemDesired
- CIM_SoftwareElementVersionCheck.UpperSoftwareElementVersion
- CIM_SoftwareElementVersionCheck.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: eb55a44a3aba9092567cdc91b668ba1b63e33174
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104163912"
---
# <a name="cim_softwareelementversioncheck-class"></a><span data-ttu-id="afa8f-103">\_Classe CIM SoftwareElementVersionCheck</span><span class="sxs-lookup"><span data-stu-id="afa8f-103">CIM\_SoftwareElementVersionCheck class</span></span>

<span data-ttu-id="afa8f-104">A classe **CIM \_ SoftwareElementVersionCheck** representa um tipo de elemento de software que deve existir no ambiente.</span><span class="sxs-lookup"><span data-stu-id="afa8f-104">The **CIM\_SoftwareElementVersionCheck** class represents a type of software element that must exist in the environment.</span></span> <span data-ttu-id="afa8f-105">Essa verificação pode ser para um determinado, mínimo, máximo ou um intervalo de versões.</span><span class="sxs-lookup"><span data-stu-id="afa8f-105">This check can be for a specific, minimum, maximum, or a range of versions.</span></span> <span data-ttu-id="afa8f-106">Para especificar uma versão específica, as versões inferior e superior devem ser as mesmas.</span><span class="sxs-lookup"><span data-stu-id="afa8f-106">To specify a specific version, the lower and upper versions must be the same.</span></span> <span data-ttu-id="afa8f-107">Para especificar uma versão mínima, especifique apenas a versão inferior.</span><span class="sxs-lookup"><span data-stu-id="afa8f-107">To specify a minimum version, specify only the lower version.</span></span> <span data-ttu-id="afa8f-108">Para especificar uma versão máxima, especifique apenas a versão superior.</span><span class="sxs-lookup"><span data-stu-id="afa8f-108">To specify a maximum version, specify only the upper version.</span></span> <span data-ttu-id="afa8f-109">Para especificar um intervalo, as versões superior e inferior devem ser especificadas.</span><span class="sxs-lookup"><span data-stu-id="afa8f-109">To specify a range, both upper and lower versions must be specified.</span></span> <span data-ttu-id="afa8f-110">Os detalhes das verificações são comparados com os detalhes correspondentes encontrados em um objeto [**CIM \_ softwareelement**](cim-softwareelement.md) referenciado por uma associação [**\_ InstalledSoftwareElement**](cim-installedsoftwareelement.md) do CIM para o objeto de [**\_ ComputerSystem do CIM**](cim-computersystem.md) .</span><span class="sxs-lookup"><span data-stu-id="afa8f-110">Details of the checks are compared with the corresponding details found in a [**CIM\_SoftwareElement**](cim-softwareelement.md) object referenced by a [**CIM\_InstalledSoftwareElement**](cim-installedsoftwareelement.md) association for the [**CIM\_ComputerSystem**](cim-computersystem.md) object.</span></span> <span data-ttu-id="afa8f-111">Pelo menos um **CIM \_ softwareelement** precisa satisfazer os detalhes da condição para que a verificação seja satisfeita.</span><span class="sxs-lookup"><span data-stu-id="afa8f-111">At least one **CIM\_SoftwareElement** needs to satisfy the details of the condition for the check to be satisfied.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="afa8f-112">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="afa8f-112">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="afa8f-113">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="afa8f-113">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="afa8f-114">A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="afa8f-114">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="afa8f-115">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="afa8f-115">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="afa8f-116">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="afa8f-116">Syntax</span></span>

``` syntax
[UUID("{4D23FBD0-DB31-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_SoftwareElementVersionCheck : CIM_Check
{
  string  Caption;
  string  CheckID;
  boolean CheckMode;
  string  Description;
  string  LowerSoftwareElementVersion;
  string  Name;
  string  SoftwareElementID;
  string  SoftwareElementName;
  uint16  SoftwareElementState;
  uint16  SoftwareElementStateDesired;
  uint16  TargetOperatingSystem;
  uint16  TargetOperatingSystemDesired;
  string  UpperSoftwareElementVersion;
  string  Version;
};
```

## <a name="members"></a><span data-ttu-id="afa8f-117">Membros</span><span class="sxs-lookup"><span data-stu-id="afa8f-117">Members</span></span>

<span data-ttu-id="afa8f-118">A classe **CIM \_ SoftwareElementVersionCheck** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="afa8f-118">The **CIM\_SoftwareElementVersionCheck** class has these types of members:</span></span>

-   [<span data-ttu-id="afa8f-119">Métodos</span><span class="sxs-lookup"><span data-stu-id="afa8f-119">Methods</span></span>](#methods)
-   [<span data-ttu-id="afa8f-120">Propriedades</span><span class="sxs-lookup"><span data-stu-id="afa8f-120">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="afa8f-121">Métodos</span><span class="sxs-lookup"><span data-stu-id="afa8f-121">Methods</span></span>

<span data-ttu-id="afa8f-122">A classe **CIM \_ SoftwareElementVersionCheck** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="afa8f-122">The **CIM\_SoftwareElementVersionCheck** class has these methods.</span></span>



| <span data-ttu-id="afa8f-123">Método</span><span class="sxs-lookup"><span data-stu-id="afa8f-123">Method</span></span>                                                                   | <span data-ttu-id="afa8f-124">Descrição</span><span class="sxs-lookup"><span data-stu-id="afa8f-124">Description</span></span>                                                   |
|:-------------------------------------------------------------------------|:--------------------------------------------------------------|
| [<span data-ttu-id="afa8f-125">**Chame**</span><span class="sxs-lookup"><span data-stu-id="afa8f-125">**Invoke**</span></span>](invoke-method-in-class-cim-softwareelementversioncheck.md) | <span data-ttu-id="afa8f-126">Executa uma ação específica.</span><span class="sxs-lookup"><span data-stu-id="afa8f-126">Takes a particular action.</span></span> <span data-ttu-id="afa8f-127">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="afa8f-127">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="afa8f-128">Propriedades</span><span class="sxs-lookup"><span data-stu-id="afa8f-128">Properties</span></span>

<span data-ttu-id="afa8f-129">A classe **CIM \_ SoftwareElementVersionCheck** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="afa8f-129">The **CIM\_SoftwareElementVersionCheck** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="afa8f-130">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="afa8f-130">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afa8f-131">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="afa8f-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="afa8f-132">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="afa8f-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="afa8f-133">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="afa8f-133">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="afa8f-134">Breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="afa8f-134">Short textual description of the object.</span></span>

<span data-ttu-id="afa8f-135">Essa propriedade é herdada [**da \_ verificação CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="afa8f-135">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="afa8f-136">**CheckID**</span><span class="sxs-lookup"><span data-stu-id="afa8f-136">**CheckID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afa8f-137">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="afa8f-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="afa8f-138">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="afa8f-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="afa8f-139">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="afa8f-139">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="afa8f-140">Identificador usado em conjunto com outras chaves para identificar exclusivamente a verificação.</span><span class="sxs-lookup"><span data-stu-id="afa8f-140">Identifier used in conjunction with other keys to uniquely identify the check.</span></span>

<span data-ttu-id="afa8f-141">Essa propriedade é herdada [**da \_ verificação CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="afa8f-141">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="afa8f-142">**CheckMode**</span><span class="sxs-lookup"><span data-stu-id="afa8f-142">**CheckMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afa8f-143">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="afa8f-143">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="afa8f-144">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="afa8f-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="afa8f-145">Se for **true**, espera-se que a condição exista no ambiente (por exemplo, se um arquivo estiver em um sistema, o método [**Invoke**](invoke-method-in-class-cim-softwareelementversioncheck.md) deverá retornar **true**).</span><span class="sxs-lookup"><span data-stu-id="afa8f-145">If **TRUE**, the condition is expected to exist in the environment (for example, if a file is on a system, the [**Invoke**](invoke-method-in-class-cim-softwareelementversioncheck.md) method should return **TRUE**).</span></span> <span data-ttu-id="afa8f-146">Se for **false**, a condição não deverá existir (por exemplo, se um arquivo não estiver em um sistema, o método **Invoke** deverá retornar **false**).</span><span class="sxs-lookup"><span data-stu-id="afa8f-146">If **FALSE**, the condition should not exist (for example, if a file is not on a system, the **Invoke** method should return **FALSE**).</span></span>

<span data-ttu-id="afa8f-147">Essa propriedade é herdada [**da \_ verificação CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="afa8f-147">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="afa8f-148">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="afa8f-148">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afa8f-149">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="afa8f-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="afa8f-150">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="afa8f-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="afa8f-151">Descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="afa8f-151">Description of the object.</span></span>

<span data-ttu-id="afa8f-152">Essa propriedade é herdada [**da \_ verificação CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="afa8f-152">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="afa8f-153">**LowerSoftwareElementVersion**</span><span class="sxs-lookup"><span data-stu-id="afa8f-153">**LowerSoftwareElementVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afa8f-154">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="afa8f-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="afa8f-155">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="afa8f-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="afa8f-156">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ softwareelement**](cim-softwareelement.md).**Version**")</span><span class="sxs-lookup"><span data-stu-id="afa8f-156">Qualifiers: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Version**")</span></span>
</dt> </dl>

<span data-ttu-id="afa8f-157">Versão mínima de um elemento de software que está sendo verificado.</span><span class="sxs-lookup"><span data-stu-id="afa8f-157">Minimum version of a software elements being checked.</span></span>

</dd> <dt>

<span data-ttu-id="afa8f-158">**Nome**</span><span class="sxs-lookup"><span data-stu-id="afa8f-158">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afa8f-159">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="afa8f-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="afa8f-160">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="afa8f-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="afa8f-161">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ softwareelement**](cim-softwareelement.md).**Name**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="afa8f-161">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Name**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="afa8f-162">Nome usado para identificar o elemento de software.</span><span class="sxs-lookup"><span data-stu-id="afa8f-162">Name used to identify the software element.</span></span>

<span data-ttu-id="afa8f-163">Essa propriedade é herdada [**da \_ verificação CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="afa8f-163">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="afa8f-164">**SoftwareElementID**</span><span class="sxs-lookup"><span data-stu-id="afa8f-164">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afa8f-165">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="afa8f-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="afa8f-166">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="afa8f-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="afa8f-167">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ softwareelement**](cim-softwareelement.md).**SoftwareElementID**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="afa8f-167">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="afa8f-168">Identificador para o elemento de software.</span><span class="sxs-lookup"><span data-stu-id="afa8f-168">Identifier for the software element.</span></span>

<span data-ttu-id="afa8f-169">Essa propriedade é herdada [**da \_ verificação CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="afa8f-169">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="afa8f-170">**SoftwareElementName**</span><span class="sxs-lookup"><span data-stu-id="afa8f-170">**SoftwareElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afa8f-171">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="afa8f-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="afa8f-172">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="afa8f-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="afa8f-173">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ softwareelement**](cim-softwareelement.md).**Nome**")</span><span class="sxs-lookup"><span data-stu-id="afa8f-173">Qualifiers: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Name**")</span></span>
</dt> </dl>

<span data-ttu-id="afa8f-174">Nome do elemento de software que está sendo verificado.</span><span class="sxs-lookup"><span data-stu-id="afa8f-174">Name of the software element being checked.</span></span>

</dd> <dt>

<span data-ttu-id="afa8f-175">**SoftwareElementState**</span><span class="sxs-lookup"><span data-stu-id="afa8f-175">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afa8f-176">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="afa8f-176">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="afa8f-177">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="afa8f-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="afa8f-178">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ softwareelement**](cim-softwareelement.md).**SoftwareElementState**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="afa8f-178">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="afa8f-179">Estado de um elemento de software.</span><span class="sxs-lookup"><span data-stu-id="afa8f-179">State of a software element.</span></span>

<span data-ttu-id="afa8f-180">Essa propriedade é herdada [**da \_ verificação CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="afa8f-180">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="afa8f-181"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Implantável** (0)</span><span class="sxs-lookup"><span data-stu-id="afa8f-181"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Deployable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="afa8f-182">Descreve os detalhes necessários para a distribuição bem-sucedida e os detalhes (condições e ações) necessários para criar um elemento de software no estado instalável (ou seja, o próximo estado).</span><span class="sxs-lookup"><span data-stu-id="afa8f-182">Describes the details necessary for successful distribution and the details (conditions and actions) required to create a software element in the installable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="afa8f-183"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Instalável** (1)</span><span class="sxs-lookup"><span data-stu-id="afa8f-183"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="afa8f-184">Descreve os detalhes necessários para a instalação bem-sucedida e os detalhes (condições e ações) necessários para criar um elemento de software no estado executável (ou seja, o próximo estado).</span><span class="sxs-lookup"><span data-stu-id="afa8f-184">Describes the details necessary for successful installation and the details (conditions and actions) required to create a software element in the executable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="afa8f-185"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executável** (2)</span><span class="sxs-lookup"><span data-stu-id="afa8f-185"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="afa8f-186">Descreve os detalhes necessários para a execução bem-sucedida e os detalhes (condições e ações) necessários para criar um elemento de software no estado em execução (ou seja, o próximo estado).</span><span class="sxs-lookup"><span data-stu-id="afa8f-186">Describes the details necessary for successful execution and the details (conditions and actions) required to create a software element in the running state (that is, the next state).</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="afa8f-187"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Em execução** (3)</span><span class="sxs-lookup"><span data-stu-id="afa8f-187"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd>

<span data-ttu-id="afa8f-188">Descreve os detalhes necessários para monitorar e operar em um elemento inicial.</span><span class="sxs-lookup"><span data-stu-id="afa8f-188">Describes the details necessary to monitor and operate on a start element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="afa8f-189">**SoftwareElementStateDesired**</span><span class="sxs-lookup"><span data-stu-id="afa8f-189">**SoftwareElementStateDesired**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afa8f-190">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="afa8f-190">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="afa8f-191">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="afa8f-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="afa8f-192">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ softwareelement**](cim-softwareelement.md).**SoftwareElementState**")</span><span class="sxs-lookup"><span data-stu-id="afa8f-192">Qualifiers: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**")</span></span>
</dt> </dl>

<span data-ttu-id="afa8f-193">Estado do elemento de software que está sendo verificado.</span><span class="sxs-lookup"><span data-stu-id="afa8f-193">State of the software element being checked.</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="afa8f-194"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Implantável** (0)</span><span class="sxs-lookup"><span data-stu-id="afa8f-194"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Deployable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="afa8f-195">Descreve os detalhes necessários para a distribuição bem-sucedida e os detalhes (condições e ações) necessários para criar um elemento de software no estado instalável (ou seja, o próximo estado).</span><span class="sxs-lookup"><span data-stu-id="afa8f-195">Describes the details necessary for successful distribution and the details (conditions and actions) required to create a software element in the installable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="afa8f-196"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Instalável** (1)</span><span class="sxs-lookup"><span data-stu-id="afa8f-196"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="afa8f-197">Descreve os detalhes necessários para a instalação bem-sucedida e os detalhes (condições e ações) necessários para criar um elemento de software no estado executável (ou seja, o próximo estado).</span><span class="sxs-lookup"><span data-stu-id="afa8f-197">Describes the details necessary for successful installation and the details (conditions and actions) required to create a software element in the executable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="afa8f-198"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executável** (2)</span><span class="sxs-lookup"><span data-stu-id="afa8f-198"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="afa8f-199">Descreve os detalhes necessários para a execução bem-sucedida e os detalhes (condições e ações) necessários para criar um elemento de software no estado em execução (ou seja, o próximo estado).</span><span class="sxs-lookup"><span data-stu-id="afa8f-199">Describes the details necessary for successful execution and the details (conditions and actions) required to create a software element in the running state (that is, the next state).</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="afa8f-200"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Em execução** (3)</span><span class="sxs-lookup"><span data-stu-id="afa8f-200"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd>

<span data-ttu-id="afa8f-201">Descreve os detalhes necessários para monitorar e operar em um elemento inicial.</span><span class="sxs-lookup"><span data-stu-id="afa8f-201">Describes the details necessary to monitor and operate on a start element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="afa8f-202">**TargetOperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="afa8f-202">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afa8f-203">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="afa8f-203">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="afa8f-204">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="afa8f-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="afa8f-205">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ softwareelement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Informações do componente de software DMTF \| 2,5 ")</span><span class="sxs-lookup"><span data-stu-id="afa8f-205">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.5")</span></span>
</dt> </dl>

<span data-ttu-id="afa8f-206">Sistema operacional de destino do elemento de software.</span><span class="sxs-lookup"><span data-stu-id="afa8f-206">Target operating system of the software element.</span></span>

<span data-ttu-id="afa8f-207">Essa propriedade é herdada [**da \_ verificação CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="afa8f-207">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="afa8f-208"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="afa8f-208"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="afa8f-209"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="afa8f-209"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="afa8f-210"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span><span class="sxs-lookup"><span data-stu-id="afa8f-210"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="afa8f-211">Mac OS</span><span class="sxs-lookup"><span data-stu-id="afa8f-211">Mac OS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="afa8f-212"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span><span class="sxs-lookup"><span data-stu-id="afa8f-212"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd>

<span data-ttu-id="afa8f-213">ATT UNIX</span><span class="sxs-lookup"><span data-stu-id="afa8f-213">ATT UNIX</span></span>

</dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="afa8f-214"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span><span class="sxs-lookup"><span data-stu-id="afa8f-214"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="afa8f-215"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span><span class="sxs-lookup"><span data-stu-id="afa8f-215"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="afa8f-216"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Unix Digital** (6)</span><span class="sxs-lookup"><span data-stu-id="afa8f-216"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="afa8f-217"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span><span class="sxs-lookup"><span data-stu-id="afa8f-217"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="afa8f-218">Abrir VMS</span><span class="sxs-lookup"><span data-stu-id="afa8f-218">Open VMS</span></span>

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="afa8f-219"><span id="HPUX"></span><span id="hpux"></span>HP **(8** )</span><span class="sxs-lookup"><span data-stu-id="afa8f-219"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd>

<span data-ttu-id="afa8f-220">HP-UX</span><span class="sxs-lookup"><span data-stu-id="afa8f-220">HP-UX</span></span>

</dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="afa8f-221"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span><span class="sxs-lookup"><span data-stu-id="afa8f-221"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="afa8f-222"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span><span class="sxs-lookup"><span data-stu-id="afa8f-222"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="afa8f-223"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span><span class="sxs-lookup"><span data-stu-id="afa8f-223"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="afa8f-224"><span id="OS_2"></span><span id="os_2"></span>**Sistema operacional/2** (12)</span><span class="sxs-lookup"><span data-stu-id="afa8f-224"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="afa8f-225"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span><span class="sxs-lookup"><span data-stu-id="afa8f-225"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd>

<span data-ttu-id="afa8f-226">VM (máquina virtual) da Microsoft para Java</span><span class="sxs-lookup"><span data-stu-id="afa8f-226">Microsoft Virtual Machine (VM) for Java</span></span>

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="afa8f-227"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span><span class="sxs-lookup"><span data-stu-id="afa8f-227"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="afa8f-228"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span><span class="sxs-lookup"><span data-stu-id="afa8f-228"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd>

<span data-ttu-id="afa8f-229">Windows 3. x</span><span class="sxs-lookup"><span data-stu-id="afa8f-229">Windows 3.x</span></span>

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="afa8f-230"><span id="WIN95"></span><span id="win95"></span>**Win95** (16)</span><span class="sxs-lookup"><span data-stu-id="afa8f-230"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd>

<span data-ttu-id="afa8f-231">Windows 95</span><span class="sxs-lookup"><span data-stu-id="afa8f-231">Windows 95</span></span>

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="afa8f-232"><span id="WIN98"></span><span id="win98"></span>**Win98** (17)</span><span class="sxs-lookup"><span data-stu-id="afa8f-232"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd>

<span data-ttu-id="afa8f-233">Windows 98</span><span class="sxs-lookup"><span data-stu-id="afa8f-233">Windows 98</span></span>

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="afa8f-234"><span id="WINNT"></span><span id="winnt"></span>**WinNT** (18)</span><span class="sxs-lookup"><span data-stu-id="afa8f-234"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd>

<span data-ttu-id="afa8f-235">Windows NT</span><span class="sxs-lookup"><span data-stu-id="afa8f-235">Windows NT</span></span>

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="afa8f-236"><span id="WINCE"></span><span id="wince"></span>**WinCE** (19)</span><span class="sxs-lookup"><span data-stu-id="afa8f-236"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd>

<span data-ttu-id="afa8f-237">Windows CE</span><span class="sxs-lookup"><span data-stu-id="afa8f-237">Windows CE</span></span>

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="afa8f-238"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span><span class="sxs-lookup"><span data-stu-id="afa8f-238"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd>

<span data-ttu-id="afa8f-239">NCR 3000</span><span class="sxs-lookup"><span data-stu-id="afa8f-239">NCR 3000</span></span>

</dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="afa8f-240"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span><span class="sxs-lookup"><span data-stu-id="afa8f-240"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="afa8f-241"><span id="OSF"></span><span id="osf"></span>**Uso** (22)</span><span class="sxs-lookup"><span data-stu-id="afa8f-241"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="afa8f-242"><span id="DC_OS"></span><span id="dc_os"></span>**DC/os** (23)</span><span class="sxs-lookup"><span data-stu-id="afa8f-242"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="afa8f-243"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Unix dependente** (24)</span><span class="sxs-lookup"><span data-stu-id="afa8f-243"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="afa8f-244"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span><span class="sxs-lookup"><span data-stu-id="afa8f-244"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="afa8f-245"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span><span class="sxs-lookup"><span data-stu-id="afa8f-245"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="afa8f-246"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Subsequentes** (27)</span><span class="sxs-lookup"><span data-stu-id="afa8f-246"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="afa8f-247"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span><span class="sxs-lookup"><span data-stu-id="afa8f-247"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="afa8f-248"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span><span class="sxs-lookup"><span data-stu-id="afa8f-248"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="afa8f-249"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span><span class="sxs-lookup"><span data-stu-id="afa8f-249"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="afa8f-250"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span><span class="sxs-lookup"><span data-stu-id="afa8f-250"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="afa8f-251"><span id="ASERIES"></span><span id="aseries"></span>**ASeries** (32)</span><span class="sxs-lookup"><span data-stu-id="afa8f-251"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd>

<span data-ttu-id="afa8f-252">Uma série</span><span class="sxs-lookup"><span data-stu-id="afa8f-252">A Series</span></span>

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="afa8f-253"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span><span class="sxs-lookup"><span data-stu-id="afa8f-253"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd>

<span data-ttu-id="afa8f-254">NSK tandem</span><span class="sxs-lookup"><span data-stu-id="afa8f-254">Tandem NSK</span></span>

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="afa8f-255"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span><span class="sxs-lookup"><span data-stu-id="afa8f-255"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd>

<span data-ttu-id="afa8f-256">NT em tandem</span><span class="sxs-lookup"><span data-stu-id="afa8f-256">Tandem NT</span></span>

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="afa8f-257"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span><span class="sxs-lookup"><span data-stu-id="afa8f-257"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd>

<span data-ttu-id="afa8f-258">BS2000/OSD</span><span class="sxs-lookup"><span data-stu-id="afa8f-258">BS2000/OSD</span></span>

</dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="afa8f-259"><span id="LINUX"></span><span id="linux"></span>**Linux** (36)</span><span class="sxs-lookup"><span data-stu-id="afa8f-259"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="afa8f-260"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span><span class="sxs-lookup"><span data-stu-id="afa8f-260"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="afa8f-261"><span id="XENIX"></span><span id="xenix"></span>**Xenix** (38)</span><span class="sxs-lookup"><span data-stu-id="afa8f-261"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="afa8f-262"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span><span class="sxs-lookup"><span data-stu-id="afa8f-262"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="afa8f-263"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Unix interativo** (40)</span><span class="sxs-lookup"><span data-stu-id="afa8f-263"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="afa8f-264"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span><span class="sxs-lookup"><span data-stu-id="afa8f-264"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd>

<span data-ttu-id="afa8f-265">BSD UNIX</span><span class="sxs-lookup"><span data-stu-id="afa8f-265">BSD UNIX</span></span>

</dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="afa8f-266"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span><span class="sxs-lookup"><span data-stu-id="afa8f-266"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="afa8f-267"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span><span class="sxs-lookup"><span data-stu-id="afa8f-267"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="afa8f-268"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span><span class="sxs-lookup"><span data-stu-id="afa8f-268"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="afa8f-269"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span><span class="sxs-lookup"><span data-stu-id="afa8f-269"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd>

<span data-ttu-id="afa8f-270">Mac OS 9</span><span class="sxs-lookup"><span data-stu-id="afa8f-270">Mac OS 9</span></span>

</dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="afa8f-271"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**Kernel Mach** (46)</span><span class="sxs-lookup"><span data-stu-id="afa8f-271"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="afa8f-272"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span><span class="sxs-lookup"><span data-stu-id="afa8f-272"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="afa8f-273"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span><span class="sxs-lookup"><span data-stu-id="afa8f-273"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="afa8f-274"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span><span class="sxs-lookup"><span data-stu-id="afa8f-274"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="afa8f-275"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span><span class="sxs-lookup"><span data-stu-id="afa8f-275"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="afa8f-276"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span><span class="sxs-lookup"><span data-stu-id="afa8f-276"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="afa8f-277"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**Menta** (52)</span><span class="sxs-lookup"><span data-stu-id="afa8f-277"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="afa8f-278"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span><span class="sxs-lookup"><span data-stu-id="afa8f-278"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="afa8f-279"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span><span class="sxs-lookup"><span data-stu-id="afa8f-279"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="afa8f-280"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NEXTSTEP** (55)</span><span class="sxs-lookup"><span data-stu-id="afa8f-280"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="afa8f-281"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span><span class="sxs-lookup"><span data-stu-id="afa8f-281"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd>

<span data-ttu-id="afa8f-282">Sistema operacional Palm</span><span class="sxs-lookup"><span data-stu-id="afa8f-282">Palm OS</span></span>

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="afa8f-283"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span><span class="sxs-lookup"><span data-stu-id="afa8f-283"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="afa8f-284"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span><span class="sxs-lookup"><span data-stu-id="afa8f-284"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="afa8f-285"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicado** (59)</span><span class="sxs-lookup"><span data-stu-id="afa8f-285"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="afa8f-286"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span><span class="sxs-lookup"><span data-stu-id="afa8f-286"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="afa8f-287"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span><span class="sxs-lookup"><span data-stu-id="afa8f-287"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="afa8f-288">**TargetOperatingSystemDesired**</span><span class="sxs-lookup"><span data-stu-id="afa8f-288">**TargetOperatingSystemDesired**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afa8f-289">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="afa8f-289">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="afa8f-290">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="afa8f-290">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="afa8f-291">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ softwareelement**](cim-softwareelement.md).**TargetOperatingSystem**")</span><span class="sxs-lookup"><span data-stu-id="afa8f-291">Qualifiers: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**")</span></span>
</dt> </dl>

<span data-ttu-id="afa8f-292">Sistema operacional de destino do elemento de software que está sendo verificado.</span><span class="sxs-lookup"><span data-stu-id="afa8f-292">Target operating system of the software element being checked.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="afa8f-293"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="afa8f-293"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="afa8f-294"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="afa8f-294"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="afa8f-295"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span><span class="sxs-lookup"><span data-stu-id="afa8f-295"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="afa8f-296">Mac OS</span><span class="sxs-lookup"><span data-stu-id="afa8f-296">Mac OS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="afa8f-297"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span><span class="sxs-lookup"><span data-stu-id="afa8f-297"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd>

<span data-ttu-id="afa8f-298">ATT UNIX</span><span class="sxs-lookup"><span data-stu-id="afa8f-298">ATT UNIX</span></span>

</dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="afa8f-299"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span><span class="sxs-lookup"><span data-stu-id="afa8f-299"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="afa8f-300"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span><span class="sxs-lookup"><span data-stu-id="afa8f-300"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="afa8f-301"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Unix Digital** (6)</span><span class="sxs-lookup"><span data-stu-id="afa8f-301"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="afa8f-302"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span><span class="sxs-lookup"><span data-stu-id="afa8f-302"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="afa8f-303">Abrir VMS</span><span class="sxs-lookup"><span data-stu-id="afa8f-303">Open VMS</span></span>

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="afa8f-304"><span id="HPUX"></span><span id="hpux"></span>HP **(8** )</span><span class="sxs-lookup"><span data-stu-id="afa8f-304"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd>

<span data-ttu-id="afa8f-305">HP-UX</span><span class="sxs-lookup"><span data-stu-id="afa8f-305">HP-UX</span></span>

</dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="afa8f-306"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span><span class="sxs-lookup"><span data-stu-id="afa8f-306"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="afa8f-307"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span><span class="sxs-lookup"><span data-stu-id="afa8f-307"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="afa8f-308"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span><span class="sxs-lookup"><span data-stu-id="afa8f-308"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="afa8f-309"><span id="OS_2"></span><span id="os_2"></span>**Sistema operacional/2** (12)</span><span class="sxs-lookup"><span data-stu-id="afa8f-309"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="afa8f-310"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span><span class="sxs-lookup"><span data-stu-id="afa8f-310"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd>

<span data-ttu-id="afa8f-311">VM (máquina virtual) da Microsoft para Java</span><span class="sxs-lookup"><span data-stu-id="afa8f-311">Microsoft Virtual Machine (VM) for Java</span></span>

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="afa8f-312"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span><span class="sxs-lookup"><span data-stu-id="afa8f-312"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="afa8f-313"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span><span class="sxs-lookup"><span data-stu-id="afa8f-313"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd>

<span data-ttu-id="afa8f-314">Windows 3. x</span><span class="sxs-lookup"><span data-stu-id="afa8f-314">Windows 3.x</span></span>

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="afa8f-315"><span id="WIN95"></span><span id="win95"></span>**Win95** (16)</span><span class="sxs-lookup"><span data-stu-id="afa8f-315"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd>

<span data-ttu-id="afa8f-316">Windows 95</span><span class="sxs-lookup"><span data-stu-id="afa8f-316">Windows 95</span></span>

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="afa8f-317"><span id="WIN98"></span><span id="win98"></span>**Win98** (17)</span><span class="sxs-lookup"><span data-stu-id="afa8f-317"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd>

<span data-ttu-id="afa8f-318">Windows 98</span><span class="sxs-lookup"><span data-stu-id="afa8f-318">Windows 98</span></span>

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="afa8f-319"><span id="WINNT"></span><span id="winnt"></span>**WinNT** (18)</span><span class="sxs-lookup"><span data-stu-id="afa8f-319"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd>

<span data-ttu-id="afa8f-320">Windows NT</span><span class="sxs-lookup"><span data-stu-id="afa8f-320">Windows NT</span></span>

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="afa8f-321"><span id="WINCE"></span><span id="wince"></span>**WinCE** (19)</span><span class="sxs-lookup"><span data-stu-id="afa8f-321"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd>

<span data-ttu-id="afa8f-322">Windows CE</span><span class="sxs-lookup"><span data-stu-id="afa8f-322">Windows CE</span></span>

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="afa8f-323"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span><span class="sxs-lookup"><span data-stu-id="afa8f-323"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd>

<span data-ttu-id="afa8f-324">NCR 3000</span><span class="sxs-lookup"><span data-stu-id="afa8f-324">NCR 3000</span></span>

</dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="afa8f-325"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span><span class="sxs-lookup"><span data-stu-id="afa8f-325"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="afa8f-326"><span id="OSF"></span><span id="osf"></span>**Uso** (22)</span><span class="sxs-lookup"><span data-stu-id="afa8f-326"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="afa8f-327"><span id="DC_OS"></span><span id="dc_os"></span>**DC/os** (23)</span><span class="sxs-lookup"><span data-stu-id="afa8f-327"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="afa8f-328"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Unix dependente** (24)</span><span class="sxs-lookup"><span data-stu-id="afa8f-328"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="afa8f-329"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span><span class="sxs-lookup"><span data-stu-id="afa8f-329"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="afa8f-330"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span><span class="sxs-lookup"><span data-stu-id="afa8f-330"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="afa8f-331"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Subsequentes** (27)</span><span class="sxs-lookup"><span data-stu-id="afa8f-331"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="afa8f-332"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span><span class="sxs-lookup"><span data-stu-id="afa8f-332"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="afa8f-333"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span><span class="sxs-lookup"><span data-stu-id="afa8f-333"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="afa8f-334"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span><span class="sxs-lookup"><span data-stu-id="afa8f-334"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="afa8f-335"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span><span class="sxs-lookup"><span data-stu-id="afa8f-335"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="afa8f-336"><span id="ASERIES"></span><span id="aseries"></span>**ASeries** (32)</span><span class="sxs-lookup"><span data-stu-id="afa8f-336"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd>

<span data-ttu-id="afa8f-337">Uma série</span><span class="sxs-lookup"><span data-stu-id="afa8f-337">A Series</span></span>

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="afa8f-338"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span><span class="sxs-lookup"><span data-stu-id="afa8f-338"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd>

<span data-ttu-id="afa8f-339">NSK tandem</span><span class="sxs-lookup"><span data-stu-id="afa8f-339">Tandem NSK</span></span>

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="afa8f-340"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span><span class="sxs-lookup"><span data-stu-id="afa8f-340"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd>

<span data-ttu-id="afa8f-341">NT em tandem</span><span class="sxs-lookup"><span data-stu-id="afa8f-341">Tandem NT</span></span>

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="afa8f-342"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span><span class="sxs-lookup"><span data-stu-id="afa8f-342"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd>

<span data-ttu-id="afa8f-343">BS2000/OSD</span><span class="sxs-lookup"><span data-stu-id="afa8f-343">BS2000/OSD</span></span>

</dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="afa8f-344"><span id="LINUX"></span><span id="linux"></span>**Linux** (36)</span><span class="sxs-lookup"><span data-stu-id="afa8f-344"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="afa8f-345"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span><span class="sxs-lookup"><span data-stu-id="afa8f-345"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="afa8f-346"><span id="XENIX"></span><span id="xenix"></span>**Xenix** (38)</span><span class="sxs-lookup"><span data-stu-id="afa8f-346"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="afa8f-347"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span><span class="sxs-lookup"><span data-stu-id="afa8f-347"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="afa8f-348"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Unix interativo** (40)</span><span class="sxs-lookup"><span data-stu-id="afa8f-348"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="afa8f-349"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span><span class="sxs-lookup"><span data-stu-id="afa8f-349"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd>

<span data-ttu-id="afa8f-350">BSD UNIX</span><span class="sxs-lookup"><span data-stu-id="afa8f-350">BSD UNIX</span></span>

</dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="afa8f-351"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span><span class="sxs-lookup"><span data-stu-id="afa8f-351"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="afa8f-352"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span><span class="sxs-lookup"><span data-stu-id="afa8f-352"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="afa8f-353"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span><span class="sxs-lookup"><span data-stu-id="afa8f-353"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="afa8f-354"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span><span class="sxs-lookup"><span data-stu-id="afa8f-354"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd>

<span data-ttu-id="afa8f-355">Mac OS 9</span><span class="sxs-lookup"><span data-stu-id="afa8f-355">Mac OS 9</span></span>

</dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="afa8f-356"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**Kernel Mach** (46)</span><span class="sxs-lookup"><span data-stu-id="afa8f-356"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="afa8f-357"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span><span class="sxs-lookup"><span data-stu-id="afa8f-357"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="afa8f-358"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span><span class="sxs-lookup"><span data-stu-id="afa8f-358"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="afa8f-359"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span><span class="sxs-lookup"><span data-stu-id="afa8f-359"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="afa8f-360"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span><span class="sxs-lookup"><span data-stu-id="afa8f-360"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="afa8f-361"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span><span class="sxs-lookup"><span data-stu-id="afa8f-361"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="afa8f-362"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**Menta** (52)</span><span class="sxs-lookup"><span data-stu-id="afa8f-362"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="afa8f-363"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span><span class="sxs-lookup"><span data-stu-id="afa8f-363"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="afa8f-364"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span><span class="sxs-lookup"><span data-stu-id="afa8f-364"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="afa8f-365"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NEXTSTEP** (55)</span><span class="sxs-lookup"><span data-stu-id="afa8f-365"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="afa8f-366"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span><span class="sxs-lookup"><span data-stu-id="afa8f-366"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd>

<span data-ttu-id="afa8f-367">Sistema operacional Palm</span><span class="sxs-lookup"><span data-stu-id="afa8f-367">Palm OS</span></span>

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="afa8f-368"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span><span class="sxs-lookup"><span data-stu-id="afa8f-368"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="afa8f-369"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span><span class="sxs-lookup"><span data-stu-id="afa8f-369"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="afa8f-370"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicado** (59)</span><span class="sxs-lookup"><span data-stu-id="afa8f-370"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="afa8f-371"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span><span class="sxs-lookup"><span data-stu-id="afa8f-371"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="afa8f-372"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span><span class="sxs-lookup"><span data-stu-id="afa8f-372"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="afa8f-373">**UpperSoftwareElementVersion**</span><span class="sxs-lookup"><span data-stu-id="afa8f-373">**UpperSoftwareElementVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afa8f-374">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="afa8f-374">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="afa8f-375">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="afa8f-375">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="afa8f-376">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ softwareelement**](cim-softwareelement.md).**Version**")</span><span class="sxs-lookup"><span data-stu-id="afa8f-376">Qualifiers: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Version**")</span></span>
</dt> </dl>

<span data-ttu-id="afa8f-377">Versão máxima de um elemento de software que está sendo verificado.</span><span class="sxs-lookup"><span data-stu-id="afa8f-377">Maximum version of a software element being checked.</span></span>

</dd> <dt>

<span data-ttu-id="afa8f-378">**Versão**</span><span class="sxs-lookup"><span data-stu-id="afa8f-378">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afa8f-379">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="afa8f-379">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="afa8f-380">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="afa8f-380">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="afa8f-381">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ softwareelement**](cim-softwareelement.md).**Version**"), [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Componente DMTF \| 1,3 ")</span><span class="sxs-lookup"><span data-stu-id="afa8f-381">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Version**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="afa8f-382">Versão da operação.</span><span class="sxs-lookup"><span data-stu-id="afa8f-382">Version of the operation.</span></span>

<span data-ttu-id="afa8f-383">A versão da operação deve estar em um dos seguintes formatos:</span><span class="sxs-lookup"><span data-stu-id="afa8f-383">The version of the operation should be in one of the following forms:</span></span>

-   <span data-ttu-id="afa8f-384"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="afa8f-384"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="afa8f-385"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="afa8f-385"><major>.<minor><letter><revision></span></span>

<span data-ttu-id="afa8f-386">Essa propriedade é herdada da classe de [**\_ verificação CIM**](cim-check.md) .</span><span class="sxs-lookup"><span data-stu-id="afa8f-386">This property is inherited from the [**CIM\_Check**](cim-check.md) class.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="afa8f-387">Comentários</span><span class="sxs-lookup"><span data-stu-id="afa8f-387">Remarks</span></span>

<span data-ttu-id="afa8f-388">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="afa8f-388">WMI does not implement this class.</span></span>

<span data-ttu-id="afa8f-389">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="afa8f-389">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="afa8f-390">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="afa8f-390">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="afa8f-391">Requisitos</span><span class="sxs-lookup"><span data-stu-id="afa8f-391">Requirements</span></span>



| <span data-ttu-id="afa8f-392">Requisito</span><span class="sxs-lookup"><span data-stu-id="afa8f-392">Requirement</span></span> | <span data-ttu-id="afa8f-393">Valor</span><span class="sxs-lookup"><span data-stu-id="afa8f-393">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="afa8f-394">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="afa8f-394">Minimum supported client</span></span><br/> | <span data-ttu-id="afa8f-395">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="afa8f-395">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="afa8f-396">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="afa8f-396">Minimum supported server</span></span><br/> | <span data-ttu-id="afa8f-397">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="afa8f-397">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="afa8f-398">Namespace</span><span class="sxs-lookup"><span data-stu-id="afa8f-398">Namespace</span></span><br/>                | <span data-ttu-id="afa8f-399">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="afa8f-399">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="afa8f-400">MOF</span><span class="sxs-lookup"><span data-stu-id="afa8f-400">MOF</span></span><br/>                      | <dl> <span data-ttu-id="afa8f-401"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="afa8f-401"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="afa8f-402">DLL</span><span class="sxs-lookup"><span data-stu-id="afa8f-402">DLL</span></span><br/>                      | <dl> <span data-ttu-id="afa8f-403"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="afa8f-403"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="afa8f-404">Confira também</span><span class="sxs-lookup"><span data-stu-id="afa8f-404">See also</span></span>

<dl> <dt>

[<span data-ttu-id="afa8f-405">**Verificação de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="afa8f-405">**CIM\_Check**</span></span>](cim-check.md)
</dt> </dl>

 

