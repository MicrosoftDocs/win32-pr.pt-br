---
title: Sintaxe de Variável
description: Use as regras de sintaxe a seguir para declarar variáveis HLSL.
ms.assetid: 684c42d1-2dd4-42e1-9cff-580edb5c6bcd
keywords:
- externo, sintaxe de variável (DirectX HLSL)
- nointerpolação, sintaxe de variável (DirectX HLSL)
- Sintaxe compartilhada, variável (DirectX HLSL)
- groupshared, sintaxe de variável (DirectX HLSL)
- Sintaxe estática, variável (DirectX HLSL)
- Sintaxe uniforme e variável (DirectX HLSL)
- volátil, sintaxe de variável (DirectX HLSL)
- Sintaxe precisa, variável (DirectX HLSL)
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f6e63bafa62a9857af678e0848c81237dcd0d585
ms.sourcegitcommit: 4e0bde7dfa48a0b60bca4a5230eb2b05be3778d3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/11/2020
ms.locfileid: "104988724"
---
# <a name="variable-syntax"></a><span data-ttu-id="325fd-111">Sintaxe de Variável</span><span class="sxs-lookup"><span data-stu-id="325fd-111">Variable Syntax</span></span>

<span data-ttu-id="325fd-112">Use as regras de sintaxe a seguir para declarar variáveis HLSL.</span><span class="sxs-lookup"><span data-stu-id="325fd-112">Use the following syntax rules to declare HLSL variables.</span></span>



|                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="325fd-113">\[*Armazenamento \_ do Tipo de classe* \] \[ *\_ modificador* \] *nome* \[ *índice* \] \[ *: semântica* \] \[ *: Packoffset* \] \[ *: registrar* \] ;    \[  \] Anotações \[ *= Inicial \_ Valor* do                    \]</span><span class="sxs-lookup"><span data-stu-id="325fd-113">\[*Storage\_Class*\] \[*Type\_Modifier*\] *Type Name*\[*Index*\]     \[*: Semantic*\]     \[*: Packoffset*\]     \[*: Register*\];    \[*Annotations*\]     \[*= Initial\_Value*\]</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="325fd-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="325fd-114">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="325fd-115"><span id="Storage_Class_"></span><span id="storage_class_"></span><span id="STORAGE_CLASS_"></span>*Classe de armazenamento \_*</span><span class="sxs-lookup"><span data-stu-id="325fd-115"><span id="Storage_Class_"></span><span id="storage_class_"></span><span id="STORAGE_CLASS_"></span>*Storage\_Class*</span></span> 
</dt> <dd>

<span data-ttu-id="325fd-116">Modificadores de classe de armazenamento opcionais que fornecem dicas de compilador sobre escopo de variável e tempo de vida; os modificadores podem ser especificados em qualquer ordem.</span><span class="sxs-lookup"><span data-stu-id="325fd-116">Optional storage-class modifiers that give the compiler hints about variable scope and lifetime; the modifiers can be specified in any order.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="325fd-117">Valor</span><span class="sxs-lookup"><span data-stu-id="325fd-117">Value</span></span></th>
<th><span data-ttu-id="325fd-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="325fd-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="325fd-119"><strong>extern</strong></span><span class="sxs-lookup"><span data-stu-id="325fd-119"><strong>extern</strong></span></span></td>
<td><span data-ttu-id="325fd-120">Marcar uma variável global como uma entrada externa para o sombreador; Essa é a marcação padrão para todas as variáveis globais.</span><span class="sxs-lookup"><span data-stu-id="325fd-120">Mark a global variable as an external input to the shader; this is the default marking for all global variables.</span></span> <span data-ttu-id="325fd-121">Não pode ser combinado com <strong>static</strong>.</span><span class="sxs-lookup"><span data-stu-id="325fd-121">Cannot be combined with <strong>static</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="325fd-122"><strong>nointerpolação</strong></span><span class="sxs-lookup"><span data-stu-id="325fd-122"><strong>nointerpolation</strong></span></span></td>
<td><span data-ttu-id="325fd-123">Não interpolar as saídas de um sombreador de vértice antes de passá-las para um sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="325fd-123">Do not interpolate the outputs of a vertex shader before passing them to a pixel shader.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="325fd-124"><strong>Precisas</strong></span><span class="sxs-lookup"><span data-stu-id="325fd-124"><strong>precise</strong></span></span></td>
<td><span data-ttu-id="325fd-125">A palavra-chave <strong>precisa</strong> quando aplicada a uma variável restringirá quaisquer cálculos usados para produzir o valor atribuído a essa variável das seguintes maneiras:</span><span class="sxs-lookup"><span data-stu-id="325fd-125">The <strong>precise</strong> keyword when applied to a variable will restrict any calculations used to produce the value assigned to that variable in the following ways:</span></span>

