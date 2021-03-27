---
description: Essa classe é a classe de tipo de evento para eventos de processo. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: b114d7fd-c308-4f21-8f1a-ab27dc93abc5
title: Classe Process_V1_TypeGroup1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Process_V1_TypeGroup1
- Process_V1_TypeGroup1.PageDirectoryBase
- Process_V1_TypeGroup1.ProcessId
- Process_V1_TypeGroup1.ParentId
- Process_V1_TypeGroup1.SessionId
- Process_V1_TypeGroup1.ExitStatus
- Process_V1_TypeGroup1.UserSID
- Process_V1_TypeGroup1.ImageFileName
api_type:
- NA
api_location: ''
ms.openlocfilehash: fc2308965de5c06a25858a138d4536763613a4d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297217"
---
# <a name="process_v1_typegroup1-class"></a><span data-ttu-id="0d51d-104">\_Classe Process v1 \_ TypeGroup1</span><span class="sxs-lookup"><span data-stu-id="0d51d-104">Process\_V1\_TypeGroup1 class</span></span>

<span data-ttu-id="0d51d-105">Essa classe é a classe de tipo de evento para eventos de processo.</span><span class="sxs-lookup"><span data-stu-id="0d51d-105">This class is the event type class for process events.</span></span>

<span data-ttu-id="0d51d-106">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="0d51d-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d51d-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0d51d-107">Syntax</span></span>

``` syntax
[EventType{1, 2, 3, 4}, EventTypeName{"Start", "End", "DCStart", "DCEnd"}]
class Process_V1_TypeGroup1 : Process_V1
{
  uint32 PageDirectoryBase;
  uint32 ProcessId;
  uint32 ParentId;
  uint32 SessionId;
  sint32 ExitStatus;
  object UserSID;
  string ImageFileName;
};
```

## <a name="members"></a><span data-ttu-id="0d51d-108">Membros</span><span class="sxs-lookup"><span data-stu-id="0d51d-108">Members</span></span>

<span data-ttu-id="0d51d-109">A classe **process \_ v1 \_ TypeGroup1** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="0d51d-109">The **Process\_V1\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="0d51d-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0d51d-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0d51d-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0d51d-111">Properties</span></span>

<span data-ttu-id="0d51d-112">A classe **process \_ v1 \_ TypeGroup1** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="0d51d-112">The **Process\_V1\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0d51d-113">ExitStatus</span><span class="sxs-lookup"><span data-stu-id="0d51d-113">ExitStatus</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d51d-114">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="0d51d-114">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0d51d-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0d51d-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d51d-116">Qualificadores: WmiDataId (5)</span><span class="sxs-lookup"><span data-stu-id="0d51d-116">Qualifiers: WmiDataId(5)</span></span>
</dt> </dl>

<span data-ttu-id="0d51d-117">Status de saída do processo interrompido.</span><span class="sxs-lookup"><span data-stu-id="0d51d-117">Exit status of the stopped process.</span></span>

</dd> <dt>

<span data-ttu-id="0d51d-118">ImageFileName</span><span class="sxs-lookup"><span data-stu-id="0d51d-118">ImageFileName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d51d-119">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d51d-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d51d-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0d51d-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d51d-121">Qualificadores: WmiDataId (7), StringTermination ("NullTerminated")</span><span class="sxs-lookup"><span data-stu-id="0d51d-121">Qualifiers: WmiDataId(7), StringTermination("NullTerminated")</span></span>
</dt> </dl>

<span data-ttu-id="0d51d-122">Caminho para o arquivo executável do processo.</span><span class="sxs-lookup"><span data-stu-id="0d51d-122">Path to the executable file of the process.</span></span>

</dd> <dt>

<span data-ttu-id="0d51d-123">PageDirectoryBase</span><span class="sxs-lookup"><span data-stu-id="0d51d-123">PageDirectoryBase</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d51d-124">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0d51d-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0d51d-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0d51d-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d51d-126">Qualificadores: WmiDataId (1), ponteiro</span><span class="sxs-lookup"><span data-stu-id="0d51d-126">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="0d51d-127">Reservado.</span><span class="sxs-lookup"><span data-stu-id="0d51d-127">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="0d51d-128">ParentId</span><span class="sxs-lookup"><span data-stu-id="0d51d-128">ParentId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d51d-129">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0d51d-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0d51d-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0d51d-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d51d-131">Qualificadores: WmiDataId (3)</span><span class="sxs-lookup"><span data-stu-id="0d51d-131">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="0d51d-132">Identificador exclusivo do processo que cria esse processo.</span><span class="sxs-lookup"><span data-stu-id="0d51d-132">Unique identifier of the process that creates this process.</span></span> <span data-ttu-id="0d51d-133">Os números de identificador de processo são reutilizados, portanto, eles identificam apenas um processo durante o tempo de vida desse processo.</span><span class="sxs-lookup"><span data-stu-id="0d51d-133">Process identifier numbers are reused, so they only identify a process for the lifetime of that process.</span></span> <span data-ttu-id="0d51d-134">É possível que o processo identificado pelo ParentProcessId seja encerrado; portanto, ParentProcessId pode não se referir a um processo em execução.</span><span class="sxs-lookup"><span data-stu-id="0d51d-134">It is possible that the process identified by ParentProcessId is terminated, so ParentProcessId may not refer to a running process.</span></span> <span data-ttu-id="0d51d-135">Também é possível que o ParentProcessId incorretamente faça referência a um processo que reutiliza um identificador de processo.</span><span class="sxs-lookup"><span data-stu-id="0d51d-135">It is also possible that ParentProcessId incorrectly refers to a process that reuses a process identifier.</span></span>

