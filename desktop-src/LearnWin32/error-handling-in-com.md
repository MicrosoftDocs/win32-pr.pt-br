---
title: Tratamento de erros no COM (introdução ao Win32 e ao C++)
description: Tratamento de erros no COM (introdução ao Win32 e ao C++)
ms.assetid: 022ca652-59d2-4513-9d73-1c6d8688c478
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b69cf89170087469fa6ef8587fb5377e6374f6a8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103914"
---
# <a name="error-handling-in-com-get-started-with-win32-and-c"></a><span data-ttu-id="7b867-103">Tratamento de erros no COM (introdução ao Win32 e ao C++)</span><span class="sxs-lookup"><span data-stu-id="7b867-103">Error Handling in COM (Get Started with Win32 and C++)</span></span>

<span data-ttu-id="7b867-104">COM usa valores **HRESULT** para indicar o êxito ou a falha de um método ou uma chamada de função.</span><span class="sxs-lookup"><span data-stu-id="7b867-104">COM uses **HRESULT** values to indicate the success or failure of a method or function call.</span></span> <span data-ttu-id="7b867-105">Vários cabeçalhos de SDK definem várias constantes **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7b867-105">Various SDK headers define various **HRESULT** constants.</span></span> <span data-ttu-id="7b867-106">Um conjunto comum de códigos de todo o sistema é definido no WinError. h.</span><span class="sxs-lookup"><span data-stu-id="7b867-106">A common set of system-wide codes is defined in WinError.h.</span></span> <span data-ttu-id="7b867-107">A tabela a seguir mostra alguns desses códigos de retorno em todo o sistema.</span><span class="sxs-lookup"><span data-stu-id="7b867-107">The following table shows some of those system-wide return codes.</span></span>



| <span data-ttu-id="7b867-108">Constante</span><span class="sxs-lookup"><span data-stu-id="7b867-108">Constant</span></span>            | <span data-ttu-id="7b867-109">Valor numérico</span><span class="sxs-lookup"><span data-stu-id="7b867-109">Numeric value</span></span> | <span data-ttu-id="7b867-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="7b867-110">Description</span></span>                                          |
|---------------------|---------------|------------------------------------------------------|
| <span data-ttu-id="7b867-111">**E \_ ACCESSDENIED**</span><span class="sxs-lookup"><span data-stu-id="7b867-111">**E\_ACCESSDENIED**</span></span> | <span data-ttu-id="7b867-112">0x80070005</span><span class="sxs-lookup"><span data-stu-id="7b867-112">0x80070005</span></span>    | <span data-ttu-id="7b867-113">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="7b867-113">Access denied.</span></span>                                       |
| <span data-ttu-id="7b867-114">**E \_ falha**</span><span class="sxs-lookup"><span data-stu-id="7b867-114">**E\_FAIL**</span></span>         | <span data-ttu-id="7b867-115">0x80004005</span><span class="sxs-lookup"><span data-stu-id="7b867-115">0x80004005</span></span>    | <span data-ttu-id="7b867-116">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="7b867-116">Unspecified error.</span></span>                                   |
| <span data-ttu-id="7b867-117">**E \_ INVALIDARG**</span><span class="sxs-lookup"><span data-stu-id="7b867-117">**E\_INVALIDARG**</span></span>   | <span data-ttu-id="7b867-118">0x80070057</span><span class="sxs-lookup"><span data-stu-id="7b867-118">0x80070057</span></span>    | <span data-ttu-id="7b867-119">Valor de parâmetro inválido.</span><span class="sxs-lookup"><span data-stu-id="7b867-119">Invalid parameter value.</span></span>                             |
| <span data-ttu-id="7b867-120">**E \_ OUTOFMEMORY**</span><span class="sxs-lookup"><span data-stu-id="7b867-120">**E\_OUTOFMEMORY**</span></span>  | <span data-ttu-id="7b867-121">0x8007000E</span><span class="sxs-lookup"><span data-stu-id="7b867-121">0x8007000E</span></span>    | <span data-ttu-id="7b867-122">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="7b867-122">Out of memory.</span></span>                                       |
| <span data-ttu-id="7b867-123">**\_ponteiro E**</span><span class="sxs-lookup"><span data-stu-id="7b867-123">**E\_POINTER**</span></span>      | <span data-ttu-id="7b867-124">0x80004003</span><span class="sxs-lookup"><span data-stu-id="7b867-124">0x80004003</span></span>    | <span data-ttu-id="7b867-125">**NULL** foi passado incorretamente para um valor de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="7b867-125">**NULL** was passed incorrectly for a pointer value.</span></span> |
| <span data-ttu-id="7b867-126">**E \_ inesperado**</span><span class="sxs-lookup"><span data-stu-id="7b867-126">**E\_UNEXPECTED**</span></span>   | <span data-ttu-id="7b867-127">0x8000FFFF</span><span class="sxs-lookup"><span data-stu-id="7b867-127">0x8000FFFF</span></span>    | <span data-ttu-id="7b867-128">Condição inesperada.</span><span class="sxs-lookup"><span data-stu-id="7b867-128">Unexpected condition.</span></span>                                |
| <span data-ttu-id="7b867-129">**S \_ OK**</span><span class="sxs-lookup"><span data-stu-id="7b867-129">**S\_OK**</span></span>           | <span data-ttu-id="7b867-130">0x0</span><span class="sxs-lookup"><span data-stu-id="7b867-130">0x0</span></span>           | <span data-ttu-id="7b867-131">Sucesso.</span><span class="sxs-lookup"><span data-stu-id="7b867-131">Success.</span></span>                                             |
| <span data-ttu-id="7b867-132">**\_falso**</span><span class="sxs-lookup"><span data-stu-id="7b867-132">**S\_FALSE**</span></span>        | <span data-ttu-id="7b867-133">0x1</span><span class="sxs-lookup"><span data-stu-id="7b867-133">0x1</span></span>           | <span data-ttu-id="7b867-134">Sucesso.</span><span class="sxs-lookup"><span data-stu-id="7b867-134">Success.</span></span>                                             |



 

