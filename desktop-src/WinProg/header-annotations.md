---
title: Anotações de cabeçalho
description: As anotações de cabeçalho descrevem como uma função usa seus parâmetros e valor de retorno.
ms.assetid: 4f9e42b1-2fe4-4173-946e-ab1805a96b9e
keywords:
- API do Windows, anotações de arquivo de cabeçalho
- anotações de arquivo de cabeçalho
- Specstrings. h
- idioma de anotação padrão (SAL)
- _bcount
- _deref
- _deref_opt
- _ecount
- _full
- _in
- _inout
- _opt
- _out
- _part
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8535118383a97d6c48f19246ad24ce324e8bb528
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105802092"
---
# <a name="header-annotations"></a><span data-ttu-id="e7064-117">Anotações de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="e7064-117">Header Annotations</span></span>

<span data-ttu-id="e7064-118">\[Este tópico descreve as anotações com suporte nos cabeçalhos do Windows por meio do Windows 7.</span><span class="sxs-lookup"><span data-stu-id="e7064-118">\[This topic describes the annotations supported in the Windows headers through Windows 7.</span></span> <span data-ttu-id="e7064-119">Se você estiver desenvolvendo para o Windows 8, deverá usar as anotações descritas em [anotações sal]( /previous-versions/visualstudio/visual-studio-2013/ms182032(v=vs.120)).\]</span><span class="sxs-lookup"><span data-stu-id="e7064-119">If you are developing for Windows 8, you should use the annotations described in [SAL Annotations]( /previous-versions/visualstudio/visual-studio-2013/ms182032(v=vs.120)).\]</span></span>

<span data-ttu-id="e7064-120">As anotações de cabeçalho descrevem como uma função usa seus parâmetros e valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="e7064-120">Header annotations describe how a function uses its parameters and return value.</span></span> <span data-ttu-id="e7064-121">Essas anotações foram adicionadas a muitos dos arquivos de cabeçalho do Windows para ajudá-lo a garantir que você está chamando a API do Windows corretamente.</span><span class="sxs-lookup"><span data-stu-id="e7064-121">These annotations have been added to many of the Windows header files to help you ensure that you are calling the Windows API correctly.</span></span> <span data-ttu-id="e7064-122">Se você habilitar a análise de código, que está disponível a partir do Visual Studio 2005, o compilador produzirá avisos de nível 6000 se você não estiver chamando essas funções de acordo com o uso descrito por meio das anotações.</span><span class="sxs-lookup"><span data-stu-id="e7064-122">If you enable code analysis, which is available starting with the Visual Studio 2005, the compiler will produce level 6000 warnings if you are not calling these functions per the usage described through the annotations.</span></span> <span data-ttu-id="e7064-123">Você também pode adicionar essas anotações em seu próprio código para garantir que ele esteja sendo chamado corretamente.</span><span class="sxs-lookup"><span data-stu-id="e7064-123">You can also add these annotations in your own code to ensure that it is being called correctly.</span></span> <span data-ttu-id="e7064-124">Para habilitar a análise de código no Visual Studio, consulte a documentação da sua versão do Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="e7064-124">To enable code analysis in Visual Studio, see the documentation for your version of Visual Studio.</span></span>

<span data-ttu-id="e7064-125">Essas anotações são definidas em Specstrings. h.</span><span class="sxs-lookup"><span data-stu-id="e7064-125">These annotations are defined in Specstrings.h.</span></span> <span data-ttu-id="e7064-126">Eles são criados em primitivos que fazem parte da linguagem de anotação padrão (SAL) e implementados usando o `_declspec("SAL_*")` .</span><span class="sxs-lookup"><span data-stu-id="e7064-126">They are built on primitives that are part of the Standard Annotation Language (SAL) and implemented using `_declspec("SAL_*")`.</span></span>

<span data-ttu-id="e7064-127">Há duas classes de anotações: anotações de buffer e anotações avançadas.</span><span class="sxs-lookup"><span data-stu-id="e7064-127">There are two classes of annotations: buffer annotations and advanced annotations.</span></span>

## <a name="buffer-annotations"></a><span data-ttu-id="e7064-128">Anotações de buffer</span><span class="sxs-lookup"><span data-stu-id="e7064-128">Buffer Annotations</span></span>

<span data-ttu-id="e7064-129">As anotações de buffer descrevem como as funções usam seus ponteiros e podem ser usadas para detectar saturações de buffer.</span><span class="sxs-lookup"><span data-stu-id="e7064-129">Buffer annotations describe how functions use their pointers and can be used to detect buffer overruns.</span></span> <span data-ttu-id="e7064-130">Cada parâmetro pode usar uma anotação de buffer ou zero.</span><span class="sxs-lookup"><span data-stu-id="e7064-130">Each parameter may use zero or one buffer annotation.</span></span> <span data-ttu-id="e7064-131">Uma anotação de buffer é construída com um sublinhado à esquerda e os componentes descritos nas seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="e7064-131">A buffer annotation is constructed with a leading underscore and the components described in the following sections.</span></span>



| <span data-ttu-id="e7064-132">Tamanho do buffer</span><span class="sxs-lookup"><span data-stu-id="e7064-132">Buffer size</span></span>                                                                                  | <span data-ttu-id="e7064-133">Description</span><span class="sxs-lookup"><span data-stu-id="e7064-133">Description</span></span>                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7064-134"><span id="_size_"></span><span id="_SIZE_"></span>(*tamanho*)</span><span class="sxs-lookup"><span data-stu-id="e7064-134"><span id="_size_"></span><span id="_SIZE_"></span>(*size*)</span></span><br/>                        | <span data-ttu-id="e7064-135">Especifica o tamanho total do buffer.</span><span class="sxs-lookup"><span data-stu-id="e7064-135">Specifies the total size of the buffer.</span></span> <span data-ttu-id="e7064-136">Use with \_ bcount e \_ ecount; não use with \_ Part.</span><span class="sxs-lookup"><span data-stu-id="e7064-136">Use with \_bcount and \_ecount; do not use with \_part.</span></span> <span data-ttu-id="e7064-137">Esse valor é o espaço acessível; pode ser menor do que o espaço alocado.</span><span class="sxs-lookup"><span data-stu-id="e7064-137">This value is the accessible space; it may be less than the allocated space.</span></span><br/> |
| <span data-ttu-id="e7064-138"><span id="_size_length_"></span><span id="_SIZE_LENGTH_"></span>(*tamanho*,*comprimento*)</span><span class="sxs-lookup"><span data-stu-id="e7064-138"><span id="_size_length_"></span><span id="_SIZE_LENGTH_"></span>(*size*,*length*)</span></span><br/> | <span data-ttu-id="e7064-139">Especifica o tamanho total e o tamanho inicializado do buffer.</span><span class="sxs-lookup"><span data-stu-id="e7064-139">Specifies the total size and initialized length of the buffer.</span></span> <span data-ttu-id="e7064-140">Use with \_ bcount \_ Part e \_ ecount \_ Part.</span><span class="sxs-lookup"><span data-stu-id="e7064-140">Use with \_bcount\_part and \_ecount\_part.</span></span> <span data-ttu-id="e7064-141">O tamanho total pode ser menor do que o espaço alocado.</span><span class="sxs-lookup"><span data-stu-id="e7064-141">The total size may be less than the allocated space.</span></span><br/>              |



 



