---
title: " Diretivas If, elif, Else e endif"
description: Diretivas de pré-processador que controlam a compilação de partes de um arquivo de origem.
ms.assetid: f29e5a9b-cc0c-4fca-aac7-809a226eda58
keywords:
- Diretivas If, elif, Else e endif HLSL
topic_type:
- apiref
api_name:
- if, elif, else, and endif Directives
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a32206232c726f19febf77c3f3270882894a6747
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084553"
---
# <a name="if-elif-else-and-endif-directives"></a><span data-ttu-id="18c34-104">\#Diretivas If, \# elif, \# else e \# endif</span><span class="sxs-lookup"><span data-stu-id="18c34-104">\#if, \#elif, \#else, and \#endif Directives</span></span>

<span data-ttu-id="18c34-105">Diretivas de pré-processador que controlam a compilação de partes de um arquivo de origem.</span><span class="sxs-lookup"><span data-stu-id="18c34-105">Preprocessor directives that control compilation of portions of a source file.</span></span>



| <span data-ttu-id="18c34-106">\#Se *ifCondition* ...</span><span class="sxs-lookup"><span data-stu-id="18c34-106">\#if *ifCondition* ...</span></span>         |
|--------------------------------|
| <span data-ttu-id="18c34-107">\[\#*elifCondition* de elif...\]</span><span class="sxs-lookup"><span data-stu-id="18c34-107">\[\#elif *elifCondition* ...\]</span></span> |
| <span data-ttu-id="18c34-108">\[\#senão...\]</span><span class="sxs-lookup"><span data-stu-id="18c34-108">\[\#else ...\]</span></span>                 |
| <span data-ttu-id="18c34-109">\#endif</span><span class="sxs-lookup"><span data-stu-id="18c34-109">\#endif</span></span>                        |



 

## <a name="parameters"></a><span data-ttu-id="18c34-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="18c34-110">Parameters</span></span>



| <span data-ttu-id="18c34-111">Item</span><span class="sxs-lookup"><span data-stu-id="18c34-111">Item</span></span>                                                                                                                                                                                                 | <span data-ttu-id="18c34-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="18c34-112">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18c34-113"><span id="ifCondition"></span><span id="ifcondition"></span><span id="IFCONDITION"></span>*ifCondition*</span><span class="sxs-lookup"><span data-stu-id="18c34-113"><span id="ifCondition"></span><span id="ifcondition"></span><span id="IFCONDITION"></span>*ifCondition*</span></span><br/>                                                                                   | <span data-ttu-id="18c34-114">Condição principal a ser avaliada.</span><span class="sxs-lookup"><span data-stu-id="18c34-114">Primary condition to evaluate.</span></span> <span data-ttu-id="18c34-115">Se esse parâmetro for avaliado como um valor diferente de zero, todo o texto entre essa \# diretiva If e a próxima instância da \# diretiva elif, \# Else ou \# endif será mantido na unidade de tradução; caso contrário, o código-fonte subsequente não será retido.</span><span class="sxs-lookup"><span data-stu-id="18c34-115">If this parameter evaluates to a nonzero value, all text between this \#if directive and the next instance of the \#elif, \#else, or \#endif directive is retained in the translation unit; otherwise, the subsequent source code is not retained.</span></span> <br/> <span data-ttu-id="18c34-116">A condição pode usar o operador de pré-processador definido para determinar se uma macro ou constante de pré-processador específico está definida; Esse uso é equivalente ao uso da diretiva [ \# ifdef](dx-graphics-hlsl-appendix-pre-ifdef.md) .</span><span class="sxs-lookup"><span data-stu-id="18c34-116">The condition can use the preprocessor operator defined to determine whether a specific preprocessor constant or macro is defined; this usage is equivalent to the use of the [\#ifdef](dx-graphics-hlsl-appendix-pre-ifdef.md) directive.</span></span> <br/> <span data-ttu-id="18c34-117">Consulte a seção comentários para obter restrições sobre o valor do parâmetro *ifCondition* .</span><span class="sxs-lookup"><span data-stu-id="18c34-117">See the Remarks section for restrictions on the value of the *ifCondition* parameter.</span></span> <br/>                                                                                        |
| <span data-ttu-id="18c34-118"><span id="elifCondition__optional__________"></span><span id="elifcondition__optional__________"></span><span id="ELIFCONDITION__OPTIONAL__________"></span>*elifCondition* \[ adicional\]</span><span class="sxs-lookup"><span data-stu-id="18c34-118"><span id="elifCondition__optional__________"></span><span id="elifcondition__optional__________"></span><span id="ELIFCONDITION__OPTIONAL__________"></span>*elifCondition* \[optional\]</span></span> <br/> | <span data-ttu-id="18c34-119">Outra condição a ser avaliada.</span><span class="sxs-lookup"><span data-stu-id="18c34-119">Other condition to evaluate.</span></span> <span data-ttu-id="18c34-120">Se o parâmetro *ifCondition* e todas as \# diretivas elif anteriores forem avaliadas como zero, e esse parâmetro for avaliado como um valor diferente de zero, todo o texto entre essa \# diretiva elif e a próxima instância da \# diretiva elif, \# Else ou \# endif será mantido na unidade de tradução; caso contrário, o código-fonte subsequente não será retido.</span><span class="sxs-lookup"><span data-stu-id="18c34-120">If the *ifCondition* parameter and all previous \#elif directives evaluate to zero, and this parameter evaluates to a nonzero value, all text between this \#elif directive and the next instance of the \#elif, \#else, or \#endif directive is retained in the translation unit; otherwise, the subsequent source code is not retained.</span></span> <br/> <span data-ttu-id="18c34-121">A condição pode usar o operador de pré-processador definido para determinar se uma macro ou constante de pré-processador específico está definida; Esse uso é equivalente ao uso da diretiva [ \# ifdef](dx-graphics-hlsl-appendix-pre-ifdef.md) .</span><span class="sxs-lookup"><span data-stu-id="18c34-121">The condition can use the preprocessor operator defined to determine whether a specific preprocessor constant or macro is defined; this usage is equivalent to the use of the [\#ifdef](dx-graphics-hlsl-appendix-pre-ifdef.md) directive.</span></span> <br/> <span data-ttu-id="18c34-122">Consulte a seção comentários para obter restrições sobre o valor do parâmetro *elifCondition* .</span><span class="sxs-lookup"><span data-stu-id="18c34-122">See the Remarks section for restrictions on the value of the *elifCondition* parameter.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="18c34-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="18c34-123">Remarks</span></span>

<span data-ttu-id="18c34-124">Cada \# diretiva If em um arquivo de origem deve ser correspondida por uma \# diretiva de fechamento endif.</span><span class="sxs-lookup"><span data-stu-id="18c34-124">Each \#if directive in a source file must be matched by a closing \#endif directive.</span></span> <span data-ttu-id="18c34-125">Qualquer número de \# diretivas de elif pode aparecer entre as \# diretivas If e \# endif, mas no máximo uma \# diretiva else é permitida.</span><span class="sxs-lookup"><span data-stu-id="18c34-125">Any number of \#elif directives can appear between the \#if and \#endif directives, but at most one \#else directive is allowed.</span></span> <span data-ttu-id="18c34-126">A \# diretiva Else, se presente, deve ser a última diretiva antes de \# endif.</span><span class="sxs-lookup"><span data-stu-id="18c34-126">The \#else directive, if present, must be the last directive before \#endif.</span></span> <span data-ttu-id="18c34-127">As diretivas de compilação condicional contidas nos arquivos de inclusão devem atender às mesmas condições.</span><span class="sxs-lookup"><span data-stu-id="18c34-127">Conditional-compilation directives contained in include files must satisfy the same conditions.</span></span>

<span data-ttu-id="18c34-128">As \# diretivas If, \# elif, \# else e \# endif podem aninhar as partes de texto de outras \# diretivas If.</span><span class="sxs-lookup"><span data-stu-id="18c34-128">The \#if, \#elif, \#else, and \#endif directives can nest in the text portions of other \#if directives.</span></span> <span data-ttu-id="18c34-129">Cada diretiva aninhada \# Else, \# elif ou \# endif pertence à diretiva precedentes mais próxima \# .</span><span class="sxs-lookup"><span data-stu-id="18c34-129">Each nested \#else, \#elif, or \#endif directive belongs to the closest preceding \#if directive.</span></span>

<span data-ttu-id="18c34-130">Se nenhuma condição for avaliada como um valor diferente de zero, o pré-processador selecionará o bloco de texto após a \# diretiva else.</span><span class="sxs-lookup"><span data-stu-id="18c34-130">If no conditions evaluate to a nonzero value, the preprocessor selects the text block after the \#else directive.</span></span> <span data-ttu-id="18c34-131">Se a \# cláusula else for omitida e nenhuma condição for avaliada como um valor diferente de zero, nenhum bloco de texto será selecionado.</span><span class="sxs-lookup"><span data-stu-id="18c34-131">If the \#else clause is omitted and no conditions evaluate to a nonzero value, no text block is selected.</span></span>

<span data-ttu-id="18c34-132">Os parâmetros *ifCondition* e *elifCondition* muito atendem aos seguintes requisitos:</span><span class="sxs-lookup"><span data-stu-id="18c34-132">The *ifCondition* and *elifCondition* parameters much meet the following requirements:</span></span>

-   <span data-ttu-id="18c34-133">As expressões de compilação condicional são tratadas como valores [**longos assinados**](https://msdn.microsoft.com/library/cc953fe1(v=VS.71).aspx) e essas expressões são avaliadas usando as mesmas regras que as expressões em C++.</span><span class="sxs-lookup"><span data-stu-id="18c34-133">Conditional compilation expressions are treated as [**signed long**](https://msdn.microsoft.com/library/cc953fe1(v=VS.71).aspx) values, and these expressions are evaluated using the same rules as expressions in C++.</span></span>
-   <span data-ttu-id="18c34-134">As expressões devem ter o tipo integral e podem incluir apenas constantes de inteiros, constantes de caracteres e o operador defined.</span><span class="sxs-lookup"><span data-stu-id="18c34-134">Expressions must have integral type and can include only integer constants, character constants, and the defined operator.</span></span>
-   <span data-ttu-id="18c34-135">As expressões não podem usar **sizeof** ou um operador de conversão de tipo.</span><span class="sxs-lookup"><span data-stu-id="18c34-135">Expressions cannot use **sizeof** or a type-cast operator.</span></span>
-   <span data-ttu-id="18c34-136">O ambiente de destino talvez não consiga representar todos os intervalos de inteiros.</span><span class="sxs-lookup"><span data-stu-id="18c34-136">The target environment may not be able to represent all ranges of integers.</span></span>
-   <span data-ttu-id="18c34-137">A conversão representa o tipo [**int**](/windows/desktop/WinProg/windows-data-types) , o mesmo que o tipo **Long**, e o [**int não assinado**](https://msdn.microsoft.com/library/cc953fe1(v=VS.71).aspx) é o mesmo que o **Long não assinado**.</span><span class="sxs-lookup"><span data-stu-id="18c34-137">The translation represents type [**int**](/windows/desktop/WinProg/windows-data-types) the same as type **long**, and [**unsigned int**](https://msdn.microsoft.com/library/cc953fe1(v=VS.71).aspx) the same as **unsigned long**.</span></span>
-   <span data-ttu-id="18c34-138">O tradutor pode traduzir a constante de caracteres como um conjunto de valores de código diferentes do conjunto para o ambiente de destino.</span><span class="sxs-lookup"><span data-stu-id="18c34-138">The translator can translate character constants to a set of code values different from the set for the target environment.</span></span> <span data-ttu-id="18c34-139">Para determinar as propriedades do ambiente de destino, verifique os valores das macros de LIMITS.H em um aplicativo compilado para o ambiente de destino.</span><span class="sxs-lookup"><span data-stu-id="18c34-139">To determine the properties of the target environment, check values of macros from LIMITS.H in an application built for the target environment.</span></span>
-   <span data-ttu-id="18c34-140">A expressão não deve executar consultas ambientais e deve permanecer isolada de detalhes da implementação no computador de destino.</span><span class="sxs-lookup"><span data-stu-id="18c34-140">The expression must not perform any environmental inquiries and must remain insulated from implementation details on the target computer.</span></span>

## <a name="examples"></a><span data-ttu-id="18c34-141">Exemplos</span><span class="sxs-lookup"><span data-stu-id="18c34-141">Examples</span></span>

<span data-ttu-id="18c34-142">Esta seção contém exemplos que demonstram como usar as diretivas de pré-processador de compilação condicional.</span><span class="sxs-lookup"><span data-stu-id="18c34-142">This section contains examples that demonstrate how to use conditional compilation preprocessor directives.</span></span>

### <a name="use-of-the-defined-operator"></a><span data-ttu-id="18c34-143">Uso do operador definido</span><span class="sxs-lookup"><span data-stu-id="18c34-143">Use of the defined operator</span></span>

<span data-ttu-id="18c34-144">O exemplo a seguir mostra o uso do operador definido.</span><span class="sxs-lookup"><span data-stu-id="18c34-144">The following example shows the use of the defined operator.</span></span> <span data-ttu-id="18c34-145">Se o crédito do identificador for definido, a chamada para a função de **crédito** será compilada.</span><span class="sxs-lookup"><span data-stu-id="18c34-145">If the identifier CREDIT is defined, the call to the **credit** function is compiled.</span></span> <span data-ttu-id="18c34-146">Se o débito do identificador for definido, a chamada para a função **Debit** será compilada.</span><span class="sxs-lookup"><span data-stu-id="18c34-146">If the identifier DEBIT is defined, the call to the **debit** function is compiled.</span></span> <span data-ttu-id="18c34-147">Se nenhum identificador for definido, a chamada para a função de **erro** é compilada.</span><span class="sxs-lookup"><span data-stu-id="18c34-147">If neither identifier is defined, the call to the **printerror** function is compiled.</span></span> <span data-ttu-id="18c34-148">Observe que "crédito" e "crédito" são identificadores distintos em C e C++ porque seus casos são diferentes.</span><span class="sxs-lookup"><span data-stu-id="18c34-148">Note that "CREDIT" and "credit" are distinct identifiers in C and C++ because their cases are different.</span></span>


```
#if defined(CREDIT)
    credit();
#elif defined(DEBIT)
    debit();
#else
    printerror();
#endif
```



### <a name="use-of-nested-if-directives"></a><span data-ttu-id="18c34-149">Uso de \# diretivas If aninhadas</span><span class="sxs-lookup"><span data-stu-id="18c34-149">Use of nested \#if directives</span></span>

<span data-ttu-id="18c34-150">O exemplo a seguir mostra como aninhar as \# diretivas If.</span><span class="sxs-lookup"><span data-stu-id="18c34-150">The following example shows how to nest \#if directives.</span></span> <span data-ttu-id="18c34-151">Este exemplo supõe que uma constante simbólica denominada DLEVEL tenha sido definida anteriormente.</span><span class="sxs-lookup"><span data-stu-id="18c34-151">This example assumes that a symbolic constant named DLEVEL has been previously defined.</span></span> <span data-ttu-id="18c34-152">As \# diretivas elif e \# else são usadas para fazer uma das quatro opções, com base no valor de DLEVEL.</span><span class="sxs-lookup"><span data-stu-id="18c34-152">The \#elif and \#else directives are used to make one of four choices, based on the value of DLEVEL.</span></span> <span data-ttu-id="18c34-153">A pilha de constantes é definida como 0, 100 ou 200, dependendo da definição de DLEVEL.</span><span class="sxs-lookup"><span data-stu-id="18c34-153">The constant STACK is set to 0, 100, or 200, depending on the definition of DLEVEL.</span></span> <span data-ttu-id="18c34-154">Se DLEVEL for maior que 5, STACK não será definido.</span><span class="sxs-lookup"><span data-stu-id="18c34-154">If DLEVEL is greater than 5, then STACK is not defined.</span></span>


```
#if DLEVEL > 5
    #define SIGNAL  1
    #if STACKUSE == 1
        #define STACK   200
    #else
        #define STACK   100
    #endif
#else
    #define SIGNAL  0
    #if STACKUSE == 1
        #define STACK   100
    #else
        #define STACK   50
    #endif
#endif
#if DLEVEL == 0
    #define STACK 0
#elif DLEVEL == 1
    #define STACK 100
#elif DLEVEL > 5
    display( debugptr );
#else
    #define STACK 200
#endif
```



### <a name="use-for-including-header-files"></a><span data-ttu-id="18c34-155">Usar para incluir arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="18c34-155">Use for including header files</span></span>

<span data-ttu-id="18c34-156">A compilação condicional é usada normalmente para evitar várias inclusões do mesmo arquivo de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="18c34-156">A common use for conditional compilation is to prevent multiple inclusions of the same header file.</span></span> <span data-ttu-id="18c34-157">Em C++, em que as classes geralmente são definidas em arquivos de cabeçalho, as construções de compilação condicional podem ser usadas para impedir várias definições.</span><span class="sxs-lookup"><span data-stu-id="18c34-157">In C++, where classes are often defined in header files, conditional compilation constructs can be used to prevent multiple definitions.</span></span> <span data-ttu-id="18c34-158">O exemplo a seguir determina se o exemplo de constante simbólico \_ H está definido.</span><span class="sxs-lookup"><span data-stu-id="18c34-158">The following example determines whether the symbolic constant EXAMPLE\_H is defined.</span></span> <span data-ttu-id="18c34-159">Nesse caso, o arquivo já foi incluído e não precisa ser reprocessado; caso contrário, o exemplo de constante \_ H é definido para indicar esse exemplo. H já foi processada.</span><span class="sxs-lookup"><span data-stu-id="18c34-159">If so, the file has already been included and does not need to be reprocessed; if not, the constant EXAMPLE\_H is defined to indicate that EXAMPLE.H has already been processed.</span></span>


```
#if !defined( EXAMPLE_H )
#define EXAMPLE_H

class Example
{
...
};

#endif // !defined( EXAMPLE_H )
```



## <a name="see-also"></a><span data-ttu-id="18c34-160">Confira também</span><span class="sxs-lookup"><span data-stu-id="18c34-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18c34-161">Diretivas de pré-processador (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="18c34-161">Preprocessor Directives (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> </dl>

 

