---
description: Um DIB (bitmap independente de dispositivo) contém uma tabela de cores.
ms.assetid: 56b39a3d-48a4-4620-9652-ec41ea4d6423
title: Device-Independent bitmaps
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1aa35201a9a27c2d16a5a18b0125d25a3938890c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091196"
---
# <a name="device-independent-bitmaps"></a>Device-Independent bitmaps

Um DIB (bitmap independente de dispositivo) contém uma *tabela de cores*. Uma tabela de cores descreve como os valores de pixel correspondem aos valores de cor *RGB* , que descrevem as cores que são produzidas emitindo luz. Assim, um DIB pode atingir o esquema de cores adequado em qualquer dispositivo. Um DIB contém as seguintes informações de cor e dimensão:

-   O formato de cor do dispositivo no qual a imagem retangular foi criada.
-   A resolução do dispositivo no qual a imagem retangular foi criada.
-   A paleta do dispositivo no qual a imagem foi criada.
-   Uma matriz de bits que mapeia tercetos vermelho, verde e azul ( [**RGB**](/windows/desktop/api/Wingdi/nf-wingdi-rgb) ) para pixels na imagem retangular.
-   Um identificador de compactação de dados que indica o esquema de compactação de dados (se houver) usado para reduzir o tamanho da matriz de bits.

As informações de cor e dimensão são armazenadas em uma estrutura [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) , que consiste em uma estrutura [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) seguida por duas ou mais estruturas [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) . A estrutura **BITMAPINFOHEADER** especifica as dimensões do retângulo de pixel, descreve a tecnologia de cores do dispositivo e identifica os esquemas de compactação usados para reduzir o tamanho do bitmap. As estruturas **RGBQUAD** identificam as cores que aparecem no retângulo de pixel.

Há duas variedades de DIBs:

-   Um DIB de baixo para cima, no qual a origem está no canto inferior esquerdo.
-   Um DIB de cima para baixo, no qual a origem está no canto superior esquerdo.

Se a altura de uma DIB, conforme indicado pelo membro **Height** da estrutura de cabeçalho de informações de bitmap, for um valor positivo, será um DIB de baixo para cima; se a altura for um valor negativo, será um DIB de cima para baixo. Os DIBs de cima para baixo não podem ser compactados.

O formato de cor é especificado em termos de uma contagem de planos de cores e bits de cor. A contagem de planos de cores é sempre 1; a contagem de bits de cor é 1 para bitmaps monocromáticos, 4 para bitmaps VGA e 8, 16, 24 ou 32 para bitmaps em outros dispositivos de cores. Um aplicativo recupera o número de bits de cor que uma exibição (ou impressora) específica usa chamando a função [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) , especificando BITSPIXEL como o segundo argumento.

A resolução de um dispositivo de vídeo é especificada em pixels por medidor. Um aplicativo pode recuperar a resolução horizontal para uma exibição de vídeo, ou impressora, seguindo este processo de três etapas.

1.  Chame a função [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) , especificando HORZRES como o segundo argumento.
2.  Chame [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) uma segunda vez, especificando HORZSIZE como o segundo argumento.
3.  Divida o primeiro valor de retorno pelo segundo valor de retorno.

O aplicativo pode recuperar a resolução vertical usando o mesmo processo de três etapas com parâmetros diferentes: VERTRES no lugar de HORZRES e VERTSIZE no lugar de HORZSIZE.

A paleta é representada por uma matriz de estruturas [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) que especificam os componentes de intensidade vermelha, verde e azul para cada cor em uma paleta de cores do dispositivo de vídeo. Cada índice de cor na matriz da paleta é mapeado para um pixel específico na região retangular associada ao bitmap. O tamanho dessa matriz, em bits, é equivalente à largura do retângulo, em pixels, multiplicado pela altura do retângulo, em pixels, multiplicado pela contagem de bits de cor para o dispositivo. Um aplicativo pode recuperar o tamanho da paleta do dispositivo chamando a função [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) , especificando NUMCOLORS como o segundo argumento.

O Windows dá suporte à compactação da matriz de paleta para 8-bpp e 4-bpp de baixo para cima. Essas matrizes podem ser compactadas usando o esquema RLE (codificação de comprimento de execução). O esquema RLE usa valores de 2 bytes, o primeiro byte que especifica o número de pixels consecutivos que usam um índice de cores e o segundo byte que especifica o índice. Para obter mais informações sobre compactação de bitmap, consulte a descrição das estruturas [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)), [**BITMAPFILEHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapfileheader), [**BITMAPV4HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv4header)e [**BITMAPV5HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv5header) .

Um aplicativo pode criar um DIB de um BDD Inicializando as estruturas necessárias e chamando a função [**GetDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-getdibits) . Para determinar se um dispositivo dá suporte a essa função, chame a função [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) , especificando o \_ \_ bitmap de di RC como o sinalizador RasterCaps.

Um aplicativo que precisa copiar um bitmap pode usar [**TransparentBlt**](/windows/desktop/api/WinGdi/nf-wingdi-transparentblt) para copiar todos os pixels em um bitmap de origem para um bitmap de destino, exceto os pixels que correspondem à cor transparente.

Um aplicativo pode usar um DIB para definir pixels no dispositivo de vídeo chamando a função [**SetDIBitsToDevice**](/windows/desktop/api/Wingdi/nf-wingdi-setdibitstodevice) ou [**StretchDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits) . Para determinar se um dispositivo dá suporte à função **SetDIBitsToDevice** , chame a função [**GETDEVICECAPS**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) , especificando RC \_ DIBTODEV como o sinalizador RasterCaps. Especifique \_ STRETCHDIB RC como o sinalizador RasterCaps para determinar se o dispositivo dá suporte a **StretchDIBits**.

Um aplicativo que simplesmente precisa exibir um DIB já existente pode usar a função [**SetDIBitsToDevice**](/windows/desktop/api/Wingdi/nf-wingdi-setdibitstodevice) . Por exemplo, um aplicativo de planilha pode abrir gráficos existentes e exibi-los em uma janela usando a função **SetDIBitsToDevice** . No entanto, para redesenhar repetidamente um bitmap em uma janela, o aplicativo deve usar a função [**BitBlt**](/windows/desktop/api/Wingdi/nf-wingdi-bitblt) . Por exemplo, um aplicativo multimídia que combina gráficos animados com som pode se beneficiar de chamar a função **BitBlt** porque ela é executada mais rápido do que **SetDIBitsToDevice**.

 

 
