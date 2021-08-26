---
title: Trabalhando com Cadeias de Caracteres
description: Trabalhando com Cadeias de Caracteres
ms.assetid: 876ff8bb-67c3-4dcc-aa94-7fbd915c67dc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1850d531a1cff713ec71a7e96399f029794545db9b695abe5b826ed63f0f080
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075196"
---
# <a name="working-with-strings"></a>Trabalhando com Cadeias de Caracteres

Windows na verdade dá suporte a cadeias de caracteres Unicode para elementos de interface do usuário, nomes de arquivo e assim por diante. Unicode é a codificação de caractere preferencial, pois dá suporte a todos os conjuntos de caracteres e idiomas. Windows representa caracteres Unicode usando a codificação UTF-16, na qual cada caractere é codificado como um valor de 16 bits. Caracteres UTF-16 são chamados *de caracteres* largos, para diferenciá-los de caracteres ANSI de 8 bits. O Visual C++ compilador dá suporte ao tipo de dados **integrado wchar \_ t** para caracteres largos. O arquivo de título WinNT.h também define o **typedef a seguir.**


```C++
typedef wchar_t WCHAR;
```



Você verá as duas versões no código de exemplo do MSDN. Para declarar um literal de caractere largo ou um literal de cadeia de caracteres largos, coloque **L antes** do literal.


```C++
wchar_t a = L'a';
wchar_t *str = L"hello";
```



Aqui estão alguns outros typedefs relacionados à cadeia de caracteres que você verá:



| Typedef                   | Definição       |
|---------------------------|------------------|
| **CHAR**                  | `char`           |
| **PSTR** ou **LPSTR**     | `char*`          |
| **PCSTR** ou **LPCSTR**   | `const char*`    |
| **PWSTR** ou **LPWSTR**   | `wchar_t*`       |
| **PCWSTR** ou **LPCWSTR** | `const wchar_t*` |



 

## <a name="unicode-and-ansi-functions"></a>Funções Unicode e ANSI

Quando a Microsoft introduziu o suporte a Unicode para Windows, ela facilizou a transição fornecendo dois conjuntos paralelos de APIs, um para cadeias de caracteres ANSI e outro para cadeias de caracteres Unicode. Por exemplo, há duas funções para definir o texto da barra de título de uma janela:

-   **SetWindowTextA aceita** uma cadeia de caracteres ANSI.
-   **SetWindowTextW aceita** uma cadeia de caracteres Unicode.

Internamente, a versão ANSI converte a cadeia de caracteres em Unicode. Os Windows também definem uma macro que é resolvida para a versão Unicode quando o símbolo do pré-processador é definido ou a `UNICODE` versão ANSI, caso contrário.


```C++
#ifdef UNICODE
#define SetWindowText  SetWindowTextW
#else
#define SetWindowText  SetWindowTextA
#endif 
```



No MSDN, a função é documentada com o nome [**SetWindowText**](/windows/desktop/api/winuser/nf-winuser-setwindowtexta), mesmo que esse seja realmente o nome da macro, não o nome real da função.

Novos aplicativos sempre devem chamar as versões Unicode. Muitas linguagens do mundo exigem Unicode. Se você usar cadeias de caracteres ANSI, será impossível localizar seu aplicativo. As versões ANSI também são menos eficientes, porque o sistema operacional deve converter as cadeias de caracteres ANSI em Unicode em tempo de operação. Dependendo de sua preferência, você pode chamar as funções Unicode explicitamente, como **SetWindowTextW** ou usar as macros. O código de exemplo no MSDN normalmente chama as macros, mas os dois formulários são exatamente equivalentes. A maioria das APIs mais Windows tem apenas uma versão Unicode, sem nenhuma versão ANSI correspondente.

## <a name="tchars"></a>Tchars

Quando os aplicativos precisavam dar suporte a Windows NT, bem como Windows 95, Windows 98 e Windows Me, era útil compilar o mesmo código para cadeias de caracteres ANSI ou Unicode, dependendo da plataforma de destino. Para esse fim, o SDK Windows fornece macros que mapeiam cadeias de caracteres para Unicode ou ANSI, dependendo da plataforma.



| Macro     | Unicode   | ANSI   |
|-----------|-----------|--------|
| Tchar     | `wchar_t` | `char` |
| TEXT("x") | `L"x"`    | `"x"`  |



 

Por exemplo, o código a seguir:


```C++
SetWindowText(TEXT("My Application"));
```



resolve para um dos seguintes:


```C++
SetWindowTextW(L"My Application"); // Unicode function with wide-character string.

SetWindowTextA("My Application");  // ANSI function.
```



As **macros TEXT** **e TCHAR** são menos úteis atualmente, porque todos os aplicativos devem usar Unicode. No entanto, você pode vê-los em código mais antigo e em alguns dos exemplos de código MSDN.

Os headers das bibliotecas de tempo de run time do Microsoft C definem um conjunto semelhante de macros. Por exemplo, **\_ tcslen** resolve para **strlen** se for indefinido; caso contrário, ele resolverá para wcslen , que é a versão de caractere largo `_UNICODE` de **strlen.** 


```C++
#ifdef _UNICODE
#define _tcslen     wcslen
#else
#define _tcslen     strlen
#endif 
```



Tenha cuidado: alguns headers usam o símbolo de pré-processador `UNICODE` , outros usam com um `_UNICODE` prefixo de sublinhado. Sempre defina os dois símbolos. Visual C++ define ambos por padrão quando você cria um novo projeto.

## <a name="next"></a>Avançar

[O que é uma janela?](what-is-a-window-.md)

 

 
