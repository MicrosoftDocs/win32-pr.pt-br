---
description: o Windows dá suporte a formatos para compactação de bitmaps que definem suas cores com 8 ou 4 bits por pixel. A compactação reduz o armazenamento de disco e memória necessário para o bitmap.
ms.assetid: 14d14662-910a-4f3f-914e-6ccfc602c822
title: Compactação de bitmap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a3fa089401e77e882cf62472d007495e3e6c686d52259f095cb5a2758204736
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105765"
---
# <a name="bitmap-compression"></a>Compactação de bitmap

o Windows dá suporte a formatos para compactação de bitmaps que definem suas cores com 8 ou 4 bits por pixel. A compactação reduz o armazenamento de disco e memória necessário para o bitmap.

Quando o membro de **compactação** da estrutura de cabeçalho de informações de bitmap é bi \_ RLE8, um formato RLE (codificação de comprimento de execução) é usado para compactar um bitmap de 8 bits. Esse formato pode ser compactado em modos codificados ou absolutos. Ambos os modos podem ocorrer em qualquer lugar no mesmo bitmap:

-   O *modo codificado* consiste em dois bytes: o primeiro byte Especifica o número de pixels consecutivos a serem desenhados usando o índice de cores contido no segundo byte. Além disso, o primeiro byte do par pode ser definido como zero para indicar um caractere de escape que denota o final de uma linha, o final de um bitmap ou um Delta, dependendo do valor do segundo byte. A interpretação do escape depende do valor do segundo byte do par, que pode ser um dos valores a seguir.



| Valor | Significado                                                                                                                                                     |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | Fim da linha.                                                                                                                                                |
| 1     | Fim do bitmap.                                                                                                                                              |
| 2     | Trifásico. Os 2 bytes após o escape contêm valores não assinados indicando os deslocamentos horizontal e vertical do próximo pixel da posição atual. |



 

-   No *modo absoluto*, o primeiro byte é zero e o segundo byte é um valor no intervalo de 03H a FFH. O segundo byte representa o número de bytes a seguir, cada um contendo o índice de cores de um único pixel. Quando o segundo byte é dois ou menos, o escape tem o mesmo significado que o modo codificado. No modo absoluto, cada execução deve ser preenchida com zero para terminar em um limite de palavras de 16 bits.

O exemplo a seguir mostra os valores hexadecimais de um bitmap compactado de 8 bits:


```C++
[03 04] [05 06] [00 03 45 56 67 00] [02 78] [00 02 05 01] 
[02 78] [00 00] [09 1E] [00 01] 
```



O bitmap é expandido da seguinte maneira (valores de dois dígitos representam um índice de cores para um único pixel):


```C++
04 04 04 
06 06 06 06 06 
45 56 67 
78 78 
move current position 5 right and 1 down 
78 78 
end of line 
1E 1E 1E 1E 1E 1E 1E 1E 1E 
end of RLE bitmap 
```



Quando o membro de **compactação** é bi \_ RLE4, o bitmap é compactado usando um formato de codificação de comprimento de execução para um bitmap de 4 bits, que também usa modos codificados e absolutos:

-   No modo codificado, o primeiro byte do par contém o número de pixels a serem desenhados usando os índices de cores no segundo byte. O segundo byte contém dois índices de cores, um em seus quatro bits de ordem superior e outro em seus 4 bits de ordem inferior. O primeiro dos pixels é desenhado usando a cor especificada pelos quatro bits de ordem superior, o segundo é desenhado usando a cor nos 4 bits de ordem inferior, o terceiro é desenhado usando a cor nos quatro bits de ordem superior e assim por diante, até que todos os pixels especificados pelo primeiro byte tenham sido desenhados.
-   No modo absoluto, o primeiro byte é zero. O segundo byte contém o número de índices de cores a seguir. Os bytes subsequentes contêm índices de cores em seus 4 bits de ordem alta e baixa, um índice de cor para cada pixel. No modo absoluto, cada execução deve estar alinhada em um limite de palavra. Os escapes de fim de linha, fim de bitmap e Delta descritos para BI \_ RLE8 também se aplicam à \_ compactação de bi RLE4.

O exemplo a seguir mostra os valores hexadecimais de um bitmap compactado de 4 bits:


```C++
03 04 05 06 00 06 45 56 67 00 04 78 00 02 05 01 
04 78 00 00 09 1E 00 01 
```



O bitmap é expandido da seguinte maneira (valores de dígito único representam um índice de cor para um único pixel):


```C++
0 4 0 
0 6 0 6 0 
4 5 5 6 6 7 
7 8 7 8 
move current position 5 right and 1 down 
7 8 7 8 
end of line 
1 E 1 E 1 E 1 E 1 
end of RLE bitmap 
```



 

 



