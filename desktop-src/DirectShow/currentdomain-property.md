---
description: A propriedade CurrentDomain recupera o domínio de DVD no qual o objeto MSWebDVD está.
ms.assetid: 9d545438-9a3d-4c57-a3df-5e75af2e4d1b
title: Propriedade CurrentDomain
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ead6d61cd622fceac2a4d133a0297892992e763a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104456660"
---
# <a name="currentdomain-property"></a><span data-ttu-id="f60bf-103">Propriedade CurrentDomain</span><span class="sxs-lookup"><span data-stu-id="f60bf-103">CurrentDomain Property</span></span>

> [!Note]  
> <span data-ttu-id="f60bf-104">Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="f60bf-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="f60bf-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="f60bf-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="f60bf-106">A `CurrentDomain` propriedade recupera o domínio de DVD no qual o objeto MSWebDVD está.</span><span class="sxs-lookup"><span data-stu-id="f60bf-106">The `CurrentDomain` property retrieves the DVD domain that the MSWebDVD object is in.</span></span>

``` syntax
[ iDomain = ] MSWebDVD.CurrentDomain
```

## <a name="return-value"></a><span data-ttu-id="f60bf-107">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="f60bf-107">Return Value</span></span>

<span data-ttu-id="f60bf-108">Retorna um valor inteiro que representa o domínio atual.</span><span class="sxs-lookup"><span data-stu-id="f60bf-108">Returns an integer value representing the current domain.</span></span>

## <a name="remarks"></a><span data-ttu-id="f60bf-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="f60bf-109">Remarks</span></span>

<span data-ttu-id="f60bf-110">Os valores possíveis da propriedade são:</span><span class="sxs-lookup"><span data-stu-id="f60bf-110">The possible values of the property are:</span></span>



| <span data-ttu-id="f60bf-111">Valor</span><span class="sxs-lookup"><span data-stu-id="f60bf-111">Value</span></span> | <span data-ttu-id="f60bf-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="f60bf-112">Description</span></span>          |
|-------|----------------------|
| <span data-ttu-id="f60bf-113">1</span><span class="sxs-lookup"><span data-stu-id="f60bf-113">1</span></span>     | <span data-ttu-id="f60bf-114">Primeira reprodução</span><span class="sxs-lookup"><span data-stu-id="f60bf-114">First play</span></span>           |
| <span data-ttu-id="f60bf-115">2</span><span class="sxs-lookup"><span data-stu-id="f60bf-115">2</span></span>     | <span data-ttu-id="f60bf-116">Menu Gerenciador de vídeo</span><span class="sxs-lookup"><span data-stu-id="f60bf-116">Video Manager Menu</span></span>   |
| <span data-ttu-id="f60bf-117">3</span><span class="sxs-lookup"><span data-stu-id="f60bf-117">3</span></span>     | <span data-ttu-id="f60bf-118">Menu de conjunto de título de vídeo</span><span class="sxs-lookup"><span data-stu-id="f60bf-118">Video Title Set Menu</span></span> |
| <span data-ttu-id="f60bf-119">4</span><span class="sxs-lookup"><span data-stu-id="f60bf-119">4</span></span>     | <span data-ttu-id="f60bf-120">Título</span><span class="sxs-lookup"><span data-stu-id="f60bf-120">Title</span></span>                |
| <span data-ttu-id="f60bf-121">5</span><span class="sxs-lookup"><span data-stu-id="f60bf-121">5</span></span>     | <span data-ttu-id="f60bf-122">Stop</span><span class="sxs-lookup"><span data-stu-id="f60bf-122">Stop</span></span>                 |



 

<span data-ttu-id="f60bf-123">Chame esse método para garantir que o navegador de DVD esteja em um domínio válido para o método que você está prestes a chamar.</span><span class="sxs-lookup"><span data-stu-id="f60bf-123">Call this method to ensure that the DVD Navigator is in a valid domain for the method you are about to call.</span></span> <span data-ttu-id="f60bf-124">Por exemplo, antes de chamar [**PlayTitle**](playtitle-method.md), verifique a propriedade para certificar-se `CurrentDomain` de que o navegador de DVD não está no domínio de parada ou da primeira reprodução.</span><span class="sxs-lookup"><span data-stu-id="f60bf-124">For example, before calling [**PlayTitle**](playtitle-method.md), check the `CurrentDomain` property to make sure that the DVD Navigator is not in the Stop or First Play domain.</span></span>

 

 



