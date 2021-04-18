---
description: O ADPCM (modulação diferencial de código de pulso) adaptável é um formato de compactação com perdas que é implementado para XAudio2 a fim de fornecer recursos adicionais para especificar o tamanho do bloco de amostra de compactação.
ms.assetid: ae8a0a3e-293c-8193-d252-046d79771cfb
title: Visão geral de ADPCM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fb918a611cb0840b2f02dfb13b547b795fb3304
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105788704"
---
# <a name="adpcm-overview"></a>Visão geral de ADPCM

O ADPCM (modulação diferencial de código de pulso) adaptável é um formato de compactação com perdas que é implementado para XAudio2 a fim de fornecer recursos adicionais para especificar o tamanho do bloco de amostra de compactação. Com um formato de compactação com perdas, alguns dados são alterados e perdidos durante a compactação. O ADPCM pode obter taxas de compactação de até 4:1.

A implementação de ADPCM for XAudio2 fornece recursos adicionais para especificar o tamanho do bloco de amostra de compactação. O ADPCM permite que o designer de áudio escolha uma configuração que seja um comprometimento apropriado entre o tamanho, a qualidade e a resolução (para colocar pontos de loop).

O XAudio2 usa uma versão modificada do codec ADPCM da Microsoft que dá suporte à formatação de dados estendidos necessária para fornecer tamanhos de bloco de amostra personalizados. Por esse motivo, os dados de áudio XAudio2 não podem ser reproduzidos por mecanismos de áudio que não dão suporte a essa versão do codec ADPCM.

> [!Note]  
> Atualmente, a compactação ADPCM só está disponível para o Windows, incluindo o XNA Game Studio Express para implantações do Windows.

 

## <a name="adpcm-encoding"></a>Codificação ADPCM

Os dados de áudio são codificados para ADPCM usando a ferramenta de linha de comando AdpcmEncode.

-   AdpcmEncode

    Para codificar arquivos de áudio como ADPCM para uso com XAudio2, use a ferramenta de linha de comando **AdpcmEncode** .

## <a name="adpcm-decoding"></a>Decodificação de ADPCM

A decodificação de software de ADPCM tem suporte em XAudio2.

-   XAudio2

    Para usar dados codificados em ADPCM no XAudio2, você precisa inicializar uma estrutura **ADPCMWAVEFORMAT** com valores específicos de ADPCM e passá-la como um argumento para [**IXAudio2:: CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice) ao criar uma voz de origem. Para obter um exemplo de como carregar e reproduzir um som no XAudio2, consulte [como: tocar um som com XAudio2](how-to--play-a-sound-with-xaudio2.md).

## <a name="samplesperblock"></a>SamplesPerBlock

A compactação ADPCM funciona separando a forma de onda em blocos e prevendo a variação das amostras de forma de onda dentro de cada bloco. O tamanho dos blocos é medido em exemplos. O menor tamanho de bloco é de 32 amostras e os mais altos são os exemplos de 512.

Blocos maiores permitem uma melhor compactação, o que resulta em tamanhos de arquivo menores, mas às custas da qualidade de som e da resolução para alinhar pontos de loop.

Em geral, modificar o valor de SamplesPerBlock resulta nessas compensações:



| Se SamplesPerBlock...      | Compactação de arquivo | Qualidade do som | Resolução de ponto de loop |
|----------------------------|------------------|---------------|-----------------------|
| Aumenta (até o máximo 512)  | Aumento        | Diminui     | Diminui             |
| Diminui (até o mínimo 32) | Diminui        | Aumento     | Aumento             |



 

## <a name="restrictions"></a>Restrições

Como o ADPCM usa blocos de exemplo alinhados um após o outro, uma onda compactada com ADPCM pode ter um bloco não concluído e parcial em seu final. O decodificador ADPCM gera silêncio para o restante deste bloco parcial, o que impede que a onda faça um loop contínuo.

O valor do parâmetro *SamplesPerBlock* afeta a resolução com a qual você pode alinhar os dados de onda e os pontos de loop.

Se você tentar aplicar a compactação a uma onda não alinhada, receberá um erro ou um aviso, dependendo se a onda é usada em qualquer evento de reprodução de looping. Não é possível compactar uma onda usada em qualquer evento de reprodução de looping. Remova-o dos eventos de reprodução de loop e aplique novamente a compactação.

Se você usar a onda exclusivamente no modo sem looping, a restrição de alinhamento de bloco de exemplo não se aplicará.

## <a name="adpcm-file-structure"></a>Estrutura de arquivo ADPCM

Um arquivo ADPCM é um arquivo RIFF padrão com os seguintes tipos de bloco.



| Parte da FCC     | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| RIFF          | A parte padrão do RIFF que contém um tipo de arquivo com o valor WAVE nos primeiros quatro bytes de sua seção de dados e as outras partes no arquivo no restante de sua seção de dados.                                                                                                                                                                                                                                                                 |
| fmt           | Contém o cabeçalho de formato do arquivo ADPCM. Os dados nessa parte correspondem a uma estrutura **ADPCMWAVEFORMAT** .                                                                                                                                                                                                                                                                                                                             |
| data          | Contém os dados de áudio ADPCM codificados. Ao usar o ADPCM em XAudio2, você precisa ler o conteúdo da parte de dados em um buffer e passá-lo para uma voz de origem como o membro **pAudioData** de uma estrutura de [**\_ buffer XAudio2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) . Você não precisa trocar o conteúdo da parte de dados.                                                                                                                            |
| smpl e wsmp | Tipos de bloco opcionais que contêm as informações de loop para o arquivo ADPCM. Quando você usa o ADPCM em XAudio2, os valores contidos nas partes smpl ou wsmp são usados para preencher os membros **LoopBeginLoopLength** e **LoopCount** da estrutura de [**\_ buffer XAudio2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) . No Xbox 360, você precisa trocar os dados carregados de uma parte smpl para considerar a diferença de endian entre o Windows e o Xbox 360. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Guia de programação](programming-guide.md)
</dt> </dl>

 

 
