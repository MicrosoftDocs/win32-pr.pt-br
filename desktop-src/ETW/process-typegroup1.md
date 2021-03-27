---
description: Essa classe é a classe de tipo de evento para eventos de processo. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: 4f06e1af-3f9a-4346-aa50-50f3ee82cd98
title: Classe Process_TypeGroup1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Process_TypeGroup1
- Process_TypeGroup1.UniqueProcessKey
- Process_TypeGroup1.ProcessId
- Process_TypeGroup1.ParentId
- Process_TypeGroup1.SessionId
- Process_TypeGroup1.ExitStatus
- Process_TypeGroup1.DirectoryTableBase
- Process_TypeGroup1.UserSID
- Process_TypeGroup1.ImageFileName
- Process_TypeGroup1.CommandLine
api_type:
- NA
api_location: ''
ms.openlocfilehash: 4ad2ebcd9a3e1563f6e2f4c82d90dd4d2c80112f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827358"
---
# <a name="process_typegroup1-class"></a><span data-ttu-id="82d42-104">\_Classe Process TypeGroup1</span><span class="sxs-lookup"><span data-stu-id="82d42-104">Process\_TypeGroup1 class</span></span>

<span data-ttu-id="82d42-105">Essa classe é a classe de tipo de evento para eventos de processo.</span><span class="sxs-lookup"><span data-stu-id="82d42-105">This class is the event type class for process events.</span></span>

<span data-ttu-id="82d42-106">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="82d42-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="82d42-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="82d42-107">Syntax</span></span>

``` syntax
[EventType{1, 2, 3, 4, 39}, EventTypeName{"Start", "End", "DCStart", "DCEnd", "Defunct"}]
class Process_TypeGroup1 : Process
{
  uint32 UniqueProcessKey;
  uint32 ProcessId;
  uint32 ParentId;
  uint32 SessionId;
  sint32 ExitStatus;
  uint32 DirectoryTableBase;
  object UserSID;
  string ImageFileName;
  string CommandLine;
};
```

## <a name="members"></a><span data-ttu-id="82d42-108">Membros</span><span class="sxs-lookup"><span data-stu-id="82d42-108">Members</span></span>

<span data-ttu-id="82d42-109">A classe **process \_ TypeGroup1** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="82d42-109">The **Process\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="82d42-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="82d42-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="82d42-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="82d42-111">Properties</span></span>

<span data-ttu-id="82d42-112">A classe **process \_ TypeGroup1** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="82d42-112">The **Process\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="82d42-113">CommandLine</span><span class="sxs-lookup"><span data-stu-id="82d42-113">CommandLine</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82d42-114">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="82d42-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82d42-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="82d42-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="82d42-116">Qualificadores: WmiDataId (9), StringTermination ("NullTerminated"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="82d42-116">Qualifiers: WmiDataId(9), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="82d42-117">Linha de comando completa do processo.</span><span class="sxs-lookup"><span data-stu-id="82d42-117">Full command line of the process.</span></span>

</dd> <dt>

<span data-ttu-id="82d42-118">DirectoryTableBase</span><span class="sxs-lookup"><span data-stu-id="82d42-118">DirectoryTableBase</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82d42-119">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="82d42-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="82d42-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="82d42-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="82d42-121">Qualificadores: WmiDataId (6), ponteiro</span><span class="sxs-lookup"><span data-stu-id="82d42-121">Qualifiers: WmiDataId(6), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="82d42-122">O endereço físico da tabela de página do processo.</span><span class="sxs-lookup"><span data-stu-id="82d42-122">The physical address of the page table of the process.</span></span>

</dd> <dt>

<span data-ttu-id="82d42-123">ExitStatus</span><span class="sxs-lookup"><span data-stu-id="82d42-123">ExitStatus</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82d42-124">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="82d42-124">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="82d42-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="82d42-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="82d42-126">Qualificadores: WmiDataId (5)</span><span class="sxs-lookup"><span data-stu-id="82d42-126">Qualifiers: WmiDataId(5)</span></span>
</dt> </dl>

<span data-ttu-id="82d42-127">Status de saída do processo interrompido.</span><span class="sxs-lookup"><span data-stu-id="82d42-127">Exit status of the stopped process.</span></span>

</dd> <dt>

<span data-ttu-id="82d42-128">ImageFileName</span><span class="sxs-lookup"><span data-stu-id="82d42-128">ImageFileName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82d42-129">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="82d42-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82d42-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="82d42-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="82d42-131">Qualificadores: WmiDataId (8), StringTermination ("NullTerminated")</span><span class="sxs-lookup"><span data-stu-id="82d42-131">Qualifiers: WmiDataId(8), StringTermination("NullTerminated")</span></span>
</dt> </dl>

<span data-ttu-id="82d42-132">Caminho para o arquivo executável do processo.</span><span class="sxs-lookup"><span data-stu-id="82d42-132">Path to the executable file of the process.</span></span>

</dd> <dt>

