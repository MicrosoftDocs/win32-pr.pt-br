---
title: comutador/Win64
description: A opção/Win64 instrui o compilador MIDL a gerar arquivos stub, ou um arquivo de biblioteca de tipos, para um ambiente de 64 bits. Observe que essa opção está obsoleta.
ms.assetid: 6f4780d3-6415-42af-a8ee-3884a8cebe26
keywords:
- MIDL do comutador/Win64
topic_type:
- apiref
api_name:
- /win64
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e61906126607c0a8d4b81ef76805bb4b7e0d4145
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104293112"
---
# <a name="win64-switch"></a><span data-ttu-id="78977-104">comutador/Win64</span><span class="sxs-lookup"><span data-stu-id="78977-104">/win64 switch</span></span>

<span data-ttu-id="78977-105">A opção **/Win64** instrui o compilador MIDL a gerar arquivos stub, ou um arquivo de biblioteca de tipos, para um ambiente de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="78977-105">The **/win64** switch directs the MIDL compiler to generate stub files, or a type library file, for a 64-bit environment.</span></span>

> [!Note]  
> <span data-ttu-id="78977-106">Essa opção é obsoleta.</span><span class="sxs-lookup"><span data-stu-id="78977-106">This switch is obsolete.</span></span> <span data-ttu-id="78977-107">Em vez disso, use a opção [**/IA64**](-ia64.md) ou [**/AMD64**](-amd64.md) .</span><span class="sxs-lookup"><span data-stu-id="78977-107">Please use the [**/ia64**](-ia64.md) or [**/amd64**](-amd64.md) switch instead.</span></span> <span data-ttu-id="78977-108">A opção **/Win64** é equivalente à opção **/IA64** .</span><span class="sxs-lookup"><span data-stu-id="78977-108">The **/win64** switch is equivalent to the **/ia64** switch.</span></span>

 

``` syntax
midl /win64
```

## <a name="switch-options"></a><span data-ttu-id="78977-109">Opções de comutação</span><span class="sxs-lookup"><span data-stu-id="78977-109">Switch Options</span></span>

<span data-ttu-id="78977-110">Essa opção não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="78977-110">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="78977-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="78977-111">Remarks</span></span>

<span data-ttu-id="78977-112">A opção **/Win64** é equivalente a definir a opção [**/env**](-env.md) como Win64.</span><span class="sxs-lookup"><span data-stu-id="78977-112">The **/win64** switch is equivalent to setting the [**/env**](-env.md) switch to win64.</span></span>

> [!Note]  
> <span data-ttu-id="78977-113">Não é possível usar MIDL.exe para produzir um TLB de 64 bits no Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="78977-113">It is not possible to use MIDL.exe to produce a 64bit tlb on Windows 2000.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="78977-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="78977-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78977-115">**/env**</span><span class="sxs-lookup"><span data-stu-id="78977-115">**/env**</span></span>](-env.md)
</dt> <dt>

[<span data-ttu-id="78977-116">**/ia64**</span><span class="sxs-lookup"><span data-stu-id="78977-116">**/ia64**</span></span>](-ia64.md)
</dt> <dt>

[<span data-ttu-id="78977-117">**/amd64**</span><span class="sxs-lookup"><span data-stu-id="78977-117">**/amd64**</span></span>](-amd64.md)
</dt> </dl>

 

 




