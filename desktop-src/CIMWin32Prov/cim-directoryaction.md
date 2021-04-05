---
description: A \_ classe abstrata do CIM directoryaction gerencia diretórios. A criação de diretório é tratada pela \_ classe CIM Createdirectoryaction e a remoção de diretório é tratada pela \_ classe CIM RemoveDirectoryAction.
ms.assetid: 3c1e7023-cf54-4321-a340-b8616300c4c0
ms.tgt_platform: multiple
title: Classe CIM_DirectoryAction
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DirectoryAction
- CIM_DirectoryAction.ActionID
- CIM_DirectoryAction.Caption
- CIM_DirectoryAction.Description
- CIM_DirectoryAction.Direction
- CIM_DirectoryAction.Name
- CIM_DirectoryAction.SoftwareElementID
- CIM_DirectoryAction.SoftwareElementState
- CIM_DirectoryAction.TargetOperatingSystem
- CIM_DirectoryAction.Version
- CIM_DirectoryAction.DirectoryName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 130284e8cf19640e7861b17d80a4612b130f7062
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826532"
---
# <a name="cim_directoryaction-class"></a><span data-ttu-id="cb067-104">\_Classe directoryaction do CIM</span><span class="sxs-lookup"><span data-stu-id="cb067-104">CIM\_DirectoryAction class</span></span>

<span data-ttu-id="cb067-105">A classe abstrata do **CIM \_ directoryaction** gerencia diretórios.</span><span class="sxs-lookup"><span data-stu-id="cb067-105">The **CIM\_DirectoryAction** abstract class manages directories.</span></span> <span data-ttu-id="cb067-106">A criação de diretório é tratada pela classe [**CIM \_ createdirectoryaction**](cim-createdirectoryaction.md) e a remoção de diretório é tratada pela classe [**CIM \_ RemoveDirectoryAction**](cim-removedirectoryaction.md) .</span><span class="sxs-lookup"><span data-stu-id="cb067-106">Directory creation is handled by the [**CIM\_CreateDirectoryAction**](cim-createdirectoryaction.md) class and directory removal is handled by the [**CIM\_RemoveDirectoryAction**](cim-removedirectoryaction.md) class.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cb067-107">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="cb067-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="cb067-108">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="cb067-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="cb067-109">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="cb067-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="cb067-110">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="cb067-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb067-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cb067-111">Syntax</span></span>

``` syntax
[UUID("{8875A39E-DB29-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_DirectoryAction : CIM_Action
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
  string DirectoryName;
};
```

## <a name="members"></a><span data-ttu-id="cb067-112">Membros</span><span class="sxs-lookup"><span data-stu-id="cb067-112">Members</span></span>

<span data-ttu-id="cb067-113">A **classe \_ directoryaction do CIM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="cb067-113">The **CIM\_DirectoryAction** class has these types of members:</span></span>

