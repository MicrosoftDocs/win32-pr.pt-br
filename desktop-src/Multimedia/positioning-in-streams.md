---
title: Posicionamento em Fluxos
description: Posicionamento em Fluxos
ms.assetid: 97ab491d-1a58-4b4b-a13a-215be24dac1c
keywords:
- Função AVIStreamStart
- Função AVIStreamFindSample
- Função AVIStreamSampleToTime
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0528fea9ea10e28a418d253bd1abe6c599a952fe95a8c8f6c86807abe0e41159
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119805856"
---
# <a name="positioning-in-streams"></a>Posicionamento em Fluxos

O AVIFile fornece várias maneiras de localizar e mover para uma posição em um fluxo de dados. As funções e macros nesta seção permitem que seu aplicativo encontre a posição inicial, o comprimento e os quadros-chave (contendo uma imagem completa no exemplo) dentro de um fluxo. As funções e macros também associam o tempo às posições em um fluxo calculando o tempo decorrido necessário para reproduzir um fluxo do início para qualquer ponto em um fluxo.

## <a name="finding-the-starting-position"></a>Encontrando a posição inicial

Você pode recuperar o número de exemplo do primeiro quadro em um fluxo de vídeo usando a [**função AVIStreamStart.**](/windows/desktop/api/Vfw/nf-vfw-avistreamstart) (Os quadros de um filme podem começar no exemplo 0 ou 1, dependendo da preferência do autor.) Você também pode obter essas informações usando a [**função AVIStreamInfo.**](/windows/desktop/api/Vfw/nf-vfw-avistreaminfoa) Essa função armazena o número de exemplo no **membro dwStart** da [**estrutura AVISTREAMINFO.**](/windows/desktop/api/Vfw/ns-vfw-avistreaminfoa) Você pode recuperar a hora de início do primeiro exemplo de um fluxo usando a [**macro AVIStreamStartTime.**](/windows/desktop/api/Vfw/nf-vfw-avistreamstarttime)

Você pode recuperar o comprimento do fluxo usando a [**função AVIStreamLength.**](/windows/desktop/api/Vfw/nf-vfw-avistreamlength) Essa função retorna o número de amostras no fluxo. Você também pode obter essas informações usando a **função AVIStreamInfo.** Essa função armazena o comprimento do fluxo no **membro dwLength** da **estrutura AVISTREAMINFO.** Para recuperar o comprimento de um fluxo em milissegundos, use a macro [**AVIStreamLengthTime.**](/windows/desktop/api/Vfw/nf-vfw-avistreamlengthtime)

Em um fluxo de vídeo, cada amostra geralmente corresponde a um quadro de vídeo. No entanto, pode haver exemplos para os quais nenhum dado de vídeo está presente. Se você chamar a [**função AVIStreamRead**](/windows/desktop/api/Vfw/nf-vfw-avistreamread) especificando uma dessas posições, ela retornará um comprimento de dados de 0 bytes. Você pode encontrar exemplos que contêm dados usando a [**função AVIStreamFindSample**](/windows/desktop/api/Vfw/nf-vfw-avistreamfindsample) e especificando o sinalizador FIND \_ ANY.

Em um fluxo de áudio, cada amostra corresponde a um bloco de dados de dados de áudio. Por exemplo, se os dados de áudio têm um formato ADPCM de 22 kHz (Modularidade de Código de Pulso Diferencial Adaptável), cada amostra de **AVIStreamLength** corresponde a um bloco de 256 bytes de dados de áudio compactados. Esse bloco de dados de áudio contém aproximadamente 500 amostras de áudio quando descompactados. As funções e macros de AVIFile, no entanto, tratam cada bloco de 256 byte como um único exemplo.

> [!Note]  
> Posições válidas dentro de um intervalo de fluxo do início ao final do fluxo, que é a soma do ponto de partida do fluxo e seu comprimento. A posição representada pela soma da posição inicial e o comprimento correspondem a um tempo após os últimos dados ter sido renderizados; ele não contém nenhum dado. Você pode recuperar o número de exemplo que representa o final do fluxo usando a [**macro AVIStreamEnd.**](/windows/desktop/api/Vfw/nf-vfw-avistreamend) Você pode recuperar o valor temporal em milissegundos que representa o final do fluxo usando a [**macro AVIStreamEndTime.**](/windows/desktop/api/Vfw/nf-vfw-avistreamendtime)

 

## <a name="finding-sample-and-key-frames"></a>Localizar exemplos e quadros-chave

Você pode pesquisar diferentes tipos de amostras em um fluxo usando a [**função AVIStreamFindSample.**](/windows/desktop/api/Vfw/nf-vfw-avistreamfindsample) Essa função pesquisa para trás ou para frente por meio de um fluxo para um exemplo do tipo apropriado, começando com o número de exemplo especificado. Você pode pesquisar diferentes tipos de exemplos em um fluxo especificando um sinalizador na sequência de chamada **AVIStreamFindSample.** Especifique \_ o sinalizador FIND ANY para localizar amostras nãompty ou para ignorar exemplos que não têm dados. Especifique o sinalizador FIND KEY para pesquisar quadros-chave que contenham os dados para renderizar uma imagem completa sem a necessidade de \_ referenciar quadros anteriores. Especifique o \_ sinalizador FIND FORMAT para pesquisar alterações no formato. **AVIStreamFindSample** é usado principalmente com fluxos de vídeo.

