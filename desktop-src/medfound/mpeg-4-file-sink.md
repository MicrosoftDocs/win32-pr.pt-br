---
description: O sink de arquivo MPEG-4 cria arquivos MP4.
ms.assetid: 069b8e72-d081-466e-ac8d-c3f81c8a6f35
title: MPEG-4 File Sink
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92e0175a5c21cc9f7c0186f70b37a5f94f5bf12151e606a2a441b4c75919d7e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119102106"
---
# <a name="mpeg-4-file-sink"></a>MPEG-4 File Sink

O sink de arquivo MPEG-4 cria arquivos MP4. Para obter mais informações sobre o formato de arquivo MP4, consulte os seguintes documentos padrão:

-   ISO/IEC 14496-12: Tecnologia da informação – Codificação de objetos *audiovisual – Parte 12: Formato* de arquivo de mídia base ISO
-   ISO/IEC 14496-14: Tecnologia da informação – Codificação de objetos *audiovisual – Parte 14: Formato de arquivo MP4*

> [!Note]  
> (Esses recursos podem não estar disponíveis em alguns idiomas e países.)

 

O sink de arquivo MPEG-4 não encapsula a funcionalidade de codificação.

Para criar o sink de arquivo MPEG-4, chame a [**função MFCreateMPEG4MediaSink.**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatempeg4mediasink) O sink de arquivo MPEG-4 expõe as seguintes interfaces por meio **de QueryInterface:**

-   [**IMFClockStateSink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink)
-   [**IMFFinalizableMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imffinalizablemediasink)
-   [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
-   [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator)
-   [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink)

## <a name="sample-description-box"></a>Caixa de descrição de exemplo

MP4 é um formato de contêiner extensível. A especificação MP4 não define uma estrutura fixa para descrever tipos de mídia em um contêiner MP4. Em vez disso, ele define uma hierarquia de objetos que permite que estruturas personalizadas sejam definidas para cada formato. A descrição do formato é armazenada na caixa de descrição de exemplo ('stsd') para cada fluxo. A caixa de descrição de exemplo contém uma lista de entradas de exemplo. Para cada entrada de exemplo, um código de 4 byte, semelhante a um FOURCC, define a estrutura de formato.

O Sink de Arquivos MPEG-4 pode gerar a caixa de descrição de exemplo para os seguintes formatos:

-   Vídeo H.264/AVC
-   Áudio do AAC
-   Áudio MP3

Para outros formatos, a caixa de descrição de exemplo deve ser fornecida no tipo de mídia para cada fluxo. Para especificar a caixa de descrição de exemplo, de definir os seguintes atributos no tipo de mídia:



| Atributo                                                                     | Descrição                                                                                                                                                   |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MF \_ MT \_ MPEG4 \_ SAMPLE \_ DESCRIPTION](mf-mt-mpeg4-sample-description.md)      | Contém a caixa de descrição de exemplo como um blob binário.                                                                                                         |
| [ENTRADA DE \_ EXEMPLO ATUAL DO MF MT \_ MPEG4 \_ \_ \_](mf-mt-mpeg4-current-sample-entry.md) | Especifica qual das entradas de exemplo na caixa de descrição de exemplo está ativa no momento. (Opcional).<br/> Atualmente, o valor deve ser zero.<br/> |



 

Em alguns casos, não é possível gerar uma caixa de descrição de exemplo até que todos os dados foram codificados. Por exemplo, informações como a taxa média de bits podem não ser conhecidas com antecedência. Nesse caso, você pode atualizar o tipo de mídia usando a interface [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) no sink de arquivos MPEG-4. Isso deve ser feito antes que o sink de mídia seja finalizado.

Normalmente, o tipo de mídia é criado por um codificador upstream. O codificador pode gerar um novo tipo de mídia durante o streaming, por meio de uma alteração de formato dinâmico. Para obter mais informações, consulte [Alterações de formato dinâmico.](basic-mft-processing-model.md)

## <a name="h264avc-video"></a>Vídeo H.264/AVC

O sink de arquivo MPEG-4 dá suporte à versão do fluxo do AVC que tem um fluxo de vídeo elementar, com SPS (conjunto de parâmetros de sequência) e NALUs pps (conjunto de parâmetros de imagem) contidos na caixa de descrição de exemplo, conforme definido em ISO/IEC 14496 parte 15 seção 5.1. O sink de arquivo não dá suporte ao método alternativo de armazenar NALUs SPS/PPS como um fluxo elementar separado do conjunto de parâmetros.

O sink de arquivo MPEG-4 pode gerar a caixa de descrição de exemplo, mas deve ser fornecido com as NALUs SPS e PPS. Especifique essas informações no tipo de mídia definindo o [**atributo \_ MF \_ MT MPEG \_ SEQUENCE \_ HEADER.**](mf-mt-mpeg-sequence-header-attribute.md) O valor do atributo é o header de sequência H.264. O header de sequência deve consistir nas NALUs SPS e PPS delimitadas por códigos de início de 3 ou 4 byte.

