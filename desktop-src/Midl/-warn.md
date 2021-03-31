---
title: comutador/Warn
description: A opção/warn especifica o nível de aviso do compilador MIDL.
ms.assetid: b1e26e67-8c47-40a2-8f34-22273ddfaa1d
keywords:
- MIDL do comutador/Warn
topic_type:
- apiref
api_name:
- /warn
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebb2effd65175bf7bf54cb74cb63a56af0278784
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103638468"
---
# <a name="warn-switch"></a><span data-ttu-id="a1bad-104">comutador/Warn</span><span class="sxs-lookup"><span data-stu-id="a1bad-104">/warn switch</span></span>

<span data-ttu-id="a1bad-105">A opção **/Warn** especifica o nível de aviso do compilador MIDL.</span><span class="sxs-lookup"><span data-stu-id="a1bad-105">The **/warn** switch specifies the warning level of the MIDL compiler.</span></span>

``` syntax
midl /warn level
```

## <a name="switch-options"></a><span data-ttu-id="a1bad-106">Opções de comutação</span><span class="sxs-lookup"><span data-stu-id="a1bad-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="a1bad-107">*level*</span><span class="sxs-lookup"><span data-stu-id="a1bad-107">*level*</span></span> 
</dt> <dd>

<span data-ttu-id="a1bad-108">Especifica o nível de aviso, um número inteiro no intervalo de 0 a 4.</span><span class="sxs-lookup"><span data-stu-id="a1bad-108">Specifies the warning level, an integer in the range 0 through 4.</span></span> <span data-ttu-id="a1bad-109">Não há espaço entre a opção **/Warn** e o dígito que indica o valor de nível de aviso.</span><span class="sxs-lookup"><span data-stu-id="a1bad-109">There is no space between the **/warn** switch and the digit indicating the warning-level value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a1bad-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="a1bad-110">Remarks</span></span>

<span data-ttu-id="a1bad-111">O nível de aviso indica a severidade do aviso.</span><span class="sxs-lookup"><span data-stu-id="a1bad-111">The warning level indicates the severity of the warning.</span></span> <span data-ttu-id="a1bad-112">Os níveis de aviso variam de 1 a 4, com um valor de zero significado para não exibir nenhuma informação de aviso.</span><span class="sxs-lookup"><span data-stu-id="a1bad-112">Warning levels range from 1 to 4, with a value of zero meaning to display no warning information.</span></span> <span data-ttu-id="a1bad-113">O aviso de severidade mais alta é o nível 1.</span><span class="sxs-lookup"><span data-stu-id="a1bad-113">The highest severity warning is level 1.</span></span> <span data-ttu-id="a1bad-114">A tabela a seguir descreve os avisos para cada nível de aviso.</span><span class="sxs-lookup"><span data-stu-id="a1bad-114">The following table describes the warnings for each warning level.</span></span>