<span data-ttu-id="0d51d-136">**Windows Server 2003:** Inclui o qualificador de formato ("x").</span><span class="sxs-lookup"><span data-stu-id="0d51d-136">**Windows Server 2003:** Includes the Format("x") qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="0d51d-137">ProcessId</span><span class="sxs-lookup"><span data-stu-id="0d51d-137">ProcessId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d51d-138">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0d51d-138">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0d51d-139">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0d51d-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d51d-140">Qualificadores: WmiDataId (2)</span><span class="sxs-lookup"><span data-stu-id="0d51d-140">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="0d51d-141">Identificador de processo global que você pode usar para identificar um processo.</span><span class="sxs-lookup"><span data-stu-id="0d51d-141">Global process identifier that you can use to identify a process.</span></span> <span data-ttu-id="0d51d-142">O valor é válido a partir do momento em que um processo é criado até ser encerrado.</span><span class="sxs-lookup"><span data-stu-id="0d51d-142">The value is valid from the time a process is created until it is terminated.</span></span>

<span data-ttu-id="0d51d-143">**Windows Server 2003:** Inclui o qualificador de formato ("x").</span><span class="sxs-lookup"><span data-stu-id="0d51d-143">**Windows Server 2003:** Includes the Format("x") qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="0d51d-144">SessionId</span><span class="sxs-lookup"><span data-stu-id="0d51d-144">SessionId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d51d-145">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0d51d-145">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0d51d-146">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0d51d-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d51d-147">Qualificadores: WmiDataId (4)</span><span class="sxs-lookup"><span data-stu-id="0d51d-147">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="0d51d-148">Identificador exclusivo que um sistema operacional gera ao criar uma nova sessão.</span><span class="sxs-lookup"><span data-stu-id="0d51d-148">Unique identifier that an operating system generates when it creates a new session.</span></span> <span data-ttu-id="0d51d-149">Uma sessão abrange um período de tempo do logon até o logoff de um sistema específico.</span><span class="sxs-lookup"><span data-stu-id="0d51d-149">A session spans a period of time from log on until log off from a specific system.</span></span>

</dd> <dt>

<span data-ttu-id="0d51d-150">UserSID</span><span class="sxs-lookup"><span data-stu-id="0d51d-150">UserSID</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d51d-151">Tipo de dados: **objeto**</span><span class="sxs-lookup"><span data-stu-id="0d51d-151">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="0d51d-152">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0d51d-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d51d-153">Qualificadores: WmiDataId (6), extensão ("Sid")</span><span class="sxs-lookup"><span data-stu-id="0d51d-153">Qualifiers: WmiDataId(6), Extension("Sid")</span></span>
</dt> </dl>

<span data-ttu-id="0d51d-154">SID (identificador de segurança) para o contexto do usuário no qual o evento ocorre.</span><span class="sxs-lookup"><span data-stu-id="0d51d-154">Security identifier (SID) for the user context under which the event happens.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0d51d-155">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0d51d-155">Requirements</span></span>



| <span data-ttu-id="0d51d-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d51d-156">Requirement</span></span> | <span data-ttu-id="0d51d-157">Valor</span><span class="sxs-lookup"><span data-stu-id="0d51d-157">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0d51d-158">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0d51d-158">Minimum supported client</span></span><br/> | <span data-ttu-id="0d51d-159">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="0d51d-159">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="0d51d-160">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0d51d-160">Minimum supported server</span></span><br/> | <span data-ttu-id="0d51d-161">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0d51d-161">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0d51d-162">Confira também</span><span class="sxs-lookup"><span data-stu-id="0d51d-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d51d-163">**Processo \_ v1**</span><span class="sxs-lookup"><span data-stu-id="0d51d-163">**Process\_V1**</span></span>](process.md)
</dt> <dt>

[<span data-ttu-id="0d51d-164">**Processo \_ v1**</span><span class="sxs-lookup"><span data-stu-id="0d51d-164">**Process\_V1**</span></span>](process-v1.md)
</dt> </dl>

 

 




