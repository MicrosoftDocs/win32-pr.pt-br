---
title: Opção/w
description: A opção/W especifica o nível de aviso do compilador MIDL. O nível de aviso indica a severidade do aviso.
ms.assetid: ee894d73-cbd1-455f-9836-a6d80cfc95f9
keywords:
- /W opção MIDL
topic_type:
- apiref
api_name:
- /W
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00b1f15ae0c28722adaca8c4b0651606681ce3af
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "105789785"
---
# <a name="w-switch"></a><span data-ttu-id="7d199-105">Opção/w</span><span class="sxs-lookup"><span data-stu-id="7d199-105">/W switch</span></span>

<span data-ttu-id="7d199-106">A opção **/w** especifica o nível de aviso do compilador MIDL.</span><span class="sxs-lookup"><span data-stu-id="7d199-106">The **/W** switch specifies the warning level of the MIDL compiler.</span></span> <span data-ttu-id="7d199-107">O nível de aviso indica a severidade do aviso.</span><span class="sxs-lookup"><span data-stu-id="7d199-107">The warning level indicates the severity of the warning.</span></span>

``` syntax
midl /W level
```

## <a name="switch-options"></a><span data-ttu-id="7d199-108">Opções de comutação</span><span class="sxs-lookup"><span data-stu-id="7d199-108">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="7d199-109">*level*</span><span class="sxs-lookup"><span data-stu-id="7d199-109">*level*</span></span> 
</dt> <dd>

<span data-ttu-id="7d199-110">Especifica o nível de aviso, um número inteiro no intervalo de 0 a 4.</span><span class="sxs-lookup"><span data-stu-id="7d199-110">Specifies the warning level, an integer in the range 0 through 4.</span></span> <span data-ttu-id="7d199-111">Não há espaço entre a opção **/w** e o dígito que indica o valor de nível de aviso.</span><span class="sxs-lookup"><span data-stu-id="7d199-111">There is no space between the **/W** switch and the digit indicating the warning-level value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7d199-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="7d199-112">Remarks</span></span>

<span data-ttu-id="7d199-113">Os níveis de aviso variam de 1 a 4, com um valor de zero significado para não exibir nenhuma informação de aviso.</span><span class="sxs-lookup"><span data-stu-id="7d199-113">Warning levels range from 1 to 4, with a value of zero meaning to display no warning information.</span></span> <span data-ttu-id="7d199-114">O aviso de severidade mais alta é o nível 1.</span><span class="sxs-lookup"><span data-stu-id="7d199-114">The highest-severity warning is level 1.</span></span> <span data-ttu-id="7d199-115">A tabela a seguir descreve os avisos para cada nível de aviso.</span><span class="sxs-lookup"><span data-stu-id="7d199-115">The following table describes the warnings for each warning level.</span></span>



