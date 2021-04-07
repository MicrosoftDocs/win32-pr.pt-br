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
# <a name="conventions-for-function-prototypes"></a><span data-ttu-id="fb9cb-103">Convenções para protótipos de função</span><span class="sxs-lookup"><span data-stu-id="fb9cb-103">Conventions for Function Prototypes</span></span>

<span data-ttu-id="fb9cb-104">O SDK do Windows fornece protótipos de função em Generic, [página de código do Windows](code-pages.md)e versões [Unicode](unicode.md) .</span><span class="sxs-lookup"><span data-stu-id="fb9cb-104">The Windows SDK provides function prototypes in generic, [Windows code page](code-pages.md), and [Unicode](unicode.md) versions.</span></span> <span data-ttu-id="fb9cb-105">Os protótipos podem ser compilados para produzir protótipos de página de código do Windows ou protótipos Unicode.</span><span class="sxs-lookup"><span data-stu-id="fb9cb-105">The prototypes can be compiled to produce either Windows code page prototypes or Unicode prototypes.</span></span> <span data-ttu-id="fb9cb-106">Todos os três protótipos são discutidos neste tópico e são ilustrados por exemplos de código para a função [**SetWindowText**](/windows/win32/api/winuser/nf-winuser-setwindowtexta) .</span><span class="sxs-lookup"><span data-stu-id="fb9cb-106">All three prototypes are discussed in this topic and are illustrated by code samples for the [**SetWindowText**](/windows/win32/api/winuser/nf-winuser-setwindowtexta) function.</span></span>

<span data-ttu-id="fb9cb-107">A seguir está um exemplo de um protótipo genérico.</span><span class="sxs-lookup"><span data-stu-id="fb9cb-107">The following is an example of a generic prototype.</span></span>


```C++
BOOL SetWindowText(
  HWND hwnd,
  LPCTSTR lpText
);
```



<span data-ttu-id="fb9cb-108">O arquivo de cabeçalho fornece o nome genérico da função implementada como uma macro.</span><span class="sxs-lookup"><span data-stu-id="fb9cb-108">The header file provides the generic function name implemented as a macro.</span></span>


```C++
#ifdef UNICODE
#define SetWindowText SetWindowTextW
#else
#define SetWindowText SetWindowTextA
#endif // !UNICODE
```



<span data-ttu-id="fb9cb-109">O pré-processador expande a macro na página de código do Windows ou no nome da função Unicode.</span><span class="sxs-lookup"><span data-stu-id="fb9cb-109">The preprocessor expands the macro into either the Windows code page or Unicode function name.</span></span> <span data-ttu-id="fb9cb-110">A letra "A" (ANSI) ou "W" (Unicode) é adicionada ao final do nome da função genérica, conforme apropriado.</span><span class="sxs-lookup"><span data-stu-id="fb9cb-110">The letter "A" (ANSI) or "W" (Unicode) is added at the end of the generic function name, as appropriate.</span></span> <span data-ttu-id="fb9cb-111">Em seguida, o arquivo de cabeçalho fornece dois protótipos específicos, um para páginas de código do Windows e outro para Unicode, conforme mostrado nos exemplos a seguir.</span><span class="sxs-lookup"><span data-stu-id="fb9cb-111">The header file then provides two specific prototypes, one for Windows code pages and one for Unicode, as shown in the following examples.</span></span>


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



<span data-ttu-id="fb9cb-112">Conforme explicado em [tipos de dados do Windows para cadeias de caracteres](windows-data-types-for-strings.md), o protótipo de função genérico usa o tipo de dados LPCTSTR para o parâmetro text.</span><span class="sxs-lookup"><span data-stu-id="fb9cb-112">As explained in [Windows Data Types for Strings](windows-data-types-for-strings.md), the generic function prototype uses the data type LPCTSTR for the text parameter.</span></span> <span data-ttu-id="fb9cb-113">No entanto, o protótipo de página do código do Windows usa o tipo LPCSTR e o protótipo Unicode usa LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="fb9cb-113">However, the Windows code page prototype uses the type LPCSTR, and the Unicode prototype uses LPCWSTR.</span></span>

<span data-ttu-id="fb9cb-114">Para todas as funções com argumentos de texto, os aplicativos devem normalmente usar os protótipos genéricos de função.</span><span class="sxs-lookup"><span data-stu-id="fb9cb-114">For all functions with text arguments, applications should normally use the generic function prototypes.</span></span> <span data-ttu-id="fb9cb-115">Se um aplicativo definir "UNICODE" antes das instruções **\# include** para os arquivos de cabeçalho ou durante a compilação, as instruções serão compiladas em funções Unicode.</span><span class="sxs-lookup"><span data-stu-id="fb9cb-115">If an application defines "UNICODE" either before the **\#include** statements for the header files or during compilation, the statements will be compiled into Unicode functions.</span></span>

