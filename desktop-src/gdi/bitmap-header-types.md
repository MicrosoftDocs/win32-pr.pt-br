---
description: Tipos de cabeçalho de bitmap
ms.assetid: 6df4655a-f707-4893-b6e6-f7e4d7f67b4e
title: Tipos de cabeçalho de bitmap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c88839947845cc45633cbc07b7c36aec727318c91910bfc277680b1946080531
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119966406"
---
# <a name="bitmap-header-types"></a>Tipos de cabeçalho de bitmap

O bitmap tem quatro tipos de cabeçalho básicos:

-   [**BITMAPCOREHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapcoreheader)
-   [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85))
-   [**BITMAPV4HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv4header)
-   [**BITMAPV5HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv5header)

Os quatro tipos de cabeçalhos de bitmap são diferenciados pelo membro de **tamanho** , que é a primeira **DWORD** em cada uma das estruturas.

A estrutura [**BITMAPV5HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv5header) é uma estrutura [**BITMAPV4HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv4header) estendida, que é uma estrutura [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) estendida. No entanto, **BITMAPINFOHEADER** e [**BITMAPCOREHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapcoreheader) têm apenas o membro **size** em comum com outras estruturas de cabeçalho de bitmap.

Os formatos [**BITMAPCOREHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapcoreheader) e [**BITMAPV4HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv4header) foram substituídos pelos formatos [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) e [**BITMAPV5HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv5header) , respectivamente. Os formatos **BITMAPCOREHEADER** e **BITMAPV4HEADER** são apresentados para fins de integridade e compatibilidade com versões anteriores.

o formato de um DIB é o seguinte (para obter mais informações, consulte [Bitmap Armazenamento](bitmap-storage.md) ):

-   uma estrutura [**BITMAPFILEHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapfileheader)
-   uma estrutura [**BITMAPCOREHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapcoreheader), uma [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)), uma [**BITMAPV4HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv4header)ou uma [**BITMAPV5HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv5header) .
-   uma tabela de cores opcional, que é um conjunto de estruturas [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) ou um conjunto de estruturas [**RGBTRIPLE**](/windows/win32/api/wingdi/ns-wingdi-rgbtriple) .
-   os dados de bitmap
-   dados de perfil opcionais

Uma tabela de cores descreve como os valores de pixel correspondem aos valores de cor RGB. O RGB é um modelo para descrever as cores que são produzidas emitindo luz.

Os *dados de perfil* referem-se ao nome do arquivo de perfil (perfil vinculado) ou aos bits de perfil reais (perfil incorporado). O formato de arquivo coloca os dados de perfil no final do arquivo. Os dados do perfil são colocados logo após a tabela de cores (se houver). No entanto, se a função receber uma DIB compactada, os dados de perfil vêm após os bits de bitmap, como no formato de arquivo.

Os dados de perfil só existirão para estruturas [**BITMAPV5HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv5header) em que **BV5CSTYPE** é um perfil \_ vinculado ou perfil \_ inserido. Para funções que recebem DIBs embalado, os dados de perfil vêm após os dados de bitmap.

Um dispositivo palettized é qualquer dispositivo que usa paletas para atribuir cores. O exemplo clássico de um dispositivo palettized é uma exibição em execução na profundidade de cor de 8 bits (ou seja, 256 cores). A exibição nesse modo usa uma pequena tabela de cores para atribuir cores a um bitmap. As cores em um bitmap são atribuídas à cor mais próxima na paleta que o dispositivo está usando. O dispositivo palettized não cria uma paleta ideal para exibir o bitmap; Ele simplesmente usa qualquer coisa que esteja na paleta atual. Os aplicativos são responsáveis por criar uma paleta e selecioná-la no sistema. Em geral, bitmaps de 16, 24 e 32 bits por pixel (BPP) não contêm tabelas de cores (também conhecido como paletas ideais para o bitmap); o aplicativo é responsável por gerar uma paleta ideal nesse caso. No entanto, os bitmaps de 16, 24 e 32-bpp podem conter tabelas de cores ideais para exibição em dispositivos palettized; Nesse caso, o aplicativo precisa apenas criar uma paleta com base na tabela de cores presente no arquivo de bitmap.

Bitmaps que são 1, 4 ou 8 bpp devem ter uma tabela de cores com um tamanho máximo baseado em BPP. O tamanho máximo para bitmaps de 1, 4 e 8 bpp é 2 para a potência de BPP. Assim, um bitmap de 1 bpp tem um máximo de duas cores, o bitmap de 4 bpp tem um máximo de 16 cores e o bitmap de 8 bpp tem um máximo de 256 cores.

Os bitmaps que são 16-, 24 ou 32-bpp não exigem tabelas de cores, mas podem tê-los especificar cores para dispositivos palettized. Se uma tabela de cores estiver presente para bitmap de 16, 24 ou 32-bpp, o membro **biClrUsed** especificará o tamanho da tabela de cores e a tabela de cores deverá ter várias cores nela. Se **biClrUsed** for zero, não haverá nenhuma tabela de cores.

As máscaras de campo de bits vermelha, verde e azul para bitmaps de campo de bits de BI \_ seguem imediatamente as estruturas [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)), [**BITMAPV4HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv4header)e [**BITMAPV5HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv5header) . As estruturas **BITMAPV4HEADER** e **BITMAPV5HEADER** contêm membros adicionais para máscaras vermelha, verde e azul, como a seguir.



| Membro        | Significado                                                                                                                        |
|---------------|--------------------------------------------------------------------------------------------------------------------------------|
| **RedMask**   | Máscara de cor que especifica o componente vermelho de cada pixel, válida somente se o membro de **compactação** for definido como bi \_ BITFIELDS.   |
| **GreenMask** | Máscara de cor que especifica o componente verde de cada pixel, válida somente se o membro de **compactação** for definido como bi \_ BITFIELDS. |
| **BlueMask**  | Máscara de cor que especifica o componente azul de cada pixel, válida somente se o membro de **compactação** for definido como bi \_ BITFIELDS.  |



 

Quando o membro de **bicompressão** de [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) é definido como bi \_ BITFIELDS e a função recebe um argumento do tipo **LPBITMAPINFO**, as máscaras de cor imediatamente seguem o cabeçalho. A tabela de cores, se presente, seguirá as máscaras de cores. Os bitmaps [**BITMAPCOREHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapcoreheader) não dão suporte a máscaras de cores.

Por padrão, os dados de bitmap são de baixo para cima em seu formato. De baixo para cima significa que a primeira linha de varredura nos dados de bitmap é a última linha de varredura a ser exibida. Por exemplo, o 0<sup>ésimo</sup> pixel da linha de<sup>varredura 0</sup> para os dados de bitmap de um bitmap de 10 pixels de 10 pixels será o 0<sup>th</sup> pixel da linha<sup>de varredura 9</sup> -pixel da imagem exibida ou impressa. Bitmaps de formato RLE e bitmaps [**BITMAPCOREHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapcoreheader) não podem ser bitmaps de cima para baixo. As linhas de verificação são alinhadas em **DWORD** , exceto para bitmaps compactados por RLE. Eles devem ser preenchidos para as larguras de linha de verificação, em bytes, que não são igualmente divisíveis por quatro, exceto para bitmaps compactados de RLE. Por exemplo, um bitmap de 10 a 10 pixels com 24-bpp terá dois bytes de preenchimento no final de cada linha de exame.

 

 