<span data-ttu-id="82d42-133">ParentId</span><span class="sxs-lookup"><span data-stu-id="82d42-133">ParentId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82d42-134">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="82d42-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="82d42-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="82d42-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="82d42-136">Qualificadores: WmiDataId (3), formato ("x")</span><span class="sxs-lookup"><span data-stu-id="82d42-136">Qualifiers: WmiDataId(3), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="82d42-137">Identificador exclusivo do processo que cria esse processo.</span><span class="sxs-lookup"><span data-stu-id="82d42-137">Unique identifier of the process that creates this process.</span></span> <span data-ttu-id="82d42-138">Os números de identificador de processo são reutilizados, portanto, eles identificam apenas um processo durante o tempo de vida desse processo.</span><span class="sxs-lookup"><span data-stu-id="82d42-138">Process identifier numbers are reused, so they only identify a process for the lifetime of that process.</span></span> <span data-ttu-id="82d42-139">É possível que o processo identificado pelo ParentProcessId seja encerrado; portanto, ParentProcessId pode não se referir a um processo em execução.</span><span class="sxs-lookup"><span data-stu-id="82d42-139">It is possible that the process identified by ParentProcessId is terminated, so ParentProcessId may not refer to a running process.</span></span> <span data-ttu-id="82d42-140">Também é possível que o ParentProcessId incorretamente faça referência a um processo que reutiliza um identificador de processo.</span><span class="sxs-lookup"><span data-stu-id="82d42-140">It is also possible that ParentProcessId incorrectly refers to a process that reuses a process identifier.</span></span>

</dd> <dt>

<span data-ttu-id="82d42-141">ProcessId</span><span class="sxs-lookup"><span data-stu-id="82d42-141">ProcessId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82d42-142">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="82d42-142">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="82d42-143">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="82d42-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="82d42-144">Qualificadores: WmiDataId (2), formato ("x")</span><span class="sxs-lookup"><span data-stu-id="82d42-144">Qualifiers: WmiDataId(2), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="82d42-145">Identificador de processo global que você pode usar para identificar um processo.</span><span class="sxs-lookup"><span data-stu-id="82d42-145">Global process identifier that you can use to identify a process.</span></span> <span data-ttu-id="82d42-146">O valor é válido a partir do momento em que um processo é criado até ser encerrado.</span><span class="sxs-lookup"><span data-stu-id="82d42-146">The value is valid from the time a process is created until it is terminated.</span></span>

</dd> <dt>

<span data-ttu-id="82d42-147">SessionId</span><span class="sxs-lookup"><span data-stu-id="82d42-147">SessionId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82d42-148">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="82d42-148">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="82d42-149">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="82d42-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="82d42-150">Qualificadores: WmiDataId (4)</span><span class="sxs-lookup"><span data-stu-id="82d42-150">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="82d42-151">Identificador exclusivo que um sistema operacional gera ao criar uma nova sessão.</span><span class="sxs-lookup"><span data-stu-id="82d42-151">Unique identifier that an operating system generates when it creates a new session.</span></span> <span data-ttu-id="82d42-152">Uma sessão abrange um período de tempo do logon até o logoff de um sistema específico.</span><span class="sxs-lookup"><span data-stu-id="82d42-152">A session spans a period of time from log on until log off from a specific system.</span></span>

</dd> <dt>

<span data-ttu-id="82d42-153">UniqueProcessKey</span><span class="sxs-lookup"><span data-stu-id="82d42-153">UniqueProcessKey</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82d42-154">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="82d42-154">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="82d42-155">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="82d42-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="82d42-156">Qualificadores: WmiDataId (1), ponteiro</span><span class="sxs-lookup"><span data-stu-id="82d42-156">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="82d42-157">O endereço do objeto de processo no kernel.</span><span class="sxs-lookup"><span data-stu-id="82d42-157">The address of the process object in the kernel.</span></span>

</dd> <dt>

<span data-ttu-id="82d42-158">UserSID</span><span class="sxs-lookup"><span data-stu-id="82d42-158">UserSID</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82d42-159">Tipo de dados: **objeto**</span><span class="sxs-lookup"><span data-stu-id="82d42-159">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="82d42-160">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="82d42-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="82d42-161">Qualificadores: WmiDataId (7), extensão ("Sid")</span><span class="sxs-lookup"><span data-stu-id="82d42-161">Qualifiers: WmiDataId(7), Extension("Sid")</span></span>
</dt> </dl>

<span data-ttu-id="82d42-162">SID (identificador de segurança) para o contexto do usuário no qual o evento ocorre.</span><span class="sxs-lookup"><span data-stu-id="82d42-162">Security identifier (SID) for the user context under which the event happens.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="82d42-163">Comentários</span><span class="sxs-lookup"><span data-stu-id="82d42-163">Remarks</span></span>

<span data-ttu-id="82d42-164">Os tipos de evento DCStart e DCEnd enumeram o processo que está em execução no momento, incluindo o processo de ociosidade e do sistema, no momento em que a sessão do kernel é iniciada e termina, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="82d42-164">The DCStart and DCEnd event types enumerate the process that are currently running, including idle and system process, at the time the kernel session starts and ends, respectively.</span></span>

## <a name="requirements"></a><span data-ttu-id="82d42-165">Requisitos</span><span class="sxs-lookup"><span data-stu-id="82d42-165">Requirements</span></span>



| <span data-ttu-id="82d42-166">Requisito</span><span class="sxs-lookup"><span data-stu-id="82d42-166">Requirement</span></span> | <span data-ttu-id="82d42-167">Valor</span><span class="sxs-lookup"><span data-stu-id="82d42-167">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="82d42-168">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="82d42-168">Minimum supported client</span></span><br/> | <span data-ttu-id="82d42-169">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="82d42-169">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="82d42-170">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="82d42-170">Minimum supported server</span></span><br/> | <span data-ttu-id="82d42-171">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="82d42-171">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="82d42-172">Confira também</span><span class="sxs-lookup"><span data-stu-id="82d42-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82d42-173">**Processar**</span><span class="sxs-lookup"><span data-stu-id="82d42-173">**Process**</span></span>](process.md)
</dt> </dl>

 

 