| <span data-ttu-id="a1bad-115">Nível de aviso</span><span class="sxs-lookup"><span data-stu-id="a1bad-115">Warning level</span></span> | <span data-ttu-id="a1bad-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="a1bad-116">Description</span></span>                                             | <span data-ttu-id="a1bad-117">Exemplo</span><span class="sxs-lookup"><span data-stu-id="a1bad-117">Example</span></span>                                                                   |
|---------------|---------------------------------------------------------|---------------------------------------------------------------------------|
| <span data-ttu-id="a1bad-118">0</span><span class="sxs-lookup"><span data-stu-id="a1bad-118">0</span></span>             | <span data-ttu-id="a1bad-119">Sem avisos.</span><span class="sxs-lookup"><span data-stu-id="a1bad-119">No warnings.</span></span>                                            |                                                                           |
| <span data-ttu-id="a1bad-120">1</span><span class="sxs-lookup"><span data-stu-id="a1bad-120">1</span></span>             | <span data-ttu-id="a1bad-121">Avisos graves que podem causar erros de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a1bad-121">Severe warnings that can cause application errors.</span></span>      | <span data-ttu-id="a1bad-122">Nenhum identificador de associação especificado, ponteiros sem atributo, opções conflitantes.</span><span class="sxs-lookup"><span data-stu-id="a1bad-122">No binding handle specified, unattributed pointers, conflicting switches.</span></span> |
| <span data-ttu-id="a1bad-123">2</span><span class="sxs-lookup"><span data-stu-id="a1bad-123">2</span></span>             | <span data-ttu-id="a1bad-124">Pode causar problemas no ambiente operacional do usuário.</span><span class="sxs-lookup"><span data-stu-id="a1bad-124">May cause problems in the user's operating environment.</span></span> | <span data-ttu-id="a1bad-125">O comprimento do identificador excede 31 caracteres.</span><span class="sxs-lookup"><span data-stu-id="a1bad-125">Identifier length exceeds 31 characters.</span></span> <span data-ttu-id="a1bad-126">Nenhum ARM de União padrão especificado.</span><span class="sxs-lookup"><span data-stu-id="a1bad-126">No default union arm specified.</span></span>  |
| <span data-ttu-id="a1bad-127">3</span><span class="sxs-lookup"><span data-stu-id="a1bad-127">3</span></span>             | <span data-ttu-id="a1bad-128">Reservado.</span><span class="sxs-lookup"><span data-stu-id="a1bad-128">Reserved.</span></span>                                               |                                                                           |
| <span data-ttu-id="a1bad-129">4</span><span class="sxs-lookup"><span data-stu-id="a1bad-129">4</span></span>             | <span data-ttu-id="a1bad-130">Nível de aviso mais baixo.</span><span class="sxs-lookup"><span data-stu-id="a1bad-130">Lowest warning level.</span></span>                                   | <span data-ttu-id="a1bad-131">Construções não-ANSI C.</span><span class="sxs-lookup"><span data-stu-id="a1bad-131">Non-ANSI C constructs.</span></span>                                                    |



 

<span data-ttu-id="a1bad-132">Os avisos são diferentes dos erros.</span><span class="sxs-lookup"><span data-stu-id="a1bad-132">Warnings are different from errors.</span></span> <span data-ttu-id="a1bad-133">Os erros fazem com que o compilador MIDL pare o processamento do arquivo IDL.</span><span class="sxs-lookup"><span data-stu-id="a1bad-133">Errors cause the MIDL compiler to halt processing of the IDL file.</span></span> <span data-ttu-id="a1bad-134">Os avisos fazem com que o compilador MIDL emita uma mensagem informativa e continue processando o arquivo IDL.</span><span class="sxs-lookup"><span data-stu-id="a1bad-134">Warnings cause the MIDL compiler to emit an informational message and continue processing the IDL file.</span></span>

<span data-ttu-id="a1bad-135">O nível de aviso definido pela opção **/Warn** pode ser usado com a opção [**WX**](-wx.md) para fazer com que o compilador MIDL pare o processamento do arquivo IDL.</span><span class="sxs-lookup"><span data-stu-id="a1bad-135">The warning level set by the **/warn** switch can be used with the [**WX**](-wx.md) switch to cause the MIDL compiler to halt processing of the IDL file.</span></span>

<span data-ttu-id="a1bad-136">A opção **/Warn** se comporta da mesma forma que a opção [**/w**](-w.md) .</span><span class="sxs-lookup"><span data-stu-id="a1bad-136">The **/warn** switch behaves the same as the [**/W**](-w.md) switch.</span></span>

## <a name="examples"></a><span data-ttu-id="a1bad-137">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a1bad-137">Examples</span></span>

<span data-ttu-id="a1bad-138">**MIDL/warn2 filename. idl**</span><span class="sxs-lookup"><span data-stu-id="a1bad-138">**midl /warn2 filename.idl**</span></span>

<span data-ttu-id="a1bad-139">**MIDL/warn4 bar. idl**</span><span class="sxs-lookup"><span data-stu-id="a1bad-139">**midl /warn4 bar.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="a1bad-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="a1bad-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1bad-141">Sintaxe de linha de comando MIDL geral</span><span class="sxs-lookup"><span data-stu-id="a1bad-141">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> </dl>

 

 




