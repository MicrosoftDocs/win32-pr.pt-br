---
description: A \_ classe CIM ExecuteProgram representa os arquivos que podem ser executados no sistema onde o elemento de software está instalado.
ms.assetid: 4329d228-4069-4a5a-b1eb-2dbad9644118
ms.tgt_platform: multiple
title: Classe CIM_ExecuteProgram
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ExecuteProgram
- CIM_ExecuteProgram.ActionID
- CIM_ExecuteProgram.Caption
- CIM_ExecuteProgram.Description
- CIM_ExecuteProgram.Direction
- CIM_ExecuteProgram.Name
- CIM_ExecuteProgram.SoftwareElementID
- CIM_ExecuteProgram.SoftwareElementState
- CIM_ExecuteProgram.TargetOperatingSystem
- CIM_ExecuteProgram.Version
- CIM_ExecuteProgram.CommandLine
- CIM_ExecuteProgram.ProgramPath
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 76743d255bc50d213a4ce3f44057d97830078ccd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089289"
---
# <a name="cim_executeprogram-class"></a><span data-ttu-id="9225a-103">\_Classe CIM ExecuteProgram</span><span class="sxs-lookup"><span data-stu-id="9225a-103">CIM\_ExecuteProgram class</span></span>

<span data-ttu-id="9225a-104">A classe **CIM \_ ExecuteProgram** representa os arquivos que podem ser executados no sistema onde o elemento de software está instalado.</span><span class="sxs-lookup"><span data-stu-id="9225a-104">The **CIM\_ExecuteProgram** class represents files that can be executed on the system where the software element is installed.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9225a-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="9225a-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="9225a-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="9225a-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="9225a-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="9225a-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="9225a-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="9225a-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="9225a-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9225a-109">Syntax</span></span>

``` syntax
[UUID("{149ADDEE-DB2A-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_ExecuteProgram : CIM_Action
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
  string CommandLine;
  string ProgramPath;
};
```

## <a name="members"></a><span data-ttu-id="9225a-110">Membros</span><span class="sxs-lookup"><span data-stu-id="9225a-110">Members</span></span>

<span data-ttu-id="9225a-111">A classe **CIM \_ ExecuteProgram** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="9225a-111">The **CIM\_ExecuteProgram** class has these types of members:</span></span>