| <span data-ttu-id="e7064-142">Unidades de tamanho do buffer</span><span class="sxs-lookup"><span data-stu-id="e7064-142">Buffer size units</span></span>                                                       | <span data-ttu-id="e7064-143">Description</span><span class="sxs-lookup"><span data-stu-id="e7064-143">Description</span></span>                                |
|-------------------------------------------------------------------------|--------------------------------------------|
| <span data-ttu-id="e7064-144"><span id="_bcount"></span><span id="_BCOUNT"></span>\_bcount</span><span class="sxs-lookup"><span data-stu-id="e7064-144"><span id="_bcount"></span><span id="_BCOUNT"></span>\_bcount</span></span><br/> | <span data-ttu-id="e7064-145">O tamanho do buffer está em bytes.</span><span class="sxs-lookup"><span data-stu-id="e7064-145">The buffer size is in bytes.</span></span><br/>    |
| <span data-ttu-id="e7064-146"><span id="_ecount"></span><span id="_ECOUNT"></span>\_ecount</span><span class="sxs-lookup"><span data-stu-id="e7064-146"><span id="_ecount"></span><span id="_ECOUNT"></span>\_ecount</span></span><br/> | <span data-ttu-id="e7064-147">O tamanho do buffer está em elementos.</span><span class="sxs-lookup"><span data-stu-id="e7064-147">The buffer size is in elements.</span></span><br/> |



 



| <span data-ttu-id="e7064-148">Direção</span><span class="sxs-lookup"><span data-stu-id="e7064-148">Direction</span></span>                                                            | <span data-ttu-id="e7064-149">Descrição</span><span class="sxs-lookup"><span data-stu-id="e7064-149">Description</span></span>                                                                                                                                                                                                                |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7064-150"><span id="_in"></span><span id="_IN"></span>\_no</span><span class="sxs-lookup"><span data-stu-id="e7064-150"><span id="_in"></span><span id="_IN"></span>\_in</span></span><br/>          | <span data-ttu-id="e7064-151">A função lê do buffer.</span><span class="sxs-lookup"><span data-stu-id="e7064-151">The function reads from the buffer.</span></span> <span data-ttu-id="e7064-152">O chamador fornece o buffer e o inicializa.</span><span class="sxs-lookup"><span data-stu-id="e7064-152">The caller provides the buffer and initializes it.</span></span><br/>                                                                                                                          |
| <span data-ttu-id="e7064-153"><span id="_inout"></span><span id="_INOUT"></span>\_InOut</span><span class="sxs-lookup"><span data-stu-id="e7064-153"><span id="_inout"></span><span id="_INOUT"></span>\_inout</span></span><br/> | <span data-ttu-id="e7064-154">A função lê e grava no buffer.</span><span class="sxs-lookup"><span data-stu-id="e7064-154">The function both reads from and writes to buffer.</span></span> <span data-ttu-id="e7064-155">O chamador fornece o buffer e o inicializa.</span><span class="sxs-lookup"><span data-stu-id="e7064-155">The caller provides the buffer and initializes it.</span></span> <span data-ttu-id="e7064-156">Se usado com \_ Deref, o buffer pode ser realocado pela função.</span><span class="sxs-lookup"><span data-stu-id="e7064-156">If used with \_deref, the buffer may be reallocated by the function.</span></span><br/>                                      |
| <span data-ttu-id="e7064-157"><span id="_out"></span><span id="_OUT"></span>\_fora</span><span class="sxs-lookup"><span data-stu-id="e7064-157"><span id="_out"></span><span id="_OUT"></span>\_out</span></span><br/>       | <span data-ttu-id="e7064-158">A função grava no buffer.</span><span class="sxs-lookup"><span data-stu-id="e7064-158">The function writes to the buffer.</span></span> <span data-ttu-id="e7064-159">Se usado no valor de retorno ou com \_ Deref, a função fornece o buffer e o inicializa.</span><span class="sxs-lookup"><span data-stu-id="e7064-159">If used on the return value or with \_deref, the function provides the buffer and initializes it.</span></span> <span data-ttu-id="e7064-160">Caso contrário, o chamador fornecerá o buffer e a função o inicializará.</span><span class="sxs-lookup"><span data-stu-id="e7064-160">Otherwise, the caller provides the buffer and the function initializes it.</span></span><br/> |



 



| <span data-ttu-id="e7064-161">Indireção</span><span class="sxs-lookup"><span data-stu-id="e7064-161">Indirection</span></span>                                                                       | <span data-ttu-id="e7064-162">Description</span><span class="sxs-lookup"><span data-stu-id="e7064-162">Description</span></span>                                                                                            |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7064-163"><span id="_deref"></span><span id="_DEREF"></span>\_Deref</span><span class="sxs-lookup"><span data-stu-id="e7064-163"><span id="_deref"></span><span id="_DEREF"></span>\_deref</span></span><br/>              | <span data-ttu-id="e7064-164">Desfaça referência ao parâmetro para obter o ponteiro do buffer.</span><span class="sxs-lookup"><span data-stu-id="e7064-164">Dereference the parameter to obtain the buffer pointer.</span></span> <span data-ttu-id="e7064-165">Este parâmetro não pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="e7064-165">This parameter may not be **NULL**.</span></span><br/> |
| <span data-ttu-id="e7064-166"><span id="_deref_opt"></span><span id="_DEREF_OPT"></span>\_Deref \_ aceitar</span><span class="sxs-lookup"><span data-stu-id="e7064-166"><span id="_deref_opt"></span><span id="_DEREF_OPT"></span>\_deref\_opt</span></span><br/> | <span data-ttu-id="e7064-167">Desfaça referência ao parâmetro para obter o ponteiro do buffer.</span><span class="sxs-lookup"><span data-stu-id="e7064-167">Dereference the parameter to obtain the buffer pointer.</span></span> <span data-ttu-id="e7064-168">Este parâmetro pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="e7064-168">This parameter can be **NULL**.</span></span><br/>     |



 



