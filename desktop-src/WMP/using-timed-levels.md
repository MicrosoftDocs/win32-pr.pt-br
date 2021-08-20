---
title: Usando níveis de tempo
description: Usando níveis de tempo
ms.assetid: 4a253521-3036-488a-98bc-62596b538f68
keywords:
- visualizações, eventos cronometrados
- visualizações personalizadas, eventos cronometrados
- visualizações, matriz de frequência
- visualizações personalizadas, matriz de frequência
- visualizações, matriz de formato de onda
- visualizações personalizadas, matriz de formato de onda
- visualizações, variável de estado
- visualizações personalizadas, variável de estado
- visualizações, variável timeStamp
- visualizações personalizadas, variável timeStamp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e6ce4d675fa37a519952f1b31d3c52cd93005a82eef977b7bd7d77623f1e508
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118116933"
---
# <a name="using-timed-levels"></a>Usando níveis de tempo

A estrutura **TimedLevel** é composta de matrizes 2 2-dimensional, um valor de estado e um valor de carimbo de data/hora.

## <a name="frequency-array"></a>Matriz de frequência

A matriz Frequency é uma matriz bidimensional. A primeira dimensão de cada matriz corresponde ao canal de áudio estéreo (esquerda ou direita) e a segunda corresponde aos níveis de frequência (em bytes) do instantâneo, onde o espectro de áudio é dividido em regiões de 1024.

você pode obter os dados da matriz de frequência fornecidos pelo Windows Media Player da seguinte maneira:


```C++
TimedLevel *pLevels;
int snapshot = pLevels->frequency[0][0];
```



O valor de instantâneo é para o canal esquerdo e contém o valor da parte mais baixa do espectro de frequência. Por exemplo, se o instantâneo tiver um valor grande, ele indica que a parte mais baixa da 1024th do espectro de frequência é avançada em frequência. Um valor de zero indica que não há valores de frequência baixa nessa parte do espectro para o canal esquerdo. Se você tiver um sinal de monotelephony, somente a primeira dimensão terá valores válidos.

Se o sinal for não estéreo, a segunda matriz conterá uma cópia do sinal mono. Ou seja, \[ a frequência 0 \] \[ *n* \] e \[ a frequência 1 \] \[ *n* \] conterão os mesmos dados, em que *n* é o índice em uma determinada célula.

## <a name="waveform-array"></a>Matriz de formato de onda

A matriz de formato de onda também é uma matriz bidimensional. A primeira dimensão da matriz corresponde ao canal (esquerda ou direita) e a segunda corresponde aos níveis de energia (em bytes) do instantâneo, onde a energia de áudio é dividida em 1024 segmentos de tempo contíguos.

você pode obter os dados da matriz de forma de onda de Windows Media Player da seguinte maneira:


```C++
TimedLevel *pLevels;
int snapshot = pLevels->waveform[0][0];

```



O valor de instantâneo é para o canal esquerdo e contém o primeiro valor do instantâneo quantificado dos valores de energia. Quando um instantâneo é obtido, ele consiste em 1024 pequenas medidas incrementais da potência de áudio. O valor mais baixo da matriz é gerado pela primeira medida incremental de energia de áudio. Observe que os valores da potência são medidos de-128 a + 127, mas os valores na matriz variam de 0 a 255. Se você tiver uma onda de telefonia, somente a primeira dimensão terá valores válidos.

Se o sinal for não estéreo, a segunda matriz conterá uma cópia do sinal mono. Ou seja, Wave \[ 0 \] \[ *n* \] e forma de onda \[ 1 \] \[ *n* \] conterão os mesmos dados, em que *n* é o índice em uma determinada célula.

## <a name="state"></a>Estado

A variável de estado reflete o estado de reprodução de áudio de Windows Media Player. Os valores de enumeração do Playerstate são


```C++
    stop_state              = 0,    // audio is currently stopped
    pause_state             = 1,    // audio is currently paused
    play_state              = 2     // audio is currently playing

```



Você pode usar essa variável para executar ações diferentes dependendo do estado de reprodução de áudio. Por exemplo, você pode reproduzir um tipo de visualização quando o áudio estiver sendo reproduzido e outro quando for interrompido.

## <a name="time-stamp"></a>Carimbo de Data/Hora

A variável timeStamp reflete a hora atual em que o instantâneo é tirado. Isso pode ser usado para medir a frequência com que os instantâneos são obtidos.

Você pode usar essa variável para cronometrar suas animações. Se os instantâneos forem muito frequentes, você poderá degradar a imagem de forma elegante para exibição da maneira que escolher.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Implementando renderização**](implementing-render.md)
</dt> </dl>

 

 




