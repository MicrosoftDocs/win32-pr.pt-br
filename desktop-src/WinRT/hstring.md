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
# <a name="hstring"></a><span data-ttu-id="a2f81-103">HSTRING</span><span class="sxs-lookup"><span data-stu-id="a2f81-103">HSTRING</span></span>

<span data-ttu-id="a2f81-104">Um identificador para uma cadeia de caracteres Windows Runtime.</span><span class="sxs-lookup"><span data-stu-id="a2f81-104">A handle to a Windows Runtime string.</span></span>


```C++
typedef HSTRING__* HSTRING;
```



## <a name="remarks"></a><span data-ttu-id="a2f81-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="a2f81-105">Remarks</span></span>

<span data-ttu-id="a2f81-106">Use **HSTRING** para representar cadeias de caracteres imutáveis no Windows Runtime.</span><span class="sxs-lookup"><span data-stu-id="a2f81-106">Use **HSTRING** to represent immutable strings in the Windows Runtime.</span></span>

<span data-ttu-id="a2f81-107">O JavaScript e outras linguagens, como C \# e Microsoft Visual Basic, podem usar cadeias de caracteres que são representadas usando **HSTRING**.</span><span class="sxs-lookup"><span data-stu-id="a2f81-107">JavaScript and other languages, such as C\#, and Microsoft Visual Basic, can use strings that are represented by using **HSTRING**.</span></span> <span data-ttu-id="a2f81-108">A tabela a seguir mostra como um **HSTRING** é representado em outros idiomas.</span><span class="sxs-lookup"><span data-stu-id="a2f81-108">The following table shows how an **HSTRING** is represented in other languages.</span></span>



| <span data-ttu-id="a2f81-109">Linguagem de programação</span><span class="sxs-lookup"><span data-stu-id="a2f81-109">Programming Language</span></span>                                                                    | <span data-ttu-id="a2f81-110">Representação de cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="a2f81-110">String Representation</span></span>                                      |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------|
| [<span data-ttu-id="a2f81-111">C++/WinRT</span><span class="sxs-lookup"><span data-stu-id="a2f81-111">C++/WinRT</span></span>](/windows/uwp/cpp-and-winrt-apis/intro-to-using-cpp-with-winrt)              | <span data-ttu-id="a2f81-112">classe [winrt:: hstring](/uwp/cpp-ref-for-winrt/hstring)</span><span class="sxs-lookup"><span data-stu-id="a2f81-112">[winrt::hstring](/uwp/cpp-ref-for-winrt/hstring) class</span></span>     |
| <span data-ttu-id="a2f81-113">Extensões de componente Visual C++ ([C++/CX](/cpp/cppcx/visual-c-language-reference-c-cx))</span><span class="sxs-lookup"><span data-stu-id="a2f81-113">Visual C++ component extensions ([C++/CX](/cpp/cppcx/visual-c-language-reference-c-cx))</span></span> | <span data-ttu-id="a2f81-114">Classe [Platform:: String](/cpp/cppcx/platform-string-class)</span><span class="sxs-lookup"><span data-stu-id="a2f81-114">[Platform::String](/cpp/cppcx/platform-string-class) class</span></span> |
| <span data-ttu-id="a2f81-115">JavaScript</span><span class="sxs-lookup"><span data-stu-id="a2f81-115">JavaScript</span></span>                                                                              | <span data-ttu-id="a2f81-116">Objeto String</span><span class="sxs-lookup"><span data-stu-id="a2f81-116">String object</span></span>                                              |
| <span data-ttu-id="a2f81-117">.NET Framework</span><span class="sxs-lookup"><span data-stu-id="a2f81-117">.NET Framework</span></span>                                                                          | <span data-ttu-id="a2f81-118">Classe System. String</span><span class="sxs-lookup"><span data-stu-id="a2f81-118">System.String class</span></span>                                        |



 