| <span data-ttu-id="e7064-169">Inicialização</span><span class="sxs-lookup"><span data-stu-id="e7064-169">Initialization</span></span>                                                    | <span data-ttu-id="e7064-170">Description</span><span class="sxs-lookup"><span data-stu-id="e7064-170">Description</span></span>                                                                                                              |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7064-171"><span id="_full"></span><span id="_FULL"></span>\_completo</span><span class="sxs-lookup"><span data-stu-id="e7064-171"><span id="_full"></span><span id="_FULL"></span>\_full</span></span><br/> | <span data-ttu-id="e7064-172">A função inicializa todo o buffer.</span><span class="sxs-lookup"><span data-stu-id="e7064-172">The function initializes the entire buffer.</span></span> <span data-ttu-id="e7064-173">Use somente com buffers de saída.</span><span class="sxs-lookup"><span data-stu-id="e7064-173">Use only with output buffers.</span></span><br/>                                     |
| <span data-ttu-id="e7064-174"><span id="_part"></span><span id="_PART"></span>\_parte</span><span class="sxs-lookup"><span data-stu-id="e7064-174"><span id="_part"></span><span id="_PART"></span>\_part</span></span><br/> | <span data-ttu-id="e7064-175">A função inicializa parte do buffer e indica explicitamente o quanto.</span><span class="sxs-lookup"><span data-stu-id="e7064-175">The function initializes part of the buffer, and explicitly indicates how much.</span></span> <span data-ttu-id="e7064-176">Use somente com buffers de saída.</span><span class="sxs-lookup"><span data-stu-id="e7064-176">Use only with output buffers.</span></span><br/> |



 



| <span data-ttu-id="e7064-177">Buffer necessário ou opcional</span><span class="sxs-lookup"><span data-stu-id="e7064-177">Required or optional buffer</span></span>                                    | <span data-ttu-id="e7064-178">Description</span><span class="sxs-lookup"><span data-stu-id="e7064-178">Description</span></span>                                |
|----------------------------------------------------------------|--------------------------------------------|
| <span data-ttu-id="e7064-179"><span id="_opt"></span><span id="_OPT"></span>\_opt</span><span class="sxs-lookup"><span data-stu-id="e7064-179"><span id="_opt"></span><span id="_OPT"></span>\_opt</span></span><br/> | <span data-ttu-id="e7064-180">Este parâmetro pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="e7064-180">This parameter can be **NULL**.</span></span><br/> |



 

<span data-ttu-id="e7064-181">O exemplo a seguir mostra as anotações da função **GetModuleFileName** .</span><span class="sxs-lookup"><span data-stu-id="e7064-181">The following example shows the annotations for the **GetModuleFileName** function.</span></span> <span data-ttu-id="e7064-182">O parâmetro *HMODULE* é um parâmetro de entrada opcional.</span><span class="sxs-lookup"><span data-stu-id="e7064-182">The *hModule* parameter is an optional input parameter .</span></span> <span data-ttu-id="e7064-183">O parâmetro *lpFileName* é um parâmetro de saída; seu tamanho em caracteres é especificado pelo parâmetro *nSize* e seu comprimento inclui o caractere de terminação **nula**.</span><span class="sxs-lookup"><span data-stu-id="e7064-183">The *lpFilename* parameter is an output parameter; its size in characters is specified by the *nSize* parameter and its length includes the **null**-terminating character.</span></span> <span data-ttu-id="e7064-184">O parâmetro *nSize* é um parâmetro de entrada.</span><span class="sxs-lookup"><span data-stu-id="e7064-184">The *nSize* parameter is an input parameter.</span></span>


```C++
DWORD
WINAPI
GetModuleFileName(
    __in_opt HMODULE hModule,
    __out_ecount_part(nSize, return + 1) LPTSTR lpFilename,
    __in DWORD nSize
    );
```



<span data-ttu-id="e7064-185">A seguir estão as anotações definidas em Specstrings. h.</span><span class="sxs-lookup"><span data-stu-id="e7064-185">The following are the annotations defined in Specstrings.h.</span></span> <span data-ttu-id="e7064-186">Use as informações nas tabelas acima para interpretar seu significado.</span><span class="sxs-lookup"><span data-stu-id="e7064-186">Use the information in the tables above to interpret their meaning.</span></span>

