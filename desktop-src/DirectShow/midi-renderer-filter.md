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
# <a name="midi-renderer-filter"></a>Filtro de renderizador MIDI

O filtro de renderizador MIDI renderiza dados MIDI do filtro [analisador de Midi](midi-parser-filter.md) .



| Label | Valor |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Filtrar interfaces                        | [**IAMClockSlave**](/windows/desktop/api/Strmif/nn-strmif-iamclockslave), [**IAMDirectSound**](/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound), [**IAMResourceControl**](/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IBasicAudio**](/windows/desktop/api/Control/nn-control-ibasicaudio), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol), [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) |
| Tipos de mídia de pino de entrada                    | \_MEDIASUBTYPE de mídia MIDI, \_ nulo                                                                                                                                                                                                                                                                                                                                                  |
| Interfaces de pino de entrada                     | [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                                                                                                                                                                                                                               |
| Tipos de mídia do pino de saída                   | Não aplicável                                                                                                                                                                                                                                                                                                                                                                       |
| Interfaces de pino de saída                    | Não aplicável                                                                                                                                                                                                                                                                                                                                                                       |
| CLSID do filtro                             | \_AVIMIDIRENDER CLSID                                                                                                                                                                                                                                                                                                                                                                 |
| CLSID de página de propriedades                      | Nenhuma página de propriedades                                                                                                                                                                                                                                                                                                                                                                     |
| Executável                               | quartz.dll                                                                                                                                                                                                                                                                                                                                                                           |
| [Núcleo](merit.md)                       | MÉRITO \_ preferido                                                                                                                                                                                                                                                                                                                                                                     |
| [Categoria do filtro](filter-categories.md) | \_MIDIRENDERERCATEGORY CLSID                                                                                                                                                                                                                                                                                                                                                          |



 

## <a name="remarks"></a>Comentários

O GUID para o tipo de formato é **nulo**, mas o bloco de formato contém a seguinte estrutura:


```C++
typedef struct _MIDIFORMAT {
    DWORD       dwDivision;
    DWORD       dwReserved[7];
} MIDIFORMAT, FAR * LPMIDIFORMAT;
```



O membro **dwDivision** especifica a divisão de tempo do arquivo. A divisão de tempo é fornecida no cabeçalho de qualquer arquivo MIDI padrão (SMF), na `MThd` parte. O renderizador MIDI define essa propriedade no fluxo de dados MIDI chamando a função **midiStreamProperty** .

Exemplos do filtro analisador de MIDI contêm um segundo de dados MIDI. O renderizador MIDI usa a função **midiStreamOut** para renderizar os dados de Midi. Cada exemplo é um ponto de sincronização: o início do buffer contém todos os comandos necessários para definir o estado correto para renderização desse buffer.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Windows. Devices. MIDI. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Filtros do DirectShow](directshow-filters.md)
</dt> </dl>

 

 




