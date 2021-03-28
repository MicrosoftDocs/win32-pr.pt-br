---
description: Os aplicativos que usam as métricas de texto TrueType podem alcançar um alto grau de portabilidade de impressora e documento; Eles podem usar métricas TrueType mesmo se precisarem manter a compatibilidade com as versões iniciais de 16 bits do Windows.
ms.assetid: 29b54315-7c4e-4b8c-ad79-0b85c7386860
title: Usando métricas TrueType portáteis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83360b620bde11e20726b0ee4124d35bf6cf00b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988954"
---
# <a name="using-portable-truetype-metrics"></a>Usando métricas TrueType portáteis

Os aplicativos que usam as métricas de texto TrueType podem alcançar um alto grau de portabilidade de impressora e documento; Eles podem usar métricas TrueType mesmo se precisarem manter a compatibilidade com as versões iniciais de 16 bits do Windows.

As larguras de design superam a maioria dos problemas do texto dependente de dispositivo introduzido por dispositivos físicos. As larguras de design são um tipo de largura lógica. Independentemente de quaisquer problemas de rasterização ou transformações de escala, cada glifo tem uma largura lógica e uma altura. Composto por uma página lógica, cada caractere em uma cadeia de caracteres tem um lugar que é independente das larguras do dispositivo físico. Embora uma largura lógica indique que as larguras podem ser escaladas linearmente em todos os tamanhos de ponto, isso não é necessariamente verdadeiro para as fontes não portáveis ou mais TrueType. Em tamanhos de pontos menores, alguns glifos são tornados mais largos em relação à sua altura para melhor legibilidade.

Os caracteres em fontes de núcleo TrueType são projetados em relação a uma grade de 2048 por 2048. A largura do design é a largura de um caractere nessas unidades de grade. (O TrueType dá suporte a qualquer tamanho de grade de inteiro de até 16.384 por 16.384; tamanhos de grade que são potências de inteiro de 2 escalas mais rápido do que outros tamanhos de grade.)

O contorno de fonte é projetado em unidades de noções. O quadrado em é a grade de noções em relação à qual a estrutura de tópicos da fonte está ajustada. (Você pode usar o membro **otmEMSquare** de [OUTLINETEXTMETRIC](/windows/desktop/api/Wingdi/ns-wingdi-outlinetextmetrica) e o membro **ntmSizeEM** de [NEWTEXTMETRIC](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) para recuperar o tamanho do quadrado em unidades de noções.) Quando é criada uma fonte que tem um tamanho de ponto (em unidades de dispositivo) igual ao tamanho de seu quadrado em, as larguras ABC dessa fonte são as larguras de design desejadas. Por exemplo, suponha que o tamanho de um quadrado em é 1000 e que as larguras ABC de um caractere na fonte são 150, 400 e 150. Um caractere nessa fonte com 10 unidades de dispositivo alta teria larguras ABC de 1,5, 4 e 1,5, respectivamente. Como o \_ modo de mapeamento de texto mm é mais comumente usado com fontes (e o texto mm \_ é equivalente às unidades do dispositivo), esse é um cálculo simples.

Devido à alta resolução de larguras de design TrueType, os aplicativos que os usam devem levar em conta os valores numéricos grandes que podem ser criados. Para mais informações, consulte os seguintes tópicos:

-   [Dispositivo versus unidades de design](device-vs--design-units.md)
-   [Métricas para documentos portáteis](metrics-for-portable-documents.md)

 

 



