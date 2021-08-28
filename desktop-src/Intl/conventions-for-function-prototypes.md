---
description: O Windows SDK fornece protótipos de função em versões genéricas, Windows código e Unicode.
ms.assetid: 601d24b0-11bb-48fa-a257-207c3acee226
title: Convenções para protótipos de função
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cd37171ed4cd1f0f00267b935ec57f17ef2957514b63d770efdc851b9c08bb6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119746136"
---
# <a name="conventions-for-function-prototypes"></a>Convenções para protótipos de função

O Windows SDK fornece protótipos de função em versões genéricas, [Windows código](code-pages.md)e [Unicode.](unicode.md) Os protótipos podem ser compilados para produzir protótipos Windows página de código ou protótipos Unicode. Todos os três protótipos são discutidos neste tópico e são ilustrados por exemplos de código para a [**função SetWindowText.**](/windows/win32/api/winuser/nf-winuser-setwindowtexta)

A seguir está um exemplo de um protótipo genérico.


```C++
BOOL SetWindowText(
  HWND hwnd,
  LPCTSTR lpText
);
```



O arquivo de cabeçalho fornece o nome genérico da função implementada como uma macro.


```C++
#ifdef UNICODE
#define SetWindowText SetWindowTextW
#else
#define SetWindowText SetWindowTextA
#endif // !UNICODE
```



O pré-processador expande a macro para a página Windows código ou o nome da função Unicode. A letra "A" (ANSI) ou "W" (Unicode) é adicionada ao final do nome da função genérica, conforme apropriado. O arquivo de header fornece dois protótipos específicos, um para Windows páginas de código e outro para Unicode, conforme mostrado nos exemplos a seguir.


```C++
BOOL SetWindowTextA(
  HWND hwnd,
  LPCSTR lpText
);
```




```C++
BOOL SetWindowTextW(
  HWND hwnd,
  LPCWSTR lpText
);
```



Conforme explicado em Windows tipos de dados para cadeias de [caracteres,](windows-data-types-for-strings.md)o protótipo de função genérica usa o tipo de dados LPCTSTR para o parâmetro de texto. No entanto, o protótipo de página do código do Windows usa o tipo LPCSTR e o protótipo Unicode usa LPCWSTR.

Para todas as funções com argumentos de texto, os aplicativos devem normalmente usar os protótipos genéricos de função. Se um aplicativo definir "UNICODE" antes das instruções **\# include** para os arquivos de header ou durante a compilação, as instruções serão compiladas em funções Unicode.

> [!Note]  
> Novos Windows aplicativos devem usar Unicode para evitar inconsistências de páginas de código variadas e para facilitar a localização. Eles devem ser escritos com funções genéricas e devem definir UNICODE para compilar as funções em funções Unicode. Nos poucos locais em que um aplicativo deve trabalhar com dados de caracteres de 8 bits, ele pode fazer uso explícito das funções para Windows páginas de código.

 

Seu aplicativo sempre deve usar um protótipo genérico da função com a cadeia de caracteres e os tipos de caracteres genéricos. Todos os nomes de função que terminam com “W” maiúscula usam Unicode, ou seja, caracteres e parâmetros largos. Algumas funções existem somente em versões Unicode e podem ser usadas somente com os tipos de dados apropriados. Por exemplo, [**LCIDToLocaleName**](/windows/desktop/api/Winnls/nf-winnls-lcidtolocalename) e [**LocaleNameToLCID**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) têm apenas versões Unicode.

A seção Requisitos na documentação de referência para cada função Unicode e conjunto de caracteres fornece informações sobre as versões de função implementadas pelos sistemas operacionais com suporte. Se uma linha que começa com "Unicode" for incluída, a função terá versões de página de código Unicode e Windows separadas.

> [!Note]  
> Quando uma função tem um parâmetro de comprimento para uma cadeia de caracteres, o comprimento deve ser documentado como uma contagem de valores TCHAR na cadeia de caracteres. Esse tipo de dados refere-se a bytes Windows versões de página de código da função ou palavras de 16 bits para versões Unicode. No entanto, as funções que exigem ou retornam ponteiros para blocos de memória sem tipo, como a [**função GlobalAlloc,**](/windows/win32/api/winbase/nf-winbase-globalalloc) geralmente têm um tamanho em bytes, independentemente do protótipo usado. Se a alocação de memória não com tipo for para uma cadeia de caracteres, o aplicativo deverá multiplicar o número de caracteres por sizeof(TCHAR). Para obter informações adicionais, consulte [Usando tipos de dados genéricos](using-generic-data-types.md).

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Unicode na API do Windows](unicode-in-the-windows-api.md)
</dt> </dl>

 

 
