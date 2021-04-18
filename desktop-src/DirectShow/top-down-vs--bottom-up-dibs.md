---
description: Top-Down vs.
ms.assetid: c292f145-f385-4f18-8f98-e414d86860e2
title: Top-Down x Bottom-Up DIBs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e719bea5923aeccc4a0a92b5f73a253e13d2e12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105756948"
---
# <a name="top-down-vs-bottom-up-dibs"></a>Top-Down x Bottom-Up DIBs

Se você for novo na programação de gráficos, poderá esperar que um bitmap seja organizado na memória para que a linha superior da imagem apareça no início do buffer, seguida pela próxima linha e assim por diante. No entanto, isso não é necessariamente o caso. No Windows, os bitmaps independentes de dispositivo (DIBs) podem ser colocados na memória em duas orientações diferentes, de baixo para cima e de cima para baixo.

Em um DIB de baixo para cima, o buffer de imagem começa com a linha inferior de pixels, seguida pela próxima linha e assim por diante. A linha superior da imagem é a última linha no buffer. Portanto, o primeiro byte na memória é o pixel inferior esquerdo da imagem. No GDI, todos os DIBs são de baixo para cima. O diagrama a seguir mostra o layout físico de um DIB de baixo para cima.

![DIB de baixo para cima](images/pixel-layout-bottomup.png)

Em um DIB de cima para baixo, a ordem das linhas é invertida. A linha superior da imagem é a primeira linha na memória, seguida pela próxima linha abaixo. A linha inferior da imagem é a última linha no buffer. Com um DIB de cima para baixo, o primeiro byte na memória é o pixel superior esquerdo da imagem. O DirectDraw usa DIBs de cima para baixo. O diagrama a seguir mostra o layout físico de um DIB de cima para baixo:

![DIB de cima para baixo](images/pixel-layout-topdown.png)

Para o DIBs RGB, a orientação da imagem é indicada pelo membro de **doheight** da estrutura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) . Se a **interheight** for positiva, a imagem será de baixo para cima. Se a **interheight** for negativa, a imagem será de cima para baixo.

Os DIBs em formatos YUV são sempre de cima para baixo, e o sinal do membro de **monoheight** é ignorado. Os decodificadores devem oferecer formatos YUV com uma **altura** positiva, mas também devem aceitar formatos YUV com uma **biHeight** negativa e ignorar o sinal.

Além disso, qualquer tipo de DIB que usa um **FOURCC** no membro da **bicompressão** deve expressar sua **altura** como um número positivo, independentemente do que é sua orientação, pois o próprio **FOURCC** identifica um esquema de compactação cuja orientação de imagem deve ser compreendida por qualquer filtro compatível.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Trabalhando com quadros de vídeo](working-with-video-frames.md)
</dt> </dl>

 

 



