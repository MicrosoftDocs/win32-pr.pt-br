---
description: A classe de tipo de evento para o evento de cabeçalho do arquivo de log. Essa classe contém informações sobre a sessão de rastreamento de eventos.
ms.assetid: 3d0c4044-da06-4850-95c4-99b4ea28fcd9
title: Classe EventTrace_Header
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EventTrace_Header
- EventTrace_Header.BufferSize
- EventTrace_Header.Version
- EventTrace_Header.ProviderVersion
- EventTrace_Header.NumberOfProcessors
- EventTrace_Header.EndTime
- EventTrace_Header.TimerResolution
- EventTrace_Header.MaxFileSize
- EventTrace_Header.LogFileMode
- EventTrace_Header.BuffersWritten
- EventTrace_Header.StartBuffers
- EventTrace_Header.PointerSize
- EventTrace_Header.EventsLost
- EventTrace_Header.CPUSpeed
- EventTrace_Header.LoggerName
- EventTrace_Header.LogFileName
- EventTrace_Header.TimeZoneInformation
- EventTrace_Header.BootTime
- EventTrace_Header.PerfFreq
- EventTrace_Header.StartTime
- EventTrace_Header.ReservedFlags
- EventTrace_Header.BuffersLost
api_type:
- NA
api_location: ''
ms.openlocfilehash: dea803849d6aa15c2a3a14deb850d85ade569116
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501926"
---
# <a name="eventtrace_header-class"></a><span data-ttu-id="93599-104">\_Classe de cabeçalho EventTrace</span><span class="sxs-lookup"><span data-stu-id="93599-104">EventTrace\_Header class</span></span>

<span data-ttu-id="93599-105">A classe de tipo de evento para o evento de cabeçalho do arquivo de log.</span><span class="sxs-lookup"><span data-stu-id="93599-105">The event type class for the log file header event.</span></span> <span data-ttu-id="93599-106">Essa classe contém informações sobre a sessão de rastreamento de eventos.</span><span class="sxs-lookup"><span data-stu-id="93599-106">This class contains information about the event tracing session.</span></span>

<span data-ttu-id="93599-107">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="93599-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="93599-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="93599-108">Syntax</span></span>

``` syntax
[EventType(0)]
class EventTrace_Header : EventTraceEvent
{
  uint32 BufferSize;
  uint32 Version;
  uint32 ProviderVersion;
  uint32 NumberOfProcessors;
  uint64 EndTime;
  uint32 TimerResolution;
  uint32 MaxFileSize;
  uint32 LogFileMode;
  uint32 BuffersWritten;
  uint32 StartBuffers;
  uint32 PointerSize;
  uint32 EventsLost;
  uint32 CPUSpeed;
  uint32 LoggerName;
  uint32 LogFileName;
  uint8  TimeZoneInformation[];
  uint64 BootTime;
  uint64 PerfFreq;
  uint64 StartTime;
  uint32 ReservedFlags;
  uint32 BuffersLost;
};
```

## <a name="members"></a><span data-ttu-id="93599-109">Membros</span><span class="sxs-lookup"><span data-stu-id="93599-109">Members</span></span>

<span data-ttu-id="93599-110">A classe de **\_ cabeçalho EventTrace** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="93599-110">The **EventTrace\_Header** class has these types of members:</span></span>

