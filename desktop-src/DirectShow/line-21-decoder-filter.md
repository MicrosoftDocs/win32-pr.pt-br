---
description: Filtro de decodificador de linha 21
ms.assetid: 48fa5484-1f8c-4133-b2e1-888cb1834402
title: Filtro de decodificador de linha 21
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b0668d4b71b8dcccf4ceacf7f5428fa7a65ad52
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122468233"
---
# <a name="line-21-decoder-filter"></a>Filtro de decodificador de linha 21

Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

Esse filtro de decodificador de Linha 21 decodifica dados da linha 21 e desenha o texto de legenda em bitmaps.

O pino de entrada se conecta a qualquer provedor de dados de linha 21, normalmente um decodificador de vídeo de DVD ou o filtro [do decodificador](cc-decoder-filter.md) CC. O Decodificador cc fornece dados de linha 21 da VBI de um sinal de tv análogo. O pino de saída conecta-se a um pin secundário no Mixer [sobreposição](overlay-mixer-filter.md) ou a outro renderador de vídeo, como a VMR.

Esse filtro aceita dados de linha 21 no formato de par de byte padrão ou, para DVD, como um pacote para todo o grupo de imagens (GOP). Para cada GOP no fluxo de vídeo de DVD, pode haver um pacote de dados do usuário que tenha as informações de header e os dados de linha 21 do GOP específicos. O formato dos pares de byte é definido no padrão EIA/CEA-608-B; consulte esse padrão para obter mais informações.

Duas versões desse filtro estão disponíveis:



| Filtrar            | CLSID                 |
|-------------------|-----------------------|
| Decodificador de Linha 21   | CLSID \_ Line21Decoder  |
| Decodificador de linha 21 | CLSID \_ Line21Decoder2 |



 

O filtro da versão 1 é usado nas plataformas Microsoft® Windows® 95/98/Me e Windows 2000. O filtro da versão 2 está disponível no Microsoft Windows XP e posterior e é usado sempre que o Renderização de Combinação de Vídeo está no grafo.

As informações na tabela a seguir se aplica a ambas as versões do filtro:




| | | Interfaces de filtro | <a href="/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder"><strong>IAMLine21Decoder,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter | |</strong></a> Tipos de mídia de pino de entrada | Tipo principal: MEDIATYPE_AUXLine21DataSubtype:<br /><ul><li>MEDIASUBTYPE_Line21_BytePair (linha padrão 21)</li><li>MEDIASUBTYPE_Line21_GOPPacket (linha de DVD 21)</li></ul>Tipo de formato: FORMAT_VideoInfo ou GUID_NULL<br /> | | Interfaces de pino de entrada | <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | | Tipos de mídia de pino de | Tipo principal: MEDIATYPE_VideoSubtype:<br /><ul><li>MEDIASUBTYPE_RGB8</li><li>MEDIASUBTYPE_RGB555</li><li>MEDIASUBTYPE_RGB565</li><li>MEDIASUBTYPE_RGB24</li><li>MEDIASUBTYPE_RGB32</li></ul>Tipo de formato: FORMAT_VideoInfo<br /> | | Interfaces de pino de | <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | | Filtrar CLSID | Consulte a tabela | | ClSID da página de propriedades | Nenhum | | Arquivo executável | qdvd.dll | | <a href="merit.md">|</a> Decodificador de linha 21: MERIT_NORMALLine 21 Decodificador 2: MERIT_NORMAL + 2<br /> | | <a href="filter-categories.md">Categoria de</a> filtro | CLSID_LegacyAmFilterCategory | 




 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[DirectShow Filtros](directshow-filters.md)
</dt> <dt>

[Legendas fechadas e teletexto](closed-captions-and-teletext.md)
</dt> <dt>

[Configuração de filtro Graph DVD](dvd-filter-graph-configuration.md)
</dt> </dl>

 

 