<span data-ttu-id="7b867-135">Todas as constantes com o prefixo "E \_ " são códigos de erro.</span><span class="sxs-lookup"><span data-stu-id="7b867-135">All of the constants with the prefix "E\_" are error codes.</span></span> <span data-ttu-id="7b867-136">As constantes **s \_ OK** e **s \_ false** são códigos de êxito.</span><span class="sxs-lookup"><span data-stu-id="7b867-136">The constants **S\_OK** and **S\_FALSE** are both success codes.</span></span> <span data-ttu-id="7b867-137">Provavelmente, 99% dos métodos COM retornarão **S \_ OK** quando forem bem-sucedidos; mas não deixe esse fato enganar.</span><span class="sxs-lookup"><span data-stu-id="7b867-137">Probably 99% of COM methods return **S\_OK** when they succeed; but do not let this fact mislead you.</span></span> <span data-ttu-id="7b867-138">Um método pode retornar outros códigos de êxito e, portanto, sempre testar erros usando a macro [**Succeeded**](/windows/desktop/api/winerror/nf-winerror-succeeded) ou [**Failed**](/windows/desktop/api/winerror/nf-winerror-failed) .</span><span class="sxs-lookup"><span data-stu-id="7b867-138">A method might return other success codes, so always test for errors by using the [**SUCCEEDED**](/windows/desktop/api/winerror/nf-winerror-succeeded) or [**FAILED**](/windows/desktop/api/winerror/nf-winerror-failed) macro.</span></span> <span data-ttu-id="7b867-139">O código de exemplo a seguir mostra a maneira errada e a maneira correta de testar o êxito de uma chamada de função.</span><span class="sxs-lookup"><span data-stu-id="7b867-139">The following example code shows the wrong way and the right way to test for the success of a function call.</span></span>


```C++
// Wrong.
HRESULT hr = SomeFunction();
if (hr != S_OK)
{
    printf("Error!\n"); // Bad. hr might be another success code.
}

// Right.
HRESULT hr = SomeFunction();
if (FAILED(hr))
{
    printf("Error!\n"); 
}
```



