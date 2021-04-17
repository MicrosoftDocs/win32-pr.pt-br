---
description: Esta seção descreve o formato dos registros para cada um dos tokens de registro. As informações são divididas nas seções a seguir.
ms.assetid: 4fdd8339-f660-4389-878a-e7ab067d8508
title: Registros de token
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ae7e1dcdd36d538ed44205fa51b8e2094d1ff14
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105772705"
---
# <a name="token-records"></a><span data-ttu-id="458d4-104">Registros de token</span><span class="sxs-lookup"><span data-stu-id="458d4-104">Token Records</span></span>

<span data-ttu-id="458d4-105">Esta seção descreve o formato dos registros para cada um dos tokens de registro.</span><span class="sxs-lookup"><span data-stu-id="458d4-105">This section describes the format of the records for each of the record-bearing tokens.</span></span> <span data-ttu-id="458d4-106">As informações são divididas nas seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="458d4-106">Information is divided into the following sections.</span></span>

-   [<span data-ttu-id="458d4-107">nome do TOKEN \_</span><span class="sxs-lookup"><span data-stu-id="458d4-107">TOKEN\_NAME</span></span>](/windows)
-   [<span data-ttu-id="458d4-108">Cadeia de caracteres de TOKEN \_</span><span class="sxs-lookup"><span data-stu-id="458d4-108">TOKEN\_STRING</span></span>](/windows)
-   [<span data-ttu-id="458d4-109">inteiro de TOKEN \_</span><span class="sxs-lookup"><span data-stu-id="458d4-109">TOKEN\_INTEGER</span></span>](/windows)
-   [<span data-ttu-id="458d4-110">GUID do TOKEN \_</span><span class="sxs-lookup"><span data-stu-id="458d4-110">TOKEN\_GUID</span></span>](/windows)
-   [<span data-ttu-id="458d4-111">\_lista de inteiros de token \_</span><span class="sxs-lookup"><span data-stu-id="458d4-111">TOKEN\_INTEGER\_LIST</span></span>](/windows)
-   [<span data-ttu-id="458d4-112">\_lista de floats de token \_</span><span class="sxs-lookup"><span data-stu-id="458d4-112">TOKEN\_FLOAT\_LIST</span></span>](/windows)

## <a name="token_name"></a><span data-ttu-id="458d4-113">nome do TOKEN \_</span><span class="sxs-lookup"><span data-stu-id="458d4-113">TOKEN\_NAME</span></span>

<span data-ttu-id="458d4-114">Um registro de comprimento variável.</span><span class="sxs-lookup"><span data-stu-id="458d4-114">A variable-length record.</span></span> <span data-ttu-id="458d4-115">O token é seguido por um valor de contagem que especifica o número de bytes que se seguem no campo nome.</span><span class="sxs-lookup"><span data-stu-id="458d4-115">The token is followed by a count value that specifies the number of bytes that follow in the name field.</span></span> <span data-ttu-id="458d4-116">Um nome ASCII de contagem de comprimento conclui o registro.</span><span class="sxs-lookup"><span data-stu-id="458d4-116">An ASCII name of length count completes the record.</span></span>



