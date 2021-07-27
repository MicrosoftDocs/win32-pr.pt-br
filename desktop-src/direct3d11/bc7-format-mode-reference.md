---
title: Referência do modo de formato BC7
description: Esta documentação contém uma lista de 8 modos de bloqueio e alocações de bits para blocos de formato de compactação de textura BC7.
ms.assetid: B1CEB729-6694-49BF-ACB9-FD1EFAB0B0D1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9756582d7d5ac52d4c16b2f4734decebbd66ae8
ms.sourcegitcommit: 5a78723ad484955ac91a23cf282cf9c176c1eab6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/22/2021
ms.locfileid: "114436101"
---
# <a name="bc7-format-mode-reference"></a>Referência do modo de formato BC7

Esta documentação contém uma lista de 8 modos de bloqueio e alocações de bits para blocos de formato de compactação de textura BC7.

As cores para cada subconjunto dentro de um bloco são representadas por duas cores de ponto de extremidade explícitas e um conjunto de cores interpoladas entre elas. Dependendo da precisão de índice do bloco, cada subconjunto pode ter 4, 8 ou 16 cores possíveis.

-   [Modo 0](#mode-0)
-   [Modo 1](#mode-1)
-   [Modo 2](#mode-2)
-   [Modo 3](#mode-3)
-   [Modo 4](#mode-4)
-   [Modo 5](#mode-5)
-   [Modo 6](#mode-6)
-   [Modo 7](#mode-7)
-   [Comentários](#remarks)
-   [Tópicos relacionados](#related-topics)

## <a name="mode-0"></a>Modo 0

O modo 0 do BC7 tem as seguintes características:

-   Componentes de cor apenas (nenhum alfa)
-   3 subconjuntos por bloco
-   Pontos de extremidade RGBP 4.4.4.1 com um bit P exclusivo por ponto de extremidade
-   índices de 3 bits
-   16 partições

![Layout de bit do modo 0](images/bc7-mode0.png)

## <a name="mode-1"></a>Modo 1

O modo 1 do BC7 tem as seguintes características:

-   Componentes de cor apenas (nenhum alfa)
-   2 subconjuntos por bloco
-   Pontos de extremidade RGBP 6.6.6.1 com um bit P compartilhado por subconjunto)
-   índices de 3 bits
-   64 partições

![Layout de bit do modo 1](images/bc7-mode1.png)

## <a name="mode-2"></a>Modo 2

O modo 2 do BC7 tem as seguintes características:

-   Componentes de cor apenas (nenhum alfa)
-   3 subconjuntos por bloco
-   Pontos de extremidade RGB 5.5.5
-   índices de 2 bits
-   64 partições

![Layout de bit do modo 2](images/bc7-mode2.png)

## <a name="mode-3"></a>Modo 3

O modo 3 do BC7 tem as seguintes características:

-   Componentes de cor apenas (nenhum alfa)
-   2 subconjuntos por bloco
-   Pontos de extremidade RGBP 7.7.7.1 com um bit P único por subconjunto)
-   índices de 2 bits
-   64 partições

![Layout de bit do modo 3](images/bc7-mode3.png)

## <a name="mode-4"></a>Modo 4

O modo 4 do BC7 tem as seguintes características:

-   Componentes de cor com o componente alfa separado
-   1 subconjunto por bloco
-   pontos de extremidade de cor RGB 5.5.5
-   pontos de extremidade alfa 6 bits
-   índices de 16 x 2 bits
-   índices de 16 x 3 bits
-   rotação de componente de 2 bits
-   seletor de índice de 1 bit (se os índices de 2 ou 3 bits forem usados)

![layout de bit do modo 4](images/bc7-mode4.png)

## <a name="mode-5"></a>Modo 5

O modo 5 do BC7 tem as seguintes características:

-   Componentes de cor com o componente alfa separado
-   1 subconjunto por bloco
-   pontos de extremidade de cor RGB 7.7.7
-   pontos de extremidade alfa de 8 bits
-   índices de cores de 16 x 2 bits
-   índices alfa de 16 x 2 bits
-   rotação de componente de 2 bits

![Layout de bit do modo 5](images/bc7-mode5.png)

## <a name="mode-6"></a>Modo 6

O modo 6 do BC7 tem as seguintes características:

-   Componentes de cor e alfa combinados
-   Um subconjunto por bloco
-   Pontos de extremidade de cor RGBAP 7.7.7.7.1 (e alfa) (bit P exclusivo por ponto de extremidade)
-   índices de 16 x 4 bits

![layout de bit do modo 6](images/bc7-mode6.png)

## <a name="mode-7"></a>Modo 7

O modo 7 do BC7 tem as seguintes características:

-   Componentes de cor e alfa combinados
-   2 subconjuntos por bloco
-   Pontos de extremidade de cor RGBAP 5.5.5.5.1 (e alfa) (bit P exclusivo por ponto de extremidade)
-   índices de 2 bits
-   64 partições

![layout de bit do modo 7](images/bc7-mode7.png)

## <a name="remarks"></a>Comentários

O modo 8 (o byte menos significativo está definido como 0x00) é reservado. Não use-o em seu codificador. Se você passar esse modo para o hardware, será retornado um bloco inicializado para todos os zeros.

No BC7, você pode codificar o componente alfa de uma das seguintes maneiras:

-   Tipos de bloco sem codificação explícita de componente alfa. Nesses blocos, os pontos de extremidade de cor têm uma codificação somente RGB, com o componente alfa decodificado em 1.0 para todos os texels.
-   Os tipos de bloco com componentes de cor e alfa combinados. Nesses blocos, os valores de cor de ponto de extremidade são especificados no formato RGBA, e os valores de componente alfa são interpolados juntamente com os valores de cor.
-   Os tipos de bloco com componentes de cor e alfa separados. Nesses blocos, os valores de cor e alfa são especificados separadamente, cada um com seu próprio conjunto de índices. Como resultado, eles têm um vetor efetivo e um canal escalar com codificação separada, em que o vetor normalmente especifica os canais de cor \[ R, G, B \] e escalar especifica o canal alfa \[ a \] . Para dar suporte a essa abordagem, um campo de 2 bits separado é fornecido na codificação, que permite a especificação da codificação de canal separado como um valor escalar. Como resultado, o bloco pode ter uma das quatro representações diferentes a seguir dessa codificação alfa (conforme indicado pelo campo de 2 bits):
    -   RGB \| A: canal alfa separado
    -   AGB \| R: canal de cores "vermelho" separado
    -   RAB \| G: canal de cores "verde" separado
    -   RGA \| B: canal de cores "azul" separado

    O decodificador reordena a ordem de canal para RGBA após a decodificação, portanto, o formato de bloco interno é invisível para o desenvolvedor. Blocos com cores separadas e componentes alfa também têm dois conjuntos de dados de índice: um para o conjunto vetorado de canais e outro para o canal escalar. (No caso do Modo 4, esses índices têm larguras diferentes \[ de 2 ou 3 \] bits. O modo 4 também contém um seletor de 1 bit que especifica se o vetor ou o canal escalar usa os índices de 3 bits.)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Formato BC7](bc7-format.md)
</dt> </dl>

 

 




