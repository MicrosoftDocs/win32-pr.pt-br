---
description: A fonte de arquivo MPEG-4 analisa arquivos MP4 e 3GPP.
ms.assetid: e64c1554-9702-4cc0-98ad-8a33e04ed09d
title: Fonte de arquivo MPEG-4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c90df56d58df19a53c37436bd631a1cc68dd8114
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164909"
---
# <a name="mpeg-4-file-source"></a>Fonte de arquivo MPEG-4

A fonte de arquivo MPEG-4 analisa arquivos MP4 e 3GPP. Para obter mais informações sobre o formato de arquivo MP4, consulte os seguintes documentos de padrões:

-   ISO/IEC 14496-12: *tecnologia da informação – codificação de objetos de áudio-visual--parte 12: formato de arquivo de mídia base ISO*
-   ISO/IEC 14496-14: *tecnologia da informação – codificação de objetos de áudio-visual--parte 14: formato de arquivo MP4*

> [!Note]  
> (Esses recursos podem não estar disponíveis em alguns idiomas e países.)

 

A origem do arquivo MPEG-4 não decodifica os dados de áudio/vídeo no arquivo.

Este tópico contém as seguintes seções:

## <a name="file-extensions-and-mime-types"></a>Extensões de arquivo e tipos MIME

A origem do arquivo MPEG-4 é a origem de mídia padrão para as seguintes extensões de nome de arquivo.



| Extensão de arquivo | Descrição           |
|----------------|-----------------------|
| .3g2           | 3GPP2                 |
| .3gp           | 3GPP                  |
| .3gp2          | 3GPP2                 |
| .3gpp          | 3GPP                  |
| .m4a           | Áudio MPEG-4          |
| .m4v           | Vídeo MPEG-4          |
| .mov           | Filme do Apple QuickTime |
| .mp4           | Áudio ou vídeo MPEG-4 |
| .mp4v          | Vídeo MPEG-4          |



 

Também é a fonte de mídia padrão para os tipos MIME a seguir.



| tipo MIME   | Descrição  |
|-------------|--------------|
| áudio/3GPP  | áudio 3GPP   |
| áudio/3GPP2 | áudio 3GPP2  |
| áudio/MP4   | Áudio MPEG-4 |
| vídeo/3GPP  | vídeo do 3GPP   |
| vídeo/3GPP2 | vídeo do 3GPP2  |
| vídeo/MP4   | Vídeo MPEG-4 |



 

## <a name="media-types"></a>Tipos de mídia

MP4 é um formato de contêiner extensível. A especificação MP4 não define uma estrutura fixa para descrever os tipos de mídia em um contêiner MP4. Em vez disso, ele define uma hierarquia de objetos que permite que as estruturas personalizadas sejam definidas para cada formato. A descrição do formato é armazenada na caixa Descrição de exemplo (' stsd ') para esse fluxo. A caixa Descrição de exemplo contém uma lista de entradas de exemplo. Para cada entrada de exemplo, um código de 4 bytes, semelhante a um FOURCC, define a estrutura de formato.

Essa extensibilidade significa que a origem do arquivo MPEG-4 não pode reconhecer todas as descrições de formato possíveis. Em vez disso, ele usa uma abordagem de duas camadas ao criar tipos de mídia para os fluxos. No mínimo, cada tipo de mídia contém os atributos a seguir.



| Atributo                                                                     | Descrição                                                    |
|-------------------------------------------------------------------------------|----------------------------------------------------------------|
| [**\_ \_ tipo principal MF \_ MT**](mf-mt-major-type-attribute.md)                     | Igual a **MFMediaType \_ áudio** ou **MFMediaType \_ vídeo**.     |
| [**subtipo MF \_ MT \_**](mf-mt-subtype-attribute.md)                            | Especifica o subtipo de fluxo.                                  |
| [\_Descrição de \_ exemplo de MPEG4 \_ \_ do MF MT](mf-mt-mpeg4-sample-description.md)      | Contém a caixa de descrição de exemplo completo como um blob binário. |
| [\_Entrada de \_ \_ exemplo atual \_ \_ do MF MT MPEG4](mf-mt-mpeg4-current-sample-entry.md) | Especifica a entrada atual na caixa Descrição de exemplo.     |



 

