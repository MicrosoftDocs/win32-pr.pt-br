---
description: Windows dá suporte a formatos para compactar bitmaps que definem suas cores com 8 ou 4 bits por pixel. A compactação reduz o armazenamento de disco e memória necessário para o bitmap.
ms.assetid: 14d14662-910a-4f3f-914e-6ccfc602c822
title: Compactação de bitmap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 462b41bffe207aecc82deece7e2090cfe6389635
ms.sourcegitcommit: 8eb9ae480cf2cb3524d83a1e7adcdaa875d625e0
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2021
ms.locfileid: "123096442"
---
# <a name="bitmap-compression"></a>Compactação de bitmap

Windows dá suporte a formatos para compactar bitmaps que definem suas cores com 8 ou 4 bits por pixel. A compactação reduz o armazenamento de disco e memória necessário para o bitmap.

Quando o membro **compactação** da estrutura de header de informações de bitmap é BI RLE8, um formato RLE (codificação de comprimento de run)é usado para compactar um bitmap de \_ 8 bits. Esse formato pode ser compactado em modos codificados ou absolutos. Ambos os modos podem ocorrer em qualquer lugar no mesmo bitmap:

-   *O modo codificado* consiste em dois bytes: o primeiro byte especifica o número de pixels consecutivos a serem desenhados usando o índice de cores contido no segundo byte. Além disso, o primeiro byte do par pode ser definido como zero para indicar um caractere de escape que indica o final de uma linha, o final de um bitmap ou um delta, dependendo do valor do segundo byte. A interpretação do escape depende do valor do segundo byte do par, que pode ser um dos valores a seguir.



| Valor | Significado                                                                                                                                                |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | Fim da linha.                                                                                                                                           |
| 1     | Fim do bitmap.                                                                                                                                         |
| 2     | Delta. Os 2 bytes após o escape contêm valores não assinados que indicam o deslocamento para a direita e para cima do próximo pixel da posição atual. |



 

-   No *modo absoluto*, o primeiro byte é zero e o segundo byte é um valor no intervalo de 03H a FFH. O segundo byte representa o número de bytes a seguir, cada um deles contém o índice de cores de um único pixel. Quando o segundo byte é dois ou menos, o escape tem o mesmo significado que o modo codificado. No modo absoluto, cada executar deve ter preenchimento zero para terminar em um limite de palavra de 16 bits.

O exemplo a seguir mostra os valores hexadecimais de um bitmap compactado de 8 bits:


```C++
[03 04] [05 06] [00 03 45 56 67 00] [02 78] [00 02 05 01] 
[02 78] [00 00] [09 1E] [00 01] 
```



O bitmap expande da seguinte forma (valores de dois dígitos representam um índice de cores para um único pixel):


```C++
04 04 04 
06 06 06 06 06 
45 56 67 
78 78 
move current position 5 right and 1 up 
78 78 
end of line 
1E 1E 1E 1E 1E 1E 1E 1E 1E 
end of RLE bitmap 
```



Quando o membro **compression** é BI RLE4, o bitmap é compactado usando um formato de codificação de comprimento de run para um bitmap de 4 bits, que também usa modos codificados e \_ absolutos:

-   No modo codificado, o primeiro byte do par contém o número de pixels a serem desenhados usando os índices de cores no segundo byte. O segundo byte contém dois índices de cores, um em seus 4 bits de ordem alta e outro em seus 4 bits de ordem baixa. O primeiro dos pixels é desenhado usando a cor especificada pelos 4 bits de ordem alta, o segundo é desenhado usando a cor nos 4 bits de ordem baixa, o terceiro é desenhado usando a cor nos 4 bits de ordem alta e assim por diante, até que todos os pixels especificados pelo primeiro byte sejam desenhados.
-   No modo absoluto, o primeiro byte é zero. O segundo byte contém o número de índices de cores a seguir. Os bytes subsequentes contêm índices de cores em seus 4 bits de ordem alta e baixa, um índice de cores para cada pixel. No modo absoluto, cada executar deve ser alinhada em um limite de palavra. Os escapes de fim de linha, fim de bitmap e delta descritos para BI RLE8 também se aplicam à \_ \_ compactação RLE4 de BI.

O exemplo a seguir mostra os valores hexadecimais de um bitmap compactado de 4 bits:


```C++
03 04 05 06 00 06 45 56 67 00 04 78 00 02 05 01 
04 78 00 00 09 1E 00 01 
```



O bitmap expande da seguinte forma (valores de dígito único representam um índice de cores para um único pixel):


```C++
0 4 0 
0 6 0 6 0 
4 5 5 6 6 7 
7 8 7 8 
move current position 5 right and 1 up 
7 8 7 8 
end of line 
1 E 1 E 1 E 1 E 1 
end of RLE bitmap 
```



 

 



