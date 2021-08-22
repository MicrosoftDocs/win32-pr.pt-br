---
description: Um metadado aprimorado é uma matriz de registros.
ms.assetid: af3261c7-2113-4777-97c0-504f23022550
title: Registros de metadados aprimorados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 506ca77dda1bd90fc04b692dbbd98bc06f4da44c5fc6f8edb0fd17cbd3e94c96
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119038014"
---
# <a name="enhanced-metafile-records"></a>Registros de metadados aprimorados

Um metadado aprimorado é uma matriz de registros. Um registro de metadados é uma estrutura [**EN FOCALARECORD**](/windows/win32/api/wingdi/ns-wingdi-enhmetarecord) de comprimento variável. No início de cada registro de metadados aprimorado há uma [**estrutura EMR,**](/windows/win32/api/wingdi/ns-wingdi-emr) que contém dois membros. O primeiro membro, iType, identifica o tipo de registro, ou seja, a função GDI cujos parâmetros estão contidos no registro. Como as estruturas são variáveis de comprimento, o outro membro, nSize, contém o tamanho do registro. Imediatamente após o membro nSize estão os parâmetros restantes, se for o caso, da função GDI. O restante da estrutura contém dados adicionais que dependem do tipo de registro.

O primeiro registro em um metadado aprimorado é sempre a estrutura [**EN LTDAHEADER,**](/windows/win32/api/wingdi/ns-wingdi-enhmetaheader) que é o header enhanced-metafile. O header especifica as seguintes informações:

-   Tamanho do metadado, em bytes
-   Dimensões do quadro de imagem, em unidades de dispositivo
-   Dimensões do quadro de imagem, em unidades de milímetros .01
-   Número de registros no metadado
-   Deslocamento para uma descrição de texto opcional
-   Tamanho da paleta opcional
-   Resolução do dispositivo original, em pixels
-   Resolução do dispositivo original, em milímetros

Uma descrição de texto opcional pode seguir o registro de header. A descrição do texto descreve a imagem e o nome do autor. A paleta opcional especifica as cores usadas para criar o metadado aprimorado. Os registros restantes identificam as funções GDI usadas para criar a imagem. A saída hexadecimal a seguir corresponde a um registro gerado para uma chamada à [**função SetMapMode.**](/windows/desktop/api/Wingdi/nf-wingdi-setmapmode)


```C++
00000011 0000000C 00000004 
```



O valor 0x00000011 especifica o tipo de registro (corresponde à constante EMR SETMAPMODE definida no arquivo \_ Wingdi.h). O valor 0x0000000C especifica o comprimento do registro, em bytes. O valor 0x00000004 identifica o modo de mapeamento (corresponde à constante MM \_ LOENGLISH definida na [**função SetMapMode).**](/windows/desktop/api/Wingdi/nf-wingdi-setmapmode)

Para obter uma lista de tipos de registro adicionais, consulte [Estruturas de metadados](metafile-structures.md).

 

 