Várias macros que usam funções AVIFile complementam os recursos de pesquisa de fluxo. A lista a seguir fornece uma breve descrição de cada macro. As macros que pesquisam uma posição específica ou um tipo de dados exigem que um local inicial seja especificado no fluxo.



| Macro                                                                | Descrição                                                                                                                 |
|----------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [**AVIStreamIsKeyFrame**](/windows/desktop/api/Vfw/nf-vfw-avistreamiskeyframe)                   | Indica se um exemplo em um fluxo especificado é um quadro-chave.                                                            |
| [**AVIStreamNekeyFrame**](/windows/desktop/api/Vfw/nf-vfw-avistreamnearestkeyframe)         | Localiza o quadro-chave em ou antes de uma posição especificada em um fluxo.                                                     |
| [**AVIStreamNekeyFrameTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamnearestkeyframetime) | Determina a hora correspondente ao início do quadro-chave mais próximo (ou anterior) de uma hora especificada em um fluxo. |
| [**AVIStreamNestreamSample**](/windows/desktop/api/Vfw/nf-vfw-avistreamnearestsample)             | Localiza a amostra sem valor mais próxima em ou antes de uma posição especificada em um fluxo.                                       |
| [**AVIStreamNestreamSampleTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamnearestsampletime)     | Determina o tempo correspondente ao início de uma amostra mais próxima de um horário especificado em um fluxo.             |
| [**AVIStreamNextKeyFrame**](/windows/desktop/api/Vfw/nf-vfw-avistreamnextkeyframe)               | Localiza o próximo quadro-chave após uma posição especificada em um fluxo.                                                      |
| [**AVIStreamNextKeyFrameTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamnextkeyframetime)       | Retorna a hora do próximo quadro-chave em um fluxo, começando em um determinado momento.                                               |
| [**AVIStreamNextSample**](/windows/desktop/api/Vfw/nf-vfw-avistreamnextsample)                   | Localiza a próxima amostra sem valor de uma posição especificada em um fluxo.                                                     |
| [**AVIStreamNextSampleTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamnextsampletime)           | Retorna a hora em que um exemplo muda para o próximo exemplo no fluxo.                                                    |
| [**AVIStreamPrevKeyFrame**](/windows/desktop/api/Vfw/nf-vfw-avistreamprevkeyframe)               | Localiza o quadro-chave que precede uma posição especificada em um fluxo.                                                       |
| [**AVIStreamPrevKeyFrameTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamprevkeyframetime)       | Retorna a hora do quadro-chave anterior no fluxo, começando em um determinado momento.                                         |
| [**AVIStreamPrevSample**](/windows/desktop/api/Vfw/nf-vfw-avistreamprevsample)                   | Localiza o exemplo sem valor que precede uma posição especificada em um fluxo.                                                 |
| [**AVIStreamPrevSampleTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamprevsampletime)           | Determina a hora em que o exemplo anterior substitui seu antecessor no fluxo.                                    |
| [**AVIStreamSampleToSample**](/windows/desktop/api/Vfw/nf-vfw-avistreamsampletosample)           | Retorna o exemplo em um fluxo que ocorre ao mesmo tempo que um exemplo que ocorre em um segundo fluxo.                     |



 

## <a name="switching-between-samples-and-time"></a>Alternando entre exemplos e tempo

Você pode determinar o tempo decorrido do início de um fluxo para um exemplo usando a [**função AVIStreamSampleToTime.**](/windows/desktop/api/Vfw/nf-vfw-avistreamsampletotime) Essa função converte o número de exemplo em um valor de tempo expresso em milissegundos. Para um quadro de vídeo (que abrange vários milissegundos), esse valor representa a hora em que o exemplo começa a ser reproduzir desde o início da reprodução e pressupo que o clipe de vídeo é reproduzindo em velocidade normal. Para um exemplo de áudio (que tem várias amostras em um milissegundo), o valor de tempo corresponde à hora em que o exemplo começa a ser reproduzindo e pressupondo que o fluxo de áudio seja reproduzindo em velocidade normal.

Por outro lado, você pode encontrar o número de exemplo associado a um valor temporal usando a [**função AVIStreamTimeToSample.**](/windows/desktop/api/Vfw/nf-vfw-avistreamtimetosample) Essa função converte o valor de milissegundo em um número de exemplo e assume que o clipe de vídeo é reproduzida em velocidade normal.

Como **AVIStreamSampleToTime** retorna a hora em que um quadro começa a ser reproduzida, a relação entre **AVIStreamSampleToTime** e **AVIStreamTimeToSample** não é realmente inversa. Eles determinam a posição em um arquivo de forma mais acurada do que determinam o tempo. Por exemplo, dois exemplos de áudio consecutivos podem ser reproduzir no mesmo milissegundo. Usar **AVIStreamSampleToTime** para converter os números de exemplo resultaria em valores de tempo idênticos. Se você converter o valor temporal de volta em um número de exemplo usando **AVIStreamTimeToSample,** uma única amostra será referenciada.

 

 




