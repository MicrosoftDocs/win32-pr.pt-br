---
description: A \_ classe de processo CIM representa uma única instância de um programa em execução. Um usuário normalmente vê um processo como um aplicativo ou uma tarefa.
ms.assetid: 8b00ef6e-5c7f-410c-9e48-1205ea6e5a4c
ms.tgt_platform: multiple
title: Classe CIM_Process
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Process
- CIM_Process.Caption
- CIM_Process.CreationClassName
- CIM_Process.CreationDate
- CIM_Process.CSCreationClassName
- CIM_Process.CSName
- CIM_Process.Description
- CIM_Process.ExecutionState
- CIM_Process.Handle
- CIM_Process.InstallDate
- CIM_Process.KernelModeTime
- CIM_Process.Name
- CIM_Process.OSCreationClassName
- CIM_Process.OSName
- CIM_Process.Priority
- CIM_Process.Status
- CIM_Process.TerminationDate
- CIM_Process.UserModeTime
- CIM_Process.WorkingSetSize
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 355e29929dc05a701a2beac0919a28aca573ca9c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920564"
---
# <a name="cim_process-class"></a><span data-ttu-id="c84a9-104">\_Classe de processo CIM</span><span class="sxs-lookup"><span data-stu-id="c84a9-104">CIM\_Process class</span></span>

