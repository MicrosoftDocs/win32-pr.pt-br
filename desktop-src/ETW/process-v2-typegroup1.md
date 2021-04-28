---
description: Classe Process_V2_TypeGroup1-essa classe é a classe de tipo de evento para eventos de processo. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: ff5c1f64-2087-4238-81f9-6283f0f0e68a
title: Classe Process_V2_TypeGroup1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Process_V2_TypeGroup1
- Process_V2_TypeGroup1.UniqueProcessKey
- Process_V2_TypeGroup1.ProcessId
- Process_V2_TypeGroup1.ParentId
- Process_V2_TypeGroup1.SessionId
- Process_V2_TypeGroup1.ExitStatus
- Process_V2_TypeGroup1.UserSID
- Process_V2_TypeGroup1.ImageFileName
- Process_V2_TypeGroup1.CommandLine
api_type:
- NA
api_location: ''
ms.openlocfilehash: b587a07f33b066cfd7dbeebc44d7277b33c6bee8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106304"
---
# <a name="process_v2_typegroup1-class"></a><span data-ttu-id="c4f1d-104">\_Classe Process v2 \_ TypeGroup1</span><span class="sxs-lookup"><span data-stu-id="c4f1d-104">Process\_V2\_TypeGroup1 class</span></span>

<span data-ttu-id="c4f1d-105">Essa classe é a classe de tipo de evento para eventos de processo.</span><span class="sxs-lookup"><span data-stu-id="c4f1d-105">This class is the event type class for process events.</span></span>

<span data-ttu-id="c4f1d-106">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="c4f1d-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4f1d-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c4f1d-107">Syntax</span></span>

``` syntax
[EventType{1, 2, 3, 4, 39}, EventTypeName{"Start", "End", "DCStart", "DCEnd", "Defunct"}]
class Process_V2_TypeGroup1 : Process_V2
{
  uint32 UniqueProcessKey;
  uint32 ProcessId;
  uint32 ParentId;
  uint32 SessionId;
  sint32 ExitStatus;
  object UserSID;
  string ImageFileName;
  string CommandLine;
};
```

## <a name="members"></a><span data-ttu-id="c4f1d-108">Membros</span><span class="sxs-lookup"><span data-stu-id="c4f1d-108">Members</span></span>

<span data-ttu-id="c4f1d-109">A classe **process \_ v2 \_ TypeGroup1** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="c4f1d-109">The **Process\_V2\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="c4f1d-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c4f1d-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c4f1d-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c4f1d-111">Properties</span></span>

<span data-ttu-id="c4f1d-112">A classe **process \_ v2 \_ TypeGroup1** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="c4f1d-112">The **Process\_V2\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c4f1d-113">CommandLine</span><span class="sxs-lookup"><span data-stu-id="c4f1d-113">CommandLine</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4f1d-114">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c4f1d-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4f1d-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c4f1d-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c4f1d-116">Qualificadores: WmiDataId (8), StringTermination ("NullTerminated"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="c4f1d-116">Qualifiers: WmiDataId(8), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="c4f1d-117">Linha de comando completa do processo.</span><span class="sxs-lookup"><span data-stu-id="c4f1d-117">Full command line of the process.</span></span>

</dd> <dt>

<span data-ttu-id="c4f1d-118">ExitStatus</span><span class="sxs-lookup"><span data-stu-id="c4f1d-118">ExitStatus</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4f1d-119">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c4f1d-119">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c4f1d-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c4f1d-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c4f1d-121">Qualificadores: WmiDataId (5)</span><span class="sxs-lookup"><span data-stu-id="c4f1d-121">Qualifiers: WmiDataId(5)</span></span>
</dt> </dl>

<span data-ttu-id="c4f1d-122">Status de saída do processo interrompido.</span><span class="sxs-lookup"><span data-stu-id="c4f1d-122">Exit status of the stopped process.</span></span>

</dd> <dt>

<span data-ttu-id="c4f1d-123">ImageFileName</span><span class="sxs-lookup"><span data-stu-id="c4f1d-123">ImageFileName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4f1d-124">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c4f1d-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4f1d-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c4f1d-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c4f1d-126">Qualificadores: WmiDataId (7), StringTermination ("NullTerminated")</span><span class="sxs-lookup"><span data-stu-id="c4f1d-126">Qualifiers: WmiDataId(7), StringTermination("NullTerminated")</span></span>
</dt> </dl>

<span data-ttu-id="c4f1d-127">Caminho para o arquivo executável do processo.</span><span class="sxs-lookup"><span data-stu-id="c4f1d-127">Path to the executable file of the process.</span></span>

</dd> <dt>

<span data-ttu-id="c4f1d-128">ParentId</span><span class="sxs-lookup"><span data-stu-id="c4f1d-128">ParentId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4f1d-129">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c4f1d-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c4f1d-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c4f1d-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c4f1d-131">Qualificadores: WmiDataId (3), formato ("x")</span><span class="sxs-lookup"><span data-stu-id="c4f1d-131">Qualifiers: WmiDataId(3), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="c4f1d-132">Identificador exclusivo do processo que cria esse processo.</span><span class="sxs-lookup"><span data-stu-id="c4f1d-132">Unique identifier of the process that creates this process.</span></span> <span data-ttu-id="c4f1d-133">Os números de identificador de processo são reutilizados, portanto, eles identificam apenas um processo durante o tempo de vida desse processo.</span><span class="sxs-lookup"><span data-stu-id="c4f1d-133">Process identifier numbers are reused, so they only identify a process for the lifetime of that process.</span></span> <span data-ttu-id="c4f1d-134">É possível que o processo identificado pelo ParentProcessId seja encerrado; portanto, ParentProcessId pode não se referir a um processo em execução.</span><span class="sxs-lookup"><span data-stu-id="c4f1d-134">It is possible that the process identified by ParentProcessId is terminated, so ParentProcessId may not refer to a running process.</span></span> <span data-ttu-id="c4f1d-135">Também é possível que o ParentProcessId incorretamente faça referência a um processo que reutiliza um identificador de processo.</span><span class="sxs-lookup"><span data-stu-id="c4f1d-135">It is also possible that ParentProcessId incorrectly refers to a process that reuses a process identifier.</span></span>

