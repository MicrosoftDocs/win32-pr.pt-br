---
title: Regras para usar ponteiros
description: Portar seu código para compilar para o Microsoft Windows de 32 e 64 bits é simples. Você só precisa seguir algumas regras simples sobre ponteiros de conversão e usar os novos tipos de dados em seu código. As regras para manipulação de ponteiros são as seguintes.
ms.assetid: 4c38bee2-fa1c-493f-a12d-e673df4d4895
keywords:
- regras para usar ponteiros de programação do Windows de 64 bits
- manipulação de ponteiros programação do Windows de 64 bits
- ponteiros de conversão de programação de 64 bits do Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 318ff5beed6dc90bd49b6b293131e17db6f92f6b
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/08/2020
ms.locfileid: "103917748"
---
# <a name="rules-for-using-pointers"></a><span data-ttu-id="1e498-108">Regras para usar ponteiros</span><span class="sxs-lookup"><span data-stu-id="1e498-108">Rules for Using Pointers</span></span>

<span data-ttu-id="1e498-109">Portar seu código para compilar para o Microsoft Windows de 32 e 64 bits é simples.</span><span class="sxs-lookup"><span data-stu-id="1e498-109">Porting your code to compile for both 32- and 64-bit Microsoft Windows is straightforward.</span></span> <span data-ttu-id="1e498-110">Você só precisa seguir algumas regras simples sobre ponteiros de conversão e usar os novos tipos de dados em seu código.</span><span class="sxs-lookup"><span data-stu-id="1e498-110">You need only follow a few simple rules about casting pointers, and use the new data types in your code.</span></span> <span data-ttu-id="1e498-111">As regras para manipulação de ponteiros são as seguintes.</span><span class="sxs-lookup"><span data-stu-id="1e498-111">The rules for pointer manipulation are as follows.</span></span>

1.  <span data-ttu-id="1e498-112">Não converta ponteiros para **int**, **Long**, **ULONG** ou **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="1e498-112">Do not cast pointers to **int**, **long**, **ULONG**, or **DWORD**.</span></span>

    <span data-ttu-id="1e498-113">Se você precisar converter um ponteiro para testar alguns bits, definir ou limpar bits, ou então manipular seu conteúdo, use o tipo de PTR **\_ PTR** ou **int \_** .</span><span class="sxs-lookup"><span data-stu-id="1e498-113">If you must cast a pointer to test some bits, set or clear bits, or otherwise manipulate its contents, use the **UINT\_PTR** or **INT\_PTR** type.</span></span> <span data-ttu-id="1e498-114">Esses tipos são tipos integrais que são dimensionados para o tamanho de um ponteiro para o Windows de 32 e 64 bits (por exemplo, **ULONG** para windows de 32 bits e \_ Int64 para o Windows de 64 bits).</span><span class="sxs-lookup"><span data-stu-id="1e498-114">These types are integral types that scale to the size of a pointer for both 32- and 64-bit Windows (for example, **ULONG** for 32-bit Windows and \_int64 for 64-bit Windows).</span></span> <span data-ttu-id="1e498-115">Por exemplo, suponha que você esteja portando o código a seguir:</span><span class="sxs-lookup"><span data-stu-id="1e498-115">For example, assume you are porting the following code:</span></span>

    `ImageBase = (PVOID)((ULONG)ImageBase | 1);`

    <span data-ttu-id="1e498-116">Como parte do processo de portabilidade, você alteraria o código da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="1e498-116">As a part of the porting process, you would change the code as follows:</span></span>

    `ImageBase = (PVOID)((ULONG_PTR)ImageBase | 1);`

    <span data-ttu-id="1e498-117">Use o modo **uint \_** e o **int \_ PTR** quando apropriado (e se você não tiver certeza se eles são obrigatórios, não há nenhum dano em usá-los apenas no caso).</span><span class="sxs-lookup"><span data-stu-id="1e498-117">Use **UINT\_PTR** and **INT\_PTR** where appropriate (and if you are uncertain whether they are required, there is no harm in using them just in case).</span></span> <span data-ttu-id="1e498-118">Não Converta seus ponteiros para os tipos **ULONG**, **Long**, **int**, **uint** ou **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="1e498-118">Do not cast your pointers to the types **ULONG**, **LONG**, **INT**, **UINT**, or **DWORD**.</span></span>

    <span data-ttu-id="1e498-119">Observe que o **identificador** é definido como **void \***, portanto, typecasting um valor de **identificador** para um valor **ULONG** para testar, definir ou limpar os 2 bits de ordem inferior é um erro no Windows de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="1e498-119">Note that **HANDLE** is defined as a **void\***, so typecasting a **HANDLE** value to a **ULONG** value to test, set, or clear the low-order 2 bits is an error on 64-bit Windows.</span></span>