| <span data-ttu-id="458d4-117">Campo</span><span class="sxs-lookup"><span data-stu-id="458d4-117">Field</span></span> | <span data-ttu-id="458d4-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="458d4-118">Type</span></span>       | <span data-ttu-id="458d4-119">Tamanho (bytes)</span><span class="sxs-lookup"><span data-stu-id="458d4-119">Size (bytes)</span></span> | <span data-ttu-id="458d4-120">Sumário</span><span class="sxs-lookup"><span data-stu-id="458d4-120">Contents</span></span>                       |
|-------|------------|--------------|--------------------------------|
| <span data-ttu-id="458d4-121">token</span><span class="sxs-lookup"><span data-stu-id="458d4-121">token</span></span> | <span data-ttu-id="458d4-122">WORD</span><span class="sxs-lookup"><span data-stu-id="458d4-122">WORD</span></span>       | <span data-ttu-id="458d4-123">2</span><span class="sxs-lookup"><span data-stu-id="458d4-123">2</span></span>            | <span data-ttu-id="458d4-124">nome do token \_</span><span class="sxs-lookup"><span data-stu-id="458d4-124">token\_name</span></span>                    |
| <span data-ttu-id="458d4-125">count</span><span class="sxs-lookup"><span data-stu-id="458d4-125">count</span></span> | <span data-ttu-id="458d4-126">DWORD</span><span class="sxs-lookup"><span data-stu-id="458d4-126">DWORD</span></span>      | <span data-ttu-id="458d4-127">4</span><span class="sxs-lookup"><span data-stu-id="458d4-127">4</span></span>            | <span data-ttu-id="458d4-128">Comprimento do campo de nome, em bytes</span><span class="sxs-lookup"><span data-stu-id="458d4-128">Length of name field, in bytes</span></span> |
| <span data-ttu-id="458d4-129">name</span><span class="sxs-lookup"><span data-stu-id="458d4-129">name</span></span>  | <span data-ttu-id="458d4-130">Matriz de bytes</span><span class="sxs-lookup"><span data-stu-id="458d4-130">BYTE array</span></span> | <span data-ttu-id="458d4-131">count</span><span class="sxs-lookup"><span data-stu-id="458d4-131">count</span></span>        | <span data-ttu-id="458d4-132">Nome ASCII</span><span class="sxs-lookup"><span data-stu-id="458d4-132">ASCII name</span></span>                     |



 

## <a name="token_string"></a><span data-ttu-id="458d4-133">Cadeia de caracteres de TOKEN \_</span><span class="sxs-lookup"><span data-stu-id="458d4-133">TOKEN\_STRING</span></span>

<span data-ttu-id="458d4-134">Um registro de comprimento variável.</span><span class="sxs-lookup"><span data-stu-id="458d4-134">A variable-length record.</span></span> <span data-ttu-id="458d4-135">O token é seguido por um valor de contagem que especifica o número de bytes que acompanham o campo de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="458d4-135">The token is followed by a count value that specifies the number of bytes that follow in the string field.</span></span> <span data-ttu-id="458d4-136">Uma cadeia de caracteres ASCII de contagem de comprimento continua o registro, que é concluído por um token de terminação.</span><span class="sxs-lookup"><span data-stu-id="458d4-136">An ASCII string of length count continues the record, which is completed by a terminating token.</span></span> <span data-ttu-id="458d4-137">A escolha do terminador é determinada pelos problemas de sintaxe discutidos em outro lugar.</span><span class="sxs-lookup"><span data-stu-id="458d4-137">The choice of terminator is determined by syntax issues discussed elsewhere.</span></span>



