---
description: A \_ classe de thread CIM representa a capacidade de executar unidades de um processo ou tarefa, em paralelo. Um processo pode ter muitos threads, cada um dos quais é fraco para o processo.
ms.assetid: 57222d57-61bd-4641-a77c-805263be04b7
ms.tgt_platform: multiple
title: Classe CIM_Thread
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Thread
- CIM_Thread.Caption
- CIM_Thread.CreationClassName
- CIM_Thread.CSCreationClassName
- CIM_Thread.CSName
- CIM_Thread.Description
- CIM_Thread.ExecutionState
- CIM_Thread.Handle
- CIM_Thread.InstallDate
- CIM_Thread.KernelModeTime
- CIM_Thread.Name
- CIM_Thread.OSCreationClassName
- CIM_Thread.OSName
- CIM_Thread.Priority
- CIM_Thread.ProcessCreationClassName
- CIM_Thread.ProcessHandle
- CIM_Thread.Status
- CIM_Thread.UserModeTime
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e0a69554ef50a82695d2904b11f4189c3aab11b7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756258"
---
# <a name="cim_thread-class"></a><span data-ttu-id="bb597-104">\_Classe de thread CIM</span><span class="sxs-lookup"><span data-stu-id="bb597-104">CIM\_Thread class</span></span>