*   <span data-ttu-id="325fd-126">Operações separadas são mantidas separadas.</span><span class="sxs-lookup"><span data-stu-id="325fd-126">Separate operations are kept separate.</span></span> <span data-ttu-id="325fd-127">Por exemplo, onde um Mul e uma operação de adição podem ter sido fundidos em uma operação Mad, a <strong>precisão</strong> força as operações a permanecerem separadas.</span><span class="sxs-lookup"><span data-stu-id="325fd-127">For example, where a mul and add operation might have been fused into a mad operation, <strong>precise</strong> forces the operations to remain separate.</span></span> <span data-ttu-id="325fd-128">Em vez disso, você deve usar explicitamente a função intrínseca Mad.</span><span class="sxs-lookup"><span data-stu-id="325fd-128">Instead, you must explicitly use the mad intrinsic function.</span></span>
*   <span data-ttu-id="325fd-129">A ordem das operações é mantida.</span><span class="sxs-lookup"><span data-stu-id="325fd-129">Order of operations are maintained.</span></span> <span data-ttu-id="325fd-130">Onde a ordem das instruções pode ter sido embaralhada para melhorar o desempenho, a <strong>precisão</strong> garante que o compilador preserve o pedido como escrito.</span><span class="sxs-lookup"><span data-stu-id="325fd-130">Where the order of instructions might have been shuffled to improve performance, <strong>precise</strong> ensures that the compiler preserves the order as written.</span></span>
*   <span data-ttu-id="325fd-131">As operações IEEE não seguras são restritas.</span><span class="sxs-lookup"><span data-stu-id="325fd-131">IEEE unsafe operations are restricted.</span></span> <span data-ttu-id="325fd-132">Onde o compilador pode ter usado operações matemáticas rápidas que não contenham valores NaN (não um número) e INF (infinitos), <strong>preciso</strong> força os requisitos de IEEE relacionados a valores Nan e inf a serem respeitados.</span><span class="sxs-lookup"><span data-stu-id="325fd-132">Where the compiler might have used fast math operations that don't account for NaN (not a number) and INF (infinite) values, <strong>precise</strong> forces IEEE requirements concerning NaN and INF values to be respected.</span></span> <span data-ttu-id="325fd-133">Sem <strong>precisa</strong>, essas otimizações e operações matemáticas não são seguras para IEEE.</span><span class="sxs-lookup"><span data-stu-id="325fd-133">Without <strong>precise</strong>, these optimizations and mathematical operations are not IEEE safe.</span></span>
*   <span data-ttu-id="325fd-134">A qualificação de uma variável <strong>precisa</strong> não faz com que as operações usem a variável <strong>precisa</strong>.</span><span class="sxs-lookup"><span data-stu-id="325fd-134">Qualifying a variable <strong>precise</strong> doesn't make operations that use the variable <strong>precise</strong>.</span></span> <span data-ttu-id="325fd-135">Como a propagação <strong>precisa</strong> apenas para as operações que contribuem com os valores atribuídos à variável qualificada com <strong>precisão</strong>, fazer <strong>os cálculos</strong> desejados corretamente pode ser complicado, portanto, recomendamos que você marque as saídas de sombreador de forma <strong>precisa</strong> diretamente onde declará-las, sejam elas em um campo de estrutura, ou em um parâmetro de saída, ou o tipo de retorno da função de entrada.</span><span class="sxs-lookup"><span data-stu-id="325fd-135">Since <strong>precise</strong> propagates only to operations that contribute to the values that are assigned to the <strong>precise</strong>-qualified variable, correctly making desired calculations <strong>precise</strong> can be tricky, so we recommended that you mark the shader outputs <strong>precise</strong> directly where you declare them, whether that's on a structure field, or on an output parameter, or the return type of the entry function.</span></span>

