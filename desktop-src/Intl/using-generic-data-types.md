---
description: Se você usar tipos de dados genéricos em seu código, ele poderá ser compilado para Unicode simplesmente usando uma diretiva de pré-processador para definir &\# 0034; UNICODE&\# 0034; antes das \# instruções include para os arquivos de cabeçalho.
ms.assetid: 1c9cbb18-9295-4847-86c1-d596668cbe57
title: Usando tipos de dados genéricos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0e2604f87b12e86076bed47f509c6398fa8482b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105758134"
---
# <a name="using-generic-data-types"></a><span data-ttu-id="05db1-103">Usando tipos de dados genéricos</span><span class="sxs-lookup"><span data-stu-id="05db1-103">Using Generic Data Types</span></span>

<span data-ttu-id="05db1-104">Se você usar tipos de dados genéricos em seu código, ele poderá ser compilado para [Unicode](unicode.md) simplesmente usando uma diretiva de pré-processador para definir "Unicode" antes das instruções **\# include** para os arquivos de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="05db1-104">If you use generic data types in your code, it can be compiled for [Unicode](unicode.md) simply by using a preprocessor directive to define "UNICODE" before the **\#include** statements for the header files.</span></span> <span data-ttu-id="05db1-105">Para compilar o código para [páginas de código do Windows (ANSI)](code-pages.md), omita a definição "Unicode".</span><span class="sxs-lookup"><span data-stu-id="05db1-105">To compile the code for [Windows (ANSI) code pages](code-pages.md), omit the "UNICODE" definition.</span></span> <span data-ttu-id="05db1-106">Novos aplicativos do Windows devem usar Unicode para evitar as inconsistências de páginas de código variadas e simplificar a localização.</span><span class="sxs-lookup"><span data-stu-id="05db1-106">New Windows applications should use Unicode to avoid the inconsistencies of varied code pages and simplify localization.</span></span>

<span data-ttu-id="05db1-107">Para criar o código-fonte que pode ser compilado para usar caracteres e cadeias Unicode ou para usar caracteres e cadeias de caractere de páginas de código do Windows:</span><span class="sxs-lookup"><span data-stu-id="05db1-107">To create source code that can be compiled either to use Unicode characters and strings or to use characters and strings from Windows code pages:</span></span>

1.  <span data-ttu-id="05db1-108">Use tipos de dados genéricos, como TCHAR, LPTSTR e LPTCH, para todos os tipos de caracteres e cadeias de caracteres usados para texto.</span><span class="sxs-lookup"><span data-stu-id="05db1-108">Use generic data types, such as TCHAR, LPTSTR, and LPTCH, for all character and string types used for text.</span></span> <span data-ttu-id="05db1-109">Para obter mais informações sobre tipos genéricos, consulte [tipos de dados do Windows para cadeias de caracteres](windows-data-types-for-strings.md).</span><span class="sxs-lookup"><span data-stu-id="05db1-109">For more about generic types, see [Windows Data Types for Strings](windows-data-types-for-strings.md).</span></span>
2.  <span data-ttu-id="05db1-110">Certifique-se de que os ponteiros para buffers de dados não texto ou matrizes de bytes binários sejam codificados com tipos de dados como LPBYTE ou LPWORD, em vez do tipo LPTSTR ou LPTCH.</span><span class="sxs-lookup"><span data-stu-id="05db1-110">Be sure that pointers to non-text data buffers or binary byte arrays are coded with data types such as LPBYTE or LPWORD, instead of the LPTSTR or LPTCH type.</span></span>
3.  <span data-ttu-id="05db1-111">Declare ponteiros de tipo indeterminado explicitamente como ponteiros void usando LPVOID conforme apropriado.</span><span class="sxs-lookup"><span data-stu-id="05db1-111">Declare pointers of indeterminate type explicitly as void pointers by using LPVOID as appropriate.</span></span>
4.  <span data-ttu-id="05db1-112">Torne o tipo aritmético de ponteiro independente.</span><span class="sxs-lookup"><span data-stu-id="05db1-112">Make pointer arithmetic type-independent.</span></span> <span data-ttu-id="05db1-113">O uso de unidades de tamanho TCHAR produz variáveis que são 2 bytes se o UNICODE estiver definido e 1 byte se UNICODE não estiver definido.</span><span class="sxs-lookup"><span data-stu-id="05db1-113">Using units of TCHAR size yields variables that are 2 bytes if UNICODE is defined, and 1 byte if UNICODE is not defined.</span></span> <span data-ttu-id="05db1-114">O uso de aritmética de ponteiro sempre retorna o número de elementos indicados pelo ponteiro, se os elementos têm 1 ou 2 bytes de tamanho.</span><span class="sxs-lookup"><span data-stu-id="05db1-114">Using pointer arithmetic always returns the number of elements indicated by the pointer, whether the elements are 1 or 2 bytes in size.</span></span> <span data-ttu-id="05db1-115">A expressão a seguir sempre recupera o número de elementos, independentemente de o UNICODE ser definido ou não.</span><span class="sxs-lookup"><span data-stu-id="05db1-115">The following expression always retrieves the number of elements, regardless of whether UNICODE is defined.</span></span>

    ```C++
    cCount = lpEnd - lpStart;
    ```

    

    <span data-ttu-id="05db1-116">A expressão a seguir determina o número de bytes usados.</span><span class="sxs-lookup"><span data-stu-id="05db1-116">The following expression determines the number of bytes used.</span></span>

    ```C++
    cByteCount = (lpEnd - lpStart) * sizeof(TCHAR);
    ```

    

    <span data-ttu-id="05db1-117">Não é necessário alterar uma instrução como a seguinte, pois o incremento do ponteiro aponta para o próximo elemento Character.</span><span class="sxs-lookup"><span data-stu-id="05db1-117">There is no need to change a statement like the following one, because the pointer increment points to the next character element.</span></span>

    ```C++
    chNext = *++lpText;
    ```

    

