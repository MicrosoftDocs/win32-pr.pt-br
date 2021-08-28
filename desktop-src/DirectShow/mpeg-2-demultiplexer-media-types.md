---
description: Tipos de mídia de demultiplexer MPEG-2
ms.assetid: 240d1753-df8c-45fe-b5a7-9faa96fc5b18
title: Tipos de mídia de demultiplexer MPEG-2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bef3c7006f13b07394da7d9dc92e9295beda816c
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122982599"
---
# <a name="mpeg-2-demultiplexer-media-types"></a>Tipos de mídia de demultiplexer MPEG-2

O [filtro Demultiplexer MPEG-2](mpeg-2-demultiplexer.md) reconhece os seguintes tipos de mídia.

### <a name="input-types"></a>Tipos de entrada

O tipo principal é sempre **MEDIATYPE \_ Stream.** O subtipo pode ser qualquer um dos seguintes.



| GUID                                             | Descrição                                                                                                                                                                                               |
|--------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **SUBTIPO KSDATAFORMAT \_ \_ BDA \_ MPEG2 \_ TRANSPORT** | Fluxo de transporte de um filtro de dispositivo BDA (Arquitetura de Driver de Difusão). O demultiplexer MPEG-2 trata esse subtipo de forma idêntica **a MEDIASUBTYPE \_ MPEG2 \_ TRANSPORT.**                                |
| **MEDIASUBTYPE \_ MPEG2 \_ PROGRAM**                 | Fluxo do programa                                                                                                                                                                                            |
| **MEDIASUBTYPE \_ MPEG2 \_ TRANSPORT**               | Fluxo de transporte (TS), com pacotes de 188 byte                                                                                                                                                              |
| **MEDIASUBTYPE \_ MPEG2 \_ TRANSPORT \_ STRIDE**       | Fluxo de transporte com pacotes "estridente". Esse subtipo indica que os pacotes TS podem ser preenchimento com bytes extras. Para obter mais informações, consulte [**MPEG2 \_ TRANSPORT \_ STRIDE**](mpeg2-transport-stride.md). |



 

Para pacotes de transporte estridente (**MEDIASUBTYPE \_ MPEG2 \_ TRANSPORT \_ STRIDE**), cada amostra de mídia deve conter um número integral de pacotes de transporte, conforme descrito em [**MPEG2 \_ TRANSPORT \_ STRIDE**](mpeg2-transport-stride.md). Para todos os outros tipos de entrada, não há restrições em limites de exemplo; pacotes individuais podem abranger limites de exemplo.

### <a name="output-types"></a>Tipos de saída

O Demultiplexer MPEG-2 não valida os tipos de saída; O filtro downstream é responsável por analisar os dados recebidos do demultiplexer. No entanto, os tipos a seguir normalmente são aceitos por filtros downstream como saída do demultiplexer.

### <a name="mpeg-2-sections"></a>Seções MPEG-2




| Rótulo | Valor |
|--------|-------|
| Tipo principal | <strong>MEDIATYPE_MPEG2_SECTIONS</strong> | 
| Subtype | Um dos seguintes:<br /><ul><li><strong>MEDIASUBTYPE_ATSC_SI:</strong>informações do serviço ATSC.</li><li><strong>MEDIASUBTYPE_DVB_SI:</strong>informações do serviço DVB.</li><li><strong>MEDIASUBTYPE_ISDB_SI:</strong>informações de serviço isdb (difusão digital) dos Serviços Integrados.</li><li><strong>MEDIASUBTYPE_MPEG2DATA:</strong>dados da seção MPEG-2.</li></ul> | 
| Tipo de formato | Nenhum | 




 

### <a name="mpeg-2-video"></a>Vídeo do MPEG-2



| Rótulo | Valor |
|------------------|------------------------------------------|
| Tipo principal       | **Vídeo \_ MEDIATYPE**                     |
| Subtype          | **VÍDEO MEDIASUBTYPE \_ MPEG2 \_**           |
| Tipo de formato      | **FORMATO \_ MPEG2Video**                   |
| Estrutura de formato | [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) |



 

### <a name="mpeg-2-audio"></a>Áudio MPEG-2



| Rótulo | Valor |
|------------------|--------------------------------------|
| Tipo principal       | **ÁUDIO \_ MEDIATYPE**                 |
| Subtype          | **ÁUDIO MEDIASUBTYPE \_ MPEG2 \_**       |
| Tipo de formato      | **FORMAT \_ WaveFormatEx**             |
| Estrutura de formato | [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tipos de mídia MPEG-2](mpeg-2-media-types.md)
</dt> </dl>

 

 
