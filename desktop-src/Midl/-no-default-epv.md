---
title: opção/no_default_epv
description: A \_ opção EPV padrão de// \_ r instrui o compilador MIDL a não gerar um vetor de ponto de entrada (EPV) padrão. O uso desse atributo não é recomendado.
ms.assetid: 160b5fd3-cd9c-4f51-8c35-6cddab120021
keywords:
- /no_default_epv MIDL do comutador
topic_type:
- apiref
api_name:
- /no_default_epv
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0a6e39319c5f03c1cd41959a009307b07bef66f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103917192"
---
# <a name="no_default_epv-switch"></a><span data-ttu-id="e634b-105">\_opção de EPV padrão de//. \_</span><span class="sxs-lookup"><span data-stu-id="e634b-105">/no\_default\_epv switch</span></span>

<span data-ttu-id="e634b-106">A **opção \_ \_ EPV padrão de//** r instrui o compilador MIDL a não gerar um vetor de ponto de entrada (EPV) padrão.</span><span class="sxs-lookup"><span data-stu-id="e634b-106">The **/no\_default\_epv** switch directs the MIDL compiler not to generate a default entry-point vector (epv).</span></span> <span data-ttu-id="e634b-107">O uso desse atributo não é recomendado.</span><span class="sxs-lookup"><span data-stu-id="e634b-107">The use of this attribute is not recommended.</span></span>

``` syntax
midl /no_default_epv
```

## <a name="switch-options"></a><span data-ttu-id="e634b-108">Opções de comutação</span><span class="sxs-lookup"><span data-stu-id="e634b-108">Switch Options</span></span>

<span data-ttu-id="e634b-109">Essa opção não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="e634b-109">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="e634b-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="e634b-110">Remarks</span></span>

<span data-ttu-id="e634b-111">Nesse caso, o aplicativo deve registrar um EPV com a chamada [**RpcServerRegisterIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif) .</span><span class="sxs-lookup"><span data-stu-id="e634b-111">In this case, the application must register an epv with the [**RpcServerRegisterIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif) call.</span></span> <span data-ttu-id="e634b-112">Compare essa opção com o comutador [**/use \_ EPV**](-use-epv.md) .</span><span class="sxs-lookup"><span data-stu-id="e634b-112">Compare this switch with the [**/use\_epv**](-use-epv.md) switch.</span></span>

## <a name="examples"></a><span data-ttu-id="e634b-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e634b-113">Examples</span></span>

<span data-ttu-id="e634b-114">**MIDL/ \_ Default \_ EPV filename. idl**</span><span class="sxs-lookup"><span data-stu-id="e634b-114">**midl /no\_default\_epv filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="e634b-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="e634b-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e634b-116">Sintaxe de linha de comando MIDL geral</span><span class="sxs-lookup"><span data-stu-id="e634b-116">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="e634b-117">Arquivo de definição de interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="e634b-117">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="e634b-118">**/Use \_ EPV**</span><span class="sxs-lookup"><span data-stu-id="e634b-118">**/use\_epv**</span></span>](-use-epv.md)
</dt> <dt>

[<span data-ttu-id="e634b-119">**RpcServerRegisterIf**</span><span class="sxs-lookup"><span data-stu-id="e634b-119">**RpcServerRegisterIf**</span></span>](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif)
</dt> </dl>

 

 