5.  <span data-ttu-id="05db1-118">Substitua cadeias de caracteres literais e constantes de caractere de manifesto por macros.</span><span class="sxs-lookup"><span data-stu-id="05db1-118">Replace literal strings and manifest character constants with macros.</span></span> <span data-ttu-id="05db1-119">Altere expressões como a seguinte.</span><span class="sxs-lookup"><span data-stu-id="05db1-119">Change expressions like the following one.</span></span>

    ```C++
    while(*lpFileName++ != '\\')
    {
        // ...
    }
    ```

    

    <span data-ttu-id="05db1-120">Use a macro de [**texto**](/windows/desktop/api/Winnt/nf-winnt-text) da seguinte maneira nesta expressão.</span><span class="sxs-lookup"><span data-stu-id="05db1-120">Use the [**TEXT**](/windows/desktop/api/Winnt/nf-winnt-text) macro as follows in this expression.</span></span>

    ```C++
    while(*lpFileName++ != TEXT('\\'))
    {
        // ...
    }
    ```

    

    <span data-ttu-id="05db1-121">A macro [**Text**](/windows/desktop/api/Winnt/nf-winnt-text) faz com que as cadeias de caracteres sejam avaliadas como L "String" quando o Unicode é definido e como "String" caso contrário.</span><span class="sxs-lookup"><span data-stu-id="05db1-121">The [**TEXT**](/windows/desktop/api/Winnt/nf-winnt-text) macro causes strings to be evaluated as L"string" when UNICODE is defined, and as "string" otherwise.</span></span> <span data-ttu-id="05db1-122">Para um gerenciamento mais fácil, mova cadeias de caracteres literais para recursos, especialmente se eles contiverem personagens fora do intervalo ASCII (0x00 a 0x7F) ou forem expostos na interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="05db1-122">For easier management, move literal strings into resources, especially if they contain characters outside the ASCII range (0x00 through 0x7F) or are exposed at the user interface.</span></span> <span data-ttu-id="05db1-123">Para dar suporte à localização de seu aplicativo para diferentes idiomas nacionais, é muito importante que todas as cadeias de caracteres da interface do usuário estejam em recursos localizáveis.</span><span class="sxs-lookup"><span data-stu-id="05db1-123">To support localization of your application for different national languages, it is very important for all user interface strings to be in localizable resources.</span></span>

6.  <span data-ttu-id="05db1-124">Use as versões genéricas das funções do Windows.</span><span class="sxs-lookup"><span data-stu-id="05db1-124">Use the generic versions of the Windows functions.</span></span> <span data-ttu-id="05db1-125">Para obter mais informações, consulte [convenções para protótipos de função](conventions-for-function-prototypes.md).</span><span class="sxs-lookup"><span data-stu-id="05db1-125">For more information, see [Conventions for Function Prototypes](conventions-for-function-prototypes.md).</span></span>
7.  <span data-ttu-id="05db1-126">Use as versões genéricas das funções de cadeia de caracteres da biblioteca C padrão e lembre-se de definir " \_ Unicode", bem como "Unicode", conforme discutido nas [funções padrão do C](standard-c-functions.md).</span><span class="sxs-lookup"><span data-stu-id="05db1-126">Use the generic versions of the standard C library string functions, and remember to define "\_UNICODE" as well as "UNICODE", as discussed in [Standard C Functions](standard-c-functions.md).</span></span>
8.  <span data-ttu-id="05db1-127">Se você estiver adaptando um aplicativo originalmente escrito para páginas de código do Windows, lembre-se de alterar qualquer código que dependa de 255 como o maior valor para um caractere.</span><span class="sxs-lookup"><span data-stu-id="05db1-127">If you are adapting an application originally written for Windows code pages, remember to change any code that relies on 255 as the largest value for a character.</span></span>

<span data-ttu-id="05db1-128">Quando você compila o código escrito conforme descrito acima, o compilador pode criar versões de página de código Unicode e do Windows de seu aplicativo a partir da mesma origem.</span><span class="sxs-lookup"><span data-stu-id="05db1-128">When you compile code that you have written as outlined above, the compiler can create both Unicode and Windows code page versions of your application from the same source.</span></span> <span data-ttu-id="05db1-129">Dependendo das definições de UNICODE, as funções genéricas são resolvidas para produzir os mesmos arquivos binários como se você escrevesse o código exclusivamente para Unicode ou exclusivamente para páginas de código do Windows.</span><span class="sxs-lookup"><span data-stu-id="05db1-129">Depending on the definitions for UNICODE, the generic functions are resolved to produce the same binary files as if you wrote code exclusively for Unicode or exclusively for Windows code pages.</span></span>

## <a name="related-topics"></a><span data-ttu-id="05db1-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="05db1-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="05db1-131">Usando Unicode e conjuntos de caracteres</span><span class="sxs-lookup"><span data-stu-id="05db1-131">Using Unicode and Character Sets</span></span>](using-unicode-and-character-sets.md)
</dt> </dl>

 

 



