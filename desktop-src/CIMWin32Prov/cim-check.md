---
description: A \_ classe de verificação CIM representa uma condição ou característica que deve ser verdadeira em um ambiente definido ou com escopo por uma instância de uma classe de \_ sistema CIM.
ms.assetid: f7862fe5-4412-4d57-b5fa-03c939ddba02
ms.tgt_platform: multiple
title: Classe CIM_Check
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Check
- CIM_Check.CheckID
- CIM_Check.Caption
- CIM_Check.Description
- CIM_Check.CheckMode
- CIM_Check.Name
- CIM_Check.TargetOperatingSystem
- CIM_Check.Version
- CIM_Check.SoftwareElementID
- CIM_Check.SoftwareElementState
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3cbe742fb4cd2510ec4c502f89b3b3b1eb79bc47
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826504"
---
# <a name="cim_check-class"></a><span data-ttu-id="9be02-103">\_Classe de verificação CIM</span><span class="sxs-lookup"><span data-stu-id="9be02-103">CIM\_Check class</span></span>

<span data-ttu-id="9be02-104">A classe de **\_ verificação CIM** representa uma condição ou característica que deve ser verdadeira em um ambiente definido ou com escopo por uma instância de uma classe [**de \_ sistema CIM**](cim-computersystem.md) .</span><span class="sxs-lookup"><span data-stu-id="9be02-104">The **CIM\_Check** class represents a condition or characteristic that is expected to be true in an environment defined or scoped by an instance of a [**CIM\_ComputerSystem**](cim-computersystem.md) class.</span></span> <span data-ttu-id="9be02-105">As verificações associadas a um determinado elemento de software são organizadas em um dos dois grupos usando a propriedade **Phase** da Associação [**\_ SoftwareElementChecks do CIM**](cim-softwareelementchecks.md) .</span><span class="sxs-lookup"><span data-stu-id="9be02-105">The checks associated with a particular software element are organized into one of two groups using the **Phase** property of the [**CIM\_SoftwareElementChecks**](cim-softwareelementchecks.md) association.</span></span>

<span data-ttu-id="9be02-106">As condições que devem ser satisfeitas quando um elemento de software está em um ambiente específico são conhecidas como condições em estado.</span><span class="sxs-lookup"><span data-stu-id="9be02-106">Conditions that are expected to be satisfied when a software element is in a particular environment are known as in-state conditions.</span></span> <span data-ttu-id="9be02-107">As condições que devem ser satisfeitas para fazer a transição do elemento de software atual para seu próximo estado são conhecidas como condições do próximo estado.</span><span class="sxs-lookup"><span data-stu-id="9be02-107">Conditions that must be satisfied to transition the current software element to its next state are known as next-state conditions.</span></span>

<span data-ttu-id="9be02-108">Um objeto de [**\_ sistema CIM**](cim-computersystem.md) representa o ambiente em que [**um \_ software CIM**](cim-softwareelement.md) já está instalado ou no qual um **\_ software. CIM** será instalado.</span><span class="sxs-lookup"><span data-stu-id="9be02-108">A [**CIM\_ComputerSystem**](cim-computersystem.md) object represents the environment in which a [**CIM\_SoftwareElement**](cim-softwareelement.md) is already installed, or in which a **CIM\_SoftwareElement** will be installed.</span></span> <span data-ttu-id="9be02-109">Para o caso em que um elemento de software já está instalado, a associação [**CIM \_ InstalledSoftwareElement**](cim-installedsoftwareelement.md) é usada para identificar o objeto de **sistema de \_ ComputerSystem CIM** que representa o "ambiente".</span><span class="sxs-lookup"><span data-stu-id="9be02-109">For the case in which a software element is already installed, the [**CIM\_InstalledSoftwareElement**](cim-installedsoftwareelement.md) association is used to identify the **CIM\_ComputerSystem** object that represents the "environment."</span></span> <span data-ttu-id="9be02-110">Quando um elemento de software está sendo distribuído e instalado em um computador diferente, o objeto de sistema de computador **CIM \_** para o System de destino é o ambiente.</span><span class="sxs-lookup"><span data-stu-id="9be02-110">When a software element is being distributed and installed on a different computer, the **CIM\_ComputerSystem** object for the targeted system is the environment.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9be02-111">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="9be02-111">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="9be02-112">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="9be02-112">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="9be02-113">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="9be02-113">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="9be02-114">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="9be02-114">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="9be02-115">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9be02-115">Syntax</span></span>

