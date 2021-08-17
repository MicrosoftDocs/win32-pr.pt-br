---
description: A maioria das operações de cadeia de caracteres pode usar a mesma lógica para Unicode e para Windows de código.
ms.assetid: 5364ec09-68e1-444c-9493-ca9426ac9c34
title: Tipos de dados do Windows para cadeias de caracteres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a2bef3dc98b7b8649b6cb0fc5bd9450c6f22c8b2bb6e3345790dab0dd24587f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146809"
---
# <a name="windows-data-types-for-strings"></a>Tipos de dados do Windows para cadeias de caracteres

A maioria das operações de cadeia de caracteres pode usar a mesma lógica [para Unicode](unicode.md) e para [Windows páginas de código](code-pages.md). A única diferença é que a unidade básica de operação é um caractere de 16 bits (também conhecido como caractere largo) para Unicode e um caractere de 8 bits para Windows páginas de código. Os Windows de Windows fornecem várias definições de tipo que facilitam a criação de fontes que podem ser compiladas para Unicode ou para Windows de código.

Windows dá suporte a três conjuntos de tipos de dados de caractere e cadeia de caracteres: um conjunto de definições de tipo genérico que pode ser compilado para páginas de código Unicode ou Windows e dois conjuntos de definições de tipo específicas. Um conjunto de definições de tipo específico é para uso com Unicode e o outro é para uso com Windows de código.

Um aplicativo que usa tipos de dados genéricos pode ser compilado para Unicode simplesmente definindo "UNICODE" antes das instruções **\# include** para os arquivos de header ou durante a compilação. Novos Windows aplicativos devem usar Unicode para evitar inconsistências de páginas de código variadas e simplificar a localização. Eles devem ser escritos com tipos de dados genéricos e devem definir "UNICODE" para compilar esses tipos em tipos Unicode. Nos poucos locais em que um aplicativo deve trabalhar com dados de caracteres de 8 bits, ele pode fazer uso explícito dos tipos para Windows páginas de código.

A capacidade de compilar os tipos genéricos em tipos para Windows páginas de código existe principalmente para dar suporte a aplicativos herdados. Para compilar para Windows de código, o aplicativo apenas omite a definição UNICODE.

O exemplo a seguir mostra o método usado nos arquivos Windows de Windows para definir os três conjuntos de tipos de dados. Para a implementação, consulte o arquivo de título Winnt.h.


```C++
// Generic types

#ifdef UNICODE
    typedef wchar_t TCHAR;
#else
    typedef unsigned char TCHAR;
#endif

typedef TCHAR *LPTSTR, *LPTCH;

// 8-bit character specific

typedef unsigned char CHAR;
typedef CHAR *LPSTR, *LPCH;

// Unicode specific (wide characters)

typedef unsigned wchar_t WCHAR;
typedef WCHAR *LPWSTR, *LPWCH;
```



A letra "T" em uma definição de tipo, por exemplo, TCHAR ou LPTSTR, designa um tipo genérico que pode ser compilado para páginas de código Windows ou Unicode. A letra "W" em uma definição de tipo, por exemplo, WCHAR ou LPWSTR, designa um tipo Unicode. Como Windows páginas de código são da forma mais antiga, elas têm definições de tipo simples, como CHAR e LPSTR. Para ver uma descrição completa dos tipos de dados Windows, consulte [Windows tipos de dados](../winprog/windows-data-types.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Unicode na API do Windows](unicode-in-the-windows-api.md)
</dt> </dl>

 

 
