---
description: Uma \_ classe de ação CIM é uma operação que faz parte de um processo para criar um elemento de software em seu estado seguinte ou para eliminar o elemento de software no estado atual.
ms.assetid: d1f72aaf-7e26-414f-99e7-ff8f14d66360
ms.tgt_platform: multiple
title: Classe CIM_Action
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Action
- CIM_Action.ActionID
- CIM_Action.Caption
- CIM_Action.Description
- CIM_Action.Direction
- CIM_Action.Name
- CIM_Action.SoftwareElementID
- CIM_Action.SoftwareElementState
- CIM_Action.TargetOperatingSystem
- CIM_Action.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a5f37fa4b62c1e8b678533de4abaa7f6a172904e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089118"
---
# <a name="cim_action-class"></a><span data-ttu-id="7633c-103">\_Classe de ação CIM</span><span class="sxs-lookup"><span data-stu-id="7633c-103">CIM\_Action class</span></span>

<span data-ttu-id="7633c-104">Uma classe de **\_ ação CIM** é uma operação que faz parte de um processo para criar um elemento de software em seu estado seguinte ou para eliminar o elemento de software no estado atual.</span><span class="sxs-lookup"><span data-stu-id="7633c-104">A **CIM\_Action** class is an operation that is part of a process to either create a software element in its next state or to eliminate the software element in the current state.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7633c-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="7633c-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="7633c-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="7633c-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="7633c-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="7633c-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="7633c-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="7633c-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="7633c-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7633c-109">Syntax</span></span>

``` syntax
[UUID("{2F156260-DB21-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_Action
{
  string ActionID;
  string Caption;
  string Description;
  uint16 Direction;
  string Name;
  string SoftwareElementID;
  uint16 SoftwareElementState;
  uint16 TargetOperatingSystem;
  string Version;
};
```

## <a name="members"></a><span data-ttu-id="7633c-110">Membros</span><span class="sxs-lookup"><span data-stu-id="7633c-110">Members</span></span>

<span data-ttu-id="7633c-111">A classe de **\_ ação CIM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="7633c-111">The **CIM\_Action** class has these types of members:</span></span>

-   [<span data-ttu-id="7633c-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="7633c-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="7633c-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="7633c-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="7633c-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="7633c-114">Methods</span></span>

<span data-ttu-id="7633c-115">A classe de **\_ ação CIM** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="7633c-115">The **CIM\_Action** class has these methods.</span></span>



| <span data-ttu-id="7633c-116">Método</span><span class="sxs-lookup"><span data-stu-id="7633c-116">Method</span></span>                                              | <span data-ttu-id="7633c-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="7633c-117">Description</span></span>                                                   |
|:----------------------------------------------------|:--------------------------------------------------------------|
| [<span data-ttu-id="7633c-118">**Chame**</span><span class="sxs-lookup"><span data-stu-id="7633c-118">**Invoke**</span></span>](invoke-method-in-class-cim-action.md) | <span data-ttu-id="7633c-119">Executa uma ação específica.</span><span class="sxs-lookup"><span data-stu-id="7633c-119">Takes a particular action.</span></span> <span data-ttu-id="7633c-120">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="7633c-120">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="7633c-121">Propriedades</span><span class="sxs-lookup"><span data-stu-id="7633c-121">Properties</span></span>

<span data-ttu-id="7633c-122">A classe de **\_ ação CIM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="7633c-122">The **CIM\_Action** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7633c-123">**ActionID**</span><span class="sxs-lookup"><span data-stu-id="7633c-123">**ActionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7633c-124">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7633c-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7633c-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7633c-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7633c-126">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="7633c-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="7633c-127">Identificador exclusivo atribuído a uma ação específica para um elemento de software.</span><span class="sxs-lookup"><span data-stu-id="7633c-127">Unique identifier assigned to a particular action for a software element.</span></span>

</dd> <dt>

<span data-ttu-id="7633c-128">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="7633c-128">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7633c-129">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7633c-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7633c-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7633c-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7633c-131">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="7633c-131">Qualifiers: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="7633c-132">Breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="7633c-132">Short textual description of the object.</span></span>

</dd> <dt>

<span data-ttu-id="7633c-133">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="7633c-133">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7633c-134">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7633c-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7633c-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7633c-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7633c-136">Descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="7633c-136">Description of the object.</span></span>

</dd> <dt>

<span data-ttu-id="7633c-137">**Direção**</span><span class="sxs-lookup"><span data-stu-id="7633c-137">**Direction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7633c-138">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7633c-138">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7633c-139">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7633c-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7633c-140">Indica se um objeto **de \_ ação CIM** específico faz parte de uma sequência de ações para fazer a transição do elemento de software atual para seu próximo estado, como "instalar" ou para remover o elemento de software atual, como "Desinstalar".</span><span class="sxs-lookup"><span data-stu-id="7633c-140">Indicates whether a particular **CIM\_Action** object is part of a sequence of actions to transition the current software element to its next state, such as "Install", or to remove the current software element, such as "Uninstall".</span></span>

<dt>

<span id="Install"></span><span id="install"></span><span id="INSTALL"></span>

<span data-ttu-id="7633c-141">**Instalar** (0)</span><span class="sxs-lookup"><span data-stu-id="7633c-141">**Install** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Uninstall"></span><span id="uninstall"></span><span id="UNINSTALL"></span>

<span data-ttu-id="7633c-142">**Desinstalar** (1)</span><span class="sxs-lookup"><span data-stu-id="7633c-142">**Uninstall** (1)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7633c-143">**Nome**</span><span class="sxs-lookup"><span data-stu-id="7633c-143">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7633c-144">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7633c-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7633c-145">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7633c-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7633c-146">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ softwareelement**](cim-softwareelement.md).**Name**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="7633c-146">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Name**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="7633c-147">Identifica o elemento de software.</span><span class="sxs-lookup"><span data-stu-id="7633c-147">Identifies the software element.</span></span>