> [!Note]  
> <span data-ttu-id="fb9cb-116">Novos aplicativos do Windows devem usar Unicode para evitar as inconsistências de páginas de código variadas e para facilitar a localização.</span><span class="sxs-lookup"><span data-stu-id="fb9cb-116">New Windows applications should use Unicode to avoid the inconsistencies of varied code pages and for ease of localization.</span></span> <span data-ttu-id="fb9cb-117">Eles devem ser escritos com funções genéricas e devem definir o UNICODE para compilar as funções em funções Unicode.</span><span class="sxs-lookup"><span data-stu-id="fb9cb-117">They should be written with generic functions, and should define UNICODE to compile the functions into Unicode functions.</span></span> <span data-ttu-id="fb9cb-118">Nos poucos lugares em que um aplicativo deve trabalhar com dados de caractere de 8 bits, ele pode fazer uso explícito das funções para páginas de código do Windows.</span><span class="sxs-lookup"><span data-stu-id="fb9cb-118">In the few places where an application must work with 8-bit character data, it can make explicit use of the functions for Windows code pages.</span></span>

 

<span data-ttu-id="fb9cb-119">Seu aplicativo sempre deve usar um protótipo genérico da função com a cadeia de caracteres e os tipos de caracteres genéricos.</span><span class="sxs-lookup"><span data-stu-id="fb9cb-119">Your application should always use a generic function prototype with the generic string and character types.</span></span> <span data-ttu-id="fb9cb-120">Todos os nomes de função que terminam com “W” maiúscula usam Unicode, ou seja, caracteres e parâmetros largos.</span><span class="sxs-lookup"><span data-stu-id="fb9cb-120">All function names that end with an uppercase "W" take Unicode, that is, wide character, parameters.</span></span> <span data-ttu-id="fb9cb-121">Algumas funções existem apenas em versões Unicode e podem ser usadas somente com os tipos de dados apropriados.</span><span class="sxs-lookup"><span data-stu-id="fb9cb-121">Some functions exist only in Unicode versions and can be used only with the appropriate data types.</span></span> <span data-ttu-id="fb9cb-122">Por exemplo, [**LCIDToLocaleName**](/windows/desktop/api/Winnls/nf-winnls-lcidtolocalename) e [**LocaleNameToLCID**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) têm apenas versões Unicode.</span><span class="sxs-lookup"><span data-stu-id="fb9cb-122">For example, [**LCIDToLocaleName**](/windows/desktop/api/Winnls/nf-winnls-lcidtolocalename) and [**LocaleNameToLCID**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) have only Unicode versions.</span></span>

<span data-ttu-id="fb9cb-123">A seção requisitos na documentação de referência para cada função de conjunto de caracteres e Unicode fornece informações sobre as versões de função implementadas por sistemas operacionais com suporte.</span><span class="sxs-lookup"><span data-stu-id="fb9cb-123">The Requirements section in the reference documentation for each Unicode and character set function provides information on the function versions implemented by supported operating systems.</span></span> <span data-ttu-id="fb9cb-124">Se uma linha que começa com "Unicode" estiver incluída, a função terá versões de página de código Unicode e do Windows separadas.</span><span class="sxs-lookup"><span data-stu-id="fb9cb-124">If a line beginning with "Unicode" is included, the function has separate Unicode and Windows code page versions.</span></span>

> [!Note]  
> <span data-ttu-id="fb9cb-125">Quando uma função tem um parâmetro de comprimento para uma cadeia de caracteres, o comprimento deve ser documentado como uma contagem de valores de TCHAR na cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="fb9cb-125">When a function has a length parameter for a character string, the length should be documented as a count of TCHAR values in the string.</span></span> <span data-ttu-id="fb9cb-126">Esse tipo de dados se refere a bytes para versões de página de código do Windows da função ou palavras de 16 bits para versões Unicode.</span><span class="sxs-lookup"><span data-stu-id="fb9cb-126">This data type refers to bytes for Windows code page versions of the function or 16-bit words for Unicode versions.</span></span> <span data-ttu-id="fb9cb-127">No entanto, as funções que exigem ou retornam ponteiros para blocos de memória não tipados, como a função [**GlobalAlloc**](/windows/win32/api/winbase/nf-winbase-globalalloc) , geralmente usam um tamanho em bytes, independentemente do protótipo usado.</span><span class="sxs-lookup"><span data-stu-id="fb9cb-127">However, functions that require or return pointers to untyped memory blocks, such as the [**GlobalAlloc**](/windows/win32/api/winbase/nf-winbase-globalalloc) function, generally take a size in bytes, regardless of the prototype that is used.</span></span> <span data-ttu-id="fb9cb-128">Se a alocação de memória não tipada for para uma cadeia de caracteres, o aplicativo deverá multiplicar o número de caracteres por sizeof (TCHAR).</span><span class="sxs-lookup"><span data-stu-id="fb9cb-128">If the allocation of untyped memory is for a string, the application must multiply the number of characters by sizeof(TCHAR).</span></span> <span data-ttu-id="fb9cb-129">Para obter informações adicionais, consulte [usando tipos de dados genéricos](using-generic-data-types.md).</span><span class="sxs-lookup"><span data-stu-id="fb9cb-129">For additional information, see [Using Generic Data Types](using-generic-data-types.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="fb9cb-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fb9cb-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fb9cb-131">Unicode na API do Windows</span><span class="sxs-lookup"><span data-stu-id="fb9cb-131">Unicode in the Windows API</span></span>](unicode-in-the-windows-api.md)
</dt> </dl>

 

 
