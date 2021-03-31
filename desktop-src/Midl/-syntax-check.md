---
title: opção/syntax_check
description: A \_ opção check/Syntax indica que o compilador verifica apenas a sintaxe e não gera arquivos de saída.
ms.assetid: 8d9139d3-6018-48a7-bea5-0c843b6273d3
keywords:
- /syntax_check MIDL do comutador
topic_type:
- apiref
api_name:
- /syntax_check
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51b064a096b5064e6996ea4288c9ae9d4a798c2e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103638561"
---
# <a name="syntax_check-switch"></a><span data-ttu-id="94875-104">opção de verificação de/Syntax \_</span><span class="sxs-lookup"><span data-stu-id="94875-104">/syntax\_check switch</span></span>

<span data-ttu-id="94875-105">A **opção \_ check/Syntax** indica que o compilador verifica apenas a sintaxe e não gera arquivos de saída.</span><span class="sxs-lookup"><span data-stu-id="94875-105">The **/syntax\_check** switch indicates that the compiler checks only syntax and does not generate output files.</span></span>

``` syntax
midl /syntax_check
midl /Zs
```

## <a name="switch-options"></a><span data-ttu-id="94875-106">Opções de comutação</span><span class="sxs-lookup"><span data-stu-id="94875-106">Switch Options</span></span>

<span data-ttu-id="94875-107">Essa opção não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="94875-107">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="94875-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="94875-108">Remarks</span></span>

<span data-ttu-id="94875-109">Essa opção substitui todas as outras opções que especificam informações sobre os arquivos de saída.</span><span class="sxs-lookup"><span data-stu-id="94875-109">This switch overrides all other switches that specify information about output files.</span></span>

<span data-ttu-id="94875-110">Você também pode especificar o modo de verificação de sintaxe com a opção de compilador MIDL [**/ZS**](-zs.md).</span><span class="sxs-lookup"><span data-stu-id="94875-110">You can also specify syntax-checking mode with the MIDL compiler option [**/Zs**](-zs.md).</span></span>

## <a name="examples"></a><span data-ttu-id="94875-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="94875-111">Examples</span></span>

<span data-ttu-id="94875-112">**MIDL/ZS filename. idl**</span><span class="sxs-lookup"><span data-stu-id="94875-112">**midl /Zs filename.idl**</span></span>

<span data-ttu-id="94875-113">**MIDL/Syntax \_ verificar filename. idl**</span><span class="sxs-lookup"><span data-stu-id="94875-113">**midl /syntax\_check filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="94875-114">Consulte também</span><span class="sxs-lookup"><span data-stu-id="94875-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94875-115">Sintaxe de linha de comando MIDL geral</span><span class="sxs-lookup"><span data-stu-id="94875-115">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="94875-116">**/ZS**</span><span class="sxs-lookup"><span data-stu-id="94875-116">**/Zs**</span></span>](-zs.md)
</dt> </dl>

 

 