<span data-ttu-id="a2f81-119">O identificador **HSTRING** é um tipo de identificador padrão.</span><span class="sxs-lookup"><span data-stu-id="a2f81-119">The **HSTRING** handle is a standard handle type.</span></span> <span data-ttu-id="a2f81-120">Semanticamente, um **HSTRING** que contém o valor **NULL** representa a cadeia de caracteres vazia, que consiste em zero caracteres de conteúdo e um caractere **nulo** de terminação.</span><span class="sxs-lookup"><span data-stu-id="a2f81-120">Semantically, an **HSTRING** containing the value **NULL** represents the empty string, which consists of zero content characters and a terminating **NULL** character.</span></span> <span data-ttu-id="a2f81-121">A criação de uma cadeia de caracteres por meio de [**WindowsCreateString**](/windows/win32/api/winstring/nf-winstring-windowscreatestring) com zero caracteres produzirá o valor de identificador **NULL**.</span><span class="sxs-lookup"><span data-stu-id="a2f81-121">Creating a string via [**WindowsCreateString**](/windows/win32/api/winstring/nf-winstring-windowscreatestring) with zero characters will produce the handle value **NULL**.</span></span> <span data-ttu-id="a2f81-122">Ao chamar [**WindowsGetStringRawBuffer**](/windows/win32/api/winstring/nf-winstring-windowsgetstringrawbuffer) com o valor **NULL**, um ponteiro para uma cadeia de caracteres vazia, seguido somente pelo caractere de terminação **nul** , será retornado.</span><span class="sxs-lookup"><span data-stu-id="a2f81-122">When calling [**WindowsGetStringRawBuffer**](/windows/win32/api/winstring/nf-winstring-windowsgetstringrawbuffer) with the value **NULL**, a pointer to an empty string followed only by the **NUL** terminating character will be returned.</span></span> <span data-ttu-id="a2f81-123">Nenhum valor distinto existe para representar um **HSTRING** que não foi inicializado.</span><span class="sxs-lookup"><span data-stu-id="a2f81-123">No distinct value exists to represent an **HSTRING** that is uninitialized.</span></span>

<span data-ttu-id="a2f81-124">Chame a função [**WindowsCreateString**](/windows/win32/api/winstring/nf-winstring-windowscreatestring) para criar um novo **HSTRING** e chame a função [**WindowsDeleteString**](/windows/win32/api/winstring/nf-winstring-windowsdeletestring) para liberar a referência à memória de cadeia de caracteres de apoio.</span><span class="sxs-lookup"><span data-stu-id="a2f81-124">Call the [**WindowsCreateString**](/windows/win32/api/winstring/nf-winstring-windowscreatestring) function to create a new **HSTRING**, and call the [**WindowsDeleteString**](/windows/win32/api/winstring/nf-winstring-windowsdeletestring) function to release the reference to the backing string memory.</span></span> <span data-ttu-id="a2f81-125">Chame a função [**WindowsCreateStringReference**](/windows/win32/api/winstring/nf-winstring-windowscreatestringreference) para criar uma referência de cadeia de caracteres, que também é chamada de uma *cadeia de caracteres de passagem rápida*.</span><span class="sxs-lookup"><span data-stu-id="a2f81-125">Call the [**WindowsCreateStringReference**](/windows/win32/api/winstring/nf-winstring-windowscreatestringreference) function to create a string reference, which is also called a *fast-pass string*.</span></span>

<span data-ttu-id="a2f81-126">Copie um **HSTRING** chamando a função [**WindowsDuplicateString**](/windows/win32/api/winstring/nf-winstring-windowsduplicatestring) .</span><span class="sxs-lookup"><span data-stu-id="a2f81-126">Copy an **HSTRING** by calling the [**WindowsDuplicateString**](/windows/win32/api/winstring/nf-winstring-windowsduplicatestring) function.</span></span>

