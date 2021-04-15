---
description: Um identificador para uma cadeia de caracteres Windows Runtime.
ms.assetid: 763ACE57-EFDD-482E-851E-668D7756C5DF
title: HSTRING (hstring. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76b9e73d7627a4bab8f02a95056e5b208569d922
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105761314"
---
# <a name="hstring"></a>HSTRING

Um identificador para uma cadeia de caracteres Windows Runtime.


```C++
typedef HSTRING__* HSTRING;
```



## <a name="remarks"></a>Comentários

Use **HSTRING** para representar cadeias de caracteres imutáveis no Windows Runtime.

O JavaScript e outras linguagens, como C \# e Microsoft Visual Basic, podem usar cadeias de caracteres que são representadas usando **HSTRING**. A tabela a seguir mostra como um **HSTRING** é representado em outros idiomas.



| Linguagem de programação                                                                    | Representação de cadeia de caracteres                                      |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------|
| [C++/WinRT](/windows/uwp/cpp-and-winrt-apis/intro-to-using-cpp-with-winrt)              | classe [winrt:: hstring](/uwp/cpp-ref-for-winrt/hstring)     |
| Extensões de componente Visual C++ ([C++/CX](/cpp/cppcx/visual-c-language-reference-c-cx)) | Classe [Platform:: String](/cpp/cppcx/platform-string-class) |
| JavaScript                                                                              | Objeto String                                              |
| .NET Framework                                                                          | Classe System. String                                        |



 

O identificador **HSTRING** é um tipo de identificador padrão. Semanticamente, um **HSTRING** que contém o valor **NULL** representa a cadeia de caracteres vazia, que consiste em zero caracteres de conteúdo e um caractere **nulo** de terminação. A criação de uma cadeia de caracteres por meio de [**WindowsCreateString**](/windows/win32/api/winstring/nf-winstring-windowscreatestring) com zero caracteres produzirá o valor de identificador **NULL**. Ao chamar [**WindowsGetStringRawBuffer**](/windows/win32/api/winstring/nf-winstring-windowsgetstringrawbuffer) com o valor **NULL**, um ponteiro para uma cadeia de caracteres vazia, seguido somente pelo caractere de terminação **nul** , será retornado. Nenhum valor distinto existe para representar um **HSTRING** que não foi inicializado.

Chame a função [**WindowsCreateString**](/windows/win32/api/winstring/nf-winstring-windowscreatestring) para criar um novo **HSTRING** e chame a função [**WindowsDeleteString**](/windows/win32/api/winstring/nf-winstring-windowsdeletestring) para liberar a referência à memória de cadeia de caracteres de apoio. Chame a função [**WindowsCreateStringReference**](/windows/win32/api/winstring/nf-winstring-windowscreatestringreference) para criar uma referência de cadeia de caracteres, que também é chamada de uma *cadeia de caracteres de passagem rápida*.

Copie um **HSTRING** chamando a função [**WindowsDuplicateString**](/windows/win32/api/winstring/nf-winstring-windowsduplicatestring) .

Concatene duas cadeias de caracteres chamando a função [**WindowsConcatString**](/windows/win32/api/winstring/nf-winstring-windowsconcatstring) .

Acesse a memória de cadeia de caracteres de backup chamando a função [**WindowsGetStringRawBuffer**](/windows/win32/api/winstring/nf-winstring-windowsgetstringrawbuffer) .

**HSTRING** pode armazenar e usar os caracteres **nul** inseridos. Use a função [**WindowsStringHasEmbeddedNull**](/windows/win32/api/winstring/nf-winstring-windowsstringhasembeddednull) para verificar se há caracteres **nul** inseridos antes de usar qualquer função que possa produzir resultados inesperados. Por exemplo, a maioria das funções do Windows usa **LPCWSTR** como um parâmetro de entrada e calcula o comprimento da cadeia de caracteres somente até que a primeira **nul** seja encontrada.

A cadeia de caracteres de backup deve permanecer imutável e terminada em nulo. Quando o código de chamada cria uma referência de cadeia de caracteres usando a função [**WindowsCreateStringReference**](/windows/win32/api/winstring/nf-winstring-windowscreatestringreference) , a memória que contém a representação de cadeia de caracteres de backup pertence ao chamador. O Windows Runtime se baseia no conteúdo da cadeia de caracteres original para permanecer inalterado. Ao passar uma referência de cadeia de caracteres para o Windows Runtime, é responsabilidade do chamador garantir que o conteúdo da cadeia de caracteres seja inalterável e **nul** seja encerrado durante a chamada. O Windows Runtime libera Todas as referências para a referência de cadeia de caracteres quando a chamada retorna.

Quando você recebe um **HSTRING** como um parâmetro out, é uma prática recomendada definir o identificador como **nulo** quando terminar com ele.

Chame a função [**WindowsPreallocateStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspreallocatestringbuffer) para alocar um buffer de cadeia de caracteres mutável que você pode usar para criar uma **HSTRING** imutável. Quando você terminar de preencher o buffer, chame a função [**WindowsPromoteStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspromotestringbuffer) para criar o **HSTRING**. Esse padrão de construção de duas fases permite a funcionalidade semelhante a um "Construtor de cadeias de caracteres".

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8<br/>                                                                 |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                       |
| parâmetro<br/>                   | <dl> <dt>Hstring. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>


</dt> <dt>

[**WindowsCreateString**](/windows/win32/api/winstring/nf-winstring-windowscreatestring)
</dt> <dt>

[**WindowsDeleteString**](/windows/win32/api/winstring/nf-winstring-windowsdeletestring)
</dt> <dt>

[**WindowsDuplicateString**](/windows/win32/api/winstring/nf-winstring-windowsduplicatestring)
</dt> <dt>

[**WindowsPreallocateStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspreallocatestringbuffer)
</dt> </dl>

 

 