<span data-ttu-id="e7064-187">__bcount (*tamanho*)</span><span class="sxs-lookup"><span data-stu-id="e7064-187">__bcount(*size*)</span></span>  
<span data-ttu-id="e7064-188">__bcount_opt (*tamanho*)</span><span class="sxs-lookup"><span data-stu-id="e7064-188">__bcount_opt(*size*)</span></span>  
<span data-ttu-id="e7064-189">__deref_bcount (*tamanho*)</span><span class="sxs-lookup"><span data-stu-id="e7064-189">__deref_bcount(*size*)</span></span>  
<span data-ttu-id="e7064-190">__deref_bcount_opt (*tamanho*)</span><span class="sxs-lookup"><span data-stu-id="e7064-190">__deref_bcount_opt(*size*)</span></span>  
<span data-ttu-id="e7064-191">__deref_ecount (*tamanho*)</span><span class="sxs-lookup"><span data-stu-id="e7064-191">__deref_ecount(*size*)</span></span>  
<span data-ttu-id="e7064-192">__deref_ecount_opt (*tamanho*)</span><span class="sxs-lookup"><span data-stu-id="e7064-192">__deref_ecount_opt(*size*)</span></span>  
<span data-ttu-id="e7064-193">__deref_in</span><span class="sxs-lookup"><span data-stu-id="e7064-193">__deref_in</span></span>  
<span data-ttu-id="e7064-194">__deref_in_bcount (*tamanho*)</span><span class="sxs-lookup"><span data-stu-id="e7064-194">__deref_in_bcount(*size*)</span></span>  
<span data-ttu-id="e7064-195">__deref_in_bcount_opt (*tamanho*)</span><span class="sxs-lookup"><span data-stu-id="e7064-195">__deref_in_bcount_opt(*size*)</span></span>  
<span data-ttu-id="e7064-196">__deref_in_ecount (*tamanho*)</span><span class="sxs-lookup"><span data-stu-id="e7064-196">__deref_in_ecount(*size*)</span></span>  
<span data-ttu-id="e7064-197">__deref_in_ecount_opt (*tamanho*)</span><span class="sxs-lookup"><span data-stu-id="e7064-197">__deref_in_ecount_opt(*size*)</span></span>  
<span data-ttu-id="e7064-198">__deref_in_opt</span><span class="sxs-lookup"><span data-stu-id="e7064-198">__deref_in_opt</span></span>  
<span data-ttu-id="e7064-199">__deref_inout</span><span class="sxs-lookup"><span data-stu-id="e7064-199">__deref_inout</span></span>  
<span data-ttu-id="e7064-200">__deref_inout_bcount (*tamanho*)</span><span class="sxs-lookup"><span data-stu-id="e7064-200">__deref_inout_bcount(*size*)</span></span>  
<span data-ttu-id="e7064-201">__deref_inout_bcount_full (*tamanho*)</span><span class="sxs-lookup"><span data-stu-id="e7064-201">__deref_inout_bcount_full(*size*)</span></span>  
<span data-ttu-id="e7064-202">__deref_inout_bcount_full_opt (*tamanho*)</span><span class="sxs-lookup"><span data-stu-id="e7064-202">__deref_inout_bcount_full_opt(*size*)</span></span>  
<span data-ttu-id="e7064-203">__deref_inout_bcount_opt (*tamanho*)</span><span class="sxs-lookup"><span data-stu-id="e7064-203">__deref_inout_bcount_opt(*size*)</span></span>  
<span data-ttu-id="e7064-204">__deref_inout_bcount_part (*tamanho*,*comprimento*)</span><span class="sxs-lookup"><span data-stu-id="e7064-204">__deref_inout_bcount_part(*size*,*length*)</span></span>  
<span data-ttu-id="e7064-205">__deref_inout_bcount_part_opt (*tamanho*,*comprimento*)</span><span class="sxs-lookup"><span data-stu-id="e7064-205">__deref_inout_bcount_part_opt(*size*,*length*)</span></span>  
<span data-ttu-id="e7064-206">__deref_inout_ecount (*tamanho*)</span><span class="sxs-lookup"><span data-stu-id="e7064-206">__deref_inout_ecount(*size*)</span></span>  
<span data-ttu-id="e7064-207">__deref_inout_ecount_full (*tamanho*)</span><span class="sxs-lookup"><span data-stu-id="e7064-207">__deref_inout_ecount_full(*size*)</span></span>  
<span data-ttu-id="e7064-208">__deref_inout_ecount_full_opt (*tamanho*)</span><span class="sxs-lookup"><span data-stu-id="e7064-208">__deref_inout_ecount_full_opt(*size*)</span></span>  
<span data-ttu-id="e7064-209">__deref_inout_ecount_opt (*tamanho*)</span><span class="sxs-lookup"><span data-stu-id="e7064-209">__deref_inout_ecount_opt(*size*)</span></span>  
<span data-ttu-id="e7064-210">__deref_inout_ecount_part (*tamanho*,*comprimento*)</span><span class="sxs-lookup"><span data-stu-id="e7064-210">__deref_inout_ecount_part(*size*,*length*)</span></span>  
<span data-ttu-id="e7064-211">__deref_inout_ecount_part_opt (*tamanho*,*comprimento*)</span><span class="sxs-lookup"><span data-stu-id="e7064-211">__deref_inout_ecount_part_opt(*size*,*length*)</span></span>  
<span data-ttu-id="e7064-212">__deref_inout_opt</span><span class="sxs-lookup"><span data-stu-id="e7064-212">__deref_inout_opt</span></span>  
<span data-ttu-id="e7064-213">__deref_opt_bcount (*tamanho*)</span><span class="sxs-lookup"><span data-stu-id="e7064-213">__deref_opt_bcount(*size*)</span></span>  
<span data-ttu-id="e7064-214">__deref_opt_bcount_opt (*tamanho*)</span><span class="sxs-lookup"><span data-stu-id="e7064-214">__deref_opt_bcount_opt(*size*)</span></span>  
<span data-ttu-id="e7064-215">__deref_opt_ecount (*tamanho*)</span><span class="sxs-lookup"><span data-stu-id="e7064-215">__deref_opt_ecount(*size*)</span></span>  
<span data-ttu-id="e7064-216">__deref_opt_ecount_opt (*tamanho*)</span><span class="sxs-lookup"><span data-stu-id="e7064-216">__deref_opt_ecount_opt(*size*)</span></span>  
<span data-ttu-id="e7064-217">__deref_opt_in</span><span class="sxs-lookup"><span data-stu-id="e7064-217">__deref_opt_in</span></span>  
<span data-ttu-id="e7064-218">__deref_opt_in_bcount (*tamanho*)</span><span class="sxs-lookup"><span data-stu-id="e7064-218">__deref_opt_in_bcount(*size*)</span></span>  
<span data-ttu-id="e7064-219">__deref_opt_in_bcount_opt (*tamanho*)</span><span class="sxs-lookup"><span data-stu-id="e7064-219">__deref_opt_in_bcount_opt(*size*)</span></span>  
<span data-ttu-id="e7064-220">__deref_opt_in_ecount (*tamanho*)</span><span class="sxs-lookup"><span data-stu-id="e7064-220">__deref_opt_in_ecount(*size*)</span></span>  
<span data-ttu-id="e7064-221">__deref_opt_in_ecount_opt (*tamanho*)</span><span class="sxs-lookup"><span data-stu-id="e7064-221">__deref_opt_in_ecount_opt(*size*)</span></span>  
<span data-ttu-id="e7064-222">__deref_opt_in_opt</span><span class="sxs-lookup"><span data-stu-id="e7064-222">__deref_opt_in_opt</span></span>  
<span data-ttu-id="e7064-223">__deref_opt_inout</span><span class="sxs-lookup"><span data-stu-id="e7064-223">__deref_opt_inout</span></span>  
<span data-ttu-id="e7064-224">__deref_opt_inout_bcount (*tamanho*)</span><span class="sxs-lookup"><span data-stu-id="e7064-224">__deref_opt_inout_bcount(*size*)</span></span>  
<span data-ttu-id="e7064-225">__deref_opt_inout_bcount_full (*tamanho*)</span><span class="sxs-lookup"><span data-stu-id="e7064-225">__deref_opt_inout_bcount_full(*size*)</span></span>  
<span data-ttu-id="e7064-226">__deref_opt_inout_bcount_full_opt (*tamanho*)</span><span class="sxs-lookup"><span data-stu-id="e7064-226">__deref_opt_inout_bcount_full_opt(*size*)</span></span>  
<span data-ttu-id="e7064-227">__deref_opt_inout_bcount_opt (*tamanho*)</span><span class="sxs-lookup"><span data-stu-id="e7064-227">__deref_opt_inout_bcount_opt(*size*)</span></span>  
<span data-ttu-id="e7064-228">__deref_opt_inout_bcount_part (*tamanho*,*comprimento*)</span><span class="sxs-lookup"><span data-stu-id="e7064-228">__deref_opt_inout_bcount_part(*size*,*length*)</span></span>  
<span data-ttu-id="e7064-229">__deref_opt_inout_bcount_part_opt (*tamanho*,*comprimento*)</span><span class="sxs-lookup"><span data-stu-id="e7064-229">__deref_opt_inout_bcount_part_opt(*size*,*length*)</span></span>  
<span data-ttu-id="e7064-230">__deref_opt_inout_ecount (*tamanho*)</span><span class="sxs-lookup"><span data-stu-id="e7064-230">__deref_opt_inout_ecount(*size*)</span></span>  
<span data-ttu-id="e7064-231">__deref_opt_inout_ecount_full (*tamanho*)</span><span class="sxs-lookup"><span data-stu-id="e7064-231">__deref_opt_inout_ecount_full(*size*)</span></span>  
<span data-ttu-id="e7064-232">__deref_opt_inout_ecount_full_opt (*tamanho*)</span><span class="sxs-lookup"><span data-stu-id="e7064-232">__deref_opt_inout_ecount_full_opt(*size*)</span></span>  
<span data-ttu-id="e7064-233">__deref_opt_inout_ecount_opt (*tamanho*)</span><span class="sxs-lookup"><span data-stu-id="e7064-233">__deref_opt_inout_ecount_opt(*size*)</span></span>  
<span data-ttu-id="e7064-234">__deref_opt_inout_ecount_part (*tamanho*,*comprimento*)</span><span class="sxs-lookup"><span data-stu-id="e7064-234">__deref_opt_inout_ecount_part(*size*,*length*)</span></span>  
<span data-ttu-id="e7064-235">__deref_opt_inout_ecount_part_opt (*tamanho*,*comprimento*)</span><span class="sxs-lookup"><span data-stu-id="e7064-235">__deref_opt_inout_ecount_part_opt(*size*,*length*)</span></span>  
<span data-ttu-id="e7064-236">__deref_opt_inout_opt</span><span class="sxs-lookup"><span data-stu-id="e7064-236">__deref_opt_inout_opt</span></span>  
<span data-ttu-id="e7064-237">__deref_opt_out</span><span class="sxs-lookup"><span data-stu-id="e7064-237">__deref_opt_out</span></span>  
<span data-ttu-id="e7064-238">__deref_opt_out_bcount (*tamanho*)</span><span class="sxs-lookup"><span data-stu-id="e7064-238">__deref_opt_out_bcount(*size*)</span></span>  
<span data-ttu-id="e7064-239">__deref_opt_out_bcount_full (*tamanho*)</span><span class="sxs-lookup"><span data-stu-id="e7064-239">__deref_opt_out_bcount_full(*size*)</span></span>  
<span data-ttu-id="e7064-240">__deref_opt_out_bcount_full_opt (*tamanho*)</span><span class="sxs-lookup"><span data-stu-id="e7064-240">__deref_opt_out_bcount_full_opt(*size*)</span></span>  
<span data-ttu-id="e7064-241">__deref_opt_out_bcount_opt (*tamanho*)</span><span class="sxs-lookup"><span data-stu-id="e7064-241">__deref_opt_out_bcount_opt(*size*)</span></span>  
<span data-ttu-id="e7064-242">__deref_opt_out_bcount_part (*tamanho*,*comprimento*)</span><span class="sxs-lookup"><span data-stu-id="e7064-242">__deref_opt_out_bcount_part(*size*,*length*)</span></span>  
<span data-ttu-id="e7064-243">__deref_opt_out_bcount_part_opt (*tamanho*,*comprimento*)</span><span class="sxs-lookup"><span data-stu-id="e7064-243">__deref_opt_out_bcount_part_opt(*size*,*length*)</span></span>  
<span data-ttu-id="e7064-244">__deref_opt_out_ecount (*tamanho*)</span><span class="sxs-lookup"><span data-stu-id="e7064-244">__deref_opt_out_ecount(*size*)</span></span>  
<span data-ttu-id="e7064-245">__deref_opt_out_ecount_full (*tamanho*)</span><span class="sxs-lookup"><span data-stu-id="e7064-245">__deref_opt_out_ecount_full(*size*)</span></span>  
<span data-ttu-id="e7064-246">__deref_opt_out_ecount_full_opt (*tamanho*)</span><span class="sxs-lookup"><span data-stu-id="e7064-246">__deref_opt_out_ecount_full_opt(*size*)</span></span>  
<span data-ttu-id="e7064-247">__deref_opt_out_ecount_opt (*tamanho*)</span><span class="sxs-lookup"><span data-stu-id="e7064-247">__deref_opt_out_ecount_opt(*size*)</span></span>  
<span data-ttu-id="e7064-248">__deref_opt_out_ecount_part (*tamanho*,*comprimento*)</span><span class="sxs-lookup"><span data-stu-id="e7064-248">__deref_opt_out_ecount_part(*size*,*length*)</span></span>  
<span data-ttu-id="e7064-249">__deref_opt_out_ecount_part_opt (*tamanho*,*comprimento*)</span><span class="sxs-lookup"><span data-stu-id="e7064-249">__deref_opt_out_ecount_part_opt(*size*,*length*)</span></span>  
<span data-ttu-id="e7064-250">__deref_opt_out_opt</span><span class="sxs-lookup"><span data-stu-id="e7064-250">__deref_opt_out_opt</span></span>  
<span data-ttu-id="e7064-251">__deref_out</span><span class="sxs-lookup"><span data-stu-id="e7064-251">__deref_out</span></span>  
<span data-ttu-id="e7064-252">__deref_out_bcount (*tamanho*)</span><span class="sxs-lookup"><span data-stu-id="e7064-252">__deref_out_bcount(*size*)</span></span>  
<span data-ttu-id="e7064-253">__deref_out_bcount_full (*tamanho*)</span><span class="sxs-lookup"><span data-stu-id="e7064-253">__deref_out_bcount_full(*size*)</span></span>  
<span data-ttu-id="e7064-254">__deref_out_bcount_full_opt (*tamanho*)</span><span class="sxs-lookup"><span data-stu-id="e7064-254">__deref_out_bcount_full_opt(*size*)</span></span>  
<span data-ttu-id="e7064-255">__deref_out_bcount_opt (*tamanho*)</span><span class="sxs-lookup"><span data-stu-id="e7064-255">__deref_out_bcount_opt(*size*)</span></span>  
<span data-ttu-id="e7064-256">__deref_out_bcount_part (*tamanho*,*comprimento*)</span><span class="sxs-lookup"><span data-stu-id="e7064-256">__deref_out_bcount_part(*size*,*length*)</span></span>  
<span data-ttu-id="e7064-257">__deref_out_bcount_part_opt (*tamanho*,*comprimento*)</span><span class="sxs-lookup"><span data-stu-id="e7064-257">__deref_out_bcount_part_opt(*size*,*length*)</span></span>  
<span data-ttu-id="e7064-258">__deref_out_ecount (*tamanho*)</span><span class="sxs-lookup"><span data-stu-id="e7064-258">__deref_out_ecount(*size*)</span></span>  
<span data-ttu-id="e7064-259">__deref_out_ecount_full (*tamanho*)</span><span class="sxs-lookup"><span data-stu-id="e7064-259">__deref_out_ecount_full(*size*)</span></span>  
<span data-ttu-id="e7064-260">__deref_out_ecount_full_opt (*tamanho*)</span><span class="sxs-lookup"><span data-stu-id="e7064-260">__deref_out_ecount_full_opt(*size*)</span></span>  
<span data-ttu-id="e7064-261">__deref_out_ecount_opt (*tamanho*)</span><span class="sxs-lookup"><span data-stu-id="e7064-261">__deref_out_ecount_opt(*size*)</span></span>  
<span data-ttu-id="e7064-262">__deref_out_ecount_part (*tamanho*,*comprimento*)</span><span class="sxs-lookup"><span data-stu-id="e7064-262">__deref_out_ecount_part(*size*,*length*)</span></span>  
<span data-ttu-id="e7064-263">__deref_out_ecount_part_opt (*tamanho*,*comprimento*)</span><span class="sxs-lookup"><span data-stu-id="e7064-263">__deref_out_ecount_part_opt(*size*,*length*)</span></span>  
<span data-ttu-id="e7064-264">__deref_out_opt</span><span class="sxs-lookup"><span data-stu-id="e7064-264">__deref_out_opt</span></span>  
<span data-ttu-id="e7064-265">__ecount (*tamanho*)</span><span class="sxs-lookup"><span data-stu-id="e7064-265">__ecount(*size*)</span></span>  
<span data-ttu-id="e7064-266">__ecount_opt (*tamanho*)</span><span class="sxs-lookup"><span data-stu-id="e7064-266">__ecount_opt(*size*)</span></span>  
<span data-ttu-id="e7064-267">__in</span><span class="sxs-lookup"><span data-stu-id="e7064-267">__in</span></span>  
<span data-ttu-id="e7064-268">__in_bcount (*tamanho*)</span><span class="sxs-lookup"><span data-stu-id="e7064-268">__in_bcount(*size*)</span></span>  
<span data-ttu-id="e7064-269">__in_bcount_opt (*tamanho*)</span><span class="sxs-lookup"><span data-stu-id="e7064-269">__in_bcount_opt(*size*)</span></span>  
<span data-ttu-id="e7064-270">__in_ecount (*tamanho*)</span><span class="sxs-lookup"><span data-stu-id="e7064-270">__in_ecount(*size*)</span></span>  
<span data-ttu-id="e7064-271">__in_ecount_opt (*tamanho*)</span><span class="sxs-lookup"><span data-stu-id="e7064-271">__in_ecount_opt(*size*)</span></span>  
<span data-ttu-id="e7064-272">__in_opt</span><span class="sxs-lookup"><span data-stu-id="e7064-272">__in_opt</span></span>  
<span data-ttu-id="e7064-273">__inout</span><span class="sxs-lookup"><span data-stu-id="e7064-273">__inout</span></span>  
<span data-ttu-id="e7064-274">__inout_bcount (*tamanho*)</span><span class="sxs-lookup"><span data-stu-id="e7064-274">__inout_bcount(*size*)</span></span>  
<span data-ttu-id="e7064-275">__inout_bcount_full (*tamanho*)</span><span class="sxs-lookup"><span data-stu-id="e7064-275">__inout_bcount_full(*size*)</span></span>  
<span data-ttu-id="e7064-276">__inout_bcount_full_opt (*tamanho*)</span><span class="sxs-lookup"><span data-stu-id="e7064-276">__inout_bcount_full_opt(*size*)</span></span>  
<span data-ttu-id="e7064-277">__inout_bcount_opt (*tamanho*)</span><span class="sxs-lookup"><span data-stu-id="e7064-277">__inout_bcount_opt(*size*)</span></span>  
<span data-ttu-id="e7064-278">__inout_bcount_part (*tamanho*,*comprimento*)</span><span class="sxs-lookup"><span data-stu-id="e7064-278">__inout_bcount_part(*size*,*length*)</span></span>  
<span data-ttu-id="e7064-279">__inout_bcount_part_opt (*tamanho*,*comprimento*)</span><span class="sxs-lookup"><span data-stu-id="e7064-279">__inout_bcount_part_opt(*size*,*length*)</span></span>  
<span data-ttu-id="e7064-280">__inout_ecount (*tamanho*)</span><span class="sxs-lookup"><span data-stu-id="e7064-280">__inout_ecount(*size*)</span></span>  
<span data-ttu-id="e7064-281">__inout_ecount_full (*tamanho*)</span><span class="sxs-lookup"><span data-stu-id="e7064-281">__inout_ecount_full(*size*)</span></span>  
<span data-ttu-id="e7064-282">__inout_ecount_full_opt (*tamanho*)</span><span class="sxs-lookup"><span data-stu-id="e7064-282">__inout_ecount_full_opt(*size*)</span></span>  
<span data-ttu-id="e7064-283">__inout_ecount_opt (*tamanho*)</span><span class="sxs-lookup"><span data-stu-id="e7064-283">__inout_ecount_opt(*size*)</span></span>  
<span data-ttu-id="e7064-284">__inout_ecount_part (*tamanho*,*comprimento*)</span><span class="sxs-lookup"><span data-stu-id="e7064-284">__inout_ecount_part(*size*,*length*)</span></span>  
<span data-ttu-id="e7064-285">__inout_ecount_part_opt (*tamanho*,*comprimento*)</span><span class="sxs-lookup"><span data-stu-id="e7064-285">__inout_ecount_part_opt(*size*,*length*)</span></span>  
<span data-ttu-id="e7064-286">__inout_opt</span><span class="sxs-lookup"><span data-stu-id="e7064-286">__inout_opt</span></span>  
<span data-ttu-id="e7064-287">__out</span><span class="sxs-lookup"><span data-stu-id="e7064-287">__out</span></span>  
<span data-ttu-id="e7064-288">__out_bcount (*tamanho*)</span><span class="sxs-lookup"><span data-stu-id="e7064-288">__out_bcount(*size*)</span></span>  
<span data-ttu-id="e7064-289">__out_bcount_full (*tamanho*)</span><span class="sxs-lookup"><span data-stu-id="e7064-289">__out_bcount_full(*size*)</span></span>  
<span data-ttu-id="e7064-290">__out_bcount_full_opt (*tamanho*)</span><span class="sxs-lookup"><span data-stu-id="e7064-290">__out_bcount_full_opt(*size*)</span></span>  
<span data-ttu-id="e7064-291">__out_bcount_opt (*tamanho*)</span><span class="sxs-lookup"><span data-stu-id="e7064-291">__out_bcount_opt(*size*)</span></span>  
<span data-ttu-id="e7064-292">__out_bcount_part (*tamanho*,*comprimento*)</span><span class="sxs-lookup"><span data-stu-id="e7064-292">__out_bcount_part(*size*,*length*)</span></span>  
<span data-ttu-id="e7064-293">__out_bcount_part_opt (*tamanho*,*comprimento*)</span><span class="sxs-lookup"><span data-stu-id="e7064-293">__out_bcount_part_opt(*size*,*length*)</span></span>  
<span data-ttu-id="e7064-294">__out_ecount (*tamanho*)</span><span class="sxs-lookup"><span data-stu-id="e7064-294">__out_ecount(*size*)</span></span>  
<span data-ttu-id="e7064-295">__out_ecount_full (*tamanho*)</span><span class="sxs-lookup"><span data-stu-id="e7064-295">__out_ecount_full(*size*)</span></span>  
<span data-ttu-id="e7064-296">__out_ecount_full_opt (*tamanho*)</span><span class="sxs-lookup"><span data-stu-id="e7064-296">__out_ecount_full_opt(*size*)</span></span>  
<span data-ttu-id="e7064-297">__out_ecount_opt (*tamanho*)</span><span class="sxs-lookup"><span data-stu-id="e7064-297">__out_ecount_opt(*size*)</span></span>  
<span data-ttu-id="e7064-298">__out_ecount_part (*tamanho*,*comprimento*)</span><span class="sxs-lookup"><span data-stu-id="e7064-298">__out_ecount_part(*size*,*length*)</span></span>  
<span data-ttu-id="e7064-299">__out_ecount_part_opt (*tamanho*,*comprimento*)</span><span class="sxs-lookup"><span data-stu-id="e7064-299">__out_ecount_part_opt(*size*,*length*)</span></span>  
<span data-ttu-id="e7064-300">__out_opt</span><span class="sxs-lookup"><span data-stu-id="e7064-300">__out_opt</span></span>  

