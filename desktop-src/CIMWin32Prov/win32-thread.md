---
description: O \_ Thread Win32&\# 8194; A classe WMI representa um thread de execução.
ms.assetid: a284616c-1977-441a-9173-dff4f56b2d39
ms.tgt_platform: multiple
title: Classe Win32_Thread
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Thread
- Win32_Thread.Caption
- Win32_Thread.CreationClassName
- Win32_Thread.CSCreationClassName
- Win32_Thread.CSName
- Win32_Thread.Description
- Win32_Thread.ElapsedTime
- Win32_Thread.ExecutionState
- Win32_Thread.Handle
- Win32_Thread.InstallDate
- Win32_Thread.KernelModeTime
- Win32_Thread.Name
- Win32_Thread.OSCreationClassName
- Win32_Thread.OSName
- Win32_Thread.Priority
- Win32_Thread.PriorityBase
- Win32_Thread.ProcessCreationClassName
- Win32_Thread.ProcessHandle
- Win32_Thread.StartAddress
- Win32_Thread.Status
- Win32_Thread.ThreadState
- Win32_Thread.ThreadWaitReason
- Win32_Thread.UserModeTime
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6e9f6a8c821aa327e8b810b634c85bb06459910f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105750175"
---
# <a name="win32_thread-class"></a><span data-ttu-id="4f926-103">\_Classe de Thread Win32</span><span class="sxs-lookup"><span data-stu-id="4f926-103">Win32\_Thread class</span></span>

<span data-ttu-id="4f926-104">A  [classe WMI](../wmisdk/retrieving-a-class.md) de **\_ thread do Win32** representa um thread de execução.</span><span class="sxs-lookup"><span data-stu-id="4f926-104">The **Win32\_Thread** [WMI class](../wmisdk/retrieving-a-class.md) represents a thread of execution.</span></span> <span data-ttu-id="4f926-105">Embora um processo deva ter um thread de execução, o processo pode criar outros threads para executar tarefas em paralelo.</span><span class="sxs-lookup"><span data-stu-id="4f926-105">While a process must have one thread of execution, the process can create other threads to execute tasks in parallel.</span></span> <span data-ttu-id="4f926-106">Os threads compartilham o ambiente de processo, assim, vários threads no mesmo processo usam menos memória do que o mesmo número de processos.</span><span class="sxs-lookup"><span data-stu-id="4f926-106">Threads share the process environment, thus multiple threads under the same process use less memory than the same number of processes.</span></span>

