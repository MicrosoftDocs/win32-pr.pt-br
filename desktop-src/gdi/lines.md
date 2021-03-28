---
description: 'Uma linha é um conjunto de pixels realçados em uma exibição rasterizada (ou um conjunto de pontos em uma página impressa) identificado por dois pontos: um ponto inicial e um ponto final.'
ms.assetid: 538aa3c3-e13a-40dc-b977-3e353a7e9893
title: Linhas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64cd678f782567e98d32ab7f8786d5b87aab1918
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165070"
---
# <a name="lines"></a>Linhas

Uma linha é um conjunto de pixels realçados em uma exibição rasterizada (ou um conjunto de pontos em uma página impressa) identificado por dois pontos: um ponto inicial e um ponto final. O pixel localizado no ponto de partida é sempre incluído na linha, e o pixel localizado no ponto final é sempre excluído. (Esse tipo de linha às vezes é chamado de inclusão exclusiva.)

Quando um aplicativo chama uma das funções de desenho de linha, GDI (interface gráfica de dispositivo) ou, em alguns casos, um driver de dispositivo, determina quais pixels devem ser realçados. O GDI é uma DLL (biblioteca de vínculo dinâmico) que processa chamadas de função gráficas de um aplicativo e passa essas chamadas para um driver de dispositivo. Um driver de dispositivo é uma DLL que recebe entrada de GDI, converte a entrada em comandos de dispositivo e passa esses comandos para o dispositivo apropriado. O GDI usa um analisador diferencial digital (DDA) para determinar o conjunto de pixels que definem uma linha. Um DDA determina o conjunto de pixels examinando cada ponto na linha e identificando os pixels na superfície de exibição (ou pontos em uma página impressa) que correspondem aos pontos. A ilustração a seguir mostra uma linha, seu ponto de partida, seu ponto final e os pixels realçados usando um simples DDA.

![ilustração mostrando uma grade de pixels, pontos iniciais e finais, uma linha e sombreamento nos pixels que estão ao longo da linha](images/cslcv-01.png)

O mais simples e mais comum DDA é o Bresenham, ou incremental, DDA. Uma versão modificada desse algoritmo desenha linhas no Windows. O DDA incremental é observado para sua simplicidade, mas também é anotado para sua inexatidão. Como ele arredonda para o valor inteiro mais próximo, às vezes, ele não representa a linha original solicitada pelo aplicativo. O DDA usado pelo GDI não é arredondado para o número inteiro mais próximo. Como resultado, esse novo DDA produz uma saída que às vezes é muito mais próxima da aparência à linha original solicitada pelo aplicativo.

> [!Note]  
> Se um aplicativo exigir uma saída de linha que não possa ser obtida com o novo DDA, ele poderá desenhar suas próprias linhas chamando a função [**LineDDA**](/windows/desktop/api/Wingdi/nf-wingdi-linedda) e fornecendo um DDA ([**LineDDAProc**](/windows/desktop/api/Wingdi/nc-wingdi-lineddaproc)) particular. No entanto, a função **LineDDA** desenha linhas muito mais lentas do que as funções de desenho de linha. Não use essa função em um aplicativo se a velocidade for uma preocupação principal.

 

Um aplicativo pode usar o novo DDA para desenhar linhas únicas e vários segmentos de linha conectados. Um aplicativo pode desenhar uma única linha chamando a função [**LineTo**](/windows/desktop/api/Wingdi/nf-wingdi-lineto) . Essa função desenha uma linha da posição atual até, mas não incluindo, um ponto final especificado. Um aplicativo pode desenhar uma série de segmentos de linha conectados chamando a função [**Polyline**](/windows/desktop/api/Wingdi/nf-wingdi-polyline) , fornecendo uma matriz de pontos que especificam o ponto final de cada segmento de linha. Um aplicativo pode desenhar várias séries desenvolvidas de segmentos de linha conectados chamando a função [**Polyline**](/windows/desktop/api/Wingdi/nf-wingdi-polypolyline) , fornecendo os pontos finais necessários.

A ilustração a seguir mostra a saída de linha criada chamando as funções [**LineTo**](/windows/desktop/api/Wingdi/nf-wingdi-lineto), [**Polyline**](/windows/desktop/api/Wingdi/nf-wingdi-polyline)e [**Polyline**](/windows/desktop/api/Wingdi/nf-wingdi-polypolyline) .

![ilustração mostrando uma linha reta, uma caixa em forma de "l" e duas formas que aparecem tridimensionais](images/cslcv-02.png)

 

 



