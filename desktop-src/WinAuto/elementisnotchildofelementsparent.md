---
title: ElementIsNotChildOfElementsParent
description: ElementIsNotChildOfElementsParent
ms.assetid: DFD5CC2A-B5F4-49F2-B3EF-2CD447A575E2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c5a3d62a6ae656bffffca442ed3cbb9b85be8dc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364486"
---
# <a name="elementisnotchildofelementsparent"></a><span data-ttu-id="161a8-103">ElementIsNotChildOfElementsParent</span><span class="sxs-lookup"><span data-stu-id="161a8-103">ElementIsNotChildOfElementsParent</span></span>

## <a name="text"></a><span data-ttu-id="161a8-104">Texto</span><span class="sxs-lookup"><span data-stu-id="161a8-104">Text</span></span>

<span data-ttu-id="161a8-105">O elemento não é um filho do seu pai</span><span class="sxs-lookup"><span data-stu-id="161a8-105">Element is not a child of it's parent</span></span>

## <a name="type"></a><span data-ttu-id="161a8-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="161a8-106">Type</span></span>

<span data-ttu-id="161a8-107">Erro</span><span class="sxs-lookup"><span data-stu-id="161a8-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="161a8-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="161a8-108">Description</span></span>

<span data-ttu-id="161a8-109">Quando [**Get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) é chamado no elemento filho retornado por [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) (usando as \_ constantes de navegação NAVDIR FIRSTCHILD ou NAVDIR \_ LASTCHILD), o elemento pai retornado não corresponde ao elemento pai especificado na chamada **accNavigate** .</span><span class="sxs-lookup"><span data-stu-id="161a8-109">When [**get\_accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) is called on the child element returned by [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) (using either the NAVDIR\_FIRSTCHILD or NAVDIR\_LASTCHILD navigation constants), the parent element returned does not match the parent element specified in the **accNavigate** call.</span></span>

<span data-ttu-id="161a8-110">Esse problema pode causar problemas de navegação para ferramentas automatizadas porque a passagem de elementos pode ser irregular e imprevisível.</span><span class="sxs-lookup"><span data-stu-id="161a8-110">This issue can cause navigation problems for automated tools because traversing elements might be erratic and unpredictable.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="161a8-111">Possíveis causas</span><span class="sxs-lookup"><span data-stu-id="161a8-111">Possible causes</span></span>

<span data-ttu-id="161a8-112">Uma implementação de MSAA incorreta ou inválida.</span><span class="sxs-lookup"><span data-stu-id="161a8-112">An incorrect or invalid MSAA implementation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="161a8-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="161a8-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="161a8-114">**IAccessible:: accNavigate**</span><span class="sxs-lookup"><span data-stu-id="161a8-114">**IAccessible::accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
</dt> <dt>

[<span data-ttu-id="161a8-115">**IAccessible:: obter \_ accParent**</span><span class="sxs-lookup"><span data-stu-id="161a8-115">**IAccessible::get\_accParent**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)
</dt> </dl>

 

 




