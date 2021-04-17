---
description: A estrutura PERFINFO do \_ DShow \_ AVREND contém dados para um evento de rastreamento do tipo Guid \_ VIDEOREND. O VMR registra esse evento imediatamente antes de renderizar um quadro.
ms.assetid: 95deda21-0ef4-4bf0-9fa3-826a813757b9
title: Estrutura de PERFINFO_DSHOW_AVREND (Perfstruct. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PERFINFO_DSHOW_AVREND
api_type:
- HeaderDef
api_location:
- Perfstruct.h
ms.openlocfilehash: ee2d944d086f9c1a4ea7944f023321dfbc06d547
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780046"
---
# <a name="perfinfo_dshow_avrend-structure"></a><span data-ttu-id="aea37-103">Estrutura do PERFINFO \_ DShow \_ AVREND</span><span class="sxs-lookup"><span data-stu-id="aea37-103">PERFINFO\_DSHOW\_AVREND structure</span></span>

<span data-ttu-id="aea37-104">A `PERFINFO_DSHOW_AVREND` estrutura contém dados para um evento de rastreamento do tipo Guid \_ VIDEOREND.</span><span class="sxs-lookup"><span data-stu-id="aea37-104">The `PERFINFO_DSHOW_AVREND` structure contains data for a trace event of type GUID\_VIDEOREND.</span></span>

<span data-ttu-id="aea37-105">O VMR registra esse evento imediatamente antes de renderizar um quadro.</span><span class="sxs-lookup"><span data-stu-id="aea37-105">The VMR logs this event immediately before rendering a frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="aea37-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="aea37-106">Syntax</span></span>


```C++
typedef struct PERFINFO_DSHOW_AVREND {
  ULONGLONG cycleCounter;
  ULONGLONG dshowClock;
  ULONGLONG sampleTime;
} PERFINFO_DSHOW_AVREND, *PPERFINFO_DSHOW_AVREND;
```



## <a name="members"></a><span data-ttu-id="aea37-107">Membros</span><span class="sxs-lookup"><span data-stu-id="aea37-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="aea37-108">**cycleCounter**</span><span class="sxs-lookup"><span data-stu-id="aea37-108">**cycleCounter**</span></span>
</dt> <dd>

<span data-ttu-id="aea37-109">Contagem de ciclos de relógio mais recente (instrução RDTSC).</span><span class="sxs-lookup"><span data-stu-id="aea37-109">Latest clock cycle count (RDTSC instruction).</span></span>

</dd> <dt>

<span data-ttu-id="aea37-110">**dshowClock**</span><span class="sxs-lookup"><span data-stu-id="aea37-110">**dshowClock**</span></span>
</dt> <dd>

<span data-ttu-id="aea37-111">Tempo de referência atual, conforme retornado pelo método [**IReferenceClock:: getTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) .</span><span class="sxs-lookup"><span data-stu-id="aea37-111">Current reference time, as returned by the [**IReferenceClock::GetTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) method.</span></span>

</dd> <dt>

<span data-ttu-id="aea37-112">**exemplo de**</span><span class="sxs-lookup"><span data-stu-id="aea37-112">**sampleTime**</span></span>
</dt> <dd>

<span data-ttu-id="aea37-113">Hora de início do exemplo.</span><span class="sxs-lookup"><span data-stu-id="aea37-113">Start time of the sample.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="aea37-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="aea37-114">Remarks</span></span>

<span data-ttu-id="aea37-115">Para habilitar esse evento, você deve definir o \_ sinalizador DXMPERF VIDEOREND no parâmetro *EnableFlag* ao chamar **EnableTrace**.</span><span class="sxs-lookup"><span data-stu-id="aea37-115">To enable this event, you must set the DXMPERF\_VIDEOREND flag in the *EnableFlag* parameter when you call **EnableTrace**.</span></span> <span data-ttu-id="aea37-116">Esse sinalizador é definido no arquivo de cabeçalho Dxmperf. h, que está incluído nas classes base do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="aea37-116">This flag is defined in the header file Dxmperf.h, which is included in the DirectShow base classes.</span></span>

<span data-ttu-id="aea37-117">Para registrar esse evento de um filtro do DirectShow, use a macro **PERFLOG \_ VIDEOREND** , que é definida em Dxmperf. h.</span><span class="sxs-lookup"><span data-stu-id="aea37-117">To log this event from a DirectShow filter, use the **PERFLOG\_VIDEOREND** macro, which is defined in Dxmperf.h.</span></span>

## <a name="requirements"></a><span data-ttu-id="aea37-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aea37-118">Requirements</span></span>



| <span data-ttu-id="aea37-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="aea37-119">Requirement</span></span> | <span data-ttu-id="aea37-120">Valor</span><span class="sxs-lookup"><span data-stu-id="aea37-120">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="aea37-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="aea37-121">Header</span></span><br/> | <dl> <span data-ttu-id="aea37-122"><dt>Perfstruct. h</dt></span><span class="sxs-lookup"><span data-stu-id="aea37-122"><dt>Perfstruct.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aea37-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="aea37-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aea37-124">Estruturas do DirectShow</span><span class="sxs-lookup"><span data-stu-id="aea37-124">DirectShow Structures</span></span>](directshow-structures.md)
</dt> <dt>

[<span data-ttu-id="aea37-125">Rastreamento de eventos no DirectShow</span><span class="sxs-lookup"><span data-stu-id="aea37-125">Event Tracing in DirectShow</span></span>](event-tracing-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="aea37-126">GUIDs de evento de rastreamento</span><span class="sxs-lookup"><span data-stu-id="aea37-126">Trace Event GUIDs</span></span>](trace-guids.md)
</dt> </dl>

 

 




