---
description: Um &\# 0034; conjunto de caracteres&\# 0034; é um mapeamento de caracteres para seus valores de código de identificação.
ms.assetid: 0a055c02-c5ed-4790-83e4-183bc3cc6b51
title: Conjuntos de caracteres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b8e62a0afbe9e5b2b3ab596a8129db833477e53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105759395"
---
# <a name="character-sets"></a>Conjuntos de caracteres

Um "conjunto de caracteres" é um mapeamento de caracteres para seus valores de código de identificação. O conjunto de caracteres mais comumente usado em computadores hoje é [Unicode](unicode.md), um padrão global para codificação de caracteres. Internamente, os aplicativos do Windows usam a implementação UTF-16 do Unicode. Em UTF-16, a maioria dos caracteres é identificada por códigos de dois bytes. Os caracteres suplementares usados com menos frequência são representados por um par alternativo, que é um par de códigos de dois bytes. Para obter mais informações, consulte [substitutos e caracteres suplementares](surrogates-and-supplementary-characters.md).

Alguns aplicativos do Windows devem funcionar com os conjuntos de caracteres mais antigos que são nativos do Windows me/98/95. As [páginas de código do Windows](code-pages.md) permitem que seu aplicativo funcione com esses conjuntos de caracteres. Esses conjuntos de caracteres podem ser divididos em:

-   SBCS ( [conjuntos de caracteres de byte único](single-byte-character-sets.md) ). Em um SBCS, cada caractere é identificado por um valor de um byte de largura.
-   Conjuntos de caracteres multibyte, em particular os [conjuntos de caracteres de dois bytes](double-byte-character-sets.md) (DBCS). Conjuntos de caracteres multibyte fornecem um meio para representar o grande número de caracteres em muitos idiomas asiáticos.

Para mais informações, consulte os seguintes tópicos:

-   [Páginas de código](code-pages.md)
-   [Conjuntos de caracteres de byte duplo](double-byte-character-sets.md)
-   [Conjuntos de caracteres de byte único](single-byte-character-sets.md)
-   [Caracteres substitutos e suplementares](surrogates-and-supplementary-characters.md)
-   [Unicode](unicode.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre Unicode e conjuntos de caracteres](about-unicode-and-character-sets.md)
</dt> </dl>

 

 



