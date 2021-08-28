---
description: Um handle para uma cadeia de Windows runtime.
ms.assetid: 763ACE57-EFDD-482E-851E-668D7756C5DF
title: HSTRING (Hstring.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4b43c92d439cec10c0d1683efb1e8ceafd8165a35c3c8aa9a1b35150e43a33a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121566"
---
# <a name="hstring"></a>HSTRING

Um handle para uma cadeia de Windows runtime.


```C++
typedef HSTRING__* HSTRING;
```



## <a name="remarks"></a>Comentários

Use **HSTRING** para representar cadeias de caracteres imutáveis no Windows Runtime.

JavaScript e outras linguagens, como C e Microsoft Visual Basic, podem usar cadeias de \# caracteres representadas usando **HSTRING**. A tabela a seguir mostra como um **HSTRING** é representado em outras linguagens.



| Linguagem de programação                                                                    | Representação de cadeia de caracteres                                      |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------|
| [C++/WinRT](/windows/uwp/cpp-and-winrt-apis/intro-to-using-cpp-with-winrt)              | [Classe winrt::hstring](/uwp/cpp-ref-for-winrt/hstring)     |
| Visual C++ de componente[(C++/CX)](/cpp/cppcx/visual-c-language-reference-c-cx) | [Classe Platform::String](/cpp/cppcx/platform-string-class) |
| JavaScript                                                                              | Objeto String                                              |
| .NET Framework                                                                          | Classe System.String                                        |



 

O **identificador HSTRING** é um tipo de identificador padrão. Semanticamente, um **HSTRING que** contém o valor **NULL** representa a cadeia de caracteres vazia, que consiste em zero caracteres de conteúdo e um caractere **NULL de** terminação. A criação de uma cadeia de [**caracteres por meio do WindowsCreateString**](/windows/win32/api/winstring/nf-winstring-windowscreatestring) com zero caracteres produzirá o valor do handle **NULL.** Ao chamar [**WindowsGetStringRawBuffer**](/windows/win32/api/winstring/nf-winstring-windowsgetstringrawbuffer) com o valor **NULL**, um ponteiro para uma cadeia de caracteres vazia seguida apenas pelo caractere de terminação **NUL** será retornado. Não existe nenhum valor distinto para representar **um HSTRING** não reinicializado.

Chame a [**função WindowsCreateString**](/windows/win32/api/winstring/nf-winstring-windowscreatestring) para criar uma **nova HSTRING** e chame a função [**WindowsDeleteString**](/windows/win32/api/winstring/nf-winstring-windowsdeletestring) para liberar a referência à memória da cadeia de caracteres de suporte. Chame a [**função WindowsCreateStringReference**](/windows/win32/api/winstring/nf-winstring-windowscreatestringreference) para criar uma referência de cadeia de caracteres, que também é chamada de cadeia de caracteres *de passagem rápida.*

Copie um **HSTRING** chamando a [**função WindowsDuplicateString.**](/windows/win32/api/winstring/nf-winstring-windowsduplicatestring)

Concatene duas cadeias de caracteres chamando a [**função WindowsConcatString.**](/windows/win32/api/winstring/nf-winstring-windowsconcatstring)

Acesse a memória da cadeia de caracteres de suporte chamando a [**função WindowsGetStringRawBuffer.**](/windows/win32/api/winstring/nf-winstring-windowsgetstringrawbuffer)

**O HSTRING** pode armazenar e usar caracteres **NUL inseridos.** Use a [**função WindowsStringHasEmbeddedNull**](/windows/win32/api/winstring/nf-winstring-windowsstringhasembeddednull) para verificar se há caracteres **NUL** inseridos antes de usar funções que podem produzir resultados inesperados. Por exemplo, a maioria das funções Windows usam **LPCWSTR** como um parâmetro de entrada e calculam o comprimento da cadeia de caracteres somente até que a primeira **NUL** seja encontrada.

A cadeia de caracteres de backing deve permanecer imutável e terminada em nulo. Ao chamar código cria uma referência de cadeia de caracteres usando a função [**WindowsCreateStringReference,**](/windows/win32/api/winstring/nf-winstring-windowscreatestringreference) a memória que contém a representação de cadeia de caracteres de suporte pertence ao chamador. O Windows Runtime depende do conteúdo da cadeia de caracteres original para permanecer inalterado. Ao passar uma referência de cadeia de caracteres para o runtime do Windows, é responsabilidade do chamador garantir que o conteúdo da cadeia de caracteres seja inalterável e **que o NUL** seja encerrado durante a chamada. O Windows Runtime libera todas as referências à referência de cadeia de caracteres quando a chamada é retornada.

Quando você recebe um **HSTRING** como um parâmetro out, é uma boa prática definir o handle como **NULL** quando você terminar de fazer isso.

Chame a [**função WindowsPreallocateStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspreallocatestringbuffer) para alocar um buffer de cadeia de caracteres mutável que você pode usar para criar um **HSTRING imutável.** Quando terminar de preencher o buffer, chame a função [**WindowsPromoteStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspromotestringbuffer) para criar o **HSTRING.** Esse padrão de construção de duas fases habilita a funcionalidade semelhante a um "construtor de cadeia de caracteres".

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8<br/>                                                                 |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                       |
| Cabeçalho<br/>                   | <dl> <dt>Hstring.h</dt> </dl> |



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

 

 
