---
description: Referência de arquivo RIFF AVI
ms.assetid: 2d8cf5be-1252-4b58-89b1-f5c53ea17d0e
title: Referência de arquivo RIFF AVI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83f28a7254ac9eb927381e313603ffd2bd0d050c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104456831"
---
# <a name="avi-riff-file-reference"></a>Referência de arquivo RIFF AVI

O formato de arquivo AVI da Microsoft é uma especificação de arquivo RIFF usada com aplicativos que capturam, editam e reproduzem sequências de vídeo de áudio. Em geral, os arquivos AVI contêm vários fluxos de diferentes tipos de dados. A maioria das sequências AVI usa fluxos de áudio e vídeo. Uma variação simples para uma sequência AVI usa dados de vídeo e não requer um fluxo de áudio.

Esta seção não descreve as extensões de formato de arquivo AVI OpenDML. Para obter mais informações sobre essas extensões, consulte *extensões de formato de arquivo AVI OpenDML*, publicadas pelo Subcomitê OpenDML AVI M-JPEG File Format.

## <a name="fourccs"></a>FOURCC

Um FOURCC (código de quatro caracteres) é um inteiro sem sinal de 32 bits criado com a concatenação de quatro caracteres ASCII. Por exemplo, o ' ABCD ' FOURCC é representado em um sistema de Little-Endian como 0x64636261. Os FOURCCs podem conter caracteres de espaço, portanto, ' abc ' é um FOURCC válido. O formato de arquivo AVI usa códigos FOURCC para identificar tipos de fluxo, partes de dados, entradas de índice e outras informações.

## <a name="riff-file-format"></a>Formato de arquivo RIFF

O formato de arquivo AVI é baseado no formato de documento RIFF (formato de arquivo de intercâmbio de recursos). Um arquivo RIFF consiste em um cabeçalho RIFF seguido por zero ou mais *listas* e *partes*.

-   O cabeçalho RIFF tem o seguinte formato:

    `'RIFF' fileSize fileType (data)`

    onde ' RIFF ' é o código FOURCC literal ' RIFF ', `fileSize` é um valor de 4 bytes fornecendo o tamanho dos dados no arquivo e `fileType` é um FOURCC que identifica o tipo de arquivo específico. O valor de `fileSize` inclui o tamanho do `fileType` FOURCC mais o tamanho dos dados a seguir, mas não inclui o tamanho de ' riff ' FOURCC ou o tamanho de `fileSize` . Os dados de arquivo consistem em partes e listas, em qualquer ordem.

-   Uma parte tem o seguinte formato:

    `ckID ckSize ckData`

    onde `ckID` é um FOURCC que identifica os dados contidos na parte, `ckSize` é um valor de 4 bytes fornecendo o tamanho dos dados `ckData` e `ckData` é zero ou mais bytes de dados. Os dados sempre são preenchidos para o limite de **palavras** mais próximo. `ckSize` fornece o tamanho dos dados válidos na parte; Ele não inclui o preenchimento, o tamanho `ckID` ou o tamanho de `ckSize` .

-   Uma lista tem o seguinte formato:

    `'LIST' listSize listType listData`

    onde ' LIST ' é o código FOURCC literal ' LIST ', `listSize` é um valor de 4 bytes que dá o tamanho da lista, `listType` é um código FOURCC e `listData` consiste em partes ou listas, em qualquer ordem. O valor de `listSize` inclui o tamanho de `listType` mais o tamanho de `listData` ; ele não inclui o FOURCC ' list ' ou o tamanho de `listSize` .

O restante desta seção usa a seguinte notação para descrever as partes do RIFF:

`ckID ( ckData )`

onde o tamanho da parte é implícito. Usando essa notação, uma lista pode ser representada como:

`'LIST' ( listType ( listData ) )`

Elementos opcionais são colocados entre colchetes: `[ optional element ]`

## <a name="avi-riff-form"></a>Formulário RIFF AVI

