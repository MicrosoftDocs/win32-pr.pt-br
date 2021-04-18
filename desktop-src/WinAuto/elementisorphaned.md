---
title: ElementIsOrphaned
description: ElementIsOrphaned
ms.assetid: EB603052-2B0F-418C-947E-827453440F46
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1878556af6f1954224bc9b5eadfd4d77e6e3419
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105789326"
---
# <a name="elementisorphaned"></a><span data-ttu-id="04eef-103">ElementIsOrphaned</span><span class="sxs-lookup"><span data-stu-id="04eef-103">ElementIsOrphaned</span></span>

## <a name="text"></a><span data-ttu-id="04eef-104">Texto</span><span class="sxs-lookup"><span data-stu-id="04eef-104">Text</span></span>

<span data-ttu-id="04eef-105">O elemento é um IAccessible órfão na árvore</span><span class="sxs-lookup"><span data-stu-id="04eef-105">Element is an orphaned IAccessible in the tree</span></span>

## <a name="type"></a><span data-ttu-id="04eef-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="04eef-106">Type</span></span>

<span data-ttu-id="04eef-107">Erro</span><span class="sxs-lookup"><span data-stu-id="04eef-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="04eef-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="04eef-108">Description</span></span>

<span data-ttu-id="04eef-109">O endereço da interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) do objeto obtido para as coordenadas fornecidas é uma referência a um elemento órfão na árvore de elementos.</span><span class="sxs-lookup"><span data-stu-id="04eef-109">The address of the object's [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface obtained for the given coordinates is a reference to an orphaned element in the element tree.</span></span>

<span data-ttu-id="04eef-110">Esse problema é um problema para as pessoas que contam com um leitor de tela e um teclado para navegação porque os elementos serão tratados como invisíveis e não serão anunciados para o usuário.</span><span class="sxs-lookup"><span data-stu-id="04eef-110">This issue is a problem for people who rely on a screen-reader and keyboard for navigation because elements will be treated as invisible and will not be announced to the user.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="04eef-111">Possíveis causas</span><span class="sxs-lookup"><span data-stu-id="04eef-111">Possible causes</span></span>

-   <span data-ttu-id="04eef-112">A interação do usuário durante a verificação, como a movimentação do foco para um HWND não-alvo, interfere no processo de verificação.</span><span class="sxs-lookup"><span data-stu-id="04eef-112">User interaction during verification, such as moving focus to a non-target HWND, interfered with the verification process.</span></span>
-   <span data-ttu-id="04eef-113">Uma implementação de MSAA incorreta ou inválida.</span><span class="sxs-lookup"><span data-stu-id="04eef-113">An incorrect or invalid MSAA implementation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="04eef-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="04eef-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="04eef-115">Navegação por meio de teste de clique e local da tela</span><span class="sxs-lookup"><span data-stu-id="04eef-115">Navigation Through Hit Testing and Screen Location</span></span>](navigation-through-hit-testing-and-screen-location.md)
</dt> <dt>

[<span data-ttu-id="04eef-116">**AccessibleObjectFromPoint**</span><span class="sxs-lookup"><span data-stu-id="04eef-116">**AccessibleObjectFromPoint**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)
</dt> </dl>

 

 