| <span data-ttu-id="458d4-138">Campo</span><span class="sxs-lookup"><span data-stu-id="458d4-138">Field</span></span>      | <span data-ttu-id="458d4-139">Tipo</span><span class="sxs-lookup"><span data-stu-id="458d4-139">Type</span></span>       | <span data-ttu-id="458d4-140">Tamanho (bytes)</span><span class="sxs-lookup"><span data-stu-id="458d4-140">Size (bytes)</span></span> | <span data-ttu-id="458d4-141">Sumário</span><span class="sxs-lookup"><span data-stu-id="458d4-141">Contents</span></span>                         |
|------------|------------|--------------|----------------------------------|
| <span data-ttu-id="458d4-142">token</span><span class="sxs-lookup"><span data-stu-id="458d4-142">token</span></span>      | <span data-ttu-id="458d4-143">WORD</span><span class="sxs-lookup"><span data-stu-id="458d4-143">WORD</span></span>       | <span data-ttu-id="458d4-144">2</span><span class="sxs-lookup"><span data-stu-id="458d4-144">2</span></span>            | <span data-ttu-id="458d4-145">Cadeia de caracteres de token \_</span><span class="sxs-lookup"><span data-stu-id="458d4-145">token\_string</span></span>                    |
| <span data-ttu-id="458d4-146">count</span><span class="sxs-lookup"><span data-stu-id="458d4-146">count</span></span>      | <span data-ttu-id="458d4-147">DWORD</span><span class="sxs-lookup"><span data-stu-id="458d4-147">DWORD</span></span>      | <span data-ttu-id="458d4-148">4</span><span class="sxs-lookup"><span data-stu-id="458d4-148">4</span></span>            | <span data-ttu-id="458d4-149">Comprimento do campo de cadeia de caracteres em bytes</span><span class="sxs-lookup"><span data-stu-id="458d4-149">Length of string field in bytes</span></span>  |
| <span data-ttu-id="458d4-150">Strings</span><span class="sxs-lookup"><span data-stu-id="458d4-150">strinG</span></span>     | <span data-ttu-id="458d4-151">Matriz de bytes</span><span class="sxs-lookup"><span data-stu-id="458d4-151">BYTE array</span></span> | <span data-ttu-id="458d4-152">count</span><span class="sxs-lookup"><span data-stu-id="458d4-152">count</span></span>        | <span data-ttu-id="458d4-153">Cadeia de caracteres ASCII</span><span class="sxs-lookup"><span data-stu-id="458d4-153">ASCII string</span></span>                     |
| <span data-ttu-id="458d4-154">encerra</span><span class="sxs-lookup"><span data-stu-id="458d4-154">terminator</span></span> | <span data-ttu-id="458d4-155">DWORD</span><span class="sxs-lookup"><span data-stu-id="458d4-155">DWORD</span></span>      | <span data-ttu-id="458d4-156">4</span><span class="sxs-lookup"><span data-stu-id="458d4-156">4</span></span>            | <span data-ttu-id="458d4-157">\_ponto e vírgula do \_ token</span><span class="sxs-lookup"><span data-stu-id="458d4-157">tOKEN\_SEMICOLON or TOKEN\_COMMA</span></span> |



 

## <a name="token_integer"></a><span data-ttu-id="458d4-158">inteiro de TOKEN \_</span><span class="sxs-lookup"><span data-stu-id="458d4-158">TOKEN\_INTEGER</span></span>

<span data-ttu-id="458d4-159">Um registro de comprimento fixo.</span><span class="sxs-lookup"><span data-stu-id="458d4-159">A fixed length record.</span></span> <span data-ttu-id="458d4-160">O token é seguido pelo valor inteiro necessário.</span><span class="sxs-lookup"><span data-stu-id="458d4-160">The token is followed by the integer value required.</span></span>



| <span data-ttu-id="458d4-161">Campo</span><span class="sxs-lookup"><span data-stu-id="458d4-161">Field</span></span> | <span data-ttu-id="458d4-162">Tipo</span><span class="sxs-lookup"><span data-stu-id="458d4-162">Type</span></span>  | <span data-ttu-id="458d4-163">Tamanho (bytes)</span><span class="sxs-lookup"><span data-stu-id="458d4-163">Size (bytes)</span></span> | <span data-ttu-id="458d4-164">Sumário</span><span class="sxs-lookup"><span data-stu-id="458d4-164">Contents</span></span>       |
|-------|-------|--------------|----------------|
| <span data-ttu-id="458d4-165">token</span><span class="sxs-lookup"><span data-stu-id="458d4-165">token</span></span> | <span data-ttu-id="458d4-166">WORD</span><span class="sxs-lookup"><span data-stu-id="458d4-166">WORD</span></span>  | <span data-ttu-id="458d4-167">2</span><span class="sxs-lookup"><span data-stu-id="458d4-167">2</span></span>            | <span data-ttu-id="458d4-168">inteiro de tOKEN \_</span><span class="sxs-lookup"><span data-stu-id="458d4-168">tOKEN\_INTEGER</span></span> |
| <span data-ttu-id="458d4-169">Valor</span><span class="sxs-lookup"><span data-stu-id="458d4-169">valuE</span></span> | <span data-ttu-id="458d4-170">DWORD</span><span class="sxs-lookup"><span data-stu-id="458d4-170">DWORD</span></span> | <span data-ttu-id="458d4-171">4</span><span class="sxs-lookup"><span data-stu-id="458d4-171">4</span></span>            | <span data-ttu-id="458d4-172">Inteiro único</span><span class="sxs-lookup"><span data-stu-id="458d4-172">Single integer</span></span> |



 

