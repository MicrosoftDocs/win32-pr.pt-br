---
description: Um DBCS (conjunto de caracteres de dois bytes), também conhecido como um &0034; um conjunto de \# caracteres de 8 bits expandido&\# 0034;, é um SBCS (conjunto de caracteres de byte único) estendido, implementado como uma página de código.
ms.assetid: df049d22-02e2-48b2-8b74-52f71c00c549
title: Conjuntos de caracteres de byte duplo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 431b762b19f5531644e4bbaace548f34245c9d5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105789793"
---
# <a name="double-byte-character-sets"></a>Conjuntos de caracteres de byte duplo

Um DBCS (conjunto de caracteres de dois bytes), também conhecido como "conjunto de caracteres de 8 bits expandido", é um conjunto de caracteres estendido de [byte único](single-byte-character-sets.md) (SBCS), implementado como uma página de código. Os DBCS foram desenvolvidos originalmente para estender o design de SBCS para lidar com linguagens como japonês e chinês. Alguns caracteres em um DBCS, incluindo os dígitos e as letras usados para escrever em inglês, têm valores de código de byte único. Outros caracteres, como ideogramas de chinês ou japonês kanji, têm valores de código de dois bytes. Um DBCS pode corresponder a uma página de código do Windows ou a uma página de código OEM. Uma página de código DBCS também pode incluir uma página de código não nativa, por exemplo, uma página de código EBCDIC. Para obter definições dessas páginas de código, consulte [páginas de código](code-pages.md).

> [!Note]  
> Novos aplicativos do Windows devem usar [Unicode](unicode.md) para evitar as inconsistências de páginas de código variadas e para facilitar a localização. No entanto, alguns protocolos herdados podem exigir o uso de páginas de código DBCS. Cada página de código DBCS dá suporte a caracteres diferentes, mas nenhuma página dá suporte a toda a amplitude de caracteres fornecida pelo Unicode. Cada página de código DBCS dá suporte a um subconjunto diferente, codificado de forma diferente. Os dados convertidos de uma página de código DBCS para outro estão sujeitos a corrupção porque o mesmo valor de dados em páginas de código diferentes pode codificar um caractere diferente. Os dados convertidos de Unicode para DBCS estão sujeitos à perda de dados, pois uma determinada página de código pode não ser capaz de representar todos os caracteres usados nesses dados Unicode específicos.

 

Para interpretar uma cadeia de caracteres DBCS, um aplicativo deve começar no início da cadeia de caracteres e continuar a verificação. Ele controla quando encontra um byte de Lead na cadeia de caracteres e trata o próximo byte como a parte à direita do mesmo caractere. Se o aplicativo simplesmente examina a cadeia de caracteres um byte por vez e encontra um byte que parece ser o valor do código que representa uma barra invertida (" \\ "), esse byte pode simplesmente ser o byte final de um caractere de dois bytes. O aplicativo não pode apenas fazer backup de um byte para ver se o byte anterior é um byte de Lead, pois esse valor de byte pode estar qualificado para ser usado como um byte de Lead e um byte de trilha. Assim, o aplicativo tem, essencialmente, o mesmo problema que com a barra invertida possível. Em outras palavras, as pesquisas de subcadeias são muito mais complicadas com um DBCS do que com SBCS ou Unicode. Da mesma forma, os aplicativos que dão suporte a um DBCS devem usar funções especiais, como [ \_ mbsstr](/cpp/c-runtime-library/reference/strstr-wcsstr-mbsstr-mbsstr-l), em vez da função [**StrStr**](https://msdn.microsoft.com/library/z9da80kz(v=VS.71).aspx) .

Seus aplicativos usam páginas de código do Windows DBCS com as versões "A" do Windows functions. Consulte [convenções para protótipos de função](conventions-for-function-prototypes.md) e [páginas de código](code-pages.md). Para ajudar a identificar uma página de código DBCS, um aplicativo pode usar a função [**GetCPInfo**](/windows/desktop/api/Winnls/nf-winnls-getcpinfo) ou [**GetCPInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getcpinfoexa) . Um aplicativo pode usar a função [**IsDBCSLeadByte**](/windows/desktop/api/Winnls/nf-winnls-isdbcsleadbyte) para determinar se um determinado valor pode ser usado como o byte de avanço de um caractere de 2 bytes. Além disso, um aplicativo pode usar as funções [**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) e [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) para mapear entre cadeias de caracteres Unicode e DBCS.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Conjuntos de caracteres](character-sets.md)
</dt> <dt>

[Conjuntos de caracteres de byte único](single-byte-character-sets.md)
</dt> </dl>

 

 