<span data-ttu-id="4f926-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="4f926-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="4f926-108">As propriedades e os métodos estão em ordem alfabética, não em ordem de MOF.</span><span class="sxs-lookup"><span data-stu-id="4f926-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f926-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4f926-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4DD-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_Thread : CIM_Thread
{
  string   Caption;
  string   CreationClassName;
  string   CSCreationClassName;
  string   CSName;
  string   Description;
  uint64   ElapsedTime;
  uint16   ExecutionState;
  string   Handle;
  datetime InstallDate;
  uint64   KernelModeTime;
  string   Name;
  string   OSCreationClassName;
  string   OSName;
  uint32   Priority;
  uint32   PriorityBase;
  string   ProcessCreationClassName;
  string   ProcessHandle;
  uint32   StartAddress;
  string   Status;
  uint32   ThreadState;
  uint32   ThreadWaitReason;
  uint64   UserModeTime;
};
```

## <a name="members"></a><span data-ttu-id="4f926-110">Membros</span><span class="sxs-lookup"><span data-stu-id="4f926-110">Members</span></span>

<span data-ttu-id="4f926-111">A **classe \_ thread do Win32** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="4f926-111">The **Win32\_Thread** class has these types of members:</span></span>

-   [<span data-ttu-id="4f926-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="4f926-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4f926-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="4f926-113">Properties</span></span>

<span data-ttu-id="4f926-114">A **classe \_ thread do Win32** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="4f926-114">The **Win32\_Thread** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4f926-115">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="4f926-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f926-116">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="4f926-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4f926-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4f926-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f926-118">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="4f926-118">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="4f926-119">Breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="4f926-119">Short description of the object.</span></span>

<span data-ttu-id="4f926-120">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="4f926-120">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4f926-121">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="4f926-121">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f926-122">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="4f926-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4f926-123">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4f926-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f926-124">Qualificadores: [**\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="4f926-124">Qualifiers: [**Cim\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="4f926-125">Nome da primeira classe concreta a ser exibida na cadeia de herança usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="4f926-125">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="4f926-126">Quando usado com as outras propriedades de chave da classe, essa propriedade permite que todas as instâncias dessa classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="4f926-126">When used with the other key properties of the class, this property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="4f926-127">Essa propriedade é herdada [**do \_ thread CIM**](cim-thread.md).</span><span class="sxs-lookup"><span data-stu-id="4f926-127">This property is inherited from [**CIM\_Thread**](cim-thread.md).</span></span>

</dd> <dt>

<span data-ttu-id="4f926-128">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="4f926-128">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f926-129">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="4f926-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4f926-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4f926-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f926-131">Qualificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ processo CIM**](cim-process.md).**CSCreationClassName**"), [**\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="4f926-131">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Process**](cim-process.md).**CSCreationClassName**"), [**Cim\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="4f926-132">Nome da classe de criação do sistema de computador de escopo.</span><span class="sxs-lookup"><span data-stu-id="4f926-132">Creation class name of the scoping computer system.</span></span>

<span data-ttu-id="4f926-133">Essa propriedade é herdada [**do \_ thread CIM**](cim-thread.md).</span><span class="sxs-lookup"><span data-stu-id="4f926-133">This property is inherited from [**CIM\_Thread**](cim-thread.md).</span></span>

</dd> <dt>

<span data-ttu-id="4f926-134">**CSName**</span><span class="sxs-lookup"><span data-stu-id="4f926-134">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f926-135">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="4f926-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4f926-136">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4f926-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f926-137">Qualificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ processo CIM**](cim-process.md).**CSName**"), [**\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="4f926-137">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Process**](cim-process.md).**CSName**"), [**Cim\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="4f926-138">Nome do sistema de computador de escopo.</span><span class="sxs-lookup"><span data-stu-id="4f926-138">Name of the scoping computer system.</span></span>

<span data-ttu-id="4f926-139">Essa propriedade é herdada [**do \_ thread CIM**](cim-thread.md).</span><span class="sxs-lookup"><span data-stu-id="4f926-139">This property is inherited from [**CIM\_Thread**](cim-thread.md).</span></span>

</dd> <dt>

<span data-ttu-id="4f926-140">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="4f926-140">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f926-141">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="4f926-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4f926-142">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4f926-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f926-143">Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="4f926-143">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="4f926-144">Descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="4f926-144">Description of the object.</span></span>

<span data-ttu-id="4f926-145">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="4f926-145">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4f926-146">**ElapsedTime**</span><span class="sxs-lookup"><span data-stu-id="4f926-146">**ElapsedTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f926-147">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="4f926-147">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4f926-148">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4f926-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f926-149">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api de \| dados de desempenho de estruturas \| [**PerfTime de \_ \_ tipo de objeto**](/windows/win32/api/winperf/ns-winperf-perf_object_type) \| "), [**unidades**](../wmisdk/standard-qualifiers.md) ("milissegundos")</span><span class="sxs-lookup"><span data-stu-id="4f926-149">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Performance Data Structures\|[**PERF\_OBJECT\_TYPE**](/windows/win32/api/winperf/ns-winperf-perf_object_type)\|PerfTime"), [**Units**](../wmisdk/standard-qualifiers.md) ("milliseconds")</span></span>
</dt> </dl>

<span data-ttu-id="4f926-150">Tempo de execução total, em milissegundos, fornecido para esse thread desde sua criação.</span><span class="sxs-lookup"><span data-stu-id="4f926-150">Total execution time, in milliseconds, given to this thread since its creation.</span></span>

<span data-ttu-id="4f926-151">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="4f926-151">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="4f926-152">**ExecutionState**</span><span class="sxs-lookup"><span data-stu-id="4f926-152">**ExecutionState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f926-153">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4f926-153">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4f926-154">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4f926-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f926-155">Condição operacional atual do thread.</span><span class="sxs-lookup"><span data-stu-id="4f926-155">Current operating condition of the thread.</span></span>

<span data-ttu-id="4f926-156">Essa propriedade é herdada [**do \_ thread CIM**](cim-thread.md).</span><span class="sxs-lookup"><span data-stu-id="4f926-156">This property is inherited from [**CIM\_Thread**](cim-thread.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4f926-157">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="4f926-157">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="4f926-158">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="4f926-158">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Ready"></span><span id="ready"></span><span id="READY"></span>

<span data-ttu-id="4f926-159">**Pronto** (2)</span><span class="sxs-lookup"><span data-stu-id="4f926-159">**Ready** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="4f926-160">**Em execução** (3)</span><span class="sxs-lookup"><span data-stu-id="4f926-160">**Running** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Blocked"></span><span id="blocked"></span><span id="BLOCKED"></span>

<span data-ttu-id="4f926-161">**Bloqueado** (4)</span><span class="sxs-lookup"><span data-stu-id="4f926-161">**Blocked** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Suspended_Blocked"></span><span id="suspended_blocked"></span><span id="SUSPENDED_BLOCKED"></span>

<span data-ttu-id="4f926-162">**Bloqueado suspenso** (5)</span><span class="sxs-lookup"><span data-stu-id="4f926-162">**Suspended Blocked** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Suspended_Ready"></span><span id="suspended_ready"></span><span id="SUSPENDED_READY"></span>

<span data-ttu-id="4f926-163">**Pronto suspenso** (6)</span><span class="sxs-lookup"><span data-stu-id="4f926-163">**Suspended Ready** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4f926-164">**Handle**</span><span class="sxs-lookup"><span data-stu-id="4f926-164">**Handle**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f926-165">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="4f926-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4f926-166">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4f926-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f926-167">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**substitua**](../wmisdk/standard-qualifiers.md) ("Handle"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api de \| ferramentas de ajuda da ferramenta \| [**THREADENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-threadentry32) \| th32ThreadID")</span><span class="sxs-lookup"><span data-stu-id="4f926-167">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**Override**](../wmisdk/standard-qualifiers.md) ("Handle"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Tool Help Structures\|[**THREADENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-threadentry32)\|th32ThreadID")</span></span>
</dt> </dl>

<span data-ttu-id="4f926-168">Identificador para um thread.</span><span class="sxs-lookup"><span data-stu-id="4f926-168">Handle to a thread.</span></span> <span data-ttu-id="4f926-169">O identificador tem direitos de acesso completo por padrão.</span><span class="sxs-lookup"><span data-stu-id="4f926-169">The handle has full access rights by default.</span></span> <span data-ttu-id="4f926-170">Com o acesso de segurança correto, o identificador pode ser usado em qualquer função que aceite um identificador de thread.</span><span class="sxs-lookup"><span data-stu-id="4f926-170">With the correct security access, the handle can be used in any function that accepts a thread handle.</span></span> <span data-ttu-id="4f926-171">Dependendo do sinalizador de herança especificado quando ele é criado, esse identificador pode ser herdado por processos filho.</span><span class="sxs-lookup"><span data-stu-id="4f926-171">Depending on the inheritance flag specified when it is created, this handle can be inherited by child processes.</span></span>

</dd> <dt>

<span data-ttu-id="4f926-172">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="4f926-172">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f926-173">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="4f926-173">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="4f926-174">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4f926-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f926-175">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="4f926-175">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="4f926-176">O objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="4f926-176">Object was installed.</span></span> <span data-ttu-id="4f926-177">Essa propriedade não precisa de um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="4f926-177">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="4f926-178">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="4f926-178">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4f926-179">**KernelModeTime**</span><span class="sxs-lookup"><span data-stu-id="4f926-179">**KernelModeTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f926-180">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="4f926-180">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4f926-181">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4f926-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f926-182">Qualificadores: [**override**](../wmisdk/standard-qualifiers.md) ("KernelModeTime"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| desempenho estruturas de dados \| [**perf de \_ \_ tipo de objeto**](/windows/win32/api/winperf/ns-winperf-perf_object_type)com \| privilegetime"), [**unidades**](../wmisdk/standard-qualifiers.md) ("100 nanossegundos")</span><span class="sxs-lookup"><span data-stu-id="4f926-182">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("KernelModeTime"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Performance Data Structures\|[**PERF\_OBJECT\_TYPE**](/windows/win32/api/winperf/ns-winperf-perf_object_type)\|PrivilegedTime"), [**Units**](../wmisdk/standard-qualifiers.md) ("100 nanoseconds")</span></span>
</dt> </dl>

<span data-ttu-id="4f926-183">Tempo no modo kernel, em unidades de 100 nanossegundos.</span><span class="sxs-lookup"><span data-stu-id="4f926-183">Time in kernel mode, in 100 nanosecond units.</span></span> <span data-ttu-id="4f926-184">Se essas informações não estiverem disponíveis, um valor de 0 (zero) deverá ser usado.</span><span class="sxs-lookup"><span data-stu-id="4f926-184">If this information is not available, a value of 0 (zero) should be used.</span></span>

<span data-ttu-id="4f926-185">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="4f926-185">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="4f926-186">**Nome**</span><span class="sxs-lookup"><span data-stu-id="4f926-186">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f926-187">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="4f926-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4f926-188">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4f926-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f926-189">Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="4f926-189">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="4f926-190">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="4f926-190">Label by which the object is known.</span></span> <span data-ttu-id="4f926-191">Quando em uma subclasse, a propriedade pode ser substituída para ser uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="4f926-191">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="4f926-192">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="4f926-192">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4f926-193">**OSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="4f926-193">**OSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f926-194">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="4f926-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4f926-195">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4f926-195">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f926-196">Qualificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ processo CIM**](cim-process.md).**OSCreationClassName**"), [**\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="4f926-196">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Process**](cim-process.md).**OSCreationClassName**"), [**Cim\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="4f926-197">Nome da classe de criação do sistema operacional de escopo.</span><span class="sxs-lookup"><span data-stu-id="4f926-197">Creation class name of the scoping operating system.</span></span>

<span data-ttu-id="4f926-198">Essa propriedade é herdada [**do \_ thread CIM**](cim-thread.md).</span><span class="sxs-lookup"><span data-stu-id="4f926-198">This property is inherited from [**CIM\_Thread**](cim-thread.md).</span></span>

</dd> <dt>

<span data-ttu-id="4f926-199">**OSName**</span><span class="sxs-lookup"><span data-stu-id="4f926-199">**OSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f926-200">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="4f926-200">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4f926-201">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4f926-201">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f926-202">Qualificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ processo CIM**](cim-process.md).**OSName**"), [**\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="4f926-202">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Process**](cim-process.md).**OSName**"), [**Cim\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="4f926-203">Nome do sistema operacional de escopo.</span><span class="sxs-lookup"><span data-stu-id="4f926-203">Name of the scoping operating system.</span></span>

<span data-ttu-id="4f926-204">Essa propriedade é herdada [**do \_ thread CIM**](cim-thread.md).</span><span class="sxs-lookup"><span data-stu-id="4f926-204">This property is inherited from [**CIM\_Thread**](cim-thread.md).</span></span>

</dd> <dt>

<span data-ttu-id="4f926-205">**Prioridade**</span><span class="sxs-lookup"><span data-stu-id="4f926-205">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f926-206">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4f926-206">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4f926-207">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4f926-207">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f926-208">Qualificadores: [**override**](../wmisdk/standard-qualifiers.md) ("Priority"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api da \| ferramenta de ajuda do \| [**THREADENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-threadentry32) \| tpDeltaPri")</span><span class="sxs-lookup"><span data-stu-id="4f926-208">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Priority"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Tool Help Structures\|[**THREADENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-threadentry32)\|tpDeltaPri")</span></span>
</dt> </dl>

<span data-ttu-id="4f926-209">Prioridade dinâmica do thread.</span><span class="sxs-lookup"><span data-stu-id="4f926-209">Dynamic priority of the thread.</span></span> <span data-ttu-id="4f926-210">Cada thread tem uma prioridade dinâmica que o Agendador usa para determinar qual thread deve ser executado.</span><span class="sxs-lookup"><span data-stu-id="4f926-210">Each thread has a dynamic priority that the scheduler uses to determine which thread to execute.</span></span> <span data-ttu-id="4f926-211">Inicialmente, a prioridade dinâmica de um thread é igual à prioridade base.</span><span class="sxs-lookup"><span data-stu-id="4f926-211">Initially, a thread's dynamic priority is the same as its base priority.</span></span> <span data-ttu-id="4f926-212">O sistema pode aumentar e diminuir a prioridade dinâmica, para garantir que ela seja responsiva (garantindo que nenhum thread fique sem falta para o tempo do processador).</span><span class="sxs-lookup"><span data-stu-id="4f926-212">The system can raise and lower the dynamic priority, to ensure that it is responsive (guaranteeing that no threads are starved for processor time).</span></span> <span data-ttu-id="4f926-213">O sistema não aumenta a prioridade de threads com um nível de prioridade base entre 16 e 31.</span><span class="sxs-lookup"><span data-stu-id="4f926-213">The system does not boost the priority of threads with a base priority level between 16 and 31.</span></span> <span data-ttu-id="4f926-214">Somente os threads com uma prioridade básica entre 0 e 15 recebem aumentos de prioridade dinâmica.</span><span class="sxs-lookup"><span data-stu-id="4f926-214">Only threads with a base priority between 0 and 15 receive dynamic priority boosts.</span></span> <span data-ttu-id="4f926-215">Números mais altos indicam prioridades mais altas.</span><span class="sxs-lookup"><span data-stu-id="4f926-215">Higher numbers indicate higher priorities.</span></span>

</dd> <dt>

<span data-ttu-id="4f926-216">**PriorityBase**</span><span class="sxs-lookup"><span data-stu-id="4f926-216">**PriorityBase**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f926-217">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4f926-217">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4f926-218">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4f926-218">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f926-219">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api do \| tipo de \| [**\_ objeto perf \_**](/windows/win32/api/winperf/ns-winperf-perf_object_type)de estruturas de dados de desempenho \| PerfPriorityBase")</span><span class="sxs-lookup"><span data-stu-id="4f926-219">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Performance Data Structures\|[**PERF\_OBJECT\_TYPE**](/windows/win32/api/winperf/ns-winperf-perf_object_type)\|PerfPriorityBase")</span></span>
</dt> </dl>

<span data-ttu-id="4f926-220">Prioridade base atual de um thread.</span><span class="sxs-lookup"><span data-stu-id="4f926-220">Current base priority of a thread.</span></span> <span data-ttu-id="4f926-221">O sistema operacional pode aumentar a prioridade dinâmica do thread acima da prioridade base se o thread estiver manipulando a entrada do usuário ou reduzindo-a em direção à prioridade base se o thread se tornar associado à computação.</span><span class="sxs-lookup"><span data-stu-id="4f926-221">The operating system may raise the thread's dynamic priority above the base priority if the thread is handling user input, or lower it toward the base priority if the thread becomes compute-bound.</span></span> <span data-ttu-id="4f926-222">A propriedade **PriorityBase** pode ter um valor entre 0 e 31.</span><span class="sxs-lookup"><span data-stu-id="4f926-222">The **PriorityBase** property can have a value between 0 and 31.</span></span>

</dd> <dt>

<span data-ttu-id="4f926-223">**ProcessCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="4f926-223">**ProcessCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f926-224">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="4f926-224">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4f926-225">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4f926-225">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f926-226">Qualificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ processo CIM**](cim-process.md).**CreationClassName**"), [**\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="4f926-226">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Process**](cim-process.md).**CreationClassName**"), [**Cim\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="4f926-227">Valor da propriedade **CreationClassName** do processo de escopo.</span><span class="sxs-lookup"><span data-stu-id="4f926-227">Value of the scoping process **CreationClassName** property.</span></span>

<span data-ttu-id="4f926-228">Essa propriedade é herdada [**do \_ thread CIM**](cim-thread.md).</span><span class="sxs-lookup"><span data-stu-id="4f926-228">This property is inherited from [**CIM\_Thread**](cim-thread.md).</span></span>

</dd> <dt>

<span data-ttu-id="4f926-229">**ProcessHandle**</span><span class="sxs-lookup"><span data-stu-id="4f926-229">**ProcessHandle**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f926-230">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="4f926-230">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4f926-231">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4f926-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f926-232">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**override**](../wmisdk/standard-qualifiers.md) ("ProcessHandle"), [**propagado**](../wmisdk/standard-qualifiers.md) ([**" \_ processo CIM**](cim-process.md).**Handle**"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" win32api \| ferramenta ajuda estruturas \| [**THREADENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-threadentry32) \| th32OwnerProcessID ")</span><span class="sxs-lookup"><span data-stu-id="4f926-232">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**Override**](../wmisdk/standard-qualifiers.md) ("ProcessHandle"), [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Process**](cim-process.md).**Handle**"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Tool Help Structures\|[**THREADENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-threadentry32)\|th32OwnerProcessID")</span></span>
</dt> </dl>

<span data-ttu-id="4f926-233">Processo que criou o thread.</span><span class="sxs-lookup"><span data-stu-id="4f926-233">Process that created the thread.</span></span> <span data-ttu-id="4f926-234">O conteúdo dessa propriedade pode ser usado pelos elementos da API (interface de programação de aplicativo) do Windows.</span><span class="sxs-lookup"><span data-stu-id="4f926-234">The contents of this property can be used by Windows application programming interface (API) elements.</span></span>

</dd> <dt>

<span data-ttu-id="4f926-235">**StartAddress**</span><span class="sxs-lookup"><span data-stu-id="4f926-235">**StartAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f926-236">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4f926-236">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4f926-237">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4f926-237">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f926-238">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| objeto de thread WIn32API \| LPTHREAD lpStartAddress de rotina de \_ inicialização \_ \| ")</span><span class="sxs-lookup"><span data-stu-id="4f926-238">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WIn32API\|Thread Object\|LPTHREAD\_START\_ROUTINE\|lpStartAddress")</span></span>
</dt> </dl>

<span data-ttu-id="4f926-239">Endereço inicial do thread.</span><span class="sxs-lookup"><span data-stu-id="4f926-239">Starting address of the thread.</span></span> <span data-ttu-id="4f926-240">Como qualquer aplicativo com acesso apropriado ao thread pode alterar o contexto do thread, esse valor pode ser apenas uma aproximação do endereço inicial do thread.</span><span class="sxs-lookup"><span data-stu-id="4f926-240">Because any application with appropriate access to the thread can change the thread's context, this value may only be an approximation of the thread's starting address.</span></span>

</dd> <dt>

<span data-ttu-id="4f926-241">**Status**</span><span class="sxs-lookup"><span data-stu-id="4f926-241">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f926-242">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="4f926-242">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4f926-243">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4f926-243">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f926-244">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="4f926-244">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="4f926-245">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="4f926-245">Current status of the object.</span></span> <span data-ttu-id="4f926-246">Vários status de operação e não operacional podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="4f926-246">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="4f926-247">Os status operacionais incluem: "OK", "degradado" e "Pred falha" (um elemento, como uma unidade de disco rígido habilitado para inteligente, pode estar funcionando corretamente, mas prevendo uma falha em um futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="4f926-247">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="4f926-248">Os status não operacionais incluem: "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="4f926-248">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="4f926-249">O último, "Service", pode ser aplicado durante o espelhamento de espelho de um disco, recarregar uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="4f926-249">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="4f926-250">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="4f926-250">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="4f926-251">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="4f926-251">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="4f926-252">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="4f926-252">The values are:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="4f926-253">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="4f926-253">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="4f926-254">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="4f926-254">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="4f926-255">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="4f926-255">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4f926-256">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="4f926-256">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="4f926-257">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="4f926-257">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="4f926-258">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="4f926-258">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="4f926-259">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="4f926-259">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="4f926-260">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="4f926-260">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="4f926-261">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="4f926-261">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="4f926-262">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="4f926-262">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="4f926-263">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="4f926-263">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="4f926-264">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="4f926-264">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4f926-265">**ThreadState**</span><span class="sxs-lookup"><span data-stu-id="4f926-265">**ThreadState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f926-266">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4f926-266">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4f926-267">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4f926-267">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f926-268">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estado de thread win32api")</span><span class="sxs-lookup"><span data-stu-id="4f926-268">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Thread State")</span></span>
</dt> </dl>

<span data-ttu-id="4f926-269">Estado de execução atual do thread.</span><span class="sxs-lookup"><span data-stu-id="4f926-269">Current execution state for the thread.</span></span>

<dt>

<span id="Initialized"></span><span id="initialized"></span><span id="INITIALIZED"></span>

<span data-ttu-id="4f926-270"><span id="Initialized"></span><span id="initialized"></span><span id="INITIALIZED"></span>**Inicializado** (0)</span><span class="sxs-lookup"><span data-stu-id="4f926-270"><span id="Initialized"></span><span id="initialized"></span><span id="INITIALIZED"></span>**Initialized** (0)</span></span>


</dt> <dd>

<span data-ttu-id="4f926-271">Inicializado — ele é reconhecido pelo microkernel.</span><span class="sxs-lookup"><span data-stu-id="4f926-271">Initialized — It is recognized by the microkernel.</span></span>

</dd> <dt>

<span id="Ready"></span><span id="ready"></span><span id="READY"></span>

<span data-ttu-id="4f926-272"><span id="Ready"></span><span id="ready"></span><span id="READY"></span>**Pronto** (1)</span><span class="sxs-lookup"><span data-stu-id="4f926-272"><span id="Ready"></span><span id="ready"></span><span id="READY"></span>**Ready** (1)</span></span>


</dt> <dd>

<span data-ttu-id="4f926-273">Pronto — ele está preparado para ser executado no próximo processador disponível.</span><span class="sxs-lookup"><span data-stu-id="4f926-273">Ready — It is prepared to run on the next available processor.</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="4f926-274"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Em execução** (2)</span><span class="sxs-lookup"><span data-stu-id="4f926-274"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (2)</span></span>


</dt> <dd>

<span data-ttu-id="4f926-275">Em execução — está em execução.</span><span class="sxs-lookup"><span data-stu-id="4f926-275">Running — It is executing.</span></span>

</dd> <dt>

<span id="Standby"></span><span id="standby"></span><span id="STANDBY"></span>

<span data-ttu-id="4f926-276"><span id="Standby"></span><span id="standby"></span><span id="STANDBY"></span>Em **espera** (3)</span><span class="sxs-lookup"><span data-stu-id="4f926-276"><span id="Standby"></span><span id="standby"></span><span id="STANDBY"></span>**Standby** (3)</span></span>


</dt> <dd>

<span data-ttu-id="4f926-277">Em espera — está prestes a ser executado, somente um thread pode estar nesse estado por vez.</span><span class="sxs-lookup"><span data-stu-id="4f926-277">Standby — It is about to run, only one thread may be in this state at a time.</span></span>

</dd> <dt>

<span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>

<span data-ttu-id="4f926-278"><span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>**Encerrado** (4)</span><span class="sxs-lookup"><span data-stu-id="4f926-278"><span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>**Terminated** (4)</span></span>


</dt> <dd>

<span data-ttu-id="4f926-279">Encerrado – concluiu a execução.</span><span class="sxs-lookup"><span data-stu-id="4f926-279">Terminated — It is finished executing.</span></span>

</dd> <dt>

<span id="Waiting"></span><span id="waiting"></span><span id="WAITING"></span>

<span data-ttu-id="4f926-280"><span id="Waiting"></span><span id="waiting"></span><span id="WAITING"></span>**Aguardando** (5)</span><span class="sxs-lookup"><span data-stu-id="4f926-280"><span id="Waiting"></span><span id="waiting"></span><span id="WAITING"></span>**Waiting** (5)</span></span>


</dt> <dd>

<span data-ttu-id="4f926-281">Aguardando — ele não está pronto para o processador, quando estiver pronto, ele será reagendado.</span><span class="sxs-lookup"><span data-stu-id="4f926-281">Waiting — It is not ready for the processor, when ready, it will be rescheduled.</span></span>

</dd> <dt>

<span id="Transition"></span><span id="transition"></span><span id="TRANSITION"></span>

<span data-ttu-id="4f926-282"><span id="Transition"></span><span id="transition"></span><span id="TRANSITION"></span>**Transição** (6)</span><span class="sxs-lookup"><span data-stu-id="4f926-282"><span id="Transition"></span><span id="transition"></span><span id="TRANSITION"></span>**Transition** (6)</span></span>


</dt> <dd>

<span data-ttu-id="4f926-283">Transição — o thread está aguardando recursos diferentes do processador,</span><span class="sxs-lookup"><span data-stu-id="4f926-283">Transition — The thread is waiting for resources other than the processor,</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4f926-284"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (7)</span><span class="sxs-lookup"><span data-stu-id="4f926-284"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (7)</span></span>


</dt> <dd>

<span data-ttu-id="4f926-285">Desconhecido — o estado do thread é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="4f926-285">Unknown — The thread state is unknown.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="4f926-286">**ThreadWaitReason**</span><span class="sxs-lookup"><span data-stu-id="4f926-286">**ThreadWaitReason**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f926-287">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4f926-287">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4f926-288">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4f926-288">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f926-289">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| motivo de espera de thread win32api")</span><span class="sxs-lookup"><span data-stu-id="4f926-289">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Thread Wait Reason")</span></span>
</dt> </dl>

<span data-ttu-id="4f926-290">Motivo pelo qual o thread está aguardando.</span><span class="sxs-lookup"><span data-stu-id="4f926-290">Reason why the thread is waiting.</span></span> <span data-ttu-id="4f926-291">Esse valor só será válido se o membro **ThreadState** estiver definido como Transition (6).</span><span class="sxs-lookup"><span data-stu-id="4f926-291">This value is only valid if the **ThreadState** member is set to Transition (6).</span></span> <span data-ttu-id="4f926-292">Os pares de eventos permitem a comunicação com subsistemas protegidos.</span><span class="sxs-lookup"><span data-stu-id="4f926-292">Event pairs allow communication with protected subsystems.</span></span>

<dt>

<span id="Executive"></span><span id="executive"></span><span id="EXECUTIVE"></span>

<span data-ttu-id="4f926-293"><span id="Executive"></span><span id="executive"></span><span id="EXECUTIVE"></span>**Executivo** (0)</span><span class="sxs-lookup"><span data-stu-id="4f926-293"><span id="Executive"></span><span id="executive"></span><span id="EXECUTIVE"></span>**Executive** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>

<span data-ttu-id="4f926-294"><span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>**FreePage** (1)</span><span class="sxs-lookup"><span data-stu-id="4f926-294"><span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>**FreePage** (1)</span></span>


</dt> <dd>

<span data-ttu-id="4f926-295">FreePage</span><span class="sxs-lookup"><span data-stu-id="4f926-295">FreePage</span></span>

</dd> <dt>

<span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>

<span data-ttu-id="4f926-296"><span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>**Página** (2)</span><span class="sxs-lookup"><span data-stu-id="4f926-296"><span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>**PageIn** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="PoolAllocation"></span><span id="poolallocation"></span><span id="POOLALLOCATION"></span>

<span data-ttu-id="4f926-297"><span id="PoolAllocation"></span><span id="poolallocation"></span><span id="POOLALLOCATION"></span>**PoolAllocation** (3)</span><span class="sxs-lookup"><span data-stu-id="4f926-297"><span id="PoolAllocation"></span><span id="poolallocation"></span><span id="POOLALLOCATION"></span>**PoolAllocation** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ExecutionDelay"></span><span id="executiondelay"></span><span id="EXECUTIONDELAY"></span>

<span data-ttu-id="4f926-298"><span id="ExecutionDelay"></span><span id="executiondelay"></span><span id="EXECUTIONDELAY"></span>**ExecutionDelay** (4)</span><span class="sxs-lookup"><span data-stu-id="4f926-298"><span id="ExecutionDelay"></span><span id="executiondelay"></span><span id="EXECUTIONDELAY"></span>**ExecutionDelay** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>

<span data-ttu-id="4f926-299"><span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>**FreePage** (5)</span><span class="sxs-lookup"><span data-stu-id="4f926-299"><span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>**FreePage** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>

<span data-ttu-id="4f926-300"><span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>**Página** (6)</span><span class="sxs-lookup"><span data-stu-id="4f926-300"><span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>**PageIn** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Executive"></span><span id="executive"></span><span id="EXECUTIVE"></span>

<span data-ttu-id="4f926-301"><span id="Executive"></span><span id="executive"></span><span id="EXECUTIVE"></span>**Executivo** (7)</span><span class="sxs-lookup"><span data-stu-id="4f926-301"><span id="Executive"></span><span id="executive"></span><span id="EXECUTIVE"></span>**Executive** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>

<span data-ttu-id="4f926-302"><span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>**FreePage** (8)</span><span class="sxs-lookup"><span data-stu-id="4f926-302"><span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>**FreePage** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>

<span data-ttu-id="4f926-303"><span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>**Página** (9)</span><span class="sxs-lookup"><span data-stu-id="4f926-303"><span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>**PageIn** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="PoolAllocation"></span><span id="poolallocation"></span><span id="POOLALLOCATION"></span>

<span data-ttu-id="4f926-304"><span id="PoolAllocation"></span><span id="poolallocation"></span><span id="POOLALLOCATION"></span>**PoolAllocation** (10)</span><span class="sxs-lookup"><span data-stu-id="4f926-304"><span id="PoolAllocation"></span><span id="poolallocation"></span><span id="POOLALLOCATION"></span>**PoolAllocation** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="ExecutionDelay"></span><span id="executiondelay"></span><span id="EXECUTIONDELAY"></span>

<span data-ttu-id="4f926-305"><span id="ExecutionDelay"></span><span id="executiondelay"></span><span id="EXECUTIONDELAY"></span>**ExecutionDelay** (11)</span><span class="sxs-lookup"><span data-stu-id="4f926-305"><span id="ExecutionDelay"></span><span id="executiondelay"></span><span id="EXECUTIONDELAY"></span>**ExecutionDelay** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>

<span data-ttu-id="4f926-306"><span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>**FreePage** (12)</span><span class="sxs-lookup"><span data-stu-id="4f926-306"><span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>**FreePage** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>

<span data-ttu-id="4f926-307"><span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>**Página** (13)</span><span class="sxs-lookup"><span data-stu-id="4f926-307"><span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>**PageIn** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="EventPairHigh"></span><span id="eventpairhigh"></span><span id="EVENTPAIRHIGH"></span>

<span data-ttu-id="4f926-308"><span id="EventPairHigh"></span><span id="eventpairhigh"></span><span id="EVENTPAIRHIGH"></span>**EventPairHigh** (14)</span><span class="sxs-lookup"><span data-stu-id="4f926-308"><span id="EventPairHigh"></span><span id="eventpairhigh"></span><span id="EVENTPAIRHIGH"></span>**EventPairHigh** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="EventPairLow"></span><span id="eventpairlow"></span><span id="EVENTPAIRLOW"></span>

<span data-ttu-id="4f926-309"><span id="EventPairLow"></span><span id="eventpairlow"></span><span id="EVENTPAIRLOW"></span>**EventPairLow** (15)</span><span class="sxs-lookup"><span data-stu-id="4f926-309"><span id="EventPairLow"></span><span id="eventpairlow"></span><span id="EVENTPAIRLOW"></span>**EventPairLow** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="LPCReceive"></span><span id="lpcreceive"></span><span id="LPCRECEIVE"></span>

<span data-ttu-id="4f926-310"><span id="LPCReceive"></span><span id="lpcreceive"></span><span id="LPCRECEIVE"></span>**LPCReceive** (16)</span><span class="sxs-lookup"><span data-stu-id="4f926-310"><span id="LPCReceive"></span><span id="lpcreceive"></span><span id="LPCRECEIVE"></span>**LPCReceive** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="LPCReply"></span><span id="lpcreply"></span><span id="LPCREPLY"></span>

<span data-ttu-id="4f926-311"><span id="LPCReply"></span><span id="lpcreply"></span><span id="LPCREPLY"></span>**LPCReply** (17)</span><span class="sxs-lookup"><span data-stu-id="4f926-311"><span id="LPCReply"></span><span id="lpcreply"></span><span id="LPCREPLY"></span>**LPCReply** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="VirtualMemory"></span><span id="virtualmemory"></span><span id="VIRTUALMEMORY"></span>

<span data-ttu-id="4f926-312"><span id="VirtualMemory"></span><span id="virtualmemory"></span><span id="VIRTUALMEMORY"></span>**VirtualMemory** (18)</span><span class="sxs-lookup"><span data-stu-id="4f926-312"><span id="VirtualMemory"></span><span id="virtualmemory"></span><span id="VIRTUALMEMORY"></span>**VirtualMemory** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="PageOut"></span><span id="pageout"></span><span id="PAGEOUT"></span>

<span data-ttu-id="4f926-313"><span id="PageOut"></span><span id="pageout"></span><span id="PAGEOUT"></span>**Pageout** (19)</span><span class="sxs-lookup"><span data-stu-id="4f926-313"><span id="PageOut"></span><span id="pageout"></span><span id="PAGEOUT"></span>**PageOut** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4f926-314"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (20)</span><span class="sxs-lookup"><span data-stu-id="4f926-314"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (20)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4f926-315">**Usermodetime**</span><span class="sxs-lookup"><span data-stu-id="4f926-315">**UserModeTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f926-316">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="4f926-316">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4f926-317">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4f926-317">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f926-318">Qualificadores: [**substituir**](../wmisdk/standard-qualifiers.md) ("usermodetime"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api de \| dados de desempenho do \| [**\_ tipo perf Object \_ Type**](/windows/win32/api/winperf/ns-winperf-perf_object_type) \| "), [**Units**](../wmisdk/standard-qualifiers.md) ("100 nanossegundos")</span><span class="sxs-lookup"><span data-stu-id="4f926-318">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("UserModeTime"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Performance Data Structures\|[**PERF\_OBJECT\_TYPE**](/windows/win32/api/winperf/ns-winperf-perf_object_type)\|UserTime"), [**Units**](../wmisdk/standard-qualifiers.md) ("100 nanoseconds")</span></span>
</dt> </dl>

<span data-ttu-id="4f926-319">Tempo no modo de usuário, em unidades de 100 nanossegundos.</span><span class="sxs-lookup"><span data-stu-id="4f926-319">Time in user mode, in 100 nanoseconds units.</span></span> <span data-ttu-id="4f926-320">Se essas informações não estiverem disponíveis, um valor de 0 (zero) deverá ser usado.</span><span class="sxs-lookup"><span data-stu-id="4f926-320">If this information is not available, a value of 0 (zero) should be used.</span></span>

<span data-ttu-id="4f926-321">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="4f926-321">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4f926-322">Comentários</span><span class="sxs-lookup"><span data-stu-id="4f926-322">Remarks</span></span>

<span data-ttu-id="4f926-323">A classe de **\_ Thread Win32** é derivada [**do \_ thread CIM**](cim-thread.md).</span><span class="sxs-lookup"><span data-stu-id="4f926-323">The **Win32\_Thread** class is derived from [**CIM\_Thread**](cim-thread.md).</span></span>

<span data-ttu-id="4f926-324">**Visão geral**</span><span class="sxs-lookup"><span data-stu-id="4f926-324">**Overview**</span></span>

<span data-ttu-id="4f926-325">Para o monitoramento diário de rotina, geralmente há pouco motivo para ter uma lista detalhada de threads e suas propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="4f926-325">For routine day-to-day monitoring, there is usually little reason to have a detailed list of threads and their associated properties.</span></span> <span data-ttu-id="4f926-326">Os computadores criam e excluem milhares de threads durante um dia, e algumas dessas criações ou exclusões são significativas para qualquer pessoa, exceto para o desenvolvedor que escreveu o software.</span><span class="sxs-lookup"><span data-stu-id="4f926-326">Computers create and delete thousands of threads during the course of a day, and few of these creations or deletions are meaningful to anyone but the developer who wrote the software.</span></span>

<span data-ttu-id="4f926-327">No entanto, quando você está Solucionando problemas com um aplicativo, controlar os threads individuais de um processo permite que você identifique quando os threads são criados e quando (ou se) eles são destruídos.</span><span class="sxs-lookup"><span data-stu-id="4f926-327">However, when you are troubleshooting problems with an application, tracking the individual threads for a process allows you to identify when threads are created and when (or if) they are destroyed.</span></span> <span data-ttu-id="4f926-328">Como os threads criados mas não destruídos causam vazamentos de memória, o acompanhamento de threads individuais pode ser uma informação útil para técnicos de suporte.</span><span class="sxs-lookup"><span data-stu-id="4f926-328">Because threads that are created but not destroyed cause memory leaks, tracking individual threads can be useful information for support technicians.</span></span> <span data-ttu-id="4f926-329">Da mesma forma, a identificação de prioridades de thread pode ajudar a identificar threads que, ao executar em uma prioridade muito alta, estão admitindo antecipadamente os ciclos de CPU necessários para outros threads e outros processos.</span><span class="sxs-lookup"><span data-stu-id="4f926-329">Likewise, identifying thread priorities can help pinpoint threads that, by running at an abnormally high priority, are preempting CPU cycles needed by other threads and other processes.</span></span>

<span data-ttu-id="4f926-330">**Usando thread do Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="4f926-330">**Using Win32\_Thread**</span></span>

<span data-ttu-id="4f926-331">Como implícito no bloco de sintaxe anterior, a classe **\_ thread do Win32** não relata o nome do processo no qual cada thread é executado.</span><span class="sxs-lookup"><span data-stu-id="4f926-331">As implied in the preceding syntax block, the **Win32\_Thread** class does not report the name of the process under which each thread runs.</span></span> <span data-ttu-id="4f926-332">Em vez disso, ele relata a ID do processo sob o qual o thread é executado.</span><span class="sxs-lookup"><span data-stu-id="4f926-332">Instead, it reports the ID of the process under which the thread runs.</span></span> <span data-ttu-id="4f926-333">Para retornar o nome de um processo e uma lista de todos os seus threads, o script deve:</span><span class="sxs-lookup"><span data-stu-id="4f926-333">To return the name of a process and a list of all its threads, your script must:</span></span>

1.  <span data-ttu-id="4f926-334">Conecte-se à classe de [**\_ processo do Win32**](win32-process.md) e retorne a lista de processos e suas IDs de processo.</span><span class="sxs-lookup"><span data-stu-id="4f926-334">Connect to the [**Win32\_Process**](win32-process.md) class and return the list of processes and their process IDs.</span></span>
2.  <span data-ttu-id="4f926-335">Armazene temporariamente essas informações em um objeto de matriz ou de dicionário.</span><span class="sxs-lookup"><span data-stu-id="4f926-335">Temporarily store this information in an array or Dictionary object.</span></span>
3.  <span data-ttu-id="4f926-336">Para cada ID de processo, retorne a lista de threads para esse processo e, em seguida, exiba o nome do processo e a lista de threads.</span><span class="sxs-lookup"><span data-stu-id="4f926-336">For each process ID, return the list of threads for that process, and then display the process name and the list of threads.</span></span>

## <a name="examples"></a><span data-ttu-id="4f926-337">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4f926-337">Examples</span></span>

<span data-ttu-id="4f926-338">O exemplo de VBScript a seguir monitora os threads em execução em um computador.</span><span class="sxs-lookup"><span data-stu-id="4f926-338">The following VBScript sample monitors the threads running on a computer.</span></span>


```VB
Set objDictionary = CreateObject("Scripting.Dictionary")
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colProcesses = objWMIService.ExecQuery("SELECT * FROM Win32_Process")
For Each objProcess in colProcesses
 objDictionary.Add objProcess.ProcessID, objProcess.Name