<span data-ttu-id="7b867-140">O código de sucesso **S \_ false** merece menção.</span><span class="sxs-lookup"><span data-stu-id="7b867-140">The success code **S\_FALSE** deserves mention.</span></span> <span data-ttu-id="7b867-141">Alguns métodos usam **S \_ false** para significar, aproximadamente, uma condição negativa que não é uma falha.</span><span class="sxs-lookup"><span data-stu-id="7b867-141">Some methods use **S\_FALSE** to mean, roughly, a negative condition that is not a failure.</span></span> <span data-ttu-id="7b867-142">Ele também pode indicar um "não op" — o método foi bem-sucedido, mas não teve nenhum efeito.</span><span class="sxs-lookup"><span data-stu-id="7b867-142">It can also indicate a "no-op"—the method succeeded, but had no effect.</span></span> <span data-ttu-id="7b867-143">Por exemplo, a função [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) retornará **S \_ false** se você chamá-la uma segunda vez a partir do mesmo thread.</span><span class="sxs-lookup"><span data-stu-id="7b867-143">For example, the [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) function returns **S\_FALSE** if you call it a second time from the same thread.</span></span> <span data-ttu-id="7b867-144">Se você precisar diferenciar entre **s \_ OK** e o **\_ falso** em seu código, você deve testar o valor diretamente, mas ainda assim usar [**com falha**](/windows/desktop/api/winerror/nf-winerror-failed) ou com [**êxito**](/windows/desktop/api/winerror/nf-winerror-succeeded) para lidar com os casos restantes, conforme mostrado no código de exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="7b867-144">If you need to differentiate between **S\_OK** and **S\_FALSE** in your code, you should test the value directly, but still use [**FAILED**](/windows/desktop/api/winerror/nf-winerror-failed) or [**SUCCEEDED**](/windows/desktop/api/winerror/nf-winerror-succeeded) to handle the remaining cases, as shown in the following example code.</span></span>


```C++
if (hr == S_FALSE)
{
    // Handle special case.
}
else if (SUCCEEDED(hr))
{
    // Handle general success case.
}
else
{
    // Handle errors.
    printf("Error!\n"); 
}
```



<span data-ttu-id="7b867-145">Alguns valores **HRESULT** são específicos de um determinado recurso ou subsistema do Windows.</span><span class="sxs-lookup"><span data-stu-id="7b867-145">Some **HRESULT** values are specific to a particular feature or subsystem of Windows.</span></span> <span data-ttu-id="7b867-146">Por exemplo, a API de gráficos do Direct2D define o código de erro **D2DERR \_ \_ \_ formato de pixel sem suporte**, o que significa que o programa usou um formato de pixel sem suporte.</span><span class="sxs-lookup"><span data-stu-id="7b867-146">For example, the Direct2D graphics API defines the error code **D2DERR\_UNSUPPORTED\_PIXEL\_FORMAT**, which means that the program used an unsupported pixel format.</span></span> <span data-ttu-id="7b867-147">A documentação do MSDN geralmente fornece uma lista de códigos de erro específicos que um método pode retornar.</span><span class="sxs-lookup"><span data-stu-id="7b867-147">MSDN documentation often gives a list of specific error codes that a method might return.</span></span> <span data-ttu-id="7b867-148">No entanto, você não deve considerar essas listas como definitivas.</span><span class="sxs-lookup"><span data-stu-id="7b867-148">However, you should not consider these lists to be definitive.</span></span> <span data-ttu-id="7b867-149">Um método sempre pode retornar um valor **HRESULT** que não esteja listado na documentação.</span><span class="sxs-lookup"><span data-stu-id="7b867-149">A method can always return an **HRESULT** value that is not listed in the documentation.</span></span> <span data-ttu-id="7b867-150">Novamente, use as macros com [**êxito**](/windows/desktop/api/winerror/nf-winerror-succeeded) e [**com falha**](/windows/desktop/api/winerror/nf-winerror-failed) .</span><span class="sxs-lookup"><span data-stu-id="7b867-150">Again, use the [**SUCCEEDED**](/windows/desktop/api/winerror/nf-winerror-succeeded) and [**FAILED**](/windows/desktop/api/winerror/nf-winerror-failed) macros.</span></span> <span data-ttu-id="7b867-151">Se você testar um código de erro específico, inclua também um caso padrão.</span><span class="sxs-lookup"><span data-stu-id="7b867-151">If you test for a specific error code, include a default case as well.</span></span>


```C++
if (hr == D2DERR_UNSUPPORTED_PIXEL_FORMAT)
{
    // Handle the specific case of an unsupported pixel format.
}
else if (FAILED(hr))
{
    // Handle other errors.
}
```



## <a name="patterns-for-error-handling"></a><span data-ttu-id="7b867-152">Padrões para tratamento de erros</span><span class="sxs-lookup"><span data-stu-id="7b867-152">Patterns for Error Handling</span></span>

