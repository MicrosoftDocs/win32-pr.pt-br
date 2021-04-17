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
ms.openlocfilehash: 060bb00629b78fb1edbfbfd193aeaf7514c98ba4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761834"
---
# <a name="midi-renderer-filter"></a><span data-ttu-id="f0305-103">Filtro de renderizador MIDI</span><span class="sxs-lookup"><span data-stu-id="f0305-103">MIDI Renderer Filter</span></span>

<span data-ttu-id="f0305-104">O filtro de renderizador MIDI renderiza dados MIDI do filtro [analisador de Midi](midi-parser-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="f0305-104">The MIDI Renderer filter renders MIDI data from the [MIDI Parser](midi-parser-filter.md) filter.</span></span>



|                                          |                                                                                                                                                                                                                                                                                                                                                                                      |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0305-105">Filtrar interfaces</span><span class="sxs-lookup"><span data-stu-id="f0305-105">Filter Interfaces</span></span>                        | <span data-ttu-id="f0305-106">[**IAMClockSlave**](/windows/desktop/api/Strmif/nn-strmif-iamclockslave), [**IAMDirectSound**](/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound), [**IAMResourceControl**](/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IBasicAudio**](/windows/desktop/api/Control/nn-control-ibasicaudio), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol), [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock)</span><span class="sxs-lookup"><span data-stu-id="f0305-106">[**IAMClockSlave**](/windows/desktop/api/Strmif/nn-strmif-iamclockslave), [**IAMDirectSound**](/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound), [**IAMResourceControl**](/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IBasicAudio**](/windows/desktop/api/Control/nn-control-ibasicaudio), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol), [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock)</span></span> |
| <span data-ttu-id="f0305-107">Tipos de mídia de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="f0305-107">Input Pin Media Types</span></span>                    | <span data-ttu-id="f0305-108">\_MEDIASUBTYPE de mídia MIDI, \_ nulo</span><span class="sxs-lookup"><span data-stu-id="f0305-108">MEDIATYPE\_Midi, MEDIASUBTYPE\_NULL</span></span>                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="f0305-109">Interfaces de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="f0305-109">Input Pin Interfaces</span></span>                     | <span data-ttu-id="f0305-110">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="f0305-110">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="f0305-111">Tipos de mídia do pino de saída</span><span class="sxs-lookup"><span data-stu-id="f0305-111">Output Pin Media Types</span></span>                   | <span data-ttu-id="f0305-112">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="f0305-112">Not applicable</span></span>                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="f0305-113">Interfaces de pino de saída</span><span class="sxs-lookup"><span data-stu-id="f0305-113">Output Pin Interfaces</span></span>                    | <span data-ttu-id="f0305-114">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="f0305-114">Not applicable</span></span>                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="f0305-115">CLSID do filtro</span><span class="sxs-lookup"><span data-stu-id="f0305-115">Filter CLSID</span></span>                             | <span data-ttu-id="f0305-116">\_AVIMIDIRENDER CLSID</span><span class="sxs-lookup"><span data-stu-id="f0305-116">CLSID\_AVIMIDIRender</span></span>                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="f0305-117">CLSID de página de propriedades</span><span class="sxs-lookup"><span data-stu-id="f0305-117">Property Page CLSID</span></span>                      | <span data-ttu-id="f0305-118">Nenhuma página de propriedades</span><span class="sxs-lookup"><span data-stu-id="f0305-118">No property page</span></span>                                                                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="f0305-119">Executável</span><span class="sxs-lookup"><span data-stu-id="f0305-119">Executable</span></span>                               | <span data-ttu-id="f0305-120">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="f0305-120">quartz.dll</span></span>                                                                                                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="f0305-121">Núcleo</span><span class="sxs-lookup"><span data-stu-id="f0305-121">Merit</span></span>](merit.md)                       | <span data-ttu-id="f0305-122">MÉRITO \_ preferido</span><span class="sxs-lookup"><span data-stu-id="f0305-122">MERIT\_PREFERRED</span></span>                                                                                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="f0305-123">Categoria do filtro</span><span class="sxs-lookup"><span data-stu-id="f0305-123">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="f0305-124">\_MIDIRENDERERCATEGORY CLSID</span><span class="sxs-lookup"><span data-stu-id="f0305-124">CLSID\_MidiRendererCategory</span></span>                                                                                                                                                                                                                                                                                                                                                          |



 

## <a name="remarks"></a><span data-ttu-id="f0305-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="f0305-125">Remarks</span></span>

<span data-ttu-id="f0305-126">O GUID para o tipo de formato é **nulo**, mas o bloco de formato contém a seguinte estrutura:</span><span class="sxs-lookup"><span data-stu-id="f0305-126">The GUID for the format type is **NULL**, but the format block contains the following structure:</span></span>


```C++
typedef struct _MIDIFORMAT {
    DWORD       dwDivision;
    DWORD       dwReserved[7];
} MIDIFORMAT, FAR * LPMIDIFORMAT;
```



<span data-ttu-id="f0305-127">O membro **dwDivision** especifica a divisão de tempo do arquivo.</span><span class="sxs-lookup"><span data-stu-id="f0305-127">The **dwDivision** member specifies the time division of the file.</span></span> <span data-ttu-id="f0305-128">A divisão de tempo é fornecida no cabeçalho de qualquer arquivo MIDI padrão (SMF), na `MThd` parte.</span><span class="sxs-lookup"><span data-stu-id="f0305-128">The time division is given in the header of any standard MIDI file (SMF), in the `MThd` chunk.</span></span> <span data-ttu-id="f0305-129">O renderizador MIDI define essa propriedade no fluxo de dados MIDI chamando a função **midiStreamProperty** .</span><span class="sxs-lookup"><span data-stu-id="f0305-129">The MIDI Renderer sets this property on the MIDI data stream by calling the **midiStreamProperty** function.</span></span>

<span data-ttu-id="f0305-130">Exemplos do filtro analisador de MIDI contêm um segundo de dados MIDI.</span><span class="sxs-lookup"><span data-stu-id="f0305-130">Samples from the MIDI Parser filter contain one second of MIDI data.</span></span> <span data-ttu-id="f0305-131">O renderizador MIDI usa a função **midiStreamOut** para renderizar os dados de Midi.</span><span class="sxs-lookup"><span data-stu-id="f0305-131">The MIDI Renderer uses the **midiStreamOut** function to render the MIDI data.</span></span> <span data-ttu-id="f0305-132">Cada exemplo é um ponto de sincronização: o início do buffer contém todos os comandos necessários para definir o estado correto para renderização desse buffer.</span><span class="sxs-lookup"><span data-stu-id="f0305-132">Each sample is a synchronization point: the start of the buffer contains all of the commands necessary to set the correct state for rendering that buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0305-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f0305-133">Requirements</span></span>



| <span data-ttu-id="f0305-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0305-134">Requirement</span></span> | <span data-ttu-id="f0305-135">Valor</span><span class="sxs-lookup"><span data-stu-id="f0305-135">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0305-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f0305-136">Header</span></span><br/> | <dl> <span data-ttu-id="f0305-137"><dt>Windows. Devices. MIDI. h</dt></span><span class="sxs-lookup"><span data-stu-id="f0305-137"><dt>Windows.devices.midi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0305-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="f0305-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0305-139">Filtros do DirectShow</span><span class="sxs-lookup"><span data-stu-id="f0305-139">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 