<span data-ttu-id="a2f81-127">Concatene duas cadeias de caracteres chamando a função [**WindowsConcatString**](/windows/win32/api/winstring/nf-winstring-windowsconcatstring) .</span><span class="sxs-lookup"><span data-stu-id="a2f81-127">Concatenate two strings by calling the [**WindowsConcatString**](/windows/win32/api/winstring/nf-winstring-windowsconcatstring) function.</span></span>

<span data-ttu-id="a2f81-128">Acesse a memória de cadeia de caracteres de backup chamando a função [**WindowsGetStringRawBuffer**](/windows/win32/api/winstring/nf-winstring-windowsgetstringrawbuffer) .</span><span class="sxs-lookup"><span data-stu-id="a2f81-128">Access the backing string memory by calling the [**WindowsGetStringRawBuffer**](/windows/win32/api/winstring/nf-winstring-windowsgetstringrawbuffer) function.</span></span>

<span data-ttu-id="a2f81-129">**HSTRING** pode armazenar e usar os caracteres **nul** inseridos.</span><span class="sxs-lookup"><span data-stu-id="a2f81-129">**HSTRING** can store and use embedded **NUL** characters.</span></span> <span data-ttu-id="a2f81-130">Use a função [**WindowsStringHasEmbeddedNull**](/windows/win32/api/winstring/nf-winstring-windowsstringhasembeddednull) para verificar se há caracteres **nul** inseridos antes de usar qualquer função que possa produzir resultados inesperados.</span><span class="sxs-lookup"><span data-stu-id="a2f81-130">Use the [**WindowsStringHasEmbeddedNull**](/windows/win32/api/winstring/nf-winstring-windowsstringhasembeddednull) function to check for embedded **NUL** characters before using any functions which may produce unexpected results.</span></span> <span data-ttu-id="a2f81-131">Por exemplo, a maioria das funções do Windows usa **LPCWSTR** como um parâmetro de entrada e calcula o comprimento da cadeia de caracteres somente até que a primeira **nul** seja encontrada.</span><span class="sxs-lookup"><span data-stu-id="a2f81-131">For example, most of the Windows functions use **LPCWSTR** as an input parameter, and they compute the length of the string only until the first **NUL** is encountered.</span></span>

<span data-ttu-id="a2f81-132">A cadeia de caracteres de backup deve permanecer imutável e terminada em nulo.</span><span class="sxs-lookup"><span data-stu-id="a2f81-132">The backing string must remain immutable and null-terminated.</span></span> <span data-ttu-id="a2f81-133">Quando o código de chamada cria uma referência de cadeia de caracteres usando a função [**WindowsCreateStringReference**](/windows/win32/api/winstring/nf-winstring-windowscreatestringreference) , a memória que contém a representação de cadeia de caracteres de backup pertence ao chamador.</span><span class="sxs-lookup"><span data-stu-id="a2f81-133">When calling code creates a string reference by using the [**WindowsCreateStringReference**](/windows/win32/api/winstring/nf-winstring-windowscreatestringreference) function, the memory containing the backing string representation is owned by the caller.</span></span> <span data-ttu-id="a2f81-134">O Windows Runtime se baseia no conteúdo da cadeia de caracteres original para permanecer inalterado.</span><span class="sxs-lookup"><span data-stu-id="a2f81-134">The Windows Runtime relies on the contents of the original string to remain unchanged.</span></span> <span data-ttu-id="a2f81-135">Ao passar uma referência de cadeia de caracteres para o Windows Runtime, é responsabilidade do chamador garantir que o conteúdo da cadeia de caracteres seja inalterável e **nul** seja encerrado durante a chamada.</span><span class="sxs-lookup"><span data-stu-id="a2f81-135">When passing a string reference into the Windows Runtime, it is the caller’s responsibility to ensure that the string’s contents are unchanging and **NUL** terminated for the duration of the call.</span></span> <span data-ttu-id="a2f81-136">O Windows Runtime libera Todas as referências para a referência de cadeia de caracteres quando a chamada retorna.</span><span class="sxs-lookup"><span data-stu-id="a2f81-136">The Windows Runtime releases all references to the string reference when the call returns.</span></span>

