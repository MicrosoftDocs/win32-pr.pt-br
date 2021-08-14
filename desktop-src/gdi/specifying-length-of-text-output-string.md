---
description: Várias das funções de fonte e saída de texto têm um parâmetro que especifica o comprimento da cadeia de caracteres de saída de texto. Um exemplo típico é o parâmetro cchText de DrawTextEx.
ms.assetid: 695fd0f9-abd4-4666-acad-2c409624ddc6
title: Especificando o comprimento da cadeia de caracteres de saída de texto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e35a673a23a310da33536f389c85a44af68b895e4f05e0a0f835656e7bc3fbd5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117885944"
---
# <a name="specifying-length-of-text-output-string"></a>Especificando o comprimento da cadeia de caracteres de saída de texto

Várias das funções de fonte e saída de texto têm um parâmetro que especifica o comprimento da cadeia de caracteres de saída de texto. Um exemplo típico é o *parâmetro cchText* de [**DrawTextEx.**](/windows/desktop/api/Winuser/nf-winuser-drawtextexa)

Cada uma dessas funções tem uma versão "ANSI" e uma versão Unicode (por exemplo, [**DrawTextExA**](/windows/desktop/api/Winuser/nf-winuser-drawtextexa) e **DrawTextExW,** respectivamente). Para a versão "ANSI" de cada função, o comprimento é especificado como uma contagem de BYTE e para a função Unicode é especificado como uma contagem de WORD.

É tradicional pensar nisso como uma "contagem de caracteres". Isso geralmente é preciso para muitos idiomas, incluindo inglês, mas não é preciso em geral. Em cadeias de caracteres "ANSI", os caracteres nas páginas de código [SBCS](../intl/single-byte-character-sets.md) levam um byte cada, mas a maioria dos caracteres nas páginas de código [DBCS](../intl/double-byte-character-sets.md) leva dois bytes. Da mesma forma, a maioria dos caracteres Unicode definidos atualmente residem no BMP (Plano Multilíngue Básico) e suas representações UTF-16 se ajustam em um WORD, mas caracteres suplementares são representados em Unicode por ''substitutos'' que exigem dois WORDs.

Cada uma dessas funções tem uma contagem de comprimento. Para a versão "ANSI" de cada função, o comprimento é especificado como um comprimento de contagem de BYTE de uma cadeia de caracteres que não inclui o terminador **NULL.** Para a função Unicode, a contagem de comprimento é a contagem de byte dividida por sizeof(WCHAR), que é 2, não incluindo o terminador **NULL.** A contagem de caracteres é a contagem do número de caracteres, que pode não ser igual à contagem de comprimento da cadeia de caracteres. Em alguns casos, os caracteres levam mais de um BYTE para ANSI (por exemplo, caractere [DBCS)](../intl/double-byte-character-sets.md) e mais de uma PALAVRA para Unicode (por exemplo, caracteres substitutos). Além disso, o número de glifos pode não ser igual ao número de caracteres porque vários caracteres podem ser compostos para fazer um glifo. A contagem de comprimento é a quantidade de dados. Contagem de caracteres é o número de unidades processadas como uma entidade. Glifos são o que é renderizado. Por exemplo, em Unicode, você pode ter uma cadeia de caracteres com comprimento de 3, que é de 2 caracteres e que resulta em 1 glifo sendo renderizado. No entanto, normalmente, a maioria dos comprimentos de cadeias de caracteres Unicode, a contagem de caracteres e o número de glifos renderizados são iguais.

Você pode usar \_ tcslen() para obter o comprimento da cadeia de caracteres. Para ANSI, \_ tcslen() retorna o número de bytes. Para Unicode, \_ tcslen() retorna o número de WCHARs (ou seja, WORDs).

Caracteres de processamento especiais, como guias e hifens suaves que nem sempre são desenhados, podem afetar a saída desenhada. Eles são incluídos nas contagens de caracteres e comprimento da cadeia de caracteres, mas podem não ser representados diretamente por um glifo renderizado.

Algumas dessas funções permitem que o chamador especifique o comprimento como -1 para indicar que a cadeia de caracteres é terminada em nulo; nesse caso, a função calculará a contagem de caracteres automaticamente. Nem todas as funções oferecem essa funcionalidade. Isso é especificado de acordo com a função; consulte a documentação da função individual.

 

 
