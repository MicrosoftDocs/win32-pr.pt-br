---
title: opção/no_format_opt
description: O \_ switch opt de formato de \_ alteração altera a maneira como o MIDL otimiza os descritores de tipo e de procedimento.
ms.assetid: 721ac828-7b47-4991-8bce-f9babf6c77a8
keywords:
- /no_format_opt MIDL do comutador
topic_type:
- apiref
api_name:
- /no_format_opt
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4d6e54b963c9637c4f5a583fc9d8f44a0f2880e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "105792502"
---
# <a name="no_format_opt-switch"></a><span data-ttu-id="fc125-104">opção de aceitação de \_ formato de/// \_</span><span class="sxs-lookup"><span data-stu-id="fc125-104">/no\_format\_opt switch</span></span>

<span data-ttu-id="fc125-105">O **switch \_ \_ opt de formato** de alteração altera a maneira como o MIDL otimiza os descritores de tipo e de procedimento.</span><span class="sxs-lookup"><span data-stu-id="fc125-105">The **/no\_format\_opt** switch changes the way MIDL optimizes type and procedure descriptors.</span></span>

``` syntax
midl /no_format_opt
```

## <a name="switch-options"></a><span data-ttu-id="fc125-106">Opções de comutação</span><span class="sxs-lookup"><span data-stu-id="fc125-106">Switch Options</span></span>

<span data-ttu-id="fc125-107">Essa opção não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="fc125-107">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="fc125-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="fc125-108">Remarks</span></span>

<span data-ttu-id="fc125-109">Por padrão, MIDL elimina o tipo duplicado e descritores de procedimento para reduzir o tamanho do código stub gerado.</span><span class="sxs-lookup"><span data-stu-id="fc125-109">By default, MIDL eliminates duplicate type and procedure descriptors in order to reduce the size of the generated stub code.</span></span> <span data-ttu-id="fc125-110">O uso da opção de escolha de **\_ formato \_** de alteração desativa esse comportamento de otimização.</span><span class="sxs-lookup"><span data-stu-id="fc125-110">Using the **/no\_format\_opt** switch turns off this optimizing behavior.</span></span>

## <a name="examples"></a><span data-ttu-id="fc125-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="fc125-111">Examples</span></span>

<span data-ttu-id="fc125-112">**a opção MIDL/ \_ Format \_ aceitar mylean. idl**</span><span class="sxs-lookup"><span data-stu-id="fc125-112">**midl /no\_format\_opt mylean.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="fc125-113">Confira também</span><span class="sxs-lookup"><span data-stu-id="fc125-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc125-114">Sintaxe de linha de comando MIDL geral</span><span class="sxs-lookup"><span data-stu-id="fc125-114">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="fc125-115">**/Oi**</span><span class="sxs-lookup"><span data-stu-id="fc125-115">**/Oi**</span></span>](-oi.md)
</dt> </dl>

 

 




