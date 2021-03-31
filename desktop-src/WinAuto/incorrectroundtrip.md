---
title: IncorrectRoundTrip
description: IncorrectRoundTrip
ms.assetid: 244537EB-E7DC-49E4-BEAF-CFE3ED25E0B2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1f154c0ccc0fff9bb654b94ef9d0807aa459d4b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104160184"
---
# <a name="incorrectroundtrip"></a><span data-ttu-id="0d9ce-103">IncorrectRoundTrip</span><span class="sxs-lookup"><span data-stu-id="0d9ce-103">IncorrectRoundTrip</span></span>

## <a name="text"></a><span data-ttu-id="0d9ce-104">Texto</span><span class="sxs-lookup"><span data-stu-id="0d9ce-104">Text</span></span>

<span data-ttu-id="0d9ce-105">Chame para accNavigate (clique em adiar para ser lembrado novamente em:), 1, NAVDIR \_ Next), em seguida, accNavigate ((Open), 2, NAVDIR \_ Previous), deve ter retornado clique em adiar para ser lembrado novamente em: (childID = 1), mas retornado clique em adiar para ser lembrado novamente em:</span><span class="sxs-lookup"><span data-stu-id="0d9ce-105">Call to accNavigate((Click Snooze to be reminded again in:), 1, NAVDIR\_NEXT), then accNavigate((Open), 2, NAVDIR\_PREVIOUS), should have returned Click Snooze to be reminded again in:(ChildId=1), but returned Click Snooze to be reminded again in:</span></span>

## <a name="type"></a><span data-ttu-id="0d9ce-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="0d9ce-106">Type</span></span>

<span data-ttu-id="0d9ce-107">Erro</span><span class="sxs-lookup"><span data-stu-id="0d9ce-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="0d9ce-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="0d9ce-108">Description</span></span>

<span data-ttu-id="0d9ce-109">usar [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) para atravessar a árvore de elementos do destino de verificação não retorna o mesmo elemento inicial quando a direção de passagem é invertida.</span><span class="sxs-lookup"><span data-stu-id="0d9ce-109">using [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) to traverse the element tree of the verification target does not return the same starting element when the direction of traversal is reversed.</span></span>

![exemplo de uma implementação de MSAA inválida que causou navegação de ida e volta incorreta](images/accchecker-invalid-round-trip.png)

<span data-ttu-id="0d9ce-111">Esse problema pode causar problemas de navegação para ferramentas automatizadas porque a passagem de elementos pode ser irregular e imprevisível.</span><span class="sxs-lookup"><span data-stu-id="0d9ce-111">This issue can cause navigation problems for automated tools because traversing elements might be erratic and unpredictable.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="0d9ce-112">Possíveis causas</span><span class="sxs-lookup"><span data-stu-id="0d9ce-112">Possible causes</span></span>

<span data-ttu-id="0d9ce-113">Uma implementação de MSAA incorreta ou inválida.</span><span class="sxs-lookup"><span data-stu-id="0d9ce-113">An incorrect or invalid MSAA implementation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0d9ce-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0d9ce-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0d9ce-115">**IAccessible:: accNavigate**</span><span class="sxs-lookup"><span data-stu-id="0d9ce-115">**IAccessible::accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
</dt> </dl>

 

 




