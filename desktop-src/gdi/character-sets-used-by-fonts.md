---
description: Todas as fontes usam um conjunto de caracteres. Um conjunto de caracteres contém marcas de pontuação, numerais, letras maiúsculas e minúsculas e todos os outros caracteres imprimíveis. Cada elemento de um conjunto de caracteres é identificado por um número.
ms.assetid: 7989c59e-2ec6-4d1a-bb86-f4037ca32764
title: Conjuntos de caracteres usados por fontes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e33c4c5cc193c4474b39113acdedafec699456e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967712"
---
# <a name="character-sets-used-by-fonts"></a>Conjuntos de caracteres usados por fontes

Todas as fontes usam um conjunto de caracteres. Um conjunto de caracteres contém marcas de pontuação, numerais, letras maiúsculas e minúsculas e todos os outros caracteres imprimíveis. Cada elemento de um conjunto de caracteres é identificado por um número.

A maioria dos conjuntos de caracteres em uso são subconjuntos do conjunto de caracteres ASCII dos EUA, que define caracteres para os valores numéricos 96 de 32 a 127. Há cinco grupos principais de conjuntos de caracteres:

-   Windows
-   Unicode
-   OEM (fabricante original do equipamento)
-   Símbolo
-   Específico do fornecedor

## <a name="windows-character-set"></a>Conjunto de caracteres do Windows

O conjunto de caracteres do Windows é o conjunto de caracteres usado com mais frequência. Ele é essencialmente equivalente ao conjunto de caracteres ANSI. O caractere em branco é o primeiro caractere no conjunto de caracteres do Windows. Ele tem um valor hexadecimal de 0x20 (decimal 32). O último caractere no conjunto de caracteres do Windows tem um valor hexadecimal de 0xFF (decimal 255).

Muitas fontes especificam um caractere padrão. Sempre que uma solicitação é feita para um caractere que não está na fonte, o sistema fornece esse caractere padrão. Muitas fontes que usam o conjunto de caracteres do Windows especificam o ponto final (.) como o caractere padrão. As fontes TrueType e OpenType normalmente usam uma caixa aberta como o caractere padrão.

As fontes usam um caractere de quebra chamado Quad para separar palavras e justificar o texto. A maioria das fontes usando o conjunto de caracteres do Windows especifica que o caractere em branco funcionará como o caractere de quebra.

## <a name="unicode-character-set"></a>Conjunto de caracteres Unicode

O conjunto de caracteres do Windows usa 8 bits para representar cada caractere; Portanto, o número máximo de caracteres que podem ser expressos usando 8 bits é 256 (2 ^ 8). Isso geralmente é suficiente para idiomas ocidentais, incluindo as marcas de sinais diacríticos usadas em francês, alemão, espanhol e outras linguagens. No entanto, as linguagens do leste empregam milhares de caracteres separados, que não podem ser codificados usando um esquema de codificação de byte único. Com a proliferação do comércio de computadores, esquemas de codificação de dois bytes foram desenvolvidos para que os caracteres pudessem ser representados em sequências de 8 bits, 16 bits, 24 bits ou 32 bits. Isso requer algoritmos de passagem complicados; mesmo assim, o uso de diferentes conjuntos de código poderia gerar resultados totalmente diferentes em dois computadores diferentes.

Para resolver o problema de vários esquemas de codificação, o padrão Unicode para representação de dados foi desenvolvido. Um esquema de codificação de caracteres de 16 bits, o Unicode pode representar 65.536 (2 ^ 16) caracteres, o que é suficiente para incluir todos os idiomas no comércio do computador hoje, bem como marcas de pontuação, símbolos matemáticos e espaço para expansão. O Unicode estabelece um código exclusivo para cada caractere para garantir que a conversão de caracteres seja sempre precisa.

## <a name="oem-character-set"></a>Conjunto de caracteres OEM

O conjunto de caracteres OEM é normalmente usado em sessões de tela inteira do MS-DOS para exibição de tela. Os caracteres de 32 a 127 geralmente são os mesmos nos conjuntos de caracteres OEM, ASCII e Windows. Os outros caracteres no conjunto de caracteres OEM (0 a 31 e 128 a 255) correspondem aos caracteres que podem ser exibidos em uma sessão do MS-DOS de tela inteira. Esses caracteres são geralmente diferentes dos caracteres do Windows.

## <a name="symbol-character-set"></a>Conjunto de caracteres de símbolo

O conjunto de caracteres de símbolo contém caracteres especiais normalmente usados para representar fórmulas matemáticas e científicas.

## <a name="vendor-specific-character-sets"></a>Conjuntos de caracteres específicos do fornecedor

Muitas impressoras e outros dispositivos de saída fornecem fontes baseadas em conjuntos de caracteres que diferem do exemplo de setsfor do Windows e OEM, o conjunto de caracteres de Extended Binary Coded Decimal Interchange Code (EBCDIC). Para usar um desses conjuntos de caracteres, o driver de impressora é convertido do conjunto de caracteres do Windows para o conjunto de caracteres específicos do fornecedor.

 

 



