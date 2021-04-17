---
title: AccNavigate_ReturnedElementWithIncorrectParent
description: AccNavigate \_ ReturnedElementWithIncorrectParent
ms.assetid: 44447E47-04D5-4784-B5E9-E8C62A9834CE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a3bdff54c9c594cde4e6e57fe1886a900c913eb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104559452"
---
# <a name="accnavigate_returnedelementwithincorrectparent"></a><span data-ttu-id="82722-103">AccNavigate \_ ReturnedElementWithIncorrectParent</span><span class="sxs-lookup"><span data-stu-id="82722-103">AccNavigate\_ReturnedElementWithIncorrectParent</span></span>

## <a name="text"></a><span data-ttu-id="82722-104">Texto</span><span class="sxs-lookup"><span data-stu-id="82722-104">Text</span></span>

<span data-ttu-id="82722-105">Chamar accNavigate ((Live Search), 0, NAVDIR \_ FIRSTCHILD) que retornou (x-gadget:///gadget.html) retornou o pai incorreto ( \[ NULL \] ) e não (Live Search)</span><span class="sxs-lookup"><span data-stu-id="82722-105">Calling accNavigate((Live Search), 0, NAVDIR\_FIRSTCHILD) which returned (x-gadget:///gadget.html) returned the incorrect parent(\[NULL\]) and not (Live Search)</span></span>

## <a name="type"></a><span data-ttu-id="82722-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="82722-106">Type</span></span>

<span data-ttu-id="82722-107">Erro</span><span class="sxs-lookup"><span data-stu-id="82722-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="82722-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="82722-108">Description</span></span>

<span data-ttu-id="82722-109">Quando [**Get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) é chamado no elemento filho retornado por [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) (usando as \_ constantes de navegação NAVDIR FIRSTCHILD ou NAVDIR \_ LASTCHILD), o elemento pai retornado não corresponde ao elemento pai especificado na chamada **accNavigate** .</span><span class="sxs-lookup"><span data-stu-id="82722-109">When [**get\_accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) is called on the child element returned by [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) (using either the NAVDIR\_FIRSTCHILD or NAVDIR\_LASTCHILD navigation constants), the parent element returned does not match the parent element specified in the **accNavigate** call.</span></span>

![exemplo de uma implementação de MSAA inválida que retorna um elemento pai incorreto.](images/accchecker-invalid-msaa-parent.png)

<span data-ttu-id="82722-111">Esse problema pode causar problemas de navegação para ferramentas automatizadas porque a passagem de elementos pode ser irregular e imprevisível.</span><span class="sxs-lookup"><span data-stu-id="82722-111">This issue can cause navigation problems for automated tools because traversing elements might be erratic and unpredictable.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="82722-112">Possíveis causas</span><span class="sxs-lookup"><span data-stu-id="82722-112">Possible causes</span></span>

<span data-ttu-id="82722-113">Uma implementação de MSAA incorreta ou inválida.</span><span class="sxs-lookup"><span data-stu-id="82722-113">An incorrect or invalid MSAA implementation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="82722-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="82722-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="82722-115">**IAccessible:: accNavigate**</span><span class="sxs-lookup"><span data-stu-id="82722-115">**IAccessible::accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
</dt> <dt>

[<span data-ttu-id="82722-116">**IAccessible:: obter \_ accParent**</span><span class="sxs-lookup"><span data-stu-id="82722-116">**IAccessible::get\_accParent**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)
</dt> </dl>

 

 




