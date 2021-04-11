---
title: comutador/Client
description: A opção/Client instrui o compilador MIDL a gerar arquivos de origem C do lado do cliente para uma interface RPC.
ms.assetid: bce5af72-2201-4b42-9348-cb97f08b7fdf
keywords:
- MIDL do comutador/Client
topic_type:
- apiref
api_name:
- /client
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbf7e17e1893b918d926cd94a93eb8b1c372ee75
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104293333"
---
# <a name="client-switch"></a><span data-ttu-id="aebab-104">comutador/Client</span><span class="sxs-lookup"><span data-stu-id="aebab-104">/client switch</span></span>

<span data-ttu-id="aebab-105">A opção **/Client** instrui o compilador MIDL a gerar arquivos de origem C do lado do cliente para uma interface RPC.</span><span class="sxs-lookup"><span data-stu-id="aebab-105">The **/client** switch directs the MIDL compiler to generate client-side C source files for an RPC interface.</span></span>

``` syntax
midl /client { stub | none }
```

## <a name="switch-options"></a><span data-ttu-id="aebab-106">Opções de comutação</span><span class="sxs-lookup"><span data-stu-id="aebab-106">Switch Options</span></span>

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="stub"></span><span id="STUB"></span>

<span data-ttu-id="aebab-107"><span id="stub"></span><span id="STUB"></span>stub \* \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="aebab-107"><span id="stub"></span><span id="STUB"></span>\*\*\*\*stub\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="aebab-108">Gera os arquivos do lado do cliente.</span><span class="sxs-lookup"><span data-stu-id="aebab-108">Generates the client-side files.</span></span>

</dd> <dt>

<span id="none"></span><span id="NONE"></span>

<span data-ttu-id="aebab-109"><span id="none"></span><span id="NONE"></span>nenhum \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="aebab-109"><span id="none"></span><span id="NONE"></span>\*\*\*\*none\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="aebab-110">Não gera nenhum arquivo do lado do cliente.</span><span class="sxs-lookup"><span data-stu-id="aebab-110">Does not generate any client-side files.</span></span>

</dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="aebab-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="aebab-111">Remarks</span></span>

<span data-ttu-id="aebab-112">Quando a opção **/Client** não é especificada, o compilador MIDL gera o arquivo stub do cliente.</span><span class="sxs-lookup"><span data-stu-id="aebab-112">When the **/client** switch is not specified, the MIDL compiler generates the client stub file.</span></span> <span data-ttu-id="aebab-113">Essa opção não afeta as interfaces OLE.</span><span class="sxs-lookup"><span data-stu-id="aebab-113">This switch does not affect OLE interfaces.</span></span>

<span data-ttu-id="aebab-114">A opção **/Client** tem precedência sobre a opção [**/cstub**](-cstub.md)</span><span class="sxs-lookup"><span data-stu-id="aebab-114">The **/client** switch takes precedence over the [**/cstub**](-cstub.md) switch.</span></span>

## <a name="examples"></a><span data-ttu-id="aebab-115">Exemplos</span><span class="sxs-lookup"><span data-stu-id="aebab-115">Examples</span></span>

<span data-ttu-id="aebab-116">**MIDL/Client None filename. idl**</span><span class="sxs-lookup"><span data-stu-id="aebab-116">**midl /client none filename.idl**</span></span>

<span data-ttu-id="aebab-117">**nome de arquivo stub/Client de MIDL. idl**</span><span class="sxs-lookup"><span data-stu-id="aebab-117">**midl /client stub filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="aebab-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="aebab-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aebab-119">**/cstub**</span><span class="sxs-lookup"><span data-stu-id="aebab-119">**/cstub**</span></span>](-cstub.md)
</dt> <dt>

[<span data-ttu-id="aebab-120">**/Server**</span><span class="sxs-lookup"><span data-stu-id="aebab-120">**/server**</span></span>](-server.md)
</dt> <dt>

[<span data-ttu-id="aebab-121">Sintaxe de linha de comando MIDL geral</span><span class="sxs-lookup"><span data-stu-id="aebab-121">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> </dl>

 

 




