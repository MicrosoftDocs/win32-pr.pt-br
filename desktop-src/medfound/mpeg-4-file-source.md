---
description: A fonte de arquivo MPEG-4 analisará arquivos MP4 e 3GPP.
ms.assetid: e64c1554-9702-4cc0-98ad-8a33e04ed09d
title: Origem do arquivo MPEG-4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ece07ec0f2a2d94b477335e885f11c0d36769bffd11002ba464cec1d9c6ffb21
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119848046"
---
# <a name="mpeg-4-file-source"></a>Origem do arquivo MPEG-4

A fonte de arquivo MPEG-4 analisará arquivos MP4 e 3GPP. Para obter mais informações sobre o formato de arquivo MP4, consulte os seguintes documentos padrão:

-   ISO/IEC 14496-12: Tecnologia da informação – Codificação de objetos *audiovisual – Parte 12: Formato* de arquivo de mídia base ISO
-   ISO/IEC 14496-14: Tecnologia da informação – Codificação de objetos *audiovisual – Parte 14: Formato de arquivo MP4*

> [!Note]  
> (Esses recursos podem não estar disponíveis em alguns idiomas e países.)

 

A origem do arquivo MPEG-4 não decodifica os dados de áudio/vídeo no arquivo.

Este tópico contém as seguintes seções:

## <a name="file-extensions-and-mime-types"></a>Extensões de arquivo e tipos MIME

A origem do arquivo MPEG-4 é a fonte de mídia padrão para as seguintes extensões de nome de arquivo.



| Extensão de arquivo | Descrição           |
|----------------|-----------------------|
| .3g2           | 3GPP2                 |
| .3gp           | 3GPP                  |
| .3gp2          | 3GPP2                 |
| .3gpp          | 3GPP                  |
| .m4a           | Áudio MPEG-4          |
| .m4v           | Vídeo do MPEG-4          |
| .mov           | Filme de QuickTime da Apple |
| .mp4           | Áudio ou vídeo MPEG-4 |
| .mp4v          | Vídeo do MPEG-4          |



 

Também é a fonte de mídia padrão para os seguintes tipos MIME.



| tipo MIME   | Descrição  |
|-------------|--------------|
| audio/3gpp  | Áudio 3GPP   |
| audio/3gpp2 | Áudio 3GPP2  |
| audio/mp4   | Áudio MPEG-4 |
| video/3gpp  | Vídeo do 3GPP   |
| video/3gpp2 | Vídeo do 3GPP2  |
| vídeo/mp4   | Vídeo do MPEG-4 |



 

## <a name="media-types"></a>Tipos de mídia

MP4 é um formato de contêiner extensível. A especificação MP4 não define uma estrutura fixa para descrever tipos de mídia em um contêiner MP4. Em vez disso, ele define uma hierarquia de objetos que permite que estruturas personalizadas sejam definidas para cada formato. A descrição do formato é armazenada na caixa de descrição de exemplo ('stsd') desse fluxo. A caixa de descrição de exemplo contém uma lista de entradas de exemplo. Para cada entrada de exemplo, um código de 4 byte, semelhante a um FOURCC, define a estrutura de formato.

Essa extensibilidade significa que a origem do arquivo MPEG-4 não pode reconhecer todas as descrições de formato possíveis. Em vez disso, ele assume uma abordagem de duas camadas ao criar tipos de mídia para os fluxos. No mínimo, cada tipo de mídia contém os atributos a seguir.



| Atributo                                                                     | Descrição                                                    |
|-------------------------------------------------------------------------------|----------------------------------------------------------------|
| [**MF \_ MT \_ MAJOR \_ TYPE**](mf-mt-major-type-attribute.md)                     | Igual a **Áudio MFMediaType \_ ou** **Vídeo MFMediaType \_**.     |
| [**SUBTIPO \_ MF MT \_**](mf-mt-subtype-attribute.md)                            | Especifica o subtipo de fluxo.                                  |
| [MF \_ MT \_ MPEG4 \_ SAMPLE \_ DESCRIPTION](mf-mt-mpeg4-sample-description.md)      | Contém a caixa de descrição de exemplo completa como um blob binário. |
| [ENTRADA DE \_ EXEMPLO ATUAL DO MF MT \_ MPEG4 \_ \_ \_](mf-mt-mpeg4-current-sample-entry.md) | Especifica a entrada atual na caixa de descrição de exemplo.     |



 