``` syntax
[UUID("{7A9135CA-DB21-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_Check
{
  string  CheckID;
  string  Caption;
  string  Description;
  boolean CheckMode;
  string  Name;
  uint16  TargetOperatingSystem;
  string  Version;
  string  SoftwareElementID;
  uint16  SoftwareElementState;
};
```

## <a name="members"></a><span data-ttu-id="9be02-116">Membros</span><span class="sxs-lookup"><span data-stu-id="9be02-116">Members</span></span>

<span data-ttu-id="9be02-117">A classe de **\_ verificação CIM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="9be02-117">The **CIM\_Check** class has these types of members:</span></span>

-   [<span data-ttu-id="9be02-118">Métodos</span><span class="sxs-lookup"><span data-stu-id="9be02-118">Methods</span></span>](#methods)
-   [<span data-ttu-id="9be02-119">Propriedades</span><span class="sxs-lookup"><span data-stu-id="9be02-119">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="9be02-120">Métodos</span><span class="sxs-lookup"><span data-stu-id="9be02-120">Methods</span></span>

<span data-ttu-id="9be02-121">A classe de **\_ verificação CIM** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="9be02-121">The **CIM\_Check** class has these methods.</span></span>



| <span data-ttu-id="9be02-122">Método</span><span class="sxs-lookup"><span data-stu-id="9be02-122">Method</span></span>                                             | <span data-ttu-id="9be02-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="9be02-123">Description</span></span>                                                   |
|:---------------------------------------------------|:--------------------------------------------------------------|
| [<span data-ttu-id="9be02-124">**Chame**</span><span class="sxs-lookup"><span data-stu-id="9be02-124">**Invoke**</span></span>](invoke-method-in-class-cim-check.md) | <span data-ttu-id="9be02-125">Executa uma ação específica.</span><span class="sxs-lookup"><span data-stu-id="9be02-125">Takes a particular action.</span></span> <span data-ttu-id="9be02-126">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="9be02-126">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="9be02-127">Propriedades</span><span class="sxs-lookup"><span data-stu-id="9be02-127">Properties</span></span>

<span data-ttu-id="9be02-128">A classe de **\_ verificação CIM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="9be02-128">The **CIM\_Check** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9be02-129">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="9be02-129">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be02-130">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9be02-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9be02-131">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9be02-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9be02-132">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="9be02-132">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="9be02-133">Uma breve descrição textual do assunto.</span><span class="sxs-lookup"><span data-stu-id="9be02-133">A short textual description of the subject.</span></span>

</dd> <dt>

<span data-ttu-id="9be02-134">**CheckID**</span><span class="sxs-lookup"><span data-stu-id="9be02-134">**CheckID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be02-135">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9be02-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9be02-136">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9be02-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9be02-137">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="9be02-137">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="9be02-138">Identificador usado em conjunto com outras chaves para identificar exclusivamente a verificação.</span><span class="sxs-lookup"><span data-stu-id="9be02-138">Identifier used in conjunction with other keys to uniquely identify the check.</span></span>

</dd> <dt>

<span data-ttu-id="9be02-139">**CheckMode**</span><span class="sxs-lookup"><span data-stu-id="9be02-139">**CheckMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be02-140">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="9be02-140">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9be02-141">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9be02-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9be02-142">Se for **true**, espera-se que a condição exista no ambiente.</span><span class="sxs-lookup"><span data-stu-id="9be02-142">If **TRUE**, the condition is expected to exist in the environment.</span></span> <span data-ttu-id="9be02-143">Por exemplo, espera-se que um arquivo esteja em um sistema, portanto, o método [**Invoke**](invoke-method-in-class-cim-check.md) deve retornar **true**.</span><span class="sxs-lookup"><span data-stu-id="9be02-143">For example, a file is expected to be on a system, so the [**Invoke**](invoke-method-in-class-cim-check.md) method should return **TRUE**.</span></span>

<span data-ttu-id="9be02-144">Se for **false**, a condição não deverá existir.</span><span class="sxs-lookup"><span data-stu-id="9be02-144">If **FALSE**, the condition is not expected to exist.</span></span> <span data-ttu-id="9be02-145">Por exemplo, um arquivo não está em um sistema, portanto, o método [**Invoke**](invoke-method-in-class-cim-check.md) deve retornar **false**.</span><span class="sxs-lookup"><span data-stu-id="9be02-145">For example, a file is not on a system, so the [**Invoke**](invoke-method-in-class-cim-check.md) method should return **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="9be02-146">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="9be02-146">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be02-147">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9be02-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9be02-148">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9be02-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9be02-149">Uma descrição dos objetos.</span><span class="sxs-lookup"><span data-stu-id="9be02-149">A description of the objects.</span></span>

</dd> <dt>

<span data-ttu-id="9be02-150">**Nome**</span><span class="sxs-lookup"><span data-stu-id="9be02-150">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be02-151">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9be02-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9be02-152">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9be02-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9be02-153">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ softwareelement**](cim-softwareelement.md).**Name**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="9be02-153">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Name**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="9be02-154">Nome usado para identificar o elemento de software.</span><span class="sxs-lookup"><span data-stu-id="9be02-154">Name used to identify the software element.</span></span>

</dd> <dt>

<span data-ttu-id="9be02-155">**SoftwareElementID**</span><span class="sxs-lookup"><span data-stu-id="9be02-155">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be02-156">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9be02-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9be02-157">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9be02-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9be02-158">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ softwareelement**](cim-softwareelement.md).**SoftwareElementID**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="9be02-158">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="9be02-159">Este é um identificador para este elemento de software.</span><span class="sxs-lookup"><span data-stu-id="9be02-159">This is an identifier for this software element.</span></span>

</dd> <dt>

<span data-ttu-id="9be02-160">**SoftwareElementState**</span><span class="sxs-lookup"><span data-stu-id="9be02-160">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be02-161">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9be02-161">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9be02-162">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9be02-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9be02-163">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ softwareelement**](cim-softwareelement.md).**SoftwareElementState**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="9be02-163">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="9be02-164">O estado do elemento de software de um elemento de software.</span><span class="sxs-lookup"><span data-stu-id="9be02-164">The software element state of a software element.</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="9be02-165"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Implantável** (0)</span><span class="sxs-lookup"><span data-stu-id="9be02-165"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Deployable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="9be02-166">Descreve os detalhes necessários para a distribuição bem-sucedida e os detalhes (condições e ações) necessários para criar um elemento de software no estado instalável (ou seja, o próximo estado).</span><span class="sxs-lookup"><span data-stu-id="9be02-166">Describes the details necessary for successful distribution and the details (conditions and actions) required to create a software element in the installable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="9be02-167"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Instalável** (1)</span><span class="sxs-lookup"><span data-stu-id="9be02-167"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="9be02-168">Descreve os detalhes necessários para a instalação bem-sucedida e os detalhes (condições e ações) necessários para criar um elemento de software no estado executável (ou seja, o próximo estado).</span><span class="sxs-lookup"><span data-stu-id="9be02-168">Describes the details necessary for successful installation and the details (conditions and actions) required to create a software element in the executable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="9be02-169"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executável** (2)</span><span class="sxs-lookup"><span data-stu-id="9be02-169"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="9be02-170">Descreve os detalhes necessários para a execução bem-sucedida e os detalhes (condições e ações) necessários para criar um elemento de software no estado em execução (ou seja, o próximo estado).</span><span class="sxs-lookup"><span data-stu-id="9be02-170">Describes the details necessary for successful execution and the details (conditions and actions) required to create a software element in the running state (that is, the next state).</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="9be02-171"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Em execução** (3)</span><span class="sxs-lookup"><span data-stu-id="9be02-171"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd>

<span data-ttu-id="9be02-172">Descreve os detalhes necessários para monitorar e operar em um elemento inicial.</span><span class="sxs-lookup"><span data-stu-id="9be02-172">Describes the details necessary to monitor and operate on a start element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="9be02-173">**TargetOperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="9be02-173">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be02-174">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9be02-174">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9be02-175">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9be02-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9be02-176">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ softwareelement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Informações do componente de software DMTF \| 2,5 ")</span><span class="sxs-lookup"><span data-stu-id="9be02-176">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.5")</span></span>
</dt> </dl>