</dd> <dt>

<span data-ttu-id="7633c-148">**SoftwareElementID**</span><span class="sxs-lookup"><span data-stu-id="7633c-148">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7633c-149">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7633c-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7633c-150">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7633c-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7633c-151">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ softwareelement**](cim-softwareelement.md).**SoftwareElementID**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="7633c-151">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="7633c-152">Identificador para o elemento de software.</span><span class="sxs-lookup"><span data-stu-id="7633c-152">Identifier for the software element.</span></span>

</dd> <dt>

<span data-ttu-id="7633c-153">**SoftwareElementState**</span><span class="sxs-lookup"><span data-stu-id="7633c-153">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7633c-154">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7633c-154">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7633c-155">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7633c-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7633c-156">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ softwareelement**](cim-softwareelement.md).**SoftwareElementState**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="7633c-156">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="7633c-157">Estado de um elemento de software.</span><span class="sxs-lookup"><span data-stu-id="7633c-157">State of a software element.</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="7633c-158"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Implantável** (0)</span><span class="sxs-lookup"><span data-stu-id="7633c-158"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Deployable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="7633c-159">Descreve os detalhes necessários para a distribuição bem-sucedida e os detalhes (condições e ações) necessários para criar um elemento de software no estado instalável (ou seja, o próximo estado).</span><span class="sxs-lookup"><span data-stu-id="7633c-159">Describes the details necessary for successful distribution and the details (conditions and actions) required to create a software element in the installable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="7633c-160"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Instalável** (1)</span><span class="sxs-lookup"><span data-stu-id="7633c-160"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="7633c-161">Descreve os detalhes necessários para a instalação bem-sucedida e os detalhes (condições e ações) necessários para criar um elemento de software no estado executável (ou seja, o próximo estado).</span><span class="sxs-lookup"><span data-stu-id="7633c-161">Describes the details necessary for successful installation and the details (conditions and actions) required to create a software element in the executable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="7633c-162"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executável** (2)</span><span class="sxs-lookup"><span data-stu-id="7633c-162"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="7633c-163">Descreve os detalhes necessários para a execução bem-sucedida e os detalhes (condições e ações) necessários para criar um elemento de software no estado em execução (ou seja, o próximo estado).</span><span class="sxs-lookup"><span data-stu-id="7633c-163">Describes the details necessary for successful execution and the details (conditions and actions) required to create a software element in the running state (that is, the next state).</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="7633c-164"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Em execução** (3)</span><span class="sxs-lookup"><span data-stu-id="7633c-164"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd>

