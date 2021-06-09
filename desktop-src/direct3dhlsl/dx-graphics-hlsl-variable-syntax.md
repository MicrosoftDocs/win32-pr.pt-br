---
title: Sintaxe de Variável
description: Use as seguintes regras de sintaxe para declarar variáveis HLSL.
ms.assetid: 684c42d1-2dd4-42e1-9cff-580edb5c6bcd
keywords:
- extern, sintaxe de variável (DirectX HLSL)
- nointerpolation, sintaxe de variável (DirectX HLSL)
- shared, Variable Syntax (DirectX HLSL)
- groupshared, sintaxe de variável (DirectX HLSL)
- static, Variable Syntax (DirectX HLSL)
- Sintaxe uniforme e variável (DirectX HLSL)
- volatile, Variable Syntax (DirectX HLSL)
- sintaxe precisa e variável (DirectX HLSL)
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 446444e09b0b6aff3e0ba8ca8b12cfbf6dc94128
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/09/2021
ms.locfileid: "111826064"
---
# <a name="variable-syntax"></a><span data-ttu-id="cf8cc-111">Sintaxe de Variável</span><span class="sxs-lookup"><span data-stu-id="cf8cc-111">Variable Syntax</span></span>

<span data-ttu-id="cf8cc-112">Use as seguintes regras de sintaxe para declarar variáveis HLSL.</span><span class="sxs-lookup"><span data-stu-id="cf8cc-112">Use the following syntax rules to declare HLSL variables.</span></span>

<span data-ttu-id="cf8cc-113">\[*Armazenamento \_ Índice* \] \[ *de nome do \_ tipo modificador* \] *de* \[ *tipo de* \] \[ *classe: semântico:* \] \[ *Packoffset:* \] \[ *Register* \] ;    \[  \] Anotações \[ *= Inicial \_ Valor*                    \]</span><span class="sxs-lookup"><span data-stu-id="cf8cc-113">\[*Storage\_Class*\] \[*Type\_Modifier*\] *Type Name*\[*Index*\]     \[*: Semantic*\]     \[*: Packoffset*\]     \[*: Register*\];    \[*Annotations*\]     \[*= Initial\_Value*\]</span></span>



 

## <a name="parameters"></a><span data-ttu-id="cf8cc-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cf8cc-114">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf8cc-115"><span id="Storage_Class_"></span><span id="storage_class_"></span><span id="STORAGE_CLASS_"></span>*Classe de \_ armazenamento*</span><span class="sxs-lookup"><span data-stu-id="cf8cc-115"><span id="Storage_Class_"></span><span id="storage_class_"></span><span id="STORAGE_CLASS_"></span>*Storage\_Class*</span></span> 
</dt> <dd>

<span data-ttu-id="cf8cc-116">Modificadores opcionais de classe de armazenamento que dão ao compilador dicas sobre o escopo e o tempo de vida da variável; os modificadores podem ser especificados em qualquer ordem.</span><span class="sxs-lookup"><span data-stu-id="cf8cc-116">Optional storage-class modifiers that give the compiler hints about variable scope and lifetime; the modifiers can be specified in any order.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cf8cc-117">Valor</span><span class="sxs-lookup"><span data-stu-id="cf8cc-117">Value</span></span></th>
<th><span data-ttu-id="cf8cc-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="cf8cc-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cf8cc-119"><strong>extern</strong></span><span class="sxs-lookup"><span data-stu-id="cf8cc-119"><strong>extern</strong></span></span></td>
<td><span data-ttu-id="cf8cc-120">Marcar uma variável global como uma entrada externa para o sombreador; essa é a marcação padrão para todas as variáveis globais.</span><span class="sxs-lookup"><span data-stu-id="cf8cc-120">Mark a global variable as an external input to the shader; this is the default marking for all global variables.</span></span> <span data-ttu-id="cf8cc-121">Não pode ser combinado com <strong>estático.</strong></span><span class="sxs-lookup"><span data-stu-id="cf8cc-121">Cannot be combined with <strong>static</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf8cc-122"><strong>nointerpolation</strong></span><span class="sxs-lookup"><span data-stu-id="cf8cc-122"><strong>nointerpolation</strong></span></span></td>
<td><span data-ttu-id="cf8cc-123">Não interpole as saídas de um sombreador de vértice antes de passá-las para um sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="cf8cc-123">Do not interpolate the outputs of a vertex shader before passing them to a pixel shader.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf8cc-124"><strong>Preciso</strong></span><span class="sxs-lookup"><span data-stu-id="cf8cc-124"><strong>precise</strong></span></span></td>
<td><span data-ttu-id="cf8cc-125">A <strong>palavra-chave</strong> precisa quando aplicada a uma variável restringirá todos os cálculos usados para produzir o valor atribuído a essa variável das seguintes maneiras:</span><span class="sxs-lookup"><span data-stu-id="cf8cc-125">The <strong>precise</strong> keyword when applied to a variable will restrict any calculations used to produce the value assigned to that variable in the following ways:</span></span>

