---
title: '\#diretiva define (macro)'
description: Diretiva de pré-processador que cria uma macro semelhante a uma função.
ms.assetid: 73c19cf8-fbc5-444b-a51f-dc9f881f397b
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d0c54c0c433c91522c8a72c5955a419eb72f9eee
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387512"
---
# <a name="define-directive-macro"></a><span data-ttu-id="f4f21-103">\#diretiva define (macro)</span><span class="sxs-lookup"><span data-stu-id="f4f21-103">\#define directive (macro)</span></span>

<span data-ttu-id="f4f21-104">Diretiva de pré-processador que cria uma macro semelhante a uma função.</span><span class="sxs-lookup"><span data-stu-id="f4f21-104">Preprocessor directive that creates a function-like macro.</span></span>



| <span data-ttu-id="f4f21-105">\#define *identifier*( *argument0*, ... , *argumentN-1* ) *token-string*</span><span class="sxs-lookup"><span data-stu-id="f4f21-105">\#define *identifier*( *argument0*, ... , *argumentN-1* ) *token-string*</span></span> |
|--------------------------------------------------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="f4f21-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f4f21-106">Parameters</span></span>



| <span data-ttu-id="f4f21-107">Item</span><span class="sxs-lookup"><span data-stu-id="f4f21-107">Item</span></span>                                                                                                                                                                                                                                                          | <span data-ttu-id="f4f21-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="f4f21-108">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4f21-109"><span id="identifier"></span><span id="IDENTIFIER"></span>*Identificador*</span><span class="sxs-lookup"><span data-stu-id="f4f21-109"><span id="identifier"></span><span id="IDENTIFIER"></span>*identifier*</span></span><br/>                                                                                                                                                                             | <span data-ttu-id="f4f21-110">Identificador da macro.</span><span class="sxs-lookup"><span data-stu-id="f4f21-110">Identifier of the macro.</span></span> <br/> <span data-ttu-id="f4f21-111">Uma segunda [ \# definição](dx-graphics-hlsl-appendix-pre-define.md) para uma macro com um identificador que já existe no contexto atual gera um erro, a menos que a segunda sequência de token seja idêntica à primeira.</span><span class="sxs-lookup"><span data-stu-id="f4f21-111">A second [\#define](dx-graphics-hlsl-appendix-pre-define.md) for a macro with an identifier that already exists in the current context generates an error unless the second token sequence is identical to the first.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="f4f21-112"><span id="___________argument0___...___argumentN-1_________"></span><span id="___________argument0___...___argumentn-1_________"></span><span id="___________ARGUMENT0___...___ARGUMENTN-1_________"></span> ( *argument0*, ... , *argumentN-1* )</span><span class="sxs-lookup"><span data-stu-id="f4f21-112"><span id="___________argument0___...___argumentN-1_________"></span><span id="___________argument0___...___argumentn-1_________"></span><span id="___________ARGUMENT0___...___ARGUMENTN-1_________"></span> ( *argument0*, ... , *argumentN-1* )</span></span> <br/> | <span data-ttu-id="f4f21-113">Lista de argumentos para a macro.</span><span class="sxs-lookup"><span data-stu-id="f4f21-113">List of arguments to the macro.</span></span> <span data-ttu-id="f4f21-114">A lista de argumentos é delimitada por vírgulas, pode ter qualquer comprimento e deve ser entre parênteses.</span><span class="sxs-lookup"><span data-stu-id="f4f21-114">The argument list is comma-delimited, can be of any length, and must be enclosed in parentheses.</span></span> <span data-ttu-id="f4f21-115">Cada nome de argumento na lista deve ser exclusivo.</span><span class="sxs-lookup"><span data-stu-id="f4f21-115">Each argument name in the list must be unique.</span></span> <span data-ttu-id="f4f21-116">Nenhum espaço em branco pode separar *o parâmetro de identificador* e o parêntese de abertura.</span><span class="sxs-lookup"><span data-stu-id="f4f21-116">No white space can separate the *identifier* parameter and the opening parenthesis.</span></span> <br/> <span data-ttu-id="f4f21-117">Use a concatenação de linha coloque uma faixa invertida ( ) imediatamente antes do caractere de nova linha para dividir \\ diretivas longas em várias linhas de origem.</span><span class="sxs-lookup"><span data-stu-id="f4f21-117">Use line concatenation place a backslash (\\) immediately before the newline character to split long directives onto multiple source lines.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="f4f21-118"><span id="token-string__optional________"></span><span id="TOKEN-STRING__OPTIONAL________"></span>*cadeia de caracteres de token* \[ Opcional\]</span><span class="sxs-lookup"><span data-stu-id="f4f21-118"><span id="token-string__optional________"></span><span id="TOKEN-STRING__OPTIONAL________"></span>*token-string* \[optional\]</span></span> <br/>                                                                                                                     | <span data-ttu-id="f4f21-119">Valor da macro.</span><span class="sxs-lookup"><span data-stu-id="f4f21-119">Value of the macro.</span></span> <span data-ttu-id="f4f21-120">Esse parâmetro consiste em uma série de tokens, como palavras-chave, constantes ou instruções completas.</span><span class="sxs-lookup"><span data-stu-id="f4f21-120">This parameter consists of a series of tokens, such as keywords, constants, or complete statements.</span></span> <span data-ttu-id="f4f21-121">Um ou mais caracteres de espaço em branco devem separar esse parâmetro do *parâmetro do identificador;* esse espaço em branco não é considerado parte do texto substituído, nem qualquer espaço em branco após o último token do texto.</span><span class="sxs-lookup"><span data-stu-id="f4f21-121">One or more white-space characters must separate this parameter from the *identifier* parameter; this white space is not considered part of the substituted text, nor is any white space following the last token of the text.</span></span> <span data-ttu-id="f4f21-122">Use parênteses para garantir que argumentos complicados sejam interpretados corretamente.</span><span class="sxs-lookup"><span data-stu-id="f4f21-122">Make liberal use of parentheses to ensure that complicated arguments are interpreted correctly.</span></span> <br/> <span data-ttu-id="f4f21-123">Se o valor do parâmetro *identificador* ocorrer dentro do parâmetro de cadeia de caracteres de *token* (mesmo como resultado de outra expansão de macro), ele não será expandido.</span><span class="sxs-lookup"><span data-stu-id="f4f21-123">If the value of the *identifier* parameter occurs within the *token-string* parameter (even as a result of another macro expansion), it is not expanded.</span></span> <br/> <span data-ttu-id="f4f21-124">Se você excluir esse parâmetro, todas as instâncias do parâmetro *identificador* serão removidas do arquivo de origem.</span><span class="sxs-lookup"><span data-stu-id="f4f21-124">If you exclude this parameter, all instances of the *identifier* parameter are removed from the source file.</span></span> <span data-ttu-id="f4f21-125">O identificador permanece definido e pode ser testado usando as diretivas [ \# ,](dx-graphics-hlsl-appendix-pre-ifdef.md) \# ifdef e \# ifndef definidas.</span><span class="sxs-lookup"><span data-stu-id="f4f21-125">The identifier remains defined, and can be tested using the [\#if defined](dx-graphics-hlsl-appendix-pre-ifdef.md), \#ifdef, and \#ifndef directives.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="f4f21-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="f4f21-126">Remarks</span></span>

<span data-ttu-id="f4f21-127">Todas as instâncias do parâmetro de *identificador* que ocorrem após a diretiva [ \# define](dx-graphics-hlsl-appendix-pre-define.md) no arquivo de origem constituem uma chamada de macro e o identificador será substituído por uma versão do parâmetro de cadeia de caracteres de *token* que tem argumentos reais substituídos por parâmetros formais.</span><span class="sxs-lookup"><span data-stu-id="f4f21-127">All instances of the *identifier* parameter that occur after the [\#define](dx-graphics-hlsl-appendix-pre-define.md) directive in the source file constitute a macro call, and the identifier will be replaced by a version of the *token-string* parameter that has actual arguments substituted for formal parameters.</span></span> <span data-ttu-id="f4f21-128">O número de parâmetros na chamada deve corresponder ao número de parâmetros na definição de macro.</span><span class="sxs-lookup"><span data-stu-id="f4f21-128">The number of parameters in the call must match the number of parameters in the macro definition.</span></span> <span data-ttu-id="f4f21-129">O identificador é substituído somente quando ele forma um token; por exemplo, o identificador não será substituído se ele aparecer em um comentário, em uma cadeia de caracteres ou como parte de um identificador mais longo.</span><span class="sxs-lookup"><span data-stu-id="f4f21-129">The identifier is replaced only when it forms a token; for example, the identifier is not replaced if it appears in a comment, within a string, or as part of a longer identifier.</span></span>

<span data-ttu-id="f4f21-130">A [ \# diretiva undef](dx-graphics-hlsl-appendix-pre-undef.md) instrui o pré-processador a esquecer a definição de um identificador; para obter mais informações, consulte \# Diretiva undef (DirectX HLSL).</span><span class="sxs-lookup"><span data-stu-id="f4f21-130">The [\#undef](dx-graphics-hlsl-appendix-pre-undef.md) directive instructs the preprocessor to forget the definition of an identifier; for more information, see \#undef Directive (DirectX HLSL).</span></span>

<span data-ttu-id="f4f21-131">Definir constantes com a opção do compilador /D tem o mesmo efeito que usar a diretiva [ \# define](dx-graphics-hlsl-appendix-pre-define.md) no início do arquivo.</span><span class="sxs-lookup"><span data-stu-id="f4f21-131">Defining constants with the /D compiler option has the same effect as using the [\#define](dx-graphics-hlsl-appendix-pre-define.md) directive at the beginning of your file.</span></span> <span data-ttu-id="f4f21-132">Até 30 macros podem ser definidas com a opção /D.</span><span class="sxs-lookup"><span data-stu-id="f4f21-132">Up to 30 macros can be defined with the /D option.</span></span>

<span data-ttu-id="f4f21-133">Os argumentos reais na chamada de macro são correspondentes aos argumentos formais correspondentes na definição de macro.</span><span class="sxs-lookup"><span data-stu-id="f4f21-133">The actual arguments in the macro call are matched to the corresponding formal arguments in the macro definition.</span></span> <span data-ttu-id="f4f21-134">Cada argumento formal na cadeia de caracteres de token é substituído pelo argumento real correspondente, a menos que o argumento seja precedido por um operador stringizing ( \# ), charizing ( @) ou \# token-pasting ( \# \# ) \# ou é seguido por um \# operador .</span><span class="sxs-lookup"><span data-stu-id="f4f21-134">Each formal argument in the token string is replaced by the corresponding actual argument, unless the argument is preceded by a stringizing (\#), charizing (\#@), or token-pasting (\#\#) operator, or is followed by a \#\# operator.</span></span> <span data-ttu-id="f4f21-135">As macros no argumento real são expandidas antes da política substituir o parâmetro formal.</span><span class="sxs-lookup"><span data-stu-id="f4f21-135">Any macros in the actual argument are expanded before the directive replaces the formal parameter.</span></span>

<span data-ttu-id="f4f21-136">A colar token no compilador HLSL é ligeiramente diferente da colar token no compilador C, já que os tokens colares devem ser tokens válidos por conta própria.</span><span class="sxs-lookup"><span data-stu-id="f4f21-136">Token pasting in the HLSL compiler is slightly different from token pasting in the C compiler, in that the pasted tokens must be valid tokens on their own.</span></span> <span data-ttu-id="f4f21-137">Por exemplo, considere a seguinte definição de macro:</span><span class="sxs-lookup"><span data-stu-id="f4f21-137">For example, consider the following macro definition:</span></span>


```
#define MERGE(a, b) a##b
MERGE(float, 4x4) test;
```



<span data-ttu-id="f4f21-138">No compilador C, isso resulta no seguinte:</span><span class="sxs-lookup"><span data-stu-id="f4f21-138">In the C compiler, this results in the following:</span></span>


```
float4x4 test
```



<span data-ttu-id="f4f21-139">No entanto, no compilador HLSL, isso resulta no seguinte:</span><span class="sxs-lookup"><span data-stu-id="f4f21-139">In the HLSL compiler however, this results in the following:</span></span>


```
float4 x4 test
```



<span data-ttu-id="f4f21-140">Você pode resolver esse comportamento usando a definição de macro a seguir.</span><span class="sxs-lookup"><span data-stu-id="f4f21-140">You can work around this behavior by using the following macro definition instead.</span></span>


```
MERGE(MERGE(float, 4), x4) test;
```



## <a name="examples"></a><span data-ttu-id="f4f21-141">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f4f21-141">Examples</span></span>

<span data-ttu-id="f4f21-142">O exemplo a seguir usa uma macro para definir linhas de cursor.</span><span class="sxs-lookup"><span data-stu-id="f4f21-142">The following example uses a macro to define cursor lines.</span></span>


```
#define CURSOR(top, bottom) (((top) << 8) | (bottom))
```



<span data-ttu-id="f4f21-143">O exemplo a seguir define uma macro que recupera um inteiro pseudorandom no intervalo especificado.</span><span class="sxs-lookup"><span data-stu-id="f4f21-143">The following example defines a macro that retrieves a pseudorandom integer in the specified range.</span></span>


```
#define getrandom(min, max) \
((rand()%(int)(((max) + 1)-(min)))+ (min))
```



## <a name="related-topics"></a><span data-ttu-id="f4f21-144">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f4f21-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f4f21-145">Diretivas de pré-processador (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f4f21-145">Preprocessor Directives (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[<span data-ttu-id="f4f21-146">\#definir sobrecargas</span><span class="sxs-lookup"><span data-stu-id="f4f21-146">\#define Overloads</span></span>](dx-graphics-hlsl-appendix-pre-define.md)
</dt> <dt>

[<span data-ttu-id="f4f21-147">\#Diretiva undef (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f4f21-147">\#undef Directive (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-pre-undef.md)
</dt> </dl>

 

 