<span data-ttu-id="a2f81-137">Quando você recebe um **HSTRING** como um parâmetro out, é uma prática recomendada definir o identificador como **nulo** quando terminar com ele.</span><span class="sxs-lookup"><span data-stu-id="a2f81-137">When you receive an **HSTRING** as an out parameter, it is good practice to set the handle to **NULL** when you are finished with it.</span></span>

<span data-ttu-id="a2f81-138">Chame a função [**WindowsPreallocateStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspreallocatestringbuffer) para alocar um buffer de cadeia de caracteres mutável que você pode usar para criar uma **HSTRING** imutável.</span><span class="sxs-lookup"><span data-stu-id="a2f81-138">Call the [**WindowsPreallocateStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspreallocatestringbuffer) function to allocate a mutable string buffer that you can use to create an immutable **HSTRING**.</span></span> <span data-ttu-id="a2f81-139">Quando você terminar de preencher o buffer, chame a função [**WindowsPromoteStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspromotestringbuffer) para criar o **HSTRING**.</span><span class="sxs-lookup"><span data-stu-id="a2f81-139">When you have finished populating the buffer, you call the [**WindowsPromoteStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspromotestringbuffer) function to create the **HSTRING**.</span></span> <span data-ttu-id="a2f81-140">Esse padrão de construção de duas fases permite a funcionalidade semelhante a um "Construtor de cadeias de caracteres".</span><span class="sxs-lookup"><span data-stu-id="a2f81-140">This two-phase construction pattern enables functionality that is similar to a "string builder."</span></span>

## <a name="requirements"></a><span data-ttu-id="a2f81-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a2f81-141">Requirements</span></span>



| <span data-ttu-id="a2f81-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="a2f81-142">Requirement</span></span> | <span data-ttu-id="a2f81-143">Valor</span><span class="sxs-lookup"><span data-stu-id="a2f81-143">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a2f81-144">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a2f81-144">Minimum supported client</span></span><br/> | <span data-ttu-id="a2f81-145">Windows 8</span><span class="sxs-lookup"><span data-stu-id="a2f81-145">Windows 8</span></span><br/>                                                                 |
| <span data-ttu-id="a2f81-146">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a2f81-146">Minimum supported server</span></span><br/> | <span data-ttu-id="a2f81-147">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a2f81-147">Windows Server 2012</span></span><br/>                                                       |
| <span data-ttu-id="a2f81-148">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a2f81-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="a2f81-149"><dt>Hstring. h</dt></span><span class="sxs-lookup"><span data-stu-id="a2f81-149"><dt>Hstring.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2f81-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="a2f81-150">See also</span></span>

<dl> <span data-ttu-id="a2f81-151"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="a2f81-151"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="a2f81-152">**WindowsCreateString**</span><span class="sxs-lookup"><span data-stu-id="a2f81-152">**WindowsCreateString**</span></span>](/windows/win32/api/winstring/nf-winstring-windowscreatestring)
</dt> <dt>

[<span data-ttu-id="a2f81-153">**WindowsDeleteString**</span><span class="sxs-lookup"><span data-stu-id="a2f81-153">**WindowsDeleteString**</span></span>](/windows/win32/api/winstring/nf-winstring-windowsdeletestring)
</dt> <dt>

[<span data-ttu-id="a2f81-154">**WindowsDuplicateString**</span><span class="sxs-lookup"><span data-stu-id="a2f81-154">**WindowsDuplicateString**</span></span>](/windows/win32/api/winstring/nf-winstring-windowsduplicatestring)
</dt> <dt>

[<span data-ttu-id="a2f81-155">**WindowsPreallocateStringBuffer**</span><span class="sxs-lookup"><span data-stu-id="a2f81-155">**WindowsPreallocateStringBuffer**</span></span>](/windows/win32/api/winstring/nf-winstring-windowspreallocatestringbuffer)
</dt> </dl>

 

 
