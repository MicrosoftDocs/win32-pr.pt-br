---
description: Tipos de mídia de divisor MPEG-2
ms.assetid: d0ff2011-4ee3-4f5e-8bd0-af9f4c6346e8
title: Tipos de mídia de divisor MPEG-2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef4e025fafabdeb8c437cc1d1cd6fbb843cf63e3
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119971"
---
# <a name="mpeg-2-splitter-media-types"></a>Tipos de mídia de divisor MPEG-2

O [filtro divisor MPEG-2](mpeg-2-splitter.md) atualmente dá suporte a áudio e vídeo. Há suporte para Dolby AC-3 como um substream conforme definido pelo DVD. O filtro também dá suporte ao áudio MPEG-2. Os tipos de mídia dependem se o divisor MPEG-2 está fornecendo pacotes PES ou cargas PES.

### <a name="video"></a>Vídeo

Para o vídeo MPEG-2, os tipos de mídia são os a seguir.


|                | Saída do PES | Saída de payload
|------------------|------------------------------------------|--------------------------------|
| **Tipo principal**       | **MEDIATYPE \_ MPEG2 \_ PES**                | **Vídeo \_ MEDIATYPE**           |
| **Subtipo**          | **VÍDEO MEDIASUBTYPE \_ MPEG2 \_**           | **VÍDEO MEDIASUBTYPE \_ MPEG2 \_** |
| **Tipo de formato**      | **FORMATO \_ MPEG2Video**                   | **FORMATO \_ MPEG2Video**         |
| **Estrutura de formato** | [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) | **MPEG2VIDEOINFO**             |



 

### <a name="ac-3-audio"></a>Áudio AC-3

Para áudio AC-3, os tipos de mídia são os a seguir.

| | Saída do PES | Saída de payload |
|------------------|--------------------------------------|------------------------------|
| **Tipo principal**       | **MEDIATYPE \_ MPEG2 \_ PES**                | **ÁUDIO \_ MEDIATYPE**         |
| **Subtipo**          | **MEDIASUBTYPE \_ DOLBY \_ AC3**             | **MEDIASUBTYPE \_ DOLBY \_ AC3** |
| **Tipo de formato**      | FORMAT \_ WaveFormatEx                 | **FORMAT \_ WaveFormatEx**     |
| **Estrutura de formato** | [**Waveformatex**](/previous-versions/dd757713(v=vs.85)) | **Waveformatex**             |



 

O membro **wFormatTag** da estrutura **WAVEFORMATEX** para AC-3 atualmente é **WAVE FORMAT \_ \_ UNKNOWN,** mas isso pode mudar.

### <a name="mpeg-2-audio"></a>Áudio MPEG-2

Para áudio MPEG-2, os tipos de mídia são os a seguir.



|  | Saída do PES | Saída de payload |
|------------------|-------------------------------|--------------------------------|
| **Tipo principal**       | **MEDIATYPE \_ MPEG2 \_ PES**     | **ÁUDIO \_ MEDIATYPE**           |
| **Subtipo**          | **MEDIASUBTYE \_ MPEG2 \_ AUDIO** | **ÁUDIO MEDIASUBTYPE \_ MPEG2 \_** |
| **Tipo de formato**      | **FORMAT \_ WaveFormatEx**      | **FORMAT \_ WaveFormatEx**       |
| **Estrutura de formato** | **Waveformatex**              | **Waveformatex**               |



 

O membro **wFormatTag** da estrutura **WAVEFORMATEX** para ÁUDIO MPEG-2 atualmente é **WAVE FORMAT \_ \_ UNKNOWN,** mas isso pode mudar.

O Divisor MPEG-2 presume que os fluxos D0 a DF são usados para o fluxo de extensão multicanal, como são para áudio MPEG-2 de DVD. Portanto, sempre que o fluxo C *x* é selecionado, o divisor encaminha os pacotes para o fluxo D *x* também.

### <a name="lpcm-audio"></a>Áudio LPCM

Para áudio LPCM, os tipos de mídia são os a seguir.



|  | Saída do PES | Saída de payload |
|------------------|------------------------------------|------------------------------------|
| **Tipo principal**       | **MEDIATYPE \_ MPEG2 \_ PES**          | **ÁUDIO \_ MEDIATYPE**               |
| **Subtipo**          | **ÁUDIO \_ LPCM DE DVD MEDIASUBTYPE \_ \_** | **ÁUDIO \_ LPCM DE DVD MEDIASUBTYPE \_ \_** |
| **Tipo de formato**      | **FORMAT \_ WaveFormatEx**           | **FORMAT \_ WaveFormatEx**           |
| **Estrutura de formato** | **Waveformatex**                   | **Waveformatex**                   |



 

O membro **wFormatTag** da estrutura **WAVEFORMATEX** para áudio LPCM atualmente é **WAVE FORMAT \_ \_ UNKNOWN,** mas isso pode mudar.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tipos de mídia MPEG-2](mpeg-2-media-types.md)
</dt> </dl>

 

 