2.  <span data-ttu-id="1e498-120">Use a função **PtrToLong** ou **PtrToUlong** para truncar ponteiros.</span><span class="sxs-lookup"><span data-stu-id="1e498-120">Use the **PtrToLong** or **PtrToUlong** function to truncate pointers.</span></span>

    <span data-ttu-id="1e498-121">Se você precisar truncar um ponteiro para um valor de 32 bits, use a função **PtrToLong** ou **PtrToUlong** (definida em Basetsd. h).</span><span class="sxs-lookup"><span data-stu-id="1e498-121">If you must truncate a pointer to a 32-bit value, use the **PtrToLong** or **PtrToUlong** function (defined in Basetsd.h).</span></span> <span data-ttu-id="1e498-122">Essas funções desabilitam o aviso de truncamento do ponteiro para a duração da chamada.</span><span class="sxs-lookup"><span data-stu-id="1e498-122">These functions disable the pointer truncation warning for the duration of the call.</span></span>

    <span data-ttu-id="1e498-123">Use essas funções com cuidado.</span><span class="sxs-lookup"><span data-stu-id="1e498-123">Use these functions carefully.</span></span> <span data-ttu-id="1e498-124">Depois de converter uma variável de ponteiro usando uma dessas funções, nunca a use como um ponteiro novamente.</span><span class="sxs-lookup"><span data-stu-id="1e498-124">After you convert a pointer variable using one of these functions, never use it as a pointer again.</span></span> <span data-ttu-id="1e498-125">Essas funções truncam os 32 bits superiores de um endereço, que geralmente são necessários para acessar a memória originalmente referenciada pelo ponteiro.</span><span class="sxs-lookup"><span data-stu-id="1e498-125">These functions truncate the upper 32 bits of an address, which are usually needed to access the memory originally referenced by pointer.</span></span> <span data-ttu-id="1e498-126">O uso dessas funções sem consideração cuidadosa resultará em um código frágil.</span><span class="sxs-lookup"><span data-stu-id="1e498-126">Using these functions without careful consideration will result in fragile code.</span></span>

3.  <span data-ttu-id="1e498-127">Tenha cuidado ao usar \_ valores de ponteiro 32 no código que pode ser compilado como código de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="1e498-127">Be careful when using POINTER\_32 values in code that may be compiled as 64-bit code.</span></span> <span data-ttu-id="1e498-128">O compilador assinará o ponteiro quando ele for atribuído a um ponteiro nativo no código de 64 bits, sem estender o ponteiro.</span><span class="sxs-lookup"><span data-stu-id="1e498-128">The compiler will sign-extend the pointer when it is assigned to a native pointer in 64-bit code, not zero-extend the pointer.</span></span>
4.  <span data-ttu-id="1e498-129">Tenha cuidado ao usar \_ valores de ponteiro 64 no código que pode ser compilado como código de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="1e498-129">Be careful when using POINTER\_64 values in code that may be compiled as 32-bit code.</span></span> <span data-ttu-id="1e498-130">O compilador assinará o ponteiro no código de 32 bits, sem estender o ponteiro.</span><span class="sxs-lookup"><span data-stu-id="1e498-130">The compiler will sign-extend the pointer in 32-bit code, not zero-extend the pointer.</span></span>
5.  <span data-ttu-id="1e498-131">Tenha cuidado ao usar parâmetros de saída.</span><span class="sxs-lookup"><span data-stu-id="1e498-131">Be careful using OUT parameters.</span></span>

    <span data-ttu-id="1e498-132">Por exemplo, suponha que você tenha uma função definida da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="1e498-132">For example, suppose you have a function defined as follows:</span></span>

    `void func( OUT PULONG *PointerToUlong );`

    <span data-ttu-id="1e498-133">Não chame essa função da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="1e498-133">Do not call this function as follows.</span></span>

    ``` syntax
    ULONG ul;
    PULONG lp;
    func((PULONG *)&ul);
    lp = (PULONG)ul;
    ```

    <span data-ttu-id="1e498-134">Em vez disso, use a chamada a seguir.</span><span class="sxs-lookup"><span data-stu-id="1e498-134">Instead, use the following call.</span></span>

    ``` syntax
    PULONG lp;
    func(&lp);
    ```

    <span data-ttu-id="1e498-135">Typecasting &UL para **Pulong \*** impede um erro de compilador, mas a função gravará um valor de ponteiro de 64 bits na memória em &UL.</span><span class="sxs-lookup"><span data-stu-id="1e498-135">Typecasting &ul to **PULONG\*** prevents a compiler error, but the function will write a 64-bit pointer value into the memory at &ul.</span></span> <span data-ttu-id="1e498-136">Esse código funciona em janelas de 32 bits, mas causará corrupção de dados em janelas de 64 bits e será uma corrupção sutil, difícil de encontrar.</span><span class="sxs-lookup"><span data-stu-id="1e498-136">This code works on 32-bit Windows, but will cause data corruption on 64-bit Windows and it will be subtle, hard-to-find corruption.</span></span> <span data-ttu-id="1e498-137">O resultado final: não jogue truques com o código C — simples e simples é melhor.</span><span class="sxs-lookup"><span data-stu-id="1e498-137">The bottom line: Do not play tricks with the C code—straightforward and simple is better.</span></span>