## <a name="token_guid"></a><span data-ttu-id="458d4-173">GUID do TOKEN \_</span><span class="sxs-lookup"><span data-stu-id="458d4-173">TOKEN\_GUID</span></span>

<span data-ttu-id="458d4-174">Um registro de comprimento fixo.</span><span class="sxs-lookup"><span data-stu-id="458d4-174">A fixed-length record.</span></span> <span data-ttu-id="458d4-175">O token é seguido pelos quatro campos de dados, conforme definido pelo padrão uso do DCE.</span><span class="sxs-lookup"><span data-stu-id="458d4-175">The token is followed by the four data fields as defined by the OSF DCE standard.</span></span>



| <span data-ttu-id="458d4-176">Campo</span><span class="sxs-lookup"><span data-stu-id="458d4-176">Field</span></span> | <span data-ttu-id="458d4-177">Tipo</span><span class="sxs-lookup"><span data-stu-id="458d4-177">Type</span></span>       | <span data-ttu-id="458d4-178">Tamanho (bytes)</span><span class="sxs-lookup"><span data-stu-id="458d4-178">Size (bytes)</span></span> | <span data-ttu-id="458d4-179">Sumário</span><span class="sxs-lookup"><span data-stu-id="458d4-179">Contents</span></span>          |
|-------|------------|--------------|-------------------|
| <span data-ttu-id="458d4-180">token</span><span class="sxs-lookup"><span data-stu-id="458d4-180">token</span></span> | <span data-ttu-id="458d4-181">WORD</span><span class="sxs-lookup"><span data-stu-id="458d4-181">WORD</span></span>       | <span data-ttu-id="458d4-182">2</span><span class="sxs-lookup"><span data-stu-id="458d4-182">2</span></span>            | <span data-ttu-id="458d4-183">GUID do tOKEN \_</span><span class="sxs-lookup"><span data-stu-id="458d4-183">tOKEN\_GUID</span></span>       |
| <span data-ttu-id="458d4-184">Data1</span><span class="sxs-lookup"><span data-stu-id="458d4-184">Data1</span></span> | <span data-ttu-id="458d4-185">DWORD</span><span class="sxs-lookup"><span data-stu-id="458d4-185">DWORD</span></span>      | <span data-ttu-id="458d4-186">4</span><span class="sxs-lookup"><span data-stu-id="458d4-186">4</span></span>            | <span data-ttu-id="458d4-187">Campo de dados UUID 1</span><span class="sxs-lookup"><span data-stu-id="458d4-187">UUID data field 1</span></span> |
| <span data-ttu-id="458d4-188">Data2</span><span class="sxs-lookup"><span data-stu-id="458d4-188">Data2</span></span> | <span data-ttu-id="458d4-189">WORD</span><span class="sxs-lookup"><span data-stu-id="458d4-189">WORD</span></span>       | <span data-ttu-id="458d4-190">2</span><span class="sxs-lookup"><span data-stu-id="458d4-190">2</span></span>            | <span data-ttu-id="458d4-191">Campo de dados UUID 2</span><span class="sxs-lookup"><span data-stu-id="458d4-191">UUID data field 2</span></span> |
| <span data-ttu-id="458d4-192">Data3</span><span class="sxs-lookup"><span data-stu-id="458d4-192">Data3</span></span> | <span data-ttu-id="458d4-193">WORD</span><span class="sxs-lookup"><span data-stu-id="458d4-193">WORD</span></span>       | <span data-ttu-id="458d4-194">2</span><span class="sxs-lookup"><span data-stu-id="458d4-194">2</span></span>            | <span data-ttu-id="458d4-195">Campo de dados UUID 3</span><span class="sxs-lookup"><span data-stu-id="458d4-195">UUID data field 3</span></span> |
| <span data-ttu-id="458d4-196">Data4</span><span class="sxs-lookup"><span data-stu-id="458d4-196">Data4</span></span> | <span data-ttu-id="458d4-197">Matriz de bytes</span><span class="sxs-lookup"><span data-stu-id="458d4-197">BYTE array</span></span> | <span data-ttu-id="458d4-198">8</span><span class="sxs-lookup"><span data-stu-id="458d4-198">8</span></span>            | <span data-ttu-id="458d4-199">Campo de dados UUID 4</span><span class="sxs-lookup"><span data-stu-id="458d4-199">UUID data field 4</span></span> |



 

