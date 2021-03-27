---
description: Fontes rasterizadas, vetoriais, TrueType e OpenType
ms.assetid: 4fe98f04-3fb0-4a03-86c3-d0ea6f07f8f0
title: Fontes rasterizadas, vetoriais, TrueType e OpenType
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e9b4be20ac7d02075fcd5c6cdbefe9eb516ea21
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988791"
---
# <a name="raster-vector-truetype-and-opentype-fonts"></a>Fontes rasterizadas, vetoriais, TrueType e OpenType

Os aplicativos podem usar quatro tipos diferentes de tecnologias de fonte para exibir e imprimir texto:

-   Raster
-   Vetor
-   TrueType
-   Microsoft OpenType

As diferenças entre essas fontes refletem a maneira como o *glifo* de cada caractere ou símbolo é armazenado no respectivo arquivo de recurso de fonte:

-   Em fontes de varredura, um glifo é um bitmap que o sistema usa para desenhar um único caractere ou símbolo na fonte.
-   Em fontes de vetor, um glifo é uma coleção de pontos de extremidade de linha que definem os segmentos de linha que o sistema usa para desenhar um caractere ou símbolo na fonte.
-   Nas fontes TrueType e OpenType, um glifo é uma coleção de comandos line e Curve, bem como uma coleção de dicas.

O sistema usa os comandos line e Curve para definir o contorno do bitmap para um caractere ou símbolo na fonte TrueType ou OpenType da Microsoft. O sistema usa as dicas para ajustar o tamanho das linhas e formas das curvas usadas para desenhar o caractere ou símbolo. Essas dicas e os respectivos ajustes se baseiam na quantidade de dimensionamento usada para reduzir ou aumentar o tamanho do bitmap. Uma fonte OpenType é equivalente a uma fonte TrueType, exceto que uma fonte OpenType permite definições de glifo PostScript, além de definições de glifo TrueType.

Como os bitmaps para cada glifo em uma fonte de varredura são projetados para uma resolução específica do dispositivo, as fontes de varredura geralmente são consideradas dependentes do dispositivo. As fontes de vetor, por outro lado, não dependem do dispositivo, pois cada glifo é armazenado como uma coleção de linhas escalonáveis. No entanto, as fontes de vetor geralmente são desenhadas mais lentamente do que as fontes rasterizadas ou TrueType e OpenType. As fontes TrueType e OpenType fornecem uma velocidade de desenho relativamente rápida e uma verdadeira independência de dispositivo. Usando as dicas associadas a um glifo, um desenvolvedor pode dimensionar os caracteres de uma fonte TrueType ou OpenType para cima ou para baixo e ainda manter sua forma original.

Como mencionado anteriormente, os glifos para uma fonte são armazenados em um arquivo de recurso de fonte. Um arquivo de recurso de fonte é, na verdade, uma DLL que contém apenas dados, não há nenhum código. Para fontes de rasterização e de vetor, esses dados são divididos em duas partes: um cabeçalho que descreve as métricas da fonte e os dados de glifo. Um arquivo de recurso de fonte para uma fonte de rasterização ou de vetor é identificado pela extensão de nome de arquivo. Fon. Para fontes TrueType e OpenType, há dois arquivos para cada fonte: o primeiro arquivo contém um cabeçalho relativamente curto e o segundo contém os dados reais da fonte. O primeiro arquivo é identificado por uma extensão. Database e o segundo é identificado por uma extensão. ttf.

 

 



