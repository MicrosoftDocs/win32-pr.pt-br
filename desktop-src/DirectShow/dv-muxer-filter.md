---
description: Filtro DV Muxer
ms.assetid: 4dd57202-f4de-40d9-b720-efaba8a60a7c
title: Filtro DV Muxer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6ad8189d7430a150c6860ef9e390a0e66aabd00971b56197ffe8651cde8967b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120102966"
---
# <a name="dv-muxer-filter"></a>Filtro DV Muxer

Esse filtro combina um vídeo digital (DV) – fluxo de vídeo codificado com um ou dois fluxos de áudio para produzir um fluxo de DV intercalado. Para gravar o fluxo em um arquivo AVI, conecte esse filtro ao filtro [AVI Mux](avi-mux-filter.md) e conecte o *multiplexador AVI* ao filtro do [gravador de arquivo](file-writer-filter.md) . Para obter mais informações, consulte [digital video in DirectShow](digital-video-in-directshow.md).



| Rótulo | Valor |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| Filtrar interfaces                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [ **IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)                                                             |
| Tipos de mídia de pino de entrada                    | **Vídeo**: \_ vídeo de MediaType, MEDIASUBTYPE \_ Dvsd, Format \_ VIDEOINFO **Audio**: MediaType \_ áudio, MEDIASUBTYPE \_ PCM, Format \_ WaveFormatEx |
| Interfaces de pino de entrada                     | [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                 |
| Tipos de mídia do pino de saída                   | MEDIATYPE \_ intercalado, MEDIASUBTYPE \_ DVSD, formato \_ DvInfo                                                                             |
| Interfaces de pino de saída                    | [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [ **IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                       |
| CLSID do filtro                             | \_DVMUX CLSID                                                                                                                           |
| CLSID de página de propriedades                      | Nenhuma página de propriedades                                                                                                                       |
| Executável                               | qdv.dll                                                                                                                                |
| [Núcleo](merit.md)                       | MÉRITO \_ improvável                                                                                                                        |
| [Categoria do filtro](filter-categories.md) | \_LEGACYAMFILTERCATEGORY CLSID                                                                                                          |



 

## <a name="remarks"></a>Comentários

O DV Muxer pode criar dois pinos de entrada de áudio. Ele dá suporte aos formatos de áudio mostrados na tabela a seguir.



PIN de áudio 1

PIN de áudio 2

Formato de Saída

Taxa de amostra (kHz)

Bits/exemplo

Canais

Taxa de amostragem

Bits/exemplo

Canais

32

16

Mono

Desconectado

Canal SD 2

32

16

Estéreo

Desconectado

Canal SD 4

44,1 ou 48

16

Estéreo ou mono

Desconectado

Canal SD 2

Desconectado

32

16

Estéreo ou mono

Não permitido

Desconectado

44,1 ou 48

16

Mono

Não permitido

Desconectado

44,1 ou 48

16

Estéreo

Canal SD 2

32

16

Mono

32

16

Mono

Canal SD 2

32

16

Estéreo ou mono\*

32

16

Estéreo ou mono\*

Canal SD 4

44,1

16

Mono

44,1

16

Mono

Canal SD 2

48

16

Mono

48

16

Mono

Canal SD 2

\* Se pelo menos um PIN de entrada for estéreo.



 

Para a finalidade desta tabela, o PIN 1 de áudio é definido como o primeiro pino de entrada conectado a uma fonte de áudio, e o PIN de áudio 2 é definido como o segundo PIN de entrada conectado a uma fonte de áudio. Depois que um pino de áudio é conectado, esse esquema de numeração permanece em vigor, a menos que ambos os pinos de áudio sejam desconectados. Por exemplo, se você conectar os dois pinos de áudio e, em seguida, desconectar o pino de áudio 1, o pino restante ainda será considerado o pino 2.

O áudio fornecido para fixar 1 é gravado no primeiro bloco de áudio dos quadros DV (CH1) e o áudio fornecido para o pino 2 é gravado no segundo bloco de áudio (CH2). Exceção: se o filtro tiver uma única entrada estéreo a 44,1 kHz ou 48 kHz, o canal de áudio esquerdo será gravado no primeiro bloco de áudio e o canal de áudio direito será gravado no segundo bloco de áudio.

Para saída de 4 canais SD: se a entrada for estéreo, a faixa esquerda será registrada em CHa ou CHc e a faixa direita será registrada em CHb ou CHd. Se a entrada for mono, o áudio será gravado em CHa ou CHc e CHb e CHd serão silenciosos.

Ao conectar e desconectar o pino de áudio 1, é possível alcançar um formato não permitido. Nesse caso, o método [**IMediaFilter::P ause**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause) do filtro retorna VFW \_ E NOT \_ \_ CONNECTED. Essa limitação impede uma situação em que o primeiro bloco de áudio não tem áudio, mas o segundo bloco de áudio tem áudio. O segundo bloco deverá ter áudio somente se o primeiro bloco também tiver áudio.

O DV Muxer não permite entradas de áudio com taxas de amostragem diferentes. No entanto, métodos de criação de grafo como [**IGraphBuilder::Conexão**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) normalmente adicionarão o filtro Wrapper do [ACM,](acm-wrapper-filter.md) que converterá o segundo fluxo de áudio para corresponder à taxa de amostragem do primeiro fluxo.

Se a entrada de áudio for de 48 kHz ou 32 kHz, a saída de áudio será bloqueada. (Não é possível bloquear o áudio de 44,1 kHz.)

Se nenhum pino de áudio estiver conectado, a saída conterá os dados de áudio dos quadros DV de entrada. Isso pode ser silêncio ou dados de áudio válidos.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[DirectShow Filtros](directshow-filters.md)
</dt> <dt>

[Vídeo digital no DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 