<span data-ttu-id="7633c-165">Descreve os detalhes necessários para monitorar e operar em um elemento inicial.</span><span class="sxs-lookup"><span data-stu-id="7633c-165">Describes the details necessary to monitor and operate on a start element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="7633c-166">**TargetOperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="7633c-166">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7633c-167">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7633c-167">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7633c-168">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7633c-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7633c-169">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ softwareelement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Informações do componente de software DMTF \| 2,5 ")</span><span class="sxs-lookup"><span data-stu-id="7633c-169">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.5")</span></span>
</dt> </dl>

<span data-ttu-id="7633c-170">Sistema operacional de destino do elemento de software proprietário.</span><span class="sxs-lookup"><span data-stu-id="7633c-170">Target operating system of the owning software element.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7633c-171"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="7633c-171"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="7633c-172"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="7633c-172"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="7633c-173"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span><span class="sxs-lookup"><span data-stu-id="7633c-173"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="7633c-174">Mac OS</span><span class="sxs-lookup"><span data-stu-id="7633c-174">Mac OS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="7633c-175"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span><span class="sxs-lookup"><span data-stu-id="7633c-175"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="7633c-176"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span><span class="sxs-lookup"><span data-stu-id="7633c-176"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="7633c-177"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span><span class="sxs-lookup"><span data-stu-id="7633c-177"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="7633c-178"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Unix Digital** (6)</span><span class="sxs-lookup"><span data-stu-id="7633c-178"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="7633c-179"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span><span class="sxs-lookup"><span data-stu-id="7633c-179"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="7633c-180">Abrir VMS</span><span class="sxs-lookup"><span data-stu-id="7633c-180">Open VMS</span></span>

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="7633c-181"><span id="HPUX"></span><span id="hpux"></span>HP **(8** )</span><span class="sxs-lookup"><span data-stu-id="7633c-181"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd>

<span data-ttu-id="7633c-182">HP-UX</span><span class="sxs-lookup"><span data-stu-id="7633c-182">HP-UX</span></span>

</dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="7633c-183"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span><span class="sxs-lookup"><span data-stu-id="7633c-183"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="7633c-184"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span><span class="sxs-lookup"><span data-stu-id="7633c-184"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="7633c-185"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span><span class="sxs-lookup"><span data-stu-id="7633c-185"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="7633c-186"><span id="OS_2"></span><span id="os_2"></span>**Sistema operacional/2** (12)</span><span class="sxs-lookup"><span data-stu-id="7633c-186"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="7633c-187"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span><span class="sxs-lookup"><span data-stu-id="7633c-187"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd>

<span data-ttu-id="7633c-188">VM (máquina virtual) da Microsoft para Java</span><span class="sxs-lookup"><span data-stu-id="7633c-188">Microsoft Virtual Machine (VM) for Java</span></span>

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="7633c-189"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span><span class="sxs-lookup"><span data-stu-id="7633c-189"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="7633c-190"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span><span class="sxs-lookup"><span data-stu-id="7633c-190"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd>

<span data-ttu-id="7633c-191">Windows 3. x</span><span class="sxs-lookup"><span data-stu-id="7633c-191">Windows 3.x</span></span>

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="7633c-192"><span id="WIN95"></span><span id="win95"></span>**Win95** (16)</span><span class="sxs-lookup"><span data-stu-id="7633c-192"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd>

<span data-ttu-id="7633c-193">Windows 95</span><span class="sxs-lookup"><span data-stu-id="7633c-193">Windows 95</span></span>

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="7633c-194"><span id="WIN98"></span><span id="win98"></span>**Win98** (17)</span><span class="sxs-lookup"><span data-stu-id="7633c-194"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd>

<span data-ttu-id="7633c-195">Windows 98</span><span class="sxs-lookup"><span data-stu-id="7633c-195">Windows 98</span></span>

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="7633c-196"><span id="WINNT"></span><span id="winnt"></span>**WinNT** (18)</span><span class="sxs-lookup"><span data-stu-id="7633c-196"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd>

<span data-ttu-id="7633c-197">Windows NT</span><span class="sxs-lookup"><span data-stu-id="7633c-197">Windows NT</span></span>

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="7633c-198"><span id="WINCE"></span><span id="wince"></span>**WinCE** (19)</span><span class="sxs-lookup"><span data-stu-id="7633c-198"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd>

<span data-ttu-id="7633c-199">Windows CE</span><span class="sxs-lookup"><span data-stu-id="7633c-199">Windows CE</span></span>

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="7633c-200"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span><span class="sxs-lookup"><span data-stu-id="7633c-200"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd>