| <span data-ttu-id="7d199-116">Nível de aviso</span><span class="sxs-lookup"><span data-stu-id="7d199-116">Warning level</span></span> | <span data-ttu-id="7d199-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="7d199-117">Description</span></span>                                             | <span data-ttu-id="7d199-118">Exemplo</span><span class="sxs-lookup"><span data-stu-id="7d199-118">Example</span></span>                                                                   |
|---------------|---------------------------------------------------------|---------------------------------------------------------------------------|
| <span data-ttu-id="7d199-119">W0</span><span class="sxs-lookup"><span data-stu-id="7d199-119">W0</span></span>            | <span data-ttu-id="7d199-120">Sem avisos.</span><span class="sxs-lookup"><span data-stu-id="7d199-120">No warnings.</span></span>                                            |                                                                           |
| <span data-ttu-id="7d199-121">W1</span><span class="sxs-lookup"><span data-stu-id="7d199-121">W1</span></span>            | <span data-ttu-id="7d199-122">Avisos graves que podem causar erros de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7d199-122">Severe warnings that can cause application errors.</span></span>      | <span data-ttu-id="7d199-123">Nenhum identificador de associação especificado, ponteiros sem atributo, opções conflitantes.</span><span class="sxs-lookup"><span data-stu-id="7d199-123">No binding handle specified, unattributed pointers, conflicting switches.</span></span> |
| <span data-ttu-id="7d199-124">W2</span><span class="sxs-lookup"><span data-stu-id="7d199-124">W2</span></span>            | <span data-ttu-id="7d199-125">Pode causar problemas no ambiente operacional do usuário.</span><span class="sxs-lookup"><span data-stu-id="7d199-125">May cause problems in the user's operating environment.</span></span> | <span data-ttu-id="7d199-126">O comprimento do identificador excede 31 caracteres.</span><span class="sxs-lookup"><span data-stu-id="7d199-126">Identifier length exceeds 31 characters.</span></span> <span data-ttu-id="7d199-127">Nenhum ARM de União padrão especificado.</span><span class="sxs-lookup"><span data-stu-id="7d199-127">No default union arm specified.</span></span>  |
| <span data-ttu-id="7d199-128">W3</span><span class="sxs-lookup"><span data-stu-id="7d199-128">W3</span></span>            | <span data-ttu-id="7d199-129">Reservado.</span><span class="sxs-lookup"><span data-stu-id="7d199-129">Reserved.</span></span>                                               |                                                                           |
| <span data-ttu-id="7d199-130">S4</span><span class="sxs-lookup"><span data-stu-id="7d199-130">W4</span></span>            | <span data-ttu-id="7d199-131">Nível de aviso mais baixo.</span><span class="sxs-lookup"><span data-stu-id="7d199-131">Lowest warning level.</span></span>                                   | <span data-ttu-id="7d199-132">Construções não-ANSI C.</span><span class="sxs-lookup"><span data-stu-id="7d199-132">Non-ANSI C constructs.</span></span>                                                    |



 

<span data-ttu-id="7d199-133">Os avisos são diferentes dos erros.</span><span class="sxs-lookup"><span data-stu-id="7d199-133">Warnings are different from errors.</span></span> <span data-ttu-id="7d199-134">Os erros fazem com que o compilador MIDL pare o processamento do arquivo IDL.</span><span class="sxs-lookup"><span data-stu-id="7d199-134">Errors cause the MIDL compiler to halt processing of the IDL file.</span></span> <span data-ttu-id="7d199-135">Os avisos fazem com que o compilador MIDL emita uma mensagem informativa e continue processando o arquivo IDL.</span><span class="sxs-lookup"><span data-stu-id="7d199-135">Warnings cause the MIDL compiler to emit an informational message and continue processing the IDL file.</span></span>

<span data-ttu-id="7d199-136">O nível de aviso definido pela opção **/w** pode ser usado com a opção [**/WX**](-wx.md) para fazer com que o compilador MIDL pare o processamento do arquivo IDL.</span><span class="sxs-lookup"><span data-stu-id="7d199-136">The warning level set by the **/W** switch can be used with the [**/WX**](-wx.md) switch to cause the MIDL compiler to halt processing of the IDL file.</span></span>

<span data-ttu-id="7d199-137">A opção **/w** comporta-se da mesma forma que a opção [**/Warn**](-warn.md)</span><span class="sxs-lookup"><span data-stu-id="7d199-137">The **/W** switch behaves the same as the [**/warn**](-warn.md) switch.</span></span>

## <a name="examples"></a><span data-ttu-id="7d199-138">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7d199-138">Examples</span></span>

<span data-ttu-id="7d199-139">**MIDL/W2 filename. idl**</span><span class="sxs-lookup"><span data-stu-id="7d199-139">**midl /W2 filename.idl**</span></span>

<span data-ttu-id="7d199-140">**MIDL/W4 bar. idl**</span><span class="sxs-lookup"><span data-stu-id="7d199-140">**midl /W4 bar.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="7d199-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="7d199-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d199-142">Sintaxe de linha de comando MIDL geral</span><span class="sxs-lookup"><span data-stu-id="7d199-142">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="7d199-143">**/Warn**</span><span class="sxs-lookup"><span data-stu-id="7d199-143">**/warn**</span></span>](-warn.md)
</dt> </dl>

 

 