<span data-ttu-id="7b867-153">Esta seção examina alguns padrões para lidar COM erros de COM de forma estruturada.</span><span class="sxs-lookup"><span data-stu-id="7b867-153">This section looks at some patterns for handling COM errors in a structured way.</span></span> <span data-ttu-id="7b867-154">Cada padrão tem vantagens e desvantagens.</span><span class="sxs-lookup"><span data-stu-id="7b867-154">Each pattern has advantages and disadvantages.</span></span> <span data-ttu-id="7b867-155">Até certo ponto, a escolha é uma questão de gosto.</span><span class="sxs-lookup"><span data-stu-id="7b867-155">To some extent, the choice is a matter of taste.</span></span> <span data-ttu-id="7b867-156">Se você trabalha em um projeto existente, talvez ele já tenha diretrizes de codificação que contratam um estilo específico.</span><span class="sxs-lookup"><span data-stu-id="7b867-156">If you work on an existing project, it might already have coding guidelines that proscribe a particular style.</span></span> <span data-ttu-id="7b867-157">Independentemente de qual padrão você adotar, o código robusto obedecerá às regras a seguir.</span><span class="sxs-lookup"><span data-stu-id="7b867-157">Regardless of which pattern you adopt, robust code will obey the following rules.</span></span>

-   <span data-ttu-id="7b867-158">Para cada método ou função que retorna um **HRESULT**, verifique o valor de retorno antes de continuar.</span><span class="sxs-lookup"><span data-stu-id="7b867-158">For every method or function that returns an **HRESULT**, check the return value before proceeding.</span></span>
-   <span data-ttu-id="7b867-159">Libere os recursos depois que eles forem usados.</span><span class="sxs-lookup"><span data-stu-id="7b867-159">Release resources after they are used.</span></span>
-   <span data-ttu-id="7b867-160">Não tente acessar recursos inválidos ou não inicializados, como ponteiros **nulos** .</span><span class="sxs-lookup"><span data-stu-id="7b867-160">Do not attempt to access invalid or uninitialized resources, such as **NULL** pointers.</span></span>
-   <span data-ttu-id="7b867-161">Não tente usar um recurso depois de liberá-lo.</span><span class="sxs-lookup"><span data-stu-id="7b867-161">Do not try to use a resource after you release it.</span></span>

<span data-ttu-id="7b867-162">Com essas regras em mente, aqui estão quatro padrões para lidar com erros.</span><span class="sxs-lookup"><span data-stu-id="7b867-162">With these rules in mind, here are four patterns for handling errors.</span></span>