<span data-ttu-id="7633c-201">NCR 3000</span><span class="sxs-lookup"><span data-stu-id="7633c-201">NCR 3000</span></span>

</dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="7633c-202"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span><span class="sxs-lookup"><span data-stu-id="7633c-202"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="7633c-203"><span id="OSF"></span><span id="osf"></span>**Uso** (22)</span><span class="sxs-lookup"><span data-stu-id="7633c-203"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="7633c-204"><span id="DC_OS"></span><span id="dc_os"></span>**DC/os** (23)</span><span class="sxs-lookup"><span data-stu-id="7633c-204"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="7633c-205"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Unix dependente** (24)</span><span class="sxs-lookup"><span data-stu-id="7633c-205"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="7633c-206"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span><span class="sxs-lookup"><span data-stu-id="7633c-206"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="7633c-207"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span><span class="sxs-lookup"><span data-stu-id="7633c-207"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="7633c-208"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Subsequentes** (27)</span><span class="sxs-lookup"><span data-stu-id="7633c-208"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="7633c-209"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span><span class="sxs-lookup"><span data-stu-id="7633c-209"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="7633c-210"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span><span class="sxs-lookup"><span data-stu-id="7633c-210"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="7633c-211"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span><span class="sxs-lookup"><span data-stu-id="7633c-211"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="7633c-212"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span><span class="sxs-lookup"><span data-stu-id="7633c-212"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="7633c-213"><span id="ASERIES"></span><span id="aseries"></span>**ASeries** (32)</span><span class="sxs-lookup"><span data-stu-id="7633c-213"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd>

<span data-ttu-id="7633c-214">Uma série</span><span class="sxs-lookup"><span data-stu-id="7633c-214">A Series</span></span>

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="7633c-215"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span><span class="sxs-lookup"><span data-stu-id="7633c-215"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd>

<span data-ttu-id="7633c-216">NSK tandem</span><span class="sxs-lookup"><span data-stu-id="7633c-216">Tandem NSK</span></span>

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="7633c-217"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span><span class="sxs-lookup"><span data-stu-id="7633c-217"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd>

<span data-ttu-id="7633c-218">NT em tandem</span><span class="sxs-lookup"><span data-stu-id="7633c-218">Tandem NT</span></span>

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="7633c-219"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span><span class="sxs-lookup"><span data-stu-id="7633c-219"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd>

<span data-ttu-id="7633c-220">BS2000/OSD</span><span class="sxs-lookup"><span data-stu-id="7633c-220">BS2000/OSD</span></span>

</dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="7633c-221"><span id="LINUX"></span><span id="linux"></span>**Linux** (36)</span><span class="sxs-lookup"><span data-stu-id="7633c-221"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="7633c-222"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span><span class="sxs-lookup"><span data-stu-id="7633c-222"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="7633c-223"><span id="XENIX"></span><span id="xenix"></span>**Xenix** (38)</span><span class="sxs-lookup"><span data-stu-id="7633c-223"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="7633c-224"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span><span class="sxs-lookup"><span data-stu-id="7633c-224"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="7633c-225"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Unix interativo** (40)</span><span class="sxs-lookup"><span data-stu-id="7633c-225"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="7633c-226"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span><span class="sxs-lookup"><span data-stu-id="7633c-226"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd>

<span data-ttu-id="7633c-227">BSD UNIX</span><span class="sxs-lookup"><span data-stu-id="7633c-227">BSD UNIX</span></span>

</dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="7633c-228"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span><span class="sxs-lookup"><span data-stu-id="7633c-228"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="7633c-229"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span><span class="sxs-lookup"><span data-stu-id="7633c-229"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="7633c-230"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span><span class="sxs-lookup"><span data-stu-id="7633c-230"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="7633c-231"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span><span class="sxs-lookup"><span data-stu-id="7633c-231"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd>

<span data-ttu-id="7633c-232">Mac OS 9</span><span class="sxs-lookup"><span data-stu-id="7633c-232">Mac OS 9</span></span>

</dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="7633c-233"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**Kernel Mach** (46)</span><span class="sxs-lookup"><span data-stu-id="7633c-233"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="7633c-234"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span><span class="sxs-lookup"><span data-stu-id="7633c-234"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="7633c-235"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span><span class="sxs-lookup"><span data-stu-id="7633c-235"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="7633c-236"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span><span class="sxs-lookup"><span data-stu-id="7633c-236"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="7633c-237"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span><span class="sxs-lookup"><span data-stu-id="7633c-237"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="7633c-238"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span><span class="sxs-lookup"><span data-stu-id="7633c-238"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="7633c-239"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**Menta** (52)</span><span class="sxs-lookup"><span data-stu-id="7633c-239"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="7633c-240"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span><span class="sxs-lookup"><span data-stu-id="7633c-240"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd>