<span data-ttu-id="bb597-105">A classe de **\_ thread CIM** representa a capacidade de executar unidades de um processo ou tarefa, em paralelo.</span><span class="sxs-lookup"><span data-stu-id="bb597-105">The **CIM\_Thread** class represents the ability to execute units of a process or task, in parallel.</span></span> <span data-ttu-id="bb597-106">Um processo pode ter muitos threads, cada um dos quais é fraco para o processo.</span><span class="sxs-lookup"><span data-stu-id="bb597-106">A process can have many threads, each of which is weak to the process.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="bb597-107">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="bb597-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="bb597-108">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="bb597-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="bb597-109">A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="bb597-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="bb597-110">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="bb597-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb597-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bb597-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C571-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_Thread : CIM_LogicalElement
{
  string   Caption;
  string   CreationClassName;
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
  string   ProcessCreationClassName;
  string   ProcessHandle;
  string   Status;
  uint64   UserModeTime;
};
```

## <a name="members"></a><span data-ttu-id="bb597-112">Membros</span><span class="sxs-lookup"><span data-stu-id="bb597-112">Members</span></span>

<span data-ttu-id="bb597-113">A classe de **\_ thread CIM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="bb597-113">The **CIM\_Thread** class has these types of members:</span></span>

-   [<span data-ttu-id="bb597-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="bb597-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bb597-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="bb597-115">Properties</span></span>

<span data-ttu-id="bb597-116">A classe de **\_ thread CIM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="bb597-116">The **CIM\_Thread** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bb597-117">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="bb597-117">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb597-118">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="bb597-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bb597-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bb597-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bb597-120">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="bb597-120">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="bb597-121">Breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="bb597-121">Short textual description of the object.</span></span>

<span data-ttu-id="bb597-122">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="bb597-122">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="bb597-123">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="bb597-123">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb597-124">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="bb597-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bb597-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bb597-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bb597-126">Qualificadores: [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="bb597-126">Qualifiers: [**Cim\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="bb597-127">Nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="bb597-127">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="bb597-128">Quando usado com outras propriedades de chave da classe, essa propriedade permite que todas as instâncias da classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="bb597-128">When used with other key properties of the class, this property allow all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="bb597-129">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="bb597-129">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb597-130">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="bb597-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bb597-131">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bb597-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bb597-132">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ processo CIM**](cim-process.md).**CSCreationClassName**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="bb597-132">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Process**](cim-process.md).**CSCreationClassName**"), [**Cim\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="bb597-133">Nome da classe de criação do sistema do computador de escopo.</span><span class="sxs-lookup"><span data-stu-id="bb597-133">Scoping computer system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="bb597-134">**CSName**</span><span class="sxs-lookup"><span data-stu-id="bb597-134">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb597-135">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="bb597-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bb597-136">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bb597-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bb597-137">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ processo CIM**](cim-process.md).**CSName**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="bb597-137">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Process**](cim-process.md).**CSName**"), [**Cim\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="bb597-138">Nome do sistema do computador de escopo.</span><span class="sxs-lookup"><span data-stu-id="bb597-138">Scoping computer system's name.</span></span>

</dd> <dt>

<span data-ttu-id="bb597-139">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="bb597-139">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb597-140">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="bb597-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bb597-141">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bb597-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bb597-142">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="bb597-142">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="bb597-143">Descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="bb597-143">Textual description of the object.</span></span>

<span data-ttu-id="bb597-144">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="bb597-144">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="bb597-145">**ExecutionState**</span><span class="sxs-lookup"><span data-stu-id="bb597-145">**ExecutionState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb597-146">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bb597-146">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bb597-147">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bb597-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bb597-148">Indica a condição operacional atual do thread.</span><span class="sxs-lookup"><span data-stu-id="bb597-148">Indicates the current operating condition of the thread.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="bb597-149">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="bb597-149">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="bb597-150">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="bb597-150">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Ready"></span><span id="ready"></span><span id="READY"></span>

<span data-ttu-id="bb597-151">**Pronto** (2)</span><span class="sxs-lookup"><span data-stu-id="bb597-151">**Ready** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="bb597-152">**Em execução** (3)</span><span class="sxs-lookup"><span data-stu-id="bb597-152">**Running** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Blocked"></span><span id="blocked"></span><span id="BLOCKED"></span>

<span data-ttu-id="bb597-153">**Bloqueado** (4)</span><span class="sxs-lookup"><span data-stu-id="bb597-153">**Blocked** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Suspended_Blocked"></span><span id="suspended_blocked"></span><span id="SUSPENDED_BLOCKED"></span>

<span data-ttu-id="bb597-154">**Bloqueado suspenso** (5)</span><span class="sxs-lookup"><span data-stu-id="bb597-154">**Suspended Blocked** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Suspended_Ready"></span><span id="suspended_ready"></span><span id="SUSPENDED_READY"></span>

<span data-ttu-id="bb597-155">**Pronto suspenso** (6)</span><span class="sxs-lookup"><span data-stu-id="bb597-155">**Suspended Ready** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="bb597-156">**Handle**</span><span class="sxs-lookup"><span data-stu-id="bb597-156">**Handle**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb597-157">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="bb597-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bb597-158">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bb597-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bb597-159">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="bb597-159">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="bb597-160">Identificador para o thread.</span><span class="sxs-lookup"><span data-stu-id="bb597-160">Identifier for the thread.</span></span>

</dd> <dt>

<span data-ttu-id="bb597-161">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="bb597-161">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb597-162">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="bb597-162">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="bb597-163">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bb597-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bb597-164">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="bb597-164">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="bb597-165">Data e hora em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="bb597-165">Date and time the object was installed.</span></span> <span data-ttu-id="bb597-166">Essa propriedade não precisa de um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="bb597-166">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="bb597-167">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="bb597-167">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="bb597-168">**KernelModeTime**</span><span class="sxs-lookup"><span data-stu-id="bb597-168">**KernelModeTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb597-169">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="bb597-169">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="bb597-170">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bb597-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bb597-171">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("milissegundos")</span><span class="sxs-lookup"><span data-stu-id="bb597-171">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliseconds")</span></span>
</dt> </dl>

<span data-ttu-id="bb597-172">Tempo, em modo kernel, em unidades de 100 nanossegundos.</span><span class="sxs-lookup"><span data-stu-id="bb597-172">Time, in kernel mode, in 100 nanosecond units.</span></span> <span data-ttu-id="bb597-173">Se essas informações não estiverem disponíveis, um valor de 0 (zero) deverá ser usado.</span><span class="sxs-lookup"><span data-stu-id="bb597-173">If this information is not available, a value of 0 (zero) should be used.</span></span>

<span data-ttu-id="bb597-174">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="bb597-174">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="bb597-175">**Nome**</span><span class="sxs-lookup"><span data-stu-id="bb597-175">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb597-176">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="bb597-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bb597-177">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bb597-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bb597-178">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="bb597-178">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="bb597-179">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="bb597-179">Label by which the object is known.</span></span> <span data-ttu-id="bb597-180">Quando em uma subclasse, essa propriedade pode ser substituída como uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="bb597-180">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="bb597-181">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="bb597-181">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="bb597-182">**OSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="bb597-182">**OSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb597-183">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="bb597-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bb597-184">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bb597-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bb597-185">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ processo CIM**](cim-process.md).**OSCreationClassName**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="bb597-185">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Process**](cim-process.md).**OSCreationClassName**"), [**Cim\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="bb597-186">Nome da classe de criação do sistema operacional do escopo.</span><span class="sxs-lookup"><span data-stu-id="bb597-186">Scoping operating system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="bb597-187">**OSName**</span><span class="sxs-lookup"><span data-stu-id="bb597-187">**OSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb597-188">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="bb597-188">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bb597-189">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bb597-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bb597-190">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ processo CIM**](cim-process.md).**OSName**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="bb597-190">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Process**](cim-process.md).**OSName**"), [**Cim\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="bb597-191">Nome do sistema operacional do escopo.</span><span class="sxs-lookup"><span data-stu-id="bb597-191">Scoping operating system's name.</span></span>

</dd> <dt>

<span data-ttu-id="bb597-192">**Prioridade**</span><span class="sxs-lookup"><span data-stu-id="bb597-192">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb597-193">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bb597-193">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bb597-194">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bb597-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bb597-195">Urgência para a execução de um thread.</span><span class="sxs-lookup"><span data-stu-id="bb597-195">Urgency for execution of a thread.</span></span> <span data-ttu-id="bb597-196">Um thread pode ter uma prioridade diferente do seu processo de propriedade.</span><span class="sxs-lookup"><span data-stu-id="bb597-196">A thread can have a different priority than its owning process.</span></span> <span data-ttu-id="bb597-197">Se essas informações não estiverem disponíveis para um thread, um valor de 0 (zero) deverá ser usado.</span><span class="sxs-lookup"><span data-stu-id="bb597-197">If this information is not available for a thread, a value of 0 (zero) should be used.</span></span>

</dd> <dt>

<span data-ttu-id="bb597-198">**ProcessCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="bb597-198">**ProcessCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb597-199">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="bb597-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bb597-200">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bb597-200">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bb597-201">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ processo CIM**](cim-process.md).**CreationClassName**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="bb597-201">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Process**](cim-process.md).**CreationClassName**"), [**Cim\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="bb597-202">Nome da classe de criação do processo de escopo.</span><span class="sxs-lookup"><span data-stu-id="bb597-202">Scoping process's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="bb597-203">**ProcessHandle**</span><span class="sxs-lookup"><span data-stu-id="bb597-203">**ProcessHandle**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb597-204">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="bb597-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bb597-205">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bb597-205">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bb597-206">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ processo CIM**](cim-process.md).**Handle**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="bb597-206">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Process**](cim-process.md).**Handle**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="bb597-207">Identificador do processo de escopo.</span><span class="sxs-lookup"><span data-stu-id="bb597-207">Scoping process's handle.</span></span>

</dd> <dt>

<span data-ttu-id="bb597-208">**Status**</span><span class="sxs-lookup"><span data-stu-id="bb597-208">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb597-209">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="bb597-209">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bb597-210">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bb597-210">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bb597-211">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="bb597-211">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="bb597-212">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="bb597-212">Current status of the object.</span></span> <span data-ttu-id="bb597-213">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="bb597-213">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="bb597-214">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="bb597-214">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="bb597-215">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="bb597-215">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="bb597-216">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="bb597-216">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="bb597-217">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="bb597-217">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="bb597-218">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="bb597-218">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="bb597-219">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="bb597-219">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="bb597-220">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="bb597-220">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="bb597-221">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="bb597-221">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="bb597-222">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="bb597-222">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="bb597-223">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="bb597-223">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="bb597-224">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="bb597-224">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="bb597-225">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="bb597-225">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="bb597-226">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="bb597-226">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="bb597-227">**Usermodetime**</span><span class="sxs-lookup"><span data-stu-id="bb597-227">**UserModeTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb597-228">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="bb597-228">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="bb597-229">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bb597-229">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bb597-230">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("milissegundos")</span><span class="sxs-lookup"><span data-stu-id="bb597-230">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliseconds")</span></span>
</dt> </dl>

<span data-ttu-id="bb597-231">Tempo, no modo de usuário, em unidades de 100 nanossegundos.</span><span class="sxs-lookup"><span data-stu-id="bb597-231">Time, in user mode, in 100 nanosecond units.</span></span> <span data-ttu-id="bb597-232">Se essas informações não estiverem disponíveis, um valor de 0 (zero) deverá ser usado.</span><span class="sxs-lookup"><span data-stu-id="bb597-232">If this information is not available, a value of 0 (zero) should be used.</span></span>

<span data-ttu-id="bb597-233">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="bb597-233">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bb597-234">Comentários</span><span class="sxs-lookup"><span data-stu-id="bb597-234">Remarks</span></span>

<span data-ttu-id="bb597-235">A classe de **\_ thread CIM** é derivada de [**CIM \_ LogicalElement**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="bb597-235">The **CIM\_Thread** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="bb597-236">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="bb597-236">WMI does not implement this class.</span></span> <span data-ttu-id="bb597-237">Para classes WMI derivadas do **\_ thread CIM**, consulte [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="bb597-237">For WMI classes derived from **CIM\_Thread**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="bb597-238">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="bb597-238">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="bb597-239">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="bb597-239">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb597-240">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bb597-240">Requirements</span></span>



| <span data-ttu-id="bb597-241">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb597-241">Requirement</span></span> | <span data-ttu-id="bb597-242">Valor</span><span class="sxs-lookup"><span data-stu-id="bb597-242">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bb597-243">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bb597-243">Minimum supported client</span></span><br/> | <span data-ttu-id="bb597-244">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bb597-244">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="bb597-245">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bb597-245">Minimum supported server</span></span><br/> | <span data-ttu-id="bb597-246">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bb597-246">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="bb597-247">Namespace</span><span class="sxs-lookup"><span data-stu-id="bb597-247">Namespace</span></span><br/>                | <span data-ttu-id="bb597-248">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="bb597-248">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="bb597-249">MOF</span><span class="sxs-lookup"><span data-stu-id="bb597-249">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bb597-250"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bb597-250"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="bb597-251">DLL</span><span class="sxs-lookup"><span data-stu-id="bb597-251">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bb597-252"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bb597-252"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb597-253">Confira também</span><span class="sxs-lookup"><span data-stu-id="bb597-253">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb597-254">**CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="bb597-254">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

