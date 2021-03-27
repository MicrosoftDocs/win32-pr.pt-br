---
description: Para permitir que os aplicativos coloquem a saída na memória em vez de enviá-la a um dispositivo real, use um contexto de dispositivo especial para operações de bitmap chamadas de contexto de dispositivo de memória.
ms.assetid: 0a682dc4-31a4-43c8-b0b1-ab01986b1dac
title: Contextos de dispositivo de memória
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 095de04fdf965a87011895015ad7ea6c9782e286
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103661602"
---
# <a name="memory-device-contexts"></a>Contextos de dispositivo de memória

Para permitir que os aplicativos coloquem a saída na memória em vez de enviá-la a um dispositivo real, use um contexto de dispositivo especial para operações de bitmap chamadas de *contexto de dispositivo de memória*. Um controlador de domínio de memória permite que o sistema trate uma parte da memória como um dispositivo virtual. É uma matriz de bits na memória que um aplicativo pode usar temporariamente para armazenar os dados de cor de bitmaps criados em uma superfície de desenho normal. Como o bitmap é compatível com o dispositivo, um controlador de domínio de memória também é chamado de *contexto de dispositivo compatível*.

O DC de memória armazena imagens de bitmap para um dispositivo específico. Um aplicativo pode criar um controlador de domínio de memória chamando a função [**CreateCompatibleDC**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatibledc) .

O bitmap original em um controlador de domínio de memória é simplesmente um espaço reservado. Suas dimensões são um pixel em um pixel. Antes que um aplicativo possa começar a desenhar, ele deve selecionar um bitmap com a largura e a altura apropriadas no controlador de domínio chamando a função [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) . Para criar um bitmap das dimensões apropriadas, use a função [**CreateBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmap), [**CreateBitmapIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmapindirect)ou [**CreateCompatibleBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap) . Depois que o bitmap é selecionado no controlador de domínio de memória, o sistema substitui a matriz de bit único por uma matriz grande o suficiente para armazenar informações de cor para o retângulo especificado de pixels.

Quando um aplicativo passa o identificador retornado pelo [**CreateCompatibleDC**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatibledc) para uma das funções de desenho, a saída solicitada não aparece na superfície de desenho de um dispositivo. Em vez disso, o sistema armazena as informações de cor da linha resultante, da curva, do texto ou da região na matriz de bits. O aplicativo pode copiar a imagem armazenada na memória de volta para uma superfície de desenho chamando a função [**BitBlt**](/windows/desktop/api/Wingdi/nf-wingdi-bitblt) , identificando o controlador de domínio de memória como o contexto do dispositivo de origem e um controlador de domínio de janela ou de tela como o contexto do dispositivo de destino.

Ao exibir uma DIB ou um BDD criado por meio de um DIB em um dispositivo de paleta, você pode melhorar a velocidade na qual a imagem é desenhada organizando a paleta lógica para corresponder ao layout da paleta do sistema. Para fazer isso, chame [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) com o valor NUMRESERVED para obter o número de cores reservadas no sistema. Em seguida, chame [**GetSystemPaletteEntries**](/windows/desktop/api/Wingdi/nf-wingdi-getsystempaletteentries) e preencha as entradas First e Last NUMRESERVED/2 da paleta lógica com as cores do sistema correspondentes. Por exemplo, se NUMRESERVED for 20, você preencherá as primeiras e últimas 10 entradas da paleta lógica com as cores do sistema. Em seguida, preencha as cores de 256-NUMRESERVED restantes da paleta lógica (em nosso exemplo, as cores de 236 restantes) com cores da DIB e defina o \_ sinalizador de DESrecolhimento do PC em cada uma dessas cores.

Para obter mais informações sobre cores e paletas, consulte [cores](colors.md). Para obter mais informações sobre bitmaps e operações de bitmap, consulte [bitmaps](bitmaps.md).

 

 