A origem do arquivo MPEG-4 reconhece alguns tipos de entrada de exemplo. Para essas entradas, ele pode analisar a estrutura de formato e criar um tipo de mídia completo, com atributos adicionais que descrevem os detalhes do formato. Consulte [atributos de tipo de mídia](media-type-attributes.md).

A origem do arquivo MPEG-4 pode analisar as entradas de exemplo a seguir.



| Código de entrada de exemplo | Tipo principal | Subtype                                                               | Descrição                                         | Observações                                                                                                                                                                                            |
|-------------------|------------|-----------------------------------------------------------------------|-----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 'alaw'            | Áudio      | **\_ALAW de formato Wave \_**                                                | Codificação a-Law                                        |                                                                                                                                                                                                  |
| JPEG            | Vídeo      | **MFVideoFormat \_ MJPG**                                               | Foto-streaming de JPEG                                   | O formato de contêiner do QuickTime também dá suporte a fluxos JPEG de movimento com entradas ' mjpa ' ou ' mjpb ', mas a origem do arquivo MPEG-4 não fornece um tipo de mídia completo para esses tipos.               |
| 'avc1'            | Vídeo      | **MFVideoFormat \_ H264**                                               | Vídeo H. 264                                         |                                                                                                                                                                                                  |
| 'mp4a'            | Áudio      | **\_AAC MFAudioFormat**<br/> **MFAudioFormat \_ mp3**<br/>   | AAC ou MP3                                          | A entrada ' mp4a ' pode descrever outros formatos de áudio MPEG, mas a origem do arquivo MPEG-4 não analisa a estrutura de formato.                                                                          |
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
-   Fragmentos de filme (caixas ' Moof ' ou ' mfra '). ' Moof ' tem suporte no Windows 8.
-   Apresentações transmitidas. A fonte de arquivo MPEG-4 ignora silenciosamente as faixas de dicas.
-   Procurando por código de tempo SMPTE.
-   Átomos compactados (' CMOV ').

Há suporte apenas para fluxos de áudio e vídeo. Todas as faixas que contêm outros tipos de fluxo são silenciosamente ignoradas. Os dados de mídia devem ser colocados dentro de átomos ' mdat '.

Se o suplemento de atualização de plataforma para Windows Vista estiver instalado, a fonte de arquivo MPEG-4 estará disponível no Windows Vista, mas poderá ser acessada somente no Windows Vista usando o [leitor de origem](source-reader.md).

## <a name="windows-8-updates-to-mpeg-4-source-and-sink"></a>Atualizações do Windows 8 para fonte e coletor MPEG-4

-   Suporte de leitura e gravação de rotação adicionado na fonte e no coletor do Windows 8 MPEG-4. Não há suporte para isso na fonte e no coletor do Windows 7 MPEG-4.

    A origem MPEG-4 lê o ângulo de rotação de uma faixa de vídeo ativa como a soma do ângulo de rotação de ' mvhd ' e de ' tkhd '.

    O coletor MPEG-4 da Microsoft grava o ângulo de rotação em ' tkhd ', mas grava a matriz de 0 grau (identidade) em ' mvhd '. Observe que o coletor MPEG-4 da Microsoft oferece suporte apenas a faixa de vídeo único.

    IPropertyStore lê o ângulo de rotação somente para a primeira faixa de vídeo que a soma do ângulo de rotação de ' mvhd ' e de ' tkhd '.

    IPropertyStore grava o ângulo de rotação somente para a primeira faixa de vídeo em ' tkhd ' depois que o ângulo de rotação é ajustado de acordo com o ângulo de rotação em ' mvhd ', se existir.

-   Os fragmentos de filme (' Moof ') têm suporte na origem e no coletor do Windows 8 MPEG-4, mas ' mfra ' não.
-   H. 263 tem suporte na origem do Windows 8 MPEG-4.

    A origem MPEG-4 agora mapeia dois FOURCC de ' H263 ' e de 263 ' no formato de arquivo MPEG-4 para o tipo de mídia de **MFVideoFormat \_ H263**.

-   Suporte mais FOURCC adicionado para MJPEG na origem do Windows 8 MPEG-4.

    A origem MPEG-4 mapeia foucc de ' dmb1 ' para o tipo de mídia de **\_ MJPG MFVideoFormat**.

