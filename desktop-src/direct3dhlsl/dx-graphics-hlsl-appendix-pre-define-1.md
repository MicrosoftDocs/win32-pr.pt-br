---
title: '\#definir diretiva (constante)'
description: Diretiva de pré-processador que atribui um nome significativo a uma constante em seu aplicativo.
ms.assetid: cc9b34a3-4c83-4999-99ec-e6261ecb2785
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: deae1ca92c2280cd31cbec2bf3482c61fcf2b88a
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/23/2019
ms.locfileid: "104006936"
---
# <a name="define-directive-constant"></a><span data-ttu-id="83407-103">\#definir diretiva (constante)</span><span class="sxs-lookup"><span data-stu-id="83407-103">\#define directive (constant)</span></span>

<span data-ttu-id="83407-104">Diretiva de pré-processador que atribui um nome significativo a uma constante em seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="83407-104">Preprocessor directive that assigns a meaningful name to a constant in your application.</span></span>



| <span data-ttu-id="83407-105">\#definir *identifiertoken-cadeia de caracteres*</span><span class="sxs-lookup"><span data-stu-id="83407-105">\#define *identifiertoken-string*</span></span> |
|-----------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="83407-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="83407-106">Parameters</span></span>



| <span data-ttu-id="83407-107">Item</span><span class="sxs-lookup"><span data-stu-id="83407-107">Item</span></span>                                                                                                                       | <span data-ttu-id="83407-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="83407-108">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83407-109"><span id="identifier"></span><span id="IDENTIFIER"></span>*ID*</span><span class="sxs-lookup"><span data-stu-id="83407-109"><span id="identifier"></span><span id="IDENTIFIER"></span>*identifier*</span></span><br/>                                          | <span data-ttu-id="83407-110">Identificador da constante.</span><span class="sxs-lookup"><span data-stu-id="83407-110">Identifier of the constant.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="83407-111"><span id="token-string__optional_"></span><span id="TOKEN-STRING__OPTIONAL_"></span>*cadeia de caracteres* \[ de token adicional\]</span><span class="sxs-lookup"><span data-stu-id="83407-111"><span id="token-string__optional_"></span><span id="TOKEN-STRING__OPTIONAL_"></span>*token-string* \[optional\]</span></span><br/> | <span data-ttu-id="83407-112">Valor da constante.</span><span class="sxs-lookup"><span data-stu-id="83407-112">Value of the constant.</span></span> <span data-ttu-id="83407-113">Esse parâmetro consiste em uma série de tokens, como palavras-chave, constantes ou instruções completas.</span><span class="sxs-lookup"><span data-stu-id="83407-113">This parameter consists of a series of tokens, such as keywords, constants, or complete statements.</span></span> <span data-ttu-id="83407-114">Um ou mais caracteres de espaço em branco devem separar esse parâmetro do parâmetro de *identificador* ; Este espaço em branco não é considerado parte do texto substituído, nem qualquer espaço em branco após o último token do texto.</span><span class="sxs-lookup"><span data-stu-id="83407-114">One or more white-space characters must separate this parameter from the *identifier* parameter; this white space is not considered part of the substituted text, nor is any white space following the last token of the text.</span></span> <br/> <span data-ttu-id="83407-115">Se você excluir esse parâmetro, todas as instâncias do parâmetro do *identificador* serão removidas do arquivo de origem.</span><span class="sxs-lookup"><span data-stu-id="83407-115">If you exclude this parameter, all instances of the *identifier* parameter are removed from the source file.</span></span> <span data-ttu-id="83407-116">O identificador permanece definido e pode ser testado usando as diretivas [ \# If definidas](dx-graphics-hlsl-appendix-pre-ifdef.md), \# ifdef e \# ifndef.</span><span class="sxs-lookup"><span data-stu-id="83407-116">The identifier remains defined, and can be tested using the [\#if defined](dx-graphics-hlsl-appendix-pre-ifdef.md), \#ifdef, and \#ifndef directives.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="83407-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="83407-117">Remarks</span></span>

<span data-ttu-id="83407-118">Todas as instâncias do parâmetro de *identificador* que ocorrem após a diretiva de [ \# definição](dx-graphics-hlsl-appendix-pre-define.md) no arquivo de origem serão substituídas pelo valor do parâmetro *token-String* .</span><span class="sxs-lookup"><span data-stu-id="83407-118">All instances of the *identifier* parameter that occur after the [\#define](dx-graphics-hlsl-appendix-pre-define.md) directive in the source file will be replaced by the value of the *token-string* parameter.</span></span> <span data-ttu-id="83407-119">O identificador é substituído somente quando ele forma um token; por exemplo, o identificador não será substituído se aparecer em um comentário, dentro de uma cadeia de caracteres ou como parte de um identificador mais longo.</span><span class="sxs-lookup"><span data-stu-id="83407-119">The identifier is replaced only when it forms a token; for example, the identifier is not replaced if it appears in a comment, within a string, or as part of a longer identifier.</span></span>

<span data-ttu-id="83407-120">A diretiva [ \# undef](dx-graphics-hlsl-appendix-pre-undef.md) instrui o pré-processador a esquecer a definição de um identificador; para obter mais informações, consulte a \# diretiva undef (DirectX HLSL).</span><span class="sxs-lookup"><span data-stu-id="83407-120">The [\#undef](dx-graphics-hlsl-appendix-pre-undef.md) directive instructs the preprocessor to forget the definition of an identifier; for more information, see \#undef Directive (DirectX HLSL).</span></span>

<span data-ttu-id="83407-121">A definição de constantes com a opção de compilador/D tem o mesmo efeito que usar a diretiva [ \# define](dx-graphics-hlsl-appendix-pre-define.md) no início do arquivo.</span><span class="sxs-lookup"><span data-stu-id="83407-121">Defining constants with the /D compiler option has the same effect as using the [\#define](dx-graphics-hlsl-appendix-pre-define.md) directive at the beginning of your file.</span></span> <span data-ttu-id="83407-122">Até 30 constantes podem ser definidas com a opção/D.</span><span class="sxs-lookup"><span data-stu-id="83407-122">Up to 30 constants can be defined with the /D option.</span></span> <span data-ttu-id="83407-123">Para obter um exemplo de como isso pode ser usado, consulte a seção de exemplos de [ \# ifdef e)](dx-graphics-hlsl-appendix-pre-ifdef.md).</span><span class="sxs-lookup"><span data-stu-id="83407-123">For an example of how this can be used, see the Examples section of [\#ifdef and )](dx-graphics-hlsl-appendix-pre-ifdef.md).</span></span>

## <a name="examples"></a><span data-ttu-id="83407-124">Exemplos</span><span class="sxs-lookup"><span data-stu-id="83407-124">Examples</span></span>

<span data-ttu-id="83407-125">O exemplo a seguir define a largura do identificador como a constante de inteiro 80 e define o comprimento em termos de largura e a constante de inteiro 10.</span><span class="sxs-lookup"><span data-stu-id="83407-125">The following example defines the identifier WIDTH as the integer constant 80 and then defines LENGTH in terms of WIDTH and the integer constant 10.</span></span>


```
#define WIDTH       80
#define LENGTH      ( WIDTH + 10 )
```



<span data-ttu-id="83407-126">Cada instância subsequente de LENGTH é substituída por (WIDTH + 10) e todas as instâncias subsequentes de WIDTH + 10 são substituídas pela expressão (80 + 10).</span><span class="sxs-lookup"><span data-stu-id="83407-126">Every subsequent instance of LENGTH is replaced by (WIDTH + 10), and every subsequent instance of WIDTH + 10 is replaced by the expression (80 + 10).</span></span> <span data-ttu-id="83407-127">Os parênteses em volta da largura + 10 são importantes porque controlam a interpretação em instruções como as seguintes.</span><span class="sxs-lookup"><span data-stu-id="83407-127">The parentheses around WIDTH + 10 are important because they control the interpretation in statements such as the following.</span></span>


```
var = LENGTH * 20;
```



<span data-ttu-id="83407-128">Após o estágio de pré-processamento, a instrução se torna o seguinte, que é avaliado como 1.800.</span><span class="sxs-lookup"><span data-stu-id="83407-128">After the preprocessing stage the statement becomes the following, which evaluates to 1,800.</span></span>


```
var = ( 80 + 10 ) * 20;
```



<span data-ttu-id="83407-129">Sem parênteses, o resultado seria o seguinte, que é avaliado como 280.</span><span class="sxs-lookup"><span data-stu-id="83407-129">Without parentheses, the result would be the following, which evaluates to 280.</span></span>


```
var = 80 + 10 * 20;
```



## <a name="related-topics"></a><span data-ttu-id="83407-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="83407-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="83407-131">Diretivas de pré-processador (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="83407-131">Preprocessor Directives (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[<span data-ttu-id="83407-132">\#definir sobrecargas</span><span class="sxs-lookup"><span data-stu-id="83407-132">\#define Overloads</span></span>](dx-graphics-hlsl-appendix-pre-define.md)
</dt> <dt>

[<span data-ttu-id="83407-133">\#Diretiva undef (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="83407-133">\#undef Directive (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-pre-undef.md)
</dt> </dl>

 

 





