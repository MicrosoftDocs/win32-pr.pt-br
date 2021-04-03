---
title: Comutador/ZS
description: A opção/Zs indica que o compilador verifica apenas a sintaxe e não gera arquivos de saída.
ms.assetid: 5ff44607-12c3-4a2d-8a7f-2056504990e2
keywords:
- MIDL do comutador/ZS
topic_type:
- apiref
api_name:
- /Zs
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 469802434d54319aa55c1e409ccb8d64e942836f
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103638456"
---
# <a name="zs-switch"></a><span data-ttu-id="fc7d0-104">Comutador/ZS</span><span class="sxs-lookup"><span data-stu-id="fc7d0-104">/Zs switch</span></span>

<span data-ttu-id="fc7d0-105">A opção **/ZS** indica que o compilador verifica apenas a sintaxe e não gera arquivos de saída.</span><span class="sxs-lookup"><span data-stu-id="fc7d0-105">The **/Zs** switch indicates that the compiler only checks syntax and does not generate output files.</span></span>

``` syntax
midl /Zs
midl /syntax_check
```

## <a name="switch-options"></a><span data-ttu-id="fc7d0-106">Opções de comutação</span><span class="sxs-lookup"><span data-stu-id="fc7d0-106">Switch Options</span></span>

<span data-ttu-id="fc7d0-107">Essa opção não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="fc7d0-107">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="fc7d0-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="fc7d0-108">Remarks</span></span>

<span data-ttu-id="fc7d0-109">Essa opção substitui todas as outras opções que especificam informações sobre os arquivos de saída.</span><span class="sxs-lookup"><span data-stu-id="fc7d0-109">This switch overrides all other switches that specify information about output files.</span></span>

<span data-ttu-id="fc7d0-110">Você também pode especificar o modo de verificação de sintaxe com a [**\_ verificação/Syntax**](-syntax-check.md)do compilador MIDL.</span><span class="sxs-lookup"><span data-stu-id="fc7d0-110">You can also specify syntax-checking mode with the MIDL compiler switch [**/syntax\_check**](-syntax-check.md).</span></span>

## <a name="examples"></a><span data-ttu-id="fc7d0-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="fc7d0-111">Examples</span></span>

<span data-ttu-id="fc7d0-112">**MIDL/ZS filename. idl**</span><span class="sxs-lookup"><span data-stu-id="fc7d0-112">**midl /Zs filename.idl**</span></span>

<span data-ttu-id="fc7d0-113">**MIDL/Syntax \_ verificar filename. idl**</span><span class="sxs-lookup"><span data-stu-id="fc7d0-113">**midl /syntax\_check filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="fc7d0-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="fc7d0-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc7d0-115">Sintaxe de linha de comando MIDL geral</span><span class="sxs-lookup"><span data-stu-id="fc7d0-115">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="fc7d0-116">**verificação de/Syntax \_**</span><span class="sxs-lookup"><span data-stu-id="fc7d0-116">**/syntax\_check**</span></span>](-syntax-check.md)
</dt> </dl>

 

 




