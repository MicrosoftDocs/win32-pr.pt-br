---
description: Para permitir que os aplicativos coloquem a saída na memória em vez de enviá-la para um dispositivo real, use um contexto de dispositivo especial para operações de bitmap chamadas de contexto de dispositivo de memória.
ms.assetid: 0a682dc4-31a4-43c8-b0b1-ab01986b1dac
title: Contextos do dispositivo de memória
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63469823e38eb98da5d43ede006e6b1e64af874d300127db6cd4cc7743672d29
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118760054"
---
# <a name="memory-device-contexts"></a>Contextos do dispositivo de memória

Para permitir que os aplicativos coloquem a saída na memória em vez de enviá-la para um dispositivo real, use um contexto de dispositivo especial para operações de bitmap chamadas de contexto *de dispositivo de memória*. Um DC de memória permite que o sistema trate uma parte da memória como um dispositivo virtual. É uma matriz de bits na memória que um aplicativo pode usar temporariamente para armazenar os dados de cores para bitmaps criados em uma superfície de desenho normal. Como o bitmap é compatível com o dispositivo, um DC de memória também é às vezes chamado de contexto *de dispositivo compatível.*

O DC de memória armazena imagens de bitmap para um dispositivo específico. Um aplicativo pode criar um DC de memória chamando a [**função CreateCompatibleDC.**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatibledc)

O bitmap original em um DC de memória é simplesmente um espaço reservado. Suas dimensões são um pixel por pixel. Antes que um aplicativo possa começar a desenhar, ele deve selecionar um bitmap com a largura e a altura apropriadas no DC chamando a [**função SelectObject.**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) Para criar um bitmap das dimensões apropriadas, use a função [**CreateBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmap), [**CreateBitmapIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmapindirect)ou [**CreateCompatibleBitmap.**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap) Depois que o bitmap é selecionado no DC de memória, o sistema substitui a matriz de bit único por uma matriz grande o suficiente para armazenar informações de cor para o retângulo especificado de pixels.

Quando um aplicativo passa o alça retornado por [**CreateCompatibleDC para**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatibledc) uma das funções de desenho, a saída solicitada não aparece na superfície de desenho de um dispositivo. Em vez disso, o sistema armazena as informações de cor para a linha, a curva, o texto ou a região resultantes na matriz de bits. O aplicativo pode copiar a imagem armazenada na memória de volta para uma superfície de desenho chamando a função [**BitBlt,**](/windows/desktop/api/Wingdi/nf-wingdi-bitblt) identificando o DC de memória como o contexto do dispositivo de origem e uma janela ou DC de tela como o contexto do dispositivo de destino.

Ao exibir um DIB ou um DDB criado de um DIB em um dispositivo de paleta, você pode melhorar a velocidade na qual a imagem é desenhada organizando a paleta lógica para corresponder ao layout da paleta do sistema. Para fazer isso, [**chame GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) com o valor NUMRESERVED para obter o número de cores reservadas no sistema. Em seguida, [**chame GetSystemPaletteEntries**](/windows/desktop/api/Wingdi/nf-wingdi-getsystempaletteentries) e preencha as primeiras e últimas entradas NUMRESERVED/2 da paleta lógica com as cores do sistema correspondentes. Por exemplo, se NUMRESERVED for 20, você preencherá a primeira e a última 10 entradas da paleta lógica com as cores do sistema. Em seguida, preencha as 256 cores NUMRESERVED restantes da paleta lógica (em nosso exemplo, as 236 cores restantes) com cores do DIB e de definido o sinalizador PC NOCOLLAPSE em cada uma \_ dessas cores.

Para obter mais informações sobre cores e paletas, consulte [Cores](colors.md). Para obter mais informações sobre bitmaps e operações de bitmap, consulte [Bitmaps](bitmaps.md).

 

 



