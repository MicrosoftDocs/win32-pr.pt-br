---
title: " Diretiva de linha"
description: Diretiva de pré-processador que define o número de linha armazenado internamente do compilador e o nome do arquivo para os valores especificados.
ms.assetid: 307410af-bd78-4b3d-b515-adf58298f35f
keywords:
- Diretiva de linha HLSL
topic_type:
- apiref
api_name:
- line Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0932138ce5aec85ad3d3e7058db0c2a93e131181
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104364842"
---
# <a name="line-directive"></a><span data-ttu-id="0d506-104">\#Diretiva de linha</span><span class="sxs-lookup"><span data-stu-id="0d506-104">\#line Directive</span></span>

<span data-ttu-id="0d506-105">Diretiva de pré-processador que define o número de linha armazenado internamente do compilador e o nome do arquivo para os valores especificados.</span><span class="sxs-lookup"><span data-stu-id="0d506-105">Preprocessor directive that sets the compiler's internally-stored line number and filename to the specified values.</span></span>



| <span data-ttu-id="0d506-106">\#linha *LineNumber* "*filename*"</span><span class="sxs-lookup"><span data-stu-id="0d506-106">\#line *lineNumber* "*filename*"</span></span> |
|----------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="0d506-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0d506-107">Parameters</span></span>



| <span data-ttu-id="0d506-108">Item</span><span class="sxs-lookup"><span data-stu-id="0d506-108">Item</span></span>                                                                                                                              | <span data-ttu-id="0d506-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="0d506-109">Description</span></span>                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d506-110"><span id="lineNumber"></span><span id="linenumber"></span><span id="LINENUMBER"></span>*lineNumber*</span><span class="sxs-lookup"><span data-stu-id="0d506-110"><span id="lineNumber"></span><span id="linenumber"></span><span id="LINENUMBER"></span>*lineNumber*</span></span><br/>                    | <span data-ttu-id="0d506-111">Número de linha a ser definido.</span><span class="sxs-lookup"><span data-stu-id="0d506-111">Line number to set.</span></span> <span data-ttu-id="0d506-112">Pode ser qualquer constante inteira.</span><span class="sxs-lookup"><span data-stu-id="0d506-112">This can be any integer constant.</span></span> <span data-ttu-id="0d506-113">A substituição de macro pode ser executada nos tokens de pré-processamento, desde que o resultado seja avaliado como a sintaxe correta.</span><span class="sxs-lookup"><span data-stu-id="0d506-113">Macro replacement can be performed on the preprocessing tokens, as long as the result evaluates to the correct syntax.</span></span> <br/>                     |
| <span data-ttu-id="0d506-114"><span id="filename__optional__________"></span><span id="FILENAME__OPTIONAL__________"></span>*nome do arquivo* \[ adicional\]</span><span class="sxs-lookup"><span data-stu-id="0d506-114"><span id="filename__optional__________"></span><span id="FILENAME__OPTIONAL__________"></span>*filename* \[optional\]</span></span> <br/> | <span data-ttu-id="0d506-115">Nome de arquivo a ser definido.</span><span class="sxs-lookup"><span data-stu-id="0d506-115">Filename to set.</span></span> <span data-ttu-id="0d506-116">O nome do arquivo pode ser qualquer combinação de caracteres e deve ser colocado entre aspas duplas ("").</span><span class="sxs-lookup"><span data-stu-id="0d506-116">The filename can be any combination of characters, and must be enclosed in double quotation marks (" ").</span></span> <span data-ttu-id="0d506-117">Se esse parâmetro for omitido, o nome de arquivo anterior permanecerá inalterado.</span><span class="sxs-lookup"><span data-stu-id="0d506-117">If this parameter is omitted, the previous filename remains unchanged.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="0d506-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="0d506-118">Remarks</span></span>

<span data-ttu-id="0d506-119">O compilador usa o número de linha e o nome de arquivo para se referir a erros encontrados durante a compilação.</span><span class="sxs-lookup"><span data-stu-id="0d506-119">The compiler uses the line number and filename to refer to errors that it finds during compilation.</span></span> <span data-ttu-id="0d506-120">O número de linha geralmente se refere à linha de entrada atual, e o nome de arquivo se refere ao arquivo de entrada atual.</span><span class="sxs-lookup"><span data-stu-id="0d506-120">The line number usually refers to the current input line, and the filename refers to the current input file.</span></span> <span data-ttu-id="0d506-121">O número de linha é incrementado depois que cada linha é processada.</span><span class="sxs-lookup"><span data-stu-id="0d506-121">The line number is incremented after each line is processed.</span></span> <span data-ttu-id="0d506-122">Se você alterar o número de linha e o nome de arquivo, o compilador irá ignorar os valores anteriores e continuar o processamento com os novos valores.</span><span class="sxs-lookup"><span data-stu-id="0d506-122">If you change the line number and filename, the compiler ignores the previous values and continues processing with the new values.</span></span> <span data-ttu-id="0d506-123">A \# diretiva de linha normalmente é usada por geradores de programa para fazer com que as mensagens de erro se refiram ao arquivo de origem original, e não ao programa gerado.</span><span class="sxs-lookup"><span data-stu-id="0d506-123">The \#line directive is typically used by program generators to cause error messages to refer to the original source file instead of to the generated program.</span></span>

<span data-ttu-id="0d506-124">O tradutor usa o número de linha e o nome de arquivo para determinar os valores do \_ \_ arquivo \_ \_ e \_ \_ linha \_ \_ de macros predefinidos.</span><span class="sxs-lookup"><span data-stu-id="0d506-124">The translator uses the line number and filename to determine the values of the predefined macros \_\_FILE\_\_ and \_\_LINE\_\_.</span></span> <span data-ttu-id="0d506-125">Você pode usar essas macros para inserir mensagens de erro autodescritivas no texto do programa.</span><span class="sxs-lookup"><span data-stu-id="0d506-125">You can use these macros to insert self-descriptive error messages into the program text.</span></span> <span data-ttu-id="0d506-126">A \_ \_ macro File se \_ \_ expande para uma cadeia de caracteres cujo conteúdo é o nome do arquivo, entre aspas duplas ("").</span><span class="sxs-lookup"><span data-stu-id="0d506-126">The \_\_FILE\_\_ macro expands to a string whose contents are the filename, surrounded by double quotation marks (" ").</span></span>

## <a name="examples"></a><span data-ttu-id="0d506-127">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0d506-127">Examples</span></span>

<span data-ttu-id="0d506-128">O exemplo a seguir define o número de linha como 151 e o nome de arquivo como "Copy. c".</span><span class="sxs-lookup"><span data-stu-id="0d506-128">The following example sets the line number to 151 and the filename to "copy.c".</span></span>


```
#line 151 "copy.c"
```



<span data-ttu-id="0d506-129">No exemplo a seguir, a macro ASSERT usa a linha e o arquivo de macros predefinidos \_ \_ \_ \_ \_ \_ \_ \_ para imprimir uma mensagem de erro sobre o arquivo de origem se a declaração especificada não for verdadeira.</span><span class="sxs-lookup"><span data-stu-id="0d506-129">In the following example, the macro ASSERT uses the predefined macros \_\_LINE\_\_ and \_\_FILE\_\_ to print an error message about the source file if the specified assertion is not true.</span></span>


```
#define ASSERT(cond)

if( !(cond) )\
{printf( "assertion error line %d, file(%s)\n", \
__LINE__, __FILE__ );}
```



## <a name="see-also"></a><span data-ttu-id="0d506-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="0d506-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d506-131">Diretivas de pré-processador (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0d506-131">Preprocessor Directives (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> </dl>

 

 





