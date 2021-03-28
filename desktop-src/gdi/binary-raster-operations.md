---
description: Esta seção lista os códigos de operação de rasterização binários usados pelas funções GetROP2 e SetROP2. Os códigos de operação de rasterização definem como a GDI combina os bits da caneta selecionada com os bits no bitmap de destino.
ms.assetid: 9a3a5b5d-b41f-4859-8830-98272983a635
title: Operações de rasterização binárias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd8a70030b1940c31d036505a80a6b1868aececd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091224"
---
# <a name="binary-raster-operations"></a>Operações de rasterização binárias

Esta seção lista os códigos de operação de rasterização binários usados pelas funções [**GetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-getrop2) e [**SetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-setrop2) . Os códigos de operação de rasterização definem como a GDI combina os bits da caneta selecionada com os bits no bitmap de destino.

Cada código de operação de rasterização representa uma operação booliana na qual os valores dos pixels na caneta selecionada e no bitmap de destino são combinados. A seguir estão os dois operandos usados nessas operações.



| Operando | Significado            |
|---------|--------------------|
| P       | Caneta selecionada       |
| D       | Bitmap de destino |



 

Os operadores boolianos usados nessas operações são os seguintes.



| Operador | Significado                    |
|----------|----------------------------|
| um        | AND bit a bit                |
| n        | Não-bit (inverso)      |
| o        | OR bit a bit                 |
| x        | Or exclusivo de bit (XOR) |



 

Todas as operações boolianas são apresentadas em notação de polonês reverso. Por exemplo, a operação a seguir substitui os valores dos pixels no bitmap de destino por uma combinação dos valores de pixel da caneta e do pincel selecionado:


```C++
DPo 
```



Cada código de operação de rasterização é um inteiro de 32 bits cuja palavra de ordem superior é um índice de operação booliano e cuja palavra de ordem inferior é o código de operação. O índice de operação de 16 bits é um valor de 8 bits com extensão zero que representa todos os resultados possíveis resultantes da operação booliana em dois parâmetros (nesse caso, os valores de caneta e de destino). Por exemplo, os índices de operação para as operações DPo e DPan são mostrados na lista a seguir.



| P   | D   | DPo | Dpan |
|-----|-----|-----|------|
| 0   | 0   | 0   | 1    |
| 0   | 1   | 1   | 1    |
| 1   | 0   | 1   | 1    |
| 1   | 1   | 1   | 0    |



 

A lista a seguir descreve os modos de desenho e as operações boolianas que eles representam.



| Operação de varredura | Operação booliana |
|------------------|-------------------|
| R2 \_ preto        | 0                 |
| \_COPYPEN R2      | P                 |
| \_MASKNOTPEN R2   | DPna              |
| \_MASKPEN R2      | DPa               |
| \_MASKPENNOT R2   | PDna              |
| \_MERGENOTPEN R2  | DPno              |
| \_MERGEPEN R2     | DPo               |
| \_MERGEPENNOT R2  | PDno              |
| \_Nop R2          | D                 |
| R2 \_ não          | Dn                |
| \_NOTCOPYPEN R2   | NP                |
| \_NOTMASKPEN R2   | DPan              |
| \_NOTMERGEPEN R2  | DPon              |
| \_NOTXORPEN R2    | DPxn              |
| R2 \_ branco        | 1                 |
| \_XORPEN R2       | DPx               |



 

Para um dispositivo monocromático, o GDI mapeia o valor zero para preto e o valor de 1 a branco. Se um aplicativo tentar desenhar com uma caneta preta em um destino branco usando as operações de varredura binária disponíveis, ocorrerão os resultados a seguir.



| Operação de varredura | Resultado             |
|------------------|--------------------|
| R2 \_ preto        | Linha preta visível |
| \_COPYPEN R2      | Linha preta visível |
| \_MASKNOTPEN R2   | Nenhuma linha visível    |
| \_MASKPEN R2      | Linha preta visível |
| \_MASKPENNOT R2   | Linha preta visível |
| \_MERGENOTPEN R2  | Nenhuma linha visível    |
| \_MERGEPEN R2     | Linha preta visível |
| \_MERGEPENNOT R2  | Linha preta visível |
| \_Nop R2          | Nenhuma linha visível    |
| R2 \_ não          | Linha preta visível |
| \_NOTCOPYPEN R2   | Nenhuma linha visível    |
| \_NOTMASKPEN R2   | Nenhuma linha visível    |
| \_NOTMERGEPEN R2  | Linha preta visível |
| \_NOTXORPEN R2    | Linha preta visível |
| R2 \_ branco        | Nenhuma linha visível    |
| \_XORPEN R2       | Nenhuma linha visível    |



 

Para um dispositivo de cores, o GDI usa valores RGB para representar as cores da caneta e o destino. Um valor de cor RGB é um inteiro longo que contém um campo de cor vermelho, verde e azul, cada um especificando a intensidade da cor especificada. As intensidades variam de 0 a 255. Os valores são empacotados nos três bytes de ordem baixa do inteiro longo. A cor de uma caneta é sempre uma cor sólida, mas a cor do destino pode ser uma mistura de duas ou três cores. Se um aplicativo tentar desenhar com uma caneta branca em um destino azul usando as operações de varredura binária disponíveis, ocorrerão os resultados a seguir.



| Operação de varredura | Resultado                 |
|------------------|------------------------|
| R2 \_ preto        | Linha preta visível     |
| \_COPYPEN R2      | Linha branca visível     |
| \_MASKNOTPEN R2   | Linha preta visível     |
| \_MASKPEN R2      | Linha azul invisível    |
| \_MASKPENNOT R2   | Linha vermelha/verde visível |
| \_MERGENOTPEN R2  | Linha azul invisível    |
| \_MERGEPEN R2     | Linha branca visível     |
| \_MERGEPENNOT R2  | Linha branca visível     |
| \_Nop R2          | Linha azul invisível    |
| R2 \_ não          | Linha vermelha/verde visível |
| \_NOTCOPYPEN R2   | Linha preta visível     |
| \_NOTMASKPEN R2   | Linha vermelha/verde visível |
| \_NOTMERGEPEN R2  | Linha preta visível     |
| \_NOTXORPEN R2    | Linha azul invisível    |
| R2 \_ branco        | Linha branca visível     |
| \_XORPEN R2       | Linha vermelha/verde visível |



 

 

 