Os arquivos AVI são identificados pelo ' AVI ' FOURCC no cabeçalho RIFF. Todos os arquivos AVI incluem duas partes de lista obrigatórias, que definem o formato dos fluxos e os dados de fluxo, respectivamente. Um arquivo AVI também pode incluir uma parte de índice, que fornece o local das partes de dados dentro do arquivo. Um arquivo AVI com esses componentes tem o seguinte formato:


```C++
RIFF ('AVI '
      LIST ('hdrl' ... )
      LIST ('movi' ... )
      ['idx1' (<AVI Index>) ]
     )
```



A lista ' hdrl ' define o formato dos dados e é a primeira parte da lista necessária. A lista ' movi ' contém os dados para a sequência AVI e é a segunda parte de lista necessária. A lista ' idx1 ' contém o índice. Os arquivos AVI devem manter esses três componentes na sequência correta.

> [!Note]  
> As extensões OpenDML definem outro tipo de índice, identificado pelo ' INDX ' FOURCC.

 

As listas ' hdrl ' e ' movi ' usam subpartes para seus dados. O exemplo a seguir mostra o formulário RIFF AVI expandido com as partes necessárias para concluir essas listas:


```C++
RIFF ('AVI '
      LIST ('hdrl'
            'avih'(<Main AVI Header>)
            LIST ('strl'
                  'strh'(<Stream header>)
                  'strf'(<Stream format>)
                  [ 'strd'(<Additional header data>) ]
                  [ 'strn'(<Stream name>) ]
                  ...
                 )
             ...
           )
      LIST ('movi'
            {SubChunk | LIST ('rec '
                              SubChunk1
                              SubChunk2
                              ...
                             )
               ...
            }
            ...
           )
      ['idx1' (<AVI Index>) ]
     )
```



## <a name="avi-main-header"></a>Cabeçalho principal AVI

A lista ' hdrl ' começa com o cabeçalho AVI principal, que está contido em uma parte ' avih '. O cabeçalho principal contém informações globais para todo o arquivo AVI, como o número de fluxos dentro do arquivo e a largura e a altura da sequência AVI. A parte do cabeçalho principal consiste em uma estrutura [**AVIMAINHEADER**](/previous-versions/windows/desktop/api/Aviriff/ns-aviriff-avimainheader) .

## <a name="avi-stream-headers"></a>Cabeçalhos de fluxo AVI

Uma ou mais listas de ' strl ' seguem o cabeçalho principal. Uma lista ' strl ' é necessária para cada fluxo de dados. Cada lista ' strl ' contém informações sobre um fluxo no arquivo e deve conter uma parte de cabeçalho de fluxo (' strh ') e uma parte de formato de fluxo (' strf '). Além disso, uma lista ' strl ' pode conter uma parte de dados de cabeçalho de fluxo (' strd ') e uma parte de nome de fluxo (' strn ').

A parte do cabeçalho do fluxo (' strh ') consiste em uma estrutura [**AVISTREAMHEADER**](/previous-versions/windows/desktop/api/avifmt/ns-avifmt-avistreamheader) .

Uma parte do formato do fluxo (' strf ') deve seguir a parte do cabeçalho do fluxo. A parte do formato do fluxo descreve o formato dos dados no fluxo. Os dados contidos nessa parte dependem do tipo de fluxo. Para fluxos de vídeo, as informações são uma estrutura [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) , incluindo informações de paleta, se apropriado. Para fluxos de áudio, as informações são uma estrutura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) .

Se a parte de dados de cabeçalho de fluxo (' strd ') estiver presente, ela seguirá a parte de formato de fluxo. O formato e o conteúdo dessa parte são definidos pelo driver do codec. Normalmente, os drivers usam essas informações para configuração. Os aplicativos que lêem e gravam arquivos AVI não precisam interpretar essas informações; Eles a transferem de forma simples para e do driver como um bloco de memória.

O bloco ' strn ' opcional contém uma cadeia de caracteres de texto terminada em nulo que descreve o fluxo.

Os cabeçalhos de fluxo na lista ' hdrl ' são associados aos dados de fluxo na lista ' movi ' de acordo com a ordem das partes ' strl '. O primeiro bloco ' strl ' se aplica ao fluxo 0, o segundo se aplica ao fluxo 1 e assim por diante.

