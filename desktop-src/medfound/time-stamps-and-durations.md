---
description: Este tópico descreve como Media Foundation transformações devem lidar com carimbos de data/hora.
ms.assetid: 4ab576ce-becd-4736-921e-e463c0dff841
title: Carimbos de data/hora e durações
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22452e8b6b8094e643126f479f13b2c447db584588f3be1c1aa6595b3e7e2bb7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119953196"
---
# <a name="time-stamps-and-durations"></a>Carimbos de data/hora e durações

Este tópico descreve como [Media Foundation transformações](media-foundation-transforms.md) devem lidar com carimbos de data/hora.

Uma MFT deve definir a precisão de um carimbo de data/hora e a duração possível em todas as amostras de saída. Para um MFT simples que usa um buffer de entrada e o processa completamente em um buffer de saída, o MFT deve simplesmente copiar o carimbo de data/hora e a duração diretamente do exemplo de entrada para o exemplo de saída. No entanto, muitas transformações são mais complexas do que isso e podem exigir cálculos mais complexos de tempo de saída. Todos os MFTs devem observar as seguintes regras básicas:

-   Um MFT deve tentar colocar um carimbo de data/hora e uma duração em todos os exemplos de saída de áudio ou vídeo não compactados se um carimbo de data/hora preciso ou a duração for dada nos exemplos de entrada ou puder ser calculado. A interpolação pode ser necessária para alguns carimbos de hora de saída, especialmente para decodificadores.
-   Os carimbos de data/hora e as durações dos exemplos de entrada devem ser preservados nas amostras de saída tanto quanto possível.
-   As durações ou os carimbos de data/hora de saída podem não corresponder à entrada porque o MFT está mantendo dados de volta ou dividindo a saída em partes de tamanhos diferentes da entrada. Nesse caso, o MFT deve calcular o carimbo de data/hora de saída do exemplo de entrada mais antigo que contém os dados usados para criar o exemplo de saída. Para calcular o carimbo de data/hora de saída, adicione o carimbo de data/hora de entrada do exemplo de entrada apropriado à duração dos dados que já foram transformados nesse exemplo. O segundo exemplo no final desta seção ilustra essa ideia.
-   Se os exemplos de entrada tiverem duração, essa duração deverá ser preservada. Se uma amostra de entrada não tiver duração, o MFT deverá calcular uma duração, se possível, a partir do tamanho do buffer de saída ou da taxa de dados fornecida pelo tipo de mídia.
-   As durações calculadas devem ser truncadas (arredondadas), não arredondadas para o incremento mais próximo. O pipeline tem uma margem de atraso suficiente para lidar com as durações que são ligeiramente imprecisas, mas é mais fácil para o pipeline lidar com uma duração que é de 1% muito curta do que uma duração que é de 1% muito longa. Dito isso, não há motivo para reduzir deliberadamente as durações, além do arredondamento.

### <a name="decoders"></a>Decodificadores

Um decodificador converte pacotes compactados em dados descompactados. Como a saída é descompactada, os decodificadores têm uma obrigação especial para obter os carimbos de data/hora e as durações corretas. Alguns formatos compactados, mais notavelmente MPEG-2, não têm carimbos de data/hora em todos os pacotes de entrada e geralmente não têm duração em nenhum pacote. Para esses formatos, o decodificador é responsável por colocar um carimbo de data/hora e uma duração válidos em cada amostra de saída, somando as durações implícitas de todas as saídas desde o último exemplo de entrada com carimbo de data/hora.

Para vídeo, se a duração não estiver disponível no formato compactado, o decodificador deverá calcular a duração como o inverso da taxa de quadros, convertido em unidades de 100 nanossegundos e arredondado para baixo.

Para áudio, se a duração não estiver disponível no formato compactado, o decodificador deverá calcular a duração como o inverso da taxa de amostra de áudio multiplicado pelo número de amostras no buffer de saída, convertido em unidades de 100 nanossegundos e arredondado para baixo.

A única vez que uma transformação deve gerar uma amostra sem um carimbo de data/hora é se a MFT nunca recebeu um carimbo de data/hora em um exemplo de entrada ou se não há nenhuma maneira de calcular um carimbo de data/hora de saída preciso do carimbo de data/hora de entrada anterior.

### <a name="audio-decoders"></a>Decodificadores de áudio

Para decodificadores de áudio, a duração de cada exemplo de saída é calculada a partir da taxa de amostragem de áudio e o número de amostras de PCM por canal no buffer de saída.

A maneira correta de calcular carimbos de hora de saída depende se os exemplos de entrada contêm carimbos de data/hora.

Se os exemplos de entrada contiverem carimbos de data/hora, o decodificador calculará os carimbos de data/hora de saída dos carimbos de data/hora

