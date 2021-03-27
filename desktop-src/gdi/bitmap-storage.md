---
description: Os bitmaps devem ser salvos em um arquivo que usa o formato de arquivo de bitmap estabelecido e atribuído um nome com a extensão. bmp de três caracteres.
ms.assetid: 44f19d14-4e0e-4512-8c86-6bd34ca4e87b
title: Armazenamento de bitmap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28046f6d78f5137d0dfc5b1396bbf76be318daa5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091219"
---
# <a name="bitmap-storage"></a>Armazenamento de bitmap

Os bitmaps devem ser salvos em um arquivo que usa o formato de arquivo de bitmap estabelecido e atribuído um nome com a extensão. bmp de três caracteres. O formato de arquivo de bitmap estabelecido consiste em uma estrutura [**BITMAPFILEHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapfileheader) seguida por uma estrutura [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)), [**BITMAPV4HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv4header)ou [**BITMAPV5HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv5header) . Uma matriz de estruturas [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) (também chamada de tabela de cores) segue a estrutura de cabeçalho de informações de bitmap. A tabela de cores é seguida por uma segunda matriz de índices na tabela de cores (os dados de bitmap reais).

O formato de arquivo de bitmap é mostrado na ilustração a seguir.

![diagrama do formato de arquivo de bitmap, mostrando a matriz BITMAPFILEHEADER, BITMAPINFOHEADER, RGBQUAD e a matriz de índice de cor](images/csbmp-02.png)

Os membros da estrutura [**BITMAPFILEHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapfileheader) identificam o arquivo; Especifique o tamanho do arquivo, em bytes; e especifique o deslocamento do primeiro byte no cabeçalho até o primeiro byte de dados de bitmap. Os membros da estrutura [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)), [**BITMAPV4HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv4header)ou [**BITMAPV5HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv5header) especificam a largura e a altura do bitmap, em pixels; o formato de cor (contagem de planos de cores e bits de cor por pixel) do dispositivo de vídeo no qual o bitmap foi criado; Se os dados de bitmap foram compactados antes do armazenamento e do tipo de compactação usados; o número de bytes de dados de bitmap; a resolução do dispositivo de vídeo no qual o bitmap foi criado; e o número de cores representadas nos dados. As estruturas [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) especificam os valores de intensidade RGB para cada uma das cores na paleta do dispositivo.

A matriz de índice de cor associa uma cor, na forma de um índice a uma estrutura [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) , com cada pixel em um bitmap. Assim, o número de bits na matriz de índice de cor é igual ao número de pixels vezes o número de bits necessário para indexar as estruturas **RGBQUAD** . Por exemplo, um bitmap preto-e-branco 8x8 tem uma matriz de índice de cor de 8 \* 8 \* 1 = 64 bits, porque é necessário um bit para indexar duas cores. O Redbrick.bmp, mencionado em [sobre bitmaps](about-bitmaps.md), é um bitmap de 32x32 com 16 cores; sua matriz de índice de cor é 32 \* 32 \* 4 = 4096 bits porque quatro cores do índice de bits 16.

Para criar uma matriz de índice de cor para um bitmap de cima para baixo, comece na linha superior do bitmap. O índice de [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) para a cor do pixel mais à esquerda é o primeiro *n* bits na matriz de índice de cor (em que *n* é o número de bits necessários para indicar todas as estruturas **RGBQUAD** ). A cor do próximo pixel à direita é os próximos *n* bits na matriz e assim por diante. Depois de alcançar o pixel mais à direita na linha, continue com o pixel mais à esquerda na linha abaixo. Continue até concluir com o bitmap inteiro. Se for um bitmap de baixo, comece na linha inferior do bitmap em vez da linha superior, ainda da esquerda para a direita e continue na linha superior do bitmap.

A saída hexadecimal a seguir mostra o conteúdo do arquivo Redbrick.bmp.