<span data-ttu-id="9be02-177">Sistema operacional de destino do elemento de software.</span><span class="sxs-lookup"><span data-stu-id="9be02-177">Target operating system of the software element.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9be02-178"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="9be02-178"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="9be02-179"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="9be02-179"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="9be02-180"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span><span class="sxs-lookup"><span data-stu-id="9be02-180"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="9be02-181">Mac OS</span><span class="sxs-lookup"><span data-stu-id="9be02-181">Mac OS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="9be02-182"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span><span class="sxs-lookup"><span data-stu-id="9be02-182"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd>

<span data-ttu-id="9be02-183">ATT UNIX</span><span class="sxs-lookup"><span data-stu-id="9be02-183">ATT UNIX</span></span>

</dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="9be02-184"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span><span class="sxs-lookup"><span data-stu-id="9be02-184"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="9be02-185"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span><span class="sxs-lookup"><span data-stu-id="9be02-185"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="9be02-186"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Unix Digital** (6)</span><span class="sxs-lookup"><span data-stu-id="9be02-186"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="9be02-187"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span><span class="sxs-lookup"><span data-stu-id="9be02-187"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="9be02-188">Abrir VMS</span><span class="sxs-lookup"><span data-stu-id="9be02-188">Open VMS</span></span>

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="9be02-189"><span id="HPUX"></span><span id="hpux"></span>HP **(8** )</span><span class="sxs-lookup"><span data-stu-id="9be02-189"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd>