<span data-ttu-id="7633c-241">Ser so</span><span class="sxs-lookup"><span data-stu-id="7633c-241">Be OS</span></span>

</dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="7633c-242"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span><span class="sxs-lookup"><span data-stu-id="7633c-242"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="7633c-243"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NEXTSTEP** (55)</span><span class="sxs-lookup"><span data-stu-id="7633c-243"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="7633c-244"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span><span class="sxs-lookup"><span data-stu-id="7633c-244"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd>

<span data-ttu-id="7633c-245">Sistema operacional Palm</span><span class="sxs-lookup"><span data-stu-id="7633c-245">Palm OS</span></span>

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="7633c-246"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span><span class="sxs-lookup"><span data-stu-id="7633c-246"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="7633c-247"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span><span class="sxs-lookup"><span data-stu-id="7633c-247"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="7633c-248"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicado** (59)</span><span class="sxs-lookup"><span data-stu-id="7633c-248"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="7633c-249"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span><span class="sxs-lookup"><span data-stu-id="7633c-249"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="7633c-250"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span><span class="sxs-lookup"><span data-stu-id="7633c-250"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7633c-251">**Versão**</span><span class="sxs-lookup"><span data-stu-id="7633c-251">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7633c-252">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7633c-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7633c-253">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7633c-253">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7633c-254">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ softwareelement**](cim-softwareelement.md).**Version**"), [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Componente DMTF \| 1,3 ")</span><span class="sxs-lookup"><span data-stu-id="7633c-254">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Version**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="7633c-255">Versão da operação.</span><span class="sxs-lookup"><span data-stu-id="7633c-255">Version of the operation.</span></span>

<span data-ttu-id="7633c-256">A versão da operação deve estar em um dos seguintes formatos:</span><span class="sxs-lookup"><span data-stu-id="7633c-256">The version of the operation should be in one of the following forms:</span></span>

-   <span data-ttu-id="7633c-257"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="7633c-257"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="7633c-258"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="7633c-258"><major>.<minor><letter><revision></span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7633c-259">Comentários</span><span class="sxs-lookup"><span data-stu-id="7633c-259">Remarks</span></span>

<span data-ttu-id="7633c-260">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="7633c-260">WMI does not implement this class.</span></span> <span data-ttu-id="7633c-261">Consulte [classes Win32](win32-provider.md) para classes derivadas da **\_ ação de CIM**.</span><span class="sxs-lookup"><span data-stu-id="7633c-261">See [Win32 Classes](win32-provider.md) for classes derived from **CIM\_Action**.</span></span>

<span data-ttu-id="7633c-262">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="7633c-262">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="7633c-263">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="7633c-263">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="7633c-264">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7633c-264">Requirements</span></span>



| <span data-ttu-id="7633c-265">Requisito</span><span class="sxs-lookup"><span data-stu-id="7633c-265">Requirement</span></span> | <span data-ttu-id="7633c-266">Valor</span><span class="sxs-lookup"><span data-stu-id="7633c-266">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7633c-267">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7633c-267">Minimum supported client</span></span><br/> | <span data-ttu-id="7633c-268">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7633c-268">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7633c-269">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7633c-269">Minimum supported server</span></span><br/> | <span data-ttu-id="7633c-270">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7633c-270">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7633c-271">Namespace</span><span class="sxs-lookup"><span data-stu-id="7633c-271">Namespace</span></span><br/>                | <span data-ttu-id="7633c-272">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="7633c-272">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7633c-273">MOF</span><span class="sxs-lookup"><span data-stu-id="7633c-273">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7633c-274"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7633c-274"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7633c-275">DLL</span><span class="sxs-lookup"><span data-stu-id="7633c-275">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7633c-276"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7633c-276"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7633c-277">Confira também</span><span class="sxs-lookup"><span data-stu-id="7633c-277">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7633c-278">Classes CIM</span><span class="sxs-lookup"><span data-stu-id="7633c-278">CIM Classes</span></span>](/windows/desktop/WmiSdk/cimclas)
</dt> </dl>

 