-   Se cada buffer de entrada contiver um ou mais quadros compactados completos, sem quadros parciais, o carimbo de data/hora de saída será igual ao carimbo de data/hora de entrada, menos a latência conhecida do decodificador. Por exemplo, um decodificador Dolby Digital (AC-3) tem uma latência de 256 amostras de PCM. Por exemplo, com taxa de amostragem de 48-kHz, a latência é de 5,33 milissegundos (MS). Portanto, se o carimbo de data/hora de entrada for 1000 mseg, o carimbo de data/hora de saída será 1000 – 5,33 = 994,66 MS. Se o buffer de entrada incluir mais de um quadro compactado inteiro, o decodificador produzirá um exemplo de saída para cada quadro no exemplo de entrada. Todos os exemplos de saída serão marcados corretamente de modo que não haja intervalos.
-   Dependendo do formato de transporte, um buffer de entrada pode conter quadros parciais. Por exemplo, um buffer pode conter parte de um quadro do buffer de entrada anterior, seguido por um ou mais quadros completos, seguidos do início do próximo quadro. Nesse caso, geralmente está correto para assumir que o carimbo de data/hora de entrada corresponde ao primeiro quadro que começa dentro do buffer. (Ou seja, um quadro parcial iniciado no buffer anterior não está incluído no carimbo de data/hora do buffer atual.) Calcule o carimbo de hora de saída de acordo.

Se os exemplos de entrada não contiverem carimbos de data/hora:

-   O decodificador deve gerar seus próprios carimbos de data/hora, definindo o primeiro carimbo de hora de saída como zero.
-   A duração da amostra é calculada a partir do número de amostras de saída no buffer e da taxa de amostra.
-   Carimbos de data/hora subsequentes são calculados do carimbo de data/hora anterior: carimbo de data/hora atual + duração atual = próximo carimbo de data/hora. Não deve haver lacunas nos carimbos de data/hora de saída.

Se o fluxo de entrada contiver inicialmente carimbos de data/hora, mas, por algum motivo, mudar para nenhum carimbo de data/hora, o decodificador deverá continuar a gerar seus próprios carimbos de hora de saída, de modo que eles sejam contínuos e não haja nenhum intervalo

Se o fluxo de entrada contiver carimbos de data/hora, mas houver lacunas nos horários, o decodificador simplesmente propagará essas lacunas. Em outras palavras, o decodificador não deve tentar corrigir carimbos de data/hora inconsistentes no fluxo de entrada.

### <a name="mixers"></a>Mixers

> [!Note]  
> no Windows Vista, o pipeline de Media Foundation não oferece suporte a MFTs com mais de uma entrada. há suporte para MFTs de várias entradas no Windows 7.

 

Um mixer usa várias entradas e as combina em uma saída. Se os fluxos de entrada não forem completamente bloqueados por taxas ou forem ligeiramente deslocados no tempo uns dos outros, poderá haver ambiguidade sobre qual tempo deve ser definido na saída. Aqui estão algumas diretrizes, dependendo do tipo de mídia:

-   Sonoro. Na inicialização ou imediatamente após uma descarga ou liberação, um mixer de áudio deve aguardar para produzir amostras de saída até receber uma amostra de entrada em todos os fluxos de entrada necessários. Nesse ponto, ele deve escolher o carimbo de data/hora mais antigo dos exemplos iniciais para usar como uma linha de base para os carimbos de data/hora de saída. Os outros fluxos devem ser preenchidos com silêncio para fazer qualquer discrepância de tempo. Se um exemplo for recebido em um fluxo de entrada opcional, ele também deverá ser acrescentado ao cálculo. Desse ponto em diante, o MFT deve se esforçar para produzir uma cadeia contínua e não quebrada de carimbos de hora de saída. Em geral, o MFT não deve tentar considerar uma descompasso de fluxo em relação a outra. Em vez disso, ele deve calcular os carimbos de hora de saída do carimbo de data/hora de linha de base, a taxa de saída e os tamanhos de buffer. Quando outro dreno ou liberação ocorre, o MFT deve redefinir seus carimbos de data/hora de linha de base.

-   Vídeo. Na inicialização ou imediatamente após uma descarga ou liberação, um mixer de vídeo deve aguardar para produzir amostras de saída até receber uma amostra de entrada em todos os fluxos de entrada necessários. Nesse ponto, ele deve escolher o carimbo de data/hora mais antigo dos exemplos iniciais para usar como uma linha de base para os carimbos de data/hora de saída. Em geral, ele deve se esforçar para manter carimbos de hora de saída contínuos e regulares e durações fixas, mesmo que a entrada não seja tão regular, se necessário, repetindo quadros de entrada.

### <a name="encoders"></a>Codificadores

Um codificador converte áudio ou vídeo descompactado em pacotes compactados. Um codificador deve seguir estas diretrizes:

-   O codificador deve seguir as convenções do formato de saída. Se o formato normalmente não carimbar o tempo de cada amostra, como em MPEG-2, nem todos os exemplos de saída precisam ter um carimbo de data/hora e uma duração.

-   Os carimbos de data/hora de entrada devem ser preservados no formato de saída, se o formato tiver campos para carimbos de data/hora, a menos que as informações de melhor hora estejam disponíveis de outra fonte, como o próprio aplicativo.

### <a name="multiplexers"></a>Multiplexadores

> [!Note]  
> no Windows Vista, o pipeline de Media Foundation não oferece suporte a MFTs com mais de uma entrada. há suporte para MFTs de várias entradas no Windows 7.

 