```C++
0000    42 4d 76 02 00 00 00 00  00 00 76 00 00 00 28 00 
0010    00 00 20 00 00 00 20 00  00 00 01 00 04 00 00 00 
0020    00 00 00 00 00 00 00 00  00 00 00 00 00 00 00 00 
0030    00 00 00 00 00 00 00 00  00 00 00 00 80 00 00 80 
0040    00 00 00 80 80 00 80 00  00 00 80 00 80 00 80 80 
0050    00 00 80 80 80 00 c0 c0  c0 00 00 00 ff 00 00 ff 
0060    00 00 00 ff ff 00 ff 00  00 00 ff 00 ff 00 ff ff 
0070    00 00 ff ff ff 00 00 00  00 00 00 00 00 00 00 00 
0080    00 00 00 00 00 00 00 00  00 00 00 00 00 00 09 00 
0090    00 00 00 00 00 00 11 11  01 19 11 01 10 10 09 09 
00a0    01 09 11 11 01 90 11 01  19 09 09 91 11 10 09 11 
00b0    09 11 19 10 90 11 19 01  19 19 10 10 11 10 09 01 
00c0    91 10 91 09 10 10 90 99  11 11 11 11 19 00 09 01 
00d0    91 01 01 19 00 99 11 10  11 91 99 11 09 90 09 91 
00e0    01 11 11 11 91 10 09 19  01 00 11 90 91 10 09 01 
00f0    11 99 10 01 11 11 91 11  11 19 10 11 99 10 09 10 
0100    01 11 11 11 19 10 11 09  09 10 19 10 10 10 09 01 
0110    11 19 00 01 10 19 10 11  11 01 99 01 11 90 09 19 
0120    11 91 11 91 01 11 19 10  99 00 01 19 09 10 09 19 
0130    10 91 11 01 11 11 91 01  91 19 11 00 99 90 09 01 
0140    01 99 19 01 91 10 19 91  91 09 11 99 11 10 09 91 
0150    11 10 11 91 99 10 90 11  01 11 11 19 11 90 09 11 
0160    00 19 10 11 01 11 99 99  99 99 99 99 99 99 09 99 
0170    99 99 99 99 99 99 00 00  00 00 00 00 00 00 00 00 
0180    00 00 00 00 00 00 90 00  00 00 00 00 00 00 00 00 
0190    00 00 00 00 00 00 99 11  11 11 19 10 19 19 11 09 
01a0    10 90 91 90 91 00 91 19  19 09 01 10 09 01 11 11 
01b0    91 11 11 11 10 00 91 11  01 19 10 11 10 01 01 11 
01c0    90 11 11 11 91 00 99 09  19 10 11 90 09 90 91 01 
01d0    19 09 91 11 01 00 90 10  19 11 00 11 11 00 10 11 
01e0    01 10 11 19 11 00 90 19  10 91 01 90 19 99 00 11 
01f0    91 01 11 01 91 00 99 09  09 01 10 11 91 01 10 91 
0200    99 11 10 90 91 00 91 11  00 10 11 01 10 19 19 09 
0210    10 00 99 01 01 00 91 01  19 91 19 91 11 09 10 11 
0220    00 91 00 10 90 00 99 01  11 10 09 10 10 19 09 01 
0230    91 90 11 09 11 00 90 99  11 11 11 90 19 01 19 01 
0240    91 01 01 19 09 00 91 10  11 91 99 09 09 90 11 91 
0250    01 19 11 11 91 00 91 19  01 00 11 00 91 10 11 01 
0260    11 11 10 01 11 00 99 99  99 99 99 99 99 99 99 99 
0270    99 99 99 99 99 90 
```



A tabela a seguir mostra os bytes de dados associados às estruturas em um arquivo de bitmap.



| Estrutura                                    | Bytes correspondentes |
|----------------------------------------------|---------------------|
| [**BITMAPFILEHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapfileheader) | 0x00 0x0D           |
| [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) | 0x0E 0x35           |
| Matriz [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad)             | 0x36 0x75           |
| Matriz de índice de cor                            | 0x76 0x275          |



 

 

 
