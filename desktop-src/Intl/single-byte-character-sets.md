---
description: Um SBCS (conjunto de caracteres de byte único) é um mapeamento de 256 caracteres individuais para seus valores de código de identificação, implementados como uma página de código.
ms.assetid: 53f74132-91aa-4257-846a-f6e1f2f9ae0b
title: Conjuntos de caracteres de byte único
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22bb0150dfaf2e3b8e8251530fd5e90e7b1ede3b3597d344e5efb192fa96ed36
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120130226"
---
# <a name="single-byte-character-sets"></a>Conjuntos de caracteres de byte único

Um SBCS (conjunto de caracteres de byte único) é um mapeamento de 256 caracteres individuais para seus valores de código de identificação, implementados como uma página de código. Um SBCS pode corresponder a uma página Windows código ou uma página de código OEM. Uma página de código SBCS também pode incluir uma página de código não nativa, por exemplo, uma página de código EBCDIC. Para definições dessas páginas de código, consulte [Páginas de código](code-pages.md).

> [!Note]  
> Novos Windows aplicativos devem usar [Unicode](unicode.md) para evitar inconsistências de páginas de código variadas e para facilitar a localização. No entanto, alguns protocolos herddos exigem o uso de um SBCS. Cada página de código SBCS dá suporte a caracteres diferentes, mas nenhuma página dá suporte à amplitude completa de caracteres fornecidos pelo Unicode. Cada página de código SBCS dá suporte a um subconjunto diferente, codificado de forma diferente. Os dados convertidos de uma página de código SBCS para outra estão sujeitos a corrupção, porque o mesmo valor de dados em páginas de código diferentes pode codificar um caractere diferente. Os dados convertidos de Unicode para SBCS estão sujeitos à perda de dados porque uma determinada página de código pode não ser capaz de representar todos os caracteres usados nos dados Unicode específicos.

 

Seus aplicativos usam SBCS Windows páginas de código com as versões "A" de Windows funções. Consulte [Convenções para protótipos de função e](conventions-for-function-prototypes.md) páginas de [código](code-pages.md). Para ajudar a identificar uma página de código SBCS, um aplicativo pode usar a [**função GetCPInfo**](/windows/desktop/api/Winnls/nf-winnls-getcpinfo) ou [**GetCPInfoEx.**](/windows/desktop/api/Winnls/nf-winnls-getcpinfoexa) Além disso, um aplicativo pode usar as funções [**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) e [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) para mapear entre cadeias de caracteres Unicode e SBCS.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Conjuntos de caracteres](character-sets.md)
</dt> <dt>

[Conjuntos de caracteres de byte duplo](double-byte-character-sets.md)
</dt> </dl>

 

 