Um multiplexador combina dois fluxos de áudio ou vídeo diferentes em um formato intercalado, como o fluxo de transporte AVI ou MPEG-2. Um multiplexador deve seguir estas diretrizes:

-   O multiplexador deve seguir as convenções do formato de saída. Se o formato normalmente não carimbar o tempo de cada amostra, como em MPEG-2, nem todos os exemplos de saída precisam ter um carimbo de data/hora e uma duração.

-   O carimbo de data/hora deve refletir a hora mais antiga que seria colocada em qualquer quadro que começa nesse pacote ou a hora do primeiro exemplo de áudio que seria decodificada a partir desse pacote. Ignore essa diretriz se ela entrar em conflito com as convenções do formato de saída.

### <a name="demultiplexers"></a>Demultiplexadores

Um demultiplexador divide um formato intercalado, como o fluxo de transporte AVI ou MPEG-2, nos fluxos de áudio e vídeo subjacentes.

Se o formato contiver informações de carimbo de data/hora específicas que podem ser usadas para calcular carimbos de tempo de saída precisos com base nos carimbos de data/hora, essas informações deverão ser usadas. No entanto, se o formato contiver vezes em uma base completamente diferente que não tenha nenhuma relação com os carimbos de data/hora de entrada, e um deslocamento preciso para o carimbo de data/hora de entrada não puder ser calculado, os tempos próprios do formato deverão ser ignorados.

Se o formato não tiver informações de carimbo de data/hora utilizáveis, o demultiplexador deverá seguir estas regras:

-   Fluxos de saída não compactados devem ter carimbos de data e durações válidos, se possível, calculados a partir do carimbo de data/hora de entrada anterior mais próximo.

-   Fluxos de saída compactados devem ter carimbos de data/hora somente no primeiro exemplo de saída derivado de um exemplo de entrada com um carimbo de data/hora. Se a amostra de entrada não tiver um carimbo de data/hora, nenhuma amostra de saída derivada desse exemplo de entrada deverá ter um carimbo de data/hora. Se o exemplo de entrada for dividido em vários exemplos de saída, somente o primeiro exemplo de saída deverá ter um carimbo de data/hora e o restante não deverá ter carimbos de data/hora.

### <a name="examples"></a>Exemplos

Exemplo 1. Suponha que um efeito de vídeo sempre assuma um quadro de entrada descompactado, aplique o efeito e o copie para a saída. Ele nunca retorne nenhum quadro ou buffers qualquer entrada. Essa MFT simplesmente copia o carimbo de data/hora e a duração do exemplo de entrada para o exemplo de saída, se eles estiverem disponíveis, e não houver nenhum cálculo de tempo.

Exemplo 2. Suponha que um efeito de áudio transforme todos, exceto 10 milissegundos (MS) de cada buffer de entrada, economizando 10 ms extra para combinar com o próximo buffer. Ele obtém um fluxo de exemplos que têm uma duração de 50 ms. Os tempos de entrada são mostrados na tabela a seguir.



| Amostra | Tempo de entrada | Duração da entrada | Tempo de saída | Duração da saída |
|--------|------------|----------------|-------------|-----------------|
| 1      | 20         | 50             | 20          | 40              |
| 2      | 70         | 50             | 60          | 50              |
| 3      | 121        | 50             | 110         | 50              |
| 4      | 171        | 50             | 161         | 50              |



 

Observe a discrepância de 1 ms entre a duração real da amostra 2 e a duração implícita com base no próximo carimbo de data/hora (121 ? 70 = 51).

Como o MFT mantém 10 ms, ele realiza a saída dos primeiros 40 ms da amostra de entrada 1 como exemplo de saída 1, com um carimbo de data/hora de 20 ms e uma duração de 40 ms.

A amostra de saída 2 combina os 10 ms anteriormente mantidos com 40 ms da amostra de entrada 2. Este exemplo recebe um carimbo de data/hora de 60 ms (o carimbo de data/hora do exemplo de entrada anterior, 20 ms, mais a duração dos dados já processados desse exemplo, 40 ms). Ele recebe uma duração de 50 ms.

Da mesma forma, a próxima amostra tem um carimbo de data/hora de 110 ms (70 ms + 40 ms) com uma duração de 50 ms.

O próximo cálculo é mais interessante. O carimbo de data/hora implícito da hora e da duração da saída anterior seria de 160 ms (carimbo de data/hora 110 ms + duração de 50 ms). No entanto, o carimbo de data/hora de saída deve ser calculado com base no carimbo de data/hora de entrada do exemplo de entrada mais antigo que sobrepõe a amostra de saída no tempo, mais o comprimento de todos os dados já processados desse exemplo. A amostra de entrada sobreposta mais próxima é a amostra 4 (carimbo de data/hora = 171), mas essa não é a mais antiga. A amostra de sobreposição mais antiga é a amostra 3 (carimbo de data/hora = 121). Adicionando os 40 ms que já foram processados desse exemplo, o resultado é 161.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Escrevendo um MFT personalizado](writing-a-custom-mft.md)
</dt> </dl>

 

 