<span data-ttu-id="9be02-190">HP-UX</span><span class="sxs-lookup"><span data-stu-id="9be02-190">HP-UX</span></span>

</dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="9be02-191"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span><span class="sxs-lookup"><span data-stu-id="9be02-191"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="9be02-192"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span><span class="sxs-lookup"><span data-stu-id="9be02-192"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="9be02-193"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span><span class="sxs-lookup"><span data-stu-id="9be02-193"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="9be02-194"><span id="OS_2"></span><span id="os_2"></span>**Sistema operacional/2** (12)</span><span class="sxs-lookup"><span data-stu-id="9be02-194"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="9be02-195"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span><span class="sxs-lookup"><span data-stu-id="9be02-195"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd>

<span data-ttu-id="9be02-196">VM (máquina virtual) da Microsoft para Java</span><span class="sxs-lookup"><span data-stu-id="9be02-196">Microsoft Virtual Machine (VM) for Java</span></span>

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="9be02-197"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span><span class="sxs-lookup"><span data-stu-id="9be02-197"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="9be02-198"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span><span class="sxs-lookup"><span data-stu-id="9be02-198"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd>

<span data-ttu-id="9be02-199">Windows 3. x</span><span class="sxs-lookup"><span data-stu-id="9be02-199">Windows 3.x</span></span>

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="9be02-200"><span id="WIN95"></span><span id="win95"></span>**Win95** (16)</span><span class="sxs-lookup"><span data-stu-id="9be02-200"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd>

<span data-ttu-id="9be02-201">Windows 95</span><span class="sxs-lookup"><span data-stu-id="9be02-201">Windows 95</span></span>

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="9be02-202"><span id="WIN98"></span><span id="win98"></span>**Win98** (17)</span><span class="sxs-lookup"><span data-stu-id="9be02-202"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd>

<span data-ttu-id="9be02-203">Windows 98</span><span class="sxs-lookup"><span data-stu-id="9be02-203">Windows 98</span></span>

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="9be02-204"><span id="WINNT"></span><span id="winnt"></span>**WinNT** (18)</span><span class="sxs-lookup"><span data-stu-id="9be02-204"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd>

<span data-ttu-id="9be02-205">Windows NT</span><span class="sxs-lookup"><span data-stu-id="9be02-205">Windows NT</span></span>

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="9be02-206"><span id="WINCE"></span><span id="wince"></span>**WinCE** (19)</span><span class="sxs-lookup"><span data-stu-id="9be02-206"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd>

