---
description: O SDK do Windows fornece protótipos de função em Generic, página de código do Windows e versões Unicode.
ms.assetid: 601d24b0-11bb-48fa-a257-207c3acee226
title: Convenções para protótipos de função
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 951860f72870dcbbcb88572f379e39dc843ecb11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828582"
---
# <a name="conventions-for-function-prototypes"></a>Convenções para protótipos de função

O SDK do Windows fornece protótipos de função em Generic, [página de código do Windows](code-pages.md)e versões [Unicode](unicode.md) . Os protótipos podem ser compilados para produzir protótipos de página de código do Windows ou protótipos Unicode. Todos os três protótipos são discutidos neste tópico e são ilustrados por exemplos de código para a função [**SetWindowText**](/windows/win32/api/winuser/nf-winuser-setwindowtexta) .

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



O pré-processador expande a macro na página de código do Windows ou no nome da função Unicode. A letra "A" (ANSI) ou "W" (Unicode) é adicionada ao final do nome da função genérica, conforme apropriado. Em seguida, o arquivo de cabeçalho fornece dois protótipos específicos, um para páginas de código do Windows e outro para Unicode, conforme mostrado nos exemplos a seguir.


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



Conforme explicado em [tipos de dados do Windows para cadeias de caracteres](windows-data-types-for-strings.md), o protótipo de função genérico usa o tipo de dados LPCTSTR para o parâmetro text. No entanto, o protótipo de página do código do Windows usa o tipo LPCSTR e o protótipo Unicode usa LPCWSTR.

Para todas as funções com argumentos de texto, os aplicativos devem normalmente usar os protótipos genéricos de função. Se um aplicativo definir "UNICODE" antes das instruções **\# include** para os arquivos de cabeçalho ou durante a compilação, as instruções serão compiladas em funções Unicode.

> [!Note]  
> Novos aplicativos do Windows devem usar Unicode para evitar as inconsistências de páginas de código variadas e para facilitar a localização. Eles devem ser escritos com funções genéricas e devem definir o UNICODE para compilar as funções em funções Unicode. Nos poucos lugares em que um aplicativo deve trabalhar com dados de caractere de 8 bits, ele pode fazer uso explícito das funções para páginas de código do Windows.

 

Seu aplicativo sempre deve usar um protótipo genérico da função com a cadeia de caracteres e os tipos de caracteres genéricos. Todos os nomes de função que terminam com “W” maiúscula usam Unicode, ou seja, caracteres e parâmetros largos. Algumas funções existem apenas em versões Unicode e podem ser usadas somente com os tipos de dados apropriados. Por exemplo, [**LCIDToLocaleName**](/windows/desktop/api/Winnls/nf-winnls-lcidtolocalename) e [**LocaleNameToLCID**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) têm apenas versões Unicode.

A seção requisitos na documentação de referência para cada função de conjunto de caracteres e Unicode fornece informações sobre as versões de função implementadas por sistemas operacionais com suporte. Se uma linha que começa com "Unicode" estiver incluída, a função terá versões de página de código Unicode e do Windows separadas.

> [!Note]  
> Quando uma função tem um parâmetro de comprimento para uma cadeia de caracteres, o comprimento deve ser documentado como uma contagem de valores de TCHAR na cadeia de caracteres. Esse tipo de dados se refere a bytes para versões de página de código do Windows da função ou palavras de 16 bits para versões Unicode. No entanto, as funções que exigem ou retornam ponteiros para blocos de memória não tipados, como a função [**GlobalAlloc**](/windows/win32/api/winbase/nf-winbase-globalalloc) , geralmente usam um tamanho em bytes, independentemente do protótipo usado. Se a alocação de memória não tipada for para uma cadeia de caracteres, o aplicativo deverá multiplicar o número de caracteres por sizeof (TCHAR). Para obter informações adicionais, consulte [usando tipos de dados genéricos](using-generic-data-types.md).

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Unicode na API do Windows](unicode-in-the-windows-api.md)
</dt> </dl>

 

 