-   [<span data-ttu-id="7b867-163">IFS aninhado</span><span class="sxs-lookup"><span data-stu-id="7b867-163">Nested ifs</span></span>](#nested-ifs)
-   [<span data-ttu-id="7b867-164">IFS em cascata</span><span class="sxs-lookup"><span data-stu-id="7b867-164">Cascading ifs</span></span>](#cascading-ifs)
-   [<span data-ttu-id="7b867-165">Falha ao saltar</span><span class="sxs-lookup"><span data-stu-id="7b867-165">Jump on Fail</span></span>](#jump-on-fail)
-   [<span data-ttu-id="7b867-166">Lançar em caso de falha</span><span class="sxs-lookup"><span data-stu-id="7b867-166">Throw on Fail</span></span>](#throw-on-fail)

### <a name="nested-ifs"></a><span data-ttu-id="7b867-167">IFS aninhado</span><span class="sxs-lookup"><span data-stu-id="7b867-167">Nested ifs</span></span>

<span data-ttu-id="7b867-168">Depois de cada chamada que retorna um **HRESULT**, use uma instrução **If** para testar o êxito.</span><span class="sxs-lookup"><span data-stu-id="7b867-168">After every call that returns an **HRESULT**, use an **if** statement to test for success.</span></span> <span data-ttu-id="7b867-169">Em seguida, coloque a próxima chamada de método dentro do escopo da instrução **If** .</span><span class="sxs-lookup"><span data-stu-id="7b867-169">Then, put the next method call within the scope of the **if** statement.</span></span> <span data-ttu-id="7b867-170">Mais instruções **If** podem ser aninhadas tão profundamente quanto necessário.</span><span class="sxs-lookup"><span data-stu-id="7b867-170">More **if** statements can be nested as deeply as needed.</span></span> <span data-ttu-id="7b867-171">Os exemplos de código anteriores neste módulo têm todos usado esse padrão, mas aqui está novamente:</span><span class="sxs-lookup"><span data-stu-id="7b867-171">The previous code examples in this module have all used this pattern, but here it is again:</span></span>


```C++
HRESULT ShowDialog()
{
    IFileOpenDialog *pFileOpen;

    HRESULT hr = CoCreateInstance(__uuidof(FileOpenDialog), NULL, 
        CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pFileOpen));
    if (SUCCEEDED(hr))
    {
        hr = pFileOpen->Show(NULL);
        if (SUCCEEDED(hr))
        {
            IShellItem *pItem;
            hr = pFileOpen->GetResult(&pItem);
            if (SUCCEEDED(hr))
            {
                // Use pItem (not shown). 
                pItem->Release();
            }
        }
        pFileOpen->Release();
    }
    return hr;
}
```



<span data-ttu-id="7b867-172">Vantagens</span><span class="sxs-lookup"><span data-stu-id="7b867-172">Advantages</span></span>

-   <span data-ttu-id="7b867-173">As variáveis podem ser declaradas com escopo mínimo.</span><span class="sxs-lookup"><span data-stu-id="7b867-173">Variables can be declared with minimal scope.</span></span> <span data-ttu-id="7b867-174">Por exemplo, *pItem* não é declarado até que seja usado.</span><span class="sxs-lookup"><span data-stu-id="7b867-174">For example, *pItem* is not declared until it is used.</span></span>
-   <span data-ttu-id="7b867-175">Dentro de cada instrução **If** , determinadas invariáveis são verdadeiras: todas as chamadas anteriores foram bem-sucedidas e todos os recursos adquiridos ainda são válidos.</span><span class="sxs-lookup"><span data-stu-id="7b867-175">Within each **if** statement, certain invariants are true: All previous calls have succeeded, and all acquired resources are still valid.</span></span> <span data-ttu-id="7b867-176">No exemplo anterior, quando o programa atinge a instrução **If** mais interna, *pItem* e *pFileOpen* são conhecidos como válidos.</span><span class="sxs-lookup"><span data-stu-id="7b867-176">In the previous example, when the program reaches the innermost **if** statement, both *pItem* and *pFileOpen* are known to be valid.</span></span>
-   <span data-ttu-id="7b867-177">Fica claro quando liberar ponteiros de interface e outros recursos.</span><span class="sxs-lookup"><span data-stu-id="7b867-177">It is clear when to release interface pointers and other resources.</span></span> <span data-ttu-id="7b867-178">Você libera um recurso no final da instrução **If** que segue imediatamente a chamada que adquiriu o recurso.</span><span class="sxs-lookup"><span data-stu-id="7b867-178">You release a resource at the end of the **if** statement that immediately follows the call that acquired the resource.</span></span>

<span data-ttu-id="7b867-179">Desvantagens</span><span class="sxs-lookup"><span data-stu-id="7b867-179">Disadvantages</span></span>

-   <span data-ttu-id="7b867-180">Algumas pessoas consideram um aninhamento profundo e difícil de ler.</span><span class="sxs-lookup"><span data-stu-id="7b867-180">Some people find deep nesting hard to read.</span></span>
-   <span data-ttu-id="7b867-181">O tratamento de erros é misturado com outras instruções de ramificação e looping.</span><span class="sxs-lookup"><span data-stu-id="7b867-181">Error handling is mixed in with other branching and looping statements.</span></span> <span data-ttu-id="7b867-182">Isso pode tornar a lógica geral do programa mais difícil de seguir.</span><span class="sxs-lookup"><span data-stu-id="7b867-182">This can make the overall program logic harder to follow.</span></span>

### <a name="cascading-ifs"></a><span data-ttu-id="7b867-183">IFS em cascata</span><span class="sxs-lookup"><span data-stu-id="7b867-183">Cascading ifs</span></span>

<span data-ttu-id="7b867-184">Depois de cada chamada de método, use uma instrução **If** para testar o sucesso.</span><span class="sxs-lookup"><span data-stu-id="7b867-184">After each method call, use an **if** statement to test for success.</span></span> <span data-ttu-id="7b867-185">Se o método tiver sucesso, coloque a próxima chamada de método dentro do bloco **If** .</span><span class="sxs-lookup"><span data-stu-id="7b867-185">If the method succeeds, place the next method call inside the **if** block.</span></span> <span data-ttu-id="7b867-186">Mas em vez de aninhar instruções **If** adicionais, coloque cada teste subsequente com [**êxito**](/windows/desktop/api/winerror/nf-winerror-succeeded) após o bloco **If** anterior.</span><span class="sxs-lookup"><span data-stu-id="7b867-186">But instead of nesting further **if** statements, place each subsequent [**SUCCEEDED**](/windows/desktop/api/winerror/nf-winerror-succeeded) test after the previous **if** block.</span></span> <span data-ttu-id="7b867-187">Se qualquer método falhar, todos os testes restantes com **êxito** simplesmente falharão até que a parte inferior da função seja atingida.</span><span class="sxs-lookup"><span data-stu-id="7b867-187">If any method fails, all the remaining **SUCCEEDED** tests simply fail until the bottom of the function is reached.</span></span>


```C++
HRESULT ShowDialog()
{
    IFileOpenDialog *pFileOpen = NULL;
    IShellItem *pItem = NULL;

    HRESULT hr = CoCreateInstance(__uuidof(FileOpenDialog), NULL, 
        CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pFileOpen));

    if (SUCCEEDED(hr))
    {
        hr = pFileOpen->Show(NULL);
    }
    if (SUCCEEDED(hr))
    {
        hr = pFileOpen->GetResult(&pItem);
    }
    if (SUCCEEDED(hr))
    {
        // Use pItem (not shown).
    }

    // Clean up.
    SafeRelease(&pItem);
    SafeRelease(&pFileOpen);
    return hr;
}
```



<span data-ttu-id="7b867-188">Nesse padrão, você libera recursos no final da função.</span><span class="sxs-lookup"><span data-stu-id="7b867-188">In this pattern, you release resources at the very end of the function.</span></span> <span data-ttu-id="7b867-189">Se ocorrer um erro, alguns ponteiros poderão ser inválidos quando a função for encerrada.</span><span class="sxs-lookup"><span data-stu-id="7b867-189">If an error occurs, some pointers might be invalid when the function exits.</span></span> <span data-ttu-id="7b867-190">Chamar a [**versão**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) em um ponteiro inválido falhará no programa (ou pior), portanto, você deve inicializar todos os ponteiros para **NULL** e verificar se eles são **nulos** antes de liberá-los.</span><span class="sxs-lookup"><span data-stu-id="7b867-190">Calling [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on an invalid pointer will crash the program (or worse), so you must initialize all pointers to **NULL** and check whether they are **NULL** before releasing them.</span></span> <span data-ttu-id="7b867-191">Este exemplo usa a `SafeRelease` função; os ponteiros inteligentes também são uma boa opção.</span><span class="sxs-lookup"><span data-stu-id="7b867-191">This example uses the `SafeRelease` function; smart pointers are also a good choice.</span></span>

<span data-ttu-id="7b867-192">Se você usar esse padrão, deverá ter cuidado com construções de loop.</span><span class="sxs-lookup"><span data-stu-id="7b867-192">If you use this pattern, you must be careful with loop constructs.</span></span> <span data-ttu-id="7b867-193">Dentro de um loop, interrompa o loop se qualquer chamada falhar.</span><span class="sxs-lookup"><span data-stu-id="7b867-193">Inside a loop, break from the loop if any call fails.</span></span>

<span data-ttu-id="7b867-194">Vantagens</span><span class="sxs-lookup"><span data-stu-id="7b867-194">Advantages</span></span>

-   <span data-ttu-id="7b867-195">Esse padrão cria menos aninhamento do que o padrão "IFS aninhado".</span><span class="sxs-lookup"><span data-stu-id="7b867-195">This pattern creates less nesting than the "nested ifs" pattern.</span></span>
-   <span data-ttu-id="7b867-196">O fluxo de controle geral é mais fácil de ver.</span><span class="sxs-lookup"><span data-stu-id="7b867-196">Overall control flow is easier to see.</span></span>
-   <span data-ttu-id="7b867-197">Os recursos são liberados em um ponto no código.</span><span class="sxs-lookup"><span data-stu-id="7b867-197">Resources are released at one point in the code.</span></span>

<span data-ttu-id="7b867-198">Desvantagens</span><span class="sxs-lookup"><span data-stu-id="7b867-198">Disadvantages</span></span>

-   <span data-ttu-id="7b867-199">Todas as variáveis devem ser declaradas e inicializadas na parte superior da função.</span><span class="sxs-lookup"><span data-stu-id="7b867-199">All variables must be declared and initialized at the top of the function.</span></span>
-   <span data-ttu-id="7b867-200">Se uma chamada falhar, a função fará várias verificações de erro desnecessárias, em vez de sair da função imediatamente.</span><span class="sxs-lookup"><span data-stu-id="7b867-200">If a call fails, the function makes multiple unneeded error checks, instead of exiting the function immediately.</span></span>
-   <span data-ttu-id="7b867-201">Como o fluxo de controle continua pela função após uma falha, você deve ter cuidado ao longo do corpo da função para não acessar recursos inválidos.</span><span class="sxs-lookup"><span data-stu-id="7b867-201">Because the flow of control continues through the function after a failure, you must be careful throughout the body of the function not to access invalid resources.</span></span>
-   <span data-ttu-id="7b867-202">Os erros dentro de um loop exigem um caso especial.</span><span class="sxs-lookup"><span data-stu-id="7b867-202">Errors inside a loop require a special case.</span></span>

### <a name="jump-on-fail"></a><span data-ttu-id="7b867-203">Falha ao saltar</span><span class="sxs-lookup"><span data-stu-id="7b867-203">Jump on Fail</span></span>

<span data-ttu-id="7b867-204">Após cada chamada de método, teste a falha (não êxito).</span><span class="sxs-lookup"><span data-stu-id="7b867-204">After each method call, test for failure (not success).</span></span> <span data-ttu-id="7b867-205">Em caso de falha, salte para um rótulo próximo à parte inferior da função.</span><span class="sxs-lookup"><span data-stu-id="7b867-205">On failure, jump to a label near the bottom of the function.</span></span> <span data-ttu-id="7b867-206">Após o rótulo, mas antes de sair da função, libere os recursos.</span><span class="sxs-lookup"><span data-stu-id="7b867-206">After the label, but before exiting the function, release resources.</span></span>


```C++
HRESULT ShowDialog()
{
    IFileOpenDialog *pFileOpen = NULL;
    IShellItem *pItem = NULL;

    HRESULT hr = CoCreateInstance(__uuidof(FileOpenDialog), NULL, 
        CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pFileOpen));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pFileOpen->Show(NULL);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pFileOpen->GetResult(&pItem);
    if (FAILED(hr))
    {
        goto done;
    }

    // Use pItem (not shown).

done:
    // Clean up.
    SafeRelease(&pItem);
    SafeRelease(&pFileOpen);
    return hr;
}
```



<span data-ttu-id="7b867-207">Vantagens</span><span class="sxs-lookup"><span data-stu-id="7b867-207">Advantages</span></span>

-   <span data-ttu-id="7b867-208">O fluxo de controle geral é fácil de ver.</span><span class="sxs-lookup"><span data-stu-id="7b867-208">The overall control flow is easy to see.</span></span>
-   <span data-ttu-id="7b867-209">Em todos os pontos do código após uma verificação [**com falha**](/windows/desktop/api/winerror/nf-winerror-failed) , se você não tiver passado para o rótulo, será garantido que todas as chamadas anteriores tenham sido bem-sucedidas.</span><span class="sxs-lookup"><span data-stu-id="7b867-209">At every point in the code after a [**FAILED**](/windows/desktop/api/winerror/nf-winerror-failed) check, if you have not jumped to the label, it is guaranteed that all the previous calls have succeeded.</span></span>
-   <span data-ttu-id="7b867-210">Os recursos são lançados em um único lugar no código.</span><span class="sxs-lookup"><span data-stu-id="7b867-210">Resources are released at one place in the code.</span></span>

<span data-ttu-id="7b867-211">Desvantagens</span><span class="sxs-lookup"><span data-stu-id="7b867-211">Disadvantages</span></span>

-   <span data-ttu-id="7b867-212">Todas as variáveis devem ser declaradas e inicializadas na parte superior da função.</span><span class="sxs-lookup"><span data-stu-id="7b867-212">All variables must be declared and initialized at the top of the function.</span></span>
-   <span data-ttu-id="7b867-213">Alguns programadores não gostam de usar **goto** em seu código.</span><span class="sxs-lookup"><span data-stu-id="7b867-213">Some programmers do not like to use **goto** in their code.</span></span> <span data-ttu-id="7b867-214">(No entanto, deve-se observar que esse uso de **goto** é altamente estruturado; o código nunca salta para fora da chamada de função atual.)</span><span class="sxs-lookup"><span data-stu-id="7b867-214">(However, it should be noted that this use of **goto** is highly structured; the code never jumps outside the current function call.)</span></span>
-   <span data-ttu-id="7b867-215">as instruções **goto** ignoram inicializadores.</span><span class="sxs-lookup"><span data-stu-id="7b867-215">**goto** statements skip initializers.</span></span>

### <a name="throw-on-fail"></a><span data-ttu-id="7b867-216">Lançar em caso de falha</span><span class="sxs-lookup"><span data-stu-id="7b867-216">Throw on Fail</span></span>

<span data-ttu-id="7b867-217">Em vez de saltar para um rótulo, você pode gerar uma exceção quando um método falhar.</span><span class="sxs-lookup"><span data-stu-id="7b867-217">Rather than jump to a label, you can throw an exception when a method fails.</span></span> <span data-ttu-id="7b867-218">Isso pode produzir um estilo mais idiomática de C++ se você estiver acostumado a escrever código de exceção segura.</span><span class="sxs-lookup"><span data-stu-id="7b867-218">This can produce a more idiomatic style of C++ if you are used to writing exception-safe code.</span></span>


```C++
#include <comdef.h>  // Declares _com_error

inline void throw_if_fail(HRESULT hr)
{
    if (FAILED(hr))
    {
        throw _com_error(hr);
    }
}

void ShowDialog()
{
    try
    {
        CComPtr<IFileOpenDialog> pFileOpen;
        throw_if_fail(CoCreateInstance(__uuidof(FileOpenDialog), NULL, 
            CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pFileOpen)));

        throw_if_fail(pFileOpen->Show(NULL));

        CComPtr<IShellItem> pItem;
        throw_if_fail(pFileOpen->GetResult(&pItem));

        // Use pItem (not shown).
    }
    catch (_com_error err)
    {
        // Handle error.
    }
}
```



<span data-ttu-id="7b867-219">Observe que este exemplo usa a classe **CComPtr** para gerenciar ponteiros de interface.</span><span class="sxs-lookup"><span data-stu-id="7b867-219">Notice that this example uses the **CComPtr** class to manage interface pointers.</span></span> <span data-ttu-id="7b867-220">Em geral, se o seu código lançar exceções, você deverá seguir o padrão RAII (aquisição de recurso é inicialização).</span><span class="sxs-lookup"><span data-stu-id="7b867-220">Generally, if your code throws exceptions, you should follow the RAII (Resource Acquisition is Initialization) pattern.</span></span> <span data-ttu-id="7b867-221">Ou seja, cada recurso deve ser gerenciado por um objeto cujo destruidor garante que o recurso seja liberado corretamente.</span><span class="sxs-lookup"><span data-stu-id="7b867-221">That is, every resource should be managed by an object whose destructor guarantees that the resource is correctly released.</span></span> <span data-ttu-id="7b867-222">Se uma exceção for lançada, a garantia do destruidor será invocada.</span><span class="sxs-lookup"><span data-stu-id="7b867-222">If an exception is thrown, the destructor is guaranteed to be invoked.</span></span> <span data-ttu-id="7b867-223">Caso contrário, seu programa poderá vazar recursos.</span><span class="sxs-lookup"><span data-stu-id="7b867-223">Otherwise, your program might leak resources.</span></span>

<span data-ttu-id="7b867-224">Vantagens</span><span class="sxs-lookup"><span data-stu-id="7b867-224">Advantages</span></span>

-   <span data-ttu-id="7b867-225">Compatível com o código existente que usa manipulação de exceção.</span><span class="sxs-lookup"><span data-stu-id="7b867-225">Compatible with existing code that uses exception handling.</span></span>
-   <span data-ttu-id="7b867-226">Compatível com bibliotecas C++ que geram exceções, como a STL (Standard Template Library).</span><span class="sxs-lookup"><span data-stu-id="7b867-226">Compatible with C++ libraries that throw exceptions, such as the Standard Template Library (STL).</span></span>

<span data-ttu-id="7b867-227">Desvantagens</span><span class="sxs-lookup"><span data-stu-id="7b867-227">Disadvantages</span></span>

-   <span data-ttu-id="7b867-228">Requer objetos C++ para gerenciar recursos como memória ou identificadores de arquivo.</span><span class="sxs-lookup"><span data-stu-id="7b867-228">Requires C++ objects to manage resources such as memory or file handles.</span></span>
-   <span data-ttu-id="7b867-229">Requer uma boa compreensão de como escrever código de exceção segura.</span><span class="sxs-lookup"><span data-stu-id="7b867-229">Requires a good understanding of how to write exception-safe code.</span></span>

## <a name="next"></a><span data-ttu-id="7b867-230">Avançar</span><span class="sxs-lookup"><span data-stu-id="7b867-230">Next</span></span>

[<span data-ttu-id="7b867-231">Módulo 3. Gráficos do Windows</span><span class="sxs-lookup"><span data-stu-id="7b867-231">Module 3. Windows Graphics</span></span>](module-3---windows-graphics.md)

 

 
