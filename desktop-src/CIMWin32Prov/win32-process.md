---
Description: O \_ processo Win32&\# 32; A classe WMI representa um processo em um sistema operacional.
ms.assetid: 51206aca-4784-4d18-95ca-bc0a45691f78
ms.tgt_platform: multiple
title: Classe Win32_Process
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/23/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Process
- Win32_Process.CreationClassName
- Win32_Process.Caption
- Win32_Process.CommandLine
- Win32_Process.CreationDate
- Win32_Process.CSCreationClassName
- Win32_Process.CSName
- Win32_Process.Description
- Win32_Process.ExecutablePath
- Win32_Process.ExecutionState
- Win32_Process.Handle
- Win32_Process.HandleCount
- Win32_Process.InstallDate
- Win32_Process.KernelModeTime
- Win32_Process.MaximumWorkingSetSize
- Win32_Process.MinimumWorkingSetSize
- Win32_Process.Name
- Win32_Process.OSCreationClassName
- Win32_Process.OSName
- Win32_Process.OtherOperationCount
- Win32_Process.OtherTransferCount
- Win32_Process.PageFaults
- Win32_Process.PageFileUsage
- Win32_Process.ParentProcessId
- Win32_Process.PeakPageFileUsage
- Win32_Process.PeakVirtualSize
- Win32_Process.PeakWorkingSetSize
- Win32_Process.Priority
- Win32_Process.PrivatePageCount
- Win32_Process.ProcessId
- Win32_Process.QuotaNonPagedPoolUsage
- Win32_Process.QuotaPagedPoolUsage
- Win32_Process.QuotaPeakNonPagedPoolUsage
- Win32_Process.QuotaPeakPagedPoolUsage
- Win32_Process.ReadOperationCount
- Win32_Process.ReadTransferCount
- Win32_Process.SessionId
- Win32_Process.Status
- Win32_Process.TerminationDate
- Win32_Process.ThreadCount
- Win32_Process.UserModeTime
- Win32_Process.VirtualSize
- Win32_Process.WindowsVersion
- Win32_Process.WorkingSetSize
- Win32_Process.WriteOperationCount
- Win32_Process.WriteTransferCount
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: bb8d1d37bd5d4db59942aaab7170119283c5cc7b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752951"
---
# <a name="win32_process-class"></a><span data-ttu-id="f47a9-103">\_Classe de processo Win32</span><span class="sxs-lookup"><span data-stu-id="f47a9-103">Win32\_Process class</span></span>

<span data-ttu-id="f47a9-104">A [classe WMI](../wmisdk/retrieving-a-class.md) de **\_ processo Win32** representa um processo em um sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="f47a9-104">The **Win32\_Process** [WMI class](../wmisdk/retrieving-a-class.md) represents a process on an operating system.</span></span>

<span data-ttu-id="f47a9-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="f47a9-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

