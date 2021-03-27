---
description: Uma curva regular é um conjunto de pixels realçados em uma exibição de varredura (ou pontos em uma página impressa) que definem o perímetro (ou parte do perímetro) de uma seção de cone.
ms.assetid: b7a1b544-8b50-45ba-918c-17472c46c8b8
title: Curvas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e694edeb535dbc7dbd4191a5a2b0b44556b810e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827666"
---
# <a name="curves"></a>Curvas

Uma curva regular é um conjunto de pixels realçados em uma exibição de varredura (ou pontos em uma página impressa) que definem o perímetro (ou parte do perímetro) de uma seção de cone. Uma curva irregular é um conjunto de pixels que definem uma curva que não se ajusta ao perímetro de uma seção de cone. O ponto final é excluído de uma curva assim como é excluído de uma linha.

Quando um aplicativo chama uma das funções de desenho de curva, o GDI quebra a curva em um número de segmentos de linha discretos extremamente pequenos. Depois de determinar os pontos de extremidade (ponto inicial e ponto final) para cada um desses segmentos de linha, o GDI determina quais pixels (ou pontos) definem cada linha aplicando seu DDA.

Um aplicativo pode desenhar uma elipse ou parte de uma elipse chamando a função [**Arc**](/windows/desktop/api/Wingdi/nf-wingdi-arc) . Essa função desenha a curva dentro do perímetro de um retângulo invisível chamado de um retângulo delimitador. O tamanho da elipse é especificado por dois radiais invisíveis que se estendem do centro do retângulo até os lados do retângulo. A ilustração a seguir mostra um arco (parte de uma elipse) desenhado usando a função **Arc** .

![diagrama mostrando um arco que representa três trimestres de um círculo completo](images/cslcv-03.png)

Ao chamar a função [**Arc**](/windows/desktop/api/Wingdi/nf-wingdi-arc) , um aplicativo especifica as coordenadas do retângulo delimitador e radials. A ilustração anterior mostra o retângulo e as radials com linhas tracejadas enquanto o arco real foi desenhado usando uma linha sólida.

Ao desenhar o arco de outro objeto, o aplicativo pode chamar as funções [**SetArcDirection**](/windows/desktop/api/Wingdi/nf-wingdi-setarcdirection) e [**GetArcDirection**](/windows/desktop/api/Wingdi/nf-wingdi-getarcdirection) para controlar a direção (no sentido horário ou anti-horário) na qual o objeto é desenhado. A direção padrão para desenhar arcos e outros objetos é no sentido anti-horário.

Além de desenhar elipses ou partes de elipses, os aplicativos podem desenhar curvas irregulares chamadas curvas Bézier. Uma *curva de Bézier* é uma curva irregular cuja curvatura é definida por quatro pontos de controle (P1, P2, P3 e P4). Os pontos de controle P1 e P4 definem os pontos inicial e final da curva, e os pontos de controle P2 e P3 definem a forma da curva por pontos de marcação em que a curva inverte a orientação, conforme mostrado no diagrama a seguir.

![ilustração mostrando duas curvas de Bézier, cada uma entre um ponto inicial e um final e cada uma com dois pontos de controle](images/cslcv-04.png)

Um aplicativo pode desenhar curvas irregulares chamando a função de [**telebezier**](/windows/desktop/api/Wingdi/nf-wingdi-polybezier) , fornecendo os pontos de controle apropriados.

 

 



