---
title: Políticas de tratamento de erros Direct2D
description: 'Este tópico descreve as políticas de tratamento de erros do Direct2D. Ele contém as seguintes seções:'
ms.assetid: b5fa327a-a315-46fa-aa78-8a5733faae01
keywords:
- Direct2D, tratamento de erro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fc930e7ee9e5b73b5f676103f45ffe25e4d4e61
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917588"
---
# <a name="direct2d-error-handling-policies"></a><span data-ttu-id="73350-105">Políticas de tratamento de erros Direct2D</span><span class="sxs-lookup"><span data-stu-id="73350-105">Direct2D Error Handling Policies</span></span>

<span data-ttu-id="73350-106">Este tópico descreve as políticas de tratamento de erros do Direct2D.</span><span class="sxs-lookup"><span data-stu-id="73350-106">This topic describes the Direct2D error handling policies.</span></span> <span data-ttu-id="73350-107">Ele contém as seguintes seções:</span><span class="sxs-lookup"><span data-stu-id="73350-107">It contains the following sections.</span></span>

-   [<span data-ttu-id="73350-108">Uso de HRESULT</span><span class="sxs-lookup"><span data-stu-id="73350-108">Use of HRESULT</span></span>](#use-of-hresult)
-   [<span data-ttu-id="73350-109">Valor de retorno das funções em lote</span><span class="sxs-lookup"><span data-stu-id="73350-109">Return Value of Batched Functions</span></span>](#return-value-of-batched-functions)
-   [<span data-ttu-id="73350-110">Entrada inválida</span><span class="sxs-lookup"><span data-stu-id="73350-110">Invalid Input</span></span>](#invalid-input)
    -   [<span data-ttu-id="73350-111">Ponteiro de saída</span><span class="sxs-lookup"><span data-stu-id="73350-111">Output Pointer</span></span>](#output-pointer)
    -   [<span data-ttu-id="73350-112">Parâmetro obrigatório</span><span class="sxs-lookup"><span data-stu-id="73350-112">Required Parameter</span></span>](#required-parameter)
-   [<span data-ttu-id="73350-113">Os RECTs de entrada NaN e inadequadamente ordenados</span><span class="sxs-lookup"><span data-stu-id="73350-113">NaN and Poorly Ordered Input RECTs</span></span>](#nan-and-poorly-ordered-input-rects)
    -   [<span data-ttu-id="73350-114">NaN como entrada</span><span class="sxs-lookup"><span data-stu-id="73350-114">NaN as Input</span></span>](#nan-as-input)
    -   [<span data-ttu-id="73350-115">Esretângulos de entrada ordenados incorretamente</span><span class="sxs-lookup"><span data-stu-id="73350-115">Poorly Ordered Input RECTs</span></span>](#poorly-ordered-input-rects)

## <a name="use-of-hresult"></a><span data-ttu-id="73350-116">Uso de HRESULT</span><span class="sxs-lookup"><span data-stu-id="73350-116">Use of HRESULT</span></span>

<span data-ttu-id="73350-117">Se uma função não estiver em lote e puder ter uma falha de tempo de execução, ela deverá retornar **HRESULT** para indicar uma falha.</span><span class="sxs-lookup"><span data-stu-id="73350-117">If a function is not batched and can have a run-time failure, it should return **HRESULT** to indicate a failure.</span></span> <span data-ttu-id="73350-118">Uma falha de tempo de execução é qualquer falha que não pode ser evitada em tempo de design, como memória insuficiente.</span><span class="sxs-lookup"><span data-stu-id="73350-118">A run-time failure is any failure that cannot be avoided at design time, such as out of memory.</span></span>

## <a name="return-value-of-batched-functions"></a><span data-ttu-id="73350-119">Valor de retorno das funções em lote</span><span class="sxs-lookup"><span data-stu-id="73350-119">Return Value of Batched Functions</span></span>

<span data-ttu-id="73350-120">Funções em lote em Direct2D são as funções que são processadas como uma única unidade quando [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) ou [**Close**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-close) é chamado.</span><span class="sxs-lookup"><span data-stu-id="73350-120">Batched functions in Direct2D are the functions that are processed as a single unit when [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) or [**Close**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-close) is called.</span></span> <span data-ttu-id="73350-121">Eles são os comandos de desenho entre [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) e **EndDraw** ou comandos em [**GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink).</span><span class="sxs-lookup"><span data-stu-id="73350-121">They are the drawing commands between [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) and **EndDraw** or commands on [**GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink).</span></span> <span data-ttu-id="73350-122">Para essas funções, os erros são relatados no momento em que o lote é concluído.</span><span class="sxs-lookup"><span data-stu-id="73350-122">For these functions, errors are reported at the time the batch is completed.</span></span> <span data-ttu-id="73350-123">O erro é retornado após **EndDraw** para comandos de desenho e, após **fechar** , para **GeometrySink**.</span><span class="sxs-lookup"><span data-stu-id="73350-123">The error is returned after **EndDraw** for drawing commands, and after **Close** for **GeometrySink**.</span></span>

<span data-ttu-id="73350-124">RenderTargets interromperá o desenho se um estado de erro for definido, mas um aplicativo puder chamar [**flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) para redefinir o estado de erro e retomar o desenho.</span><span class="sxs-lookup"><span data-stu-id="73350-124">RenderTargets stop drawing if an error state is set, but an application can call [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) to reset the error state and resume drawing.</span></span>

<span data-ttu-id="73350-125">As funções **Get** e **set** não têm valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="73350-125">**Get** and **Set** functions have no return value.</span></span> <span data-ttu-id="73350-126">No entanto, se uma função **set** tiver uma entrada inválida, a camada de depuração gerará uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="73350-126">However, if a **Set** function has an invalid input, the debug layer generates a message.</span></span> <span data-ttu-id="73350-127">Nesse caso, nenhum estado de erro é definido e a função **set** não faz nada.</span><span class="sxs-lookup"><span data-stu-id="73350-127">In this case, no error state is set and the **Set** function does nothing.</span></span>

## <a name="invalid-input"></a><span data-ttu-id="73350-128">Entrada inválida</span><span class="sxs-lookup"><span data-stu-id="73350-128">Invalid Input</span></span>

<span data-ttu-id="73350-129">Direct2D faz referência a ponteiros de saída e parâmetros obrigatórios que resultam em violações de acesso quando os ponteiros são inválidos ou **nulos**.</span><span class="sxs-lookup"><span data-stu-id="73350-129">Direct2D dereferences output pointers and required parameters which result in access violations when the pointers are invalid or **NULL**.</span></span>

### <a name="output-pointer"></a><span data-ttu-id="73350-130">Ponteiro de saída</span><span class="sxs-lookup"><span data-stu-id="73350-130">Output Pointer</span></span>

<span data-ttu-id="73350-131">Direct2D desreferencia um ponteiro de saída e o atribui a **NULL** imediatamente ao inserir a função.</span><span class="sxs-lookup"><span data-stu-id="73350-131">Direct2D dereferences an output pointer and assigns it to **NULL** immediately upon entering the function.</span></span> <span data-ttu-id="73350-132">Isso causará uma violação de acesso se um chamador passar em **NULL** como o ponteiro para o valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="73350-132">This causes an access violation if a caller passes in **NULL** as the pointer to the return value.</span></span> <span data-ttu-id="73350-133">Essa política também se aplica a matrizes de ponteiros.</span><span class="sxs-lookup"><span data-stu-id="73350-133">This policy also applies to arrays of pointers.</span></span> <span data-ttu-id="73350-134">Para outros parâmetros de saída, como uma struct, a desreferência acontece mais tarde e também resulta em uma violação de acesso.</span><span class="sxs-lookup"><span data-stu-id="73350-134">For other output parameters, such as a struct, the dereference happens later and also results in an access violation.</span></span> <span data-ttu-id="73350-135">No entanto, há alguns métodos que têm ponteiros de saída opcionais (isto é, [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw), [**flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush)) que não causarão uma violação de acesso.</span><span class="sxs-lookup"><span data-stu-id="73350-135">However, there are some methods that have optional output pointers (that is, [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw), [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush)) that will not cause an access violation.</span></span>

### <a name="required-parameter"></a><span data-ttu-id="73350-136">Parâmetro obrigatório</span><span class="sxs-lookup"><span data-stu-id="73350-136">Required Parameter</span></span>

<span data-ttu-id="73350-137">Se **NULL** for passado para qualquer função que exija um valor válido, a função desreferenciará o ponteiro insatisfatório no início, resultando em uma violação de acesso.</span><span class="sxs-lookup"><span data-stu-id="73350-137">If **NULL** is passed to any function requiring a valid value, the function dereferences the bad pointer early resulting in an access violation.</span></span> <span data-ttu-id="73350-138">Para parâmetros de entrada opcionais, **NULL** é um valor válido que resulta em algum padrão razoável.</span><span class="sxs-lookup"><span data-stu-id="73350-138">For optional input parameters, **NULL** is a valid value that results in some reasonable default.</span></span>

## <a name="nan-and-poorly-ordered-input-rects"></a><span data-ttu-id="73350-139">Os RECTs de entrada NaN e inadequadamente ordenados</span><span class="sxs-lookup"><span data-stu-id="73350-139">NaN and Poorly Ordered Input RECTs</span></span>

<span data-ttu-id="73350-140">Em Direct2D, NaN é considerada uma entrada válida e os RETÂNGULOs de entrada ordenados inadequadamente são classificados.</span><span class="sxs-lookup"><span data-stu-id="73350-140">In Direct2D, NaN is considered a valid input and poorly ordered input RECTs are sorted.</span></span>

### <a name="nan-as-input"></a><span data-ttu-id="73350-141">NaN como entrada</span><span class="sxs-lookup"><span data-stu-id="73350-141">NaN as Input</span></span>

<span data-ttu-id="73350-142">NaN é considerado uma entrada válida, embora normalmente resulte na primitiva que contém o NaN não Drawing.</span><span class="sxs-lookup"><span data-stu-id="73350-142">NaN is considered a valid input, though it typically results in the primitive that contains the NaN not drawing.</span></span> <span data-ttu-id="73350-143">A API Direct2D não fornece filtragem explícita de NaN para validar a entrada.</span><span class="sxs-lookup"><span data-stu-id="73350-143">The Direct2D API does not provide explicit filtering of NaN to validate input.</span></span>

### <a name="poorly-ordered-input-rects"></a><span data-ttu-id="73350-144">Esretângulos de entrada ordenados incorretamente</span><span class="sxs-lookup"><span data-stu-id="73350-144">Poorly Ordered Input RECTs</span></span>

<span data-ttu-id="73350-145">Os RETÂNGULOs de entrada ordenados incorretamente são classificados de forma que os cantos superior, esquerdo e inferior sejam corretamente especificados.</span><span class="sxs-lookup"><span data-stu-id="73350-145">Poorly ordered input RECTs are sorted so that the top, left and bottom, right corners are correctly specified.</span></span> <span data-ttu-id="73350-146">Para saída, retângulos vazios têm a seguinte aparência: {Infinity, Infinity, FloatMax, FloatMax}.</span><span class="sxs-lookup"><span data-stu-id="73350-146">For output, empty rectangles look like this: {Infinity, Infinity, FloatMax, FloatMax}.</span></span>

 

 