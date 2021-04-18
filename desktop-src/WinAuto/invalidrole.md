---
title: InvalidRole
description: InvalidRole
ms.assetid: B0707B90-59D6-4F86-8CBB-1DF57FDBEE31
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 531aa9917bd68b615c2cd2457d7a24bfc4af336c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105793936"
---
# <a name="invalidrole"></a><span data-ttu-id="c67a4-103">InvalidRole</span><span class="sxs-lookup"><span data-stu-id="c67a4-103">InvalidRole</span></span>

## <a name="text"></a><span data-ttu-id="c67a4-104">Texto</span><span class="sxs-lookup"><span data-stu-id="c67a4-104">Text</span></span>

<span data-ttu-id="c67a4-105">O int retornado de get \_ accRole não é uma constante de função válida, sistema de função do IE \_\_\*</span><span class="sxs-lookup"><span data-stu-id="c67a4-105">The int returned from get\_accRole is not a valid role constant, ie ROLE\_SYSTEM\_\*</span></span>

## <a name="type"></a><span data-ttu-id="c67a4-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="c67a4-106">Type</span></span>

<span data-ttu-id="c67a4-107">Erro</span><span class="sxs-lookup"><span data-stu-id="c67a4-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="c67a4-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="c67a4-108">Description</span></span>

<span data-ttu-id="c67a4-109">Um elemento está relatando uma função de MSAA inválida.</span><span class="sxs-lookup"><span data-stu-id="c67a4-109">An element is reporting an invalid MSAA role.</span></span> <span data-ttu-id="c67a4-110">Por exemplo, o método [**Get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole) retorna um valor inteiro que não é mapeado para uma constante de função de objeto válida (como \_ ListItem de sistema de função \_ ).</span><span class="sxs-lookup"><span data-stu-id="c67a4-110">For example, the [**get\_accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole) method returns an integer value that does not map to a valid object role constant (such as ROLE\_SYSTEM\_LISTITEM).</span></span>

<span data-ttu-id="c67a4-111">Esse problema causa problemas para as pessoas que dependem de um leitor de tela e teclado para navegação porque os elementos podem ser identificados incorretamente para o usuário.</span><span class="sxs-lookup"><span data-stu-id="c67a4-111">This issue causes problems for people who rely on a screen-reader and keyboard for navigation because elements may be incorrectly identified to the user.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="c67a4-112">Possíveis causas</span><span class="sxs-lookup"><span data-stu-id="c67a4-112">Possible causes</span></span>

<span data-ttu-id="c67a4-113">O elemento ou seu pai tem uma função de MSAA definida incorretamente.</span><span class="sxs-lookup"><span data-stu-id="c67a4-113">The element or its parent has an MSAA role set inappropriately.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c67a4-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c67a4-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c67a4-115">**IAccessible:: obter \_ accRole**</span><span class="sxs-lookup"><span data-stu-id="c67a4-115">**IAccessible::get\_accRole**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)
</dt> <dt>

[<span data-ttu-id="c67a4-116">**Funções de objeto**</span><span class="sxs-lookup"><span data-stu-id="c67a4-116">**Object Roles**</span></span>](object-roles.md)
</dt> </dl>

 

 