## <a name="token_integer_list"></a><span data-ttu-id="458d4-200">\_lista de inteiros de token \_</span><span class="sxs-lookup"><span data-stu-id="458d4-200">TOKEN\_INTEGER\_LIST</span></span>

<span data-ttu-id="458d4-201">Um registro de comprimento variável.</span><span class="sxs-lookup"><span data-stu-id="458d4-201">A variable-length record.</span></span> <span data-ttu-id="458d4-202">O token é seguido por um valor de contagem que especifica o número de inteiros que se seguem no campo de lista.</span><span class="sxs-lookup"><span data-stu-id="458d4-202">The token is followed by a count value that specifies the number of integers that follow in the list field.</span></span> <span data-ttu-id="458d4-203">Para eficiência, listas de inteiros consecutivas devem ser compostas em uma única lista.</span><span class="sxs-lookup"><span data-stu-id="458d4-203">For efficiency, consecutive integer lists should be compounded into a single list.</span></span>



| <span data-ttu-id="458d4-204">Campo</span><span class="sxs-lookup"><span data-stu-id="458d4-204">Field</span></span> | <span data-ttu-id="458d4-205">Tipo</span><span class="sxs-lookup"><span data-stu-id="458d4-205">Type</span></span>  | <span data-ttu-id="458d4-206">Tamanho (bytes)</span><span class="sxs-lookup"><span data-stu-id="458d4-206">Size (bytes)</span></span> | <span data-ttu-id="458d4-207">Sumário</span><span class="sxs-lookup"><span data-stu-id="458d4-207">Contents</span></span>                         |
|-------|-------|--------------|----------------------------------|
| <span data-ttu-id="458d4-208">token</span><span class="sxs-lookup"><span data-stu-id="458d4-208">token</span></span> | <span data-ttu-id="458d4-209">WORD</span><span class="sxs-lookup"><span data-stu-id="458d4-209">WORD</span></span>  | <span data-ttu-id="458d4-210">2</span><span class="sxs-lookup"><span data-stu-id="458d4-210">2</span></span>            | <span data-ttu-id="458d4-211">\_lista de inteiros de tOKEN \_</span><span class="sxs-lookup"><span data-stu-id="458d4-211">tOKEN\_INTEGER\_LISt</span></span>             |
| <span data-ttu-id="458d4-212">count</span><span class="sxs-lookup"><span data-stu-id="458d4-212">count</span></span> | <span data-ttu-id="458d4-213">DWORD</span><span class="sxs-lookup"><span data-stu-id="458d4-213">DWORD</span></span> | <span data-ttu-id="458d4-214">4</span><span class="sxs-lookup"><span data-stu-id="458d4-214">4</span></span>            | <span data-ttu-id="458d4-215">Número de inteiros no campo de lista</span><span class="sxs-lookup"><span data-stu-id="458d4-215">Number of integers in list field</span></span> |
| <span data-ttu-id="458d4-216">list</span><span class="sxs-lookup"><span data-stu-id="458d4-216">list</span></span>  | <span data-ttu-id="458d4-217">DWORD</span><span class="sxs-lookup"><span data-stu-id="458d4-217">DWORD</span></span> | <span data-ttu-id="458d4-218">contagem de 4 x</span><span class="sxs-lookup"><span data-stu-id="458d4-218">4 x count</span></span>    | <span data-ttu-id="458d4-219">Lista de inteiros</span><span class="sxs-lookup"><span data-stu-id="458d4-219">Integer list</span></span>                     |



 

## <a name="token_float_list"></a><span data-ttu-id="458d4-220">\_lista de floats de token \_</span><span class="sxs-lookup"><span data-stu-id="458d4-220">TOKEN\_FLOAT\_LIST</span></span>

