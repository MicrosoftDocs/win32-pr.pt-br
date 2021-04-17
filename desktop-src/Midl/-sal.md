---
title: comutador/sal
description: A opção/sal direciona MIDL para gerar anotações SAL nos arquivos stub gerados.
ms.assetid: 452A19CA-6F72-416F-8059-77937412DA88
keywords:
- MIDL do comutador/sal
topic_type:
- apiref
api_name:
- /sal
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ef52eb510c71bfdb153b95a5d05e992359e39b6
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "105748788"
---
# <a name="sal-switch"></a><span data-ttu-id="52fda-104">comutador/sal</span><span class="sxs-lookup"><span data-stu-id="52fda-104">/sal switch</span></span>

<span data-ttu-id="52fda-105">A opção **/sal** direciona MIDL para gerar anotações sal nos arquivos stub gerados.</span><span class="sxs-lookup"><span data-stu-id="52fda-105">The **/sal** switch directs MIDL to generate SAL annotations in the generated stub files.</span></span>

``` syntax
midl /sal
```

## <a name="switch-options"></a><span data-ttu-id="52fda-106">Opções de comutação</span><span class="sxs-lookup"><span data-stu-id="52fda-106">Switch Options</span></span>

<span data-ttu-id="52fda-107">Essa opção não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="52fda-107">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="52fda-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="52fda-108">Remarks</span></span>

<span data-ttu-id="52fda-109">MIDL marcará os parâmetros de ponteiro e de matriz com anotações que refletem a descrição do parâmetro no arquivo IDL conforme imposto pelo RPC e pelo mecanismo de marshaling do NDR.</span><span class="sxs-lookup"><span data-stu-id="52fda-109">MIDL will mark pointer and array parameters with annotations that reflect the parameter description in the IDL file as enforced by RPC and the NDR marshaling engine.</span></span> <span data-ttu-id="52fda-110">MIDL não cria anotações para parâmetros em métodos de interface marcados com o atributo [**\[ local \]**](local.md), a menos que [**/sal \_ local**](-sal-local.md) também esteja presente na linha de comando.</span><span class="sxs-lookup"><span data-stu-id="52fda-110">MIDL does not create annotations for parameters in interface methods marked with the [**\[local\]**](local.md)attribute unless [**/sal\_local**](-sal-local.md) is also present on the command line.</span></span> <span data-ttu-id="52fda-111">Para substituir a anotação gerada por MIDL, use o atributo [**\[ anotar \]**](annotate.md) .</span><span class="sxs-lookup"><span data-stu-id="52fda-111">To override the MIDL-generated annotation, use the [**\[annotate\]**](annotate.md) attribute.</span></span>

<span data-ttu-id="52fda-112">As anotações geradas por MIDL são sempre prefixadas com \_ \_ RPC \_ e exigem o uso do cabeçalho **RPCs. h** para traduzir a anotação em anotações sal padrão.</span><span class="sxs-lookup"><span data-stu-id="52fda-112">MIDL-generated annotations are always prefixed with \_\_RPC\_, and require use of the **rpcsal.h** header to translate the annotation into standard SAL annotations.</span></span>

## <a name="see-also"></a><span data-ttu-id="52fda-113">Confira também</span><span class="sxs-lookup"><span data-stu-id="52fda-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52fda-114">Sintaxe de linha de comando MIDL geral</span><span class="sxs-lookup"><span data-stu-id="52fda-114">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="52fda-115">**/sal \_ local**</span><span class="sxs-lookup"><span data-stu-id="52fda-115">**/sal\_local**</span></span>](-sal-local.md)
</dt> <dt>

<span data-ttu-id="52fda-116">[**\[anotar\]**](annotate.md)</span><span class="sxs-lookup"><span data-stu-id="52fda-116">[**\[annotate\]**](annotate.md)</span></span>
</dt> </dl>

 

 




