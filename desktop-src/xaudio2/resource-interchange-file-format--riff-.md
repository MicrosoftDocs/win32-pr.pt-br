---
description: Esta visão geral descreve o formato de arquivo de intercâmbio de recursos (RIFF), que é usado em arquivos. wav. O RIFF é o formato típico do qual os dados de áudio para XAudio2 serão carregados.
ms.assetid: b543e949-223c-ddd3-7527-a41f3709a0c1
title: RIFF (Resource Interchange File Format)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d61eb45eff8db119eb73209b53b595f1cf6d243
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105772495"
---
# <a name="resource-interchange-file-format-riff"></a>RIFF (Resource Interchange File Format)

Esta visão geral descreve o formato de arquivo de intercâmbio de recursos (RIFF), que é usado em arquivos. wav. O RIFF é o formato típico do qual os dados de áudio para XAudio2 serão carregados.

## <a name="riff"></a>RIFF

Um arquivo RIFF é composto por várias seções discretas de dados chamada *partes*.

## <a name="fourcc-identifiers"></a>Identificadores FOURCC

O tipo de dados em uma parte é indicado por um identificador de código de quatro caracteres (FOURCC). Um FOURCC é um inteiro sem sinal de 32 bits criado pela concatenação de quatro caracteres ASCII usados para identificar tipos de bloco em um arquivo RIFF. Por exemplo, o "abcd" FOURCC é representado em um sistema little-endian como 0x64636261. Os FOURCCs podem conter caracteres de espaço, portanto, "ABC" é um FOURCC válido. Os arquivos de áudio usam códigos FOURCC para identificar partes de formato de áudio, partes de dados de áudio e quaisquer outras partes específicas do formato de áudio.

A tabela a seguir mostra os identificadores FOURCC que podem ser esperados nos formatos de áudio com suporte do XAudio2. 

| Formatar | Identificadores FOURCC                     | Informações adicionais                                                                               |
|--------|----------------------------------------|------------------------------------------------------------------------------------------------------|
| PCM    | "RIFF", "fmt", "dados"                 |                                                                                                      |
| ADPCM  | "RIFF", "fmt", "data", "smpl", "wsmpl" | Consulte [visão geral de ADPCM](adpcm-overview.md) para obter uma descrição dos identificadores FOURCC específicos de ADPCM. |



 

Os identificadores FOURCC "RIFF", "fmt" e "data" são comuns a todos os formatos com suporte. A tabela a seguir descreve os identificadores FOURCC que são encontrados em todos os formatos com suporte. 

| Identificador FOURCC | Descrição                                                                                                                                                                                                                        |
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| "RIFF"            | A parte padrão do RIFF que contém um tipo de arquivo com o valor de "WAVE" ou "XWMA" nos primeiros quatro bytes de sua seção de dados e as outras partes no arquivo no restante de sua seção de dados.                                   |
| "fmt"             | Contém o cabeçalho de formato do arquivo de áudio. Os dados nessa parte correspondem a uma das seguintes estruturas: **WAVEFORMATEX**, **WAVEFORMATEXTENSIBLE ADPCMWAVEFORMAT**.                                                  |
| "data"            | Contém dados de áudio para o arquivo de áudio. No XAudio2, o conteúdo da parte de dados será lido em um buffer e passado para uma voz de origem como o membro **pAudioData** de uma estrutura de [**\_ buffer XAudio2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) . |



 

## <a name="chunks"></a>Chunks

Um arquivo RIFF consiste em uma parte de RIFF que contém zero ou mais partes.

-   A parte do RIFF tem o seguinte formato:

    "RIFF", fileSize, fileType, dados

    Onde "RIFF" é o código FOURCC literal "RIFF", *fileSize* é um valor de 4 bytes fornecendo o tamanho dos dados no arquivo e *FILETYPE* é um FOURCC que identifica o tipo de arquivo específico. O valor de *fileSize* inclui o tamanho de *filetype* FOURCC mais o tamanho dos dados a seguir, mas não inclui o tamanho de "riff" FOURCC ou o tamanho de *fileSize*. Os dados consistem em partes em qualquer ordem.

-   Outras partes têm o seguinte formato:

    ```
    chunkID, chunkSize, data
    ```

    

    Em que *chunkid* é um FOURCC que identifica os dados contidos na parte, *ChunkSize* é um valor de 4 bytes fornecendo o tamanho da seção de dados da parte e os dados são zero ou mais bytes de dados. Os dados são sempre preenchidos para o limite de palavras mais próximo. *ChunkSize* fornece o tamanho dos dados válidos na parte. Ele não inclui o preenchimento, o tamanho de *chunkid* ou o tamanho de *ChunkSize*.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Introdução](getting-started.md)
</dt> <dt>

[Como: Reproduzir um som com o XAudio2](how-to--play-a-sound-with-xaudio2.md)
</dt> <dt>

[Referência de programação em XAudio2](programming-reference.md)
</dt> </dl>

 

 



