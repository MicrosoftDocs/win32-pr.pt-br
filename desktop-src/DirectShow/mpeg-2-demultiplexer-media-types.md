---
description: Tipos de mídia de Desmultiplexador MPEG-2
ms.assetid: 240d1753-df8c-45fe-b5a7-9faa96fc5b18
title: Tipos de mídia de Desmultiplexador MPEG-2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b21eecff138b987c791ecd97056fb4cf417dd98d
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105761754"
---
# <a name="mpeg-2-demultiplexer-media-types"></a>Tipos de mídia de Desmultiplexador MPEG-2

O filtro de [Desmultiplexador MPEG-2](mpeg-2-demultiplexer.md) reconhece os seguintes tipos de mídia.

### <a name="input-types"></a>Tipos de entrada

O tipo principal é sempre **\_ fluxo de MediaType**. O subtipo pode ser qualquer um dos seguintes.



| GUID                                             | Descrição                                                                                                                                                                                               |
|--------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_Transporte do KSDATAFORMAT \_ \_ MPEG2 BDA do subtipo \_** | Fluxo de transporte de um filtro de dispositivo da arquitetura de driver de difusão (BDA). O demultiplexador MPEG-2 trata esse subtipo de forma idêntica **ao \_ \_ transporte MEDIASUBTYPE MPEG2**.                                |
| **\_Programa MEDIASUBTYPE MPEG2 \_**                 | Fluxo do programa                                                                                                                                                                                            |
| **\_Transporte MEDIASUBTYPE MPEG2 \_**               | Fluxo de transporte (TS), com pacotes de 188 bytes                                                                                                                                                              |
| **\_Stride de \_ transporte MEDIASUBTYPE MPEG2 \_**       | Fluxo de transporte com pacotes "enrided". Esse subtipo indica que os pacotes TS podem ser preenchidos com bytes extras. Para obter mais informações, consulte [**MPEG2 \_ Transport \_ Stride**](mpeg2-transport-stride.md). |



 

Para pacotes de transporte (STRIDE de **\_ transporte MEDIASUBTYPE \_ MPEG2 \_**), cada amostra de mídia deve conter um número integral de pacotes de transporte, conforme descrito no [**\_ \_ Stride de transporte MPEG2**](mpeg2-transport-stride.md). Para todos os outros tipos de entrada, não há restrições sobre os limites de amostra; pacotes individuais podem abranger limites de amostra.

### <a name="output-types"></a>Tipos de saída

O demultiplexador MPEG-2 não valida tipos de saída; o filtro downstream é responsável por analisar os dados que recebe do demultiplexador. No entanto, os seguintes tipos são normalmente aceitos por filtros downstream como saída do demultiplexador.

### <a name="mpeg-2-sections"></a>Seções MPEG-2



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Tipo principal</td>
<td><strong>MEDIATYPE_MPEG2_SECTIONS</strong></td>
</tr>
<tr class="even">
<td>Subtype</td>
<td>Um dos seguintes:<br/>
<ul>
<li><strong>MEDIASUBTYPE_ATSC_SI</strong>: informações do serviço ATSC.</li>
<li><strong>MEDIASUBTYPE_DVB_SI</strong>: informações de serviço DVB.</li>
<li><strong>MEDIASUBTYPE_ISDB_SI</strong>: informações de serviço de difusão digital de serviços integrados (ISDB).</li>
<li><strong>MEDIASUBTYPE_MPEG2DATA</strong>: dados da seção MPEG-2.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Tipo de formato</td>
<td>Nenhum</td>
</tr>
</tbody>
</table>



 

### <a name="mpeg-2-video"></a>Vídeo MPEG-2



|                  |                                          |
|------------------|------------------------------------------|
| Tipo principal       | **Vídeo de MEDIATYPE \_**                     |
| Subtype          | **Vídeo do MEDIASUBTYPE \_ MPEG2 \_**           |
| Tipo de formato      | **MPEG2Video de formato \_**                   |
| Estrutura de formato | [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) |



 

### <a name="mpeg-2-audio"></a>Áudio MPEG-2



|                  |                                      |
|------------------|--------------------------------------|
| Tipo principal       | **Áudio de MEDIATYPE \_**                 |
| Subtype          | **\_Áudio MEDIASUBTYPE MPEG2 \_**       |
| Tipo de formato      | **WaveFormatEx de formato \_**             |
| Estrutura de formato | [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tipos de mídia MPEG-2](mpeg-2-media-types.md)
</dt> </dl>

 

 
