---
description: Esta visão geral descreve o FORMATO DE ARQUIVO de Intercâmbio de Recursos (FORMAT), que é usado em arquivos .wav. É o formato típico do qual os dados de áudio para XAudio2 serão carregados.
ms.assetid: b543e949-223c-ddd3-7527-a41f3709a0c1
title: RIFF (Resource Interchange File Format)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76c223c5a1047ffc9828a42ccc09ce4a94f5e766a1bc4851996b911f15f90995
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120054326"
---
# <a name="resource-interchange-file-format-riff"></a>RIFF (Resource Interchange File Format)

Esta visão geral descreve o FORMATO DE ARQUIVO de Intercâmbio de Recursos (FORMAT), que é usado em arquivos .wav. É o formato típico do qual os dados de áudio para XAudio2 serão carregados.

## <a name="riff"></a>RIFF

Um arquivo HASH é composto por várias seções discretas de dados chamadas *partes*.

## <a name="fourcc-identifiers"></a>Identificadores FOURCC

O tipo de dados em uma parte é indicado por um identificador de código de quatro caracteres (FOURCC). Um FOURCC é um inteiro sem sinal de 32 bits criado pela concatenação de quatro caracteres ASCII usados para identificar tipos de partes em um arquivo HASH. Por exemplo, FOURCC "abcd" é representado em um sistema little-endian como 0x64636261. FOURCCs podem conter caracteres de espaço, portanto, " abc" é um FOURCC válido. Os arquivos de áudio usam códigos FOURCC para identificar partes de formato de áudio, partes de dados de áudio e quaisquer outras partes específicas para o formato de áudio.

A tabela a seguir mostra os identificadores FOURCC que podem ser esperados nos formatos de áudio com suporte pelo XAudio2. 

| Formatar | Identificadores FOURCC                     | Informações adicionais                                                                               |
|--------|----------------------------------------|------------------------------------------------------------------------------------------------------|
| PCM    | "BLUES", "fmt" , "data"                 |                                                                                                      |
| Adpcm  | "BLUES", "fmt", "data", "smpl", "wsmpl" | Consulte [Visão geral do ADPCM](adpcm-overview.md) para ver uma descrição dos identificadores FOURCC específicos do ADPCM. |



 

Os identificadores FOURCC "PDF", "fmt" e "data" são comuns a todos os formatos com suporte. A tabela a seguir descreve os identificadores FOURCC encontrados em todos os formatos com suporte. 

| Identificador FOURCC | Descrição                                                                                                                                                                                                                        |
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| "RIFF"            | Parte STANDARD DE BYTES que contém um tipo de arquivo com o valor de "WAVE" ou "XWMA" nos primeiros quatro bytes de sua seção de dados e as outras partes do arquivo no restante de sua seção de dados.                                   |
| "fmt"             | Contém o header de formato para o arquivo de áudio. Os dados nesta parte correspondem a uma das seguintes estruturas: **WAVEFORMATEX**, **WAVEFORMATEXTENSIBLE ADPCMWAVEFORMAT**.                                                  |
| "data"            | Contém dados de áudio para o arquivo de áudio. No XAudio2, o conteúdo da parte de dados será lido em um buffer e passado para uma voz de origem como o membro **pAudioData** de uma estrutura [**\_ BUFFER XAUDIO2.**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) |



 

## <a name="chunks"></a>Chunks

Um arquivo DE VALOR consiste em uma parte DE HASH que contém zero ou mais partes.

-   A parte DE VALOR TEM o seguinte formato:

    "WIDGET", fileSize, fileType, data

    Em que "LITER" é o código LITERAL FOURCC "LITER", *fileSize* é um valor de 4 byte que dá o tamanho dos dados no arquivo e *fileType* é um FOURCC que identifica o tipo de arquivo específico. O valor *de fileSize* inclui o tamanho de *fileType* FOURCC mais o tamanho dos dados a seguir, mas não inclui o tamanho do FOURCC "THE" ou o tamanho de *fileSize*. Os dados consistem em partes em qualquer ordem.

-   Outras partes têm o seguinte formato:

    ```
    chunkID, chunkSize, data
    ```

    

    Em *que chunkID* é um FOURCC que identifica os dados contidos na parte, *chunkSize* é um valor de 4 bytes que dá o tamanho da seção de dados da parte e os dados são zero ou mais bytes de dados. Os dados são sempre padded para o limite word mais próximo. *chunkSize* fornece o tamanho dos dados válidos na parte. Ele não inclui o preenchimento, o tamanho de *chunkID* ou o tamanho *de chunkSize*.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Introdução](getting-started.md)
</dt> <dt>

[Como: Reproduzir um som com o XAudio2](how-to--play-a-sound-with-xaudio2.md)
</dt> <dt>

[Referência de programação em XAudio2](programming-reference.md)
</dt> </dl>

 

 