## <a name="stream-data-movi-list"></a>Dados de fluxo (lista ' movi ')

Seguir as informações de cabeçalho é uma lista ' movi ' que contém os dados reais nos fluxos, ou seja, os quadros de vídeo e amostras de áudio. As partes de dados podem residir diretamente na lista ' movi ' ou podem ser agrupadas em listas de ' Rec '. O agrupamento ' Rec ' implica que as partes agrupadas devem ser lidas do disco de uma só vez e destinam-se a arquivos intercalados para reprodução a partir do CD-ROM.

O FOURCC que identifica cada parte de dados consiste em um número de fluxo de dois dígitos seguido por um código de dois caracteres que define o tipo de informação na parte.



| Código de dois caracteres | Descrição              |
|--------------------|--------------------------|
| db                 | Quadro de vídeo descompactado |
| dc                 | Quadro de vídeo compactado   |
| pc                 | Alteração da paleta           |
| WB                 | Dados de áudio               |



 

Por exemplo, se o fluxo 0 contiver áudio, as partes de dados desse fluxo teriam o FOURCC ' 00wb '. Se o fluxo 1 contiver vídeo, as partes de dados desse fluxo teriam o FOURCC ' 01dB ' ou ' 01dc '. As partes de dados de vídeo também podem definir novas entradas de paleta para atualizar a paleta durante uma sequência AVI. Cada bloco de alteração de paleta (' xxpc ') contém uma estrutura [**AVIPALCHANGE**](/previous-versions/windows/desktop/api/avifmt/ns-avifmt-avipalchange) . Se um fluxo contiver alterações de paleta, defina o sinalizador **AVISF de \_ vídeo \_ PALCHANGES** no membro **dwFlags** da estrutura [**AVISTREAMHEADER**](/previous-versions/windows/desktop/api/avifmt/ns-avifmt-avistreamheader) para esse fluxo.

Os fluxos de texto podem usar códigos de dois caracteres arbitrários.

## <a name="avi-index-entries"></a>Entradas de índice AVI

<dl> <dt>

<span id="AVI_1.0_index"></span><span id="avi_1.0_index"></span><span id="AVI_1.0_INDEX"></span>Índice AVI 1,0
</dt> <dd>

Um bloco de índice (' idx1 ') opcional pode seguir a lista ' movi '. O índice contém uma lista de partes de dados e sua localização no arquivo. Ele consiste em uma estrutura [**AVIOLDINDEX**](/previous-versions/windows/desktop/api/Aviriff/ns-aviriff-avioldindex) com entradas para cada parte de dados, incluindo partes ' Rec '. Se o arquivo contiver um índice, defina o sinalizador **AVIF \_ HASINDEX** no membro **dwFlags** da estrutura [**AVIMAINHEADER**](/previous-versions/windows/desktop/api/Aviriff/ns-aviriff-avimainheader) .

</dd> <dt>

<span id="AVI_2.0_index"></span><span id="avi_2.0_index"></span><span id="AVI_2.0_INDEX"></span>Índice AVI 2,0
</dt> <dd>

Um índice AVI 2,0 pode aparecer como uma única parte. Como alternativa, os segmentos de índice podem ser intercalados na parte ' movi '. Se os segmentos de índice forem colocados na parte ' movi ', um superíndice conterá um índice dos segmentos de índice. A estrutura [**AVIMETAINDEX**](/previous-versions/windows/desktop/api/aviriff/ns-aviriff-avimetaindex) é a estrutura base para os segmentos de índice e o superindex. Para obter mais informações, consulte as *extensões de formato de arquivo AVI OpenDML*, publicadas pelo Subcomitê de formato de arquivo AVI M-JPEG OpenDML. (Esse recurso pode não estar disponível em alguns idiomas e países.)

</dd> </dl>

## <a name="other-data-chunks"></a>Outras partes de dados

Os dados podem ser alinhados em um arquivo AVI inserindo partes "lixo eletrônico" conforme necessário. Os aplicativos devem ignorar o conteúdo de uma parte ' lixo '.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Formato de arquivo AVI](avi-file-format.md)
</dt> </dl>

 

 