A fonte de arquivo MPEG-4 reconhece alguns tipos de entrada de exemplo. Para essas entradas, ele pode analisar a estrutura de formato e criar um tipo de mídia completo, com atributos adicionais que descrevem os detalhes do formato. Consulte [Atributos de tipo de mídia](media-type-attributes.md).

A origem do arquivo MPEG-4 pode analisar as entradas de exemplo a seguir.



| Código de entrada de exemplo | Tipo principal | Subtype                                                               | Descrição                                         | Observações                                                                                                                                                                                            |
|-------------------|------------|-----------------------------------------------------------------------|-----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 'alaw'            | Áudio      | **WAVE \_ FORMAT \_ ALAW**                                                | Codificação de lei A                                        |                                                                                                                                                                                                  |
| 'jpeg'            | Vídeo      | **MFVideoFormat \_ MJPG**                                               | Fluxo Photo-JPEG                                   | O formato de contêiner quickTime também dá suporte a fluxos JPEG de movimento com entradas 'mjpa' ou 'mjpb', mas a fonte de arquivo MPEG-4 não fornece um tipo de mídia completo para esses tipos.               |
| 'avc1'            | Vídeo      | **MFVideoFormat \_ H264**                                               | Vídeo H.264                                         |                                                                                                                                                                                                  |
| 'mp4a'            | Áudio      | **MFAudioFormat \_ AAC**<br/> **MFAudioFormat \_ MP3**<br/>   | AAC ou MP3                                          | A entrada 'mp4a' pode descrever outros formatos de áudio MPEG, mas a fonte de arquivo MPEG-4 não analisará a estrutura de formato.                                                                          |
| 'mp4v'            | Vídeo      | **MFVideoFormat \_ M4S2**<br/> **MFVideoFormat \_ MP4V**<br/> | MPEG-4 parte 2                                       | **MFVideoFormat \_ M4S2** é usado para o perfil simples MPEG-4 parte 2.<br/> **MFVideoFormat \_ MP4V** é usado para todos os outros perfis MPEG-4 parte 2, incluindo o perfil simples avançado.<br/> |
| recebem            | Áudio      | **\_PCM MFAudioFormat**                                                | áudio PCM de 8 bits                                     |                                                                                                                                                                                                  |
| 'sowt'            | Áudio      | **\_PCM MFAudioFormat**                                                | áudio PCM de little-endian de 16 bits                      |                                                                                                                                                                                                  |
| dois Complementos            | Áudio      | **\_PCM MFAudioFormat**                                                | áudio PCM de big-endian de 16 bits                         | A origem do arquivo MPEG-4 converte os dados de áudio para o formato little-endian.                                                                                                                          |
| 'ulaw'            | Áudio      | **\_MULAW de formato Wave \_**                                               | codificação de μ-Law                                        |                                                                                                                                                                                                  |
| ' VC-1 '            | Vídeo      | **MFVideoFormat \_ WVC1**                                               | Vídeo VC-1                                          |                                                                                                                                                                                                  |
| None            | Áudio      | **\_PCM MFAudioFormat**                                                | áudio PCM de 8 ou 16 bits de big endian                | A origem do arquivo MPEG-4 converte os dados de áudio para o formato little-endian.                                                                                                                          |
| 0x00000000        | Áudio      | **\_PCM MFAudioFormat**                                                | áudio PCM de 8 ou 16 bits de big endian                | A origem do arquivo MPEG-4 converte os dados de áudio para o formato little-endian.                                                                                                                          |
| 0x6d730002        | Áudio      | **\_formato Wave \_ ADPCM**                                               | Modulação de código de pulso diferencial adaptável (ADPCM) |                                                                                                                                                                                                  |
| 0x6d730011        | Áudio      | **\_formato Wave \_ IMA \_ ADPCM**                                          | ADPCM                                               |                                                                                                                                                                                                  |



 