-   [<span data-ttu-id="93599-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="93599-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="93599-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="93599-112">Properties</span></span>

<span data-ttu-id="93599-113">A classe de **\_ cabeçalho EventTrace** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="93599-113">The **EventTrace\_Header** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="93599-114">**Boottime**</span><span class="sxs-lookup"><span data-stu-id="93599-114">**BootTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93599-115">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="93599-115">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="93599-116">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93599-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93599-117">Qualificadores: **WmiDataId** (17)</span><span class="sxs-lookup"><span data-stu-id="93599-117">Qualifiers: **WmiDataId** (17)</span></span>
</dt> </dl>

<span data-ttu-id="93599-118">Hora em que o sistema foi iniciado, em intervalos de 100 a nanossegundos desde a meia-noite, 1º de janeiro de 1601.</span><span class="sxs-lookup"><span data-stu-id="93599-118">Time at which the system was started, in 100-nanosecond intervals since midnight, January 1, 1601.</span></span>

</dd> <dt>

<span data-ttu-id="93599-119">**BufferSize**</span><span class="sxs-lookup"><span data-stu-id="93599-119">**BufferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93599-120">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="93599-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="93599-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93599-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93599-122">Qualificadores: **WmiDataId** (1)</span><span class="sxs-lookup"><span data-stu-id="93599-122">Qualifiers: **WmiDataId** (1)</span></span>
</dt> </dl>

<span data-ttu-id="93599-123">Tamanho dos buffers da sessão de rastreamento de eventos, em kilobytes.</span><span class="sxs-lookup"><span data-stu-id="93599-123">Size of the event tracing session's buffers, in kilobytes.</span></span>

</dd> <dt>

<span data-ttu-id="93599-124">**BuffersLost**</span><span class="sxs-lookup"><span data-stu-id="93599-124">**BuffersLost**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93599-125">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="93599-125">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="93599-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93599-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93599-127">Qualificadores: **WmiDataId** (21)</span><span class="sxs-lookup"><span data-stu-id="93599-127">Qualifiers: **WmiDataId** (21)</span></span>
</dt> </dl>

<span data-ttu-id="93599-128">Número total de buffers perdidos.</span><span class="sxs-lookup"><span data-stu-id="93599-128">Total number of buffers lost.</span></span>

</dd> <dt>

<span data-ttu-id="93599-129">**BuffersWritten**</span><span class="sxs-lookup"><span data-stu-id="93599-129">**BuffersWritten**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93599-130">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="93599-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="93599-131">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93599-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93599-132">Qualificadores: **WmiDataId** (9)</span><span class="sxs-lookup"><span data-stu-id="93599-132">Qualifiers: **WmiDataId** (9)</span></span>
</dt> </dl>

<span data-ttu-id="93599-133">Número total de buffers gravados pela sessão de rastreamento de eventos.</span><span class="sxs-lookup"><span data-stu-id="93599-133">Total number of buffers written by the event tracing session.</span></span>

</dd> <dt>

<span data-ttu-id="93599-134">**CPUSpeed**</span><span class="sxs-lookup"><span data-stu-id="93599-134">**CPUSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93599-135">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="93599-135">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="93599-136">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93599-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93599-137">Qualificadores: **WmiDataId** (13)</span><span class="sxs-lookup"><span data-stu-id="93599-137">Qualifiers: **WmiDataId** (13)</span></span>
</dt> </dl>

<span data-ttu-id="93599-138">Velocidade da CPU, em megahertz.</span><span class="sxs-lookup"><span data-stu-id="93599-138">CPU speed, in megahertz.</span></span>

<span data-ttu-id="93599-139">**Windows 2000:** Sem suporte.</span><span class="sxs-lookup"><span data-stu-id="93599-139">**Windows 2000:** Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="93599-140">**EndTime**</span><span class="sxs-lookup"><span data-stu-id="93599-140">**EndTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93599-141">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="93599-141">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="93599-142">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93599-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93599-143">Qualificadores: **WmiDataId** (5)</span><span class="sxs-lookup"><span data-stu-id="93599-143">Qualifiers: **WmiDataId** (5)</span></span>
</dt> </dl>

<span data-ttu-id="93599-144">Hora em que a sessão de rastreamento de eventos foi interrompida, em intervalos de 100 a nanossegundos desde a meia-noite, 1º de janeiro de 1601.</span><span class="sxs-lookup"><span data-stu-id="93599-144">Time at which the event tracing session stopped, in 100-nanosecond intervals since midnight, January 1, 1601.</span></span> <span data-ttu-id="93599-145">Esse valor pode ser 0 se você estiver consumindo eventos em tempo real ou de um arquivo de log ao qual o fornecimento ainda está registrando eventos.</span><span class="sxs-lookup"><span data-stu-id="93599-145">This value may be 0 if you are consuming events in real time or from a log file to which the provide is still logging events.</span></span>

</dd> <dt>

<span data-ttu-id="93599-146">**EventsLost**</span><span class="sxs-lookup"><span data-stu-id="93599-146">**EventsLost**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93599-147">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="93599-147">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="93599-148">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93599-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93599-149">Qualificadores: **WmiDataId** (12)</span><span class="sxs-lookup"><span data-stu-id="93599-149">Qualifiers: **WmiDataId** (12)</span></span>
</dt> </dl>

<span data-ttu-id="93599-150">Número de eventos perdidos durante a sessão de rastreamento de eventos.</span><span class="sxs-lookup"><span data-stu-id="93599-150">Number of events lost during the event tracing session.</span></span>

</dd> <dt>

<span data-ttu-id="93599-151">**LogFilemode**</span><span class="sxs-lookup"><span data-stu-id="93599-151">**LogFileMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93599-152">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="93599-152">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="93599-153">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93599-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93599-154">Qualificadores: **WmiDataId** (8), **formato ("x")**</span><span class="sxs-lookup"><span data-stu-id="93599-154">Qualifiers: **WmiDataId** (8), **Format("x")**</span></span>
</dt> </dl>

<span data-ttu-id="93599-155">Modo de log atual para a sessão de rastreamento de eventos.</span><span class="sxs-lookup"><span data-stu-id="93599-155">Current logging mode for the event tracing session.</span></span> <span data-ttu-id="93599-156">Para obter uma lista de valores, consulte constantes do modo de log.</span><span class="sxs-lookup"><span data-stu-id="93599-156">For a list of values, see Logging Mode Constants.</span></span>

</dd> <dt>

<span data-ttu-id="93599-157">**LogFileName**</span><span class="sxs-lookup"><span data-stu-id="93599-157">**LogFileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93599-158">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="93599-158">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="93599-159">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93599-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93599-160">Qualificadores: **WmiDataId** (15), **ponteiro**</span><span class="sxs-lookup"><span data-stu-id="93599-160">Qualifiers: **WmiDataId** (15), **Pointer**</span></span>
</dt> </dl>

<span data-ttu-id="93599-161">Nome do arquivo de log de rastreamento de eventos que contém os eventos.</span><span class="sxs-lookup"><span data-stu-id="93599-161">Name of the event tracing log file that contains the events.</span></span>

</dd> <dt>

<span data-ttu-id="93599-162">**Loggername**</span><span class="sxs-lookup"><span data-stu-id="93599-162">**LoggerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93599-163">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="93599-163">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="93599-164">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93599-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93599-165">Qualificadores: **WmiDataId** (14), **ponteiro**</span><span class="sxs-lookup"><span data-stu-id="93599-165">Qualifiers: **WmiDataId** (14), **Pointer**</span></span>
</dt> </dl>

<span data-ttu-id="93599-166">Nome da sessão de rastreamento de eventos.</span><span class="sxs-lookup"><span data-stu-id="93599-166">Name of the event tracing session.</span></span>

</dd> <dt>

<span data-ttu-id="93599-167">**Cedido**</span><span class="sxs-lookup"><span data-stu-id="93599-167">**MaxFileSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93599-168">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="93599-168">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="93599-169">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93599-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93599-170">Qualificadores: **WmiDataId** (7)</span><span class="sxs-lookup"><span data-stu-id="93599-170">Qualifiers: **WmiDataId** (7)</span></span>
</dt> </dl>

<span data-ttu-id="93599-171">Tamanho máximo do arquivo de log, em megabytes.</span><span class="sxs-lookup"><span data-stu-id="93599-171">Maximum size of the log file, in megabytes.</span></span>

</dd> <dt>

<span data-ttu-id="93599-172">**NumberOfProcessors**</span><span class="sxs-lookup"><span data-stu-id="93599-172">**NumberOfProcessors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93599-173">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="93599-173">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="93599-174">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93599-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93599-175">Qualificadores: **WmiDataId** (4)</span><span class="sxs-lookup"><span data-stu-id="93599-175">Qualifiers: **WmiDataId** (4)</span></span>
</dt> </dl>

<span data-ttu-id="93599-176">Número de processadores no sistema.</span><span class="sxs-lookup"><span data-stu-id="93599-176">Number of processors on the system.</span></span>

</dd> <dt>

<span data-ttu-id="93599-177">**PerfFreq**</span><span class="sxs-lookup"><span data-stu-id="93599-177">**PerfFreq**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93599-178">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="93599-178">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="93599-179">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93599-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93599-180">Qualificadores: **WmiDataId** (18)</span><span class="sxs-lookup"><span data-stu-id="93599-180">Qualifiers: **WmiDataId** (18)</span></span>
</dt> </dl>

<span data-ttu-id="93599-181">Frequência do contador de desempenho de alta resolução, se houver.</span><span class="sxs-lookup"><span data-stu-id="93599-181">Frequency of the high-resolution performance counter, if one exists.</span></span>

</dd> <dt>

<span data-ttu-id="93599-182">**Ponteiros**</span><span class="sxs-lookup"><span data-stu-id="93599-182">**PointerSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93599-183">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="93599-183">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="93599-184">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93599-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93599-185">Qualificadores: **WmiDataId** (11)</span><span class="sxs-lookup"><span data-stu-id="93599-185">Qualifiers: **WmiDataId** (11)</span></span>
</dt> </dl>

<span data-ttu-id="93599-186">Tamanho de um tipo de dados de ponteiro, em bytes.</span><span class="sxs-lookup"><span data-stu-id="93599-186">Size of a pointer data type, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="93599-187">**ProviderVersion**</span><span class="sxs-lookup"><span data-stu-id="93599-187">**ProviderVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93599-188">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="93599-188">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="93599-189">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93599-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93599-190">Qualificadores: **WmiDataId** (3)</span><span class="sxs-lookup"><span data-stu-id="93599-190">Qualifiers: **WmiDataId** (3)</span></span>
</dt> </dl>

<span data-ttu-id="93599-191">Número de Build do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="93599-191">Build number of the operating system.</span></span>

</dd> <dt>

<span data-ttu-id="93599-192">**ReservedFlags**</span><span class="sxs-lookup"><span data-stu-id="93599-192">**ReservedFlags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93599-193">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="93599-193">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="93599-194">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93599-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93599-195">Qualificadores: **WmiDataId** (20)</span><span class="sxs-lookup"><span data-stu-id="93599-195">Qualifiers: **WmiDataId** (20)</span></span>
</dt> </dl>

<span data-ttu-id="93599-196">Reservado.</span><span class="sxs-lookup"><span data-stu-id="93599-196">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="93599-197">**StartBuffers**</span><span class="sxs-lookup"><span data-stu-id="93599-197">**StartBuffers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93599-198">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="93599-198">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="93599-199">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93599-199">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93599-200">Qualificadores: **WmiDataId** (10)</span><span class="sxs-lookup"><span data-stu-id="93599-200">Qualifiers: **WmiDataId** (10)</span></span>
</dt> </dl>

<span data-ttu-id="93599-201">Reservado.</span><span class="sxs-lookup"><span data-stu-id="93599-201">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="93599-202">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="93599-202">**StartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93599-203">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="93599-203">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="93599-204">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93599-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93599-205">Qualificadores: **WmiDataId** (19)</span><span class="sxs-lookup"><span data-stu-id="93599-205">Qualifiers: **WmiDataId** (19)</span></span>
</dt> </dl>

<span data-ttu-id="93599-206">Hora em que a sessão de rastreamento de eventos foi iniciada, em intervalos de 100 a nanossegundos desde a meia-noite, 1º de janeiro de 1601.</span><span class="sxs-lookup"><span data-stu-id="93599-206">Time at which the event tracing session started, in 100-nanosecond intervals since midnight, January 1, 1601.</span></span>

</dd> <dt>

<span data-ttu-id="93599-207">**TimerResolution**</span><span class="sxs-lookup"><span data-stu-id="93599-207">**TimerResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93599-208">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="93599-208">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="93599-209">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93599-209">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93599-210">Qualificadores: **WmiDataId** (6)</span><span class="sxs-lookup"><span data-stu-id="93599-210">Qualifiers: **WmiDataId** (6)</span></span>
</dt> </dl>

<span data-ttu-id="93599-211">Resolução do temporizador de hardware, em unidades de 100 nanossegundos.</span><span class="sxs-lookup"><span data-stu-id="93599-211">Resolution of the hardware timer, in units of 100 nanoseconds.</span></span>

</dd> <dt>

<span data-ttu-id="93599-212">**TimeZoneInformation**</span><span class="sxs-lookup"><span data-stu-id="93599-212">**TimeZoneInformation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93599-213">Tipo de dados: matriz **uint8**</span><span class="sxs-lookup"><span data-stu-id="93599-213">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="93599-214">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93599-214">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93599-215">Qualificadores: **WmiDataId** (16), **extensão ("noprint")**, **Max** (176)</span><span class="sxs-lookup"><span data-stu-id="93599-215">Qualifiers: **WmiDataId** (16), **Extension("NoPrint")**, **Max** (176)</span></span>
</dt> </dl>

<span data-ttu-id="93599-216">Uma estrutura de [**\_ \_ informações de fuso horário**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) que contém o fuso horário para os membros **boottime**, **EndTime** e **StartTime** .</span><span class="sxs-lookup"><span data-stu-id="93599-216">A [**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) structure that contains the time zone for the **BootTime**, **EndTime** and **StartTime** members.</span></span>

</dd> <dt>

<span data-ttu-id="93599-217">**Versão**</span><span class="sxs-lookup"><span data-stu-id="93599-217">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93599-218">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="93599-218">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="93599-219">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93599-219">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93599-220">Qualificadores: **WmiDataId** (2)</span><span class="sxs-lookup"><span data-stu-id="93599-220">Qualifiers: **WmiDataId** (2)</span></span>
</dt> </dl>

<span data-ttu-id="93599-221">Número de versão do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="93599-221">Version number of the operating system.</span></span> <span data-ttu-id="93599-222">Começando com os bytes de ordem inferior, os dois primeiros bytes contêm a versão principal, os dois próximos bytes contêm uma versão secundária, os dois próximos bytes contêm service pack versão principal e os dois últimos bytes contêm service pack versão secundária.</span><span class="sxs-lookup"><span data-stu-id="93599-222">Starting with the low-order bytes, the first two bytes contain major version, the next two bytes contain minor version, the next two bytes contain service pack major version, and the last two bytes contain service pack minor version.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="93599-223">Comentários</span><span class="sxs-lookup"><span data-stu-id="93599-223">Remarks</span></span>

<span data-ttu-id="93599-224">Normalmente, você deseja salvar os valores para as propriedades a seguir para uso posterior ao processar eventos do arquivo de log.</span><span class="sxs-lookup"><span data-stu-id="93599-224">Typically, you want to save the values for the following properties for use later when processing events from the log file.</span></span>

-   <span data-ttu-id="93599-225">**TimerResolution**— use com os membros de **kerneltime** e **usertime** da estrutura do [**\_ \_ cabeçalho de rastreamento de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) para determinar o custo da CPU para um conjunto de instruções.</span><span class="sxs-lookup"><span data-stu-id="93599-225">**TimerResolution**—use with the **KernelTime** and **UserTime** members of the [**EVENT\_TRACE\_HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) structure to determine the CPU cost for a set of instructions.</span></span> <span data-ttu-id="93599-226">Para obter detalhes, consulte a seção comentários [**do \_ \_ cabeçalho de rastreamento de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header).</span><span class="sxs-lookup"><span data-stu-id="93599-226">For details, see the Remarks section of [**EVENT\_TRACE\_HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header).</span></span>
-   <span data-ttu-id="93599-227">**Ponteiroize**– para propriedades que contêm o qualificador de **ponteiro** , use esse valor para determinar o tamanho do ponteiro.</span><span class="sxs-lookup"><span data-stu-id="93599-227">**PointerSize**—for properties that contain the **Pointer** qualifier, use this value to determine the size of the pointer.</span></span> <span data-ttu-id="93599-228">Observe que esse valor pode não ser preciso.</span><span class="sxs-lookup"><span data-stu-id="93599-228">Note that this value may not be accurate.</span></span> <span data-ttu-id="93599-229">Por exemplo, em um computador de 64 bits, um aplicativo de 32 bits registrará ponteiros de 4 bytes; no entanto, a sessão definirá **ponteiros** para 8.</span><span class="sxs-lookup"><span data-stu-id="93599-229">For example, on a 64-bit computer, a 32-bit application will log 4-byte pointers; however, the session will set **PointerSize** to 8.</span></span>
-   <span data-ttu-id="93599-230">**LOGFILEMODE**— use para determinar se esta sessão é uma sessão de agente de log particular.</span><span class="sxs-lookup"><span data-stu-id="93599-230">**LogFileMode**—use to determine if this session is a private logger session.</span></span> <span data-ttu-id="93599-231">Há algumas propriedades que não contêm dados para sessões de agente particular.</span><span class="sxs-lookup"><span data-stu-id="93599-231">There are some properties that do not contain data for private logger sessions.</span></span> <span data-ttu-id="93599-232">Por exemplo, os membros **kerneltime** e **usertime** da estrutura [**do \_ \_ cabeçalho de rastreamento de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) .</span><span class="sxs-lookup"><span data-stu-id="93599-232">For example, the **KernelTime** and **UserTime** members of the [**EVENT\_TRACE\_HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="93599-233">Requisitos</span><span class="sxs-lookup"><span data-stu-id="93599-233">Requirements</span></span>



| <span data-ttu-id="93599-234">Requisito</span><span class="sxs-lookup"><span data-stu-id="93599-234">Requirement</span></span> | <span data-ttu-id="93599-235">Valor</span><span class="sxs-lookup"><span data-stu-id="93599-235">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="93599-236">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="93599-236">Minimum supported client</span></span><br/> | <span data-ttu-id="93599-237">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="93599-237">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="93599-238">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="93599-238">Minimum supported server</span></span><br/> | <span data-ttu-id="93599-239">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="93599-239">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="93599-240">Confira também</span><span class="sxs-lookup"><span data-stu-id="93599-240">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93599-241">**EventTraceEvent**</span><span class="sxs-lookup"><span data-stu-id="93599-241">**EventTraceEvent**</span></span>](eventtraceevent.md)
</dt> <dt>

[<span data-ttu-id="93599-242">**cabeçalho do arquivo de log de rastreamento \_ \_**</span><span class="sxs-lookup"><span data-stu-id="93599-242">**TRACE\_LOGFILE\_HEADER**</span></span>](/windows/win32/api/evntrace/ns-evntrace-trace_logfile_header)
</dt> </dl>

 

 