6.  <span data-ttu-id="1e498-138">Tenha cuidado com interfaces polimórficas.</span><span class="sxs-lookup"><span data-stu-id="1e498-138">Be careful with polymorphic interfaces.</span></span>

    <span data-ttu-id="1e498-139">Não crie funções que aceitem parâmetros **DWORD** para dados polimórficos.</span><span class="sxs-lookup"><span data-stu-id="1e498-139">Do not create functions that accept **DWORD** parameters for polymorphic data.</span></span> <span data-ttu-id="1e498-140">Se os dados puderem ser um ponteiro ou um valor integral, use o \_ tipo de **pVoid** /PTR uint.</span><span class="sxs-lookup"><span data-stu-id="1e498-140">If the data can be a pointer or an integral value, use the UINT\_PTR or **PVOID** type.</span></span>

    <span data-ttu-id="1e498-141">Por exemplo, não crie uma função que aceite uma matriz de parâmetros de exceção digitados como valores **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="1e498-141">For example, do not create a function that accepts an array of exception parameters typed as **DWORD** values.</span></span> <span data-ttu-id="1e498-142">A matriz deve ser uma matriz de valores de **\_ PTR DWORD** .</span><span class="sxs-lookup"><span data-stu-id="1e498-142">The array should be an array of **DWORD\_PTR** values.</span></span> <span data-ttu-id="1e498-143">Portanto, os elementos da matriz podem conter endereços ou valores integrais de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="1e498-143">Therefore, the array elements can hold addresses or 32-bit integral values.</span></span> <span data-ttu-id="1e498-144">(A regra geral é que se o tipo original é **DWORD** e precisa ser a largura do ponteiro, converta-o em um valor de **\_ PTR DWORD** .</span><span class="sxs-lookup"><span data-stu-id="1e498-144">(The general rule is that if the original type is **DWORD** and it needs to be pointer width, convert it to a **DWORD\_PTR** value.</span></span> <span data-ttu-id="1e498-145">É por isso que há tipos de precisão de ponteiro correspondentes.) Se você tiver um código que usa **DWORD**, **ULONG** ou outros tipos de 32 bits de uma maneira polimórfica (ou seja, você realmente deseja que o membro do parâmetro ou da estrutura mantenha um endereço), use **um \_ PTR** no lugar do tipo atual.</span><span class="sxs-lookup"><span data-stu-id="1e498-145">That is why there are corresponding pointer-precision types.) If you have code that uses **DWORD**, **ULONG**, or other 32-bit types in a polymorphic way (that is, you really want the parameter or structure member to hold an address), use **UINT\_PTR** in place of the current type.</span></span>