<span data-ttu-id="c84a9-105">A classe de **\_ processo CIM** representa uma única instância de um programa em execução.</span><span class="sxs-lookup"><span data-stu-id="c84a9-105">The **CIM\_Process** class represents a single instance of a running program.</span></span> <span data-ttu-id="c84a9-106">Um usuário normalmente vê um processo como um aplicativo ou uma tarefa.</span><span class="sxs-lookup"><span data-stu-id="c84a9-106">A user typically sees a process as an application or task.</span></span> <span data-ttu-id="c84a9-107">Um processo é definido por um espaço de trabalho de recursos de memória e configurações ambientais que são alocados a ele.</span><span class="sxs-lookup"><span data-stu-id="c84a9-107">A process is defined by a workspace of memory resources and environmental settings that are allocated to it.</span></span> <span data-ttu-id="c84a9-108">Em um sistema multitarefa, o espaço de trabalho impede a invasão de recursos por outros processos.</span><span class="sxs-lookup"><span data-stu-id="c84a9-108">On a multitasking system, the workspace prevents intrusion of resources by other processes.</span></span> <span data-ttu-id="c84a9-109">Além disso, um processo pode ser executado como vários threads, todos executados no mesmo espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="c84a9-109">Additionally, a process can execute as multiple threads, all which run within the same workspace.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c84a9-110">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="c84a9-110">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="c84a9-111">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="c84a9-111">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="c84a9-112">A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="c84a9-112">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="c84a9-113">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="c84a9-113">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c84a9-114">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c84a9-114">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C566-5FBB-11D2-AAC1-006008C78BC7}"), DisplayName("Processes (CIM)"), AMENDMENT]
class CIM_Process : CIM_LogicalElement
{
  string   Caption;
  string   CreationClassName;
  datetime CreationDate;
  string   CSCreationClassName;
  string   CSName;
  string   Description;
  uint16   ExecutionState;
  string   Handle;
  datetime InstallDate;
  uint64   KernelModeTime;
  string   Name;
  string   OSCreationClassName;
  string   OSName;
  uint32   Priority;
  string   Status;
  datetime TerminationDate;
  uint64   UserModeTime;
  uint64   WorkingSetSize;
};
```

## <a name="members"></a><span data-ttu-id="c84a9-115">Membros</span><span class="sxs-lookup"><span data-stu-id="c84a9-115">Members</span></span>

<span data-ttu-id="c84a9-116">A classe de **\_ processo CIM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="c84a9-116">The **CIM\_Process** class has these types of members:</span></span>

-   [<span data-ttu-id="c84a9-117">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c84a9-117">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c84a9-118">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c84a9-118">Properties</span></span>

<span data-ttu-id="c84a9-119">A classe de **\_ processo CIM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="c84a9-119">The **CIM\_Process** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c84a9-120">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="c84a9-120">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c84a9-121">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c84a9-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c84a9-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c84a9-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c84a9-123">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="c84a9-123">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="c84a9-124">Breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="c84a9-124">Short textual description of the object.</span></span>

<span data-ttu-id="c84a9-125">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c84a9-125">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c84a9-126">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="c84a9-126">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c84a9-127">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c84a9-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c84a9-128">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c84a9-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c84a9-129">Qualificadores: [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("nome da classe")</span><span class="sxs-lookup"><span data-stu-id="c84a9-129">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="c84a9-130">Nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="c84a9-130">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="c84a9-131">Quando usado com outras propriedades de chave da classe, essa propriedade permite que todas as instâncias da classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="c84a9-131">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="c84a9-132">**CreationDate**</span><span class="sxs-lookup"><span data-stu-id="c84a9-132">**CreationDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c84a9-133">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c84a9-133">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c84a9-134">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c84a9-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c84a9-135">Qualificadores: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("CreationDate")</span><span class="sxs-lookup"><span data-stu-id="c84a9-135">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("CreationDate")</span></span>
</dt> </dl>

<span data-ttu-id="c84a9-136">Hora em que o processo começou a ser executado.</span><span class="sxs-lookup"><span data-stu-id="c84a9-136">Time that the process began executing.</span></span>

</dd> <dt>

<span data-ttu-id="c84a9-137">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="c84a9-137">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c84a9-138">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c84a9-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c84a9-139">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c84a9-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c84a9-140">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("sistema [**\_ operacional CIM**](cim-operatingsystem.md).**CSCreationClassName**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nome da classe do sistema de computador ")</span><span class="sxs-lookup"><span data-stu-id="c84a9-140">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**CSCreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Computer System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="c84a9-141">Nome da classe de criação do sistema do computador de escopo.</span><span class="sxs-lookup"><span data-stu-id="c84a9-141">Scoping computer system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="c84a9-142">**CSName**</span><span class="sxs-lookup"><span data-stu-id="c84a9-142">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c84a9-143">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c84a9-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c84a9-144">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c84a9-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c84a9-145">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("sistema [**\_ operacional CIM**](cim-operatingsystem.md).**CSName**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nome do sistema de computador ")</span><span class="sxs-lookup"><span data-stu-id="c84a9-145">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**CSName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Computer System Name")</span></span>
</dt> </dl>

<span data-ttu-id="c84a9-146">Nome do sistema do computador de escopo.</span><span class="sxs-lookup"><span data-stu-id="c84a9-146">Scoping computer system's name.</span></span>

</dd> <dt>

<span data-ttu-id="c84a9-147">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="c84a9-147">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c84a9-148">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c84a9-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c84a9-149">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c84a9-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c84a9-150">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="c84a9-150">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="c84a9-151">Descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="c84a9-151">Textual description of the object.</span></span>

<span data-ttu-id="c84a9-152">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c84a9-152">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c84a9-153">**ExecutionState**</span><span class="sxs-lookup"><span data-stu-id="c84a9-153">**ExecutionState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c84a9-154">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c84a9-154">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c84a9-155">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c84a9-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c84a9-156">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("estado de execução")</span><span class="sxs-lookup"><span data-stu-id="c84a9-156">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Execution State")</span></span>
</dt> </dl>

<span data-ttu-id="c84a9-157">Condição operacional atual do processo.</span><span class="sxs-lookup"><span data-stu-id="c84a9-157">Current operating condition of the process.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c84a9-158"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="c84a9-158"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="c84a9-159"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="c84a9-159"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Ready"></span><span id="ready"></span><span id="READY"></span>

<span data-ttu-id="c84a9-160"><span id="Ready"></span><span id="ready"></span><span id="READY"></span>**Pronto** (2)</span><span class="sxs-lookup"><span data-stu-id="c84a9-160"><span id="Ready"></span><span id="ready"></span><span id="READY"></span>**Ready** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="c84a9-161"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Em execução** (3)</span><span class="sxs-lookup"><span data-stu-id="c84a9-161"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Blocked"></span><span id="blocked"></span><span id="BLOCKED"></span>

<span data-ttu-id="c84a9-162"><span id="Blocked"></span><span id="blocked"></span><span id="BLOCKED"></span>**Bloqueado** (4)</span><span class="sxs-lookup"><span data-stu-id="c84a9-162"><span id="Blocked"></span><span id="blocked"></span><span id="BLOCKED"></span>**Blocked** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Suspended_Blocked"></span><span id="suspended_blocked"></span><span id="SUSPENDED_BLOCKED"></span>

<span data-ttu-id="c84a9-163"><span id="Suspended_Blocked"></span><span id="suspended_blocked"></span><span id="SUSPENDED_BLOCKED"></span>**Bloqueado suspenso** (5)</span><span class="sxs-lookup"><span data-stu-id="c84a9-163"><span id="Suspended_Blocked"></span><span id="suspended_blocked"></span><span id="SUSPENDED_BLOCKED"></span>**Suspended Blocked** (5)</span></span>


</dt> <dd>

<span data-ttu-id="c84a9-164">Bloqueado suspenso</span><span class="sxs-lookup"><span data-stu-id="c84a9-164">Suspended blocked</span></span>

</dd> <dt>

<span id="Suspended_Ready"></span><span id="suspended_ready"></span><span id="SUSPENDED_READY"></span>

<span data-ttu-id="c84a9-165"><span id="Suspended_Ready"></span><span id="suspended_ready"></span><span id="SUSPENDED_READY"></span>**Pronto suspenso** (6)</span><span class="sxs-lookup"><span data-stu-id="c84a9-165"><span id="Suspended_Ready"></span><span id="suspended_ready"></span><span id="SUSPENDED_READY"></span>**Suspended Ready** (6)</span></span>


</dt> <dd>

<span data-ttu-id="c84a9-166">Pronto suspenso</span><span class="sxs-lookup"><span data-stu-id="c84a9-166">Suspended ready</span></span>

</dd> <dt>

<span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>

<span data-ttu-id="c84a9-167"><span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>**Encerrado** (7)</span><span class="sxs-lookup"><span data-stu-id="c84a9-167"><span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>**Terminated** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>

<span data-ttu-id="c84a9-168"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Parado** (8)</span><span class="sxs-lookup"><span data-stu-id="c84a9-168"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Growing"></span><span id="growing"></span><span id="GROWING"></span>

<span data-ttu-id="c84a9-169"><span id="Growing"></span><span id="growing"></span><span id="GROWING"></span>**Crescendo** (9)</span><span class="sxs-lookup"><span data-stu-id="c84a9-169"><span id="Growing"></span><span id="growing"></span><span id="GROWING"></span>**Growing** (9)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c84a9-170">**Handle**</span><span class="sxs-lookup"><span data-stu-id="c84a9-170">**Handle**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c84a9-171">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c84a9-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c84a9-172">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c84a9-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c84a9-173">Qualificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Handle")</span><span class="sxs-lookup"><span data-stu-id="c84a9-173">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Handle")</span></span>
</dt> </dl>

<span data-ttu-id="c84a9-174">Identifica o processo.</span><span class="sxs-lookup"><span data-stu-id="c84a9-174">Identifies the process.</span></span> <span data-ttu-id="c84a9-175">Um identificador de processo é um tipo de identificador de processo.</span><span class="sxs-lookup"><span data-stu-id="c84a9-175">A process identifier is a kind of process handle.</span></span>

</dd> <dt>

<span data-ttu-id="c84a9-176">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="c84a9-176">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c84a9-177">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c84a9-177">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c84a9-178">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c84a9-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c84a9-179">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="c84a9-179">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="c84a9-180">Data e hora em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="c84a9-180">Date and time the object was installed.</span></span> <span data-ttu-id="c84a9-181">Essa propriedade não precisa de um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="c84a9-181">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="c84a9-182">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c84a9-182">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c84a9-183">**KernelModeTime**</span><span class="sxs-lookup"><span data-stu-id="c84a9-183">**KernelModeTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c84a9-184">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c84a9-184">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c84a9-185">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c84a9-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c84a9-186">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("tempo do modelo do kernel"), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("milissegundos")</span><span class="sxs-lookup"><span data-stu-id="c84a9-186">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Kernel Model Time"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliseconds")</span></span>
</dt> </dl>

<span data-ttu-id="c84a9-187">Tempo no modo kernel, em unidades de 100 nanossegundos.</span><span class="sxs-lookup"><span data-stu-id="c84a9-187">Time in kernel mode, in 100 nanosecond units.</span></span> <span data-ttu-id="c84a9-188">Se essas informações não estiverem disponíveis, um valor de 0 (zero) deverá ser usado.</span><span class="sxs-lookup"><span data-stu-id="c84a9-188">If this information is not available, a value of 0 (zero) should be used.</span></span>

<span data-ttu-id="c84a9-189">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="c84a9-189">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="c84a9-190">**Nome**</span><span class="sxs-lookup"><span data-stu-id="c84a9-190">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c84a9-191">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c84a9-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c84a9-192">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c84a9-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c84a9-193">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="c84a9-193">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="c84a9-194">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="c84a9-194">Label by which the object is known.</span></span> <span data-ttu-id="c84a9-195">Quando em uma subclasse, essa propriedade pode ser substituída como uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="c84a9-195">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="c84a9-196">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c84a9-196">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c84a9-197">**OSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="c84a9-197">**OSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c84a9-198">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c84a9-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c84a9-199">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c84a9-199">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c84a9-200">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("sistema [**\_ operacional CIM**](cim-operatingsystem.md).**CreationClassName**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nome da classe do sistema operacional ")</span><span class="sxs-lookup"><span data-stu-id="c84a9-200">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Operating System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="c84a9-201">Nome da classe de criação do sistema operacional do escopo.</span><span class="sxs-lookup"><span data-stu-id="c84a9-201">Scoping operating system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="c84a9-202">**OSName**</span><span class="sxs-lookup"><span data-stu-id="c84a9-202">**OSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c84a9-203">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c84a9-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c84a9-204">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c84a9-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c84a9-205">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("sistema [**\_ operacional CIM**](cim-operatingsystem.md).**Name**"), [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nome do sistema operacional ")</span><span class="sxs-lookup"><span data-stu-id="c84a9-205">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Operating System Name")</span></span>
</dt> </dl>

<span data-ttu-id="c84a9-206">Nome do sistema operacional do escopo.</span><span class="sxs-lookup"><span data-stu-id="c84a9-206">Scoping operating system's name.</span></span>

</dd> <dt>

<span data-ttu-id="c84a9-207">**Prioridade**</span><span class="sxs-lookup"><span data-stu-id="c84a9-207">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c84a9-208">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c84a9-208">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c84a9-209">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c84a9-209">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c84a9-210">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Priority")</span><span class="sxs-lookup"><span data-stu-id="c84a9-210">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Priority")</span></span>
</dt> </dl>

<span data-ttu-id="c84a9-211">Urgência ou importância para a execução do processo.</span><span class="sxs-lookup"><span data-stu-id="c84a9-211">Urgency or importance for process execution.</span></span> <span data-ttu-id="c84a9-212">Se uma prioridade não for definida para um processo, um valor de 0 (zero) deverá ser usado.</span><span class="sxs-lookup"><span data-stu-id="c84a9-212">If a priority is not defined for a process, a value of 0 (zero) should be used.</span></span>

</dd> <dt>

<span data-ttu-id="c84a9-213">**Status**</span><span class="sxs-lookup"><span data-stu-id="c84a9-213">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c84a9-214">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c84a9-214">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c84a9-215">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c84a9-215">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c84a9-216">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="c84a9-216">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="c84a9-217">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="c84a9-217">Current status of the object.</span></span>

<span data-ttu-id="c84a9-218">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c84a9-218">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="c84a9-219">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="c84a9-219">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="c84a9-220">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="c84a9-220">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="c84a9-221">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="c84a9-221">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="c84a9-222">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="c84a9-222">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c84a9-223">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="c84a9-223">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="c84a9-224">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="c84a9-224">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="c84a9-225">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="c84a9-225">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="c84a9-226">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="c84a9-226">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="c84a9-227">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="c84a9-227">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="c84a9-228">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="c84a9-228">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="c84a9-229">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="c84a9-229">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="c84a9-230">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="c84a9-230">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="c84a9-231">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="c84a9-231">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c84a9-232">**TerminationDate**</span><span class="sxs-lookup"><span data-stu-id="c84a9-232">**TerminationDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c84a9-233">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c84a9-233">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c84a9-234">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c84a9-234">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c84a9-235">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("data de término")</span><span class="sxs-lookup"><span data-stu-id="c84a9-235">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Termination Date")</span></span>
</dt> </dl>

<span data-ttu-id="c84a9-236">Hora em que o processo foi interrompido ou encerrado.</span><span class="sxs-lookup"><span data-stu-id="c84a9-236">Time that the process was stopped or terminated.</span></span>

</dd> <dt>

<span data-ttu-id="c84a9-237">**Usermodetime**</span><span class="sxs-lookup"><span data-stu-id="c84a9-237">**UserModeTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c84a9-238">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c84a9-238">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c84a9-239">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c84a9-239">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c84a9-240">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("tempo de modo de usuário"), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("milissegundos")</span><span class="sxs-lookup"><span data-stu-id="c84a9-240">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("User Mode Time"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliseconds")</span></span>
</dt> </dl>

<span data-ttu-id="c84a9-241">Tempo no modo de usuário, em unidades de 100 nanossegundos.</span><span class="sxs-lookup"><span data-stu-id="c84a9-241">Time in user mode, in 100 nanosecond units.</span></span> <span data-ttu-id="c84a9-242">Se essas informações não estiverem disponíveis, um valor de 0 (zero) deverá ser usado.</span><span class="sxs-lookup"><span data-stu-id="c84a9-242">If this information is not available, a value of 0 (zero) should be used.</span></span>

<span data-ttu-id="c84a9-243">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="c84a9-243">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="c84a9-244">**WorkingSetSize**</span><span class="sxs-lookup"><span data-stu-id="c84a9-244">**WorkingSetSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c84a9-245">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c84a9-245">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c84a9-246">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c84a9-246">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c84a9-247">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("tamanho do conjunto de trabalho"), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="c84a9-247">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Working Set Size"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="c84a9-248">Quantidade de memória, em bytes, que um processo precisa para ser executado com eficiência para um sistema operacional que usa o gerenciamento de memória baseado em página.</span><span class="sxs-lookup"><span data-stu-id="c84a9-248">Amount of memory, in bytes, that a process needs to execute efficiently for an operating system that uses page-based memory management.</span></span> <span data-ttu-id="c84a9-249">Se o sistema não tiver memória suficiente (menos que o tamanho do conjunto de trabalho), ultrapaginação ocorrerá.</span><span class="sxs-lookup"><span data-stu-id="c84a9-249">If the system does not have enough memory (less than the working set size), thrashing occurs.</span></span> <span data-ttu-id="c84a9-250">Se o tamanho do conjunto de trabalho não for conhecido, use **NULL** ou 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="c84a9-250">If the size of the working set is not known, use **NULL** or 0 (zero).</span></span> <span data-ttu-id="c84a9-251">Se os dados do conjunto de trabalho forem fornecidos, você poderá monitorar as informações para entender os requisitos de memória em constante mudança de um processo.</span><span class="sxs-lookup"><span data-stu-id="c84a9-251">If working set data is provided, you can monitor the information to understand the changing memory requirements of a process.</span></span>

<span data-ttu-id="c84a9-252">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="c84a9-252">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c84a9-253">Comentários</span><span class="sxs-lookup"><span data-stu-id="c84a9-253">Remarks</span></span>

<span data-ttu-id="c84a9-254">A classe de **\_ processo CIM** é derivada de [**CIM \_ LogicalElement**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="c84a9-254">The **CIM\_Process** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="c84a9-255">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="c84a9-255">WMI does not implement this class.</span></span> <span data-ttu-id="c84a9-256">Para classes WMI derivadas do **\_ processo CIM**, consulte [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="c84a9-256">For WMI classes derived from **CIM\_Process**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="c84a9-257">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="c84a9-257">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="c84a9-258">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="c84a9-258">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="c84a9-259">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c84a9-259">Requirements</span></span>



| <span data-ttu-id="c84a9-260">Requisito</span><span class="sxs-lookup"><span data-stu-id="c84a9-260">Requirement</span></span> | <span data-ttu-id="c84a9-261">Valor</span><span class="sxs-lookup"><span data-stu-id="c84a9-261">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c84a9-262">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c84a9-262">Minimum supported client</span></span><br/> | <span data-ttu-id="c84a9-263">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c84a9-263">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c84a9-264">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c84a9-264">Minimum supported server</span></span><br/> | <span data-ttu-id="c84a9-265">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c84a9-265">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c84a9-266">Namespace</span><span class="sxs-lookup"><span data-stu-id="c84a9-266">Namespace</span></span><br/>                | <span data-ttu-id="c84a9-267">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="c84a9-267">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c84a9-268">MOF</span><span class="sxs-lookup"><span data-stu-id="c84a9-268">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c84a9-269"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c84a9-269"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c84a9-270">DLL</span><span class="sxs-lookup"><span data-stu-id="c84a9-270">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c84a9-271"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c84a9-271"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c84a9-272">Confira também</span><span class="sxs-lookup"><span data-stu-id="c84a9-272">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c84a9-273">**CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="c84a9-273">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

