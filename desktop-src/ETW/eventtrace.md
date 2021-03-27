---
description: Uma classe abstrata da qual todas as classes de rastreamento de eventos são derivadas.
ms.assetid: 03eea902-5050-4ab2-8a72-9bff7777e234
title: Classe EventTrace
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EventTrace
- EventTrace.EventSize
- EventTrace.ReservedHeaderField
- EventTrace.EventType
- EventTrace.TraceLevel
- EventTrace.TraceVersion
- EventTrace.ThreadId
- EventTrace.TimeStamp
- EventTrace.EventGuid
- EventTrace.KernelTime
- EventTrace.UserTime
- EventTrace.InstanceId
- EventTrace.ParentGuid
- EventTrace.ParentInstanceId
- EventTrace.MofData
- EventTrace.MofLength
api_type:
- NA
api_location: ''
ms.openlocfilehash: f04399942b39a2da5b746933884a436a65bb370c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647376"
---
# <a name="eventtrace-class"></a><span data-ttu-id="1043b-103">Classe EventTrace</span><span class="sxs-lookup"><span data-stu-id="1043b-103">EventTrace class</span></span>

<span data-ttu-id="1043b-104">Uma classe abstrata da qual todas as classes de rastreamento de eventos são derivadas.</span><span class="sxs-lookup"><span data-stu-id="1043b-104">An abstract class from which all event trace classes are derived.</span></span>

<span data-ttu-id="1043b-105">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="1043b-105">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="1043b-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1043b-106">Syntax</span></span>

``` syntax
[abstract]
class EventTrace
{
  uint16 EventSize;
  uint16 ReservedHeaderField;
  uint8  EventType;
  uint8  TraceLevel;
  uint16 TraceVersion;
  uint64 ThreadId;
  uint64 TimeStamp;
  uint8  EventGuid[];
  uint32 KernelTime;
  uint32 UserTime;
  uint32 InstanceId;
  uint8  ParentGuid[];
  uint32 ParentInstanceId;
  uint32 MofData;
  uint32 MofLength;
};
```

## <a name="members"></a><span data-ttu-id="1043b-107">Membros</span><span class="sxs-lookup"><span data-stu-id="1043b-107">Members</span></span>

<span data-ttu-id="1043b-108">A classe **EventTrace** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="1043b-108">The **EventTrace** class has these types of members:</span></span>

