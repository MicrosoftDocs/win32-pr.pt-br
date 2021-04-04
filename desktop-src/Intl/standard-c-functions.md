---
description: As bibliotecas de tempo de execução C padrão contêm versões Unicode UTF-16 (caracteres largos) de funções de cadeia de caracteres que podem ser usadas com as versões Unicode e orientadas a bytes das funções de cadeia de caracteres que podem ser usadas com caracteres de SBCS (conjuntos de caracteres de byte único). O tipo de dados Unicode WCHAR é compatível com o tipo de dados WCHAR \_ t no ANSI C e permite o acesso às funções de cadeia de caracteres Unicode. As versões Unicode das funções começam com as letras &\# 0034; wcs&\# 0034; (ou às vezes &\# 0034; \_ WCS&\# 0034;). O tipo de dados CHAR usado para páginas de código é compatível com o caractere de tipo de dados character no ANSI C, para permitir o acesso às funções de cadeia de caracteres. As versões de caracteres das funções começam com as letras &\# 0034; str&\# 0034;. Também há versões especiais para conjuntos de caracteres de dois bytes (DBCS) que começam com as letras &\# 0034; \_ MBS&\# 0034;.
ms.assetid: a86626c1-7f90-4924-bfdd-384729bd0cc5
title: Funções padrão C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6247b3707f96908ef16d887462ba06573fd8dd7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837332"
---
# <a name="standard-c-functions"></a>Funções padrão C

As bibliotecas de tempo de execução C padrão contêm versões Unicode UTF-16 (caracteres largos) de funções de cadeia de caracteres que podem ser usadas com as versões [Unicode](unicode.md) e orientadas a bytes das funções de cadeia de caracteres que podem ser usadas com caracteres de SBCS ( [conjuntos de caracteres de byte único](single-byte-character-sets.md) ). O tipo de dados Unicode WCHAR é compatível com o tipo de dados WCHAR \_ t no ANSI C e permite o acesso às funções de cadeia de caracteres Unicode. As versões Unicode das funções começam com as letras "WCS" (ou, às vezes, " \_ WCS"). O tipo de dados CHAR usado para páginas de código é compatível com o caractere de tipo de dados character no ANSI C, para permitir o acesso às funções de cadeia de caracteres. As versões de caracteres das funções começam com as letras "Str". Também há versões especiais para [conjuntos de caracteres de byte duplo](double-byte-character-sets.md) (DBCS) que começam com as letras " \_ MBS".

As bibliotecas de tempo de execução C padrão incluem funções genéricas para todas as funções de cadeia de caracteres C padrão. Eles começam com " \_ TCS" e são listados no arquivo de cabeçalho TCHAR. h. Essas funções usam o tipo de dados TCHAR genérico.

Um aplicativo deve adicionar as seguintes linhas para usar as funções genéricas e compilar para Unicode.


```C++
#define _UNICODE

#include <tchar.h>
#include <wchar.h>
```



Observe que os arquivos TCHAR. h e WCHAR. h são necessários e que o sublinhado à esquerda na \_ variável Unicode também é necessário. Esse nomenclatura é específico para a biblioteca C padrão. O "UNICODE" renderizado sem o sublinhado é para os tempos de execução do Microsoft Windows.

As funções [wcstombs](/cpp/c-runtime-library/reference/wcstombs-wcstombs-l) e [mbstowcs](/cpp/c-runtime-library/reference/mbstowcs-s-mbstowcs-s-l) podem converter do conjunto de caracteres com suporte da biblioteca C padrão para Unicode e back, com algumas limitações. Para obter mais informações sobre a conversão de cadeias de caracteres de e para Unicode, consulte [conversão entre tipos de cadeia](translation-between-string-types.md).

A função [printf](/cpp/c-runtime-library/reference/printf-printf-l-wprintf-wprintf-l) definida em TCHAR. h dá suporte às mesmas especificações de formato que as funções de impressão strsafe. h, por exemplo, [**StringCbPrintf**](/windows/win32/api/strsafe/nf-strsafe-stringcbprintfa). Da mesma forma, TCHAR. h define uma função [wprintf](/cpp/c-runtime-library/reference/printf-printf-l-wprintf-wprintf-l) , na qual a cadeia de caracteres de formato é uma cadeia de caracteres Unicode.

> [!Caution]  
> A manipulação de buffer insatisfatório é incomplicada em muitos problemas de segurança que envolvem saturações de buffer. Consulte a [referência de strsafe. h](../menurc/strsafe-ovw.md). As funções definidas em strsafe. h fornecem processamento adicional para a manipulação de buffer adequada em seu código. Eles se destinam a substituir suas contrapartes C/C++ internas, bem como implementações específicas do Microsoft Windows. Para obter mais informações, consulte [Considerações sobre segurança: recursos internacionais](security-considerations--international-features.md).

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Unicode na API do Windows](unicode-in-the-windows-api.md)
</dt> </dl>

 

 
