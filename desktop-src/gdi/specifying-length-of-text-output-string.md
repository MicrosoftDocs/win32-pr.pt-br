---
description: Várias das funções de fonte e de saída de texto têm um parâmetro que especifica o comprimento da cadeia de caracteres de saída de texto. Um exemplo típico é o parâmetro cchText de DrawTextEx.
ms.assetid: 695fd0f9-abd4-4666-acad-2c409624ddc6
title: Especificando o comprimento da cadeia de caracteres de saída de texto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c120026d1b65170b6fe35bc65400280f6f1ffa5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922500"
---
# <a name="specifying-length-of-text-output-string"></a>Especificando o comprimento da cadeia de caracteres de saída de texto

Várias das funções de fonte e de saída de texto têm um parâmetro que especifica o comprimento da cadeia de caracteres de saída de texto. Um exemplo típico é o parâmetro *cchText* de [**DrawTextEx**](/windows/desktop/api/Winuser/nf-winuser-drawtextexa).

Cada uma dessas funções tem uma versão "ANSI" e uma versão Unicode (por exemplo, [**DrawTextExA**](/windows/desktop/api/Winuser/nf-winuser-drawtextexa) e **DrawTextExW**, respectivamente). Para a versão "ANSI" de cada função, o comprimento é especificado como uma contagem de bytes e para a função Unicode, ele é especificado como uma contagem de palavras.

É tradicional considerar isso como uma "contagem de caracteres". Isso geralmente é preciso para muitas linguagens, incluindo o inglês, mas não é preciso em geral. Em cadeias "ANSI", os caracteres nas páginas de código [SBCS](../intl/single-byte-character-sets.md) usam um byte cada, mas a maioria dos caracteres em páginas de código [DBCS](../intl/double-byte-character-sets.md) leva dois bytes. Da mesma forma, a maioria dos caracteres Unicode atualmente definidos residem no BMP (plano multilíngüe básico) e suas representações UTF-16 se ajustam a uma palavra, mas os caracteres suplementares são representados em Unicode por ' ' substitutos ' ', que exigem duas palavras.

Cada uma dessas funções usa uma contagem de comprimento. Para a versão "ANSI" de cada função, o comprimento é especificado como um comprimento de contagem de bytes de uma cadeia de caracteres que não inclui o terminador **nulo** . Para a função Unicode, a contagem de comprimento é a contagem de bytes dividida por sizeof (WCHAR), que é 2, não incluindo o terminador **nulo** . A contagem de caracteres é a contagem do número de caracteres, que pode não ser igual à contagem de comprimento da cadeia de caracteres. Em alguns casos, os caracteres demoram mais de um BYTE para ANSI (por exemplo, caractere [DBCS](../intl/double-byte-character-sets.md) ) e mais de uma palavra para Unicode (por exemplo, caracteres substitutos). Além disso, o número de glifos pode não ser igual ao número de caracteres porque vários caracteres podem ser compostos para criar um glifo. Contagem de comprimento é a quantidade de dados. Contagem de caracteres é o número de unidades processadas como uma entidade. Os glifos são renderizados. Por exemplo, em Unicode, você pode ter uma cadeia de caracteres com comprimento de 3, que tem 2 caracteres e que resulta em um glifo sendo renderizado. No entanto, normalmente, a maioria das cadeias de caracteres Unicode comprimento, contagem de caractere e número de glifos renderizados são iguais.

Você pode usar \_ tcslen () para obter o comprimento da cadeia de caracteres. Para ANSI, \_ tcslen () retorna o número de bytes. Para Unicode, \_ tcslen () retorna o número de WCHARs (ou seja, palavras).

Caracteres especiais de processamento, como guias e hifens suaves que nem sempre são desenhados, podem afetar a saída desenhada. Eles são incluídos no comprimento e nas contagens de caracteres da cadeia de caracteres, mas podem não ser representados diretamente por um glifo renderizado.

Algumas dessas funções permitem que o chamador especifique o comprimento como-1 para indicar que a cadeia de caracteres é terminada em nulo; Nesse caso, a função calculará automaticamente a contagem de caracteres. Nem todas as funções oferecem esse recurso. Que é especificado em uma base função a função; consulte a documentação da função individual.

 

 