## <a name="advanced-annotations"></a><span data-ttu-id="e7064-301">Anotações avançadas</span><span class="sxs-lookup"><span data-stu-id="e7064-301">Advanced Annotations</span></span>

<span data-ttu-id="e7064-302">As anotações avançadas fornecem informações adicionais sobre o parâmetro ou valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="e7064-302">Advanced annotations provide additional information about the parameter or return value.</span></span> <span data-ttu-id="e7064-303">Cada parâmetro ou valor de retorno pode usar uma anotação avançada ou zero.</span><span class="sxs-lookup"><span data-stu-id="e7064-303">Each parameter or return value may use zero or one advanced annotation.</span></span>



| <span data-ttu-id="e7064-304">Annotation</span><span class="sxs-lookup"><span data-stu-id="e7064-304">Annotation</span></span>                                                                                                                                               | <span data-ttu-id="e7064-305">Description</span><span class="sxs-lookup"><span data-stu-id="e7064-305">Description</span></span>                                                                                                                                                                                                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7064-306"><span id="__blocksOn_resource_"></span><span id="__blockson_resource_"></span><span id="__BLOCKSON_RESOURCE_"></span>\_\_blocos (*recurso*)</span><span class="sxs-lookup"><span data-stu-id="e7064-306"><span id="__blocksOn_resource_"></span><span id="__blockson_resource_"></span><span id="__BLOCKSON_RESOURCE_"></span>\_\_blocksOn(*resource*)</span></span><br/> | <span data-ttu-id="e7064-307">As funções são bloqueadas no recurso especificado.</span><span class="sxs-lookup"><span data-stu-id="e7064-307">The functions blocks on the specified resource.</span></span><br/>                                                                                                                                                                                                                      |
| <span data-ttu-id="e7064-308"><span id="__callback"></span><span id="__CALLBACK"></span>\_\_retorno</span><span class="sxs-lookup"><span data-stu-id="e7064-308"><span id="__callback"></span><span id="__CALLBACK"></span>\_\_callback</span></span><br/>                                                                        | <span data-ttu-id="e7064-309">A função pode ser usada como um ponteiro de função.</span><span class="sxs-lookup"><span data-stu-id="e7064-309">The function can be used as a function pointer.</span></span><br/>                                                                                                                                                                                                                      |
| <span data-ttu-id="e7064-310"><span id="__checkReturn"></span><span id="__checkreturn"></span><span id="__CHECKRETURN"></span>\_\_checkReturn</span><span class="sxs-lookup"><span data-stu-id="e7064-310"><span id="__checkReturn"></span><span id="__checkreturn"></span><span id="__CHECKRETURN"></span>\_\_checkReturn</span></span><br/>                               | <span data-ttu-id="e7064-311">Os chamadores devem verificar o valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="e7064-311">Callers must check the return value.</span></span><br/>                                                                                                                                                                                                                                 |
| <span data-ttu-id="e7064-312"><span id="__format_string"></span><span id="__FORMAT_STRING"></span>\_\_Cadeia de formato \_</span><span class="sxs-lookup"><span data-stu-id="e7064-312"><span id="__format_string"></span><span id="__FORMAT_STRING"></span>\_\_format\_string</span></span><br/>                                                        | <span data-ttu-id="e7064-313">O parâmetro é uma cadeia de caracteres que contém marcadores de estilo printf%.</span><span class="sxs-lookup"><span data-stu-id="e7064-313">The parameter is a string that contains printf-style % markers.</span></span><br/>                                                                                                                                                                                                      |
| <span data-ttu-id="e7064-314"><span id="__in_awcount_expr_size_"></span><span id="__IN_AWCOUNT_EXPR_SIZE_"></span>\_\_em \_ awcount (*expr*,*size*)</span><span class="sxs-lookup"><span data-stu-id="e7064-314"><span id="__in_awcount_expr_size_"></span><span id="__IN_AWCOUNT_EXPR_SIZE_"></span>\_\_in\_awcount(*expr*,*size*)</span></span><br/>                            | <span data-ttu-id="e7064-315">Se a expressão for verdadeira na saída, o tamanho do buffer de entrada será especificado em bytes.</span><span class="sxs-lookup"><span data-stu-id="e7064-315">If the expression is true at exit, the size of the input buffer is specified in bytes.</span></span> <span data-ttu-id="e7064-316">Se a expressão for false, o tamanho será especificado em elementos.</span><span class="sxs-lookup"><span data-stu-id="e7064-316">If the expression is false, the size is specified in elements.</span></span><br/>                                                                                                                |
| <span data-ttu-id="e7064-317"><span id="__nullnullterminated"></span><span id="__NULLNULLTERMINATED"></span>\_\_nullnullterminated</span><span class="sxs-lookup"><span data-stu-id="e7064-317"><span id="__nullnullterminated"></span><span id="__NULLNULLTERMINATED"></span>\_\_nullnullterminated</span></span><br/>                                          | <span data-ttu-id="e7064-318">O buffer pode ser acessado até e incluindo a primeira sequência de dois caracteres ou ponteiros **nulos** .</span><span class="sxs-lookup"><span data-stu-id="e7064-318">The buffer may be accessed up to and including the first sequence of two **null** characters or pointers.</span></span><br/>                                                                                                                                                            |
| <span data-ttu-id="e7064-319"><span id="__nullterminated"></span><span id="__NULLTERMINATED"></span>\_\_NullTerminated</span><span class="sxs-lookup"><span data-stu-id="e7064-319"><span id="__nullterminated"></span><span id="__NULLTERMINATED"></span>\_\_nullterminated</span></span><br/>                                                      | <span data-ttu-id="e7064-320">O buffer pode ser acessado até e incluindo o primeiro caractere ou ponteiro **nulo** .</span><span class="sxs-lookup"><span data-stu-id="e7064-320">The buffer may be accessed up to and including the first **null** character or pointer.</span></span><br/>                                                                                                                                                                              |
| <span data-ttu-id="e7064-321"><span id="__out_awcount_expr_size_"></span><span id="__OUT_AWCOUNT_EXPR_SIZE_"></span>\_\_out \_ awcount (*expr*,*size*)</span><span class="sxs-lookup"><span data-stu-id="e7064-321"><span id="__out_awcount_expr_size_"></span><span id="__OUT_AWCOUNT_EXPR_SIZE_"></span>\_\_out\_awcount(*expr*,*size*)</span></span><br/>                         | <span data-ttu-id="e7064-322">Se a expressão for verdadeira na saída, o tamanho do buffer de saída será especificado em bytes.</span><span class="sxs-lookup"><span data-stu-id="e7064-322">If the expression is true at exit, the size of the output buffer is specified in bytes.</span></span> <span data-ttu-id="e7064-323">Se a expressão for false, o tamanho será especificado em elementos.</span><span class="sxs-lookup"><span data-stu-id="e7064-323">If the expression is false, the size is specified in elements.</span></span> <br/>                                                                                                              |
| <span data-ttu-id="e7064-324"><span id="__override"></span><span id="__OVERRIDE"></span>\_\_substituição</span><span class="sxs-lookup"><span data-stu-id="e7064-324"><span id="__override"></span><span id="__OVERRIDE"></span>\_\_override</span></span><br/>                                                                        | <span data-ttu-id="e7064-325">Especifica o comportamento de substituição do estilo C# para métodos virtuais.</span><span class="sxs-lookup"><span data-stu-id="e7064-325">Specifies C#-style override behavior for virtual methods.</span></span><br/>                                                                                                                                                                                                           |
| <span data-ttu-id="e7064-326"><span id="__reserved"></span><span id="__RESERVED"></span>\_\_reservado</span><span class="sxs-lookup"><span data-stu-id="e7064-326"><span id="__reserved"></span><span id="__RESERVED"></span>\_\_reserved</span></span><br/>                                                                        | <span data-ttu-id="e7064-327">O parâmetro é reservado para uso futuro e deve ser zero ou **nulo**.</span><span class="sxs-lookup"><span data-stu-id="e7064-327">The parameter is reserved for future use and must be zero or **NULL**.</span></span><br/>                                                                                                                                                                                               |
| <span data-ttu-id="e7064-328"><span id="__success_expr_"></span><span id="__SUCCESS_EXPR_"></span>\_\_êxito (*expr*)</span><span class="sxs-lookup"><span data-stu-id="e7064-328"><span id="__success_expr_"></span><span id="__SUCCESS_EXPR_"></span>\_\_success(*expr*)</span></span><br/>                                                       | <span data-ttu-id="e7064-329">Se a expressão for verdadeira na saída, o chamador poderá contar com todas as garantias especificadas por outras anotações.</span><span class="sxs-lookup"><span data-stu-id="e7064-329">If the expression is true at exit, the caller can rely on all guarantees specified by other annotations.</span></span> <span data-ttu-id="e7064-330">Se a expressão for false, o chamador não poderá contar com as garantias.</span><span class="sxs-lookup"><span data-stu-id="e7064-330">If the expression is false, the caller cannot rely on the guarantees.</span></span> <span data-ttu-id="e7064-331">Essa anotação é adicionada automaticamente a funções que retornam um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e7064-331">This annotation is automatically added to functions that return an **HRESULT** value.</span></span><br/> |
| <span data-ttu-id="e7064-332"><span id="__typefix_ctype_"></span><span id="__TYPEFIX_CTYPE_"></span>\_\_typefix (*CType*)</span><span class="sxs-lookup"><span data-stu-id="e7064-332"><span id="__typefix_ctype_"></span><span id="__TYPEFIX_CTYPE_"></span>\_\_typefix(*ctype*)</span></span><br/>                                                    | <span data-ttu-id="e7064-333">Trate o parâmetro como o tipo especificado em vez de seu tipo declarado.</span><span class="sxs-lookup"><span data-stu-id="e7064-333">Treat the parameter as the specified type rather than its declared type.</span></span><br/>                                                                                                                                                                                             |



 

