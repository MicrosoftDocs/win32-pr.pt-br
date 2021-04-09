---
description: A maioria das operações de cadeia de caracteres pode usar a mesma lógica para Unicode e para páginas de código do Windows.
ms.assetid: 5364ec09-68e1-444c-9493-ca9426ac9c34
title: Tipos de dados do Windows para cadeias de caracteres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e24be1024736ce324e040e58f6ac45636a11d4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011846"
---
# <a name="windows-data-types-for-strings"></a>Tipos de dados do Windows para cadeias de caracteres

A maioria das operações de cadeia de caracteres pode usar a mesma lógica para [Unicode](unicode.md) e para [páginas de código do Windows](code-pages.md). A única diferença é que a unidade básica de operação é um caractere de 16 bits (também conhecido como um caractere largo) para Unicode e um caractere de 8 bits para páginas de código do Windows. Os arquivos de cabeçalho do Windows fornecem várias definições de tipo que facilitam a criação de fontes que podem ser compiladas para o Unicode ou para páginas de código do Windows.

O Windows dá suporte a três conjuntos de tipos de dados de caractere e cadeia de caracteres: um conjunto de definições de tipo genérico que pode compilar para as páginas de código Unicode ou Windows e dois conjuntos de definições de tipo específicas. Um conjunto de definições de tipo específico é para uso com Unicode e o outro é para uso com páginas de código do Windows.

Um aplicativo que usa tipos de dados genéricos pode ser compilado para Unicode simplesmente definindo "UNICODE" antes das instruções **\# include** para os arquivos de cabeçalho ou durante a compilação. Novos aplicativos do Windows devem usar Unicode para evitar as inconsistências de páginas de código variadas e simplificar a localização. Eles devem ser escritos com tipos de dados genéricos e devem definir "UNICODE" para compilar esses tipos em tipos Unicode. Nos poucos lugares em que um aplicativo deve trabalhar com dados de caractere de 8 bits, ele pode fazer uso explícito dos tipos para páginas de código do Windows.

A capacidade de compilar os tipos genéricos em tipos para páginas de código do Windows existe principalmente para dar suporte a aplicativos herdados. Para compilar para páginas de código do Windows, o aplicativo simplesmente omite a definição de UNICODE.

O exemplo a seguir mostra o método usado nos arquivos de cabeçalho do Windows para definir os três conjuntos de tipos de dados. Para a implementação, consulte o arquivo de cabeçalho WinNT. h.


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



A letra "T" em uma definição de tipo, por exemplo, TCHAR ou LPTSTR, designa um tipo genérico que pode ser compilado para as páginas de código do Windows ou para o Unicode. A letra "W" em uma definição de tipo, por exemplo, WCHAR ou LPWSTR, designa um tipo Unicode. Como as páginas de código do Windows são do formulário mais antigo, elas têm definições de tipo simples, como CHAR e LPSTR. Para obter uma descrição completa dos tipos de dados no Windows, consulte [tipos de dados do Windows](../winprog/windows-data-types.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Unicode na API do Windows](unicode-in-the-windows-api.md)
</dt> </dl>

 

 
