---
title: opção/use_epv
description: A \_ opção/use EPV instrui o compilador MIDL a gerar código stub de servidor que chama a rotina de aplicativo de servidor por meio de um vetor de ponto de entrada (EPV), em vez de uma chamada estática. O uso desse atributo não é recomendado.
ms.assetid: 2853d836-ded3-412a-916b-1143968123a2
keywords:
- /use_epv MIDL do comutador
topic_type:
- apiref
api_name:
- /use_epv
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec73b5cb9833c15a77c96a784e1ded88d266f9a6
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105785439"
---
# <a name="use_epv-switch"></a><span data-ttu-id="0f953-105">\_comutador/use EPV</span><span class="sxs-lookup"><span data-stu-id="0f953-105">/use\_epv switch</span></span>

<span data-ttu-id="0f953-106">A opção **/use \_ EPV** INSTRUI o compilador MIDL a gerar código stub de servidor que chama a rotina de aplicativo de servidor por meio de um vetor de ponto de entrada (EPV), em vez de uma chamada estática.</span><span class="sxs-lookup"><span data-stu-id="0f953-106">The **/use\_epv** switch directs the MIDL compiler to generate server stub code that calls the server application routine through an entry-point vector (epv), rather than by a static call.</span></span> <span data-ttu-id="0f953-107">O uso desse atributo não é recomendado.</span><span class="sxs-lookup"><span data-stu-id="0f953-107">The use of this attribute is not recommended.</span></span>

``` syntax
midl /use_epv
```

## <a name="switch-options"></a><span data-ttu-id="0f953-108">Opções de comutação</span><span class="sxs-lookup"><span data-stu-id="0f953-108">Switch Options</span></span>

<span data-ttu-id="0f953-109">Essa opção não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="0f953-109">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="0f953-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="0f953-110">Remarks</span></span>

<span data-ttu-id="0f953-111">Normalmente, os aplicativos exigem ligação estática para a rotina de aplicativo do servidor.</span><span class="sxs-lookup"><span data-stu-id="0f953-111">Typically, applications require static linkage to the server application routine.</span></span> <span data-ttu-id="0f953-112">O compilador MIDL gera tal chamada por padrão.</span><span class="sxs-lookup"><span data-stu-id="0f953-112">The MIDL compiler generates such a call by default.</span></span> <span data-ttu-id="0f953-113">No entanto, se um aplicativo exigir que o stub do servidor chame a rotina de aplicativo do servidor usando o EPV, a opção **/use \_ EPV** deverá ser especificada.</span><span class="sxs-lookup"><span data-stu-id="0f953-113">However, if an application requires the server stub to call the server application routine by using the epv, the **/use\_epv** switch must be specified.</span></span> <span data-ttu-id="0f953-114">Quando a opção **/use \_ EPV** é especificada, o compilador MIDL gera um EPV padrão.</span><span class="sxs-lookup"><span data-stu-id="0f953-114">When the **/use\_epv** switch is specified, the MIDL compiler generates a default epv.</span></span> <span data-ttu-id="0f953-115">Esse EPV padrão será usado se o aplicativo não registrar outro EPV por meio da chamada [**RpcServerRegisterIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif) .</span><span class="sxs-lookup"><span data-stu-id="0f953-115">This default epv is then used if the application does not register another epv through the [**RpcServerRegisterIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif) call.</span></span>

## <a name="examples"></a><span data-ttu-id="0f953-116">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0f953-116">Examples</span></span>

<span data-ttu-id="0f953-117">**MIDL/use \_ EPV** *filename \* \* *. idl**</span><span class="sxs-lookup"><span data-stu-id="0f953-117">**midl /use\_epv** *filename\*\*\*.idl*\*</span></span>

## <a name="see-also"></a><span data-ttu-id="0f953-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="0f953-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f953-119">Sintaxe de linha de comando MIDL geral</span><span class="sxs-lookup"><span data-stu-id="0f953-119">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="0f953-120">Arquivo de definição de interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="0f953-120">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="0f953-121">**/ \_ \_ EPV padrão**</span><span class="sxs-lookup"><span data-stu-id="0f953-121">**/no\_default\_epv**</span></span>](-no-default-epv.md)
</dt> <dt>

[<span data-ttu-id="0f953-122">**RpcServerRegisterIf**</span><span class="sxs-lookup"><span data-stu-id="0f953-122">**RpcServerRegisterIf**</span></span>](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif)
</dt> </dl>

 

 