</dd> <dt>

<span data-ttu-id="c4f1d-136">ProcessId</span><span class="sxs-lookup"><span data-stu-id="c4f1d-136">ProcessId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4f1d-137">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c4f1d-137">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c4f1d-138">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c4f1d-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c4f1d-139">Qualificadores: WmiDataId (2), formato ("x")</span><span class="sxs-lookup"><span data-stu-id="c4f1d-139">Qualifiers: WmiDataId(2), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="c4f1d-140">Identificador de processo global que você pode usar para identificar um processo.</span><span class="sxs-lookup"><span data-stu-id="c4f1d-140">Global process identifier that you can use to identify a process.</span></span> <span data-ttu-id="c4f1d-141">O valor é válido a partir do momento em que um processo é criado até ser encerrado.</span><span class="sxs-lookup"><span data-stu-id="c4f1d-141">The value is valid from the time a process is created until it is terminated.</span></span>

</dd> <dt>

<span data-ttu-id="c4f1d-142">SessionId</span><span class="sxs-lookup"><span data-stu-id="c4f1d-142">SessionId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4f1d-143">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c4f1d-143">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c4f1d-144">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c4f1d-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c4f1d-145">Qualificadores: WmiDataId (4)</span><span class="sxs-lookup"><span data-stu-id="c4f1d-145">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="c4f1d-146">Identificador exclusivo que um sistema operacional gera ao criar uma nova sessão.</span><span class="sxs-lookup"><span data-stu-id="c4f1d-146">Unique identifier that an operating system generates when it creates a new session.</span></span> <span data-ttu-id="c4f1d-147">Uma sessão abrange um período de tempo do logon até o logoff de um sistema específico.</span><span class="sxs-lookup"><span data-stu-id="c4f1d-147">A session spans a period of time from log on until log off from a specific system.</span></span>

</dd> <dt>

<span data-ttu-id="c4f1d-148">UniqueProcessKey</span><span class="sxs-lookup"><span data-stu-id="c4f1d-148">UniqueProcessKey</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4f1d-149">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c4f1d-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c4f1d-150">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c4f1d-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c4f1d-151">Qualificadores: WmiDataId (1), ponteiro</span><span class="sxs-lookup"><span data-stu-id="c4f1d-151">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="c4f1d-152">O endereço do objeto de processo no kernel.</span><span class="sxs-lookup"><span data-stu-id="c4f1d-152">The address of the process object in the kernel.</span></span>

</dd> <dt>

<span data-ttu-id="c4f1d-153">UserSID</span><span class="sxs-lookup"><span data-stu-id="c4f1d-153">UserSID</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4f1d-154">Tipo de dados: **objeto**</span><span class="sxs-lookup"><span data-stu-id="c4f1d-154">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="c4f1d-155">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c4f1d-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c4f1d-156">Qualificadores: WmiDataId (6), extensão ("Sid")</span><span class="sxs-lookup"><span data-stu-id="c4f1d-156">Qualifiers: WmiDataId(6), Extension("Sid")</span></span>
</dt> </dl>

<span data-ttu-id="c4f1d-157">SID (identificador de segurança) para o contexto do usuário no qual o evento ocorre.</span><span class="sxs-lookup"><span data-stu-id="c4f1d-157">Security identifier (SID) for the user context under which the event happens.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c4f1d-158">Comentários</span><span class="sxs-lookup"><span data-stu-id="c4f1d-158">Remarks</span></span>

<span data-ttu-id="c4f1d-159">Os tipos de evento DCStart e DCEnd enumeram o processo que está em execução no momento, incluindo o processo de ociosidade e do sistema, no momento em que a sessão do kernel é iniciada e termina, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="c4f1d-159">The DCStart and DCEnd event types enumerate the process that are currently running, including idle and system process, at the time the kernel session starts and ends, respectively.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4f1d-160">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c4f1d-160">Requirements</span></span>



| <span data-ttu-id="c4f1d-161">Requisito</span><span class="sxs-lookup"><span data-stu-id="c4f1d-161">Requirement</span></span> | <span data-ttu-id="c4f1d-162">Valor</span><span class="sxs-lookup"><span data-stu-id="c4f1d-162">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="c4f1d-163">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c4f1d-163">Minimum supported client</span></span><br/> | <span data-ttu-id="c4f1d-164">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c4f1d-164">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="c4f1d-165">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c4f1d-165">Minimum supported server</span></span><br/> | <span data-ttu-id="c4f1d-166">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c4f1d-166">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="c4f1d-167">Consulte também</span><span class="sxs-lookup"><span data-stu-id="c4f1d-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4f1d-168">**Processo \_ v2**</span><span class="sxs-lookup"><span data-stu-id="c4f1d-168">**Process\_V2**</span></span>](process-v2.md)
</dt> </dl>

 

 