-   Suporte a metadados Furigana adicionado à origem do Windows 8 MPEG-4.

    A origem MPEG-4 lê metadados Furigana de ' soal ', ' disparar ', ' Soaa ', ' sonm ' e ' soco '. IPropertyStore lê os metadados do Furignana por meio do conjunto de PKEYs correspondentes.

    A tabela a seguir mostra o mapeamento entre o nome canônico do Shell, a chave de propriedade e a ID da caixa/marca no formato de arquivo MPEG-4.

    

    | Campo                                | Chave de propriedade                         | ID da marca/caixa |
    |--------------------------------------|--------------------------------------|------------|
    | System. Music. AlbumTitleSortOverride  | PKEY \_ Music \_ AlbumTitleSortOverride  | soal       |
    | System. Music. ArtistSortOverride      | PKEY \_ Music \_ ArtistSortOverride      | disparar       |
    | System. Music. AlbumArtistSortOverride | PKEY \_ Music \_ AlbumArtistSortOverride | soaa       |
    | System. TitleSortOverride             | PKEY \_ TitleSortOverride             | sonm       |
    | System. Music. ComposerSortOverride    | PKEY \_ Music \_ ComposerSortOverride    | soco       |

    

     

-   O suporte ao Atom 3D estéreo foi adicionado à origem do Windows 8 MPEG-4.

-   AC3 e DD + suporte adicionado na fonte e no coletor do Windows 8 MPEG-4.
-   Há suporte para arquivos maiores que 4 gigabytes (GB) no coletor MPEG-4 do Windows 8 para MP4 não fragmentado.
-   A depuração foi otimizada na origem do Windows 8 MPEG-4.

    Para reduzir a latência, as informações para os dois quadros-chave mais próximos para uma determinada posição de busca são expostas por meio de [**IMFSeekInfo:: GetNearestKeyFrames**](/windows/desktop/api/mfidl/nf-mfidl-imfseekinfo-getnearestkeyframes). Como o quadro-chave não tem quadros dependentes, ele apresenta o quadro depois da decodificação de apenas um quadro. Use [**IMFGetService:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) para obter essa interface por meio da origem, do pipeline ou do aplicativo de mídia.

    Defina a taxa como zero na fonte MPEG-4. Quando o pipeline está no modo de depuração, a taxa é zero.

-   O SPS e o PPS podem ser armazenados em dados de exemplo no coletor MPEG-4.

    [MF \_ O atributo de \_ \_ passagem MPEG4SINK SPSPPS](mf-mpeg4sink-spspps-passthrough.md) no coletor MPEG-4 é definido para permitir que SPS e PPS sejam salvos junto com os exemplos de entrada (dados de vídeo H. 264). Os clipes MP4 produzidos são capazes de ser reproduzidos pela fonte do Windows 7 MPEG-4 e outros.

-   O SPS e o PPS podem ser extraídos de exemplos de entrada no coletor MPEG-4.

    Quando o SPS e o PPS não estiverem definidos por meio do [ \_ cabeçalho de sequência MF MT \_ MPEG \_ \_ ](mf-mt-mpeg-sequence-header-attribute.md) no tipo de mídia de entrada do coletor MPEG-4, o coletor MPEG-4 tentará extrair o SPS e o PPS de exemplos de entrada. O coletor MPEG-4 ignora qualquer amostra de entrada até encontrar o primeiro SPS e o PPS, pois todos os exemplos de entrada sem SPS e PPS não são capazes de decodificar.

-   as informações 3D no registro de configuração AVC têm suporte para MP4 não fragmentado.
-   O comprimento de NALU é exposto para exemplos compactados de H. 264 para otimizar a decodificação de H. 264 VLD DXVA.

    Os conjuntos de origem MPEG-4 [NALU o tamanho do MF em \_ \_ \_ conjunto](mf-nalu-length-set.md) no tipo de mídia de saída de **MFVideoFormat \_ H264** ou **MFVideoFormat \_ H264**. Ele define o blob de [ \_ informações de \_ comprimento \_ de NALU MF](mf-nalu-length-information.md) em cada amostra de saída, com comprimento de NALU de quatro bytes para diferentes NALU em uma amostra compactada.

-   Suporte adicionado para áudio MPEG2 ADTS na fonte MP4.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Fontes de mídia e coletores](media-sources-and-sinks.md)
</dt> <dt>

[Suporte a MPEG-4 no Media Foundation](mpeg-4-support-in-media-foundation.md)
</dt> <dt>

[Formatos de mídia compatíveis com o Media Foundation](supported-media-formats-in-media-foundation.md)
</dt> </dl>

 

 