<span data-ttu-id="9be02-207">Windows CE</span><span class="sxs-lookup"><span data-stu-id="9be02-207">Windows CE</span></span>

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="9be02-208"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span><span class="sxs-lookup"><span data-stu-id="9be02-208"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd>

<span data-ttu-id="9be02-209">NCR 3000</span><span class="sxs-lookup"><span data-stu-id="9be02-209">NCR 3000</span></span>

</dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="9be02-210"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span><span class="sxs-lookup"><span data-stu-id="9be02-210"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="9be02-211"><span id="OSF"></span><span id="osf"></span>**Uso** (22)</span><span class="sxs-lookup"><span data-stu-id="9be02-211"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="9be02-212"><span id="DC_OS"></span><span id="dc_os"></span>**DC/os** (23)</span><span class="sxs-lookup"><span data-stu-id="9be02-212"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="9be02-213"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Unix dependente** (24)</span><span class="sxs-lookup"><span data-stu-id="9be02-213"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="9be02-214"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span><span class="sxs-lookup"><span data-stu-id="9be02-214"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="9be02-215"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span><span class="sxs-lookup"><span data-stu-id="9be02-215"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="9be02-216"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Subsequentes** (27)</span><span class="sxs-lookup"><span data-stu-id="9be02-216"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="9be02-217"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span><span class="sxs-lookup"><span data-stu-id="9be02-217"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="9be02-218"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span><span class="sxs-lookup"><span data-stu-id="9be02-218"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="9be02-219"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span><span class="sxs-lookup"><span data-stu-id="9be02-219"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="9be02-220"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span><span class="sxs-lookup"><span data-stu-id="9be02-220"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="9be02-221"><span id="ASERIES"></span><span id="aseries"></span>**ASeries** (32)</span><span class="sxs-lookup"><span data-stu-id="9be02-221"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd>

<span data-ttu-id="9be02-222">Uma série</span><span class="sxs-lookup"><span data-stu-id="9be02-222">A Series</span></span>

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="9be02-223"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span><span class="sxs-lookup"><span data-stu-id="9be02-223"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd>

<span data-ttu-id="9be02-224">NSK tandem</span><span class="sxs-lookup"><span data-stu-id="9be02-224">Tandem NSK</span></span>

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="9be02-225"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span><span class="sxs-lookup"><span data-stu-id="9be02-225"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd>

<span data-ttu-id="9be02-226">NT em tandem</span><span class="sxs-lookup"><span data-stu-id="9be02-226">Tandem NT</span></span>

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="9be02-227"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span><span class="sxs-lookup"><span data-stu-id="9be02-227"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd>

<span data-ttu-id="9be02-228">BS2000/OSD</span><span class="sxs-lookup"><span data-stu-id="9be02-228">BS2000/OSD</span></span>

</dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="9be02-229"><span id="LINUX"></span><span id="linux"></span>**Linux** (36)</span><span class="sxs-lookup"><span data-stu-id="9be02-229"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="9be02-230"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span><span class="sxs-lookup"><span data-stu-id="9be02-230"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="9be02-231"><span id="XENIX"></span><span id="xenix"></span>**Xenix** (38)</span><span class="sxs-lookup"><span data-stu-id="9be02-231"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="9be02-232"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span><span class="sxs-lookup"><span data-stu-id="9be02-232"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="9be02-233"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Unix interativo** (40)</span><span class="sxs-lookup"><span data-stu-id="9be02-233"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="9be02-234"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span><span class="sxs-lookup"><span data-stu-id="9be02-234"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd>

<span data-ttu-id="9be02-235">BSD UNIX</span><span class="sxs-lookup"><span data-stu-id="9be02-235">BSD UNIX</span></span>

</dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="9be02-236"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span><span class="sxs-lookup"><span data-stu-id="9be02-236"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="9be02-237"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span><span class="sxs-lookup"><span data-stu-id="9be02-237"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="9be02-238"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span><span class="sxs-lookup"><span data-stu-id="9be02-238"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="9be02-239"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span><span class="sxs-lookup"><span data-stu-id="9be02-239"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd>

<span data-ttu-id="9be02-240">Mac OS 9</span><span class="sxs-lookup"><span data-stu-id="9be02-240">Mac OS 9</span></span>

</dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="9be02-241"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**Kernel Mach** (46)</span><span class="sxs-lookup"><span data-stu-id="9be02-241"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="9be02-242"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span><span class="sxs-lookup"><span data-stu-id="9be02-242"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="9be02-243"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span><span class="sxs-lookup"><span data-stu-id="9be02-243"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="9be02-244"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span><span class="sxs-lookup"><span data-stu-id="9be02-244"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="9be02-245"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span><span class="sxs-lookup"><span data-stu-id="9be02-245"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="9be02-246"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span><span class="sxs-lookup"><span data-stu-id="9be02-246"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="9be02-247"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**Menta** (52)</span><span class="sxs-lookup"><span data-stu-id="9be02-247"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="9be02-248"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span><span class="sxs-lookup"><span data-stu-id="9be02-248"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="9be02-249"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span><span class="sxs-lookup"><span data-stu-id="9be02-249"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="9be02-250"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NEXTSTEP** (55)</span><span class="sxs-lookup"><span data-stu-id="9be02-250"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="9be02-251"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span><span class="sxs-lookup"><span data-stu-id="9be02-251"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd>

<span data-ttu-id="9be02-252">Sistema operacional Palm</span><span class="sxs-lookup"><span data-stu-id="9be02-252">Palm OS</span></span>

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="9be02-253"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span><span class="sxs-lookup"><span data-stu-id="9be02-253"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="9be02-254"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span><span class="sxs-lookup"><span data-stu-id="9be02-254"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="9be02-255"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicado** (59)</span><span class="sxs-lookup"><span data-stu-id="9be02-255"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="9be02-256"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span><span class="sxs-lookup"><span data-stu-id="9be02-256"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="9be02-257"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span><span class="sxs-lookup"><span data-stu-id="9be02-257"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9be02-258">**Versão**</span><span class="sxs-lookup"><span data-stu-id="9be02-258">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be02-259">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9be02-259">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9be02-260">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9be02-260">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9be02-261">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ softwareelement**](cim-softwareelement.md).**Version**"), [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Componente DMTF \| 1,3 ")</span><span class="sxs-lookup"><span data-stu-id="9be02-261">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Version**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="9be02-262">Versão da operação.</span><span class="sxs-lookup"><span data-stu-id="9be02-262">Version of the operation.</span></span>

<span data-ttu-id="9be02-263">A versão da operação deve estar em um dos seguintes formatos:</span><span class="sxs-lookup"><span data-stu-id="9be02-263">The version of the operation should be in one of the following forms:</span></span>

-   <span data-ttu-id="9be02-264"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="9be02-264"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="9be02-265"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="9be02-265"><major>.<minor><letter><revision></span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9be02-266">Comentários</span><span class="sxs-lookup"><span data-stu-id="9be02-266">Remarks</span></span>

<span data-ttu-id="9be02-267">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="9be02-267">WMI does not implement this class.</span></span> <span data-ttu-id="9be02-268">Para obter mais informações sobre classes derivadas **da \_ verificação de CIM**, consulte [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="9be02-268">For more information about classes derived from **CIM\_Check**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="9be02-269">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="9be02-269">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="9be02-270">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="9be02-270">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="9be02-271">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9be02-271">Requirements</span></span>



| <span data-ttu-id="9be02-272">Requisito</span><span class="sxs-lookup"><span data-stu-id="9be02-272">Requirement</span></span> | <span data-ttu-id="9be02-273">Valor</span><span class="sxs-lookup"><span data-stu-id="9be02-273">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9be02-274">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9be02-274">Minimum supported client</span></span><br/> | <span data-ttu-id="9be02-275">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9be02-275">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9be02-276">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9be02-276">Minimum supported server</span></span><br/> | <span data-ttu-id="9be02-277">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9be02-277">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9be02-278">Namespace</span><span class="sxs-lookup"><span data-stu-id="9be02-278">Namespace</span></span><br/>                | <span data-ttu-id="9be02-279">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="9be02-279">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9be02-280">MOF</span><span class="sxs-lookup"><span data-stu-id="9be02-280">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9be02-281"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9be02-281"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9be02-282">DLL</span><span class="sxs-lookup"><span data-stu-id="9be02-282">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9be02-283"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9be02-283"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

