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
# <a name="working-with-strings"></a><span data-ttu-id="ae3c8-103">Trabalhando com Cadeias de Caracteres</span><span class="sxs-lookup"><span data-stu-id="ae3c8-103">Working with Strings</span></span>

<span data-ttu-id="ae3c8-104">O Windows nativamente dá suporte a cadeias de caracteres Unicode para elementos de interface do usuário, nomes de arquivos e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="ae3c8-104">Windows natively supports Unicode strings for UI elements, file names, and so forth.</span></span> <span data-ttu-id="ae3c8-105">Unicode é a codificação de caractere preferencial, pois dá suporte a todos os conjuntos de caracteres e idiomas.</span><span class="sxs-lookup"><span data-stu-id="ae3c8-105">Unicode is the preferred character encoding, because it supports all character sets and languages.</span></span> <span data-ttu-id="ae3c8-106">O Windows representa caracteres Unicode usando a codificação UTF-16, na qual cada caractere é codificado como um valor de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="ae3c8-106">Windows represents Unicode characters using UTF-16 encoding, in which each character is encoded as a 16-bit value.</span></span> <span data-ttu-id="ae3c8-107">Caracteres UTF-16 são chamados de caracteres *largos* , para distingui-los de caracteres ANSI de 8 bits.</span><span class="sxs-lookup"><span data-stu-id="ae3c8-107">UTF-16 characters are called *wide* characters, to distinguish them from 8-bit ANSI characters.</span></span> <span data-ttu-id="ae3c8-108">O compilador Visual C++ dá suporte ao tipo de dados interno **WCHAR \_ t** para caracteres largos.</span><span class="sxs-lookup"><span data-stu-id="ae3c8-108">The Visual C++ compiler supports the built-in data type **wchar\_t** for wide characters.</span></span> <span data-ttu-id="ae3c8-109">O arquivo de cabeçalho WinNT. h também define o seguinte **typedef**.</span><span class="sxs-lookup"><span data-stu-id="ae3c8-109">The header file WinNT.h also defines the following **typedef**.</span></span>


```C++
typedef wchar_t WCHAR;
```



<span data-ttu-id="ae3c8-110">Você verá as duas versões no código de exemplo do MSDN.</span><span class="sxs-lookup"><span data-stu-id="ae3c8-110">You will see both versions in MSDN example code.</span></span> <span data-ttu-id="ae3c8-111">Para declarar um literal de caractere largo ou um literal de cadeia de caracteres largo, coloque **L** antes do literal.</span><span class="sxs-lookup"><span data-stu-id="ae3c8-111">To declare a wide-character literal or a wide-character string literal, put **L** before the literal.</span></span>


```C++
wchar_t a = L'a';
wchar_t *str = L"hello";
```



<span data-ttu-id="ae3c8-112">Aqui estão alguns outros TYPEDEFs relacionados a cadeias de caracteres que você verá:</span><span class="sxs-lookup"><span data-stu-id="ae3c8-112">Here are some other string-related typedefs that you will see:</span></span>



| <span data-ttu-id="ae3c8-113">Typedef</span><span class="sxs-lookup"><span data-stu-id="ae3c8-113">Typedef</span></span>                   | <span data-ttu-id="ae3c8-114">Definição</span><span class="sxs-lookup"><span data-stu-id="ae3c8-114">Definition</span></span>       |
|---------------------------|------------------|
| <span data-ttu-id="ae3c8-115">**CHAR**</span><span class="sxs-lookup"><span data-stu-id="ae3c8-115">**CHAR**</span></span>                  | `char`           |
| <span data-ttu-id="ae3c8-116">**PSTR** ou **LPSTR**</span><span class="sxs-lookup"><span data-stu-id="ae3c8-116">**PSTR** or **LPSTR**</span></span>     | `char*`          |
| <span data-ttu-id="ae3c8-117">**PCSTR** ou **LPCSTR**</span><span class="sxs-lookup"><span data-stu-id="ae3c8-117">**PCSTR** or **LPCSTR**</span></span>   | `const char*`    |
| <span data-ttu-id="ae3c8-118">**PWSTR** ou **LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="ae3c8-118">**PWSTR** or **LPWSTR**</span></span>   | `wchar_t*`       |
| <span data-ttu-id="ae3c8-119">**PCWSTR** ou **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="ae3c8-119">**PCWSTR** or **LPCWSTR**</span></span> | `const wchar_t*` |



 

## <a name="unicode-and-ansi-functions"></a><span data-ttu-id="ae3c8-120">Funções Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="ae3c8-120">Unicode and ANSI Functions</span></span>