<span data-ttu-id="325fd-136">A capacidade de controlar otimizações dessa maneira mantém a invariação de resultado da variável de saída modificada desabilitando otimizações que podem afetar os resultados finais devido a diferenças nas diferenças de precisão acumuladas.</span><span class="sxs-lookup"><span data-stu-id="325fd-136">The ability to control optimizations in this way maintains result invariance for the modified output variable by disabling optimizations that might affect final results due to differences in accumulated precision differences.</span></span> <span data-ttu-id="325fd-137">É útil quando você deseja que os sombreadores para mosaico mantenham emendas de patches de água rígida ou valores de profundidade de correspondência em várias passagens.</span><span class="sxs-lookup"><span data-stu-id="325fd-137">It is useful when you want shaders for tessellation to maintain water-tight patch seams or match depth values over multiple passes.</span></span>

<span data-ttu-id="325fd-138">[Código de exemplo](https://github.com/microsoft/DirectXShaderCompiler/blob/master/tools/clang/test/HLSLFileCheck/hlsl/types/modifiers/precise/precise4.hlsl):</span><span class="sxs-lookup"><span data-stu-id="325fd-138">[Sample code](https://github.com/microsoft/DirectXShaderCompiler/blob/master/tools/clang/test/HLSLFileCheck/hlsl/types/modifiers/precise/precise4.hlsl):</span></span> 
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
<td><span data-ttu-id="325fd-139"><strong>compartilhado</strong></span><span class="sxs-lookup"><span data-stu-id="325fd-139"><strong>shared</strong></span></span></td>
<td><span data-ttu-id="325fd-140">Marcar uma variável para compartilhamento entre os efeitos; Esta é uma dica para o compilador.</span><span class="sxs-lookup"><span data-stu-id="325fd-140">Mark a variable for sharing between effects; this is a hint to the compiler.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="325fd-141"><strong>groupshared</strong></span><span class="sxs-lookup"><span data-stu-id="325fd-141"><strong>groupshared</strong></span></span></td>
<td><span data-ttu-id="325fd-142">Marque uma variável para a memória compartilhada do grupo de threads para sombreadores de computação.</span><span class="sxs-lookup"><span data-stu-id="325fd-142">Mark a variable for thread-group-shared memory for compute shaders.</span></span> <span data-ttu-id="325fd-143">Em D3D10, o tamanho total máximo de todas as variáveis com a classe de armazenamento groupshared é 16 KB, em D3D11 o tamanho máximo é 32 KB.</span><span class="sxs-lookup"><span data-stu-id="325fd-143">In D3D10 the maximum total size of all variables with the groupshared storage class is 16kb, in D3D11 the maximum size is 32kb.</span></span> <span data-ttu-id="325fd-144">Consulte exemplos.</span><span class="sxs-lookup"><span data-stu-id="325fd-144">See examples.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="325fd-145"><strong>static</strong></span><span class="sxs-lookup"><span data-stu-id="325fd-145"><strong>static</strong></span></span></td>
<td><span data-ttu-id="325fd-146">Marque uma variável local para que ela seja inicializada uma vez e persiste entre as chamadas de função.</span><span class="sxs-lookup"><span data-stu-id="325fd-146">Mark a local variable so that it is initialized one time and persists between function calls.</span></span> <span data-ttu-id="325fd-147">Se a declaração não incluir um inicializador, o valor será definido como zero.</span><span class="sxs-lookup"><span data-stu-id="325fd-147">If the declaration does not include an initializer, the value is set to zero.</span></span> <span data-ttu-id="325fd-148">Uma variável global marcada como <strong>estática</strong> não é visível para um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="325fd-148">A global variable marked <strong>static</strong> is not visible to an application.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="325fd-149"><strong>universal</strong></span><span class="sxs-lookup"><span data-stu-id="325fd-149"><strong>uniform</strong></span></span></td>
<td><span data-ttu-id="325fd-150">Marcar uma variável cujos dados são constantes durante a execução de um sombreador (como uma cor de material em um sombreador de vértice); as variáveis globais são consideradas <strong>uniformes</strong> por padrão.</span><span class="sxs-lookup"><span data-stu-id="325fd-150">Mark a variable whose data is constant throughout the execution of a shader (such as a material color in a vertex shader); global variables are considered <strong>uniform</strong> by default.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="325fd-151"><strong>volatile</strong></span><span class="sxs-lookup"><span data-stu-id="325fd-151"><strong>volatile</strong></span></span></td>
<td><span data-ttu-id="325fd-152">Marcar uma variável que é alterada com frequência; Esta é uma dica para o compilador.</span><span class="sxs-lookup"><span data-stu-id="325fd-152">Mark a variable that changes frequently; this is a hint to the compiler.</span></span> <span data-ttu-id="325fd-153">Este modificador de classe de armazenamento só se aplica a uma variável local.</span><span class="sxs-lookup"><span data-stu-id="325fd-153">This storage class modifier only applies to a local variable.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="325fd-154">O compilador HLSL atualmente ignora esse modificador de classe de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="325fd-154">The HLSL compiler currently ignores this storage class modifier.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="325fd-155"><span id="Type_Modifier"></span><span id="type_modifier"></span><span id="TYPE_MODIFIER"></span>*\_Modificador de tipo*</span><span class="sxs-lookup"><span data-stu-id="325fd-155"><span id="Type_Modifier"></span><span id="type_modifier"></span><span id="TYPE_MODIFIER"></span>*Type\_Modifier*</span></span>
</dt> <dd>

<span data-ttu-id="325fd-156">Modificador de tipo variável opcional.</span><span class="sxs-lookup"><span data-stu-id="325fd-156">Optional variable-type modifier.</span></span>



| <span data-ttu-id="325fd-157">Valor</span><span class="sxs-lookup"><span data-stu-id="325fd-157">Value</span></span>             | <span data-ttu-id="325fd-158">Descrição</span><span class="sxs-lookup"><span data-stu-id="325fd-158">Description</span></span>                                                                                                                                                                                                                                  |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="325fd-159">**const**</span><span class="sxs-lookup"><span data-stu-id="325fd-159">**const**</span></span>         | <span data-ttu-id="325fd-160">Marque uma variável que não pode ser alterada por um sombreador, portanto, ela deve ser inicializada na declaração da variável.</span><span class="sxs-lookup"><span data-stu-id="325fd-160">Mark a variable that cannot be changed by a shader, therefore, it must be initialized in the variable declaration.</span></span> <span data-ttu-id="325fd-161">Variáveis globais são consideradas **const** por padrão (suprimir esse comportamento fornecendo o sinalizador/GEC para o compilador).</span><span class="sxs-lookup"><span data-stu-id="325fd-161">Global variables are considered **const** by default (suppress this behavior by supplying the /Gec flag to the compiler).</span></span> |
| <span data-ttu-id="325fd-162">**linha \_ principal**</span><span class="sxs-lookup"><span data-stu-id="325fd-162">**row\_major**</span></span>    | <span data-ttu-id="325fd-163">Marque uma variável que armazena quatro componentes em uma única linha para que eles possam ser armazenados em um único registro constante.</span><span class="sxs-lookup"><span data-stu-id="325fd-163">Mark a variable that stores four components in a single row so they can be stored in a single constant register.</span></span>                                                                                                                             |
| <span data-ttu-id="325fd-164">**coluna \_ principal**</span><span class="sxs-lookup"><span data-stu-id="325fd-164">**column\_major**</span></span> | <span data-ttu-id="325fd-165">Marque uma variável que armazena 4 componentes em uma única coluna para otimizar a matriz matemática.</span><span class="sxs-lookup"><span data-stu-id="325fd-165">Mark a variable that stores 4 components in a single column to optimize matrix math.</span></span>                                                                                                                                                         |



 

> [!Note]  
> <span data-ttu-id="325fd-166">Se você não especificar um valor de modificador de tipo, o compilador usará a **coluna \_ principal** como o valor padrão.</span><span class="sxs-lookup"><span data-stu-id="325fd-166">If you do not specify a type-modifier value, the compiler uses **column\_major** as the default value.</span></span>

 

</dd> <dt>

<span data-ttu-id="325fd-167"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>*Escreva*</span><span class="sxs-lookup"><span data-stu-id="325fd-167"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>*Type*</span></span>
</dt> <dd>

<span data-ttu-id="325fd-168">Qualquer tipo de HLSL listado em [tipos de dados (DirectX HLSL)](dx-graphics-hlsl-data-types.md).</span><span class="sxs-lookup"><span data-stu-id="325fd-168">Any HLSL type listed in [Data Types (DirectX HLSL)](dx-graphics-hlsl-data-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="325fd-169"><span id="Name_Index_"></span><span id="name_index_"></span><span id="NAME_INDEX_"></span>*Nome* \[ do *Índice* do\]</span><span class="sxs-lookup"><span data-stu-id="325fd-169"><span id="Name_Index_"></span><span id="name_index_"></span><span id="NAME_INDEX_"></span>*Name*\[*Index*\]</span></span>
</dt> <dd>

<span data-ttu-id="325fd-170">Cadeia de caracteres ASCII que identifica exclusivamente uma variável de sombreador.</span><span class="sxs-lookup"><span data-stu-id="325fd-170">ASCII string that uniquely identifies a shader variable.</span></span> <span data-ttu-id="325fd-171">Para definir uma matriz opcional, use **index** para o tamanho da matriz, que é um inteiro positivo = 1.</span><span class="sxs-lookup"><span data-stu-id="325fd-171">To define an optional array, use **index** for the array size, which is a positive integer = 1.</span></span>

</dd> <dt>

<span data-ttu-id="325fd-172"><span id="Semantic"></span><span id="semantic"></span><span id="SEMANTIC"></span>*Semântico*</span><span class="sxs-lookup"><span data-stu-id="325fd-172"><span id="Semantic"></span><span id="semantic"></span><span id="SEMANTIC"></span>*Semantic*</span></span>
</dt> <dd>

<span data-ttu-id="325fd-173">Parâmetro opcional-informações de uso, usadas pelo compilador para vincular entradas e saídas do sombreador.</span><span class="sxs-lookup"><span data-stu-id="325fd-173">Optional parameter-usage information, used by the compiler to link shader inputs and outputs.</span></span> <span data-ttu-id="325fd-174">Há várias [semânticas](dx-graphics-hlsl-semantics.md) predefinidas para os sombreadores de vértices e de pixel.</span><span class="sxs-lookup"><span data-stu-id="325fd-174">There are several predefined [semantics](dx-graphics-hlsl-semantics.md) for vertex and pixel shaders.</span></span> <span data-ttu-id="325fd-175">O compilador ignora a semântica, a menos que elas sejam declaradas em uma variável global ou um parâmetro passado para um sombreador.</span><span class="sxs-lookup"><span data-stu-id="325fd-175">The compiler ignores semantics unless they are declared on a global variable, or a parameter passed into a shader.</span></span>

</dd> <dt>

<span data-ttu-id="325fd-176"><span id="Packoffset"></span><span id="packoffset"></span><span id="PACKOFFSET"></span>*Packoffset*</span><span class="sxs-lookup"><span data-stu-id="325fd-176"><span id="Packoffset"></span><span id="packoffset"></span><span id="PACKOFFSET"></span>*Packoffset*</span></span>
</dt> <dd>

<span data-ttu-id="325fd-177">Palavra-chave opcional para empacotar manualmente as constantes do sombreador.</span><span class="sxs-lookup"><span data-stu-id="325fd-177">Optional keyword for manually packing shader constants.</span></span> <span data-ttu-id="325fd-178">Consulte [packoffset (DirectX HLSL)](dx-graphics-hlsl-variable-packoffset.md).</span><span class="sxs-lookup"><span data-stu-id="325fd-178">See [packoffset (DirectX HLSL)](dx-graphics-hlsl-variable-packoffset.md).</span></span>

</dd> <dt>

<span data-ttu-id="325fd-179"><span id="Register"></span><span id="register"></span><span id="REGISTER"></span>*Registr*</span><span class="sxs-lookup"><span data-stu-id="325fd-179"><span id="Register"></span><span id="register"></span><span id="REGISTER"></span>*Register*</span></span>
</dt> <dd>

<span data-ttu-id="325fd-180">Palavra-chave opcional para atribuir manualmente uma variável de sombreador a um registro específico.</span><span class="sxs-lookup"><span data-stu-id="325fd-180">Optional keyword for manually assigning a shader variable to a particular register.</span></span> <span data-ttu-id="325fd-181">Consulte [registrar (DirectX HLSL)](dx-graphics-hlsl-variable-register.md).</span><span class="sxs-lookup"><span data-stu-id="325fd-181">See [register (DirectX HLSL)](dx-graphics-hlsl-variable-register.md).</span></span>

</dd> <dt>

<span data-ttu-id="325fd-182"><span id="Annotation_s_"></span><span id="annotation_s_"></span><span id="ANNOTATION_S_"></span>*Anotação (ões)*</span><span class="sxs-lookup"><span data-stu-id="325fd-182"><span id="Annotation_s_"></span><span id="annotation_s_"></span><span id="ANNOTATION_S_"></span>*Annotation(s)*</span></span>
</dt> <dd>

<span data-ttu-id="325fd-183">Metadados opcionais, na forma de uma cadeia de caracteres, anexados a uma variável global.</span><span class="sxs-lookup"><span data-stu-id="325fd-183">Optional metadata, in the form of a string, attached to a global variable.</span></span> <span data-ttu-id="325fd-184">Uma anotação é usada pela estrutura de efeito e ignorada por HLSL; para ver a sintaxe mais detalhada, consulte a [sintaxe da anotação](/windows/desktop/direct3d10/d3d10-effect-annotation-syntax).</span><span class="sxs-lookup"><span data-stu-id="325fd-184">An annotation is used by the effect framework and ignored by HLSL; to see more detailed syntax, see [annotation syntax](/windows/desktop/direct3d10/d3d10-effect-annotation-syntax).</span></span>

</dd> <dt>

<span data-ttu-id="325fd-185"><span id="Initial_Value"></span><span id="initial_value"></span><span id="INITIAL_VALUE"></span>*\_Valor inicial*</span><span class="sxs-lookup"><span data-stu-id="325fd-185"><span id="Initial_Value"></span><span id="initial_value"></span><span id="INITIAL_VALUE"></span>*Initial\_Value*</span></span>
</dt> <dd>

<span data-ttu-id="325fd-186">Valor (es) inicial (is) opcional (is); o número de valores deve corresponder ao número de componentes no *tipo*.</span><span class="sxs-lookup"><span data-stu-id="325fd-186">Optional initial value(s); the number of values should match the number of components in *Type*.</span></span> <span data-ttu-id="325fd-187">Cada variável global marcada como **externa** deve ser inicializada com um valor literal; cada variável marcada como **static** deve ser inicializada com uma constante.</span><span class="sxs-lookup"><span data-stu-id="325fd-187">Each global variable marked **extern** must be initialized with a literal value; each variable marked **static** must be initialized with a constant.</span></span>

<span data-ttu-id="325fd-188">Variáveis globais que não são marcadas como **static** ou **extern** não são compiladas no sombreador.</span><span class="sxs-lookup"><span data-stu-id="325fd-188">Global variables that are not marked **static** or **extern** are not compiled into the shader.</span></span> <span data-ttu-id="325fd-189">O compilador não define automaticamente valores padrão para variáveis globais e não pode usá-los em otimizações.</span><span class="sxs-lookup"><span data-stu-id="325fd-189">The compiler does not automatically set default values for global variables and cannot use them in optimizations.</span></span> <span data-ttu-id="325fd-190">Para inicializar esse tipo de variável global, use reflexão para obter seu valor e, em seguida, copie o valor para um buffer de constantes.</span><span class="sxs-lookup"><span data-stu-id="325fd-190">To initialize this type of global variable, use reflection to get its value and then copy the value to a constant buffer.</span></span> <span data-ttu-id="325fd-191">Por exemplo, você pode usar o método [**ID3D11ShaderReflection:: GetVariableByName**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflection-getvariablebyname) para obter a variável, usar o método [**ID3D11ShaderReflectionVariable:: GetDesc**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflectionvariable-getdesc) para obter a descrição da variável de sombreador e obter o valor inicial do membro **DefaultValue** da estrutura [**\_ \_ \_ desc da variável do sombreador D3D11**](/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_shader_variable_desc) .</span><span class="sxs-lookup"><span data-stu-id="325fd-191">For example, you can use the [**ID3D11ShaderReflection::GetVariableByName**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflection-getvariablebyname) method to get the variable, use the [**ID3D11ShaderReflectionVariable::GetDesc**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflectionvariable-getdesc) method to get the shader-variable description, and get the initial value from the **DefaultValue** member of the [**D3D11\_SHADER\_VARIABLE\_DESC**](/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_shader_variable_desc) structure.</span></span> <span data-ttu-id="325fd-192">Para copiar o valor para o buffer de constantes, você deve garantir que o buffer foi criado com acesso de gravação de CPU ([**D3D11 \_ CPU \_ Access \_ Write**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_cpu_access_flag)).</span><span class="sxs-lookup"><span data-stu-id="325fd-192">To copy the value to the constant buffer, you must ensure that the buffer was created with CPU write access ([**D3D11\_CPU\_ACCESS\_WRITE**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_cpu_access_flag)).</span></span> <span data-ttu-id="325fd-193">Para obter mais informações sobre como criar um buffer de constantes, consulte [como criar um buffer de constantes](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-constant-how-to).</span><span class="sxs-lookup"><span data-stu-id="325fd-193">For more information about how to create a constant buffer, see [How to: Create a Constant Buffer](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-constant-how-to).</span></span>

<span data-ttu-id="325fd-194">Você também pode usar a [estrutura de efeitos](../direct3d11/d3d11-graphics-programming-guide-effects.md) para processar automaticamente a reflexão e a definição do valor inicial.</span><span class="sxs-lookup"><span data-stu-id="325fd-194">You can also use the [effects framework](../direct3d11/d3d11-graphics-programming-guide-effects.md) to automatically process the reflecting and setting the initial value.</span></span> <span data-ttu-id="325fd-195">Por exemplo, você pode usar o método [**ID3DX11EffectPass:: apply**](/windows/desktop/direct3d11/id3dx11effectpass-apply) .</span><span class="sxs-lookup"><span data-stu-id="325fd-195">For example, you can use the [**ID3DX11EffectPass::Apply**](/windows/desktop/direct3d11/id3dx11effectpass-apply) method.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="325fd-196">Exemplos</span><span class="sxs-lookup"><span data-stu-id="325fd-196">Examples</span></span>

<span data-ttu-id="325fd-197">Aqui estão vários exemplos de declarações de variável de sombreador.</span><span class="sxs-lookup"><span data-stu-id="325fd-197">Here are several examples of shader-variable declarations.</span></span>


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



### <a name="group-shared"></a><span data-ttu-id="325fd-198">Grupo compartilhado</span><span class="sxs-lookup"><span data-stu-id="325fd-198">Group Shared</span></span>

<span data-ttu-id="325fd-199">O HLSL permite que threads de um sombreador de computação troquem valores por meio de memória compartilhada.</span><span class="sxs-lookup"><span data-stu-id="325fd-199">HLSL enables threads of a compute shader to exchange values via shared memory.</span></span> <span data-ttu-id="325fd-200">O HLSL fornece primitivos de barreira como [**GroupMemoryBarrierWithGroupSync**](groupmemorybarrierwithgroupsync.md)e assim por diante para garantir a ordenação correta de leituras e gravações na memória compartilhada no sombreador e evitar corridas de dados.</span><span class="sxs-lookup"><span data-stu-id="325fd-200">HLSL provides barrier primitives such as [**GroupMemoryBarrierWithGroupSync**](groupmemorybarrierwithgroupsync.md), and so on to ensure the correct ordering of reads and writes to shared memory in the shader and to avoid data races.</span></span>

> [!Note]  
> <span data-ttu-id="325fd-201">O hardware executa threads em grupos (warpes ou ondulados) e a sincronização de barreira, às vezes, pode ser omitida para aumentar o desempenho quando apenas os threads que pertencem ao mesmo grupo estão corretos.</span><span class="sxs-lookup"><span data-stu-id="325fd-201">Hardware executes threads in groups (warps or wave-fronts), and barrier synchronization can sometimes be omitted to increase performance when only synchronizing threads that belong to the same group is correct.</span></span> <span data-ttu-id="325fd-202">Mas não é altamente recomendável essa omissão por esses motivos:</span><span class="sxs-lookup"><span data-stu-id="325fd-202">But we highly discourage this omission for these reasons:</span></span>
>
> -   <span data-ttu-id="325fd-203">Essa omissão resulta em código não portátil, que pode não funcionar em algum hardware e não funciona em rasterizadores de software que normalmente executam threads em grupos menores.</span><span class="sxs-lookup"><span data-stu-id="325fd-203">This omission results in non-portable code, which might not work on some hardware and doesn't work on software rasterizers that typically execute threads in smaller groups.</span></span>
> -   <span data-ttu-id="325fd-204">As melhorias de desempenho que você pode atingir com essa omissão serão pequenas em comparação com a barreira de todos os threads.</span><span class="sxs-lookup"><span data-stu-id="325fd-204">The performance improvements that you might achieve with this omission will be minor compared to using all-thread barrier.</span></span>

 

<span data-ttu-id="325fd-205">No Direct3D 10 não há sincronização de threads ao gravar em **groupshared**, portanto, isso significa que cada thread é limitado a um único local em uma matriz para gravação.</span><span class="sxs-lookup"><span data-stu-id="325fd-205">In Direct3D 10 there is no synchronization of threads when writing to **groupshared**, so this means that each thread is limited to a single location in an array for writing.</span></span> <span data-ttu-id="325fd-206">Use o valor do sistema [ \_ GroupIndex VA](dx-graphics-hlsl-semantics.md) para indexar nessa matriz ao gravar para garantir que dois threads possam colidir.</span><span class="sxs-lookup"><span data-stu-id="325fd-206">Use the [SV\_GroupIndex](dx-graphics-hlsl-semantics.md) system value to index into this array when writing to ensure that no two threads can collide.</span></span> <span data-ttu-id="325fd-207">Em termos de leitura, todos os threads têm acesso a toda a matriz para leitura.</span><span class="sxs-lookup"><span data-stu-id="325fd-207">In terms of reading, all threads have access to the entire array for reading.</span></span>


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



### <a name="packing"></a><span data-ttu-id="325fd-208">Recibo</span><span class="sxs-lookup"><span data-stu-id="325fd-208">Packing</span></span>

<span data-ttu-id="325fd-209">Pacotes subcomponentes de vetores e escalares cujo tamanho é grande o suficiente para evitar o cruzamento dos limites de registro.</span><span class="sxs-lookup"><span data-stu-id="325fd-209">Pack subcomponents of vectors and scalars whose size is large enough to prevent crossing register boundarys.</span></span> <span data-ttu-id="325fd-210">Por exemplo, todos eles são válidos:</span><span class="sxs-lookup"><span data-stu-id="325fd-210">For example, these are all valid:</span></span>


```
cbuffer MyBuffer
{
    float4 Element1 : packoffset(c0);
    float1 Element2 : packoffset(c1);
    float1 Element3 : packoffset(c1.y);
}
        
```



<span data-ttu-id="325fd-211">Não é possível misturar tipos de empacotamento.</span><span class="sxs-lookup"><span data-stu-id="325fd-211">Cannot mix packing types.</span></span>

<span data-ttu-id="325fd-212">Assim como a palavra-chave Register, um packoffset pode ser específico de destino.</span><span class="sxs-lookup"><span data-stu-id="325fd-212">Like the register keyword, a packoffset can be target specific.</span></span> <span data-ttu-id="325fd-213">A embalagem do subcomponente só está disponível com a palavra-chave packoffset, não a palavra-chave Register.</span><span class="sxs-lookup"><span data-stu-id="325fd-213">Subcomponent packing is only available with the packoffset keyword, not the register keyword.</span></span> <span data-ttu-id="325fd-214">Dentro de uma declaração CBuffer, a palavra-chave Register é ignorada para destinos do Direct3D 10, pois ela é considerada para compatibilidade entre plataformas.</span><span class="sxs-lookup"><span data-stu-id="325fd-214">Inside a cbuffer declaration, the register keyword is ignored for Direct3D 10 targets as it is assumed to be for cross-platform compatibility.</span></span>

<span data-ttu-id="325fd-215">Elementos empacotados podem se sobrepor e o compilador não apresentará nenhum erro ou aviso.</span><span class="sxs-lookup"><span data-stu-id="325fd-215">Packed elements may overlap and the compiler will give no error or warning.</span></span> <span data-ttu-id="325fd-216">Neste exemplo, Element2 e Element3 serão sobrepostas com Element1. x e Element1. y.</span><span class="sxs-lookup"><span data-stu-id="325fd-216">In this example, Element2 and Element3 will overlap with Element1.x and Element1.y.</span></span>


```
cbuffer MyBuffer
{
    float4 Element1 : packoffset(c0);
    float1 Element2 : packoffset(c0);
    float1 Element3 : packoffset(c0.y);
}
        
```



<span data-ttu-id="325fd-217">Um exemplo que usa packoffset é: [HLSLWithoutFX10 Sample](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="325fd-217">A sample that uses packoffset is: [HLSLWithoutFX10 Sample](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx).</span></span>

## <a name="related-topics"></a><span data-ttu-id="325fd-218">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="325fd-218">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="325fd-219">Variáveis (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="325fd-219">Variables (DirectX HLSL)</span></span>](dx-graphics-hlsl-variables.md)
</dt> </dl>

 