7.  <span data-ttu-id="1e498-146">Use as novas funções de classe de janela.</span><span class="sxs-lookup"><span data-stu-id="1e498-146">Use the new window class functions.</span></span>

    <span data-ttu-id="1e498-147">Se você tiver dados de janela ou de classe privada que contenham ponteiros, seu código precisará usar as seguintes novas funções:</span><span class="sxs-lookup"><span data-stu-id="1e498-147">If you have window or class private data that contains pointers, your code will need to use the following new functions:</span></span>

    -   [<span data-ttu-id="1e498-148">**GetClassLongPtr**</span><span class="sxs-lookup"><span data-stu-id="1e498-148">**GetClassLongPtr**</span></span>](/windows/win32/api/winuser/nf-winuser-getclasslongptra)
    -   [<span data-ttu-id="1e498-149">**GetWindowLongPtr**</span><span class="sxs-lookup"><span data-stu-id="1e498-149">**GetWindowLongPtr**</span></span>](/windows/win32/api/winuser/nf-winuser-getwindowlongptra)
    -   [<span data-ttu-id="1e498-150">**SetClassLongPtr**</span><span class="sxs-lookup"><span data-stu-id="1e498-150">**SetClassLongPtr**</span></span>](/windows/win32/api/winuser/nf-winuser-setclasslongptra)
    -   [<span data-ttu-id="1e498-151">**SetWindowLongPtr**</span><span class="sxs-lookup"><span data-stu-id="1e498-151">**SetWindowLongPtr**</span></span>](/windows/win32/api/winuser/nf-winuser-setwindowlongptra)

    <span data-ttu-id="1e498-152">Essas funções podem ser usadas em janelas de 32 e 64 bits, mas são necessárias no Windows de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="1e498-152">These functions can be used on both 32- and 64-bit Windows, but they are required on 64-bit Windows.</span></span> <span data-ttu-id="1e498-153">Prepare-se para a transição usando essas funções agora.</span><span class="sxs-lookup"><span data-stu-id="1e498-153">Prepare for the transition by using these functions now.</span></span>

    <span data-ttu-id="1e498-154">Além disso, você deve acessar ponteiros ou identificadores em dados privados de classe usando as novas funções no Windows de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="1e498-154">Additionally, you must access pointers or handles in class private data using the new functions on 64-bit Windows.</span></span> <span data-ttu-id="1e498-155">Para ajudá-lo a encontrar esses casos, os seguintes índices não são definidos em winuser. h durante uma compilação de 64 bits:</span><span class="sxs-lookup"><span data-stu-id="1e498-155">To aid you in finding these cases, the following indexes are not defined in Winuser.h during a 64-bit compile:</span></span>

    -   <span data-ttu-id="1e498-156">GWL \_ WndProc</span><span class="sxs-lookup"><span data-stu-id="1e498-156">GWL\_WNDPROC</span></span>
    -   <span data-ttu-id="1e498-157">GWL \_ HINSTANCE</span><span class="sxs-lookup"><span data-stu-id="1e498-157">GWL\_HINSTANCE</span></span>
    -   <span data-ttu-id="1e498-158">GWL \_ HWDPARENT</span><span class="sxs-lookup"><span data-stu-id="1e498-158">GWL\_HWDPARENT</span></span>
    -   <span data-ttu-id="1e498-159">GWL \_ UserData</span><span class="sxs-lookup"><span data-stu-id="1e498-159">GWL\_USERDATA</span></span>

    <span data-ttu-id="1e498-160">Em vez disso, a WinUser. h define os seguintes novos índices:</span><span class="sxs-lookup"><span data-stu-id="1e498-160">Instead, Winuser.h defines the following new indexes:</span></span>

    -   <span data-ttu-id="1e498-161">GWLP \_ WndProc</span><span class="sxs-lookup"><span data-stu-id="1e498-161">GWLP\_WNDPROC</span></span>
    -   <span data-ttu-id="1e498-162">GWLP \_ HINSTANCE</span><span class="sxs-lookup"><span data-stu-id="1e498-162">GWLP\_HINSTANCE</span></span>
    -   <span data-ttu-id="1e498-163">GWLP \_ HWNDPARENT</span><span class="sxs-lookup"><span data-stu-id="1e498-163">GWLP\_HWNDPARENT</span></span>
    -   <span data-ttu-id="1e498-164">GWLP \_ UserData</span><span class="sxs-lookup"><span data-stu-id="1e498-164">GWLP\_USERDATA</span></span>
    -   <span data-ttu-id="1e498-165">ID do GWLP \_</span><span class="sxs-lookup"><span data-stu-id="1e498-165">GWLP\_ID</span></span>

    <span data-ttu-id="1e498-166">Por exemplo, o código a seguir não compila:</span><span class="sxs-lookup"><span data-stu-id="1e498-166">For example, the following code does not compile:</span></span>

    `SetWindowLong(hWnd, GWL_WNDPROC, (LONG)MyWndProc);`

    <span data-ttu-id="1e498-167">Ele deve ser alterado da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="1e498-167">It should be changed as follows:</span></span>

    `SetWindowLongPtr(hWnd, GWLP_WNDPROC, (LONG_PTR)MyWndProc);`

    <span data-ttu-id="1e498-168">Ao definir o membro **cbWndExtra** da estrutura [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) , lembre-se de reservar espaço suficiente para ponteiros.</span><span class="sxs-lookup"><span data-stu-id="1e498-168">When setting the **cbWndExtra** member of the [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) structure, be sure to reserve enough space for pointers.</span></span> <span data-ttu-id="1e498-169">Por exemplo, se você estiver reservando, no momento, os bytes sizeof (DWORD) para um valor de ponteiro, Reserve bytes de sizeof (DWORD \_ PTR).</span><span class="sxs-lookup"><span data-stu-id="1e498-169">For example, if you are currently reserving sizeof(DWORD) bytes for a pointer value, reserve sizeof(DWORD\_PTR) bytes.</span></span>

