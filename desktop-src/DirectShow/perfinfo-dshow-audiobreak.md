---
description: A estrutura PERFINFO do \_ DShow \_ AUDIOBREAK contém dados para um evento de rastreamento do tipo Guid \_ AUDIOBREAK. O filtro de renderizador do DirectSound registra esse evento quando há uma interrupção no fluxo de áudio.
ms.assetid: 9e7abdca-7d4c-4006-997f-9605f8d18e1d
title: Estrutura de PERFINFO_DSHOW_AUDIOBREAK (Perfstruct. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PERFINFO_DSHOW_AUDIOBREAK
api_type:
- HeaderDef
api_location:
- Perfstruct.h
ms.openlocfilehash: 599befea67b28acbedffd5c98ebce84aadf70838
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758140"
---
# <a name="perfinfo_dshow_audiobreak-structure"></a><span data-ttu-id="c373f-103">Estrutura do PERFINFO \_ DShow \_ AUDIOBREAK</span><span class="sxs-lookup"><span data-stu-id="c373f-103">PERFINFO\_DSHOW\_AUDIOBREAK structure</span></span>

<span data-ttu-id="c373f-104">A `PERFINFO_DSHOW_AUDIOBREAK` estrutura contém dados para um evento de rastreamento do tipo Guid \_ AUDIOBREAK.</span><span class="sxs-lookup"><span data-stu-id="c373f-104">The `PERFINFO_DSHOW_AUDIOBREAK` structure contains data for a trace event of type GUID\_AUDIOBREAK.</span></span>

<span data-ttu-id="c373f-105">O filtro de [renderizador do DirectSound](directsound-renderer-filter.md) registra esse evento quando há uma interrupção no fluxo de áudio.</span><span class="sxs-lookup"><span data-stu-id="c373f-105">The [DirectSound Renderer](directsound-renderer-filter.md) filter logs this event when there is a break in the audio stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="c373f-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c373f-106">Syntax</span></span>


```C++
typedef struct PERFINFO_DSHOW_AUDIOBREAK {
  ULONGLONG cycleCounter;
  ULONGLONG dshowClock;
  ULONGLONG sampleTime;
  ULONGLONG sampleDuration;
} PERFINFO_DSHOW_AUDIOBREAK, *PPERFINFO_DSHOW_AUDIOBREAK;
```



## <a name="members"></a><span data-ttu-id="c373f-107">Membros</span><span class="sxs-lookup"><span data-stu-id="c373f-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="c373f-108">**cycleCounter**</span><span class="sxs-lookup"><span data-stu-id="c373f-108">**cycleCounter**</span></span>
</dt> <dd>

<span data-ttu-id="c373f-109">Contagem de ciclos de relógio mais recente (instrução RDTSC).</span><span class="sxs-lookup"><span data-stu-id="c373f-109">Latest clock cycle count (RDTSC instruction).</span></span>

</dd> <dt>

<span data-ttu-id="c373f-110">**dshowClock**</span><span class="sxs-lookup"><span data-stu-id="c373f-110">**dshowClock**</span></span>
</dt> <dd>

<span data-ttu-id="c373f-111">Posição de gravação atual no buffer do DirectSound.</span><span class="sxs-lookup"><span data-stu-id="c373f-111">Current write position in the DirectSound buffer.</span></span>

</dd> <dt>

<span data-ttu-id="c373f-112">**exemplo de**</span><span class="sxs-lookup"><span data-stu-id="c373f-112">**sampleTime**</span></span>
</dt> <dd>

<span data-ttu-id="c373f-113">Início do intervalo de áudio no buffer do DirectSound.</span><span class="sxs-lookup"><span data-stu-id="c373f-113">Start of the audio break in the DirectSound buffer.</span></span>

</dd> <dt>

<span data-ttu-id="c373f-114">**sampleDuration**</span><span class="sxs-lookup"><span data-stu-id="c373f-114">**sampleDuration**</span></span>
</dt> <dd>

<span data-ttu-id="c373f-115">Duração da interrupção, em milissegundos.</span><span class="sxs-lookup"><span data-stu-id="c373f-115">Duration of the break, in milliseconds.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c373f-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="c373f-116">Remarks</span></span>

<span data-ttu-id="c373f-117">Para habilitar esse evento, você deve definir o \_ sinalizador de bit AUDIOBREAK no parâmetro *EnableFlag* ao chamar **EnableTrace**.</span><span class="sxs-lookup"><span data-stu-id="c373f-117">To enable this event, you must set the AUDIOBREAK\_BIT flag in the *EnableFlag* parameter when you call **EnableTrace**.</span></span> <span data-ttu-id="c373f-118">Esse sinalizador é definido no arquivo de cabeçalho Dxmperf. h, que está incluído nas classes base do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="c373f-118">This flag is defined in the header file Dxmperf.h, which is included in the DirectShow base classes.</span></span>

<span data-ttu-id="c373f-119">Para registrar esse evento de um filtro do DirectShow, use a macro **PERFLOG \_ AUDIOBREAK** , que é definida em Dxmperf. h.</span><span class="sxs-lookup"><span data-stu-id="c373f-119">To log this event from a DirectShow filter, use the **PERFLOG\_AUDIOBREAK** macro, which is defined in Dxmperf.h.</span></span>

## <a name="requirements"></a><span data-ttu-id="c373f-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c373f-120">Requirements</span></span>



| <span data-ttu-id="c373f-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="c373f-121">Requirement</span></span> | <span data-ttu-id="c373f-122">Valor</span><span class="sxs-lookup"><span data-stu-id="c373f-122">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c373f-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c373f-123">Header</span></span><br/> | <dl> <span data-ttu-id="c373f-124"><dt>Perfstruct. h</dt></span><span class="sxs-lookup"><span data-stu-id="c373f-124"><dt>Perfstruct.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c373f-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="c373f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c373f-126">Estruturas do DirectShow</span><span class="sxs-lookup"><span data-stu-id="c373f-126">DirectShow Structures</span></span>](directshow-structures.md)
</dt> <dt>

[<span data-ttu-id="c373f-127">Rastreamento de eventos no DirectShow</span><span class="sxs-lookup"><span data-stu-id="c373f-127">Event Tracing in DirectShow</span></span>](event-tracing-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="c373f-128">GUIDs de evento de rastreamento</span><span class="sxs-lookup"><span data-stu-id="c373f-128">Trace Event GUIDs</span></span>](trace-guids.md)
</dt> </dl>

 

 




