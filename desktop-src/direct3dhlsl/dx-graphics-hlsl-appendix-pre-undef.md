---
title: " Diretiva undef"
description: Diretiva de pré-processador que remove a definição atual de uma constante ou macro que foi definida anteriormente usando a diretiva \ define.
ms.assetid: ba6bbe6b-ecfa-40cb-887f-e42b6e22c7bd
keywords:
- Diretiva de undef HLSL
topic_type:
- apiref
api_name:
- undef Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7358dc60d002e784394f64773934a18f7413e493
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104293197"
---
# <a name="undef-directive"></a><span data-ttu-id="4c29f-104">\#Diretiva undef</span><span class="sxs-lookup"><span data-stu-id="4c29f-104">\#undef Directive</span></span>

<span data-ttu-id="4c29f-105">Diretiva de pré-processador que remove a definição atual de uma constante ou macro que foi definida anteriormente usando a diretiva de [ \# definição](dx-graphics-hlsl-appendix-pre-define.md) .</span><span class="sxs-lookup"><span data-stu-id="4c29f-105">Preprocessor directive that removes the current definition of a constant or macro that was previously defined using the [\#define](dx-graphics-hlsl-appendix-pre-define.md) directive.</span></span>



| <span data-ttu-id="4c29f-106">\#*identificador* de undef</span><span class="sxs-lookup"><span data-stu-id="4c29f-106">\#undef *identifier*</span></span> |
|----------------------|



 

## <a name="parameters"></a><span data-ttu-id="4c29f-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4c29f-107">Parameters</span></span>



| <span data-ttu-id="4c29f-108">Item</span><span class="sxs-lookup"><span data-stu-id="4c29f-108">Item</span></span>                                                                              | <span data-ttu-id="4c29f-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="4c29f-109">Description</span></span>                                                                                                                                                      |
|-----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c29f-110"><span id="identifier"></span><span id="IDENTIFIER"></span>*ID*</span><span class="sxs-lookup"><span data-stu-id="4c29f-110"><span id="identifier"></span><span id="IDENTIFIER"></span>*identifier*</span></span><br/> | <span data-ttu-id="4c29f-111">Identificador da constante ou da macro para remover a definição de.</span><span class="sxs-lookup"><span data-stu-id="4c29f-111">Identifier of the constant or macro to remove the definition of.</span></span> <span data-ttu-id="4c29f-112">Se você estiver desdefinindo uma macro, forneça apenas o identificador, não a lista de parâmetros.</span><span class="sxs-lookup"><span data-stu-id="4c29f-112">If you are undefining a macro, provide only the identifier, not the parameter list.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="4c29f-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="4c29f-113">Remarks</span></span>

<span data-ttu-id="4c29f-114">Você pode aplicar a \# diretiva undef a um identificador que não tem nenhuma definição anterior; isso garante que o identificador seja indefinido.</span><span class="sxs-lookup"><span data-stu-id="4c29f-114">You can apply the \#undef directive to an identifier that has no previous definition; this ensures that the identifier is undefined.</span></span> <span data-ttu-id="4c29f-115">A substituição de macro não é executada em \# instruções undef.</span><span class="sxs-lookup"><span data-stu-id="4c29f-115">Macro replacement is not performed within \#undef statements.</span></span>

<span data-ttu-id="4c29f-116">A \# diretiva undef normalmente é emparelhada com uma diretiva de [ \# definição](dx-graphics-hlsl-appendix-pre-define.md) para criar uma região em um programa de origem no qual um identificador tem um significado especial.</span><span class="sxs-lookup"><span data-stu-id="4c29f-116">The \#undef directive is typically paired with a [\#define](dx-graphics-hlsl-appendix-pre-define.md) directive to create a region in a source program in which an identifier has a special meaning.</span></span> <span data-ttu-id="4c29f-117">Por exemplo, uma função específica do programa de origem pode usar constantes manifestas para definir os valores específicos que não afetam o restante do programa.</span><span class="sxs-lookup"><span data-stu-id="4c29f-117">For example, a specific function of the source program can use manifest constants to define environment-specific values that do not affect the rest of the program.</span></span> <span data-ttu-id="4c29f-118">A \# diretiva undef também funciona com a diretiva [) para controlar a compilação condicional do programa de origem.</span><span class="sxs-lookup"><span data-stu-id="4c29f-118">The \#undef directive also works with the [) directive to control conditional compilation of the source program.</span></span>

<span data-ttu-id="4c29f-119">Constantes e macros podem ser indefinidas na linha de comando usando a opção/U, seguida pelos identificadores para serem indefinidos.</span><span class="sxs-lookup"><span data-stu-id="4c29f-119">Constants and macros can be undefined from the command line using the /U option, followed by the identifiers to be undefined.</span></span> <span data-ttu-id="4c29f-120">Isso é equivalente a adicionar uma sequência de \# diretivas undef no início do arquivo de origem.</span><span class="sxs-lookup"><span data-stu-id="4c29f-120">This is equivalent to adding a sequence of \#undef directives at the beginning of the source file.</span></span>

## <a name="examples"></a><span data-ttu-id="4c29f-121">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4c29f-121">Examples</span></span>

<span data-ttu-id="4c29f-122">O exemplo a seguir mostra como usar a \# diretiva undef para remover definições de uma constante simbólica e uma macro.</span><span class="sxs-lookup"><span data-stu-id="4c29f-122">The following example shows how to use the \#undef directive to remove definitions of a symbolic constant and a macro.</span></span>


```
#define WIDTH           80
#define ADD( X, Y )     (X) + (Y)

#undef WIDTH
#undef ADD
```



## <a name="see-also"></a><span data-ttu-id="4c29f-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="4c29f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c29f-124">Diretivas de pré-processador (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4c29f-124">Preprocessor Directives (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[<span data-ttu-id="4c29f-125">\#definir diretiva (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4c29f-125">\#define Directive (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-pre-define.md)
</dt> <dt>

[<span data-ttu-id="4c29f-126">\#se,)</span><span class="sxs-lookup"><span data-stu-id="4c29f-126">\#if, )</span></span>](dx-graphics-hlsl-appendix-pre-if.md)
</dt> </dl>

 

 





