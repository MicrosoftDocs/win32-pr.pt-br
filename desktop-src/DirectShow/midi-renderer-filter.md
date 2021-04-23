---
description: O filtro de renderizador MIDI renderiza dados MIDI do filtro analisador de MIDI.
ms.assetid: 2675a21d-41d0-4095-96c4-f12f52c00d5a
title: Filtro de renderizador MIDI (Windows. Devices. MIDI. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MIDI
api_type:
- HeaderDef
api_location:
- windows.devices.midi.h
ms.openlocfilehash: 5fa27ceda0c249f88f4684979382495167cb9238
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909404"
---
# <a name="midi-renderer-filter"></a><span data-ttu-id="95b12-103">Filtro de renderizador MIDI</span><span class="sxs-lookup"><span data-stu-id="95b12-103">MIDI Renderer Filter</span></span>

<span data-ttu-id="95b12-104">O filtro de renderizador MIDI renderiza dados MIDI do filtro [analisador de Midi](midi-parser-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="95b12-104">The MIDI Renderer filter renders MIDI data from the [MIDI Parser](midi-parser-filter.md) filter.</span></span>



| <span data-ttu-id="95b12-105">Label</span><span class="sxs-lookup"><span data-stu-id="95b12-105">Label</span></span> | <span data-ttu-id="95b12-106">Valor</span><span class="sxs-lookup"><span data-stu-id="95b12-106">Value</span></span> |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95b12-107">Filtrar interfaces</span><span class="sxs-lookup"><span data-stu-id="95b12-107">Filter Interfaces</span></span>                        | <span data-ttu-id="95b12-108">[**IAMClockSlave**](/windows/desktop/api/Strmif/nn-strmif-iamclockslave), [**IAMDirectSound**](/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound), [**IAMResourceControl**](/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IBasicAudio**](/windows/desktop/api/Control/nn-control-ibasicaudio), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol), [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock)</span><span class="sxs-lookup"><span data-stu-id="95b12-108">[**IAMClockSlave**](/windows/desktop/api/Strmif/nn-strmif-iamclockslave), [**IAMDirectSound**](/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound), [**IAMResourceControl**](/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IBasicAudio**](/windows/desktop/api/Control/nn-control-ibasicaudio), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol), [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock)</span></span> |
| <span data-ttu-id="95b12-109">Tipos de mídia de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="95b12-109">Input Pin Media Types</span></span>                    | <span data-ttu-id="95b12-110">\_MEDIASUBTYPE de mídia MIDI, \_ nulo</span><span class="sxs-lookup"><span data-stu-id="95b12-110">MEDIATYPE\_Midi, MEDIASUBTYPE\_NULL</span></span>                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="95b12-111">Interfaces de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="95b12-111">Input Pin Interfaces</span></span>                     | <span data-ttu-id="95b12-112">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="95b12-112">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="95b12-113">Tipos de mídia do pino de saída</span><span class="sxs-lookup"><span data-stu-id="95b12-113">Output Pin Media Types</span></span>                   | <span data-ttu-id="95b12-114">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="95b12-114">Not applicable</span></span>                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="95b12-115">Interfaces de pino de saída</span><span class="sxs-lookup"><span data-stu-id="95b12-115">Output Pin Interfaces</span></span>                    | <span data-ttu-id="95b12-116">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="95b12-116">Not applicable</span></span>                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="95b12-117">CLSID do filtro</span><span class="sxs-lookup"><span data-stu-id="95b12-117">Filter CLSID</span></span>                             | <span data-ttu-id="95b12-118">\_AVIMIDIRENDER CLSID</span><span class="sxs-lookup"><span data-stu-id="95b12-118">CLSID\_AVIMIDIRender</span></span>                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="95b12-119">CLSID de página de propriedades</span><span class="sxs-lookup"><span data-stu-id="95b12-119">Property Page CLSID</span></span>                      | <span data-ttu-id="95b12-120">Nenhuma página de propriedades</span><span class="sxs-lookup"><span data-stu-id="95b12-120">No property page</span></span>                                                                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="95b12-121">Executável</span><span class="sxs-lookup"><span data-stu-id="95b12-121">Executable</span></span>                               | <span data-ttu-id="95b12-122">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="95b12-122">quartz.dll</span></span>                                                                                                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="95b12-123">Núcleo</span><span class="sxs-lookup"><span data-stu-id="95b12-123">Merit</span></span>](merit.md)                       | <span data-ttu-id="95b12-124">MÉRITO \_ preferido</span><span class="sxs-lookup"><span data-stu-id="95b12-124">MERIT\_PREFERRED</span></span>                                                                                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="95b12-125">Categoria do filtro</span><span class="sxs-lookup"><span data-stu-id="95b12-125">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="95b12-126">\_MIDIRENDERERCATEGORY CLSID</span><span class="sxs-lookup"><span data-stu-id="95b12-126">CLSID\_MidiRendererCategory</span></span>                                                                                                                                                                                                                                                                                                                                                          |



 

## <a name="remarks"></a><span data-ttu-id="95b12-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="95b12-127">Remarks</span></span>

<span data-ttu-id="95b12-128">O GUID para o tipo de formato é **nulo**, mas o bloco de formato contém a seguinte estrutura:</span><span class="sxs-lookup"><span data-stu-id="95b12-128">The GUID for the format type is **NULL**, but the format block contains the following structure:</span></span>


```C++
typedef struct _MIDIFORMAT {
    DWORD       dwDivision;
    DWORD       dwReserved[7];
} MIDIFORMAT, FAR * LPMIDIFORMAT;
```



<span data-ttu-id="95b12-129">O membro **dwDivision** especifica a divisão de tempo do arquivo.</span><span class="sxs-lookup"><span data-stu-id="95b12-129">The **dwDivision** member specifies the time division of the file.</span></span> <span data-ttu-id="95b12-130">A divisão de tempo é fornecida no cabeçalho de qualquer arquivo MIDI padrão (SMF), na `MThd` parte.</span><span class="sxs-lookup"><span data-stu-id="95b12-130">The time division is given in the header of any standard MIDI file (SMF), in the `MThd` chunk.</span></span> <span data-ttu-id="95b12-131">O renderizador MIDI define essa propriedade no fluxo de dados MIDI chamando a função **midiStreamProperty** .</span><span class="sxs-lookup"><span data-stu-id="95b12-131">The MIDI Renderer sets this property on the MIDI data stream by calling the **midiStreamProperty** function.</span></span>

<span data-ttu-id="95b12-132">Exemplos do filtro analisador de MIDI contêm um segundo de dados MIDI.</span><span class="sxs-lookup"><span data-stu-id="95b12-132">Samples from the MIDI Parser filter contain one second of MIDI data.</span></span> <span data-ttu-id="95b12-133">O renderizador MIDI usa a função **midiStreamOut** para renderizar os dados de Midi.</span><span class="sxs-lookup"><span data-stu-id="95b12-133">The MIDI Renderer uses the **midiStreamOut** function to render the MIDI data.</span></span> <span data-ttu-id="95b12-134">Cada exemplo é um ponto de sincronização: o início do buffer contém todos os comandos necessários para definir o estado correto para renderização desse buffer.</span><span class="sxs-lookup"><span data-stu-id="95b12-134">Each sample is a synchronization point: the start of the buffer contains all of the commands necessary to set the correct state for rendering that buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="95b12-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="95b12-135">Requirements</span></span>



| <span data-ttu-id="95b12-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="95b12-136">Requirement</span></span> | <span data-ttu-id="95b12-137">Valor</span><span class="sxs-lookup"><span data-stu-id="95b12-137">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95b12-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="95b12-138">Header</span></span><br/> | <dl> <span data-ttu-id="95b12-139"><dt>Windows. Devices. MIDI. h</dt></span><span class="sxs-lookup"><span data-stu-id="95b12-139"><dt>Windows.devices.midi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95b12-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="95b12-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95b12-141">Filtros do DirectShow</span><span class="sxs-lookup"><span data-stu-id="95b12-141">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 




