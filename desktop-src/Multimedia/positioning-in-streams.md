---
title: Posicionamento em fluxos
description: Posicionamento em fluxos
ms.assetid: 97ab491d-1a58-4b4b-a13a-215be24dac1c
keywords:
- Função AVIStreamStart
- Função AVIStreamFindSample
- Função AVIStreamSampleToTime
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5252aa938d32c323da9fcf7ae106d11db0ff2fb4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635690"
---
# <a name="positioning-in-streams"></a>Posicionamento em fluxos

O AVIFile fornece várias maneiras de localizar e mover para uma posição em um fluxo de dados. As funções e macros nesta seção permitem que seu aplicativo localize a posição inicial, o comprimento e os quadros-chave (contendo uma imagem completa no exemplo) em um fluxo. As funções e macros também associam a hora com posições em um fluxo, calculando o tempo decorrido necessário para reproduzir um fluxo desde o início até qualquer ponto em um fluxo.

## <a name="finding-the-starting-position"></a>Localizando a posição inicial

Você pode recuperar o número de exemplo do primeiro quadro em um fluxo de vídeo usando a função [**AVIStreamStart**](/windows/desktop/api/Vfw/nf-vfw-avistreamstart) . (Os quadros de um filme podem começar no exemplo 0 ou 1, dependendo da preferência do autor.) Você também pode obter essas informações usando a função [**AVIStreamInfo**](/windows/desktop/api/Vfw/nf-vfw-avistreaminfoa) . Essa função armazena o número de exemplo no membro **dwStart** da estrutura [**AVISTREAMINFO**](/windows/desktop/api/Vfw/ns-vfw-avistreaminfoa) . Você pode recuperar a hora de início da primeira amostra de um fluxo usando a macro [**AVIStreamStartTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamstarttime) .

Você pode recuperar o tamanho do fluxo usando a função [**AVIStreamLength**](/windows/desktop/api/Vfw/nf-vfw-avistreamlength) . Essa função retorna o número de amostras no fluxo. Você também pode obter essas informações usando a função **AVIStreamInfo** . Essa função armazena o tamanho do fluxo no membro **dwLength** da estrutura **AVISTREAMINFO** . Para recuperar o comprimento de um fluxo em milissegundos, use a macro [**AVIStreamLengthTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamlengthtime) .

Em um fluxo de vídeo, cada exemplo geralmente corresponde a um quadro de vídeo. No entanto, pode haver exemplos para os quais não há dados de vídeo presentes. Se você chamar a função [**AVIStreamRead**](/windows/desktop/api/Vfw/nf-vfw-avistreamread) especificando uma dessas posições, ela retornará um comprimento de dados de 0 bytes. Você pode encontrar exemplos que contenham dados usando a função [**AVIStreamFindSample**](/windows/desktop/api/Vfw/nf-vfw-avistreamfindsample) e especificando o \_ sinalizador localizar qualquer.

Em um fluxo de áudio, cada amostra corresponde a um bloco de dados de dados de áudio. Por exemplo, se os dados de áudio tiverem um formato de 22 kHz ADPCM (modulação diferencial de código de pulso), cada exemplo para **AVIStreamLength** corresponderá a um bloco de 256 bytes de dados de áudio compactados. Esse bloco de dados de áudio contém aproximadamente 500 amostras de áudio quando não compactados. As funções e macros de AVIFile, no entanto, tratam cada bloco de 256 bytes como um único exemplo.

> [!Note]  
> Posições válidas dentro de um intervalo de fluxo desde o início até o fim do fluxo, que é a soma do ponto de partida do fluxo e seu comprimento. A posição representada pela soma da posição inicial e o comprimento corresponde a uma hora após a renderização dos últimos dados; Ele não contém nenhum dado. Você pode recuperar o número de exemplo que representa o final do fluxo usando a macro [**AVIStreamEnd**](/windows/desktop/api/Vfw/nf-vfw-avistreamend) . Você pode recuperar o valor de tempo em milissegundos que representa o final do fluxo usando a macro [**AVIStreamEndTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamendtime) .

 

## <a name="finding-sample-and-key-frames"></a>Localizando amostras e quadros-chave

Você pode Pesquisar tipos diferentes de exemplos em um fluxo usando a função [**AVIStreamFindSample**](/windows/desktop/api/Vfw/nf-vfw-avistreamfindsample) . Essa função pesquisa para trás ou para frente por meio de um fluxo para uma amostra do tipo apropriado, começando pelo número de exemplo que você especificar. Você pode Pesquisar tipos diferentes de exemplos em um fluxo especificando um sinalizador na sequência de chamada **AVIStreamFindSample** . Especifique o \_ sinalizador localizar qualquer para localizar amostras não vazias ou ignorar exemplos que não têm dados. Especifique o \_ sinalizador localizar chave para procurar quadros-chave que contêm os dados para renderizar uma imagem completa sem precisar fazer referência a quadros anteriores. Especifique o \_ sinalizador Localizar formato para procurar alterações no formato. **AVIStreamFindSample** é usado principalmente com fluxos de vídeo.