<span data-ttu-id="458d4-221">Um registro de comprimento variável.</span><span class="sxs-lookup"><span data-stu-id="458d4-221">A variable-length record.</span></span> <span data-ttu-id="458d4-222">O token é seguido por um valor de contagem que especifica o número de floats ou duplos que se seguem no campo de lista.</span><span class="sxs-lookup"><span data-stu-id="458d4-222">The token is followed by a count value that specifies the number of floats or doubles that follow in the list field.</span></span> <span data-ttu-id="458d4-223">O tamanho do valor de ponto flutuante (float ou Double) é determinado pelo valor de float SizeSpecified no cabeçalho do arquivo.</span><span class="sxs-lookup"><span data-stu-id="458d4-223">The size of the floating point value (float or double) is determined by the value of float sizespecified in the file header.</span></span> <span data-ttu-id="458d4-224">Para eficiência, listas flutuantes de TOKENs consecutivos devem ser compostas \_ \_ em uma única lista.</span><span class="sxs-lookup"><span data-stu-id="458d4-224">For efficiency, consecutive TOKEN\_FLOAT\_LISTs should be compounded into a single list.</span></span>



| <span data-ttu-id="458d4-225">Campo</span><span class="sxs-lookup"><span data-stu-id="458d4-225">Field</span></span> | <span data-ttu-id="458d4-226">Tipo</span><span class="sxs-lookup"><span data-stu-id="458d4-226">Type</span></span>               | <span data-ttu-id="458d4-227">Tamanho (bytes)</span><span class="sxs-lookup"><span data-stu-id="458d4-227">Size (bytes)</span></span>   | <span data-ttu-id="458d4-228">Sumário</span><span class="sxs-lookup"><span data-stu-id="458d4-228">Contents</span></span>                                  |
|-------|--------------------|----------------|-------------------------------------------|
| <span data-ttu-id="458d4-229">token</span><span class="sxs-lookup"><span data-stu-id="458d4-229">token</span></span> | <span data-ttu-id="458d4-230">WORD</span><span class="sxs-lookup"><span data-stu-id="458d4-230">WORD</span></span>               | <span data-ttu-id="458d4-231">2</span><span class="sxs-lookup"><span data-stu-id="458d4-231">2</span></span>              | <span data-ttu-id="458d4-232">\_lista de floats de tOKEN \_</span><span class="sxs-lookup"><span data-stu-id="458d4-232">tOKEN\_FLOAT\_LISt</span></span>                        |
| <span data-ttu-id="458d4-233">count</span><span class="sxs-lookup"><span data-stu-id="458d4-233">count</span></span> | <span data-ttu-id="458d4-234">DWORD</span><span class="sxs-lookup"><span data-stu-id="458d4-234">DWORD</span></span>              | <span data-ttu-id="458d4-235">4</span><span class="sxs-lookup"><span data-stu-id="458d4-235">4</span></span>              | <span data-ttu-id="458d4-236">Número de floats ou duplos no campo de lista</span><span class="sxs-lookup"><span data-stu-id="458d4-236">Number of floats or doubles in list field</span></span> |
| <span data-ttu-id="458d4-237">list</span><span class="sxs-lookup"><span data-stu-id="458d4-237">list</span></span>  | <span data-ttu-id="458d4-238">matriz float/double</span><span class="sxs-lookup"><span data-stu-id="458d4-238">float/double array</span></span> | <span data-ttu-id="458d4-239">contagem de 4 ou 8 x</span><span class="sxs-lookup"><span data-stu-id="458d4-239">4 or 8 x count</span></span> | <span data-ttu-id="458d4-240">Flutuar ou lista dupla</span><span class="sxs-lookup"><span data-stu-id="458d4-240">Float or double list</span></span>                      |



 

## <a name="related-topics"></a><span data-ttu-id="458d4-241">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="458d4-241">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="458d4-242">Codificação binária</span><span class="sxs-lookup"><span data-stu-id="458d4-242">Binary Encoding</span></span>](binary-encoding.md)
</dt> </dl>

 

 
