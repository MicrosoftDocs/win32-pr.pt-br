---
description: O filtro Microsoft MPEG-2 Video Encoder codifica o vídeo MPEG-2 e MPEG-1.
ms.assetid: d52c1299-0641-405c-8960-edd738b56823
title: Codificador de vídeo MPEG-2 da Microsoft (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02c96db605586c6abf0f51537689a9365df2842c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105759993"
---
# <a name="microsoft-mpeg-2-video-encoder"></a>Codificador de vídeo MPEG-2 da Microsoft

O filtro Microsoft MPEG-2 Video Encoder codifica o vídeo MPEG-2 e MPEG-1.

Para codificar e multiplexar fluxos de áudio/vídeo, use o filtro de [**codificador MPEG-2 da Microsoft**](microsoft-mpeg-2-encoder.md) , que encapsula as funções desse filtro e do filtro de [**codificador de áudio Microsoft MPEG-2**](microsoft-mpeg-2-audio-encoder.md) .

> [!Note]  
> Não há suporte para esse filtro em plataformas baseadas em IA-64.

 



Informações de filtro

Filtrar interfaces

[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)<br/> [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)<br/> **IEncoderAPI**<br/> [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [**IVideoEncoder**](/windows/win32/api/strmif/nn-strmif-ivideoencoder)<br/>

Tipos de mídia de pino de entrada

**MediaType \_ Vídeo**, **MEDIASUBTYPE \_ I420**<br/> **MediaType \_ Vídeo**, **MEDIASUBTYPE \_ IYUV**<br/> **MediaType \_ Vídeo**, **MEDIASUBTYPE \_ RGB24**<br/> **MediaType \_ Vídeo**, **MEDIASUBTYPE \_ UYVY**<br/> **MediaType \_ Vídeo**, **MEDIASUBTYPE \_ YUY2**<br/> **MediaType \_ Vídeo**, **MEDIASUBTYPE \_ YV12**<br/>

Interfaces de pino de entrada

[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)<br/> [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

Tipos de mídia do pino de saída

**MediaType \_** Vídeo de fluxo, **MEDIASUBTYPE \_ MPEG2 \_**<br/> **MediaType \_ Fluxo**, **\_ \_ programa MEDIASUBTYPE MPEG2**<br/> **MediaType \_ Fluxo**, **\_ \_ transporte MEDIASUBTYPE MPEG2**<br/> **MediaType \_ Vídeo**, **\_ \_ vídeo MEDIASUBTYPE MPEG2**<br/>

Interfaces de pino de saída

[**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

CLSID do filtro

**CLSID \_ do CMPEG2EncoderVideoDS** (declarado em wmcodecdsp. h)

Executável

msmpeg2enc.dll

[Núcleo](merit.md)

**MÉRITO \_ \_ não \_ use**

[Categoria do filtro](filter-categories.md)

**\_LEGACYAMFILTERCATEGORY CLSID**



 

## <a name="remarks"></a>Comentários

O codificador de vídeo MPEG-2 pode produzir os seguintes tipos de saída:

-   Fluxo elementar vídeo
-   Vídeo em um fluxo de programa MPEG-2
-   Vídeo em um fluxo de transporte MPEG-2

Ele dá suporte aos seguintes perfis e níveis MPEG-2:



| Perfil        | Níveis                     | Comentários                                            |
|----------------|----------------------------|----------------------------------------------------|
| Perfil simples | Principal                       |                                                    |
| Perfil Principal   | Baixo, principal, alto, alto-1440 |                                                    |
| Alto Perfil   | Principal, alta, alta-1440      | Sem escalabilidade ou suporte a 4:2:2/4:4:4 (somente 4:2:0) |
| Perfil 4:2:2  | Principal, alta                 | Sem escalabilidade ou suporte a 4:2:2 (somente 4:2:0)       |



 

### <a name="codec-properties"></a>Propriedades do codec

O filtro oferece suporte às seguintes propriedades por meio de [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi).



| Propriedade                                                                                      | Padrão                                                          | Valores com suporte                                                                                                                                                                                                     |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AVEncCodecType**](avenccodectype-property.md)                                             | Vídeo MPEG-2                                                     | **CODECAPI \_ GUID \_ AVEncMPEG1Video**<br/> **CODECAPI \_ GUID \_ AVEncMPEG2Video**<br/>                                                                                                                        |
| [**AVEncCommonBufferInLevel**](avenccommonbufferinlevel-property.md)                         | 12222464 bits                                                    |                                                                                                                                                                                                                      |
| [**AVEncCommonBufferOutLevel**](avenccommonbufferoutlevel-property.md)                       | 12222464 bits                                                    |                                                                                                                                                                                                                      |
| [**AVEncCommonBufferSize**](avenccommonbuffersize-property.md)                               | 12222464 bits                                                    |                                                                                                                                                                                                                      |
| [**AVEncCommonFormatConstraint**](avenccommonformatconstraint-property.md)                   | Não Especificado                                                      | **CODECAPI \_ GUID \_ AVEncCommonFormatUnSpecified** (sem restrição de formato)<br/> **CODECAPI \_ GUID \_ AVEncCommonFormatDVD \_ V** (DVD-Video)<br/> **CODECAPI \_ GUID \_ AVEncCommonFormatVCD** (CD de vídeo)<br/> |
| [**AVEncCommonMaxBitRate**](avenccommonmaxbitrate-property.md)                               | 9,8 milhões (9,8 Mbits/segundo)                                       |                                                                                                                                                                                                                      |
| [**AVEncCommonMeanBitRate**](avenccommonmeanbitrate-property.md)                             | 7 milhões (7,0 Mbits/segundo)                                       |                                                                                                                                                                                                                      |
| [**AVEncCommonMinBitRate**](avenccommonminbitrate-property.md)                               | 128                                                              |                                                                                                                                                                                                                      |
| [**AVEncCommonMultipassMode**](avenccommonmultipassmode-property.md)                         | 1                                                                | 1                                                                                                                                                                                                                    |
| [**AVEncCommonQuality**](avenccommonquality-property.md)                                     | 100                                                              | 1 – 100                                                                                                                                                                                                              |
| [**AVEncCommonQualityVsSpeed**](avenccommonqualityvsspeed-property.md)                       | 75                                                               | 0 — 100                                                                                                                                                                                                              |
| [**AVEncCommonRateControlMode**](avenccommonratecontrolmode-property.md)                     | CBR                                                              | **eAVEncCommonRateControlMode \_ CBR**<br/> **eAVEncCommonRateControlMode \_ PeakConstrainedVBR**<br/> **qualidade de eAVEncCommonRateControlMode \_**<br/>                                                   |
| [**AVEncInputVideoSystem**](avencinputvideosystem-property.md)                               | Não Especificado                                                      | eAVEncInputVideoSystem \_ não especificado<br/> \_PAL eAVEncInputVideoSystem<br/> \_NTSC eAVEncInputVideoSystem<br/>                                                                                        |
| [**AVEncMPVDefaultBPictureCount**](avencmpvdefaultbpicturecount-property.md)                 | 2                                                                | 0 – 2                                                                                                                                                                                                                |
| [**AVEncMPVFrameFieldMode**](avencmpvframefieldmode-property.md)                             | Modo de quadro                                                       |                                                                                                                                                                                                                      |
| [**AVEncMPVGenerateHeaderSeqDispExt**](avencmpvgenerateheaderseqdispext-property.md)         | **TRUE**                                                         |                                                                                                                                                                                                                      |
| [**AVEncMPVGenerateHeaderSeqExt**](avencmpvgenerateheaderseqext-property.md)                 | **TRUE**                                                         |                                                                                                                                                                                                                      |
| [**AVEncMPVGOPOpen**](avencmpvgopopen-property.md)                                           | **FALSE**                                                        |                                                                                                                                                                                                                      |
| [**AVEncMPVGOPSInSeq**](avencmpvgopsinseq-property.md)                                       | 1                                                                | 0 – 1                                                                                                                                                                                                                |
| [**AVEncMPVGOPSize**](avencmpvgopsize-property.md)                                           | 18 quadros (36 campos) para NTSC; 15 quadros (30 campos) caso contrário. | 1 – 30; Ver comentários                                                                                                                                                                                                  |
| [**AVEncMPVIntraDCPrecision**](avencmpvintradcprecision-property.md)                         | 9                                                                | 8 – 10                                                                                                                                                                                                               |
| [**AVEncMPVLevel**](avencmpvlevel-property.md)                                               | Alto                                                             |                                                                                                                                                                                                                      |
| [**AVEncMPVProfile**](avencmpvprofile-property.md)                                           | Principal                                                             |                                                                                                                                                                                                                      |
| [**AVEncVideoDefaultUpperFieldDominant**](avencvideodefaultupperfielddominant-property.md)   | **TRUE**                                                         |                                                                                                                                                                                                                      |
| [**AVEncVideoForceSourceScanType**](avencvideoforcesourcescantype-property.md)               | Interlaced                                                       | **eAVEncVideoSourceScan \_ entrelaçado**<br/> **eAVEncVideoSourceScan \_ progressivo**<br/>                                                                                                                   |
| [**AVEncVideoInputChromaResolution**](avencvideoinputchromaresolution-property.md)           | 4:2:0                                                            | **eAVEncVideoChromaResolution \_ 420** (4:2:0)<br/> **eAVEncVideoChromaResolution \_ SameAsSource**<br/>                                                                                                     |
| [**AVEncVideoInputChromaSubsampling**](avencvideoinputchromasubsampling-property.md)         | Igual à origem                                                   |                                                                                                                                                                                                                      |
| [**AVEncVideoInputColorNominalRange**](avencvideoinputcolornominalrange-property.md)         | Igual à origem                                                   |                                                                                                                                                                                                                      |
| [**AVEncVideoInputColorPrimaries**](avencvideoinputcolorprimaries-property.md)               | Igual à origem                                                   |                                                                                                                                                                                                                      |
| [**AVEncVideoInputColorTransferFunction**](avencvideoinputcolortransferfunction-property.md) | Igual à origem                                                   |                                                                                                                                                                                                                      |
| [**AVEncVideoInputColorTransferMatrix**](avencvideoinputcolortransfermatrix-property.md)     | Igual à origem                                                   |                                                                                                                                                                                                                      |
| [**AVEncVideoMaxKeyframeDistance**](avencvideomaxkeyframedistance-property.md)               | [**AVEncMPVGOPSize**](avencmpvgopsize-property.md) -1          | 0 ou [**AVEncMPVGOPSize**](avencmpvgopsize-property.md) -1                                                                                                                                                         |
| [**AVEncVideoNoOfFieldsToEncode**](avencvideonooffieldstoencode-property.md)                 | 0                                                                |                                                                                                                                                                                                                      |
| [**AVEncVideoOutputChromaResolution**](avencvideooutputchromaresolution-property.md)         | 4:2:0                                                            | **eAVEncVideoChromaResolution \_ 420** (4:2:0)<br/> **eAVEncVideoChromaResolution \_ SameAsSource**<br/>                                                                                                     |
| [**AVEncVideoOutputFrameRate**](avencvideooutputframerate-property.md)                       |                                                                  | Deve ser igual à taxa de quadros de entrada.                                                                                                                                                                            |
| [**AVEncVideoOutputScanType**](avencvideooutputscantype-property.md)                         | Igual à entrada                                                    | **eAVEncVideoOutputScan \_ SameAsInput**                                                                                                                                                                               |
| [**AVEncVideoPixelAspectRatio**](avencvideopixelaspectratio-property.md)                     | 1:1                                                              |                                                                                                                                                                                                                      |



 

É recomendável definir as propriedades na seguinte ordem:

1.  [**AVEncCommonFormatConstraint**](avenccommonformatconstraint-property.md)
2.  [**AVEncCodecType**](avenccodectype-property.md)
3.  [**AVEncMPVProfile**](avencmpvprofile-property.md)
4.  [**AVEncMPVLevel**](avencmpvlevel-property.md)
5.  [**AVEncInputVideoSystem**](avencinputvideosystem-property.md)

Defina as propriedades restantes em qualquer ordem. (No entanto, consulte [estrutura GOP](#gop-structure).)

É possível definir propriedades enquanto o grafo de filtro está em execução. Há um atraso de pelo menos um GOP antes que as novas configurações entrem em vigor.

### <a name="encoder-operation"></a>Operação do codificador

Ao codificar vídeo MPEG-1, o codificador define automaticamente o código de **\_ \_ sinalizador de parâmetros restritos** de 1 bit no cabeçalho de sequência, caso todas as restrições sejam atendidas.

Se necessário, o codificador arredonda as dimensões de vídeo de entrada para que as dimensões de vídeo de saída correspondam aos requisitos MPEG. Para o vídeo progressivo, as dimensões de saída são arredondadas para um múltiplo de 16 em largura e altura. Para vídeo entrelaçado, a largura é arredondada para um múltiplo de 16 e a altura é arredondada para um múltiplo de 32. Essa operação de arredondamento usa o preenchimento conforme necessário.

Se o vídeo estiver entrelaçado, o codificador executará a detecção de telecineon (pull-down 3:2) automática. O vídeo de entrada pode conter pares de imagens de campo, além de quadros entrelaçados.

O formato interno do codificador é 4:2:0 IYUV (idêntico a I420). Ele pode executar a conversão de cores dos formatos de vídeo YUY2, YV12, UYVY e RGB-24.

Para restringir o fragmentado a um formato de destino (DVD ou VCD), defina a propriedade [**AVEncCommonFormatConstraint**](avenccommonformatconstraint-property.md) . Se essa propriedade tiver um valor diferente de **GUID \_ AVEncCommonFormatUnSpecified**, o codificador limitará a sintaxe MPEG ao que é permitido pelo formato de destino.

Para a codificação ativa, defina a propriedade [**AVEncCommonQualityVsSpeed**](avenccommonqualityvsspeed-property.md) como zero. Isso faz com que o codificador Otimize a velocidade.

### <a name="encoding-modes"></a>Modos de codificação

O codificador dá suporte a vários modos de codificação:

-   Taxa de bits constante de passagem única (CBR).
-   Taxa de bits variável baseada em qualidade de passagem (VBR), usando um tamanho de etapa quantizador constante. Nesse modo, o codificador tenta atender a um nível de qualidade de destino, até uma taxa de bits máxima.
-   TAXA de bits de pico restrita de um passo. Nesse modo, o codificador tenta atingir uma taxa de bits média de destino dentro de determinados limites internos.

Para configurar o modo de codificação, defina as seguintes propriedades:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Mode</th>
<th>Propriedades</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>CBR</td>
<td><a href="avenccommonratecontrolmode-property.md"><strong>AVEncCommonRateControlMode</strong></a>  =  <strong>eAVEncCommonRateControlMode_CBR</strong><br/> <a href="avenccommonqualityvsspeed-property.md"><strong>AVEncCommonQualityVsSpeed</strong></a><br/> <a href="avenccommonmeanbitrate-property.md"><strong>AVEncCommonMeanBitRate</strong></a><br/></td>
</tr>
<tr class="even">
<td>Taxa de bits baseada em qualidade</td>
<td><a href="avenccommonratecontrolmode-property.md"><strong>AVEncCommonRateControlMode</strong></a>  =  <strong>eAVEncCommonRateControlMode_Quality</strong><br/> <a href="avenccommonquality-property.md"><strong>AVEncCommonQuality</strong></a><br/> <a href="avenccommonmaxbitrate-property.md"><strong>AVEncCommonMaxBitRate</strong></a><br/>
<blockquote>
[!Note]<br />
Nesse modo, as propriedades <a href="avenccommonmeanbitrate-property.md"><strong>AVEncCommonMeanBitRate</strong></a> e <a href="avenccommonminbitrate-property.md"><strong>AVEncCommonMinBitRate</strong></a> não são usadas. A taxa de bits mínima é considerada como zero.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>TAXA de bits restrita de pico</td>
<td><a href="avenccommonratecontrolmode-property.md"><strong>AVEncCommonRateControlMode</strong></a>  =  <strong>eAVEncCommonRateControlMode_PeakConstrainedVBR</strong><br/> <a href="avenccommonmultipassmode-property.md"><strong>AVEncCommonMultipassMode</strong></a> = 1<br/> <a href="avenccommonminbitrate-property.md"><strong>AVEncCommonMinBitRate</strong></a><br/> <a href="avenccommonmaxbitrate-property.md"><strong>AVEncCommonMaxBitRate</strong></a><br/> <a href="avenccommonmeanbitrate-property.md"><strong>AVEncCommonMeanBitRate</strong></a><br/></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> Não há suporte para VBR de duas passagens.

 

### <a name="aspect-ratio"></a>Taxa de proporção

A taxa de proporção de exibição e a taxa de proporção de pixel (PAR) estão relacionadas pela seguinte fórmula:

<dl> Exibir taxa de proporção = PAR × (largura da imagem/altura da imagem)  
</dl>

O codificador usa essa fórmula para calcular o valor da taxa de proporção do PEL \_ \_ para MPEG-1 fragmentado ou \_ \_ informações de taxa de proporção para fragmentado MPEG-2. (Consulte ISO/IEC 11172 e ISO/IEC 138181-2, respectivamente.)

O codificador tenta as seguintes configurações, na ordem:

1.  Se o aplicativo definir a propriedade [**AVEncVideoPixelAspectRatio**](avencvideopixelaspectratio-property.md) a qualquer momento antes de o grafo de filtro ser executado, essa propriedade será usada para o par.
2.  Caso contrário, se os membros **dwPictAspectRatioX** e **DwPictAspectRatioY** da estrutura [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) forem diferentes de zero, esses membros serão usados para a taxa de proporção de exibição e o par será calculado a partir da taxa de proporção de exibição.
3.  Se nenhum desses valores estiver presente, o PAR será considerado 1,0 e a taxa de proporção de exibição será calculada de acordo.

No modo de codificação dinâmica ([**AVEncCommonQualityVsSpeed**](avenccommonqualityvsspeed-property.md) igual a zero), a taxa de proporção de exibição deve ser 4:3 ou 16:9, com um valor padrão de 4:3. Se a taxa de proporção de exibição computada não for 4:3 ou 16:9, o codificador usará o valor 4:3.

### <a name="gop-structure"></a>Estrutura GOP

Para especificar a estrutura do grupo de imagens (GOP), defina as seguintes propriedades na ordem:

1.  [**AVEncMPVGOPSize**](avencmpvgopsize-property.md)
2.  [**AVEncVideoMaxKeyframeDistance**](avencvideomaxkeyframedistance-property.md)
3.  [**AVEncMPVDefaultBPictureCount**](avencmpvdefaultbpicturecount-property.md)

Com base nessas configurações, o codificador produz uma das seguintes estruturas GOP:



| [**AVEncVideoMaxKeyframeDistance**](avencvideomaxkeyframedistance-property.md) | [**AVEncMPVDefaultBPictureCount**](avencmpvdefaultbpicturecount-property.md) | Estrutura GOP |
|---------------------------------------------------------------------------------|-------------------------------------------------------------------------------|---------------|
| 0                                                                               | 0                                                                             | IIII...       |
| [**AVEncMPVGOPSize**](avencmpvgopsize-property.md) -1                         | 0                                                                             | IPPP...       |
| [**AVEncMPVGOPSize**](avencmpvgopsize-property.md) -1                         | 1                                                                             | IBPBP...      |
| [**AVEncMPVGOPSize**](avencmpvgopsize-property.md) -1                         | 2                                                                             | IBBPBBP...    |



 

A estrutura GOP padrão é IBBPBBP... com um tamanho de GOP de 15 quadros.

Se o aplicativo restringir o formato de destino ao DVD (por meio da propriedade [**AVEncCommonFormatConstraint**](avenccommonformatconstraint-property.md) ) e definir a propriedade [**AVEncInputVideoSystem**](avencinputvideosystem-property.md) como NTSC ou PAL, o codificador dará suporte aos seguintes tamanhos de GOP:



| Sistema de vídeo | Tamanhos de GOP válidos | Tamanho de GOP padrão |
|--------------|-----------------|------------------|
| NTSC         | 1-18            | 18 (campos 36)   |
| PAL          | 1-15            | 15 (30 campos)   |



 

### <a name="codec-property-change-lists"></a>Lista de alterações de Propriedade do codec

Definir o valor de uma propriedade de codec pode alterar o intervalo válido de outra propriedade. (Por exemplo, restringir o formato de destino restringe a taxa média de bits.) Sempre que o aplicativo definir uma propriedade, o codificador verificará se outras propriedades agora estão fora do intervalo válido. Nesse caso, o codificador redefine essa propriedade para o novo valor padrão. Para receber notificações quando isso ocorrer, faça o seguinte:

1.  Chame [**ICodecAPI:: RegisterForEvent**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-registerforevent) com o valor **CODECAPI \_ CHANGELISTS**.
2.  Use a interface [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) para monitorar eventos do grafo de filtro.
3.  Se o intervalo ou valor padrão de uma propriedade for alterado, o codificador enviará um evento de [**\_ \_ evento do EC CODECAPI**](ec-codecapi-event.md) com uma lista de propriedades alteradas.

### <a name="iencoderapi-support"></a>Suporte do IEncoderAPI

Para compatibilidade com versões anteriores, o filtro oferece suporte às seguintes propriedades por meio da interface **IEncoderAPI** :



| Propriedade                       | Descrição                                                                              |
|--------------------------------|------------------------------------------------------------------------------------------|
| **\_taxa de bits ENCAPIPARAM**       | Equivalente a [**AVEncCommonMeanBitRate**](avenccommonmeanbitrate-property.md).         |
| **taxa de bits de \_ pico ENCAPIPARAM \_** | Equivalente a [**AVEncCommonMaxBitRate**](avenccommonmaxbitrate-property.md).           |
| **\_modo de taxa de bits ENCAPIPARAM \_** | Equivalente a [**AVEncCommonRateControlMode**](avenccommonratecontrolmode-property.md). |



 

Ao definir a propriedade do **\_ \_ modo de taxa de bits ENCAPIPARAM** , os valores são mapeados da seguinte maneira:



| **\_modo de taxa de bits ENCAPIPARAM \_** | [**AVEncCommonRateControlMode**](avenccommonratecontrolmode-property.md) |
|--------------------------------|---------------------------------------------------------------------------|
| **ConstantBitRate**            | **eAVEncCommonRateControlMode \_ CBR**                                      |
| **VariableBitRateAverage**     | Consulte a observação.                                                                 |
| **VariableBitRatePeak**        | **eAVEncCommonRateControlMode \_ PeakConstrainedVBR**                       |



 

> [!Note]  
> Atualmente, o codificador de vídeo MPEG-2 não oferece suporte ao modo de codificação **VariableBitRateAverage** . Se você definir esse valor, o codificador usa como padrão a codificação de CBR (**eAVEncCommonRateControlMode \_ CBR**).

 

Ao obter a propriedade do **\_ \_ modo de taxa de bits ENCAPIPARAM** , os valores são mapeados da seguinte maneira:



| [**AVEncCommonRateControlMode**](avenccommonratecontrolmode-property.md) | **\_modo de taxa de bits ENCAPIPARAM \_** |
|---------------------------------------------------------------------------|--------------------------------|
| **eAVEncCommonRateControlMode \_ CBR**                                      | **ConstantBitRate**            |
| **qualidade de eAVEncCommonRateControlMode \_**                                  | **VariableBitRatePeak**        |
| **eAVEncCommonRateControlMode \_ PeakConstrainedVBR**                       | **VariableBitRatePeak**        |



 

### <a name="limitations"></a>Limitações

Atualmente, o codificador não oferece suporte a nenhum dos seguintes recursos:

-   Geração de pacotes de pacote de fluxo elementar (PES).
-   Conversão de taxa de quadros. O fluxo de entrada deve ter uma taxa de quadros válida para um fragmentado MPEG-2.
-   Extensões de taxa de quadros para MPEG-2 **( \_ extensão de taxa de quadros \_ \_ n**, **extensão de taxa de quadros \_ \_ \_ d**).
-   Posições do buffer de entrada/saída (VBV) para um clipe.
-   Inserção de dados de linha-21 (informações de legenda oculta) no fluxo elementar vídeo.
-   Configurando o campo **de \_ código de tempo** de 25 bits no cabeçalho GOP para MPEG-2.
-   Filtro de clareza.
-   DRM (gerenciamento de direitos digitais).

O codificador apresenta uma latência de codificação de pelo menos um GOP.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista Home Premium, Windows Vista Ultimate, Windows 7 Home Premium, Windows 7 Professional, Windows 7 Enterprise, Windows 7 Ultimate \[ Desktop apps\]<br/> |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                                                                                     |
| parâmetro<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl>                                                                                       |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Filtros do DirectShow](directshow-filters.md)
</dt> <dt>

[**Tipos de mídia de Desmultiplexador MPEG-2**](mpeg-2-demultiplexer-media-types.md)
</dt> </dl>

 

 