*   <span data-ttu-id="cf8cc-126">Operações separadas são mantidas separadas.</span><span class="sxs-lookup"><span data-stu-id="cf8cc-126">Separate operations are kept separate.</span></span> <span data-ttu-id="cf8cc-127">Por exemplo, em que uma operação mul e add pode ter sido mesclada em uma operação desarmada, <strong>a</strong> precisão força as operações a permanecerem separadas.</span><span class="sxs-lookup"><span data-stu-id="cf8cc-127">For example, where a mul and add operation might have been fused into a mad operation, <strong>precise</strong> forces the operations to remain separate.</span></span> <span data-ttu-id="cf8cc-128">Em vez disso, você deve usar explicitamente a função intrínseco intrínseco.</span><span class="sxs-lookup"><span data-stu-id="cf8cc-128">Instead, you must explicitly use the mad intrinsic function.</span></span>
*   <span data-ttu-id="cf8cc-129">A ordem das operações é mantida.</span><span class="sxs-lookup"><span data-stu-id="cf8cc-129">Order of operations are maintained.</span></span> <span data-ttu-id="cf8cc-130">Onde a ordem das instruções pode ter sido embaralhada para melhorar o desempenho, <strong>o precisa</strong> garante que o compilador preserve a ordem conforme gravado.</span><span class="sxs-lookup"><span data-stu-id="cf8cc-130">Where the order of instructions might have been shuffled to improve performance, <strong>precise</strong> ensures that the compiler preserves the order as written.</span></span>
*   <span data-ttu-id="cf8cc-131">As operações não seguras do IEEE são restritas.</span><span class="sxs-lookup"><span data-stu-id="cf8cc-131">IEEE unsafe operations are restricted.</span></span> <span data-ttu-id="cf8cc-132">Em que o compilador pode ter usado operações matemáticas rápidas que não são contabilizar valores de NaN (não um número) e INF (infinito), a precisão força os requisitos de IEEE relativos aos valores NaN e INF a serem respeitados. <strong></strong></span><span class="sxs-lookup"><span data-stu-id="cf8cc-132">Where the compiler might have used fast math operations that don't account for NaN (not a number) and INF (infinite) values, <strong>precise</strong> forces IEEE requirements concerning NaN and INF values to be respected.</span></span> <span data-ttu-id="cf8cc-133">Sem <strong>precisão</strong>, essas otimizações e operações matemáticas não são seguras para IEEE.</span><span class="sxs-lookup"><span data-stu-id="cf8cc-133">Without <strong>precise</strong>, these optimizations and mathematical operations are not IEEE safe.</span></span>
*   <span data-ttu-id="cf8cc-134">Qualificar uma variável <strong>precisa</strong> não faz operações que usam a variável <strong>precisa.</strong></span><span class="sxs-lookup"><span data-stu-id="cf8cc-134">Qualifying a variable <strong>precise</strong> doesn't make operations that use the variable <strong>precise</strong>.</span></span> <span data-ttu-id="cf8cc-135">Como <strong></strong> a precisão se propaga apenas para operações que <strong></strong>contribuem para os valores <strong>atribuídos</strong> à variável qualificada de precisão, fazer cálculos desejados com precisão pode ser complicado, portanto, recomendamos marcar as saídas do sombreador diretamente onde você as declara, seja em um campo de estrutura ou em um parâmetro de saída ou o tipo de retorno da função de entrada. <strong></strong></span><span class="sxs-lookup"><span data-stu-id="cf8cc-135">Since <strong>precise</strong> propagates only to operations that contribute to the values that are assigned to the <strong>precise</strong>-qualified variable, correctly making desired calculations <strong>precise</strong> can be tricky, so we recommended that you mark the shader outputs <strong>precise</strong> directly where you declare them, whether that's on a structure field, or on an output parameter, or the return type of the entry function.</span></span>