-   [<span data-ttu-id="1043b-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1043b-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1043b-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1043b-110">Properties</span></span>

<span data-ttu-id="1043b-111">A classe **EventTrace** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="1043b-111">The **EventTrace** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1043b-112">**EventGuid**</span><span class="sxs-lookup"><span data-stu-id="1043b-112">**EventGuid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1043b-113">Tipo de dados: matriz **uint8**</span><span class="sxs-lookup"><span data-stu-id="1043b-113">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="1043b-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1043b-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1043b-115">Qualificadores: **WmiDataId** (8), **máx** . (16)</span><span class="sxs-lookup"><span data-stu-id="1043b-115">Qualifiers: **WmiDataId** (8), **Max** (16)</span></span>
</dt> </dl>

<span data-ttu-id="1043b-116">GUID da classe de rastreamento de eventos deste evento.</span><span class="sxs-lookup"><span data-stu-id="1043b-116">Event trace class GUID of this event.</span></span>

</dd> <dt>

<span data-ttu-id="1043b-117">**Eventos de**</span><span class="sxs-lookup"><span data-stu-id="1043b-117">**EventSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1043b-118">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1043b-118">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1043b-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1043b-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1043b-120">Qualificadores: **WmiDataId** (1)</span><span class="sxs-lookup"><span data-stu-id="1043b-120">Qualifiers: **WmiDataId** (1)</span></span>
</dt> </dl>

<span data-ttu-id="1043b-121">Número total de bytes do evento.</span><span class="sxs-lookup"><span data-stu-id="1043b-121">Total number of bytes of the event.</span></span>

</dd> <dt>

<span data-ttu-id="1043b-122">**EventType**</span><span class="sxs-lookup"><span data-stu-id="1043b-122">**EventType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1043b-123">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="1043b-123">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="1043b-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1043b-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1043b-125">Qualificadores: **WmiDataId** (3)</span><span class="sxs-lookup"><span data-stu-id="1043b-125">Qualifiers: **WmiDataId** (3)</span></span>
</dt> </dl>

<span data-ttu-id="1043b-126">Tipo de evento definido pelo provedor.</span><span class="sxs-lookup"><span data-stu-id="1043b-126">Provider-defined event type.</span></span> <span data-ttu-id="1043b-127">Informa qual classe de tipo de evento deve ser usada para decifrar os dados de evento definidos pelo provedor (os dados apontados por **MofData**.</span><span class="sxs-lookup"><span data-stu-id="1043b-127">Tells you which event type class to use to decipher the provider-defined event data (the data pointed to by **MofData**.</span></span>

</dd> <dt>

<span data-ttu-id="1043b-128">**InstanceId**</span><span class="sxs-lookup"><span data-stu-id="1043b-128">**InstanceId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1043b-129">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1043b-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1043b-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1043b-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1043b-131">Qualificadores: **WmiDataId** (11)</span><span class="sxs-lookup"><span data-stu-id="1043b-131">Qualifiers: **WmiDataId** (11)</span></span>
</dt> </dl>

<span data-ttu-id="1043b-132">Identificador desta instância de evento.</span><span class="sxs-lookup"><span data-stu-id="1043b-132">Identifier of this event instance.</span></span>

</dd> <dt>

<span data-ttu-id="1043b-133">**Kerneltime**</span><span class="sxs-lookup"><span data-stu-id="1043b-133">**KernelTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1043b-134">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1043b-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1043b-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1043b-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1043b-136">Qualificadores: **WmiDataId** (9)</span><span class="sxs-lookup"><span data-stu-id="1043b-136">Qualifiers: **WmiDataId** (9)</span></span>
</dt> </dl>

<span data-ttu-id="1043b-137">Tempo de execução decorrido para instruções do modo kernel, em tiques de CPU.</span><span class="sxs-lookup"><span data-stu-id="1043b-137">Elapsed execution time for kernel-mode instructions, in CPU ticks.</span></span>

</dd> <dt>

<span data-ttu-id="1043b-138">**MofData**</span><span class="sxs-lookup"><span data-stu-id="1043b-138">**MofData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1043b-139">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1043b-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1043b-140">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1043b-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1043b-141">Qualificadores: **WmiDataId** (14), **ponteiro**</span><span class="sxs-lookup"><span data-stu-id="1043b-141">Qualifiers: **WmiDataId** (14), **Pointer**</span></span>
</dt> </dl>

<span data-ttu-id="1043b-142">Ponteiro para os dados de evento específicos do provedor.</span><span class="sxs-lookup"><span data-stu-id="1043b-142">Pointer to the provider-specific event data.</span></span>

</dd> <dt>

<span data-ttu-id="1043b-143">**MofLength**</span><span class="sxs-lookup"><span data-stu-id="1043b-143">**MofLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1043b-144">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1043b-144">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1043b-145">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1043b-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1043b-146">Qualificadores: **WmiDataId** (15)</span><span class="sxs-lookup"><span data-stu-id="1043b-146">Qualifiers: **WmiDataId** (15)</span></span>
</dt> </dl>

<span data-ttu-id="1043b-147">Comprimento dos dados de evento específicos do provedor.</span><span class="sxs-lookup"><span data-stu-id="1043b-147">Length of the provider-specific event data.</span></span>

</dd> <dt>

<span data-ttu-id="1043b-148">**ParentGuid**</span><span class="sxs-lookup"><span data-stu-id="1043b-148">**ParentGuid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1043b-149">Tipo de dados: matriz **uint8**</span><span class="sxs-lookup"><span data-stu-id="1043b-149">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="1043b-150">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1043b-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1043b-151">Qualificadores: **WmiDataId** (12), **máx** . (16)</span><span class="sxs-lookup"><span data-stu-id="1043b-151">Qualifiers: **WmiDataId** (12), **Max** (16)</span></span>
</dt> </dl>

<span data-ttu-id="1043b-152">GUID da classe de rastreamento de eventos da instância pai.</span><span class="sxs-lookup"><span data-stu-id="1043b-152">Event trace class GUID of the parent instance.</span></span>

</dd> <dt>

<span data-ttu-id="1043b-153">**ParentInstanceId**</span><span class="sxs-lookup"><span data-stu-id="1043b-153">**ParentInstanceId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1043b-154">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1043b-154">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1043b-155">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1043b-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1043b-156">Qualificadores: **WmiDataId** (13)</span><span class="sxs-lookup"><span data-stu-id="1043b-156">Qualifiers: **WmiDataId** (13)</span></span>
</dt> </dl>

<span data-ttu-id="1043b-157">Identificador dos dados da instância pai.</span><span class="sxs-lookup"><span data-stu-id="1043b-157">Identifier of the parent instance data.</span></span>

</dd> <dt>

<span data-ttu-id="1043b-158">**ReservedHeaderField**</span><span class="sxs-lookup"><span data-stu-id="1043b-158">**ReservedHeaderField**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1043b-159">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1043b-159">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1043b-160">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1043b-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1043b-161">Qualificadores: **WmiDataId** (2)</span><span class="sxs-lookup"><span data-stu-id="1043b-161">Qualifiers: **WmiDataId** (2)</span></span>
</dt> </dl>

<span data-ttu-id="1043b-162">Reservado.</span><span class="sxs-lookup"><span data-stu-id="1043b-162">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="1043b-163">**ThreadId**</span><span class="sxs-lookup"><span data-stu-id="1043b-163">**ThreadId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1043b-164">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1043b-164">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1043b-165">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1043b-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1043b-166">Qualificadores: **WmiDataId** (6), **ponteiro**</span><span class="sxs-lookup"><span data-stu-id="1043b-166">Qualifiers: **WmiDataId** (6), **Pointer**</span></span>
</dt> </dl>

<span data-ttu-id="1043b-167">Identifica o thread que gerou o evento.</span><span class="sxs-lookup"><span data-stu-id="1043b-167">Identifies the thread that generated the event.</span></span>

</dd> <dt>

<span data-ttu-id="1043b-168">**Estampa**</span><span class="sxs-lookup"><span data-stu-id="1043b-168">**TimeStamp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1043b-169">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1043b-169">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1043b-170">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1043b-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1043b-171">Qualificadores: **WmiDataId** (7)</span><span class="sxs-lookup"><span data-stu-id="1043b-171">Qualifiers: **WmiDataId** (7)</span></span>
</dt> </dl>

<span data-ttu-id="1043b-172">Contém a data e a hora em que o evento ocorreu.</span><span class="sxs-lookup"><span data-stu-id="1043b-172">Contains the date and time when the event occurred.</span></span>

</dd> <dt>

<span data-ttu-id="1043b-173">**TraceLevel**</span><span class="sxs-lookup"><span data-stu-id="1043b-173">**TraceLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1043b-174">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="1043b-174">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="1043b-175">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1043b-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1043b-176">Qualificadores: **WmiDataId** (4)</span><span class="sxs-lookup"><span data-stu-id="1043b-176">Qualifiers: **WmiDataId** (4)</span></span>
</dt> </dl>

<span data-ttu-id="1043b-177">Valor definido pelo provedor que define o nível de severidade usado para gerar o evento.</span><span class="sxs-lookup"><span data-stu-id="1043b-177">Provider-defined value that defines the severity level used to generate the event.</span></span>

</dd> <dt>

<span data-ttu-id="1043b-178">**TraceVersion**</span><span class="sxs-lookup"><span data-stu-id="1043b-178">**TraceVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1043b-179">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1043b-179">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1043b-180">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1043b-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1043b-181">Qualificadores: **WmiDataId** (5)</span><span class="sxs-lookup"><span data-stu-id="1043b-181">Qualifiers: **WmiDataId** (5)</span></span>
</dt> </dl>

<span data-ttu-id="1043b-182">Número de versão definido pelo provedor da classe de rastreamento de eventos usada para gerar o evento.</span><span class="sxs-lookup"><span data-stu-id="1043b-182">Provider-defined version number of the event trace class used to generate the event.</span></span>

</dd> <dt>

<span data-ttu-id="1043b-183">**Usertime**</span><span class="sxs-lookup"><span data-stu-id="1043b-183">**UserTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1043b-184">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1043b-184">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1043b-185">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1043b-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1043b-186">Qualificadores: **WmiDataId** (10)</span><span class="sxs-lookup"><span data-stu-id="1043b-186">Qualifiers: **WmiDataId** (10)</span></span>
</dt> </dl>

<span data-ttu-id="1043b-187">Tempo de execução decorrido para instruções do modo de usuário, em tiques de CPU.</span><span class="sxs-lookup"><span data-stu-id="1043b-187">Elapsed execution time for user-mode instructions, in CPU ticks.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1043b-188">Comentários</span><span class="sxs-lookup"><span data-stu-id="1043b-188">Remarks</span></span>

<span data-ttu-id="1043b-189">Não use essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="1043b-189">Do not use these properties.</span></span>

## <a name="requirements"></a><span data-ttu-id="1043b-190">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1043b-190">Requirements</span></span>



| <span data-ttu-id="1043b-191">Requisito</span><span class="sxs-lookup"><span data-stu-id="1043b-191">Requirement</span></span> | <span data-ttu-id="1043b-192">Valor</span><span class="sxs-lookup"><span data-stu-id="1043b-192">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1043b-193">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1043b-193">Minimum supported client</span></span><br/> | <span data-ttu-id="1043b-194">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="1043b-194">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="1043b-195">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1043b-195">Minimum supported server</span></span><br/> | <span data-ttu-id="1043b-196">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="1043b-196">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="1043b-197">MOF</span><span class="sxs-lookup"><span data-stu-id="1043b-197">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1043b-198"><dt>WMI. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1043b-198"><dt>Wmi.mof</dt></span></span> </dl> |



 

 