<span data-ttu-id="ae3c8-121">Quando a Microsoft introduziu o suporte a Unicode no Windows, ela facilitou a transição fornecendo dois conjuntos paralelos de APIs, um para cadeias de caracteres ANSI e o outro para cadeias de caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="ae3c8-121">When Microsoft introduced Unicode support to Windows, it eased the transition by providing two parallel sets of APIs, one for ANSI strings and the other for Unicode strings.</span></span> <span data-ttu-id="ae3c8-122">Por exemplo, há duas funções para definir o texto da barra de título de uma janela:</span><span class="sxs-lookup"><span data-stu-id="ae3c8-122">For example, there are two functions to set the text of a window's title bar:</span></span>

-   <span data-ttu-id="ae3c8-123">**SetWindowTextA** usa uma cadeia de caracteres ANSI.</span><span class="sxs-lookup"><span data-stu-id="ae3c8-123">**SetWindowTextA** takes an ANSI string.</span></span>
-   <span data-ttu-id="ae3c8-124">**SetWindowTextW** usa uma cadeia de caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="ae3c8-124">**SetWindowTextW** takes a Unicode string.</span></span>

<span data-ttu-id="ae3c8-125">Internamente, a versão ANSI traduz a cadeia de caracteres para Unicode.</span><span class="sxs-lookup"><span data-stu-id="ae3c8-125">Internally, the ANSI version translates the string to Unicode.</span></span> <span data-ttu-id="ae3c8-126">Os cabeçalhos do Windows também definem uma macro que é resolvida para a versão Unicode quando o símbolo de pré-processador `UNICODE` é definido ou a versão ANSI, caso contrário.</span><span class="sxs-lookup"><span data-stu-id="ae3c8-126">The Windows headers also define a macro that resolves to the Unicode version when the preprocessor symbol `UNICODE` is defined or the ANSI version otherwise.</span></span>


```C++
#ifdef UNICODE
#define SetWindowText  SetWindowTextW
#else
#define SetWindowText  SetWindowTextA
#endif 
```



<span data-ttu-id="ae3c8-127">No MSDN, a função está documentada sob o nome [**SetWindowText**](/windows/desktop/api/winuser/nf-winuser-setwindowtexta), embora seja realmente o nome da macro, não o nome real da função.</span><span class="sxs-lookup"><span data-stu-id="ae3c8-127">In MSDN, the function is documented under the name [**SetWindowText**](/windows/desktop/api/winuser/nf-winuser-setwindowtexta), even though that is really the macro name, not the actual function name.</span></span>

<span data-ttu-id="ae3c8-128">Os novos aplicativos sempre devem chamar as versões Unicode.</span><span class="sxs-lookup"><span data-stu-id="ae3c8-128">New applications should always call the Unicode versions.</span></span> <span data-ttu-id="ae3c8-129">Muitas linguagens de mundo exigem Unicode.</span><span class="sxs-lookup"><span data-stu-id="ae3c8-129">Many world languages require Unicode.</span></span> <span data-ttu-id="ae3c8-130">Se você usar cadeias de caracteres ANSI, será impossível localizar seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ae3c8-130">If you use ANSI strings, it will be impossible to localize your application.</span></span> <span data-ttu-id="ae3c8-131">As versões ANSI também são menos eficientes, pois o sistema operacional deve converter as cadeias de caracteres ANSI em Unicode em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="ae3c8-131">The ANSI versions are also less efficient, because the operating system must convert the ANSI strings to Unicode at run time.</span></span> <span data-ttu-id="ae3c8-132">Dependendo de sua preferência, você pode chamar as funções Unicode explicitamente, como **SetWindowTextW**, ou usar as macros.</span><span class="sxs-lookup"><span data-stu-id="ae3c8-132">Depending on your preference, you can call the Unicode functions explicitly, such as **SetWindowTextW**, or use the macros.</span></span> <span data-ttu-id="ae3c8-133">O código de exemplo no MSDN normalmente chama as macros, mas as duas formas são exatamente equivalentes.</span><span class="sxs-lookup"><span data-stu-id="ae3c8-133">The example code on MSDN typically calls the macros, but the two forms are exactly equivalent.</span></span> <span data-ttu-id="ae3c8-134">As APIs mais recentes do Windows têm apenas uma versão Unicode, sem nenhuma versão ANSI correspondente.</span><span class="sxs-lookup"><span data-stu-id="ae3c8-134">Most newer APIs in Windows have just a Unicode version, with no corresponding ANSI version.</span></span>

## <a name="tchars"></a><span data-ttu-id="ae3c8-135">TCHARs</span><span class="sxs-lookup"><span data-stu-id="ae3c8-135">TCHARs</span></span>