> [!NOTE]
> <span data-ttu-id="f47a9-106">Para uma discussão geral sobre processos e threads no Windows, consulte o tópico [processos e threads](/ProcThread/processes-and-threads.md).</span><span class="sxs-lookup"><span data-stu-id="f47a9-106">For a general discussion on Processes and Threads within Windows, please see the topic [Processes and Threads](/ProcThread/processes-and-threads.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="f47a9-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f47a9-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), SupportsCreate, CreateBy("Create"), SupportsDelete, DeleteBy("DeleteInstance"), UUID("{8502C4DC-5FBB-11D2-AAC1-006008C78BC7}"), DisplayName("Processes"), AMENDMENT]
class Win32_Process : CIM_Process
{
  string   CreationClassName;
  string   Caption;
  string   CommandLine;
  datetime CreationDate;
  string   CSCreationClassName;
  string   CSName;
  string   Description;
  string   ExecutablePath;
  uint16   ExecutionState;
  string   Handle;
  uint32   HandleCount;
  datetime InstallDate;
  uint64   KernelModeTime;
  uint32   MaximumWorkingSetSize;
  uint32   MinimumWorkingSetSize;
  string   Name;
  string   OSCreationClassName;
  string   OSName;
  uint64   OtherOperationCount;
  uint64   OtherTransferCount;
  uint32   PageFaults;
  uint32   PageFileUsage;
  uint32   ParentProcessId;
  uint32   PeakPageFileUsage;
  uint64   PeakVirtualSize;
  uint32   PeakWorkingSetSize;
  uint32   Priority = NULL;
  uint64   PrivatePageCount;
  uint32   ProcessId;
  uint32   QuotaNonPagedPoolUsage;
  uint32   QuotaPagedPoolUsage;
  uint32   QuotaPeakNonPagedPoolUsage;
  uint32   QuotaPeakPagedPoolUsage;
  uint64   ReadOperationCount;
  uint64   ReadTransferCount;
  uint32   SessionId;
  string   Status;
  datetime TerminationDate;
  uint32   ThreadCount;
  uint64   UserModeTime;
  uint64   VirtualSize;
  string   WindowsVersion;
  uint64   WorkingSetSize;
  uint64   WriteOperationCount;
  uint64   WriteTransferCount;
};
```

## <a name="members"></a><span data-ttu-id="f47a9-108">Membros</span><span class="sxs-lookup"><span data-stu-id="f47a9-108">Members</span></span>

<span data-ttu-id="f47a9-109">A classe de **\_ processo do Win32** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="f47a9-109">The **Win32\_Process** class has these types of members:</span></span>

-   [<span data-ttu-id="f47a9-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="f47a9-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="f47a9-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f47a9-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="f47a9-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="f47a9-112">Methods</span></span>

<span data-ttu-id="f47a9-113">A **classe \_ process do Win32** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="f47a9-113">The **Win32\_Process** class has these methods.</span></span>



| <span data-ttu-id="f47a9-114">Método</span><span class="sxs-lookup"><span data-stu-id="f47a9-114">Method</span></span>                                                                   | <span data-ttu-id="f47a9-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="f47a9-115">Description</span></span>                                                                                                                                                                                                                                                                               |
|:-------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f47a9-116">**AttachDebugger**</span><span class="sxs-lookup"><span data-stu-id="f47a9-116">**AttachDebugger**</span></span>](attachdebugger-method-in-class-win32-process.md)   | <span data-ttu-id="f47a9-117">Inicia o depurador atualmente registrado para um processo.</span><span class="sxs-lookup"><span data-stu-id="f47a9-117">Launches the currently registered debugger for a process.</span></span><br/>                                                                                                                                                                                                                      |
| [<span data-ttu-id="f47a9-118">**Criar**</span><span class="sxs-lookup"><span data-stu-id="f47a9-118">**Create**</span></span>](create-method-in-class-win32-process.md)                   | <span data-ttu-id="f47a9-119">Cria um novo processo.</span><span class="sxs-lookup"><span data-stu-id="f47a9-119">Creates a new process.</span></span><br/>                                                                                                                                                                                                                                                         |
| [<span data-ttu-id="f47a9-120">**GetAvailableVirtualSize**</span><span class="sxs-lookup"><span data-stu-id="f47a9-120">**GetAvailableVirtualSize**</span></span>](getavailablevirtualsize-win32-process.md) | <span data-ttu-id="f47a9-121">Recupera o tamanho atual, em bytes, do espaço de endereço virtual livre disponível para o processo.</span><span class="sxs-lookup"><span data-stu-id="f47a9-121">Retrieves the current size, in bytes, of the free virtual address space available to the process.</span></span><br/> <span data-ttu-id="f47a9-122">**Windows server 2012, Windows 8, Windows 7, Windows server 2008 e Windows Vista:** Esse método não tem suporte antes do Windows 8.1 e do Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="f47a9-122">**Windows Server 2012, Windows 8, Windows 7, Windows Server 2008 and Windows Vista:** This method is not supported before Windows 8.1 and Windows Server 2012 R2.</span></span><br/> |
| [<span data-ttu-id="f47a9-123">**GetOwner**</span><span class="sxs-lookup"><span data-stu-id="f47a9-123">**GetOwner**</span></span>](getowner-method-in-class-win32-process.md)               | <span data-ttu-id="f47a9-124">Recupera o nome de usuário e o nome de domínio sob os quais o processo está em execução.</span><span class="sxs-lookup"><span data-stu-id="f47a9-124">Retrieves the user name and domain name under which the process is running.</span></span><br/>                                                                                                                                                                                                    |
| [<span data-ttu-id="f47a9-125">**Getownerid**</span><span class="sxs-lookup"><span data-stu-id="f47a9-125">**GetOwnerSid**</span></span>](getownersid-method-in-class-win32-process.md)         | <span data-ttu-id="f47a9-126">Recupera o identificador de segurança (SID) do proprietário de um processo.</span><span class="sxs-lookup"><span data-stu-id="f47a9-126">Retrieves the security identifier (SID) for the owner of a process.</span></span><br/>                                                                                                                                                                                                            |
| [<span data-ttu-id="f47a9-127">**Setanteriority**</span><span class="sxs-lookup"><span data-stu-id="f47a9-127">**SetPriority**</span></span>](setpriority-method-in-class-win32-process.md)         | <span data-ttu-id="f47a9-128">Altera a prioridade de execução de um processo.</span><span class="sxs-lookup"><span data-stu-id="f47a9-128">Changes the execution priority of a process.</span></span><br/>                                                                                                                                                                                                                                   |
| [<span data-ttu-id="f47a9-129">**Encerrar**</span><span class="sxs-lookup"><span data-stu-id="f47a9-129">**Terminate**</span></span>](terminate-method-in-class-win32-process.md)             | <span data-ttu-id="f47a9-130">Encerra um processo e todos os seus threads.</span><span class="sxs-lookup"><span data-stu-id="f47a9-130">Terminates a process and all of its threads.</span></span><br/>                                                                                                                                                                                                                                   |



 

### <a name="properties"></a><span data-ttu-id="f47a9-131">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f47a9-131">Properties</span></span>

<span data-ttu-id="f47a9-132">A **classe \_ process do Win32** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="f47a9-132">The **Win32\_Process** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f47a9-133">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="f47a9-133">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f47a9-134">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f47a9-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f47a9-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f47a9-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f47a9-136">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="f47a9-136">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="f47a9-137">Breve descrição de um objeto — uma cadeia de caracteres de uma linha.</span><span class="sxs-lookup"><span data-stu-id="f47a9-137">Short description of an object—a one-line string.</span></span>

<span data-ttu-id="f47a9-138">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f47a9-138">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f47a9-139">**CommandLine**</span><span class="sxs-lookup"><span data-stu-id="f47a9-139">**CommandLine**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f47a9-140">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f47a9-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f47a9-141">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f47a9-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f47a9-142">Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("linha de comando para iniciar o processo")</span><span class="sxs-lookup"><span data-stu-id="f47a9-142">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Command Line To Start Process")</span></span>
</dt> </dl>

<span data-ttu-id="f47a9-143">Linha de comando usada para iniciar um processo específico, se aplicável.</span><span class="sxs-lookup"><span data-stu-id="f47a9-143">Command line used to start a specific process, if applicable.</span></span>

</dd> <dt>

<span data-ttu-id="f47a9-144">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="f47a9-144">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f47a9-145">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f47a9-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f47a9-146">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f47a9-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f47a9-147">Qualificadores: [**\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("nome da classe")</span><span class="sxs-lookup"><span data-stu-id="f47a9-147">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="f47a9-148">Nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="f47a9-148">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="f47a9-149">Quando usado com outras propriedades de chave da classe, essa propriedade permite que todas as instâncias da classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="f47a9-149">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="f47a9-150">Essa propriedade é herdada [**do \_ processo CIM**](cim-process.md).</span><span class="sxs-lookup"><span data-stu-id="f47a9-150">This property is inherited from [**CIM\_Process**](cim-process.md).</span></span>

</dd> <dt>

<span data-ttu-id="f47a9-151">**CreationDate**</span><span class="sxs-lookup"><span data-stu-id="f47a9-151">**CreationDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f47a9-152">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="f47a9-152">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f47a9-153">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f47a9-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f47a9-154">Qualificadores: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("CreationDate")</span><span class="sxs-lookup"><span data-stu-id="f47a9-154">Qualifiers: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("CreationDate")</span></span>
</dt> </dl>

<span data-ttu-id="f47a9-155">Data em que o processo começa a ser executado.</span><span class="sxs-lookup"><span data-stu-id="f47a9-155">Date the process begins executing.</span></span>

<span data-ttu-id="f47a9-156">Essa propriedade é herdada [**do \_ processo CIM**](cim-process.md).</span><span class="sxs-lookup"><span data-stu-id="f47a9-156">This property is inherited from [**CIM\_Process**](cim-process.md).</span></span>

</dd> <dt>

<span data-ttu-id="f47a9-157">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="f47a9-157">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f47a9-158">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f47a9-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f47a9-159">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f47a9-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f47a9-160">Qualificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ("sistema [**\_ operacional CIM**](cim-operatingsystem.md).**CSCreationClassName**"), [**\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" nome da classe do sistema de computador ")</span><span class="sxs-lookup"><span data-stu-id="f47a9-160">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**CSCreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Computer System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="f47a9-161">Nome da classe de criação do sistema de computador de escopo.</span><span class="sxs-lookup"><span data-stu-id="f47a9-161">Creation class name of the scoping computer system.</span></span>

<span data-ttu-id="f47a9-162">Essa propriedade é herdada [**do \_ processo CIM**](cim-process.md).</span><span class="sxs-lookup"><span data-stu-id="f47a9-162">This property is inherited from [**CIM\_Process**](cim-process.md).</span></span>

</dd> <dt>

<span data-ttu-id="f47a9-163">**CSName**</span><span class="sxs-lookup"><span data-stu-id="f47a9-163">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f47a9-164">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f47a9-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f47a9-165">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f47a9-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f47a9-166">Qualificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ("sistema [**\_ operacional CIM**](cim-operatingsystem.md).**CSName**"), [**\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" nome do sistema de computador ")</span><span class="sxs-lookup"><span data-stu-id="f47a9-166">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**CSName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Computer System Name")</span></span>
</dt> </dl>

<span data-ttu-id="f47a9-167">Nome do sistema de computador de escopo.</span><span class="sxs-lookup"><span data-stu-id="f47a9-167">Name of the scoping computer system.</span></span>

<span data-ttu-id="f47a9-168">Essa propriedade é herdada [**do \_ processo CIM**](cim-process.md).</span><span class="sxs-lookup"><span data-stu-id="f47a9-168">This property is inherited from [**CIM\_Process**](cim-process.md).</span></span>

</dd> <dt>

<span data-ttu-id="f47a9-169">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="f47a9-169">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f47a9-170">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f47a9-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f47a9-171">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f47a9-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f47a9-172">Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="f47a9-172">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="f47a9-173">Descrição de um objeto.</span><span class="sxs-lookup"><span data-stu-id="f47a9-173">Description of an object.</span></span>

<span data-ttu-id="f47a9-174">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f47a9-174">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f47a9-175">**ExecutablePath**</span><span class="sxs-lookup"><span data-stu-id="f47a9-175">**ExecutablePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f47a9-176">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f47a9-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f47a9-177">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f47a9-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f47a9-178">Qualificadores: [**Privileges**](../wmisdk/standard-wmi-qualifiers.md) ("SeDebugPrivilege"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api de \| ferramentas de ajuda da ferramenta \| [**MODULEENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-moduleentry32) \| szExePath"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("caminho executável")</span><span class="sxs-lookup"><span data-stu-id="f47a9-178">Qualifiers: [**Privileges**](../wmisdk/standard-wmi-qualifiers.md) ("SeDebugPrivilege"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Tool Help Structures\|[**MODULEENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-moduleentry32)\|szExePath"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Executable Path")</span></span>
</dt> </dl>

<span data-ttu-id="f47a9-179">Caminho para o arquivo executável do processo.</span><span class="sxs-lookup"><span data-stu-id="f47a9-179">Path to the executable file of the process.</span></span>

<span data-ttu-id="f47a9-180">Exemplo: "C: \\ Windows \\ System \\Explorer.Exe"</span><span class="sxs-lookup"><span data-stu-id="f47a9-180">Example: "C:\\Windows\\System\\Explorer.Exe"</span></span>

</dd> <dt>

<span data-ttu-id="f47a9-181">**ExecutionState**</span><span class="sxs-lookup"><span data-stu-id="f47a9-181">**ExecutionState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f47a9-182">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f47a9-182">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f47a9-183">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f47a9-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f47a9-184">Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("estado de execução")</span><span class="sxs-lookup"><span data-stu-id="f47a9-184">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Execution State")</span></span>
</dt> </dl>

<span data-ttu-id="f47a9-185">Condição operacional atual do processo.</span><span class="sxs-lookup"><span data-stu-id="f47a9-185">Current operating condition of the process.</span></span>

<span data-ttu-id="f47a9-186">Essa propriedade é herdada [**do \_ processo CIM**](cim-process.md).</span><span class="sxs-lookup"><span data-stu-id="f47a9-186">This property is inherited from [**CIM\_Process**](cim-process.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f47a9-187"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="f47a9-187"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="f47a9-188">Unknown</span><span class="sxs-lookup"><span data-stu-id="f47a9-188">Unknown</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="f47a9-189"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="f47a9-189"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="f47a9-190">Outro</span><span class="sxs-lookup"><span data-stu-id="f47a9-190">Other</span></span>

</dd> <dt>

<span id="Ready"></span><span id="ready"></span><span id="READY"></span>

<span data-ttu-id="f47a9-191"><span id="Ready"></span><span id="ready"></span><span id="READY"></span>**Pronto** (2)</span><span class="sxs-lookup"><span data-stu-id="f47a9-191"><span id="Ready"></span><span id="ready"></span><span id="READY"></span>**Ready** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="f47a9-192"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Em execução** (3)</span><span class="sxs-lookup"><span data-stu-id="f47a9-192"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Blocked"></span><span id="blocked"></span><span id="BLOCKED"></span>

<span data-ttu-id="f47a9-193"><span id="Blocked"></span><span id="blocked"></span><span id="BLOCKED"></span>**Bloqueado** (4)</span><span class="sxs-lookup"><span data-stu-id="f47a9-193"><span id="Blocked"></span><span id="blocked"></span><span id="BLOCKED"></span>**Blocked** (4)</span></span>


</dt> <dd>

<span data-ttu-id="f47a9-194">Bloqueado</span><span class="sxs-lookup"><span data-stu-id="f47a9-194">Blocked</span></span>

</dd> <dt>

<span id="Suspended_Blocked"></span><span id="suspended_blocked"></span><span id="SUSPENDED_BLOCKED"></span>

<span data-ttu-id="f47a9-195"><span id="Suspended_Blocked"></span><span id="suspended_blocked"></span><span id="SUSPENDED_BLOCKED"></span>**Bloqueado suspenso** (5)</span><span class="sxs-lookup"><span data-stu-id="f47a9-195"><span id="Suspended_Blocked"></span><span id="suspended_blocked"></span><span id="SUSPENDED_BLOCKED"></span>**Suspended Blocked** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Suspended_Ready"></span><span id="suspended_ready"></span><span id="SUSPENDED_READY"></span>

<span data-ttu-id="f47a9-196"><span id="Suspended_Ready"></span><span id="suspended_ready"></span><span id="SUSPENDED_READY"></span>**Pronto suspenso** (6)</span><span class="sxs-lookup"><span data-stu-id="f47a9-196"><span id="Suspended_Ready"></span><span id="suspended_ready"></span><span id="SUSPENDED_READY"></span>**Suspended Ready** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>

<span data-ttu-id="f47a9-197"><span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>**Encerrado** (7)</span><span class="sxs-lookup"><span data-stu-id="f47a9-197"><span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>**Terminated** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>

<span data-ttu-id="f47a9-198"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Parado** (8)</span><span class="sxs-lookup"><span data-stu-id="f47a9-198"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Growing"></span><span id="growing"></span><span id="GROWING"></span>

<span data-ttu-id="f47a9-199"><span id="Growing"></span><span id="growing"></span><span id="GROWING"></span>**Crescendo** (9)</span><span class="sxs-lookup"><span data-stu-id="f47a9-199"><span id="Growing"></span><span id="growing"></span><span id="GROWING"></span>**Growing** (9)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f47a9-200">**Handle**</span><span class="sxs-lookup"><span data-stu-id="f47a9-200">**Handle**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f47a9-201">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f47a9-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f47a9-202">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f47a9-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f47a9-203">Qualificadores: [**Key**](../wmisdk/key-qualifier.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Handle")</span><span class="sxs-lookup"><span data-stu-id="f47a9-203">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Handle")</span></span>
</dt> </dl>

<span data-ttu-id="f47a9-204">Identificador de processo.</span><span class="sxs-lookup"><span data-stu-id="f47a9-204">Process identifier.</span></span>

<span data-ttu-id="f47a9-205">Essa propriedade é herdada [**do \_ processo CIM**](cim-process.md).</span><span class="sxs-lookup"><span data-stu-id="f47a9-205">This property is inherited from [**CIM\_Process**](cim-process.md).</span></span>

</dd> <dt>

<span data-ttu-id="f47a9-206">**HandleCount**</span><span class="sxs-lookup"><span data-stu-id="f47a9-206">**HandleCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f47a9-207">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f47a9-207">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f47a9-208">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f47a9-208">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f47a9-209">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api de \| status do processo de processamento do \| sistema \_ \_ \| HandleCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("contagem de identificadores")</span><span class="sxs-lookup"><span data-stu-id="f47a9-209">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process Status\|SYSTEM\_PROCESS\_INFORMATION\|HandleCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Handle Count")</span></span>
</dt> </dl>

<span data-ttu-id="f47a9-210">Número total de identificadores abertos de Propriedade do processo.</span><span class="sxs-lookup"><span data-stu-id="f47a9-210">Total number of open handles owned by the process.</span></span> <span data-ttu-id="f47a9-211">**HandleCount** é a soma dos identificadores abertos no momento por cada thread nesse processo.</span><span class="sxs-lookup"><span data-stu-id="f47a9-211">**HandleCount** is the sum of the handles currently open by each thread in this process.</span></span> <span data-ttu-id="f47a9-212">Um identificador é usado para examinar ou modificar os recursos do sistema.</span><span class="sxs-lookup"><span data-stu-id="f47a9-212">A handle is used to examine or modify the system resources.</span></span> <span data-ttu-id="f47a9-213">Cada identificador tem uma entrada em uma tabela mantida internamente.</span><span class="sxs-lookup"><span data-stu-id="f47a9-213">Each handle has an entry in a table that is maintained internally.</span></span> <span data-ttu-id="f47a9-214">As entradas contêm os endereços dos recursos e dados para identificar o tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="f47a9-214">Entries contain the addresses of the resources and data to identify the resource type.</span></span>

</dd> <dt>

<span data-ttu-id="f47a9-215">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="f47a9-215">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f47a9-216">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="f47a9-216">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f47a9-217">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f47a9-217">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f47a9-218">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="f47a9-218">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="f47a9-219">Data em que um objeto é instalado.</span><span class="sxs-lookup"><span data-stu-id="f47a9-219">Date an object is installed.</span></span> <span data-ttu-id="f47a9-220">O objeto pode ser instalado sem que um valor seja gravado nessa propriedade.</span><span class="sxs-lookup"><span data-stu-id="f47a9-220">The object may be installed without a value being written to this property.</span></span>

<span data-ttu-id="f47a9-221">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f47a9-221">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f47a9-222">**KernelModeTime**</span><span class="sxs-lookup"><span data-stu-id="f47a9-222">**KernelModeTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f47a9-223">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f47a9-223">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f47a9-224">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f47a9-224">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f47a9-225">Qualificadores: [**override**](../wmisdk/standard-qualifiers.md) ("KernelModeTime"), [**Units**](../wmisdk/standard-qualifiers.md) ("100 nanossegundos")</span><span class="sxs-lookup"><span data-stu-id="f47a9-225">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("KernelModeTime"), [**Units**](../wmisdk/standard-qualifiers.md) ("100 nanoseconds")</span></span>
</dt> </dl>

<span data-ttu-id="f47a9-226">Tempo no modo kernel, em milissegundos.</span><span class="sxs-lookup"><span data-stu-id="f47a9-226">Time in kernel mode, in milliseconds.</span></span> <span data-ttu-id="f47a9-227">Se essas informações não estiverem disponíveis, use um valor de 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="f47a9-227">If this information is not available, use a value of 0 (zero).</span></span>

<span data-ttu-id="f47a9-228">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="f47a9-228">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="f47a9-229">**MaximumWorkingSetSize**</span><span class="sxs-lookup"><span data-stu-id="f47a9-229">**MaximumWorkingSetSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f47a9-230">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f47a9-230">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f47a9-231">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f47a9-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f47a9-232">Qualificadores: [**Privileges**](../wmisdk/standard-wmi-qualifiers.md) ("SeDebugPrivilege"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32 \| Winnt. H \| cota \_ limita \| MaximumWorkingSetSize "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" tamanho máximo do conjunto de trabalho "), [**unidades**](../wmisdk/standard-qualifiers.md) (" quilobytes ")</span><span class="sxs-lookup"><span data-stu-id="f47a9-232">Qualifiers: [**Privileges**](../wmisdk/standard-wmi-qualifiers.md) ("SeDebugPrivilege"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\|WINNT.H\|QUOTA\_LIMITS\|MaximumWorkingSetSize"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Maximum Working Set Size"), [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="f47a9-233">Tamanho máximo do conjunto de trabalho do processo.</span><span class="sxs-lookup"><span data-stu-id="f47a9-233">Maximum working set size of the process.</span></span> <span data-ttu-id="f47a9-234">O conjunto de trabalho de um processo é o conjunto de páginas de memória visíveis para o processo na RAM física.</span><span class="sxs-lookup"><span data-stu-id="f47a9-234">The working set of a process is the set of memory pages visible to the process in physical RAM.</span></span> <span data-ttu-id="f47a9-235">Essas páginas são residentes e estão disponíveis para um aplicativo usar sem disparar uma falha de página.</span><span class="sxs-lookup"><span data-stu-id="f47a9-235">These pages are resident, and available for an application to use without triggering a page fault.</span></span>

<span data-ttu-id="f47a9-236">Exemplo: 1413120</span><span class="sxs-lookup"><span data-stu-id="f47a9-236">Example: 1413120</span></span>

</dd> <dt>

<span data-ttu-id="f47a9-237">**MinimumWorkingSetSize**</span><span class="sxs-lookup"><span data-stu-id="f47a9-237">**MinimumWorkingSetSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f47a9-238">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f47a9-238">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f47a9-239">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f47a9-239">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f47a9-240">Qualificadores: [**Privileges**](../wmisdk/standard-wmi-qualifiers.md) ("SeDebugPrivilege"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32 \| Winnt. H \| cota \_ limita \| MinimumWorkingSetSize "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" tamanho mínimo do conjunto de trabalho "), [**unidades**](../wmisdk/standard-qualifiers.md) (" quilobytes ")</span><span class="sxs-lookup"><span data-stu-id="f47a9-240">Qualifiers: [**Privileges**](../wmisdk/standard-wmi-qualifiers.md) ("SeDebugPrivilege"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\|WINNT.H\|QUOTA\_LIMITS\|MinimumWorkingSetSize"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Minimum Working Set Size"), [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="f47a9-241">Tamanho mínimo do conjunto de trabalho do processo.</span><span class="sxs-lookup"><span data-stu-id="f47a9-241">Minimum working set size of the process.</span></span> <span data-ttu-id="f47a9-242">O conjunto de trabalho de um processo é o conjunto de páginas de memória visíveis para o processo na RAM física.</span><span class="sxs-lookup"><span data-stu-id="f47a9-242">The working set of a process is the set of memory pages visible to the process in physical RAM.</span></span> <span data-ttu-id="f47a9-243">Essas páginas são residentes e estão disponíveis para um aplicativo usar sem disparar uma falha de página.</span><span class="sxs-lookup"><span data-stu-id="f47a9-243">These pages are resident and available for an application to use without triggering a page fault.</span></span>

<span data-ttu-id="f47a9-244">Exemplo: 20480</span><span class="sxs-lookup"><span data-stu-id="f47a9-244">Example: 20480</span></span>

</dd> <dt>

<span data-ttu-id="f47a9-245">**Nome**</span><span class="sxs-lookup"><span data-stu-id="f47a9-245">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f47a9-246">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f47a9-246">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f47a9-247">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f47a9-247">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f47a9-248">Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="f47a9-248">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="f47a9-249">Nome do arquivo executável responsável pelo processo, equivalente à propriedade nome da imagem no Gerenciador de tarefas.</span><span class="sxs-lookup"><span data-stu-id="f47a9-249">Name of the executable file responsible for the process, equivalent to the Image Name property in Task Manager.</span></span>

<span data-ttu-id="f47a9-250">Quando herdado por uma subclasse, a propriedade pode ser substituída para ser uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="f47a9-250">When inherited by a subclass, the property can be overridden to be a key property.</span></span> <span data-ttu-id="f47a9-251">O nome é embutido em código no próprio aplicativo e não é afetado pela alteração do nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="f47a9-251">The name is hard-coded into the application itself and is not affected by changing the file name.</span></span> <span data-ttu-id="f47a9-252">Por exemplo, mesmo se você renomear Calc.exe, o nome Calc.exe ainda será exibido no Gerenciador de tarefas e em qualquer script WMI que recupere o nome do processo.</span><span class="sxs-lookup"><span data-stu-id="f47a9-252">For example, even if you rename Calc.exe, the name Calc.exe will still appear in Task Manager and in any WMI scripts that retrieve the process name.</span></span>

<span data-ttu-id="f47a9-253">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f47a9-253">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f47a9-254">**OSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="f47a9-254">**OSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f47a9-255">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f47a9-255">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f47a9-256">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f47a9-256">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f47a9-257">Qualificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ("sistema [**\_ operacional CIM**](cim-operatingsystem.md).**CreationClassName**"), [**\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" nome da classe do sistema operacional ")</span><span class="sxs-lookup"><span data-stu-id="f47a9-257">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Operating System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="f47a9-258">Nome da classe de criação do sistema operacional de escopo.</span><span class="sxs-lookup"><span data-stu-id="f47a9-258">Creation class name of the scoping operating system.</span></span>

<span data-ttu-id="f47a9-259">Essa propriedade é herdada [**do \_ processo CIM**](cim-process.md).</span><span class="sxs-lookup"><span data-stu-id="f47a9-259">This property is inherited from [**CIM\_Process**](cim-process.md).</span></span>

</dd> <dt>

<span data-ttu-id="f47a9-260">**OSName**</span><span class="sxs-lookup"><span data-stu-id="f47a9-260">**OSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f47a9-261">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f47a9-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f47a9-262">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f47a9-262">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f47a9-263">Qualificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ("sistema [**\_ operacional CIM**](cim-operatingsystem.md).**Name**"), [**CIM \_ Key**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" nome do sistema operacional ")</span><span class="sxs-lookup"><span data-stu-id="f47a9-263">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Operating System Name")</span></span>
</dt> </dl>

<span data-ttu-id="f47a9-264">Nome do sistema operacional de escopo.</span><span class="sxs-lookup"><span data-stu-id="f47a9-264">Name of the scoping operating system.</span></span>

<span data-ttu-id="f47a9-265">Essa propriedade é herdada [**do \_ processo CIM**](cim-process.md).</span><span class="sxs-lookup"><span data-stu-id="f47a9-265">This property is inherited from [**CIM\_Process**](cim-process.md).</span></span>

</dd> <dt>

<span data-ttu-id="f47a9-266">**OtherOperationCount**</span><span class="sxs-lookup"><span data-stu-id="f47a9-266">**OtherOperationCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f47a9-267">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f47a9-267">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f47a9-268">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f47a9-268">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f47a9-269">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| processo e estruturas de thread \| informações do processo do sistema \_ \_ \| OtherOperationCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("outra contagem de operação")</span><span class="sxs-lookup"><span data-stu-id="f47a9-269">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|SYSTEM\_PROCESS\_INFORMATION\|OtherOperationCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Other Operation Count")</span></span>
</dt> </dl>

<span data-ttu-id="f47a9-270">Número de operações de e/s executadas que não são operações de leitura ou gravação.</span><span class="sxs-lookup"><span data-stu-id="f47a9-270">Number of I/O operations performed that are not read or write operations.</span></span>

<span data-ttu-id="f47a9-271">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="f47a9-271">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="f47a9-272">**OtherTransferCount**</span><span class="sxs-lookup"><span data-stu-id="f47a9-272">**OtherTransferCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f47a9-273">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f47a9-273">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f47a9-274">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f47a9-274">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f47a9-275">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| processo e estruturas de thread \| informações do processo do sistema \_ \_ \| OtherTransferCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("outras contagens de transferência"), [**unidades**](../wmisdk/standard-qualifiers.md) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="f47a9-275">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|SYSTEM\_PROCESS\_INFORMATION\|OtherTransferCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Other Transfer Count"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="f47a9-276">Quantidade de dados transferidos durante operações que não são operações de leitura ou de gravação.</span><span class="sxs-lookup"><span data-stu-id="f47a9-276">Amount of data transferred during operations that are not read or write operations.</span></span>

<span data-ttu-id="f47a9-277">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="f47a9-277">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="f47a9-278">**PageFaults**</span><span class="sxs-lookup"><span data-stu-id="f47a9-278">**PageFaults**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f47a9-279">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f47a9-279">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f47a9-280">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f47a9-280">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f47a9-281">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| de status \| \_ do processo \_ de processos do sistema \| PageFaultCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("número de falhas de página")</span><span class="sxs-lookup"><span data-stu-id="f47a9-281">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process Status\|SYSTEM\_PROCESS\_INFORMATION\|PageFaultCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Number Of Page Faults")</span></span>
</dt> </dl>

<span data-ttu-id="f47a9-282">Número de falhas de página que um processo gera.</span><span class="sxs-lookup"><span data-stu-id="f47a9-282">Number of page faults that a process generates.</span></span>

<span data-ttu-id="f47a9-283">Exemplo: 10</span><span class="sxs-lookup"><span data-stu-id="f47a9-283">Example: 10</span></span>

</dd> <dt>

<span data-ttu-id="f47a9-284">**PageFileUsage**</span><span class="sxs-lookup"><span data-stu-id="f47a9-284">**PageFileUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f47a9-285">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f47a9-285">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f47a9-286">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f47a9-286">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f47a9-287">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api processo de status do processo do \| \| sistema \_ \_ \| PagefileUsage"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("uso do arquivo de paginação"), [**unidades**](../wmisdk/standard-qualifiers.md) ("quilobytes")</span><span class="sxs-lookup"><span data-stu-id="f47a9-287">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process Status\|SYSTEM\_PROCESS\_INFORMATION\|PagefileUsage"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Page File Usage"), [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="f47a9-288">Quantidade de espaço de arquivo de paginação que um processo está usando no momento.</span><span class="sxs-lookup"><span data-stu-id="f47a9-288">Amount of page file space that a process is using currently.</span></span> <span data-ttu-id="f47a9-289">Esse valor é consistente com o valor de **VMSize** em TaskMgr.exe.</span><span class="sxs-lookup"><span data-stu-id="f47a9-289">This value is consistent with the **VMSize** value in TaskMgr.exe.</span></span>

<span data-ttu-id="f47a9-290">Exemplo: 102435</span><span class="sxs-lookup"><span data-stu-id="f47a9-290">Example: 102435</span></span>

</dd> <dt>

<span data-ttu-id="f47a9-291">**ParentProcessId**</span><span class="sxs-lookup"><span data-stu-id="f47a9-291">**ParentProcessId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f47a9-292">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f47a9-292">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f47a9-293">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f47a9-293">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f47a9-294">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api processo de status do processo do \| \| sistema \_ \_ \| InheritedFromUniqueProcessId"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("ID do processo pai")</span><span class="sxs-lookup"><span data-stu-id="f47a9-294">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process Status\|SYSTEM\_PROCESS\_INFORMATION\|InheritedFromUniqueProcessId"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Parent Process Id")</span></span>
</dt> </dl>

<span data-ttu-id="f47a9-295">Identificador exclusivo do processo que cria um processo.</span><span class="sxs-lookup"><span data-stu-id="f47a9-295">Unique identifier of the process that creates a process.</span></span> <span data-ttu-id="f47a9-296">Os números de identificador de processo são reutilizados, portanto, eles identificam apenas um processo durante o tempo de vida desse processo.</span><span class="sxs-lookup"><span data-stu-id="f47a9-296">Process identifier numbers are reused, so they only identify a process for the lifetime of that process.</span></span> <span data-ttu-id="f47a9-297">É possível que o processo identificado pelo **ParentProcessID** seja encerrado; portanto, **ParentProcessID** pode não se referir a um processo em execução.</span><span class="sxs-lookup"><span data-stu-id="f47a9-297">It is possible that the process identified by **ParentProcessId** is terminated, so **ParentProcessId** may not refer to a running process.</span></span> <span data-ttu-id="f47a9-298">Também é possível que o **ParentProcessID** incorretamente faça referência a um processo que reutiliza um identificador de processo.</span><span class="sxs-lookup"><span data-stu-id="f47a9-298">It is also possible that **ParentProcessId** incorrectly refers to a process that reuses a process identifier.</span></span> <span data-ttu-id="f47a9-299">Você pode usar a propriedade **CreationDate** para determinar se o pai especificado foi criado depois que o processo representado por essa instância de **\_ processo Win32** foi criado.</span><span class="sxs-lookup"><span data-stu-id="f47a9-299">You can use the **CreationDate** property to determine whether the specified parent was created after the process represented by this **Win32\_Process** instance was created.</span></span>

</dd> <dt>

<span data-ttu-id="f47a9-300">**PeakPageFileUsage**</span><span class="sxs-lookup"><span data-stu-id="f47a9-300">**PeakPageFileUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f47a9-301">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f47a9-301">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f47a9-302">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f47a9-302">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f47a9-303">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api de \| status do processo de estado do \| sistema \_ \_ \| PeakPagefileUsage"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("uso de arquivo de página de pico"), [**unidades**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span><span class="sxs-lookup"><span data-stu-id="f47a9-303">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process Status\|SYSTEM\_PROCESS\_INFORMATION\|PeakPagefileUsage"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Peak Page File Usage"), [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="f47a9-304">Quantidade máxima de espaço de arquivo de paginação usada durante a vida útil de um processo.</span><span class="sxs-lookup"><span data-stu-id="f47a9-304">Maximum amount of page file space used during the life of a process.</span></span>

<span data-ttu-id="f47a9-305">Exemplo: 102367</span><span class="sxs-lookup"><span data-stu-id="f47a9-305">Example: 102367</span></span>

</dd> <dt>

<span data-ttu-id="f47a9-306">**PeakVirtualSize**</span><span class="sxs-lookup"><span data-stu-id="f47a9-306">**PeakVirtualSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f47a9-307">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f47a9-307">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f47a9-308">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f47a9-308">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f47a9-309">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api processo de status do processo do \| \| sistema \_ \_ \| PeakVirtualSize"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("pico de uso do espaço de endereço de virtual"), [**unidades**](../wmisdk/standard-qualifiers.md) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="f47a9-309">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process Status\|SYSTEM\_PROCESS\_INFORMATION\|PeakVirtualSize"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Peak Virual Address Space Usage"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="f47a9-310">Espaço de endereço virtual máximo que um processo usa a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="f47a9-310">Maximum virtual address space a process uses at any one time.</span></span> <span data-ttu-id="f47a9-311">O uso do espaço de endereço virtual não implica necessariamente o uso correspondente do disco ou das páginas de memória principal.</span><span class="sxs-lookup"><span data-stu-id="f47a9-311">Using virtual address space does not necessarily imply corresponding use of either disk or main memory pages.</span></span> <span data-ttu-id="f47a9-312">No entanto, o espaço virtual é finito e usar muito o processo pode não ser capaz de carregar bibliotecas.</span><span class="sxs-lookup"><span data-stu-id="f47a9-312">However, virtual space is finite, and by using too much the process might not be able to load libraries.</span></span>

<span data-ttu-id="f47a9-313">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="f47a9-313">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="f47a9-314">**PeakWorkingSetSize**</span><span class="sxs-lookup"><span data-stu-id="f47a9-314">**PeakWorkingSetSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f47a9-315">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f47a9-315">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f47a9-316">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f47a9-316">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f47a9-317">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api estado do processo do \| \| sistema status \_ \_ \| PeakWorkingSetSize"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("tamanho do conjunto de trabalho de pico"), [**unidades**](../wmisdk/standard-qualifiers.md) ("quilobytes")</span><span class="sxs-lookup"><span data-stu-id="f47a9-317">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process Status\|SYSTEM\_PROCESS\_INFORMATION\|PeakWorkingSetSize"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Peak Working Set Size"), [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="f47a9-318">Tamanho do conjunto de trabalho de pico de um processo.</span><span class="sxs-lookup"><span data-stu-id="f47a9-318">Peak working set size of a process.</span></span>

<span data-ttu-id="f47a9-319">Exemplo: 1413120</span><span class="sxs-lookup"><span data-stu-id="f47a9-319">Example: 1413120</span></span>

</dd> <dt>

<span data-ttu-id="f47a9-320">**Prioridade**</span><span class="sxs-lookup"><span data-stu-id="f47a9-320">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f47a9-321">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f47a9-321">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f47a9-322">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f47a9-322">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f47a9-323">Qualificadores: [**substituir**](../wmisdk/standard-qualifiers.md) ("Priority"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| processo de estado do sistema de status \| \_ \_ \| BasePriority"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Priority")</span><span class="sxs-lookup"><span data-stu-id="f47a9-323">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Priority"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process Status\|SYSTEM\_PROCESS\_INFORMATION\|BasePriority"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Priority")</span></span>
</dt> </dl>

<span data-ttu-id="f47a9-324">Prioridade de agendamento de um processo em um sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="f47a9-324">Scheduling priority of a process within an operating system.</span></span> <span data-ttu-id="f47a9-325">Quanto maior o valor, maior a prioridade que um processo recebe.</span><span class="sxs-lookup"><span data-stu-id="f47a9-325">The higher the value, the higher priority a process receives.</span></span> <span data-ttu-id="f47a9-326">Os valores de prioridade podem variar de 0 (zero), que é a prioridade mais baixa para 31, que é a prioridade mais alta.</span><span class="sxs-lookup"><span data-stu-id="f47a9-326">Priority values can range from 0 (zero), which is the lowest priority to 31, which is highest priority.</span></span>

<span data-ttu-id="f47a9-327">Exemplo: 7</span><span class="sxs-lookup"><span data-stu-id="f47a9-327">Example: 7</span></span>

</dd> <dt>

<span data-ttu-id="f47a9-328">**PrivatePageCount**</span><span class="sxs-lookup"><span data-stu-id="f47a9-328">**PrivatePageCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f47a9-329">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f47a9-329">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f47a9-330">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f47a9-330">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f47a9-331">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api de \| status do processo de processos do \| sistema \_ \_ \| PrivatePageCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("contagem de páginas particulares")</span><span class="sxs-lookup"><span data-stu-id="f47a9-331">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process Status\|SYSTEM\_PROCESS\_INFORMATION\|PrivatePageCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Private Page Count")</span></span>
</dt> </dl>

<span data-ttu-id="f47a9-332">Número atual de páginas alocadas que só podem ser acessadas pelo processo representado por essa instância de **\_ processo Win32** .</span><span class="sxs-lookup"><span data-stu-id="f47a9-332">Current number of pages allocated that are only accessible to the process represented by this **Win32\_Process** instance.</span></span>

<span data-ttu-id="f47a9-333">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="f47a9-333">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="f47a9-334">**ProcessId**</span><span class="sxs-lookup"><span data-stu-id="f47a9-334">**ProcessId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f47a9-335">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f47a9-335">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f47a9-336">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f47a9-336">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f47a9-337">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api processo \| e estruturas de thread \| [**\_ informações de processo**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-process_information) \| dwProcessId"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("ID do processo")</span><span class="sxs-lookup"><span data-stu-id="f47a9-337">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|[**PROCESS\_INFORMATION**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-process_information)\|dwProcessId "), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Process Id")</span></span>
</dt> </dl>

<span data-ttu-id="f47a9-338">Identificador numérico usado para distinguir um processo de outro.</span><span class="sxs-lookup"><span data-stu-id="f47a9-338">Numeric identifier used to distinguish one process from another.</span></span> <span data-ttu-id="f47a9-339">As ProcessIDs são válidas do tempo de criação do processo para processar o encerramento.</span><span class="sxs-lookup"><span data-stu-id="f47a9-339">ProcessIDs are valid from process creation time to process termination.</span></span> <span data-ttu-id="f47a9-340">Após o encerramento, esse mesmo identificador numérico pode ser aplicado a um novo processo.</span><span class="sxs-lookup"><span data-stu-id="f47a9-340">Upon termination, that same numeric identifier can be applied to a new process.</span></span>

<span data-ttu-id="f47a9-341">Isso significa que você não pode usar o ProcessID sozinho para monitorar um processo específico.</span><span class="sxs-lookup"><span data-stu-id="f47a9-341">This means that you cannot use ProcessID alone to monitor a particular process.</span></span> <span data-ttu-id="f47a9-342">Por exemplo, um aplicativo pode ter um ProcessID de 7 e, em seguida, falhar.</span><span class="sxs-lookup"><span data-stu-id="f47a9-342">For example, an application could have a ProcessID of 7, and then fail.</span></span> <span data-ttu-id="f47a9-343">Quando um novo processo é iniciado, o novo processo pode ser atribuído a ProcessID 7.</span><span class="sxs-lookup"><span data-stu-id="f47a9-343">When a new process is started, the new process could be assigned ProcessID 7.</span></span> <span data-ttu-id="f47a9-344">Um script que é verificado apenas para um ProcessID especificado poderia, portanto, ser "enganado" para pensar que o aplicativo original ainda estava em execução.</span><span class="sxs-lookup"><span data-stu-id="f47a9-344">A script that checked only for a specified ProcessID could thus be "fooled" into thinking that the original application was still running.</span></span>

</dd> <dt>

<span data-ttu-id="f47a9-345">**QuotaNonPagedPoolUsage**</span><span class="sxs-lookup"><span data-stu-id="f47a9-345">**QuotaNonPagedPoolUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f47a9-346">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f47a9-346">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f47a9-347">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f47a9-347">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f47a9-348">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api processo de status do processo do \| \| sistema \_ \_ \| QuotaNonPagedPoolUsage"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("cota de uso de pool não paginável")</span><span class="sxs-lookup"><span data-stu-id="f47a9-348">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process Status\|SYSTEM\_PROCESS\_INFORMATION\|QuotaNonPagedPoolUsage"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Non-Paged Pool Usage Quota")</span></span>
</dt> </dl>

<span data-ttu-id="f47a9-349">Valor da cota de uso de pool não paginável para um processo.</span><span class="sxs-lookup"><span data-stu-id="f47a9-349">Quota amount of nonpaged pool usage for a process.</span></span>

<span data-ttu-id="f47a9-350">Exemplo: 15</span><span class="sxs-lookup"><span data-stu-id="f47a9-350">Example: 15</span></span>

</dd> <dt>

<span data-ttu-id="f47a9-351">**QuotaPagedPoolUsage**</span><span class="sxs-lookup"><span data-stu-id="f47a9-351">**QuotaPagedPoolUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f47a9-352">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f47a9-352">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f47a9-353">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f47a9-353">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f47a9-354">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api processo de status do processo do \| \| sistema \_ \_ \| QuotaPagedPoolUsage"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("cota de uso do pool paginado")</span><span class="sxs-lookup"><span data-stu-id="f47a9-354">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process Status\|SYSTEM\_PROCESS\_INFORMATION\|QuotaPagedPoolUsage"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Paged Pool Usage Quota")</span></span>
</dt> </dl>

<span data-ttu-id="f47a9-355">Quantidade de cota de uso de pool paginável para um processo.</span><span class="sxs-lookup"><span data-stu-id="f47a9-355">Quota amount of paged pool usage for a process.</span></span>

<span data-ttu-id="f47a9-356">Exemplo: 22</span><span class="sxs-lookup"><span data-stu-id="f47a9-356">Example: 22</span></span>

</dd> <dt>

<span data-ttu-id="f47a9-357">**QuotaPeakNonPagedPoolUsage**</span><span class="sxs-lookup"><span data-stu-id="f47a9-357">**QuotaPeakNonPagedPoolUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f47a9-358">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f47a9-358">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f47a9-359">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f47a9-359">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f47a9-360">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api processo de status do processo do \| \| sistema \_ \_ \| QuotaPeakNonPagedPoolUsage"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("pico de cota de uso de pool não paginável")</span><span class="sxs-lookup"><span data-stu-id="f47a9-360">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process Status\|SYSTEM\_PROCESS\_INFORMATION\|QuotaPeakNonPagedPoolUsage"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Peak Non-Paged Pool Usage Quota")</span></span>
</dt> </dl>

<span data-ttu-id="f47a9-361">Valor da cota de pico do uso do pool não paginado para um processo.</span><span class="sxs-lookup"><span data-stu-id="f47a9-361">Peak quota amount of nonpaged pool usage for a process.</span></span>

<span data-ttu-id="f47a9-362">Exemplo: 31</span><span class="sxs-lookup"><span data-stu-id="f47a9-362">Example: 31</span></span>

</dd> <dt>

<span data-ttu-id="f47a9-363">**QuotaPeakPagedPoolUsage**</span><span class="sxs-lookup"><span data-stu-id="f47a9-363">**QuotaPeakPagedPoolUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f47a9-364">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f47a9-364">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f47a9-365">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f47a9-365">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f47a9-366">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api processo de status do processo do \| \| sistema \_ \_ \| QuotaPeakPagedPoolUsage"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("cota de uso do pool de picos de página")</span><span class="sxs-lookup"><span data-stu-id="f47a9-366">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process Status\|SYSTEM\_PROCESS\_INFORMATION\|QuotaPeakPagedPoolUsage"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Peak Paged Pool Usage Quota")</span></span>
</dt> </dl>

<span data-ttu-id="f47a9-367">Valor da cota de pico do uso do pool paginado para um processo.</span><span class="sxs-lookup"><span data-stu-id="f47a9-367">Peak quota amount of paged pool usage for a process.</span></span>

<span data-ttu-id="f47a9-368">Exemplo: 31</span><span class="sxs-lookup"><span data-stu-id="f47a9-368">Example: 31</span></span>

</dd> <dt>

<span data-ttu-id="f47a9-369">**ReadOperationCount**</span><span class="sxs-lookup"><span data-stu-id="f47a9-369">**ReadOperationCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f47a9-370">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f47a9-370">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f47a9-371">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f47a9-371">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f47a9-372">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| processo e estruturas de thread \| informações do processo do sistema \_ \_ \| ReadOperationCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("contagem de operação de leitura")</span><span class="sxs-lookup"><span data-stu-id="f47a9-372">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|SYSTEM\_PROCESS\_INFORMATION\|ReadOperationCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Read Operation Count")</span></span>
</dt> </dl>

<span data-ttu-id="f47a9-373">Número de operações de leitura executadas.</span><span class="sxs-lookup"><span data-stu-id="f47a9-373">Number of read operations performed.</span></span>

<span data-ttu-id="f47a9-374">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="f47a9-374">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="f47a9-375">**ReadTransferCount**</span><span class="sxs-lookup"><span data-stu-id="f47a9-375">**ReadTransferCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f47a9-376">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f47a9-376">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f47a9-377">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f47a9-377">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f47a9-378">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| processo e estruturas de thread \| informações do processo do sistema \_ \_ \| ReadTransferCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("contagem de transferência de leitura"), [**unidades**](../wmisdk/standard-qualifiers.md) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="f47a9-378">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|SYSTEM\_PROCESS\_INFORMATION\|ReadTransferCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Read Transfer Count"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="f47a9-379">Quantidade de dados lidos.</span><span class="sxs-lookup"><span data-stu-id="f47a9-379">Amount of data read.</span></span>

<span data-ttu-id="f47a9-380">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="f47a9-380">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="f47a9-381">**SessionId**</span><span class="sxs-lookup"><span data-stu-id="f47a9-381">**SessionId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f47a9-382">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f47a9-382">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f47a9-383">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f47a9-383">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f47a9-384">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api de \| status do processo de processamento do sistema ID do processo \| \_ \_ \| "), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("ID da sessão")</span><span class="sxs-lookup"><span data-stu-id="f47a9-384">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process Status\|SYSTEM\_PROCESS\_INFORMATION\|SessionId"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Session Id")</span></span>
</dt> </dl>

<span data-ttu-id="f47a9-385">Identificador exclusivo que um sistema operacional gera quando uma sessão é criada.</span><span class="sxs-lookup"><span data-stu-id="f47a9-385">Unique identifier that an operating system generates when a session is created.</span></span> <span data-ttu-id="f47a9-386">Uma sessão abrange um período de tempo desde o logon até o logoff de um sistema específico.</span><span class="sxs-lookup"><span data-stu-id="f47a9-386">A session spans a period of time from logon until logoff from a specific system.</span></span>

</dd> <dt>

<span data-ttu-id="f47a9-387">**Status**</span><span class="sxs-lookup"><span data-stu-id="f47a9-387">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f47a9-388">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f47a9-388">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f47a9-389">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f47a9-389">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f47a9-390">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="f47a9-390">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="f47a9-391">Esta propriedade não está implementada e não é preenchida para nenhuma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="f47a9-391">This property is not implemented and does not get populated for any instance of this class.</span></span> <span data-ttu-id="f47a9-392">Ele é sempre **nulo**.</span><span class="sxs-lookup"><span data-stu-id="f47a9-392">It is always **NULL**.</span></span>

<span data-ttu-id="f47a9-393">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f47a9-393">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="f47a9-394">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="f47a9-394">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="f47a9-395">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="f47a9-395">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="f47a9-396">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="f47a9-396">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="f47a9-397">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="f47a9-397">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f47a9-398">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="f47a9-398">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="f47a9-399">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="f47a9-399">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="f47a9-400">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="f47a9-400">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="f47a9-401">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="f47a9-401">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="f47a9-402">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="f47a9-402">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="f47a9-403">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="f47a9-403">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="f47a9-404">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="f47a9-404">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="f47a9-405">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="f47a9-405">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="f47a9-406">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="f47a9-406">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f47a9-407">**TerminationDate**</span><span class="sxs-lookup"><span data-stu-id="f47a9-407">**TerminationDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f47a9-408">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="f47a9-408">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f47a9-409">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f47a9-409">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f47a9-410">Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("data de término")</span><span class="sxs-lookup"><span data-stu-id="f47a9-410">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Termination Date")</span></span>
</dt> </dl>

<span data-ttu-id="f47a9-411">O processo foi interrompido ou encerrado.</span><span class="sxs-lookup"><span data-stu-id="f47a9-411">Process was stopped or terminated.</span></span> <span data-ttu-id="f47a9-412">Para obter o tempo de encerramento, um identificador para o processo deve ser mantido aberto.</span><span class="sxs-lookup"><span data-stu-id="f47a9-412">To get the termination time, a handle to the process must be held open.</span></span> <span data-ttu-id="f47a9-413">Caso contrário, essa propriedade retornará **NULL**.</span><span class="sxs-lookup"><span data-stu-id="f47a9-413">Otherwise, this property returns **NULL**.</span></span>

<span data-ttu-id="f47a9-414">Essa propriedade é herdada [**do \_ processo CIM**](cim-process.md).</span><span class="sxs-lookup"><span data-stu-id="f47a9-414">This property is inherited from [**CIM\_Process**](cim-process.md).</span></span>

</dd> <dt>

<span data-ttu-id="f47a9-415">**ThreadCount**</span><span class="sxs-lookup"><span data-stu-id="f47a9-415">**ThreadCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f47a9-416">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f47a9-416">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f47a9-417">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f47a9-417">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f47a9-418">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api processo de status do processo do \| \| sistema \_ \_ \| NumberOfThreads"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("contagem de threads")</span><span class="sxs-lookup"><span data-stu-id="f47a9-418">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process Status\|SYSTEM\_PROCESS\_INFORMATION\|NumberOfThreads"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Thread Count")</span></span>
</dt> </dl>

<span data-ttu-id="f47a9-419">Número de threads ativos em um processo.</span><span class="sxs-lookup"><span data-stu-id="f47a9-419">Number of active threads in a process.</span></span> <span data-ttu-id="f47a9-420">Uma instrução é a unidade básica de execução em um processador e um thread é o objeto que executa uma instrução.</span><span class="sxs-lookup"><span data-stu-id="f47a9-420">An instruction is the basic unit of execution in a processor, and a thread is the object that executes an instruction.</span></span> <span data-ttu-id="f47a9-421">Cada processo em execução tem pelo menos um thread.</span><span class="sxs-lookup"><span data-stu-id="f47a9-421">Each running process has at least one thread.</span></span>

</dd> <dt>

<span data-ttu-id="f47a9-422">**Usermodetime**</span><span class="sxs-lookup"><span data-stu-id="f47a9-422">**UserModeTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f47a9-423">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f47a9-423">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f47a9-424">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f47a9-424">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f47a9-425">Qualificadores: [**substituir**](../wmisdk/standard-qualifiers.md) ("usermodetime"), [**Units**](../wmisdk/standard-qualifiers.md) ("100 nanossegundos")</span><span class="sxs-lookup"><span data-stu-id="f47a9-425">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("UserModeTime"), [**Units**](../wmisdk/standard-qualifiers.md) ("100 nanoseconds")</span></span>
</dt> </dl>

<span data-ttu-id="f47a9-426">Tempo no modo de usuário, em unidades de 100 nanossegundos.</span><span class="sxs-lookup"><span data-stu-id="f47a9-426">Time in user mode, in 100 nanosecond units.</span></span> <span data-ttu-id="f47a9-427">Se essas informações não estiverem disponíveis, use um valor de 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="f47a9-427">If this information is not available, use a value of 0 (zero).</span></span>

<span data-ttu-id="f47a9-428">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="f47a9-428">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="f47a9-429">**VirtualSize**</span><span class="sxs-lookup"><span data-stu-id="f47a9-429">**VirtualSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f47a9-430">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f47a9-430">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f47a9-431">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f47a9-431">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f47a9-432">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api processo de status do processo do \| \| sistema \_ \_ \| VirtualSize"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("uso do espaço de endereço virtual"), [**unidades**](../wmisdk/standard-qualifiers.md) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="f47a9-432">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process Status\|SYSTEM\_PROCESS\_INFORMATION\|VirtualSize"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Virtual Address Space Usage"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="f47a9-433">Tamanho atual do espaço de endereço virtual que um processo está usando, não a memória física ou virtual realmente usada pelo processo.</span><span class="sxs-lookup"><span data-stu-id="f47a9-433">Current size of the virtual address space that a process is using, not the physical or virtual memory actually used by the process.</span></span> <span data-ttu-id="f47a9-434">O uso do espaço de endereço virtual não implica necessariamente o uso correspondente do disco ou das páginas de memória principal.</span><span class="sxs-lookup"><span data-stu-id="f47a9-434">Using virtual address space does not necessarily imply corresponding use of either disk or main memory pages.</span></span> <span data-ttu-id="f47a9-435">O espaço virtual é finito e, usando muito, o processo pode não ser capaz de carregar bibliotecas.</span><span class="sxs-lookup"><span data-stu-id="f47a9-435">Virtual space is finite, and by using too much, the process might not be able to load libraries.</span></span> <span data-ttu-id="f47a9-436">Esse valor é consistente com o que você vê no Perfmon.exe.</span><span class="sxs-lookup"><span data-stu-id="f47a9-436">This value is consistent with what you see in Perfmon.exe.</span></span>

<span data-ttu-id="f47a9-437">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="f47a9-437">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="f47a9-438">**WindowsVersion**</span><span class="sxs-lookup"><span data-stu-id="f47a9-438">**WindowsVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f47a9-439">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f47a9-439">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f47a9-440">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f47a9-440">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f47a9-441">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| process and thread Functions \| GetProcessVersion"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("versão do Windows")</span><span class="sxs-lookup"><span data-stu-id="f47a9-441">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Functions\|GetProcessVersion"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Windows Version")</span></span>
</dt> </dl>

<span data-ttu-id="f47a9-442">Versão do Windows em que o processo está sendo executado.</span><span class="sxs-lookup"><span data-stu-id="f47a9-442">Version of Windows in which the process is running.</span></span>

<span data-ttu-id="f47a9-443">Exemplo: 4,0</span><span class="sxs-lookup"><span data-stu-id="f47a9-443">Example: 4.0</span></span>

</dd> <dt>

<span data-ttu-id="f47a9-444">**WorkingSetSize**</span><span class="sxs-lookup"><span data-stu-id="f47a9-444">**WorkingSetSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f47a9-445">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f47a9-445">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f47a9-446">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f47a9-446">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f47a9-447">Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("tamanho do conjunto de trabalho"), [**unidades**](../wmisdk/standard-qualifiers.md) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="f47a9-447">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Working Set Size"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="f47a9-448">Quantidade de memória, em bytes, que um processo precisa para ser executado com eficiência — para um sistema operacional que usa o gerenciamento de memória baseado em página.</span><span class="sxs-lookup"><span data-stu-id="f47a9-448">Amount of memory in bytes that a process needs to execute efficiently—for an operating system that uses page-based memory management.</span></span> <span data-ttu-id="f47a9-449">Se o sistema não tiver memória suficiente (menos que o tamanho do conjunto de trabalho), ultrapaginação ocorrerá.</span><span class="sxs-lookup"><span data-stu-id="f47a9-449">If the system does not have enough memory (less than the working set size), thrashing occurs.</span></span> <span data-ttu-id="f47a9-450">Se o tamanho do conjunto de trabalho não for conhecido, use **NULL** ou 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="f47a9-450">If the size of the working set is not known, use **NULL** or 0 (zero).</span></span> <span data-ttu-id="f47a9-451">Se os dados do conjunto de trabalho forem fornecidos, você poderá monitorar as informações para entender os requisitos de memória em constante mudança de um processo.</span><span class="sxs-lookup"><span data-stu-id="f47a9-451">If working set data is provided, you can monitor the information to understand the changing memory requirements of a process.</span></span>

<span data-ttu-id="f47a9-452">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="f47a9-452">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

<span data-ttu-id="f47a9-453">Essa propriedade é herdada [**do \_ processo CIM**](cim-process.md).</span><span class="sxs-lookup"><span data-stu-id="f47a9-453">This property is inherited from [**CIM\_Process**](cim-process.md).</span></span>

</dd> <dt>

<span data-ttu-id="f47a9-454">**WriteOperationCount**</span><span class="sxs-lookup"><span data-stu-id="f47a9-454">**WriteOperationCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f47a9-455">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f47a9-455">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f47a9-456">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f47a9-456">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f47a9-457">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| processo e estruturas de thread \| informações do processo do sistema \_ \_ \| WriteOperationCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("contagem da operação de gravação")</span><span class="sxs-lookup"><span data-stu-id="f47a9-457">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|SYSTEM\_PROCESS\_INFORMATION\|WriteOperationCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Write Operation Count")</span></span>
</dt> </dl>

<span data-ttu-id="f47a9-458">Número de operações de gravação executadas.</span><span class="sxs-lookup"><span data-stu-id="f47a9-458">Number of write operations performed.</span></span>

<span data-ttu-id="f47a9-459">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="f47a9-459">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="f47a9-460">**WriteTransferCount**</span><span class="sxs-lookup"><span data-stu-id="f47a9-460">**WriteTransferCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f47a9-461">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f47a9-461">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f47a9-462">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f47a9-462">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f47a9-463">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| processo e estruturas de thread \| informações do processo do sistema \_ \_ \| WriteTransferCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("contagem de transferência de gravação"), [**unidades**](../wmisdk/standard-qualifiers.md) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="f47a9-463">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|SYSTEM\_PROCESS\_INFORMATION\|WriteTransferCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Write Transfer Count"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="f47a9-464">Quantidade de dados gravados.</span><span class="sxs-lookup"><span data-stu-id="f47a9-464">Amount of data written.</span></span>

<span data-ttu-id="f47a9-465">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="f47a9-465">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f47a9-466">Comentários</span><span class="sxs-lookup"><span data-stu-id="f47a9-466">Remarks</span></span>

<span data-ttu-id="f47a9-467">A classe de **\_ processo do Win32** é derivada do [**\_ processo CIM**](cim-process.md).</span><span class="sxs-lookup"><span data-stu-id="f47a9-467">The **Win32\_Process** class is derived from [**CIM\_Process**](cim-process.md).</span></span> <span data-ttu-id="f47a9-468">O processo de chamada que usa essa classe deve ter o privilégio **se \_ Restore \_ Name** no computador em que o registro reside.</span><span class="sxs-lookup"><span data-stu-id="f47a9-468">The calling process that uses this class must have the **SE\_RESTORE\_NAME** privilege on the computer in which the registry resides.</span></span> <span data-ttu-id="f47a9-469">Para obter mais informações, consulte [executando operações privilegiadas](../wmisdk/executing-privileged-operations.md).</span><span class="sxs-lookup"><span data-stu-id="f47a9-469">For more information, see [Executing Privileged Operations](../wmisdk/executing-privileged-operations.md).</span></span>

### <a name="overview"></a><span data-ttu-id="f47a9-470">Visão geral</span><span class="sxs-lookup"><span data-stu-id="f47a9-470">Overview</span></span>

<span data-ttu-id="f47a9-471">Processa quase tudo o que acontece em um computador.</span><span class="sxs-lookup"><span data-stu-id="f47a9-471">Processes underlie almost everything that happens on a computer.</span></span> <span data-ttu-id="f47a9-472">Na verdade, a causa raiz da maioria dos problemas do computador pode ser rastreada para processos; por exemplo, muitos processos podem estar em execução em um computador (e contendendo um conjunto finito de recursos), ou um único processo pode estar usando mais do que sua parcela de recursos.</span><span class="sxs-lookup"><span data-stu-id="f47a9-472">In fact, the root cause of most computer problems can be traced to processes; for example, too many processes might be running on a computer (and contending for a finite set of resources), or a single process might be using more than its share of resources.</span></span> <span data-ttu-id="f47a9-473">Esses fatores tornam importante manter uma inspeção próxima dos processos em execução em um computador.</span><span class="sxs-lookup"><span data-stu-id="f47a9-473">These factors make it important to keep a close watch on the processes running on a computer.</span></span> <span data-ttu-id="f47a9-474">O monitoramento de processos, a principal atividade no gerenciamento de processos, permite que você determine o que um computador realmente faz, quais aplicativos o computador executa e como esses aplicativos são afetados por alterações no ambiente computacional.</span><span class="sxs-lookup"><span data-stu-id="f47a9-474">Process monitoring, the main activity in process management, allows you to determine what a computer actually does, what applications the computer runs, and how those applications are affected by changes in the computing environment.</span></span>

### <a name="monitoring-a-process"></a><span data-ttu-id="f47a9-475">Monitorando um processo</span><span class="sxs-lookup"><span data-stu-id="f47a9-475">Monitoring a Process</span></span>

<span data-ttu-id="f47a9-476">O monitoramento de processos regularmente ajuda a garantir que um computador seja executado no máximo de eficiência e que ele execute suas tarefas deferidas conforme o esperado.</span><span class="sxs-lookup"><span data-stu-id="f47a9-476">Monitoring processes on a regular basis helps you ensure that a computer runs at peak efficiency and that it carries out its appointed tasks as expected.</span></span> <span data-ttu-id="f47a9-477">Por exemplo, monitorando processos você pode ser notificado imediatamente de qualquer aplicativo que tenha parado de responder e, em seguida, executar etapas para encerrar esse processo.</span><span class="sxs-lookup"><span data-stu-id="f47a9-477">For example, by monitoring processes you can be notified immediately of any application that has stopped responding, and then take steps to end that process.</span></span> <span data-ttu-id="f47a9-478">Além disso, o monitoramento de processos permite que você identifique problemas antes que eles ocorram.</span><span class="sxs-lookup"><span data-stu-id="f47a9-478">In addition, process monitoring enables you to identify problems before they occur.</span></span> <span data-ttu-id="f47a9-479">Por exemplo, verificando repetidamente a quantidade de memória usada por um processo, você pode identificar um vazamento de memória.</span><span class="sxs-lookup"><span data-stu-id="f47a9-479">For example, by repeatedly checking the amount of memory used by a process, you can identify a memory leak.</span></span> <span data-ttu-id="f47a9-480">Em seguida, você pode parar o processo antes que o aplicativo errônea use toda a memória disponível e coloque o computador em uma parada.</span><span class="sxs-lookup"><span data-stu-id="f47a9-480">You can then stop the process before the errant application uses all of the available memory and brings the computer to a halt.</span></span>

<span data-ttu-id="f47a9-481">O monitoramento de processos também ajuda a minimizar as interrupções causadas por interrupções planejadas para atualizações e manutenção.</span><span class="sxs-lookup"><span data-stu-id="f47a9-481">Process monitoring also helps minimize the disruptions caused by planned outages for upgrades and maintenance.</span></span> <span data-ttu-id="f47a9-482">Por exemplo, ao verificar o status de um aplicativo de banco de dados em execução em computadores cliente, você pode determinar o impacto de colocar o banco de dados offline para atualizar o software.</span><span class="sxs-lookup"><span data-stu-id="f47a9-482">For example, by checking the status of a database application running on client computers, you can determine the impact of taking the database offline in order to upgrade the software.</span></span>

<span data-ttu-id="f47a9-483">Monitorando a disponibilidade do processo.</span><span class="sxs-lookup"><span data-stu-id="f47a9-483">Monitoring process availability.</span></span> <span data-ttu-id="f47a9-484">Mede a porcentagem de tempo em que um processo está disponível.</span><span class="sxs-lookup"><span data-stu-id="f47a9-484">Measures the percentage of time that a process is available.</span></span> <span data-ttu-id="f47a9-485">A disponibilidade normalmente é monitorada pelo uso de uma investigação simples, que relata se o processo ainda está em execução.</span><span class="sxs-lookup"><span data-stu-id="f47a9-485">Availability is typically monitored by use of a simple probe, which reports whether the process is still running.</span></span> <span data-ttu-id="f47a9-486">Ao manter o controle dos resultados de cada investigação, você pode calcular a disponibilidade do processo.</span><span class="sxs-lookup"><span data-stu-id="f47a9-486">By keeping track of the results of each probe, you can calculate the availability of the process.</span></span> <span data-ttu-id="f47a9-487">Por exemplo, um processo que é investigado 100 vezes e responde em 95 dessas ocasiões tem uma disponibilidade de 95%.</span><span class="sxs-lookup"><span data-stu-id="f47a9-487">For example, a process that is probed 100 times and responds on 95 of those occasions has an availability of 95 percent.</span></span> <span data-ttu-id="f47a9-488">Esse tipo de monitoramento normalmente é reservado para bancos de dados, programas de email e outros aplicativos que devem ser executados em todos os momentos.</span><span class="sxs-lookup"><span data-stu-id="f47a9-488">This type of monitoring is typically reserved for databases, mail programs, and other applications that are expected to run at all times.</span></span> <span data-ttu-id="f47a9-489">Não é apropriado para programas de processamento de texto, planilhas ou outros aplicativos que são rotineiramente iniciados e interrompidos várias vezes por dia.</span><span class="sxs-lookup"><span data-stu-id="f47a9-489">It is not appropriate for word processing programs, spreadsheets, or other applications that are routinely started and stopped several times a day.</span></span>

<span data-ttu-id="f47a9-490">Você pode criar uma instância da classe [**Win32 \_ ProcessStartup**](win32-processstartup.md) para configurar o processo.</span><span class="sxs-lookup"><span data-stu-id="f47a9-490">You can create an instance of the [**Win32\_ProcessStartup**](win32-processstartup.md) class to configure the process.</span></span>

<span data-ttu-id="f47a9-491">Você pode monitorar o desempenho do processo com a classe de [**\_ \_ \_ processo Win32 PerfFormattedData PerfProc**](../wmisdk/retrieving-raw-and-formatted-performance-data.md) e um objeto atualizador WMI, como [**SWbemRefresher**](../wmisdk/swbemrefresher.md).</span><span class="sxs-lookup"><span data-stu-id="f47a9-491">You can monitor process performance with the [**Win32\_PerfFormattedData\_PerfProc\_Process**](../wmisdk/retrieving-raw-and-formatted-performance-data.md) class and a WMI refresher object, such as [**SWbemRefresher**](../wmisdk/swbemrefresher.md).</span></span> <span data-ttu-id="f47a9-492">Para obter mais informações, consulte [monitorando dados de desempenho](../wmisdk/monitoring-performance-data.md).</span><span class="sxs-lookup"><span data-stu-id="f47a9-492">For more information, see [Monitoring Performance Data](../wmisdk/monitoring-performance-data.md).</span></span>

## <a name="examples"></a><span data-ttu-id="f47a9-493">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f47a9-493">Examples</span></span>

<span data-ttu-id="f47a9-494">A [lista as propriedades do exemplo de código do PowerShell de classes WMI](https://Gallery.TechNet.Microsoft.Com/a7918bf3-bc03-4553-990f-aba13cf196b7) na galeria do TechNet descreve a classe de **\_ processo do Win32** e gera os resultados no formato do Excel.</span><span class="sxs-lookup"><span data-stu-id="f47a9-494">The [List the Properties of WMI Classes](https://Gallery.TechNet.Microsoft.Com/a7918bf3-bc03-4553-990f-aba13cf196b7) PowerShell code sample on TechNet Gallery describes the **Win32\_Process** class, and outputs the results in Excel format.</span></span>

<span data-ttu-id="f47a9-495">O [processo de encerramento em execução em vários servidores](https://Gallery.TechNet.Microsoft.Com/698c2512-2bbd-40ee-b3bf-a9cebdad2faf) encerra um processo em execução em um único ou vários computadores.</span><span class="sxs-lookup"><span data-stu-id="f47a9-495">The [Terminate running process on multiple servers](https://Gallery.TechNet.Microsoft.Com/698c2512-2bbd-40ee-b3bf-a9cebdad2faf) terminates a process running on a single or multiple computers.</span></span>

<span data-ttu-id="f47a9-496">No [exemplo: chamando um](../wmisdk/example--calling-a-provider-method.md) tópico de método de provedor, o código usa C++ para chamar o **\_ processo Win32** para criar um processo.</span><span class="sxs-lookup"><span data-stu-id="f47a9-496">In the [Example: Calling a Provider Method](../wmisdk/example--calling-a-provider-method.md) topic, the code uses C++ to call **Win32\_Process** to create a process.</span></span>

<span data-ttu-id="f47a9-497">A disponibilidade é a forma mais simples de monitoramento de processos: com essa abordagem, você simplesmente garante que o processo esteja em execução.</span><span class="sxs-lookup"><span data-stu-id="f47a9-497">Availability is the simplest form of process monitoring: with this approach, you simply ensure that the process is running.</span></span> <span data-ttu-id="f47a9-498">Quando você monitora a disponibilidade do processo, normalmente recupera uma lista de processos em execução em um computador e, em seguida, verifica se um processo específico ainda está ativo.</span><span class="sxs-lookup"><span data-stu-id="f47a9-498">When you monitor for process availability, you typically retrieve a list of processes running on a computer and then verify that a particular process is still active.</span></span> <span data-ttu-id="f47a9-499">Se o processo estiver ativo, ele será considerado disponível.</span><span class="sxs-lookup"><span data-stu-id="f47a9-499">If the process is active, it is considered available.</span></span> <span data-ttu-id="f47a9-500">Se o processo não estiver ativo, ele não estará disponível.</span><span class="sxs-lookup"><span data-stu-id="f47a9-500">If the process is not active, it is not available.</span></span> <span data-ttu-id="f47a9-501">O exemplo de VBScript a seguir monitora a disponibilidade do processo verificando a lista de processos em execução em um computador e emitindo uma notificação se o processo de Database.exe não for encontrado.</span><span class="sxs-lookup"><span data-stu-id="f47a9-501">The following VBScript sample monitors process availability by checking the list of processes running on a computer and issuing a notification if the Database.exe process is not found.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colProcesses = objWMIService.ExecQuery("SELECT * FROM Win32_Process WHERE Name = 'Database.exe'")
If colProcesses.Count = 0 Then
 Wscript.Echo "Database.exe is not running."
Else
 Wscript.Echo "Database.exe is running."
End If
```



<span data-ttu-id="f47a9-502">O exemplo de VBScript a seguir monitora a criação de processos usando um consumidor de evento temporário.</span><span class="sxs-lookup"><span data-stu-id="f47a9-502">The following VBScript sample monitors process creation using a temporary event consumer.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colMonitoredProcesses = objWMIService.ExecNotificationQuery("SELECT * FROM __InstanceCreationEvent " _
                                                     & "WITHIN 10 WHERE TargetInstance ISA 'Win32_Process'")
i = 0
Do While i = 0
 Set objLatestProcess = colMonitoredProcesses.NextEvent
 Wscript.Echo objLatestProcess.TargetInstance.Name, Now
Loop
```



<span data-ttu-id="f47a9-503">O VBScript a seguir monitora as informações de desempenho do processo.</span><span class="sxs-lookup"><span data-stu-id="f47a9-503">The following VBScript monitors process performance information.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colProcessList = objWMIService.ExecQuery("SELECT * FROM Win32_Process")
For Each objProcess in colProcessList
 Wscript.Echo "Process: " & objProcess.Name
 Wscript.Echo "Process ID: " & objProcess.ProcessID
 Wscript.Echo "Thread Count: " & objProcess.ThreadCount
 Wscript.Echo "Page File Size: " & objProcess.PageFileUsage
 Wscript.Echo "Page Faults: " & objProcess.PageFaults
 Wscript.Echo "Working Set Size: " & objProcess.WorkingSetSize
Next
```



<span data-ttu-id="f47a9-504">O exemplo de código VBScript a seguir mostra como obter o proprietário de cada processo em um computador local.</span><span class="sxs-lookup"><span data-stu-id="f47a9-504">The following VBScript code example shows how to obtain the owner of each process on a local computer.</span></span> <span data-ttu-id="f47a9-505">Você pode usar esse script para obter dados de um computador remoto, por exemplo, para determinar quais usuários têm processos executando o Terminal Server, substituir o nome do computador remoto por "." na primeira linha.</span><span class="sxs-lookup"><span data-stu-id="f47a9-505">You can use this script to obtain data from a remote computer, for example, to determine which users have processes running terminal server, substitute the name of the remote computer for "." in the first line.</span></span> <span data-ttu-id="f47a9-506">Você também deve ser um administrador no computador remoto.</span><span class="sxs-lookup"><span data-stu-id="f47a9-506">You must also be an administrator on the remote machine.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")

Set colProcesses = objWMIService.ExecQuery("select * from win32_process" )
For Each objProcess in colProcesses

  If objProcess.GetOwner ( User, Domain ) = 0 Then
    Wscript.Echo "Process " & objProcess.Caption & " belongs to " & Domain & "\" & User
  Else
    Wscript.Echo "Problem " & Rtn & " getting the owner for process " & objProcess.Caption
  End If
Next
```



<span data-ttu-id="f47a9-507">O exemplo de código VBScript a seguir mostra como obter a sessão de logon associada a um processo em execução.</span><span class="sxs-lookup"><span data-stu-id="f47a9-507">The following VBScript code example shows how to obtain the logon session associated with a running process.</span></span> <span data-ttu-id="f47a9-508">Um processo deve estar em execução Notepad.exe antes de o script ser iniciado.</span><span class="sxs-lookup"><span data-stu-id="f47a9-508">A process must be running Notepad.exe before the script starts.</span></span> <span data-ttu-id="f47a9-509">O exemplo localiza as instâncias de [**\_ LogonSession do Win32**](win32-logonsession.md) associadas ao **\_ processo Win32** que representa Notepad.exe.</span><span class="sxs-lookup"><span data-stu-id="f47a9-509">The example locates the instances of [**Win32\_LogonSession**](win32-logonsession.md) associated with the **Win32\_Process** that represents Notepad.exe.</span></span> <span data-ttu-id="f47a9-510">[**Win32 \_ SessionProcess**](win32-sessionprocess.md) é especificado como a classe de associação.</span><span class="sxs-lookup"><span data-stu-id="f47a9-510">[**Win32\_SessionProcess**](win32-sessionprocess.md) is specified as the association class.</span></span> <span data-ttu-id="f47a9-511">Para obter mais informações, consulte [ASSOCIATORS of Statement.](../wmisdk/associators-of-statement.md)</span><span class="sxs-lookup"><span data-stu-id="f47a9-511">For more information, see [ASSOCIATORS OF Statement.](../wmisdk/associators-of-statement.md).</span></span>


```VB
On error resume next
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\.\root\cimv2")
Set colProcesses = objWMIService.ExecQuery("Select * from Win32_Process Where Name = 'Notepad.exe'")
For Each objProcess in colProcesses
  ProcessId = objProcess.ProcessId
  Set colLogonSessions = objWMIService.ExecQuery("Associators of {Win32_Process='" & ProcessId & "'} " _
                                               & "Where Resultclass = Win32_LogonSession Assocclass = Win32_SessionProcess", "WQL", 48)
  If Err <> 0 Then
    WScript.Echo "Error on associators query= " & Err.number & " " & Err.Description
    WScript.Quit
  End If
  For Each LogonSession in colLogonSessions
    Wscript.Echo " Logon id is " & LogonSession.LogonId
  Next
Next
```



## <a name="requirements"></a><span data-ttu-id="f47a9-512">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f47a9-512">Requirements</span></span>



| <span data-ttu-id="f47a9-513">Requisito</span><span class="sxs-lookup"><span data-stu-id="f47a9-513">Requirement</span></span> | <span data-ttu-id="f47a9-514">Valor</span><span class="sxs-lookup"><span data-stu-id="f47a9-514">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f47a9-515">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f47a9-515">Minimum supported client</span></span><br/> | <span data-ttu-id="f47a9-516">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f47a9-516">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f47a9-517">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f47a9-517">Minimum supported server</span></span><br/> | <span data-ttu-id="f47a9-518">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f47a9-518">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f47a9-519">Namespace</span><span class="sxs-lookup"><span data-stu-id="f47a9-519">Namespace</span></span><br/>                | <span data-ttu-id="f47a9-520">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="f47a9-520">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f47a9-521">MOF</span><span class="sxs-lookup"><span data-stu-id="f47a9-521">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f47a9-522"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f47a9-522"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f47a9-523">DLL</span><span class="sxs-lookup"><span data-stu-id="f47a9-523">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f47a9-524"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f47a9-524"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f47a9-525">Confira também</span><span class="sxs-lookup"><span data-stu-id="f47a9-525">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f47a9-526">**\_Processo CIM**</span><span class="sxs-lookup"><span data-stu-id="f47a9-526">**CIM\_Process**</span></span>](cim-process.md)
</dt> <dt>

[<span data-ttu-id="f47a9-527">Classes do sistema operacional</span><span class="sxs-lookup"><span data-stu-id="f47a9-527">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> <dt>

[<span data-ttu-id="f47a9-528">Tarefas do WMI: processos</span><span class="sxs-lookup"><span data-stu-id="f47a9-528">WMI Tasks: Processes</span></span>](../wmisdk/wmi-tasks--processes.md)
</dt> </dl>

 

 
