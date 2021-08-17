---
description: Um DBCS (conjunto de caracteres de dois byte), também conhecido como um &0034;conjunto de caracteres expandido de 8 bits \#&0034; é um SBCS (conjunto de caracteres de byte único) estendido, implementado como uma página de \# código.
ms.assetid: df049d22-02e2-48b2-8b74-52f71c00c549
title: Conjuntos de caracteres de byte duplo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dbef827b91c5ed2468b06f759883c0ba0b874e74038871227aabe0f65f1a046
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119147659"
---
# <a name="double-byte-character-sets"></a>Conjuntos de caracteres de byte duplo

Um DBCS (conjunto de caracteres de byte duplo), também conhecido como "conjunto de caracteres expandido de 8 bits", é um SBCS (conjunto de caracteres de [byte](single-byte-character-sets.md) único) estendido, implementado como uma página de código. Os DBCSs foram originalmente desenvolvidos para estender o design SBCS para lidar com idiomas como japonês e chinês. Alguns caracteres em um DBCS, incluindo os dígitos e letras usados para escrever inglês, têm valores de código de byte único. Outros caracteres, como ideogramas chineses ou kanji japonês, têm valores de código de byte duplo. Um DBCS pode corresponder a uma página Windows código ou a uma página de código OEM. Uma página de código DBCS também pode incluir uma página de código não nativa, por exemplo, uma página de código EBCDIC. Para definições dessas páginas de código, consulte [Páginas de Código](code-pages.md).

> [!Note]  
> Novos Windows aplicativos devem usar [Unicode](unicode.md) para evitar inconsistências de páginas de código variadas e para facilitar a localização. No entanto, alguns protocolos herdadas podem exigir o uso de páginas de código DBCS. Cada página de código DBCS dá suporte a caracteres diferentes, mas nenhuma página dá suporte à amplitude completa de caracteres fornecidos pelo Unicode. Cada página de código DBCS dá suporte a um subconjunto diferente, codificado de maneira diferente. Os dados convertidos de uma página de código DBCS para outra estão sujeitos a corrupção porque o mesmo valor de dados em páginas de código diferentes pode codificar um caractere diferente. Os dados convertidos de Unicode para DBCS estão sujeitos à perda de dados, porque uma determinada página de código pode não ser capaz de representar todos os caracteres usados nos dados Unicode específicos.

 

Para interpretar uma cadeia de caracteres DBCS, um aplicativo deve começar no início da cadeia de caracteres e examinar para frente. Ele acompanha quando encontra um byte de lead na cadeia de caracteres e trata o próximo byte como a parte à frente do mesmo caractere. Se o aplicativo simplesmente examina a cadeia de caracteres um byte por vez e encontra um byte que parece ser o valor de código que representa uma barras invertida (" "), esse byte pode simplesmente ser o byte à trilha de um caractere de dois \\ byte. O aplicativo não pode apenas fazer o back-up de um byte para ver se o byte anterior é um byte principal, pois esse valor de byte pode ser qualificado para ser usado como um byte de lead e um byte à trilha. Portanto, o aplicativo tem essencialmente o mesmo problema com ele que com a possível invertida. Em outras palavras, as pesquisas de substring são muito mais complicadas com um DBCS do que com SBCSs ou Unicode. Da mesma forma, os aplicativos que suportam um DBCS devem usar funções especiais, como [ \_ mbsstr](/cpp/c-runtime-library/reference/strstr-wcsstr-mbsstr-mbsstr-l), em vez da [**função StrStr.**](https://msdn.microsoft.com/library/z9da80kz(v=VS.71).aspx)

Seus aplicativos usam DBCS Windows páginas de código com as versões "A" das Windows funções. Consulte [Convenções para protótipos de função e](conventions-for-function-prototypes.md) páginas de [código](code-pages.md). Para ajudar a identificar uma página de código DBCS, um aplicativo pode usar a [**função GetCPInfo**](/windows/desktop/api/Winnls/nf-winnls-getcpinfo) ou [**GetCPInfoEx.**](/windows/desktop/api/Winnls/nf-winnls-getcpinfoexa) Um aplicativo pode usar a [**função IsDBCSLeadByte**](/windows/desktop/api/Winnls/nf-winnls-isdbcsleadbyte) para determinar se um determinado valor pode ser usado como o byte principal de um caractere de 2 byte. Além disso, um aplicativo pode usar as funções [**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) e [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) para mapear entre cadeias de caracteres Unicode e DBCS.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Conjuntos de caracteres](character-sets.md)
</dt> <dt>

[Conjuntos de caracteres de byte único](single-byte-character-sets.md)
</dt> </dl>

 

 
