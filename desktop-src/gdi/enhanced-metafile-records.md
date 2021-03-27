---
description: Um metarquivo avançado é uma matriz de registros.
ms.assetid: af3261c7-2113-4777-97c0-504f23022550
title: Registros de metarquivo avançados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2097fd59497838c2a77a0209f6ae715dff2e1cf9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967667"
---
# <a name="enhanced-metafile-records"></a>Registros de metarquivo avançados

Um metarquivo avançado é uma matriz de registros. Um registro de metarquivo é uma estrutura de [**ENHMETARECORD**](/windows/win32/api/wingdi/ns-wingdi-enhmetarecord) de comprimento variável. No início de cada registro de metarquivo avançado está uma estrutura [**EMR**](/windows/win32/api/wingdi/ns-wingdi-emr) , que contém dois membros. O primeiro membro, iType, identifica o tipo de registro que é, a função GDI cujos parâmetros estão contidos no registro. Como as estruturas são variáveis de comprimento, o outro membro, nSize, contém o tamanho do registro. Imediatamente após o membro nSize estão os parâmetros restantes, se houver, da função GDI. O restante da estrutura contém dados adicionais que dependem do tipo de registro.

O primeiro registro em um metarquivo avançado é sempre a estrutura [**ENHMETAHEADER**](/windows/win32/api/wingdi/ns-wingdi-enhmetaheader) , que é o cabeçalho Enhanced-Metafile. O cabeçalho especifica as seguintes informações:

-   Tamanho do metarquivo, em bytes
-   Dimensões do quadro de imagem, em unidades de dispositivo
-   Dimensões do quadro de imagem, em unidades de 01 a milímetros
-   Número de registros no metarquivo
-   Deslocamento para uma descrição de texto opcional
-   Tamanho da paleta opcional
-   Resolução do dispositivo original, em pixels
-   Resolução do dispositivo original, em milímetros

Uma descrição de texto opcional pode seguir o registro de cabeçalho. A descrição do texto descreve a imagem e o nome do autor. A paleta opcional especifica as cores usadas para criar o metarquivo avançado. Os registros restantes identificam as funções GDI usadas para criar a imagem. A seguinte saída hexadecimal corresponde a um registro gerado para uma chamada para a função [**SetMapMode**](/windows/desktop/api/Wingdi/nf-wingdi-setmapmode) .


```C++
00000011 0000000C 00000004 
```



O valor 0x00000011 especifica o tipo de registro (corresponde à \_ constante EMR SETMAPMODE definida no arquivo WinGDI. h). O valor 0x0000000C especifica o comprimento do registro, em bytes. O valor 0x00000004 identifica o modo de mapeamento (corresponde à \_ constante mm LOENGLISH definida na função [**SetMapMode**](/windows/desktop/api/Wingdi/nf-wingdi-setmapmode) ).

Para obter uma lista de tipos de registro adicionais, consulte [estruturas de metarquivo](metafile-structures.md).

 

 



