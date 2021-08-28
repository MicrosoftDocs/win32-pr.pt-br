---
description: A ADPCM (Modularidade de Código de Pulso Diferencial Adaptável) é um formato de compactação com perda implementado para XAudio2 para fornecer recursos adicionais para especificar o tamanho do bloco de exemplo de compactação.
ms.assetid: ae8a0a3e-293c-8193-d252-046d79771cfb
title: Visão geral do ADPCM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e1be1155d6d9f5a542b605c497ce28aa34191c0ac129582c18ec4a47b9f510f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118962715"
---
# <a name="adpcm-overview"></a>Visão geral do ADPCM

A ADPCM (Modularidade de Código de Pulso Diferencial Adaptável) é um formato de compactação com perda implementado para XAudio2 para fornecer recursos adicionais para especificar o tamanho do bloco de exemplo de compactação. Com um formato de compactação com perda, alguns dados são alterados e perdidos durante a compactação. O ADPCM pode obter taxas de compactação de até 4:1.

A implementação do ADPCM para XAudio2 fornece recursos adicionais para especificar o tamanho do bloco de exemplo de compactação. O ADPCM permite que o designer de áudio escolha uma configuração que seja um comprometimento apropriado entre tamanho, qualidade e resolução (para colocar pontos de loop).

O XAudio2 usa uma versão modificada do codec do Microsoft ADPCM que dá suporte à formatação de dados estendida necessária para fornecer tamanhos de bloco de exemplo personalizados. Por esse motivo, os dados de áudio XAudio2 não podem ser interpretados por mecanismos de áudio que não suportam essa versão do codec do ADPCM.

> [!Note]  
> Atualmente, a compactação ADPCM só está disponível para Windows, incluindo o XNA Game Studio Express para Windows implantações.

 

## <a name="adpcm-encoding"></a>Codificação ADPCM

Os dados de áudio são codificados no ADPCM usando a ferramenta de linha de comando AdpcmEncode.

-   AdpcmEncode

    Para codificar arquivos de áudio como ADPCM para uso com XAudio2, use a ferramenta de linha de comando **AdpcmEncode.**

## <a name="adpcm-decoding"></a>Decodificação do ADPCM

Há suporte para a decodificação de software do ADPCM no XAudio2.

-   XAudio2

    Para usar dados codificados no ADPCM no XAudio2, você precisa inicializar uma estrutura **ADPCMWAVEFORMAT** com valores específicos do ADPCM e passá-los como um argumento para [**IXAudio2::CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice) ao criar uma voz de origem. Para ver um exemplo de como carregar e reproduzir um som no XAudio2, consulte Como reproduzir um [som com XAudio2](how-to--play-a-sound-with-xaudio2.md).

## <a name="samplesperblock"></a>SamplesPerBlock

A compactação do ADPCM funciona separando a forma de onda em blocos e prevendo a variação das amostras de forma de onda dentro de cada bloco. O tamanho dos blocos é medido em amostras. O menor tamanho de bloco é de 32 amostras e o mais alto é 512 amostras.

Blocos maiores permitem uma compactação melhor, o que resulta em tamanhos de arquivo menores, mas às custas da qualidade do som e da resolução para alinhar pontos de loop.

Em geral, modificar o valor SamplesPerBlock resulta nessas trocas:



| Se SamplesPerBlock...      | Compactação de arquivo | Qualidade do som | Resolução de ponto de loop |
|----------------------------|------------------|---------------|-----------------------|
| Aumentos (até no máximo 512)  | Aumenta        | Diminui     | Diminui             |
| Diminui (até o mínimo 32) | Diminui        | Aumenta     | Aumenta             |



 

## <a name="restrictions"></a>Restrições

Como o ADPCM usa blocos de exemplo alinhados um após o outro, uma onda compactada com ADPCM pode ter um bloco parcial incompleto no final. O decodificador ADPCM gera silêncio para o restante desse bloco parcial, o que impede que a onda seja em loop contínuo.

O valor do parâmetro *SamplesPerBlock* afeta a resolução com a qual você pode alinhar dados de onda e pontos de loop.

Se você tentar aplicar a compactação a uma onda não alinhada, receberá um erro ou um aviso, dependendo se a onda for usada em qualquer evento de reprodução em loop. Você não pode compactar uma onda usada em nenhum evento de reprodução em loop. Remova-o dos eventos de reprodução de loop e aplique a compactação.

Se você usar a onda exclusivamente no modo sem looping, a restrição de alinhamento de bloco de exemplo não se aplicará.

## <a name="adpcm-file-structure"></a>Estrutura de arquivos ADPCM

Um arquivo ADPCM é um arquivo DEDP padrão com os seguintes tipos de partes.



| Parte DEFC     | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| RIFF          | Parte STANDARD DE BYTES que contém um tipo de arquivo com o valor WAVE nos primeiros quatro bytes de sua seção de dados e as outras partes no arquivo no restante de sua seção de dados.                                                                                                                                                                                                                                                                 |
| Fmt           | Contém o header de formato para o arquivo ADPCM. Os dados nesta parte correspondem a uma **estrutura ADPCMWAVEFORMAT.**                                                                                                                                                                                                                                                                                                                             |
| data          | Contém os dados de áudio ADPCM codificados. Ao usar o ADPCM no XAudio2, você precisa ler o conteúdo da parte de dados em um buffer e passá-lo para uma voz de origem como o membro **pAudioData** de uma estrutura [**\_ BUFFER XAUDIO2.**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) Você não precisa trocar o conteúdo da parte de dados por byte.                                                                                                                            |
| smpl e wsmp | Tipos de partes opcionais que contêm as informações de loop para o arquivo ADPCM. Quando você usa o ADPCM no XAudio2, os valores contidos nas partes smpl ou wsmp são usados para preencher os membros **LoopBeginLoopLength** e **LoopCount** da estrutura [**\_ BUFFER XAUDIO2.**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) No Xbox 360, você precisa alternar os dados carregados de uma parte smpl para levar em conta a diferença de endianidade entre Windows e Xbox 360. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Guia de programação](programming-guide.md)
</dt> </dl>

 

 