Opcionalmente, ao configurar o sink de arquivo, você pode omitir o atributo [**\_ MF \_ MT MPEG \_ SEQUENCE \_ HEADER**](mf-mt-mpeg-sequence-header-attribute.md) do tipo de mídia inicial. Nesse caso, você deve atualizar o tipo de mídia posteriormente para incluir o header de sequência.

O sink de arquivo MPEG-4 tem os seguintes requisitos para fluxos de bits do AVC:

-   O bitstream deve estar em conformidade com a especificação de formato H.264 Anexo B. Em particular, as NALUs devem ser delimitadas com códigos de início de 3 ou 4 byte.
-   Os exemplos de mídia devem conter todas as NALUs de dados e fatia que correspondem a uma única hora de apresentação.
-   Ao escrever quadros B em um arquivo MP4, você deve definir o carimbo de data/hora de apresentação e o carimbo de data/hora de decodificar. Se o fluxo tiver um quadro B e o timestamp de decodificar não estiver definido, o autor mp4 verá o tempo do quadro voltar e soltará o quadro. 

## <a name="aac-audio"></a>Áudio AAC

Para áudio AAC, o sink de arquivo MPEG-4 pode gerar a caixa de descrição de exemplo para os seguintes subtipos:

-   **MFAudioFormat \_ AAC**
-   **MEDIASUBTYPE \_ RAW \_ AAC1**

Para obter mais informações sobre esses subtipos, consulte [Tipos de mídia do AAC](aac-media-types.md).

Para o **subtipo \_ AAC MFAudioFormat,** o tipo de mídia opcionalmente contém o [**atributo \_ MF MT \_ USER \_ DATA.**](mf-mt-user-data-attribute.md) Se presente, esse atributo é a parte da estrutura [**HEAACWAVEINFO**](/windows/win32/api/mmreg/ns-mmreg-heaacwaveinfo) que aparece após a estrutura **WAVEFORMATEX** (ou seja, após o **membro wfx).** Isso é seguido pelos dados AudioSpecificConfig(), conforme definido por ISO/IEC 14496-3. Se o atributo **\_ MF MT \_ USER \_ DATA** não estiver presente, o fluxo será presumido como um perfil de LC (Baixa Complexidade) do AAC e o sink de arquivo MPEG-4 gerará uma caixa de descrição de exemplo adequada.

Para o subtipo **RAW \_ \_ AAC1 MEDIASUBTYPE,** o sink de mídia deve conter o atributo [**\_ MF MT \_ USER \_ DATA**](mf-mt-user-data-attribute.md) e o atributo deve conter os dados AudioSpecificConfig().

O sink de arquivo MPEG-4 cria a variante MPEG-4 da caixa de descrição de exemplo do AAC, usando uma entrada de exemplo 'mp4a' com objectTypeIndication = 0x40. Ele não usa tipos de objeto MPEG-2.

## <a name="mp3-audio"></a>Áudio MP3

Para áudio MP3, o sink de arquivo MPEG-4 pode gerar a caixa de descrição de exemplo de um tipo de mídia de áudio padrão. (Consulte Tipos [de mídia de áudio](audio-media-types.md).)

O sink de arquivo MPEG-4 cria a variante MPEG-4 da caixa de descrição de exemplo MP3, usando uma entrada de exemplo 'mp4a' com objectTypeIndication = 0x6b para áudio MPEG-1.

## <a name="limitations"></a>Limitações

-   O tamanho máximo do arquivo autor é de 4 GB. No Windows 8, há suporte para arquivos com mais de 4 GB GB.
-   O sink de arquivo MPEG-4 não dá suporte a listas de edição (caixas 'edts' e 'elst').

## <a name="windows-8-updates-to-mpeg-4-source-and-sink"></a>Windows 8 atualizações para a origem e o sink MPEG-4

-   Suporte de leitura e gravação de rotação adicionado Windows 8 origem e o sink MPEG-4. Isso não tem suporte na fonte e no Windows 7 MPEG-4.

    A fonte MPEG-4 lê o ângulo de rotação de uma faixa de vídeo ativa como a soma do ângulo de rotação de 'mvhd' e 'tkhd'.

    O sink do Microsoft MPEG-4 grava o ângulo de rotação em 'tkhd', mas grava uma matriz de 0 grau (identidade) em 'mvhd'. Observe que o microsoft MPEG-4 sink dá suporte apenas a uma única faixa de vídeo.

    IPropertyStore lê o ângulo de rotação apenas para a primeira faixa de vídeo como a soma do ângulo de rotação de 'mvhd' e de 'tkhd'.

    IPropertyStore grava o ângulo de rotação apenas para a primeira faixa de vídeo em 'tkhd' depois que o ângulo de rotação é ajustado de acordo com o ângulo de rotação em 'mvhd', se ele existir.

-   Fragmentos de filme ('moof') são suportados na fonte e no Windows 8 MPEG-4, mas 'mfra' não é.
-   H.263 tem suporte na fonte Windows 8 MPEG-4.

    A origem MPEG-4 agora mapeia dois fourccs de 'h263' e 's263' no formato de arquivo MPEG-4 para o tipo de mídia **MFVideoFormat \_ H263**.

