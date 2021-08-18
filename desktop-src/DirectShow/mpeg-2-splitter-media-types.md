---
description: Tipos de mídia de divisor MPEG-2
ms.assetid: d0ff2011-4ee3-4f5e-8bd0-af9f4c6346e8
title: Tipos de mídia de divisor MPEG-2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b29151e5128531cbd2e71c6eda0f2b4b16658c8e68577de0fbb0542189c2931f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119748576"
---
# <a name="mpeg-2-splitter-media-types"></a>Tipos de mídia de divisor MPEG-2

O filtro [divisor MPEG-2](mpeg-2-splitter.md) atualmente dá suporte a áudio e vídeo. O Dolby AC-3 tem suporte como um subfluxo, conforme definido pelo DVD. O filtro também dá suporte a áudio MPEG-2. Os tipos de mídia dependem se o divisor MPEG-2 está entregando pacotes PES ou cargas PES.

### <a name="video"></a>Vídeo

Para vídeo MPEG-2, os tipos de mídia são os seguintes.


|                | Saída de PES | Saída da carga
|------------------|------------------------------------------|--------------------------------|
| **Tipo principal**       | **MEDIATYPE \_ MPEG2 \_ PES**                | **Vídeo de MEDIATYPE \_**           |
| **Subtipo**          | **Vídeo do MEDIASUBTYPE \_ MPEG2 \_**           | **Vídeo do MEDIASUBTYPE \_ MPEG2 \_** |
| **Tipo de formato**      | **MPEG2Video de formato \_**                   | **MPEG2Video de formato \_**         |
| **Estrutura de formato** | [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) | **MPEG2VIDEOINFO**             |



 

### <a name="ac-3-audio"></a>Áudio AC-3

Para áudio AC-3, os tipos de mídia são os seguintes.

| | Saída de PES | Saída da carga |
|------------------|--------------------------------------|------------------------------|
| **Tipo principal**       | **MEDIATYPE \_ MPEG2 \_ PES**                | **Áudio de MEDIATYPE \_**         |
| **Subtipo**          | **MEDIASUBTYPE \_ Dolby \_ AC3**             | **MEDIASUBTYPE \_ Dolby \_ AC3** |
| **Tipo de formato**      | WaveFormatEx de formato \_                 | **WaveFormatEx de formato \_**     |
| **Estrutura de formato** | [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) | **WAVEFORMATEX**             |



 

O membro **wFormatTag** da estrutura **WAVEFORMATEX** para AC-3 atualmente é **um \_ formato Wave \_ desconhecido**, mas isso pode ser alterado.

### <a name="mpeg-2-audio"></a>Áudio MPEG-2

Para áudio MPEG-2, os tipos de mídia são os seguintes.



|  | Saída de PES | Saída da carga |
|------------------|-------------------------------|--------------------------------|
| **Tipo principal**       | **MEDIATYPE \_ MPEG2 \_ PES**     | **Áudio de MEDIATYPE \_**           |
| **Subtipo**          | **\_Áudio MEDIASUBTYE MPEG2 \_** | **\_Áudio MEDIASUBTYPE MPEG2 \_** |
| **Tipo de formato**      | **WaveFormatEx de formato \_**      | **WaveFormatEx de formato \_**       |
| **Estrutura de formato** | **WAVEFORMATEX**              | **WAVEFORMATEX**               |



 

O membro **wFormatTag** da estrutura **WAVEFORMATEX** para áudio MPEG-2 está no **\_ formato Wave \_ desconhecido** no momento, mas isso pode ser alterado.

O divisor MPEG-2 pressupõe que fluxos D0 por meio de DF são usados para o fluxo de extensão multicanal, como são para áudio MPEG-2 de DVD. Portanto, sempre que o fluxo C *x* é selecionado, o divisor encaminha os pacotes para o fluxo D *x* também.

### <a name="lpcm-audio"></a>Áudio LPCM

Para áudio LPCM, os tipos de mídia são os seguintes.



|  | Saída de PES | Saída da carga |
|------------------|------------------------------------|------------------------------------|
| **Tipo principal**       | **MEDIATYPE \_ MPEG2 \_ PES**          | **Áudio de MEDIATYPE \_**               |
| **Subtipo**          | **\_áudio MEDIASUBTYPE DVD \_ LPCM \_** | **\_áudio MEDIASUBTYPE DVD \_ LPCM \_** |
| **Tipo de formato**      | **WaveFormatEx de formato \_**           | **WaveFormatEx de formato \_**           |
| **Estrutura de formato** | **WAVEFORMATEX**                   | **WAVEFORMATEX**                   |



 

Atualmente, o membro **wFormatTag** da estrutura **WAVEFORMATEX** para áudio LPCM **é \_ \_ desconhecido no formato Wave**, mas isso pode ser alterado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tipos de mídia MPEG-2](mpeg-2-media-types.md)
</dt> </dl>

 

 