<span data-ttu-id="cf8cc-136">A capacidade de controlar otimizações dessa maneira mantém a invariância de resultado para a variável de saída modificada desabilitando otimizações que podem afetar os resultados finais devido a diferenças nas diferenças de precisão acumuladas.</span><span class="sxs-lookup"><span data-stu-id="cf8cc-136">The ability to control optimizations in this way maintains result invariance for the modified output variable by disabling optimizations that might affect final results due to differences in accumulated precision differences.</span></span> <span data-ttu-id="cf8cc-137">É útil quando você deseja que sombreadores para mosaico mantenham as marcas de patch com água rígida ou que corresponderem aos valores de profundidade em várias passagens.</span><span class="sxs-lookup"><span data-stu-id="cf8cc-137">It is useful when you want shaders for tessellation to maintain water-tight patch seams or match depth values over multiple passes.</span></span>

<span data-ttu-id="cf8cc-138">[Código de exemplo:](https://github.com/microsoft/DirectXShaderCompiler/blob/master/tools/clang/test/HLSLFileCheck/hlsl/types/modifiers/precise/precise4.hlsl)</span><span class="sxs-lookup"><span data-stu-id="cf8cc-138">[Sample code](https://github.com/microsoft/DirectXShaderCompiler/blob/master/tools/clang/test/HLSLFileCheck/hlsl/types/modifiers/precise/precise4.hlsl):</span></span> 
```HLSL
matrix g_mWorldViewProjection;
void main(in float3 InPos : Position, out precise float4 OutPos : SV_Position)
{
  // operation is precise because it contributes to the precise parameter OutPos
  OutPos = mul( float4( InPos, 1.0 ), g_mWorldViewProjection );
}
```
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf8cc-139"><strong>Compartilhado</strong></span><span class="sxs-lookup"><span data-stu-id="cf8cc-139"><strong>shared</strong></span></span></td>
<td><span data-ttu-id="cf8cc-140">Marcar uma variável para compartilhamento entre efeitos; essa é uma dica para o compilador.</span><span class="sxs-lookup"><span data-stu-id="cf8cc-140">Mark a variable for sharing between effects; this is a hint to the compiler.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf8cc-141"><strong>groupshared</strong></span><span class="sxs-lookup"><span data-stu-id="cf8cc-141"><strong>groupshared</strong></span></span></td>
<td><span data-ttu-id="cf8cc-142">Marque uma variável para memória compartilhada de grupo de threads para sombreadores de computação.</span><span class="sxs-lookup"><span data-stu-id="cf8cc-142">Mark a variable for thread-group-shared memory for compute shaders.</span></span> <span data-ttu-id="cf8cc-143">Em D3D10, o tamanho total máximo de todas as variáveis com a classe de armazenamento groupshared é de 16kb; em D3D11, o tamanho máximo é 32kb.</span><span class="sxs-lookup"><span data-stu-id="cf8cc-143">In D3D10 the maximum total size of all variables with the groupshared storage class is 16kb, in D3D11 the maximum size is 32kb.</span></span> <span data-ttu-id="cf8cc-144">Veja exemplos.</span><span class="sxs-lookup"><span data-stu-id="cf8cc-144">See examples.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf8cc-145"><strong>static</strong></span><span class="sxs-lookup"><span data-stu-id="cf8cc-145"><strong>static</strong></span></span></td>
<td><span data-ttu-id="cf8cc-146">Marque uma variável local para que ela seja inicializada uma vez e persista entre chamadas de função.</span><span class="sxs-lookup"><span data-stu-id="cf8cc-146">Mark a local variable so that it is initialized one time and persists between function calls.</span></span> <span data-ttu-id="cf8cc-147">Se a declaração não incluir um inicializador, o valor será definido como zero.</span><span class="sxs-lookup"><span data-stu-id="cf8cc-147">If the declaration does not include an initializer, the value is set to zero.</span></span> <span data-ttu-id="cf8cc-148">Uma variável global marcada <strong>como estática</strong> não é visível para um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="cf8cc-148">A global variable marked <strong>static</strong> is not visible to an application.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf8cc-149"><strong>uniforme</strong></span><span class="sxs-lookup"><span data-stu-id="cf8cc-149"><strong>uniform</strong></span></span></td>
<td><span data-ttu-id="cf8cc-150">Marque uma variável cujos dados são constantes durante a execução de um sombreador (como uma cor de material em um sombreador de vértice); as variáveis globais são <strong>consideradas uniformes</strong> por padrão.</span><span class="sxs-lookup"><span data-stu-id="cf8cc-150">Mark a variable whose data is constant throughout the execution of a shader (such as a material color in a vertex shader); global variables are considered <strong>uniform</strong> by default.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf8cc-151"><strong>volatile</strong></span><span class="sxs-lookup"><span data-stu-id="cf8cc-151"><strong>volatile</strong></span></span></td>
<td><span data-ttu-id="cf8cc-152">Marcar uma variável que muda com frequência; essa é uma dica para o compilador.</span><span class="sxs-lookup"><span data-stu-id="cf8cc-152">Mark a variable that changes frequently; this is a hint to the compiler.</span></span> <span data-ttu-id="cf8cc-153">Esse modificador de classe de armazenamento se aplica somente a uma variável local.</span><span class="sxs-lookup"><span data-stu-id="cf8cc-153">This storage class modifier only applies to a local variable.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="cf8cc-154">Atualmente, o compilador HLSL ignora esse modificador de classe de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="cf8cc-154">The HLSL compiler currently ignores this storage class modifier.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="cf8cc-155"><span id="Type_Modifier"></span><span id="type_modifier"></span><span id="TYPE_MODIFIER"></span>*Modificador \_ de tipo*</span><span class="sxs-lookup"><span data-stu-id="cf8cc-155"><span id="Type_Modifier"></span><span id="type_modifier"></span><span id="TYPE_MODIFIER"></span>*Type\_Modifier*</span></span>
</dt> <dd>

<span data-ttu-id="cf8cc-156">Modificador de tipo variável opcional.</span><span class="sxs-lookup"><span data-stu-id="cf8cc-156">Optional variable-type modifier.</span></span>



| <span data-ttu-id="cf8cc-157">Valor</span><span class="sxs-lookup"><span data-stu-id="cf8cc-157">Value</span></span>             | <span data-ttu-id="cf8cc-158">Descrição</span><span class="sxs-lookup"><span data-stu-id="cf8cc-158">Description</span></span>                                                                                                                                                                                                                                  |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf8cc-159">**const**</span><span class="sxs-lookup"><span data-stu-id="cf8cc-159">**const**</span></span>         | <span data-ttu-id="cf8cc-160">Marque uma variável que não pode ser alterada por um sombreador, portanto, ela deve ser inicializada na declaração de variável.</span><span class="sxs-lookup"><span data-stu-id="cf8cc-160">Mark a variable that cannot be changed by a shader, therefore, it must be initialized in the variable declaration.</span></span> <span data-ttu-id="cf8cc-161">As variáveis globais são **consideradas const** por padrão (suprir esse comportamento fornecendo o sinalizador /Gec ao compilador).</span><span class="sxs-lookup"><span data-stu-id="cf8cc-161">Global variables are considered **const** by default (suppress this behavior by supplying the /Gec flag to the compiler).</span></span> |
| <span data-ttu-id="cf8cc-162">**row \_ major**</span><span class="sxs-lookup"><span data-stu-id="cf8cc-162">**row\_major**</span></span>    | <span data-ttu-id="cf8cc-163">Marque uma variável que armazena quatro componentes em uma única linha para que possam ser armazenados em um único registro constante.</span><span class="sxs-lookup"><span data-stu-id="cf8cc-163">Mark a variable that stores four components in a single row so they can be stored in a single constant register.</span></span>                                                                                                                             |
| <span data-ttu-id="cf8cc-164">**coluna \_ principal**</span><span class="sxs-lookup"><span data-stu-id="cf8cc-164">**column\_major**</span></span> | <span data-ttu-id="cf8cc-165">Marque uma variável que armazena quatro componentes em uma única coluna para otimizar a matemática da matriz.</span><span class="sxs-lookup"><span data-stu-id="cf8cc-165">Mark a variable that stores 4 components in a single column to optimize matrix math.</span></span>                                                                                                                                                         |



 

> [!Note]  
> <span data-ttu-id="cf8cc-166">Se você não especificar um valor modificador de tipo, o compilador usará **a coluna \_ principal** como o valor padrão.</span><span class="sxs-lookup"><span data-stu-id="cf8cc-166">If you do not specify a type-modifier value, the compiler uses **column\_major** as the default value.</span></span>

 

</dd> <dt>

<span data-ttu-id="cf8cc-167"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>*Tipo*</span><span class="sxs-lookup"><span data-stu-id="cf8cc-167"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>*Type*</span></span>
</dt> <dd>

<span data-ttu-id="cf8cc-168">Qualquer tipo HLSL listado em [Tipos de Dados (DirectX HLSL)](dx-graphics-hlsl-data-types.md).</span><span class="sxs-lookup"><span data-stu-id="cf8cc-168">Any HLSL type listed in [Data Types (DirectX HLSL)](dx-graphics-hlsl-data-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="cf8cc-169"><span id="Name_Index_"></span><span id="name_index_"></span><span id="NAME_INDEX_"></span>*Nome* \[ *Índice*\]</span><span class="sxs-lookup"><span data-stu-id="cf8cc-169"><span id="Name_Index_"></span><span id="name_index_"></span><span id="NAME_INDEX_"></span>*Name*\[*Index*\]</span></span>
</dt> <dd>

<span data-ttu-id="cf8cc-170">Cadeia de caracteres ASCII que identifica exclusivamente uma variável de sombreador.</span><span class="sxs-lookup"><span data-stu-id="cf8cc-170">ASCII string that uniquely identifies a shader variable.</span></span> <span data-ttu-id="cf8cc-171">Para definir uma matriz opcional, use **o índice para** o tamanho da matriz, que é um inteiro positivo = 1.</span><span class="sxs-lookup"><span data-stu-id="cf8cc-171">To define an optional array, use **index** for the array size, which is a positive integer = 1.</span></span>

</dd> <dt>

<span data-ttu-id="cf8cc-172"><span id="Semantic"></span><span id="semantic"></span><span id="SEMANTIC"></span>*Semântica*</span><span class="sxs-lookup"><span data-stu-id="cf8cc-172"><span id="Semantic"></span><span id="semantic"></span><span id="SEMANTIC"></span>*Semantic*</span></span>
</dt> <dd>

<span data-ttu-id="cf8cc-173">Informações opcionais de uso de parâmetro, usadas pelo compilador para vincular entradas e saídas do sombreador.</span><span class="sxs-lookup"><span data-stu-id="cf8cc-173">Optional parameter-usage information, used by the compiler to link shader inputs and outputs.</span></span> <span data-ttu-id="cf8cc-174">Há várias semânticas [predefinida](dx-graphics-hlsl-semantics.md) para sombreadores de vértice e pixel.</span><span class="sxs-lookup"><span data-stu-id="cf8cc-174">There are several predefined [semantics](dx-graphics-hlsl-semantics.md) for vertex and pixel shaders.</span></span> <span data-ttu-id="cf8cc-175">O compilador ignora a semântica, a menos que elas sejam declaradas em uma variável global ou um parâmetro passado para um sombreador.</span><span class="sxs-lookup"><span data-stu-id="cf8cc-175">The compiler ignores semantics unless they are declared on a global variable, or a parameter passed into a shader.</span></span>

</dd> <dt>

<span data-ttu-id="cf8cc-176"><span id="Packoffset"></span><span id="packoffset"></span><span id="PACKOFFSET"></span>*Packoffset*</span><span class="sxs-lookup"><span data-stu-id="cf8cc-176"><span id="Packoffset"></span><span id="packoffset"></span><span id="PACKOFFSET"></span>*Packoffset*</span></span>
</dt> <dd>

<span data-ttu-id="cf8cc-177">Palavra-chave opcional para empacotar manualmente as constantes do sombreador.</span><span class="sxs-lookup"><span data-stu-id="cf8cc-177">Optional keyword for manually packing shader constants.</span></span> <span data-ttu-id="cf8cc-178">Consulte [packoffset (DirectX HLSL)](dx-graphics-hlsl-variable-packoffset.md).</span><span class="sxs-lookup"><span data-stu-id="cf8cc-178">See [packoffset (DirectX HLSL)](dx-graphics-hlsl-variable-packoffset.md).</span></span>

</dd> <dt>

<span data-ttu-id="cf8cc-179"><span id="Register"></span><span id="register"></span><span id="REGISTER"></span>*Registrar*</span><span class="sxs-lookup"><span data-stu-id="cf8cc-179"><span id="Register"></span><span id="register"></span><span id="REGISTER"></span>*Register*</span></span>
</dt> <dd>

<span data-ttu-id="cf8cc-180">Palavra-chave opcional para atribuir manualmente uma variável de sombreador a um registro específico.</span><span class="sxs-lookup"><span data-stu-id="cf8cc-180">Optional keyword for manually assigning a shader variable to a particular register.</span></span> <span data-ttu-id="cf8cc-181">Consulte [register (DirectX HLSL)](dx-graphics-hlsl-variable-register.md).</span><span class="sxs-lookup"><span data-stu-id="cf8cc-181">See [register (DirectX HLSL)](dx-graphics-hlsl-variable-register.md).</span></span>

</dd> <dt>

<span data-ttu-id="cf8cc-182"><span id="Annotation_s_"></span><span id="annotation_s_"></span><span id="ANNOTATION_S_"></span>*Anotações*</span><span class="sxs-lookup"><span data-stu-id="cf8cc-182"><span id="Annotation_s_"></span><span id="annotation_s_"></span><span id="ANNOTATION_S_"></span>*Annotation(s)*</span></span>
</dt> <dd>

<span data-ttu-id="cf8cc-183">Metadados opcionais, na forma de uma cadeia de caracteres, anexados a uma variável global.</span><span class="sxs-lookup"><span data-stu-id="cf8cc-183">Optional metadata, in the form of a string, attached to a global variable.</span></span> <span data-ttu-id="cf8cc-184">Uma anotação é usada pela estrutura de efeito e ignorada por HLSL; para ver uma sintaxe mais detalhada, consulte [sintaxe de anotação](/windows/desktop/direct3d10/d3d10-effect-annotation-syntax).</span><span class="sxs-lookup"><span data-stu-id="cf8cc-184">An annotation is used by the effect framework and ignored by HLSL; to see more detailed syntax, see [annotation syntax](/windows/desktop/direct3d10/d3d10-effect-annotation-syntax).</span></span>

</dd> <dt>

<span data-ttu-id="cf8cc-185"><span id="Initial_Value"></span><span id="initial_value"></span><span id="INITIAL_VALUE"></span>*Valor \_ inicial*</span><span class="sxs-lookup"><span data-stu-id="cf8cc-185"><span id="Initial_Value"></span><span id="initial_value"></span><span id="INITIAL_VALUE"></span>*Initial\_Value*</span></span>
</dt> <dd>

<span data-ttu-id="cf8cc-186">Valores iniciais opcionais; o número de valores deve corresponder ao número de componentes no *Tipo*.</span><span class="sxs-lookup"><span data-stu-id="cf8cc-186">Optional initial value(s); the number of values should match the number of components in *Type*.</span></span> <span data-ttu-id="cf8cc-187">Cada variável global marcada **como extern** deve ser inicializada com um valor literal; cada variável **marcada como estática** deve ser inicializada com uma constante.</span><span class="sxs-lookup"><span data-stu-id="cf8cc-187">Each global variable marked **extern** must be initialized with a literal value; each variable marked **static** must be initialized with a constant.</span></span>

<span data-ttu-id="cf8cc-188">As variáveis globais que não estão **marcadas como** estáticas ou **extern** não são compiladas no sombreador.</span><span class="sxs-lookup"><span data-stu-id="cf8cc-188">Global variables that are not marked **static** or **extern** are not compiled into the shader.</span></span> <span data-ttu-id="cf8cc-189">O compilador não configura automaticamente valores padrão para variáveis globais e não pode usá-los em otimizações.</span><span class="sxs-lookup"><span data-stu-id="cf8cc-189">The compiler does not automatically set default values for global variables and cannot use them in optimizations.</span></span> <span data-ttu-id="cf8cc-190">Para inicializar esse tipo de variável global, use reflexão para obter seu valor e, em seguida, copie o valor para um buffer constante.</span><span class="sxs-lookup"><span data-stu-id="cf8cc-190">To initialize this type of global variable, use reflection to get its value and then copy the value to a constant buffer.</span></span> <span data-ttu-id="cf8cc-191">Por exemplo, você pode usar o método [**ID3D11ShaderReflection::GetVariableByName**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflection-getvariablebyname) para obter a variável, usar o método [**ID3D11ShaderReflectionVariable::GetDesc**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflectionvariable-getdesc) para obter a descrição da variável de sombreador e obter o valor inicial do membro **DefaultValue** da estrutura [**D3D11 \_ SHADER \_ VARIABLE \_ DESC.**](/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_shader_variable_desc)</span><span class="sxs-lookup"><span data-stu-id="cf8cc-191">For example, you can use the [**ID3D11ShaderReflection::GetVariableByName**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflection-getvariablebyname) method to get the variable, use the [**ID3D11ShaderReflectionVariable::GetDesc**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflectionvariable-getdesc) method to get the shader-variable description, and get the initial value from the **DefaultValue** member of the [**D3D11\_SHADER\_VARIABLE\_DESC**](/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_shader_variable_desc) structure.</span></span> <span data-ttu-id="cf8cc-192">Para copiar o valor para o buffer constante, você deve garantir que o buffer foi criado com acesso de gravação da CPU ([**D3D11 \_ CPU \_ ACCESS \_ WRITE).**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_cpu_access_flag)</span><span class="sxs-lookup"><span data-stu-id="cf8cc-192">To copy the value to the constant buffer, you must ensure that the buffer was created with CPU write access ([**D3D11\_CPU\_ACCESS\_WRITE**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_cpu_access_flag)).</span></span> <span data-ttu-id="cf8cc-193">Para obter mais informações sobre como criar um buffer constante, consulte [Como criar um buffer constante.](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-constant-how-to)</span><span class="sxs-lookup"><span data-stu-id="cf8cc-193">For more information about how to create a constant buffer, see [How to: Create a Constant Buffer](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-constant-how-to).</span></span>

<span data-ttu-id="cf8cc-194">Você também pode usar a estrutura [de efeitos](../direct3d11/d3d11-graphics-programming-guide-effects.md) para processar automaticamente o refletindo e definindo o valor inicial.</span><span class="sxs-lookup"><span data-stu-id="cf8cc-194">You can also use the [effects framework](../direct3d11/d3d11-graphics-programming-guide-effects.md) to automatically process the reflecting and setting the initial value.</span></span> <span data-ttu-id="cf8cc-195">Por exemplo, você pode usar o [**método ID3DX11EffectPass::Apply.**](/windows/desktop/direct3d11/id3dx11effectpass-apply)</span><span class="sxs-lookup"><span data-stu-id="cf8cc-195">For example, you can use the [**ID3DX11EffectPass::Apply**](/windows/desktop/direct3d11/id3dx11effectpass-apply) method.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="cf8cc-196">Exemplos</span><span class="sxs-lookup"><span data-stu-id="cf8cc-196">Examples</span></span>

<span data-ttu-id="cf8cc-197">Aqui estão vários exemplos de declarações de variável de sombreador.</span><span class="sxs-lookup"><span data-stu-id="cf8cc-197">Here are several examples of shader-variable declarations.</span></span>


```
float fVar;
```




```
float4 color;
float fVar = 3.1f;

int iVar[3];

int iVar[3] = {1,2,3};

uniform float4 position : SV_POSITION; 
const float4 lightDirection = {0,0,1};
      
```



### <a name="group-shared"></a><span data-ttu-id="cf8cc-198">Grupo Compartilhado</span><span class="sxs-lookup"><span data-stu-id="cf8cc-198">Group Shared</span></span>

<span data-ttu-id="cf8cc-199">O HLSL permite que threads de um sombreador de computação troquem valores por meio de memória compartilhada.</span><span class="sxs-lookup"><span data-stu-id="cf8cc-199">HLSL enables threads of a compute shader to exchange values via shared memory.</span></span> <span data-ttu-id="cf8cc-200">O HLSL fornece primitivos de barreira, como [**GroupMemoryBaoryWithGroupSync**](groupmemorybarrierwithgroupsync.md)e assim por diante, para garantir a ordenação correta de leituras e gravações na memória compartilhada no sombreador e evitar a corrida de dados.</span><span class="sxs-lookup"><span data-stu-id="cf8cc-200">HLSL provides barrier primitives such as [**GroupMemoryBarrierWithGroupSync**](groupmemorybarrierwithgroupsync.md), and so on to ensure the correct ordering of reads and writes to shared memory in the shader and to avoid data races.</span></span>

> [!Note]  
> <span data-ttu-id="cf8cc-201">O hardware executa threads em grupos (warpes ou ondulados) e a sincronização de barreira, às vezes, pode ser omitida para aumentar o desempenho quando apenas os threads que pertencem ao mesmo grupo estão corretos.</span><span class="sxs-lookup"><span data-stu-id="cf8cc-201">Hardware executes threads in groups (warps or wave-fronts), and barrier synchronization can sometimes be omitted to increase performance when only synchronizing threads that belong to the same group is correct.</span></span> <span data-ttu-id="cf8cc-202">Mas não é altamente recomendável essa omissão por esses motivos:</span><span class="sxs-lookup"><span data-stu-id="cf8cc-202">But we highly discourage this omission for these reasons:</span></span>
>
> -   <span data-ttu-id="cf8cc-203">Essa omissão resulta em código não portátil, que pode não funcionar em algum hardware e não funciona em rasterizadores de software que normalmente executam threads em grupos menores.</span><span class="sxs-lookup"><span data-stu-id="cf8cc-203">This omission results in non-portable code, which might not work on some hardware and doesn't work on software rasterizers that typically execute threads in smaller groups.</span></span>
> -   <span data-ttu-id="cf8cc-204">As melhorias de desempenho que você pode atingir com essa omissão serão pequenas em comparação com a barreira de todos os threads.</span><span class="sxs-lookup"><span data-stu-id="cf8cc-204">The performance improvements that you might achieve with this omission will be minor compared to using all-thread barrier.</span></span>

 

<span data-ttu-id="cf8cc-205">No Direct3D 10 não há sincronização de threads ao gravar em **groupshared**, portanto, isso significa que cada thread é limitado a um único local em uma matriz para gravação.</span><span class="sxs-lookup"><span data-stu-id="cf8cc-205">In Direct3D 10 there is no synchronization of threads when writing to **groupshared**, so this means that each thread is limited to a single location in an array for writing.</span></span> <span data-ttu-id="cf8cc-206">Use o valor do sistema [ \_ GroupIndex VA](dx-graphics-hlsl-semantics.md) para indexar nessa matriz ao gravar para garantir que dois threads possam colidir.</span><span class="sxs-lookup"><span data-stu-id="cf8cc-206">Use the [SV\_GroupIndex](dx-graphics-hlsl-semantics.md) system value to index into this array when writing to ensure that no two threads can collide.</span></span> <span data-ttu-id="cf8cc-207">Em termos de leitura, todos os threads têm acesso a toda a matriz para leitura.</span><span class="sxs-lookup"><span data-stu-id="cf8cc-207">In terms of reading, all threads have access to the entire array for reading.</span></span>


```
struct GSData
{
    float4 Color;
    float Factor;
}

groupshared GSData data[5*5*1];

[numthreads(5,5,1)]
void main( uint index : SV_GroupIndex )
{
    data[index].Color = (float4)0;
    data[index].Factor = 2.0f;
    GroupMemoryBarrierWithGroupSync();
    ...
}
```



### <a name="packing"></a><span data-ttu-id="cf8cc-208">Recibo</span><span class="sxs-lookup"><span data-stu-id="cf8cc-208">Packing</span></span>

<span data-ttu-id="cf8cc-209">Pacotes subcomponentes de vetores e escalares cujo tamanho é grande o suficiente para evitar o cruzamento dos limites de registro.</span><span class="sxs-lookup"><span data-stu-id="cf8cc-209">Pack subcomponents of vectors and scalars whose size is large enough to prevent crossing register boundarys.</span></span> <span data-ttu-id="cf8cc-210">Por exemplo, todos eles são válidos:</span><span class="sxs-lookup"><span data-stu-id="cf8cc-210">For example, these are all valid:</span></span>


```
cbuffer MyBuffer
{
    float4 Element1 : packoffset(c0);
    float1 Element2 : packoffset(c1);
    float1 Element3 : packoffset(c1.y);
}
        
```



<span data-ttu-id="cf8cc-211">Não é possível misturar tipos de empacotamento.</span><span class="sxs-lookup"><span data-stu-id="cf8cc-211">Cannot mix packing types.</span></span>

<span data-ttu-id="cf8cc-212">Assim como a palavra-chave Register, um packoffset pode ser específico de destino.</span><span class="sxs-lookup"><span data-stu-id="cf8cc-212">Like the register keyword, a packoffset can be target specific.</span></span> <span data-ttu-id="cf8cc-213">A embalagem do subcomponente só está disponível com a palavra-chave packoffset, não a palavra-chave Register.</span><span class="sxs-lookup"><span data-stu-id="cf8cc-213">Subcomponent packing is only available with the packoffset keyword, not the register keyword.</span></span> <span data-ttu-id="cf8cc-214">Dentro de uma declaração CBuffer, a palavra-chave Register é ignorada para destinos do Direct3D 10, pois ela é considerada para compatibilidade entre plataformas.</span><span class="sxs-lookup"><span data-stu-id="cf8cc-214">Inside a cbuffer declaration, the register keyword is ignored for Direct3D 10 targets as it is assumed to be for cross-platform compatibility.</span></span>

<span data-ttu-id="cf8cc-215">Elementos empacotados podem se sobrepor e o compilador não apresentará nenhum erro ou aviso.</span><span class="sxs-lookup"><span data-stu-id="cf8cc-215">Packed elements may overlap and the compiler will give no error or warning.</span></span> <span data-ttu-id="cf8cc-216">Neste exemplo, Element2 e Element3 serão sobrepostas com Element1. x e Element1. y.</span><span class="sxs-lookup"><span data-stu-id="cf8cc-216">In this example, Element2 and Element3 will overlap with Element1.x and Element1.y.</span></span>


```
cbuffer MyBuffer
{
    float4 Element1 : packoffset(c0);
    float1 Element2 : packoffset(c0);
    float1 Element3 : packoffset(c0.y);
}
        
```



<span data-ttu-id="cf8cc-217">Um exemplo que usa packoffset é: [HLSLWithoutFX10 Sample](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="cf8cc-217">A sample that uses packoffset is: [HLSLWithoutFX10 Sample](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx).</span></span>

## <a name="related-topics"></a><span data-ttu-id="cf8cc-218">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="cf8cc-218">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cf8cc-219">Variáveis (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="cf8cc-219">Variables (DirectX HLSL)</span></span>](dx-graphics-hlsl-variables.md)
</dt> </dl>

 

