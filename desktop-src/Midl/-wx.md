---
title: Comutador/WX
description: A opção/WX instrui o compilador MIDL a lidar com todos os erros no nível de aviso fornecido como erros.
ms.assetid: 1dd9791c-0488-4ca3-8a29-082ae03c3cd4
keywords:
- MIDL do comutador/WX
topic_type:
- apiref
api_name:
- /WX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04b502cea5f686de2951f6f21ab92fdbffef779b
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103823311"
---
# <a name="wx-switch"></a><span data-ttu-id="d576a-104">Comutador/WX</span><span class="sxs-lookup"><span data-stu-id="d576a-104">/WX switch</span></span>

<span data-ttu-id="d576a-105">A opção **/WX** instrui o compilador MIDL a lidar com todos os erros no nível de aviso fornecido como erros.</span><span class="sxs-lookup"><span data-stu-id="d576a-105">The **/WX** switch instructs the MIDL compiler to handle all errors at the given warning level as errors.</span></span>

``` syntax
midl /WX
```

## <a name="switch-options"></a><span data-ttu-id="d576a-106">Opções de comutação</span><span class="sxs-lookup"><span data-stu-id="d576a-106">Switch Options</span></span>

<span data-ttu-id="d576a-107">Essa opção não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="d576a-107">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="d576a-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="d576a-108">Remarks</span></span>

<span data-ttu-id="d576a-109">Se a opção **/WX** for especificada e a opção [**/w**](-w.md)*n* não for especificada, todos os avisos no nível padrão, nível 1, serão tratados como erros.</span><span class="sxs-lookup"><span data-stu-id="d576a-109">If the **/WX** switch is specified and the [**/W**](-w.md)*n* switch is not specified, all warnings at the default level, level 1, are treated as errors.</span></span>

<span data-ttu-id="d576a-110">A opção [**/w**](-w.md)*n* instrui o compilador a exibir todos os avisos no nível *n* e o **/WX** instrui o compilador a lidar com todos os avisos como erros.</span><span class="sxs-lookup"><span data-stu-id="d576a-110">The [**/W**](-w.md)*n* switch directs the compiler to display all warnings at level *n* and **/WX** directs the compiler to handle all warnings as errors.</span></span> <span data-ttu-id="d576a-111">A combinação dessas duas opções direciona o compilador para lidar com todos os avisos no nível *n* como erros.</span><span class="sxs-lookup"><span data-stu-id="d576a-111">The combination of these two switches directs the compiler to handle all warnings at level *n* as errors.</span></span>

<span data-ttu-id="d576a-112">Os erros são diferentes dos avisos.</span><span class="sxs-lookup"><span data-stu-id="d576a-112">Errors are different from warnings.</span></span> <span data-ttu-id="d576a-113">Os erros fazem com que o compilador MIDL pare o processamento do arquivo IDL.</span><span class="sxs-lookup"><span data-stu-id="d576a-113">Errors cause the MIDL compiler to halt processing of the IDL file.</span></span> <span data-ttu-id="d576a-114">Os avisos fazem com que o compilador MIDL emita uma mensagem informativa e continue processando o arquivo IDL.</span><span class="sxs-lookup"><span data-stu-id="d576a-114">Warnings cause the MIDL compiler to emit an informational message and continue processing the IDL file.</span></span>

<span data-ttu-id="d576a-115">O nível de aviso zero (0) direciona o compilador MIDL para suprimir informações de aviso.</span><span class="sxs-lookup"><span data-stu-id="d576a-115">Warning-level zero (0) directs the MIDL compiler to suppress warning information.</span></span> <span data-ttu-id="d576a-116">Quando as opções **/W0** e **/WX** são combinadas, o compilador MIDL suprime todas as informações de aviso.</span><span class="sxs-lookup"><span data-stu-id="d576a-116">When the **/W0** and **/WX** switches are combined, the MIDL compiler suppresses all warning information.</span></span> <span data-ttu-id="d576a-117">Nesse caso, a opção **/WX** não tem nenhum efeito.</span><span class="sxs-lookup"><span data-stu-id="d576a-117">In this case, the **/WX** switch has no effect.</span></span>

## <a name="examples"></a><span data-ttu-id="d576a-118">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d576a-118">Examples</span></span>

<span data-ttu-id="d576a-119">**MIDL/WX filename. idl**</span><span class="sxs-lookup"><span data-stu-id="d576a-119">**midl /WX filename.idl**</span></span>

<span data-ttu-id="d576a-120">**MIDL/w3/WX filename. idl**</span><span class="sxs-lookup"><span data-stu-id="d576a-120">**midl /W3 /WX filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="d576a-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="d576a-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d576a-122">Sintaxe de linha de comando MIDL geral</span><span class="sxs-lookup"><span data-stu-id="d576a-122">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="d576a-123">**/W**</span><span class="sxs-lookup"><span data-stu-id="d576a-123">**/W**</span></span>](-w.md)
</dt> </dl>

 

 