<span data-ttu-id="e7064-334">Os exemplos a seguir mostram o buffer e as anotações avançadas para as funções [**DeleteTimerQueueTimer**](/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-deletetimerqueuetimer), [**FreeEnvironmentStrings**](/windows/desktop/api/processenv/nf-processenv-freeenvironmentstringsa)e [**UnhandledExceptionFilter**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-unhandledexceptionfilter) .</span><span class="sxs-lookup"><span data-stu-id="e7064-334">The following examples show the buffer and advanced annotations for the [**DeleteTimerQueueTimer**](/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-deletetimerqueuetimer), [**FreeEnvironmentStrings**](/windows/desktop/api/processenv/nf-processenv-freeenvironmentstringsa), and [**UnhandledExceptionFilter**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-unhandledexceptionfilter) functions.</span></span>


```C++
__checkReturn
BOOL
WINAPI
DeleteTimerQueueTimer(
    __in_opt HANDLE TimerQueue,
    __in     HANDLE Timer,
    __in_opt HANDLE CompletionEvent
    );

BOOL
WINAPI
FreeEnvironmentStrings(
    __in __nullnullterminated LPTCH
    );

__callback
LONG
WINAPI
UnhandledExceptionFilter(
    __in struct _EXCEPTION_POINTERS *ExceptionInfo
    );

```



## <a name="related-topics"></a><span data-ttu-id="e7064-335">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e7064-335">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e7064-336">Anotações de SAL</span><span class="sxs-lookup"><span data-stu-id="e7064-336">SAL Annotations</span></span>](/cpp/c-runtime-library/sal-annotations?view=vs-2019)
</dt> <dt>

[<span data-ttu-id="e7064-337">Walkthrough: analisando o código C/C++ para defeitos</span><span class="sxs-lookup"><span data-stu-id="e7064-337">Walkthrough: Analyzing C/C++ Code for Defects</span></span>](/visualstudio/code-quality/walkthrough-analyzing-c-cpp-code-for-defects?view=vs-2015)
</dt> </dl>

 