-   [<span data-ttu-id="cb067-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="cb067-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="cb067-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="cb067-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="cb067-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="cb067-116">Methods</span></span>

<span data-ttu-id="cb067-117">A **classe \_ Directoryaction do CIM** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="cb067-117">The **CIM\_DirectoryAction** class has these methods.</span></span>



| <span data-ttu-id="cb067-118">Método</span><span class="sxs-lookup"><span data-stu-id="cb067-118">Method</span></span>                                                       | <span data-ttu-id="cb067-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="cb067-119">Description</span></span>                                                                  |
|:-------------------------------------------------------------|:-----------------------------------------------------------------------------|
| [<span data-ttu-id="cb067-120">**Chame**</span><span class="sxs-lookup"><span data-stu-id="cb067-120">**Invoke**</span></span>](invoke-method-in-class-cim-directoryaction.md) | <span data-ttu-id="cb067-121">Executa uma ação específica.</span><span class="sxs-lookup"><span data-stu-id="cb067-121">Takes a particular action.</span></span> <span data-ttu-id="cb067-122">Esse método não é implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="cb067-122">This method is not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="cb067-123">Propriedades</span><span class="sxs-lookup"><span data-stu-id="cb067-123">Properties</span></span>

<span data-ttu-id="cb067-124">A **classe \_ Directoryaction do CIM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="cb067-124">The **CIM\_DirectoryAction** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cb067-125">**ActionID**</span><span class="sxs-lookup"><span data-stu-id="cb067-125">**ActionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb067-126">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="cb067-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cb067-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cb067-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cb067-128">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="cb067-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="cb067-129">Identificador exclusivo atribuído a uma ação específica para um elemento de software.</span><span class="sxs-lookup"><span data-stu-id="cb067-129">Unique identifier assigned to a particular action for a software element.</span></span>

<span data-ttu-id="cb067-130">Esta propriedade é herdada [**da \_ ação CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="cb067-130">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="cb067-131">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="cb067-131">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb067-132">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="cb067-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cb067-133">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cb067-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cb067-134">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="cb067-134">Qualifiers: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="cb067-135">Breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="cb067-135">Short textual description of the object.</span></span>

<span data-ttu-id="cb067-136">Esta propriedade é herdada [**da \_ ação CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="cb067-136">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="cb067-137">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="cb067-137">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb067-138">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="cb067-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cb067-139">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cb067-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cb067-140">Descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="cb067-140">Description of the object.</span></span>

<span data-ttu-id="cb067-141">Esta propriedade é herdada [**da \_ ação CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="cb067-141">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="cb067-142">**Direção**</span><span class="sxs-lookup"><span data-stu-id="cb067-142">**Direction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb067-143">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cb067-143">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cb067-144">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cb067-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cb067-145">Indica se um objeto [**de \_ ação CIM**](cim-action.md) específico faz parte de uma sequência de ações para fazer a transição do elemento de software atual para seu próximo estado, como "instalar" ou para remover o elemento de software atual, como "Desinstalar".</span><span class="sxs-lookup"><span data-stu-id="cb067-145">Indicates whether a particular [**CIM\_Action**](cim-action.md) object is part of a sequence of actions to transition the current software element to its next state, such as "Install", or to remove the current software element, such as "Uninstall".</span></span>

<span data-ttu-id="cb067-146">Esta propriedade é herdada [**da \_ ação CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="cb067-146">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

<dt>

<span id="Install"></span><span id="install"></span><span id="INSTALL"></span>

<span data-ttu-id="cb067-147">**Instalar** (0)</span><span class="sxs-lookup"><span data-stu-id="cb067-147">**Install** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Uninstall"></span><span id="uninstall"></span><span id="UNINSTALL"></span>

<span data-ttu-id="cb067-148">**Desinstalar** (1)</span><span class="sxs-lookup"><span data-stu-id="cb067-148">**Uninstall** (1)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="cb067-149">**DirectoryName**</span><span class="sxs-lookup"><span data-stu-id="cb067-149">**DirectoryName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb067-150">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="cb067-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cb067-151">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cb067-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cb067-152">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="cb067-152">Qualifiers: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="cb067-153">Nome do diretório ao qual a ação se aplica.</span><span class="sxs-lookup"><span data-stu-id="cb067-153">Name of the directory to which the action applies.</span></span>

</dd> <dt>

<span data-ttu-id="cb067-154">**Nome**</span><span class="sxs-lookup"><span data-stu-id="cb067-154">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb067-155">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="cb067-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cb067-156">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cb067-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cb067-157">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ softwareelement**](cim-softwareelement.md).**Name**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="cb067-157">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Name**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="cb067-158">Identifica o elemento de software.</span><span class="sxs-lookup"><span data-stu-id="cb067-158">Identifies the software element.</span></span>

<span data-ttu-id="cb067-159">Esta propriedade é herdada [**da \_ ação CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="cb067-159">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="cb067-160">**SoftwareElementID**</span><span class="sxs-lookup"><span data-stu-id="cb067-160">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb067-161">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="cb067-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cb067-162">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cb067-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cb067-163">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ softwareelement**](cim-softwareelement.md).**SoftwareElementID**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="cb067-163">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="cb067-164">Identificador para o elemento de software.</span><span class="sxs-lookup"><span data-stu-id="cb067-164">Identifier for the software element.</span></span>

<span data-ttu-id="cb067-165">Esta propriedade é herdada [**da \_ ação CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="cb067-165">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="cb067-166">**SoftwareElementState**</span><span class="sxs-lookup"><span data-stu-id="cb067-166">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb067-167">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cb067-167">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cb067-168">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cb067-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cb067-169">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ softwareelement**](cim-softwareelement.md).**SoftwareElementState**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="cb067-169">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="cb067-170">Estado de um elemento de software.</span><span class="sxs-lookup"><span data-stu-id="cb067-170">State of a software element.</span></span>

<span data-ttu-id="cb067-171">Esta propriedade é herdada [**da \_ ação CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="cb067-171">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="cb067-172"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Implantável** (0)</span><span class="sxs-lookup"><span data-stu-id="cb067-172"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Deployable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="cb067-173">Descreve os detalhes necessários para a distribuição bem-sucedida e os detalhes (condições e ações) necessários para criar um elemento de software no estado instalável (ou seja, o próximo estado).</span><span class="sxs-lookup"><span data-stu-id="cb067-173">Describes the details necessary for successful distribution and the details (conditions and actions) required to create a software element in the installable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="cb067-174"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Instalável** (1)</span><span class="sxs-lookup"><span data-stu-id="cb067-174"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="cb067-175">Descreve os detalhes necessários para a instalação bem-sucedida e os detalhes (condições e ações) necessários para criar um elemento de software no estado executável (ou seja, o próximo estado).</span><span class="sxs-lookup"><span data-stu-id="cb067-175">Describes the details necessary for successful installation and the details (conditions and actions) required to create a software element in the executable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="cb067-176"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executável** (2)</span><span class="sxs-lookup"><span data-stu-id="cb067-176"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="cb067-177">Descreve os detalhes necessários para a execução bem-sucedida e os detalhes (condições e ações) necessários para criar um elemento de software no estado em execução (ou seja, o próximo estado).</span><span class="sxs-lookup"><span data-stu-id="cb067-177">Describes the details necessary for successful execution and the details (conditions and actions) required to create a software element in the running state (that is, the next state).</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="cb067-178"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Em execução** (3)</span><span class="sxs-lookup"><span data-stu-id="cb067-178"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd>

<span data-ttu-id="cb067-179">Descreve os detalhes necessários para monitorar e operar em um elemento inicial.</span><span class="sxs-lookup"><span data-stu-id="cb067-179">Describes the details necessary to monitor and operate on a start element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="cb067-180">**TargetOperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="cb067-180">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb067-181">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cb067-181">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cb067-182">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cb067-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cb067-183">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ softwareelement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Informações do componente de software DMTF \| 2,5 ")</span><span class="sxs-lookup"><span data-stu-id="cb067-183">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.5")</span></span>
</dt> </dl>

<span data-ttu-id="cb067-184">Sistema operacional de destino do elemento de software proprietário.</span><span class="sxs-lookup"><span data-stu-id="cb067-184">Target operating system of the owning software element.</span></span>

<span data-ttu-id="cb067-185">Esta propriedade é herdada [**da \_ ação CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="cb067-185">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="cb067-186"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="cb067-186"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="cb067-187"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="cb067-187"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="cb067-188"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span><span class="sxs-lookup"><span data-stu-id="cb067-188"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="cb067-189">Mac OS</span><span class="sxs-lookup"><span data-stu-id="cb067-189">Mac OS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="cb067-190"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span><span class="sxs-lookup"><span data-stu-id="cb067-190"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="cb067-191"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span><span class="sxs-lookup"><span data-stu-id="cb067-191"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="cb067-192"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span><span class="sxs-lookup"><span data-stu-id="cb067-192"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="cb067-193"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Unix Digital** (6)</span><span class="sxs-lookup"><span data-stu-id="cb067-193"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="cb067-194"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span><span class="sxs-lookup"><span data-stu-id="cb067-194"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="cb067-195">Abrir VMS</span><span class="sxs-lookup"><span data-stu-id="cb067-195">Open VMS</span></span>

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="cb067-196"><span id="HPUX"></span><span id="hpux"></span>HP **(8** )</span><span class="sxs-lookup"><span data-stu-id="cb067-196"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd>

<span data-ttu-id="cb067-197">HP-UX</span><span class="sxs-lookup"><span data-stu-id="cb067-197">HP-UX</span></span>

</dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="cb067-198"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span><span class="sxs-lookup"><span data-stu-id="cb067-198"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="cb067-199"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span><span class="sxs-lookup"><span data-stu-id="cb067-199"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="cb067-200"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span><span class="sxs-lookup"><span data-stu-id="cb067-200"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="cb067-201"><span id="OS_2"></span><span id="os_2"></span>**Sistema operacional/2** (12)</span><span class="sxs-lookup"><span data-stu-id="cb067-201"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="cb067-202"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span><span class="sxs-lookup"><span data-stu-id="cb067-202"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd>

<span data-ttu-id="cb067-203">VM (máquina virtual) da Microsoft para Java</span><span class="sxs-lookup"><span data-stu-id="cb067-203">Microsoft Virtual Machine (VM) for Java</span></span>

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="cb067-204"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span><span class="sxs-lookup"><span data-stu-id="cb067-204"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="cb067-205"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span><span class="sxs-lookup"><span data-stu-id="cb067-205"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd>

<span data-ttu-id="cb067-206">Windows 3. x</span><span class="sxs-lookup"><span data-stu-id="cb067-206">Windows 3.x</span></span>

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="cb067-207"><span id="WIN95"></span><span id="win95"></span>**Win95** (16)</span><span class="sxs-lookup"><span data-stu-id="cb067-207"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd>

<span data-ttu-id="cb067-208">Windows 95</span><span class="sxs-lookup"><span data-stu-id="cb067-208">Windows 95</span></span>

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="cb067-209"><span id="WIN98"></span><span id="win98"></span>**Win98** (17)</span><span class="sxs-lookup"><span data-stu-id="cb067-209"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd>

<span data-ttu-id="cb067-210">Windows 98</span><span class="sxs-lookup"><span data-stu-id="cb067-210">Windows 98</span></span>

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="cb067-211"><span id="WINNT"></span><span id="winnt"></span>**WinNT** (18)</span><span class="sxs-lookup"><span data-stu-id="cb067-211"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd>

<span data-ttu-id="cb067-212">Windows NT</span><span class="sxs-lookup"><span data-stu-id="cb067-212">Windows NT</span></span>

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="cb067-213"><span id="WINCE"></span><span id="wince"></span>**WinCE** (19)</span><span class="sxs-lookup"><span data-stu-id="cb067-213"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd>

<span data-ttu-id="cb067-214">Windows CE</span><span class="sxs-lookup"><span data-stu-id="cb067-214">Windows CE</span></span>

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="cb067-215"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span><span class="sxs-lookup"><span data-stu-id="cb067-215"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd>

<span data-ttu-id="cb067-216">NCR 3000</span><span class="sxs-lookup"><span data-stu-id="cb067-216">NCR 3000</span></span>

</dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="cb067-217"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span><span class="sxs-lookup"><span data-stu-id="cb067-217"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="cb067-218"><span id="OSF"></span><span id="osf"></span>**Uso** (22)</span><span class="sxs-lookup"><span data-stu-id="cb067-218"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="cb067-219"><span id="DC_OS"></span><span id="dc_os"></span>**DC/os** (23)</span><span class="sxs-lookup"><span data-stu-id="cb067-219"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="cb067-220"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Unix dependente** (24)</span><span class="sxs-lookup"><span data-stu-id="cb067-220"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="cb067-221"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span><span class="sxs-lookup"><span data-stu-id="cb067-221"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="cb067-222"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span><span class="sxs-lookup"><span data-stu-id="cb067-222"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="cb067-223"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Subsequentes** (27)</span><span class="sxs-lookup"><span data-stu-id="cb067-223"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="cb067-224"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span><span class="sxs-lookup"><span data-stu-id="cb067-224"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="cb067-225"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span><span class="sxs-lookup"><span data-stu-id="cb067-225"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="cb067-226"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span><span class="sxs-lookup"><span data-stu-id="cb067-226"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="cb067-227"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span><span class="sxs-lookup"><span data-stu-id="cb067-227"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="cb067-228"><span id="ASERIES"></span><span id="aseries"></span>**ASeries** (32)</span><span class="sxs-lookup"><span data-stu-id="cb067-228"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd>

<span data-ttu-id="cb067-229">Uma série</span><span class="sxs-lookup"><span data-stu-id="cb067-229">A Series</span></span>

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="cb067-230"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span><span class="sxs-lookup"><span data-stu-id="cb067-230"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd>

<span data-ttu-id="cb067-231">NSK tandem</span><span class="sxs-lookup"><span data-stu-id="cb067-231">Tandem NSK</span></span>

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="cb067-232"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span><span class="sxs-lookup"><span data-stu-id="cb067-232"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd>

<span data-ttu-id="cb067-233">NT em tandem</span><span class="sxs-lookup"><span data-stu-id="cb067-233">Tandem NT</span></span>

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="cb067-234"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span><span class="sxs-lookup"><span data-stu-id="cb067-234"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd>

<span data-ttu-id="cb067-235">BS2000/OSD</span><span class="sxs-lookup"><span data-stu-id="cb067-235">BS2000/OSD</span></span>

</dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="cb067-236"><span id="LINUX"></span><span id="linux"></span>**Linux** (36)</span><span class="sxs-lookup"><span data-stu-id="cb067-236"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="cb067-237"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span><span class="sxs-lookup"><span data-stu-id="cb067-237"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="cb067-238"><span id="XENIX"></span><span id="xenix"></span>**Xenix** (38)</span><span class="sxs-lookup"><span data-stu-id="cb067-238"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="cb067-239"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span><span class="sxs-lookup"><span data-stu-id="cb067-239"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="cb067-240"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Unix interativo** (40)</span><span class="sxs-lookup"><span data-stu-id="cb067-240"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="cb067-241"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span><span class="sxs-lookup"><span data-stu-id="cb067-241"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd>

<span data-ttu-id="cb067-242">BSD UNIX</span><span class="sxs-lookup"><span data-stu-id="cb067-242">BSD UNIX</span></span>

</dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="cb067-243"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span><span class="sxs-lookup"><span data-stu-id="cb067-243"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="cb067-244"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span><span class="sxs-lookup"><span data-stu-id="cb067-244"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="cb067-245"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span><span class="sxs-lookup"><span data-stu-id="cb067-245"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="cb067-246"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span><span class="sxs-lookup"><span data-stu-id="cb067-246"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd>

<span data-ttu-id="cb067-247">Mac OS 9</span><span class="sxs-lookup"><span data-stu-id="cb067-247">Mac OS 9</span></span>

</dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="cb067-248"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**Kernel Mach** (46)</span><span class="sxs-lookup"><span data-stu-id="cb067-248"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="cb067-249"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span><span class="sxs-lookup"><span data-stu-id="cb067-249"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="cb067-250"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span><span class="sxs-lookup"><span data-stu-id="cb067-250"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="cb067-251"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span><span class="sxs-lookup"><span data-stu-id="cb067-251"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="cb067-252"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span><span class="sxs-lookup"><span data-stu-id="cb067-252"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="cb067-253"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span><span class="sxs-lookup"><span data-stu-id="cb067-253"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="cb067-254"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**Menta** (52)</span><span class="sxs-lookup"><span data-stu-id="cb067-254"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="cb067-255"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span><span class="sxs-lookup"><span data-stu-id="cb067-255"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd>

<span data-ttu-id="cb067-256">Ser so</span><span class="sxs-lookup"><span data-stu-id="cb067-256">Be OS</span></span>

</dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="cb067-257"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span><span class="sxs-lookup"><span data-stu-id="cb067-257"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="cb067-258"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NEXTSTEP** (55)</span><span class="sxs-lookup"><span data-stu-id="cb067-258"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="cb067-259"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span><span class="sxs-lookup"><span data-stu-id="cb067-259"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd>

<span data-ttu-id="cb067-260">Sistema operacional Palm</span><span class="sxs-lookup"><span data-stu-id="cb067-260">Palm OS</span></span>

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="cb067-261"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span><span class="sxs-lookup"><span data-stu-id="cb067-261"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="cb067-262"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span><span class="sxs-lookup"><span data-stu-id="cb067-262"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="cb067-263"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicado** (59)</span><span class="sxs-lookup"><span data-stu-id="cb067-263"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="cb067-264"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span><span class="sxs-lookup"><span data-stu-id="cb067-264"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="cb067-265"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span><span class="sxs-lookup"><span data-stu-id="cb067-265"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="cb067-266">**Versão**</span><span class="sxs-lookup"><span data-stu-id="cb067-266">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb067-267">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="cb067-267">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cb067-268">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cb067-268">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cb067-269">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ softwareelement**](cim-softwareelement.md).**Version**"), [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Componente DMTF \| 1,3 ")</span><span class="sxs-lookup"><span data-stu-id="cb067-269">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Version**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="cb067-270">Versão da operação.</span><span class="sxs-lookup"><span data-stu-id="cb067-270">Version of the operation.</span></span>

<span data-ttu-id="cb067-271">A versão da operação deve estar em um dos seguintes formatos:</span><span class="sxs-lookup"><span data-stu-id="cb067-271">The version of the operation should be in one of the following forms:</span></span>

-   <span data-ttu-id="cb067-272"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="cb067-272"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="cb067-273"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="cb067-273"><major>.<minor><letter><revision></span></span>

<span data-ttu-id="cb067-274">Esta propriedade é herdada [**da \_ ação CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="cb067-274">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cb067-275">Comentários</span><span class="sxs-lookup"><span data-stu-id="cb067-275">Remarks</span></span>

<span data-ttu-id="cb067-276">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="cb067-276">WMI does not implement this class.</span></span>

<span data-ttu-id="cb067-277">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="cb067-277">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="cb067-278">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="cb067-278">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb067-279">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cb067-279">Requirements</span></span>



| <span data-ttu-id="cb067-280">Requisito</span><span class="sxs-lookup"><span data-stu-id="cb067-280">Requirement</span></span> | <span data-ttu-id="cb067-281">Valor</span><span class="sxs-lookup"><span data-stu-id="cb067-281">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cb067-282">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cb067-282">Minimum supported client</span></span><br/> | <span data-ttu-id="cb067-283">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cb067-283">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="cb067-284">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cb067-284">Minimum supported server</span></span><br/> | <span data-ttu-id="cb067-285">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cb067-285">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="cb067-286">Namespace</span><span class="sxs-lookup"><span data-stu-id="cb067-286">Namespace</span></span><br/>                | <span data-ttu-id="cb067-287">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="cb067-287">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="cb067-288">MOF</span><span class="sxs-lookup"><span data-stu-id="cb067-288">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cb067-289"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cb067-289"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="cb067-290">DLL</span><span class="sxs-lookup"><span data-stu-id="cb067-290">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cb067-291"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cb067-291"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb067-292">Confira também</span><span class="sxs-lookup"><span data-stu-id="cb067-292">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb067-293">**Ação de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="cb067-293">**CIM\_Action**</span></span>](cim-action.md)
</dt> </dl>

 