8.  <span data-ttu-id="1e498-170">Acessar todos os dados de janela e de classe usando o **\_ deslocamento de campo**.</span><span class="sxs-lookup"><span data-stu-id="1e498-170">Access all window and class data using **FIELD\_OFFSET**.</span></span>

    <span data-ttu-id="1e498-171">É comum acessar os dados do Windows usando deslocamentos embutidos em código.</span><span class="sxs-lookup"><span data-stu-id="1e498-171">It is common to access window data using hard-coded offsets.</span></span> <span data-ttu-id="1e498-172">Essa técnica não é portátil para o Windows de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="1e498-172">This technique is not portable to 64-bit Windows.</span></span> <span data-ttu-id="1e498-173">Para tornar seu código portátil, acesse seus dados de janela e de classe usando a macro de **\_ deslocamento de campo** .</span><span class="sxs-lookup"><span data-stu-id="1e498-173">To make your code portable, access your window and class data using the **FIELD\_OFFSET** macro.</span></span> <span data-ttu-id="1e498-174">Não assuma que o segundo ponteiro tenha um deslocamento de 4.</span><span class="sxs-lookup"><span data-stu-id="1e498-174">Do not assume that the second pointer has an offset of 4.</span></span>

9.  <span data-ttu-id="1e498-175">Os tipos **lParam**, **wParam** e **LRESULT** mudam de tamanho com a plataforma.</span><span class="sxs-lookup"><span data-stu-id="1e498-175">The **LPARAM**, **WPARAM**, and **LRESULT** types change size with the platform.</span></span>

    <span data-ttu-id="1e498-176">Ao compilar o código de 64 bits, esses tipos se expandem para 64 bits, porque eles normalmente mantêm ponteiros ou tipos integrais.</span><span class="sxs-lookup"><span data-stu-id="1e498-176">When compiling 64-bit code, these types expand to 64 bits, because they typically hold pointers or integral types.</span></span> <span data-ttu-id="1e498-177">Não misture esses valores com valores **DWORD**, **ULONG**, **uint**, **int**, **int** ou **Long** .</span><span class="sxs-lookup"><span data-stu-id="1e498-177">Do not mix these values with **DWORD**, **ULONG**, **UINT**, **INT**, **int**, or **long** values.</span></span> <span data-ttu-id="1e498-178">Examine como você usa esses tipos e certifique-se de não truncar os valores inadvertidamente.</span><span class="sxs-lookup"><span data-stu-id="1e498-178">Examine how you use these types and ensure that you do not inadvertently truncate values.</span></span>

 

 