Next
Set colThreads = objWMIService.ExecQuery("SELECT * FROM Win32_Thread")
For Each objThread in colThreads
 intProcessID = CInt(objThread.ProcessHandle)
 strProcessName = objDictionary.Item(intProcessID)
 Wscript.Echo strProcessName & VbTab & objThread.ProcessHandle & _
              VbTab & objThread.Handle & VbTab & objThread.ThreadState
Next
```



## <a name="requirements"></a><span data-ttu-id="4f926-339">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4f926-339">Requirements</span></span>



| <span data-ttu-id="4f926-340">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f926-340">Requirement</span></span> | <span data-ttu-id="4f926-341">Valor</span><span class="sxs-lookup"><span data-stu-id="4f926-341">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4f926-342">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4f926-342">Minimum supported client</span></span><br/> | <span data-ttu-id="4f926-343">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4f926-343">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4f926-344">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4f926-344">Minimum supported server</span></span><br/> | <span data-ttu-id="4f926-345">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4f926-345">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4f926-346">Namespace</span><span class="sxs-lookup"><span data-stu-id="4f926-346">Namespace</span></span><br/>                | <span data-ttu-id="4f926-347">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="4f926-347">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4f926-348">MOF</span><span class="sxs-lookup"><span data-stu-id="4f926-348">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4f926-349"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4f926-349"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4f926-350">DLL</span><span class="sxs-lookup"><span data-stu-id="4f926-350">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4f926-351"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4f926-351"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f926-352">Confira também</span><span class="sxs-lookup"><span data-stu-id="4f926-352">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f926-353">**\_Thread CIM**</span><span class="sxs-lookup"><span data-stu-id="4f926-353">**CIM\_Thread**</span></span>](cim-thread.md)
</dt> <dt>

[<span data-ttu-id="4f926-354">Classes do sistema operacional</span><span class="sxs-lookup"><span data-stu-id="4f926-354">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