Várias macros que usam funções AVIFile complementam os recursos de pesquisa de fluxo. A lista a seguir fornece uma breve descrição de cada macro. As macros que pesquisam uma posição ou tipo de dados específico exigem um local inicial a ser especificado no fluxo.



| Macro                                                                | Description                                                                                                                 |
|----------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [**AVIStreamIsKeyFrame**](/windows/desktop/api/Vfw/nf-vfw-avistreamiskeyframe)                   | Indica se um exemplo em um fluxo especificado é um quadro-chave.                                                            |
| [**AVIStreamNearestKeyFrame**](/windows/desktop/api/Vfw/nf-vfw-avistreamnearestkeyframe)         | Localiza o quadro-chave em uma posição especificada ou anterior em um fluxo.                                                     |
| [**AVIStreamNearestKeyFrameTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamnearestkeyframetime) | Determina o tempo correspondente ao início do quadro de chave mais próximo (em ou anterior) uma hora especificada em um fluxo. |
| [**AVIStreamNearestSample**](/windows/desktop/api/Vfw/nf-vfw-avistreamnearestsample)             | Localiza a amostra mais próxima não vazia na posição especificada ou anterior em um fluxo.                                       |
| [**AVIStreamNearestSampleTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamnearestsampletime)     | Determina o tempo correspondente ao início de uma amostra que é mais próxima de um tempo especificado em um fluxo.             |
| [**AVIStreamNextKeyFrame**](/windows/desktop/api/Vfw/nf-vfw-avistreamnextkeyframe)               | Localiza o próximo quadro-chave após uma posição especificada em um fluxo.                                                      |
| [**AVIStreamNextKeyFrameTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamnextkeyframetime)       | Retorna a hora do próximo quadro chave em um fluxo, começando em um determinado momento.                                               |
| [**AVIStreamNextSample**](/windows/desktop/api/Vfw/nf-vfw-avistreamnextsample)                   | Localiza a próxima amostra não vazia de uma posição especificada em um fluxo.                                                     |
| [**AVIStreamNextSampleTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamnextsampletime)           | Retorna a hora em que um exemplo é alterado para o próximo exemplo no fluxo.                                                    |
| [**AVIStreamPrevKeyFrame**](/windows/desktop/api/Vfw/nf-vfw-avistreamprevkeyframe)               | Localiza o quadro-chave que precede uma posição especificada em um fluxo.                                                       |
| [**AVIStreamPrevKeyFrameTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamprevkeyframetime)       | Retorna a hora do quadro de chave anterior no fluxo, começando em um determinado momento.                                         |
| [**AVIStreamPrevSample**](/windows/desktop/api/Vfw/nf-vfw-avistreamprevsample)                   | Localiza a amostra não vazia que precede uma posição especificada em um fluxo.                                                 |
| [**AVIStreamPrevSampleTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamprevsampletime)           | Determina a hora na qual o exemplo anterior substitui seu antecessor no fluxo.                                    |
| [**AVIStreamSampleToSample**](/windows/desktop/api/Vfw/nf-vfw-avistreamsampletosample)           | Retorna o exemplo em um fluxo que ocorre ao mesmo tempo que um exemplo que ocorre em um segundo fluxo.                     |



 

## <a name="switching-between-samples-and-time"></a>Alternando entre exemplos e hora

Você pode determinar o tempo decorrido desde o início de um fluxo até um exemplo usando a função [**AVIStreamSampleToTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamsampletotime) . Essa função converte o número de exemplo em um valor de hora expresso em milissegundos. Para um quadro de vídeo (que abrange vários milissegundos), esse valor representa o tempo que o exemplo começa a reproduzir desde que a reprodução começou e assume que o clipe de vídeo é reproduzido em velocidade normal. Para um exemplo de áudio (que tem várias amostras em um milissegundo), o valor de tempo corresponde à hora em que o exemplo começa a ser reproduzido e assume que o fluxo de áudio é reproduzido em velocidade normal.

Por outro lado, você pode encontrar o número de exemplo associado a um valor de hora usando a função [**AVIStreamTimeToSample**](/windows/desktop/api/Vfw/nf-vfw-avistreamtimetosample) . Essa função converte o valor de milissegundo em um número de exemplo e assume que o clipe de vídeo é reproduzido em velocidade normal.

Como **AVIStreamSampleToTime** retorna a hora em que um quadro começa a ser reproduzido, a relação entre **AVIStreamSampleToTime** e **AVIStreamTimeToSample** não é realmente inversa. Eles determinam a posição em um arquivo mais acurately do que determinam o tempo. Por exemplo, dois exemplos de áudio consecutivos podem ser executados no mesmo milissegundo. O uso de **AVIStreamSampleToTime** para converter os números de exemplo resultaria em valores de tempo idênticos. Se você converter o valor de tempo de volta para um número de exemplo usando **AVIStreamTimeToSample**, um único exemplo será referenciado.

 

 




