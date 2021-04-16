---
title: comutador/notlb
description: A opção/notlb impede que o compilador MIDL gere um arquivo de biblioteca de tipos (TLB).
ms.assetid: 58f4210d-d3c3-42ce-b311-4ddd85bc396a
keywords:
- MIDL do comutador/notlb
topic_type:
- apiref
api_name:
- /notlb
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81911b6afb00d61713f966ba9e1981b979e51008
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104453777"
---
# <a name="notlb-switch"></a><span data-ttu-id="cdbd4-104">comutador/notlb</span><span class="sxs-lookup"><span data-stu-id="cdbd4-104">/notlb switch</span></span>

<span data-ttu-id="cdbd4-105">A opção **/notlb** impede que o compilador MIDL gere um arquivo de biblioteca de tipos (tlb).</span><span class="sxs-lookup"><span data-stu-id="cdbd4-105">The **/notlb** switch prevents the MIDL compiler from generating a type library (TLB) file.</span></span>

``` syntax
midl /notlb
```

## <a name="switch-options"></a><span data-ttu-id="cdbd4-106">Opções de comutação</span><span class="sxs-lookup"><span data-stu-id="cdbd4-106">Switch Options</span></span>

<span data-ttu-id="cdbd4-107">Essa opção não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="cdbd4-107">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="cdbd4-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="cdbd4-108">Remarks</span></span>

<span data-ttu-id="cdbd4-109">Por padrão, o compilador MIDL irá gerar um arquivo TLB sempre que encontrar uma instrução de [**biblioteca**](library.md) .</span><span class="sxs-lookup"><span data-stu-id="cdbd4-109">By default, the MIDL compiler will generate a TLB file whenever it encounters a [**LIBRARY**](library.md) statement.</span></span> <span data-ttu-id="cdbd4-110">Essa opção substitui o comportamento padrão.</span><span class="sxs-lookup"><span data-stu-id="cdbd4-110">This switch overrides the default behavior.</span></span>

<span data-ttu-id="cdbd4-111">Quando a opção **/notlb** é especificada, todos os outros stubs, cabeçalhos, etc. são gerados como de costume.</span><span class="sxs-lookup"><span data-stu-id="cdbd4-111">When the **/notlb** option is specified, all other stubs, headers, etc. are generated as usual.</span></span>

## <a name="see-also"></a><span data-ttu-id="cdbd4-112">Confira também</span><span class="sxs-lookup"><span data-stu-id="cdbd4-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cdbd4-113">**/tlb**</span><span class="sxs-lookup"><span data-stu-id="cdbd4-113">**/tlb**</span></span>](-tlb.md)
</dt> </dl>

 

 