-   Mais suporte a fourcc adicionado para MJPEG Windows 8 fonte MPEG-4.

    MPEG-4 mapeia foucc de 'dmb1' para o tipo de mídia **MFVideoFormat \_ MJPG**.

-   Suporte a metadados do Furriaa adicionado Windows 8 fonte MPEG-4.

    A origem MPEG-4 lê metadados de Furfunção de 'soal', 'soar', 'soaa', 'filhom' e 'verão'. IPropertyStore lê metadados de Furquitoa por meio do conjunto de PKEYs correspondentes.

    A tabela a seguir mostra o mapeamento entre o nome canônico do shell, a chave de propriedade e a ID da caixa/marca no formato de arquivo MPEG-4.

    

    | Campo                                | Chave de propriedade                         | ID de marca/caixa |
    |--------------------------------------|--------------------------------------|------------|
    | System.Music.AlbumTitleSortOverride  | PKEY \_ Music \_ AlbumTitleSortOverride  | soal       |
    | System. Music. ArtistSortOverride      | PKEY \_ Music \_ ArtistSortOverride      | disparar       |
    | System. Music. AlbumArtistSortOverride | PKEY \_ Music \_ AlbumArtistSortOverride | soaa       |
    | System. TitleSortOverride             | PKEY \_ TitleSortOverride             | sonm       |
    | System. Music. ComposerSortOverride    | PKEY \_ Music \_ ComposerSortOverride    | soco       |

    

     

-   o suporte ao atom 3d estéreo foi adicionado em Windows 8 fonte MPEG-4.

-   AC3 e DD + suporte adicionado em Windows 8 fonte e coletor MPEG-4.
-   há suporte para arquivos com mais de 4 GB em Windows 8 coletor MPEG-4 para MP4 não fragmentado.
-   a depuração foi otimizada na fonte Windows 8 MPEG-4.

    Para reduzir a latência, as informações para os dois quadros-chave mais próximos para uma determinada posição de busca são expostas por meio de [**IMFSeekInfo:: GetNearestKeyFrames**](/windows/desktop/api/mfidl/nf-mfidl-imfseekinfo-getnearestkeyframes). Como o quadro-chave não tem quadros dependentes, ele apresenta o quadro depois da decodificação de apenas um quadro. Use [**IMFGetService:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) para obter essa interface por meio da origem, do pipeline ou do aplicativo de mídia.

    Defina a taxa como zero na fonte MPEG-4. Quando o pipeline está no modo de depuração, a taxa é zero.

-   O SPS e o PPS podem ser armazenados em dados de exemplo no coletor MPEG-4.

    [MF \_ O atributo de \_ \_ passagem MPEG4SINK SPSPPS](mf-mpeg4sink-spspps-passthrough.md) no coletor MPEG-4 é definido para permitir que SPS e PPS sejam salvos junto com os exemplos de entrada (dados de vídeo H. 264). os clipes mp4 produzidos são capazes de ser reproduzidos por fonte Windows 7 MPEG-4 e outros.

-   O SPS e o PPS podem ser extraídos de exemplos de entrada no coletor MPEG-4.

    Quando o SPS e o PPS não estiverem definidos por meio do [ \_ cabeçalho de sequência MF MT \_ MPEG \_ \_ ](mf-mt-mpeg-sequence-header-attribute.md) no tipo de mídia de entrada do coletor MPEG-4, o coletor MPEG-4 tentará extrair o SPS e o PPS de exemplos de entrada. O coletor MPEG-4 ignora qualquer amostra de entrada até encontrar o primeiro SPS e o PPS, pois todos os exemplos de entrada sem SPS e PPS não são capazes de decodificar.

-   as informações 3D no registro de configuração AVC têm suporte para MP4 não fragmentado.
-   O comprimento de NALU é exposto para exemplos compactados de H. 264 para otimizar a decodificação de H. 264 VLD DXVA.

    Os conjuntos de origem MPEG-4 [NALU o tamanho do MF em \_ \_ \_ conjunto](mf-nalu-length-set.md) no tipo de mídia de saída de **MFVideoFormat \_ H264** ou **MFVideoFormat \_ H264**. Ele define o blob de [ \_ informações de \_ comprimento \_ de NALU MF](mf-nalu-length-information.md) em cada amostra de saída, com comprimento de NALU de quatro bytes para diferentes NALU em uma amostra compactada.

-   Suporte adicionado para áudio MPEG2 ADTS na fonte MP4.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[somente aplicativos de área de trabalho Windows 7\]<br/>              |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do Server 2008 R2\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Fontes de mídia e coletores](media-sources-and-sinks.md)
</dt> <dt>

[Coletores de mídia](media-sinks.md)
</dt> <dt>

[Suporte a MPEG-4 no Media Foundation](mpeg-4-support-in-media-foundation.md)
</dt> <dt>

[Formatos de mídia compatíveis com o Media Foundation](supported-media-formats-in-media-foundation.md)
</dt> </dl>

 

 
