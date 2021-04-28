---
title: Trabalhando com Cadeias de Caracteres
description: Trabalhando com Cadeias de Caracteres
ms.assetid: 876ff8bb-67c3-4dcc-aa94-7fbd915c67dc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4661c6b07a267d90e0fca05d04354c018be04527
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110964"
---
# <a name="working-with-strings"></a>Trabalhando com Cadeias de Caracteres

O Windows nativamente dá suporte a cadeias de caracteres Unicode para elementos de interface do usuário, nomes de arquivos e assim por diante. Unicode é a codificação de caractere preferencial, pois dá suporte a todos os conjuntos de caracteres e idiomas. O Windows representa caracteres Unicode usando a codificação UTF-16, na qual cada caractere é codificado como um valor de 16 bits. Caracteres UTF-16 são chamados de caracteres *largos* , para distingui-los de caracteres ANSI de 8 bits. O compilador Visual C++ dá suporte ao tipo de dados interno **WCHAR \_ t** para caracteres largos. O arquivo de cabeçalho WinNT. h também define o seguinte **typedef**.


```C++
typedef wchar_t WCHAR;
```



Você verá as duas versões no código de exemplo do MSDN. Para declarar um literal de caractere largo ou um literal de cadeia de caracteres largo, coloque **L** antes do literal.


```C++
wchar_t a = L'a';
wchar_t *str = L"hello";
```



Aqui estão alguns outros TYPEDEFs relacionados a cadeias de caracteres que você verá:



| Typedef                   | Definição       |
|---------------------------|------------------|
| **CHAR**                  | `char`           |
| **PSTR** ou **LPSTR**     | `char*`          |
| **PCSTR** ou **LPCSTR**   | `const char*`    |
| **PWSTR** ou **LPWSTR**   | `wchar_t*`       |
| **PCWSTR** ou **LPCWSTR** | `const wchar_t*` |



 

## <a name="unicode-and-ansi-functions"></a>Funções Unicode e ANSI

Quando a Microsoft introduziu o suporte a Unicode no Windows, ela facilitou a transição fornecendo dois conjuntos paralelos de APIs, um para cadeias de caracteres ANSI e o outro para cadeias de caracteres Unicode. Por exemplo, há duas funções para definir o texto da barra de título de uma janela:

-   **SetWindowTextA** usa uma cadeia de caracteres ANSI.
-   **SetWindowTextW** usa uma cadeia de caracteres Unicode.

Internamente, a versão ANSI traduz a cadeia de caracteres para Unicode. Os cabeçalhos do Windows também definem uma macro que é resolvida para a versão Unicode quando o símbolo de pré-processador `UNICODE` é definido ou a versão ANSI, caso contrário.


```C++
#ifdef UNICODE
#define SetWindowText  SetWindowTextW
#else
#define SetWindowText  SetWindowTextA
#endif 
```



No MSDN, a função está documentada sob o nome [**SetWindowText**](/windows/desktop/api/winuser/nf-winuser-setwindowtexta), embora seja realmente o nome da macro, não o nome real da função.

Os novos aplicativos sempre devem chamar as versões Unicode. Muitas linguagens de mundo exigem Unicode. Se você usar cadeias de caracteres ANSI, será impossível localizar seu aplicativo. As versões ANSI também são menos eficientes, pois o sistema operacional deve converter as cadeias de caracteres ANSI em Unicode em tempo de execução. Dependendo de sua preferência, você pode chamar as funções Unicode explicitamente, como **SetWindowTextW**, ou usar as macros. O código de exemplo no MSDN normalmente chama as macros, mas as duas formas são exatamente equivalentes. As APIs mais recentes do Windows têm apenas uma versão Unicode, sem nenhuma versão ANSI correspondente.

## <a name="tchars"></a>TCHARs

De volta quando os aplicativos precisarem dar suporte ao Windows NT, bem como ao Windows 95, ao Windows 98 e ao Windows me, era útil compilar o mesmo código para cadeias de caracteres ANSI ou Unicode, dependendo da plataforma de destino. Para esse fim, o SDK do Windows fornece macros que mapeiam cadeias de caracteres para Unicode ou ANSI, dependendo da plataforma.



| Macro     | Unicode   | ANSI   |
|-----------|-----------|--------|
| TCHAR     | `wchar_t` | `char` |
| TEXTO ("x") | `L"x"`    | `"x"`  |



 

Por exemplo, o código a seguir:


```C++
SetWindowText(TEXT("My Application"));
```



resolve para um dos seguintes:


```C++
SetWindowTextW(L"My Application"); // Unicode function with wide-character string.

SetWindowTextA("My Application");  // ANSI function.
```



As macros **Text** e **TCHAR** são menos úteis hoje, porque todos os aplicativos devem usar Unicode. No entanto, você pode vê-los em código mais antigo e em alguns dos exemplos de código do MSDN.

Os cabeçalhos das bibliotecas de tempo de execução do Microsoft C definem um conjunto de macros semelhantes. Por exemplo, **\_ tcslen** é resolvido para **strlen** se `_UNICODE` estiver indefinido; caso contrário, ele será resolvido para **wcslen**, que é a versão de caractere largo do **strlen**.


```C++
#ifdef _UNICODE
#define _tcslen     wcslen
#else
#define _tcslen     strlen
#endif 
```



Cuidado: alguns cabeçalhos usam o símbolo de pré-processador `UNICODE` , outros usam `_UNICODE` com um prefixo de sublinhado. Sempre defina os dois símbolos. O Visual C++ os define por padrão quando você cria um novo projeto.

## <a name="next"></a>Avançar

[O que é uma janela?](what-is-a-window-.md)

 

 