<span data-ttu-id="ae3c8-136">De volta quando os aplicativos precisarem dar suporte ao Windows NT, bem como ao Windows 95, ao Windows 98 e ao Windows me, era útil compilar o mesmo código para cadeias de caracteres ANSI ou Unicode, dependendo da plataforma de destino.</span><span class="sxs-lookup"><span data-stu-id="ae3c8-136">Back when applications needed to support both Windows NT as well as Windows 95, Windows 98, and Windows Me, it was useful to compile the same code for either ANSI or Unicode strings, depending on the target platform.</span></span> <span data-ttu-id="ae3c8-137">Para esse fim, o SDK do Windows fornece macros que mapeiam cadeias de caracteres para Unicode ou ANSI, dependendo da plataforma.</span><span class="sxs-lookup"><span data-stu-id="ae3c8-137">To this end, the Windows SDK provides macros that map strings to Unicode or ANSI, depending on the platform.</span></span>



| <span data-ttu-id="ae3c8-138">Macro</span><span class="sxs-lookup"><span data-stu-id="ae3c8-138">Macro</span></span>     | <span data-ttu-id="ae3c8-139">Unicode</span><span class="sxs-lookup"><span data-stu-id="ae3c8-139">Unicode</span></span>   | <span data-ttu-id="ae3c8-140">ANSI</span><span class="sxs-lookup"><span data-stu-id="ae3c8-140">ANSI</span></span>   |
|-----------|-----------|--------|
| <span data-ttu-id="ae3c8-141">TCHAR</span><span class="sxs-lookup"><span data-stu-id="ae3c8-141">TCHAR</span></span>     | `wchar_t` | `char` |
| <span data-ttu-id="ae3c8-142">TEXTO ("x")</span><span class="sxs-lookup"><span data-stu-id="ae3c8-142">TEXT("x")</span></span> | `L"x"`    | `"x"`  |



 

<span data-ttu-id="ae3c8-143">Por exemplo, o código a seguir:</span><span class="sxs-lookup"><span data-stu-id="ae3c8-143">For example, the following code:</span></span>


```C++
SetWindowText(TEXT("My Application"));
```



<span data-ttu-id="ae3c8-144">resolve para um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="ae3c8-144">resolves to one of the following:</span></span>


```C++
SetWindowTextW(L"My Application"); // Unicode function with wide-character string.

SetWindowTextA("My Application");  // ANSI function.
```



<span data-ttu-id="ae3c8-145">As macros **Text** e **TCHAR** são menos úteis hoje, porque todos os aplicativos devem usar Unicode.</span><span class="sxs-lookup"><span data-stu-id="ae3c8-145">The **TEXT** and **TCHAR** macros are less useful today, because all applications should use Unicode.</span></span> <span data-ttu-id="ae3c8-146">No entanto, você pode vê-los em código mais antigo e em alguns dos exemplos de código do MSDN.</span><span class="sxs-lookup"><span data-stu-id="ae3c8-146">However, you might see them in older code and in some of the MSDN code examples.</span></span>

<span data-ttu-id="ae3c8-147">Os cabeçalhos das bibliotecas de tempo de execução do Microsoft C definem um conjunto de macros semelhantes.</span><span class="sxs-lookup"><span data-stu-id="ae3c8-147">The headers for the Microsoft C run-time libraries define a similar set of macros.</span></span> <span data-ttu-id="ae3c8-148">Por exemplo, **\_ tcslen** é resolvido para **strlen** se `_UNICODE` estiver indefinido; caso contrário, ele será resolvido para **wcslen**, que é a versão de caractere largo do **strlen**.</span><span class="sxs-lookup"><span data-stu-id="ae3c8-148">For example, **\_tcslen** resolves to **strlen** if `_UNICODE` is undefined; otherwise it resolves to **wcslen**, which is the wide-character version of **strlen**.</span></span>


```C++
#ifdef _UNICODE
#define _tcslen     wcslen
#else
#define _tcslen     strlen
#endif 
```



<span data-ttu-id="ae3c8-149">Cuidado: alguns cabeçalhos usam o símbolo de pré-processador `UNICODE` , outros usam `_UNICODE` com um prefixo de sublinhado.</span><span class="sxs-lookup"><span data-stu-id="ae3c8-149">Be careful: Some headers use the preprocessor symbol `UNICODE`, others use `_UNICODE` with an underscore prefix.</span></span> <span data-ttu-id="ae3c8-150">Sempre defina os dois símbolos.</span><span class="sxs-lookup"><span data-stu-id="ae3c8-150">Always define both symbols.</span></span> <span data-ttu-id="ae3c8-151">O Visual C++ os define por padrão quando você cria um novo projeto.</span><span class="sxs-lookup"><span data-stu-id="ae3c8-151">Visual C++ sets them both by default when you create a new project.</span></span>

## <a name="next"></a><span data-ttu-id="ae3c8-152">Avançar</span><span class="sxs-lookup"><span data-stu-id="ae3c8-152">Next</span></span>

[<span data-ttu-id="ae3c8-153">O que é uma janela?</span><span class="sxs-lookup"><span data-stu-id="ae3c8-153">What Is a Window?</span></span>](what-is-a-window-.md)

 

 
