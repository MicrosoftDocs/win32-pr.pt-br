---
title: opção/no_robust
description: O comutador de// \_ avançado orienta o compilador MIDL a desabilitar explicitamente o recurso de linha de comando/robust. A opção de linha de comando/robust e seus recursos associados são a configuração de compilador padrão para MIDL versão 6.0.359 e posterior.
ms.assetid: 17ece05a-d39d-4465-8553-199a45c8c073
keywords:
- /no_robust MIDL do comutador
topic_type:
- apiref
api_name:
- /no_robust
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90691aede68f8e43ae95a4bd6c6f7fb4e2ecad29
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103638659"
---
# <a name="no_robust-switch"></a><span data-ttu-id="ed869-105">// \_ comutador robusto</span><span class="sxs-lookup"><span data-stu-id="ed869-105">/no\_robust switch</span></span>

<span data-ttu-id="ed869-106">O comutador de **// \_ avançado** orienta o compilador MIDL a desabilitar explicitamente o recurso de linha de comando [**/robust**](-robust.md) .</span><span class="sxs-lookup"><span data-stu-id="ed869-106">The **/no\_robust** switch directs the MIDL compiler to explicitly disable the [**/robust**](-robust.md) command line feature.</span></span> <span data-ttu-id="ed869-107">A opção de linha de comando **/robust** e seus recursos associados são a configuração de compilador padrão para MIDL versão 6.0.359 e posterior.</span><span class="sxs-lookup"><span data-stu-id="ed869-107">The **/robust** command line switch and its associated features is the default compiler setting for MIDL version 6.0.359 and later.</span></span>

``` syntax
midl /no_robust
```

## <a name="switch-options"></a><span data-ttu-id="ed869-108">Opções de comutação</span><span class="sxs-lookup"><span data-stu-id="ed869-108">Switch Options</span></span>

<span data-ttu-id="ed869-109">Essa opção não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="ed869-109">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="ed869-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="ed869-110">Remarks</span></span>

<span data-ttu-id="ed869-111">Com o MIDL versão 6.0.359 e posterior, o compilador MIDL define [**/robust**](-robust.md) por padrão.</span><span class="sxs-lookup"><span data-stu-id="ed869-111">With MIDL version 6.0.359 and later, the MIDL compiler sets [**/robust**](-robust.md) by default.</span></span> <span data-ttu-id="ed869-112">A opção de linha de comando de **// \_ eficiência avançada** deve ser usada para desabilitar o recurso **/robust** se os stubs gerados precisarem ser executados no Microsoft WindowsÂ NT, no WindowsÂ 95/98 ou no WindowsÂ me.</span><span class="sxs-lookup"><span data-stu-id="ed869-112">The **/no\_robust** command line switch must be used to disable the **/robust** feature if generated stubs need to run on Microsoft WindowsÂ NT, WindowsÂ 95/98, or WindowsÂ Me.</span></span>

## <a name="examples"></a><span data-ttu-id="ed869-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ed869-113">Examples</span></span>

<span data-ttu-id="ed869-114">**MIDL/ \_ robusto filename. idl**</span><span class="sxs-lookup"><span data-stu-id="ed869-114">**midl /no\_robust filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="ed869-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="ed869-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed869-116">Sintaxe de linha de comando MIDL geral</span><span class="sxs-lookup"><span data-stu-id="ed869-116">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="ed869-117">**/robust**</span><span class="sxs-lookup"><span data-stu-id="ed869-117">**/robust**</span></span>](-robust.md)
</dt> </dl>

 

 




