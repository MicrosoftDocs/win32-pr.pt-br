---
title: opção/sal_local
description: O \_ comutador local/sal DIRECIONA MIDL para gerar também anotações sal para parâmetros de métodos de interface marcados como \ local \. A opção/sal também deve estar presente.
ms.assetid: 49AFC3F6-EAD5-45F6-8862-EFB3D9C479D1
keywords:
- /sal_local MIDL do comutador
topic_type:
- apiref
api_name:
- /sal_local
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03263b94b809407d1c3e55c2f3dacc5e10684bc1
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "105759065"
---
# <a name="sal_local-switch"></a><span data-ttu-id="3a5fa-105">\_comutador local/sal</span><span class="sxs-lookup"><span data-stu-id="3a5fa-105">/sal\_local switch</span></span>

<span data-ttu-id="3a5fa-106">O comutador **\_ local/sal** direciona MIDL para gerar também anotações sal para parâmetros de métodos de interface marcados como [**\[ \] local**](local.md).</span><span class="sxs-lookup"><span data-stu-id="3a5fa-106">The **/sal\_local** switch directs MIDL to also generate SAL annotations for parameters of interface methods marked [**\[local\]**](local.md).</span></span> <span data-ttu-id="3a5fa-107">A opção [**/sal**](-sal.md) também deve estar presente.</span><span class="sxs-lookup"><span data-stu-id="3a5fa-107">The [**/sal**](-sal.md) switch must also be present.</span></span>

``` syntax
midl /sal /sal_local
```

## <a name="switch-options"></a><span data-ttu-id="3a5fa-108">Opções de comutação</span><span class="sxs-lookup"><span data-stu-id="3a5fa-108">Switch Options</span></span>

<span data-ttu-id="3a5fa-109">Essa opção não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="3a5fa-109">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="3a5fa-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="3a5fa-110">Remarks</span></span>

<span data-ttu-id="3a5fa-111">Modifica o comportamento da opção [**/sal**](-sal.md) para também fornecer anotações sobre os parâmetros dos métodos de interface marcados com o atributo [**\[ local \]**](local.md) .</span><span class="sxs-lookup"><span data-stu-id="3a5fa-111">Modifies the behavior of the [**/sal**](-sal.md) switch to also provide annotations on the parameters of interface methods marked with the [**\[local\]**](local.md) attribute.</span></span> <span data-ttu-id="3a5fa-112">Use o atributo [**\[ anotar \]**](annotate.md)para substituir a anotação gerada por MIDL por uma cadeia de caracteres de anotação diferente.</span><span class="sxs-lookup"><span data-stu-id="3a5fa-112">Use the [**\[annotate\]**](annotate.md)attribute to override the MIDL-generated annotation with a different annotation string.</span></span>

## <a name="see-also"></a><span data-ttu-id="3a5fa-113">Confira também</span><span class="sxs-lookup"><span data-stu-id="3a5fa-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a5fa-114">Sintaxe de linha de comando MIDL geral</span><span class="sxs-lookup"><span data-stu-id="3a5fa-114">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="3a5fa-115">**/sal**</span><span class="sxs-lookup"><span data-stu-id="3a5fa-115">**/sal**</span></span>](-sal.md)
</dt> <dt>

<span data-ttu-id="3a5fa-116">[**\[anotar\]**](annotate.md)</span><span class="sxs-lookup"><span data-stu-id="3a5fa-116">[**\[annotate\]**](annotate.md)</span></span>
</dt> </dl>

 

 