-   [<span data-ttu-id="9225a-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="9225a-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="9225a-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="9225a-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="9225a-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="9225a-114">Methods</span></span>

<span data-ttu-id="9225a-115">A classe **CIM \_ ExecuteProgram** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="9225a-115">The **CIM\_ExecuteProgram** class has these methods.</span></span>



| <span data-ttu-id="9225a-116">Método</span><span class="sxs-lookup"><span data-stu-id="9225a-116">Method</span></span>                                                      | <span data-ttu-id="9225a-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="9225a-117">Description</span></span>                                                   |
|:------------------------------------------------------------|:--------------------------------------------------------------|
| [<span data-ttu-id="9225a-118">**Chame**</span><span class="sxs-lookup"><span data-stu-id="9225a-118">**Invoke**</span></span>](invoke-method-in-class-cim-executeprogram.md) | <span data-ttu-id="9225a-119">Executa uma ação específica.</span><span class="sxs-lookup"><span data-stu-id="9225a-119">Takes a particular action.</span></span> <span data-ttu-id="9225a-120">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="9225a-120">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="9225a-121">Propriedades</span><span class="sxs-lookup"><span data-stu-id="9225a-121">Properties</span></span>

<span data-ttu-id="9225a-122">A classe **CIM \_ ExecuteProgram** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="9225a-122">The **CIM\_ExecuteProgram** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9225a-123">**ActionID**</span><span class="sxs-lookup"><span data-stu-id="9225a-123">**ActionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9225a-124">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9225a-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9225a-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9225a-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9225a-126">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="9225a-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="9225a-127">Identificador exclusivo atribuído a uma ação específica para um elemento de software.</span><span class="sxs-lookup"><span data-stu-id="9225a-127">Unique identifier assigned to a particular action for a software element.</span></span>

<span data-ttu-id="9225a-128">Esta propriedade é herdada [**da \_ ação CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="9225a-128">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="9225a-129">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="9225a-129">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9225a-130">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9225a-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9225a-131">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9225a-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9225a-132">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="9225a-132">Qualifiers: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="9225a-133">Breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="9225a-133">Short textual description of the object.</span></span>

<span data-ttu-id="9225a-134">Esta propriedade é herdada [**da \_ ação CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="9225a-134">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="9225a-135">**CommandLine**</span><span class="sxs-lookup"><span data-stu-id="9225a-135">**CommandLine**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9225a-136">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9225a-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9225a-137">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9225a-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9225a-138">Cadeia de caracteres que pode ser invocada em uma linha de comando do sistema.</span><span class="sxs-lookup"><span data-stu-id="9225a-138">String that can be invoked on a system command line.</span></span>

</dd> <dt>

<span data-ttu-id="9225a-139">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="9225a-139">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9225a-140">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9225a-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9225a-141">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9225a-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9225a-142">Descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="9225a-142">Description of the object.</span></span>

<span data-ttu-id="9225a-143">Esta propriedade é herdada [**da \_ ação CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="9225a-143">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="9225a-144">**Direção**</span><span class="sxs-lookup"><span data-stu-id="9225a-144">**Direction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9225a-145">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9225a-145">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9225a-146">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9225a-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9225a-147">Indica se um objeto [**de \_ ação CIM**](cim-action.md) específico faz parte de uma sequência de ações para fazer a transição do elemento de software atual para seu próximo estado, como "instalar" ou para remover o elemento de software atual, como "Desinstalar".</span><span class="sxs-lookup"><span data-stu-id="9225a-147">Indicates whether a particular [**CIM\_Action**](cim-action.md) object is part of a sequence of actions to transition the current software element to its next state, such as "Install", or to remove the current software element, such as "Uninstall".</span></span>

<span data-ttu-id="9225a-148">Esta propriedade é herdada [**da \_ ação CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="9225a-148">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

<dt>

<span id="Install"></span><span id="install"></span><span id="INSTALL"></span>

<span data-ttu-id="9225a-149">**Instalar** (0)</span><span class="sxs-lookup"><span data-stu-id="9225a-149">**Install** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Uninstall"></span><span id="uninstall"></span><span id="UNINSTALL"></span>

<span data-ttu-id="9225a-150">**Desinstalar** (1)</span><span class="sxs-lookup"><span data-stu-id="9225a-150">**Uninstall** (1)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9225a-151">**Nome**</span><span class="sxs-lookup"><span data-stu-id="9225a-151">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9225a-152">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9225a-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9225a-153">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9225a-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9225a-154">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ softwareelement**](cim-softwareelement.md).**Name**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="9225a-154">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Name**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="9225a-155">Identifica o elemento de software.</span><span class="sxs-lookup"><span data-stu-id="9225a-155">Identifies the software element.</span></span>

<span data-ttu-id="9225a-156">Esta propriedade é herdada [**da \_ ação CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="9225a-156">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="9225a-157">**ProgramPath**</span><span class="sxs-lookup"><span data-stu-id="9225a-157">**ProgramPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9225a-158">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9225a-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9225a-159">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9225a-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9225a-160">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="9225a-160">Qualifiers: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="9225a-161">Caminho para o programa.</span><span class="sxs-lookup"><span data-stu-id="9225a-161">Path to the program.</span></span>

</dd> <dt>

<span data-ttu-id="9225a-162">**SoftwareElementID**</span><span class="sxs-lookup"><span data-stu-id="9225a-162">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9225a-163">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9225a-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9225a-164">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9225a-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9225a-165">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ softwareelement**](cim-softwareelement.md).**SoftwareElementID**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="9225a-165">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="9225a-166">Identificador para o elemento de software.</span><span class="sxs-lookup"><span data-stu-id="9225a-166">Identifier for the software element.</span></span>

<span data-ttu-id="9225a-167">Esta propriedade é herdada [**da \_ ação CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="9225a-167">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="9225a-168">**SoftwareElementState**</span><span class="sxs-lookup"><span data-stu-id="9225a-168">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9225a-169">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9225a-169">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9225a-170">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9225a-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9225a-171">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ softwareelement**](cim-softwareelement.md).**SoftwareElementState**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="9225a-171">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="9225a-172">Estado de um elemento de software.</span><span class="sxs-lookup"><span data-stu-id="9225a-172">State of a software element.</span></span>

<span data-ttu-id="9225a-173">Esta propriedade é herdada [**da \_ ação CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="9225a-173">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="9225a-174"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Implantável** (0)</span><span class="sxs-lookup"><span data-stu-id="9225a-174"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Deployable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="9225a-175">Descreve os detalhes necessários para a distribuição bem-sucedida e os detalhes (condições e ações) necessários para criar um elemento de software no estado instalável (ou seja, o próximo estado).</span><span class="sxs-lookup"><span data-stu-id="9225a-175">Describes the details necessary for successful distribution and the details (conditions and actions) required to create a software element in the installable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="9225a-176"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Instalável** (1)</span><span class="sxs-lookup"><span data-stu-id="9225a-176"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="9225a-177">Descreve os detalhes necessários para a instalação bem-sucedida e os detalhes (condições e ações) necessários para criar um elemento de software no estado executável (ou seja, o próximo estado).</span><span class="sxs-lookup"><span data-stu-id="9225a-177">Describes the details necessary for successful installation and the details (conditions and actions) required to create a software element in the executable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="9225a-178"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executável** (2)</span><span class="sxs-lookup"><span data-stu-id="9225a-178"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="9225a-179">Descreve os detalhes necessários para a execução bem-sucedida e os detalhes (condições e ações) necessários para criar um elemento de software no estado em execução (ou seja, o próximo estado).</span><span class="sxs-lookup"><span data-stu-id="9225a-179">Describes the details necessary for successful execution and the details (conditions and actions) required to create a software element in the running state (that is, the next state).</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="9225a-180"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Em execução** (3)</span><span class="sxs-lookup"><span data-stu-id="9225a-180"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd>

<span data-ttu-id="9225a-181">Descreve os detalhes necessários para monitorar e operar em um elemento inicial.</span><span class="sxs-lookup"><span data-stu-id="9225a-181">Describes the details necessary to monitor and operate on a start element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="9225a-182">**TargetOperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="9225a-182">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9225a-183">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9225a-183">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9225a-184">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9225a-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9225a-185">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ softwareelement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Informações do componente de software DMTF \| 2,5 ")</span><span class="sxs-lookup"><span data-stu-id="9225a-185">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.5")</span></span>
</dt> </dl>

<span data-ttu-id="9225a-186">Sistema operacional de destino do elemento de software proprietário.</span><span class="sxs-lookup"><span data-stu-id="9225a-186">Target operating system of the owning software element.</span></span>

<span data-ttu-id="9225a-187">Esta propriedade é herdada [**da \_ ação CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="9225a-187">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9225a-188"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="9225a-188"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="9225a-189"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="9225a-189"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="9225a-190"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span><span class="sxs-lookup"><span data-stu-id="9225a-190"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="9225a-191">Mac OS</span><span class="sxs-lookup"><span data-stu-id="9225a-191">Mac OS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="9225a-192"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span><span class="sxs-lookup"><span data-stu-id="9225a-192"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="9225a-193"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span><span class="sxs-lookup"><span data-stu-id="9225a-193"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="9225a-194"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span><span class="sxs-lookup"><span data-stu-id="9225a-194"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="9225a-195"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Unix Digital** (6)</span><span class="sxs-lookup"><span data-stu-id="9225a-195"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="9225a-196"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span><span class="sxs-lookup"><span data-stu-id="9225a-196"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="9225a-197">Abrir VMS</span><span class="sxs-lookup"><span data-stu-id="9225a-197">Open VMS</span></span>

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="9225a-198"><span id="HPUX"></span><span id="hpux"></span>HP **(8** )</span><span class="sxs-lookup"><span data-stu-id="9225a-198"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd>

<span data-ttu-id="9225a-199">HP-UX</span><span class="sxs-lookup"><span data-stu-id="9225a-199">HP-UX</span></span>

</dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="9225a-200"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span><span class="sxs-lookup"><span data-stu-id="9225a-200"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="9225a-201"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span><span class="sxs-lookup"><span data-stu-id="9225a-201"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="9225a-202"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span><span class="sxs-lookup"><span data-stu-id="9225a-202"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="9225a-203"><span id="OS_2"></span><span id="os_2"></span>**Sistema operacional/2** (12)</span><span class="sxs-lookup"><span data-stu-id="9225a-203"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="9225a-204"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span><span class="sxs-lookup"><span data-stu-id="9225a-204"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd>

<span data-ttu-id="9225a-205">VM (máquina virtual) da Microsoft para Java</span><span class="sxs-lookup"><span data-stu-id="9225a-205">Microsoft Virtual Machine (VM) for Java</span></span>

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="9225a-206"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span><span class="sxs-lookup"><span data-stu-id="9225a-206"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="9225a-207"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span><span class="sxs-lookup"><span data-stu-id="9225a-207"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd>

<span data-ttu-id="9225a-208">Windows 3. x</span><span class="sxs-lookup"><span data-stu-id="9225a-208">Windows 3.x</span></span>

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="9225a-209"><span id="WIN95"></span><span id="win95"></span>**Win95** (16)</span><span class="sxs-lookup"><span data-stu-id="9225a-209"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd>

<span data-ttu-id="9225a-210">Windows 95</span><span class="sxs-lookup"><span data-stu-id="9225a-210">Windows 95</span></span>

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="9225a-211"><span id="WIN98"></span><span id="win98"></span>**Win98** (17)</span><span class="sxs-lookup"><span data-stu-id="9225a-211"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd>

<span data-ttu-id="9225a-212">Windows 98</span><span class="sxs-lookup"><span data-stu-id="9225a-212">Windows 98</span></span>

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="9225a-213"><span id="WINNT"></span><span id="winnt"></span>**WinNT** (18)</span><span class="sxs-lookup"><span data-stu-id="9225a-213"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd>

<span data-ttu-id="9225a-214">Windows NT</span><span class="sxs-lookup"><span data-stu-id="9225a-214">Windows NT</span></span>

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="9225a-215"><span id="WINCE"></span><span id="wince"></span>**WinCE** (19)</span><span class="sxs-lookup"><span data-stu-id="9225a-215"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd>

<span data-ttu-id="9225a-216">Windows CE</span><span class="sxs-lookup"><span data-stu-id="9225a-216">Windows CE</span></span>

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="9225a-217"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span><span class="sxs-lookup"><span data-stu-id="9225a-217"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd>

<span data-ttu-id="9225a-218">NCR 3000</span><span class="sxs-lookup"><span data-stu-id="9225a-218">NCR 3000</span></span>

</dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="9225a-219"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span><span class="sxs-lookup"><span data-stu-id="9225a-219"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="9225a-220"><span id="OSF"></span><span id="osf"></span>**Uso** (22)</span><span class="sxs-lookup"><span data-stu-id="9225a-220"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="9225a-221"><span id="DC_OS"></span><span id="dc_os"></span>**DC/os** (23)</span><span class="sxs-lookup"><span data-stu-id="9225a-221"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="9225a-222"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Unix dependente** (24)</span><span class="sxs-lookup"><span data-stu-id="9225a-222"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="9225a-223"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span><span class="sxs-lookup"><span data-stu-id="9225a-223"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="9225a-224"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span><span class="sxs-lookup"><span data-stu-id="9225a-224"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="9225a-225"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Subsequentes** (27)</span><span class="sxs-lookup"><span data-stu-id="9225a-225"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="9225a-226"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span><span class="sxs-lookup"><span data-stu-id="9225a-226"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="9225a-227"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span><span class="sxs-lookup"><span data-stu-id="9225a-227"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="9225a-228"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span><span class="sxs-lookup"><span data-stu-id="9225a-228"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="9225a-229"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span><span class="sxs-lookup"><span data-stu-id="9225a-229"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="9225a-230"><span id="ASERIES"></span><span id="aseries"></span>**ASeries** (32)</span><span class="sxs-lookup"><span data-stu-id="9225a-230"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd>

<span data-ttu-id="9225a-231">Uma série</span><span class="sxs-lookup"><span data-stu-id="9225a-231">A Series</span></span>

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="9225a-232"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span><span class="sxs-lookup"><span data-stu-id="9225a-232"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd>

<span data-ttu-id="9225a-233">NSK tandem</span><span class="sxs-lookup"><span data-stu-id="9225a-233">Tandem NSK</span></span>

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="9225a-234"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span><span class="sxs-lookup"><span data-stu-id="9225a-234"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd>

<span data-ttu-id="9225a-235">NT em tandem</span><span class="sxs-lookup"><span data-stu-id="9225a-235">Tandem NT</span></span>

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="9225a-236"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span><span class="sxs-lookup"><span data-stu-id="9225a-236"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd>

<span data-ttu-id="9225a-237">BS2000/OSD</span><span class="sxs-lookup"><span data-stu-id="9225a-237">BS2000/OSD</span></span>

</dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="9225a-238"><span id="LINUX"></span><span id="linux"></span>**Linux** (36)</span><span class="sxs-lookup"><span data-stu-id="9225a-238"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="9225a-239"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span><span class="sxs-lookup"><span data-stu-id="9225a-239"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="9225a-240"><span id="XENIX"></span><span id="xenix"></span>**Xenix** (38)</span><span class="sxs-lookup"><span data-stu-id="9225a-240"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="9225a-241"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span><span class="sxs-lookup"><span data-stu-id="9225a-241"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="9225a-242"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Unix interativo** (40)</span><span class="sxs-lookup"><span data-stu-id="9225a-242"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="9225a-243"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span><span class="sxs-lookup"><span data-stu-id="9225a-243"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd>

<span data-ttu-id="9225a-244">BSD UNIX</span><span class="sxs-lookup"><span data-stu-id="9225a-244">BSD UNIX</span></span>

</dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="9225a-245"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span><span class="sxs-lookup"><span data-stu-id="9225a-245"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="9225a-246"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span><span class="sxs-lookup"><span data-stu-id="9225a-246"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="9225a-247"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span><span class="sxs-lookup"><span data-stu-id="9225a-247"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="9225a-248"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span><span class="sxs-lookup"><span data-stu-id="9225a-248"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd>

<span data-ttu-id="9225a-249">Mac OS 9</span><span class="sxs-lookup"><span data-stu-id="9225a-249">Mac OS 9</span></span>

</dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="9225a-250"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**Kernel Mach** (46)</span><span class="sxs-lookup"><span data-stu-id="9225a-250"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="9225a-251"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span><span class="sxs-lookup"><span data-stu-id="9225a-251"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="9225a-252"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span><span class="sxs-lookup"><span data-stu-id="9225a-252"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="9225a-253"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span><span class="sxs-lookup"><span data-stu-id="9225a-253"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="9225a-254"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span><span class="sxs-lookup"><span data-stu-id="9225a-254"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="9225a-255"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span><span class="sxs-lookup"><span data-stu-id="9225a-255"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="9225a-256"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**Menta** (52)</span><span class="sxs-lookup"><span data-stu-id="9225a-256"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="9225a-257"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span><span class="sxs-lookup"><span data-stu-id="9225a-257"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd>

<span data-ttu-id="9225a-258">Ser so</span><span class="sxs-lookup"><span data-stu-id="9225a-258">Be OS</span></span>

</dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="9225a-259"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span><span class="sxs-lookup"><span data-stu-id="9225a-259"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="9225a-260"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NEXTSTEP** (55)</span><span class="sxs-lookup"><span data-stu-id="9225a-260"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="9225a-261"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span><span class="sxs-lookup"><span data-stu-id="9225a-261"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd>

<span data-ttu-id="9225a-262">Sistema operacional Palm</span><span class="sxs-lookup"><span data-stu-id="9225a-262">Palm OS</span></span>

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="9225a-263"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span><span class="sxs-lookup"><span data-stu-id="9225a-263"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="9225a-264"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span><span class="sxs-lookup"><span data-stu-id="9225a-264"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="9225a-265"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicado** (59)</span><span class="sxs-lookup"><span data-stu-id="9225a-265"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="9225a-266"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span><span class="sxs-lookup"><span data-stu-id="9225a-266"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="9225a-267"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span><span class="sxs-lookup"><span data-stu-id="9225a-267"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9225a-268">**Versão**</span><span class="sxs-lookup"><span data-stu-id="9225a-268">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9225a-269">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9225a-269">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9225a-270">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9225a-270">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9225a-271">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ softwareelement**](cim-softwareelement.md).**Version**"), [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Componente DMTF \| 1,3 ")</span><span class="sxs-lookup"><span data-stu-id="9225a-271">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Version**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="9225a-272">Versão da operação.</span><span class="sxs-lookup"><span data-stu-id="9225a-272">Version of the operation.</span></span>

<span data-ttu-id="9225a-273">A versão da operação deve estar em um dos seguintes formatos:</span><span class="sxs-lookup"><span data-stu-id="9225a-273">The version of the operation should be in one of the following forms:</span></span>

-   <span data-ttu-id="9225a-274"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="9225a-274"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="9225a-275"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="9225a-275"><major>.<minor><letter><revision></span></span>

<span data-ttu-id="9225a-276">Esta propriedade é herdada [**da \_ ação CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="9225a-276">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9225a-277">Comentários</span><span class="sxs-lookup"><span data-stu-id="9225a-277">Remarks</span></span>

<span data-ttu-id="9225a-278">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="9225a-278">WMI does not implement this class.</span></span>

<span data-ttu-id="9225a-279">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="9225a-279">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="9225a-280">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="9225a-280">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="9225a-281">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9225a-281">Requirements</span></span>



| <span data-ttu-id="9225a-282">Requisito</span><span class="sxs-lookup"><span data-stu-id="9225a-282">Requirement</span></span> | <span data-ttu-id="9225a-283">Valor</span><span class="sxs-lookup"><span data-stu-id="9225a-283">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9225a-284">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9225a-284">Minimum supported client</span></span><br/> | <span data-ttu-id="9225a-285">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9225a-285">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9225a-286">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9225a-286">Minimum supported server</span></span><br/> | <span data-ttu-id="9225a-287">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9225a-287">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9225a-288">Namespace</span><span class="sxs-lookup"><span data-stu-id="9225a-288">Namespace</span></span><br/>                | <span data-ttu-id="9225a-289">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="9225a-289">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9225a-290">MOF</span><span class="sxs-lookup"><span data-stu-id="9225a-290">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9225a-291"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9225a-291"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9225a-292">DLL</span><span class="sxs-lookup"><span data-stu-id="9225a-292">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9225a-293"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9225a-293"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9225a-294">Confira também</span><span class="sxs-lookup"><span data-stu-id="9225a-294">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9225a-295">**Ação de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="9225a-295">**CIM\_Action**</span></span>](cim-action.md)
</dt> </dl>

 

