---
title: opção/Server
description: A opção/Server direciona o compilador MIDL para gerar arquivos de origem C do lado do servidor para uma interface RPC.
ms.assetid: c5ca6a47-e8b0-4a13-ba73-2d35a9ac8240
keywords:
- /Server switch MIDL
topic_type:
- apiref
api_name:
- /server
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31449133fa795a90d1f11d8c06b960b74909548d
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104006562"
---
# <a name="server-switch"></a><span data-ttu-id="9ecc3-104">opção/Server</span><span class="sxs-lookup"><span data-stu-id="9ecc3-104">/server switch</span></span>

<span data-ttu-id="9ecc3-105">A opção **/Server** direciona o compilador MIDL para gerar arquivos de origem C do lado do servidor para uma interface RPC.</span><span class="sxs-lookup"><span data-stu-id="9ecc3-105">The **/server** switch directs the MIDL compiler to generate server-side C source files for an RPC interface.</span></span>

``` syntax
midl /server { stub | none }
```

## <a name="switch-options"></a><span data-ttu-id="9ecc3-106">Opções de comutação</span><span class="sxs-lookup"><span data-stu-id="9ecc3-106">Switch Options</span></span>

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="stub"></span><span id="STUB"></span>

<span data-ttu-id="9ecc3-107"><span id="stub"></span><span id="STUB"></span>stub \* \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="9ecc3-107"><span id="stub"></span><span id="STUB"></span>\*\*\*\*stub\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="9ecc3-108">Gera os arquivos do lado do servidor.</span><span class="sxs-lookup"><span data-stu-id="9ecc3-108">Generates the server-side files.</span></span>

</dd> <dt>

<span id="none"></span><span id="NONE"></span>

<span data-ttu-id="9ecc3-109"><span id="none"></span><span id="NONE"></span>nenhum \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="9ecc3-109"><span id="none"></span><span id="NONE"></span>\*\*\*\*none\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="9ecc3-110">Não gera arquivos do lado do servidor.</span><span class="sxs-lookup"><span data-stu-id="9ecc3-110">Does not generate server-side files.</span></span>

</dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9ecc3-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="9ecc3-111">Remarks</span></span>

<span data-ttu-id="9ecc3-112">Quando a opção **/Server** não é especificada, o compilador MIDL gera o arquivo stub do servidor.</span><span class="sxs-lookup"><span data-stu-id="9ecc3-112">When the **/server** switch is not specified, the MIDL compiler generates the server stub file.</span></span> <span data-ttu-id="9ecc3-113">Essa opção não afeta as interfaces OLE.</span><span class="sxs-lookup"><span data-stu-id="9ecc3-113">This switch does not affect OLE interfaces.</span></span>

<span data-ttu-id="9ecc3-114">A opção **None** não faz com que nenhum arquivo seja gerado.</span><span class="sxs-lookup"><span data-stu-id="9ecc3-114">The **none** option causes no files to be generated.</span></span>

<span data-ttu-id="9ecc3-115">A opção **/Server** tem precedência sobre a opção **/sstub**</span><span class="sxs-lookup"><span data-stu-id="9ecc3-115">The **/server** switch takes precedence over the **/sstub** switch.</span></span>

## <a name="examples"></a><span data-ttu-id="9ecc3-116">Exemplos</span><span class="sxs-lookup"><span data-stu-id="9ecc3-116">Examples</span></span>

<span data-ttu-id="9ecc3-117">**MIDL/Server None**</span><span class="sxs-lookup"><span data-stu-id="9ecc3-117">**midl /server none**</span></span>

<span data-ttu-id="9ecc3-118">**stub do MIDL/Server**</span><span class="sxs-lookup"><span data-stu-id="9ecc3-118">**midl /server stub**</span></span>

## <a name="see-also"></a><span data-ttu-id="9ecc3-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="9ecc3-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ecc3-120">Sintaxe de linha de comando MIDL geral</span><span class="sxs-lookup"><span data-stu-id="9ecc3-120">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="9ecc3-121">**/Client**</span><span class="sxs-lookup"><span data-stu-id="9ecc3-121">**/client**</span></span>](-client.md)
</dt> <dt>

[<span data-ttu-id="9ecc3-122">**/sstub**</span><span class="sxs-lookup"><span data-stu-id="9ecc3-122">**/sstub**</span></span>](-sstub.md)
</dt> </dl>

 

 