Para quaisquer outros códigos não mostrados na tabela anterior, a fonte de arquivo MPEG-4 define o subtipo da seguinte maneira:

1.  *subtipo* = \_ base MFMPEG4Format
2.  *subtipo*. Dados1 = código de entrada de exemplo

Para códigos não mostrados na tabela, um decodificador deve usar o atributo de [ \_ Descrição de exemplo MF MT \_ MPEG4 \_ \_ ](mf-mt-mpeg4-sample-description.md) para analisar a caixa de descrição de exemplo.

Para obter uma lista de códigos de entrada de exemplo e links para especificações relevantes, consulte o site da [autoridade de registro ' MP4 '](https://mp4ra.org) .

## <a name="limitations"></a>Limitações

A origem do arquivo MPEG-4 não oferece suporte aos seguintes recursos de arquivos MP4:

-   Faixas externas.
-   Fragmentos de filme (caixas ' Moof ' ou ' mfra '). ' Moof ' tem suporte em Windows 8.
-   Apresentações transmitidas. A fonte de arquivo MPEG-4 ignora silenciosamente as faixas de dicas.
-   Procurando por código de tempo SMPTE.
-   Átomos compactados (' CMOV ').

Há suporte apenas para fluxos de áudio e vídeo. Todas as faixas que contêm outros tipos de fluxo são silenciosamente ignoradas. Os dados de mídia devem ser colocados dentro de átomos ' mdat '.

se o suplemento de atualização de plataforma para o Windows Vista estiver instalado, a fonte de arquivo MPEG-4 estará disponível no Windows vista, mas poderá ser acessada no Windows vista somente usando o [leitor de origem](source-reader.md).

## <a name="windows-8-updates-to-mpeg-4-source-and-sink"></a>Windows 8 atualizações para a origem e o coletor MPEG-4

-   suporte de leitura e gravação de rotação adicionado em Windows 8 fonte e coletor MPEG-4. não há suporte para isso na origem e no coletor do Windows 7 MPEG-4.

    A origem MPEG-4 lê o ângulo de rotação de uma faixa de vídeo ativa como a soma do ângulo de rotação de ' mvhd ' e de ' tkhd '.

    O coletor MPEG-4 da Microsoft grava o ângulo de rotação em ' tkhd ', mas grava a matriz de 0 grau (identidade) em ' mvhd '. Observe que o coletor MPEG-4 da Microsoft oferece suporte apenas a faixa de vídeo único.

    IPropertyStore lê o ângulo de rotação somente para a primeira faixa de vídeo que a soma do ângulo de rotação de ' mvhd ' e de ' tkhd '.

    IPropertyStore grava o ângulo de rotação somente para a primeira faixa de vídeo em ' tkhd ' depois que o ângulo de rotação é ajustado de acordo com o ângulo de rotação em ' mvhd ', se existir.

-   os fragmentos de filme (' moof ') têm suporte na origem e no coletor Windows 8 MPEG-4, mas ' mfra ' não.
-   H. 263 tem suporte na fonte Windows 8 MPEG-4.

    A origem MPEG-4 agora mapeia dois FOURCC de ' H263 ' e de 263 ' no formato de arquivo MPEG-4 para o tipo de mídia de **MFVideoFormat \_ H263**.

-   suporte mais fourcc adicionado para MJPEG em Windows 8 fonte MPEG-4.

    A origem MPEG-4 mapeia foucc de ' dmb1 ' para o tipo de mídia de **\_ MJPG MFVideoFormat**.

-   suporte a metadados Furigana adicionado na fonte Windows 8 MPEG-4.

    A origem MPEG-4 lê metadados Furigana de ' soal ', ' disparar ', ' Soaa ', ' sonm ' e ' soco '. IPropertyStore lê os metadados do Furignana por meio do conjunto de PKEYs correspondentes.

    A tabela a seguir mostra o mapeamento entre o nome canônico do Shell, a chave de propriedade e a ID da caixa/marca no formato de arquivo MPEG-4.

    

    | Campo                                | Chave de propriedade                         | ID da marca/caixa |
    |--------------------------------------|--------------------------------------|------------|
    | System. Music. AlbumTitleSortOverride  | PKEY \_ Music \_ AlbumTitleSortOverride  | soal       |
    | System. Music. ArtistSortOverride      | PKEY \_ Music \_ ArtistSortOverride      | disparar       |
    | System. Music. AlbumArtistSortOverride | PKEY \_ Music \_ AlbumArtistSortOverride | soaa       |
    | System. TitleSortOverride             | PKEY \_ TitleSortOverride             | sonm       |
    | System. Music. ComposerSortOverride    | PKEY \_ Music \_ ComposerSortOverride    | soco       |

    

     

-   o suporte ao atom 3d estéreo foi adicionado em Windows 8 fonte MPEG-4.

-   AC3 e DD + suporte adicionado em Windows 8 fonte e coletor MPEG-4.
-   arquivos com mais de 4 gigabytes (GB) têm suporte no coletor de Windows 8 MPEG-4 para MP4 não fragmentado.
-   a depuração foi otimizada na fonte Windows 8 MPEG-4.

    Para reduzir a latência, as informações para os dois quadros-chave mais próximos para uma determinada posição de busca são expostas por meio de [**IMFSeekInfo:: GetNearestKeyFrames**](/windows/desktop/api/mfidl/nf-mfidl-imfseekinfo-getnearestkeyframes). Como o quadro-chave não tem quadros dependentes, ele apresenta o quadro depois da decodificação de apenas um quadro. Use [**IMFGetService::GetService para**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) obter essa interface por meio da fonte de mídia, pipeline ou aplicativo.

    Definir a taxa como zero na origem MPEG-4. Quando o pipeline está no modo de depuração, a taxa é zero.

-   SPS e PPS podem ser armazenados em dados de exemplo no sink MPEG-4.

    [MF \_ O atributo MPEG4SINK \_ SPSPPS \_ PASSTHROUGH](mf-mpeg4sink-spspps-passthrough.md) no sink MPEG-4 é definido para permitir que OS SPS e PPS sejam salvos junto com exemplos de entrada (dados de vídeo H.264). Os clipes mp4 produzidos são reproduzidores por Windows 7 MPEG-4 e outros.

-   SPS e PPS podem ser extraídos de exemplos de entrada no sink MPEG-4.

    Quando SPS e PPS não são definidos por meio do [ \_ \_ \_ \_ HEADER MT MPEG SEQUENCE](mf-mt-mpeg-sequence-header-attribute.md) do MF no tipo de mídia de entrada do sink MPEG-4, o sink MPEG-4 tentará extrair SPS e PPS de exemplos de entrada. O sink MPEG-4 ignora todas as amostras de entrada até encontrar o primeiro SPS e PPS, porque todas as amostras de entrada sem SPS e PPS não são decodificadas.

-   Há suporte para informações 3D no registro de configuração do AVC para MP4 não fragmentado.
-   O comprimento da NALU é exposto para amostras compactadas H.264 para otimizar a decodificação de DXVA do VLD H.264.

    MPEG-4 define [MF \_ NALU \_ LENGTH SET \_ no](mf-nalu-length-set.md) tipo de mídia de saída **MFVideoFormat \_ H264** ou **MFVideoFormat \_ h264**. Ele define o blob de INFORMAÇÕES DE COMPRIMENTO [ \_ NALU \_ \_ ](mf-nalu-length-information.md) de MF em cada amostra de saída, com comprimento NALU de quatro byte para diferentes NALUs em uma amostra compactada.

-   Suporte adicionado para áudio MPEG2 ADTS na fonte MP4.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Fontes de mídia e sinks](media-sources-and-sinks.md)
</dt> <dt>

[Suporte a MPEG-4 no Media Foundation](mpeg-4-support-in-media-foundation.md)
</dt> <dt>

[Formatos de mídia compatíveis com o Media Foundation](supported-media-formats-in-media-foundation.md)
</dt> </dl>

 

 




