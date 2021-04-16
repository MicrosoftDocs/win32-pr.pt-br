---
description: O coletor de arquivos MPEG-4 cria arquivos MP4.
ms.assetid: 069b8e72-d081-466e-ac8d-c3f81c8a6f35
title: Coletor de arquivos MPEG-4
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c27517463bca7dfa88fdbc09d77f7a6512c896d
ms.sourcegitcommit: 9c8ddec1e955f181beecad0478c1fb79013b5e9d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/21/2021
ms.locfileid: "105750563"
---
# <a name="mpeg-4-file-sink"></a>Coletor de arquivos MPEG-4

O coletor de arquivos MPEG-4 cria arquivos MP4. Para obter mais informações sobre o formato de arquivo MP4, consulte os seguintes documentos de padrões:

-   ISO/IEC 14496-12: *tecnologia da informação – codificação de objetos de áudio-visual--parte 12: formato de arquivo de mídia base ISO*
-   ISO/IEC 14496-14: *tecnologia da informação – codificação de objetos de áudio-visual--parte 14: formato de arquivo MP4*

> [!Note]  
> (Esses recursos podem não estar disponíveis em alguns idiomas e países.)

 

O coletor de arquivos MPEG-4 não encapsula a funcionalidade de codificação.

Para criar o coletor de arquivos MPEG-4, chame a função [**MFCreateMPEG4MediaSink**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatempeg4mediasink) . O coletor de arquivos MPEG-4 expõe as seguintes interfaces por meio de **QueryInterface**:

-   [**IMFClockStateSink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink)
-   [**IMFFinalizableMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imffinalizablemediasink)
-   [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
-   [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator)
-   [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink)

## <a name="sample-description-box"></a>Caixa de descrição de exemplo

MP4 é um formato de contêiner extensível. A especificação MP4 não define uma estrutura fixa para descrever os tipos de mídia em um contêiner MP4. Em vez disso, ele define uma hierarquia de objetos que permite que as estruturas personalizadas sejam definidas para cada formato. A descrição do formato é armazenada na caixa Descrição de exemplo (' stsd ') para cada fluxo. A caixa Descrição de exemplo contém uma lista de entradas de exemplo. Para cada entrada de exemplo, um código de 4 bytes, semelhante a um FOURCC, define a estrutura de formato.

O coletor de arquivos MPEG-4 pode gerar a caixa de descrição de exemplo para os seguintes formatos:

-   Vídeo H. 264/AVC
-   Áudio AAC
-   Áudio MP3

Para outros formatos, a caixa Descrição de exemplo deve ser fornecida no tipo de mídia para cada fluxo. Para especificar a caixa Descrição de exemplo, defina os seguintes atributos no tipo de mídia:



| Atributo                                                                     | Descrição                                                                                                                                                   |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [\_Descrição de \_ exemplo de MPEG4 \_ \_ do MF MT](mf-mt-mpeg4-sample-description.md)      | Contém a caixa de descrição de exemplo como um blob binário.                                                                                                         |
| [\_Entrada de \_ \_ exemplo atual \_ \_ do MF MT MPEG4](mf-mt-mpeg4-current-sample-entry.md) | Especifica quais das entradas de exemplo na caixa de descrição de exemplo estão ativas no momento. (Opcional).<br/> No momento, o valor deve ser zero.<br/> |



 

Em alguns casos, não é possível gerar uma caixa de descrição de exemplo até que todos os dados tenham sido codificados. Por exemplo, informações como a taxa média de bits podem não ser conhecidas antes do tempo. Nesse caso, você pode atualizar o tipo de mídia usando a interface [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) no coletor de arquivos MPEG-4. Isso deve ser feito antes de o coletor de mídia ser finalizado.

Normalmente, o tipo de mídia é criado por um codificador upstream. O codificador pode gerar um novo tipo de mídia durante o streaming, por meio de uma alteração de formato dinâmico. Para obter mais informações, consulte [Dynamic Format Changes](basic-mft-processing-model.md).

## <a name="h264avc-video"></a>Vídeo H. 264/AVC

O coletor de arquivos MPEG-4 dá suporte à versão do fluxo AVC que tem um fluxo de vídeo elementar, com SPS (conjunto de parâmetros de sequência) e NALUs de conjunto de parâmetros de imagem (PPS) contidos na caixa de descrição de exemplo, conforme definido na seção ISO/IEC 14496 parte 15 5,1. O coletor de arquivos não oferece suporte ao método alternativo de armazenamento do SPS/PPS NALUs como um fluxo elementar do conjunto de parâmetros separado.

O coletor de arquivos MPEG-4 pode gerar a caixa de descrição de exemplo, mas deve ser fornecido com o SPS e o PPS NALUs. Especifique essas informações no tipo de mídia definindo o atributo [**de \_ \_ cabeçalho de \_ sequência \_ MF MT MPEG**](mf-mt-mpeg-sequence-header-attribute.md) . O valor do atributo é o cabeçalho de sequência H. 264. O cabeçalho de sequência deve consistir no SPS e no PPS NALUs delimitados por códigos de inicialização de 3 ou de 4 bytes.

Opcionalmente, ao configurar o coletor de arquivos, você pode omitir o atributo de [**\_ cabeçalho de sequência MF MT \_ MPEG \_ \_**](mf-mt-mpeg-sequence-header-attribute.md) do tipo de mídia inicial. Nesse caso, você deve atualizar o tipo de mídia posteriormente para incluir o cabeçalho de sequência.

O coletor de arquivos MPEG-4 tem os seguintes requisitos para AVC fragmentado:

-   O fragmentado deve estar em conformidade com a especificação de formato H. 264 anexo B. Em particular, NALUs deve ser delimitado com códigos de início de 3 ou 4 bytes.
-   Os exemplos de mídia devem conter todos os NALUs de dados e fatias que correspondam a um único tempo de apresentação.
-   Ao escrever quadros B em um arquivo MP4, você deve definir o carimbo de data/hora da apresentação e o carimbo de data/hora de decodificação. Se Stream tiver um quadro B e o carimbo de data/hora de decodificação não estiver definido, o gravador MP4 verá o tempo de quadro voltado para trás e descartará o quadro. 

## <a name="aac-audio"></a>Áudio AAC

Para o áudio AAC, o coletor de arquivos MPEG-4 pode gerar a caixa de descrição de exemplo para os seguintes subtipos:

-   **\_AAC MFAudioFormat**
-   **\_AAC1 bruto \_ MEDIASUBTYPE**

Para obter mais informações sobre esses substypes, consulte [tipos de mídia AAC](aac-media-types.md).

Para o subtipo **MFAudioFormat \_ AAC** , o tipo de mídia contém opcionalmente o atributo de [**\_ dados de \_ usuário \_ MF MT**](mf-mt-user-data-attribute.md) . Se estiver presente, esse atributo será a parte da estrutura [**HEAACWAVEINFO**](/windows/win32/api/mmreg/ns-mmreg-heaacwaveinfo) que aparece após a estrutura **WAVEFORMATEX** (ou seja, após o membro **WFX** ). Isso é seguido pelos dados de AudioSpecificConfig (), conforme definido por ISO/IEC 14496-3. Se o atributo de **\_ dados de \_ usuário \_ MF MT** não estiver presente, o fluxo será considerado como perfil de LC (complexidade baixa) e o coletor de arquivos MPEG-4 gerará uma caixa de descrição de exemplo adequada.

Para o subtipo **\_ \_ AAC1 bruto MEDIASUBTYPE** , o coletor de mídia deve conter o atributo de [**\_ dados de \_ usuário \_ MF MT**](mf-mt-user-data-attribute.md) e o atributo deve conter os dados AudioSpecificConfig ().

O coletor de arquivos MPEG-4 cria a variante MPEG-4 da caixa de descrição de exemplo AAC, usando uma entrada de exemplo ' mp4a ' com objectTypeIndication = 0x40. Ele não usa tipos de objeto MPEG-2.

## <a name="mp3-audio"></a>Áudio MP3

Para áudio MP3, o coletor de arquivos MPEG-4 pode gerar a caixa de descrição de exemplo de um tipo de mídia de áudio padrão. (Consulte [tipos de mídia de áudio](audio-media-types.md).)

O coletor de arquivos MPEG-4 cria a variante MPEG-4 da caixa de descrição de exemplo MP3, usando uma entrada de exemplo ' mp4a ' com objectTypeIndication = 0x6b para áudio MPEG-1.

## <a name="limitations"></a>Limitações

-   O tamanho máximo do arquivo criado é de 4 GB. No Windows 8, há suporte para arquivos de tamanho superior a 4 GBGB.
-   O coletor de arquivos MPEG-4 não oferece suporte a listas de edição (caixas ' EDTs ' e ' Elst ').

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
-   Há suporte para arquivos com mais de 4 GB no coletor MPEG-4 do Windows 8 para MP4 não fragmentado.
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

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/> |



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

 

 
