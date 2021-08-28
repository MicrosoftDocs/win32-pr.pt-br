---
description: O Unicode é um padrão mundial de codificação de caracteres. O sistema usa Unicode exclusivamente para manipulação de caracteres e cadeias de caracteres. Para obter uma descrição detalhada de todos os aspectos do Unicode, consulte o padrão Unicode.
ms.assetid: ca5bcdee-ea13-4745-a565-5426c462892d
title: Unicode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c99a7af4d4fbb6b7783f97ceba37b1bf6b0bf54811beaf9c7c2348ec0125c73b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764766"
---
# <a name="unicode"></a>Unicode

O Unicode é um padrão mundial de codificação de caracteres. O sistema usa Unicode exclusivamente para manipulação de caracteres e cadeias de caracteres. Para obter uma descrição detalhada de todos os aspectos do Unicode, consulte [o padrão Unicode](https://www.unicode.org/standard/standard.html).

Em comparação com os mecanismos mais antigos para manipulação de caracteres e dados de cadeia de caracteres, o Unicode simplifica a localização de software e melhora o processamento de texto multilíngüe. Usando o Unicode para representar dados de caractere e de cadeia de caracteres em seus aplicativos, você pode habilitar recursos de troca de dados universal para marketing global, usando um único arquivo binário para cada código de caractere possível. O Unicode faz o seguinte:

-   Permite a coexistência de qualquer combinação de caracteres, extraída de qualquer combinação de scripts e idiomas, para coexistir em um único documento.
-   Define a semântica para cada caractere.
-   Padroniza o comportamento do script.
-   Fornece um algoritmo padrão para texto bidirecional.
-   Define os mapeamentos cruzados para outros padrões.
-   Define várias codificações de seu único conjunto de caracteres: UTF-7, UTF-8, UTF-16 e UTF-32. A conversão de dados entre essas codificações é sem perdas.

O Unicode dá suporte a vários scripts usados por linguagens em todo o mundo e também um grande número de símbolos técnicos e caracteres especiais usados na publicação. Os scripts com suporte incluem, mas não estão limitados a, Latin, grego, cirílico, Hebraico, árabe, devanágari, tailandês, Han, Hangul, hiragana e Katakana. Os idiomas com suporte incluem, mas não se limitam a, alemão, francês, inglês, grego, russo, Hebraico, árabe, híndi, tailandês, chinês, coreano e japonês. Atualmente, o Unicode pode representar a grande maioria dos caracteres no uso do computador moderno em todo o mundo e continua a ser atualizado para torná-lo ainda mais completo.

As funções habilitadas para Unicode são descritas em [convenções para protótipos de função](conventions-for-function-prototypes.md). essas funções usam codificação UTF-16 (caracteres largos), que é a codificação mais comum do Unicode e a usada para a codificação unicode nativa em sistemas operacionais Windows. Cada valor de código tem 16 bits de largura, em oposição à abordagem de [página de código](code-pages.md) mais antiga para caracteres e dados de cadeia de caracteres, que usa valores de código de 8 bits. O uso de 16 bits permite a codificação direta de 65.536 caracteres. Na verdade, o universo de símbolos usados para transcrever linguagens humanas é ainda maior que isso, e pontos de código UTF-16 no intervalo de U + D800 até U + DFFF são usados para formar pares substitutos, que constituem codificações de 32 bits de caracteres suplementares. Consulte [substitutos e caracteres suplementares](surrogates-and-supplementary-characters.md) para mais discussões.

O conjunto de caracteres Unicode inclui vários caracteres combináveis, como U + 0308 ("̈"), uma combinação de trema ou trema. O Unicode geralmente pode representar o mesmo glifo em um formato ' ' composto ' ' ou ' ' decomposto ' ': por exemplo, a forma composta de "Ä" é o único ponto de código Unicode "Ä" (U + 00C4), enquanto seu formulário decomposto é "A" + "̈" (U + 0041 U + 0308). O Unicode não define um formulário composto para cada glifo. Por exemplo, o "o" em vietnamita com acento circunflexo e til ("ỗ") é representado por U + 006f U + 0302 U + 0303 (o + acento circunflexo + til). Para uma discussão adicional sobre a combinação de caracteres e problemas relacionados, consulte [usando a normalização Unicode para representar cadeias](using-unicode-normalization-to-represent-strings.md).

Para compatibilidade com ambientes de 8 e 7 bits, o Unicode também pode ser codificado como UTF-8 e UTF-7, respectivamente. embora as funções habilitadas para Unicode no Windows usem utf-16, também é possível trabalhar com dados codificados em utf-8 ou utf-7, que têm suporte em Windows como páginas de [código](code-pages.md)de conjunto de caracteres multibyte.

novos aplicativos Windows devem usar UTF-16 como sua representação de dados interna. Windows também fornece amplo suporte para páginas de código e uso misto no mesmo aplicativo é possível. Até mesmo os novos aplicativos baseados em Unicode às vezes precisam trabalhar com páginas de código. Os motivos para isso são discutidos em [páginas de código](code-pages.md).

Um aplicativo pode usar as funções [**MultiByteToWideChar**](/windows/win32/api/Stringapiset/nf-stringapiset-multibytetowidechar) e [**WideCharToMultiByte**](/windows/win32/api/Stringapiset/nf-stringapiset-widechartomultibyte) para converter entre cadeias de caracteres com base em páginas de código e em cadeias de caracteres Unicode. Embora seus nomes se refiram a "MultiByte", essas funções funcionam igualmente bem com SBCS ( [conjunto de caracteres de byte único](single-byte-character-sets.md) ), DBCS ( [conjunto de caracteres de byte duplo](double-byte-character-sets.md) ) e páginas de código de MBCS (conjunto de caracteres MultiByte).

normalmente, um aplicativo Windows deve usar o UTF-16 internamente, convertendo somente como parte de uma "camada fina" pela interface que deve usar outro formato. Essa técnica defende contra perda e corrupção de dados. Cada página de código dá suporte a diferentes caracteres, mas nenhum deles dá suporte ao espectro completo de caracteres fornecidos pelo Unicode. A maioria das páginas de código dá suporte a diferentes subconjuntos, codificados de forma diferente. As páginas de código para UTF-8 e UTF-7 são uma exceção, pois elas dão suporte ao conjunto de caracteres Unicode completo e a conversão entre essas codificações e UTF-16 é sem perdas.

Os dados convertidos diretamente da codificação usada por uma página de código para a codificação usada por outro estão sujeitos a corrupção, pois o mesmo valor de dados em páginas de código diferentes pode codificar um caractere diferente. Mesmo quando o aplicativo está convertendo o mais próximo possível da interface, você deve pensar cuidadosamente sobre o intervalo de dados a ser manipulado.

Os dados convertidos de Unicode em uma página de código estão sujeitos à perda de dados, pois uma determinada página de código pode não ser capaz de representar todos os caracteres usados nesses dados Unicode específicos. Portanto, observe que [**WideCharToMultiByte**](/windows/win32/api/Stringapiset/nf-stringapiset-widechartomultibyte) pode perder alguns dados se a página de código de destino não puder representar todos os caracteres na cadeia de caracteres Unicode.

Ao modernizar aplicativos herdados baseados em página de código para usar Unicode, você pode usar funções genéricas e a macro de [**texto**](/windows/win32/api/Winnt/nf-winnt-text) para manter um único conjunto de fontes da qual Compilar duas versões do seu aplicativo. uma versão dá suporte a Unicode e a outra funciona com Windows páginas de código. usando esse mecanismo, você pode converter até mesmo aplicativos muito grandes de Windows páginas de código para Unicode e, ao mesmo tempo, manter as fontes de aplicativo que podem ser compiladas, criadas e testadas em todas as fases da conversão. Para obter mais informações, consulte [convenções para protótipos de função](conventions-for-function-prototypes.md).

Os caracteres e cadeias Unicode usam tipos de dados que são diferentes daqueles para cadeias de caracteres de códigos baseados em página de código. Juntamente com uma série de macros e convenções de nomenclatura, essa distinção minimiza a chance de misturar acidentalmente os dois tipos de dados de caractere. Ele facilita a verificação do tipo de compilador para garantir que apenas valores de parâmetro Unicode sejam usados com funções que esperam cadeias de caracteres Unicode.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Conjuntos de caracteres](character-sets.md)
</dt> <dt>

[Classificação](sorting.md)
</dt> <dt>

[Caracteres substitutos e suplementares](surrogates-and-supplementary-characters.md)
</dt> <dt>

[Usando a normalização Unicode para representar cadeias de caracteres](using-unicode-normalization-to-represent-strings.md)
</dt> </dl>

 

 



