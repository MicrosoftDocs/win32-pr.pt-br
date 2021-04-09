---
title: TabbingNotSymmetric
description: TabbingNotSymmetric
ms.assetid: 1E14ED9F-27C1-4054-B0A6-702167222196
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc19efbbbce0f299044726466dd8f87b133fc26d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084661"
---
# <a name="tabbingnotsymmetric"></a><span data-ttu-id="05bcf-103">TabbingNotSymmetric</span><span class="sxs-lookup"><span data-stu-id="05bcf-103">TabbingNotSymmetric</span></span>

## <a name="text"></a><span data-ttu-id="05bcf-104">Texto</span><span class="sxs-lookup"><span data-stu-id="05bcf-104">Text</span></span>

<span data-ttu-id="05bcf-105">A tabulação para trás e para frente não produz o mesmo elemento.</span><span class="sxs-lookup"><span data-stu-id="05bcf-105">Tabbing backwards and forwards does not yield the same element.</span></span> <span data-ttu-id="05bcf-106">Esperado {0} , mas recebido {1}</span><span class="sxs-lookup"><span data-stu-id="05bcf-106">Expected {0} but received {1}</span></span>

## <a name="type"></a><span data-ttu-id="05bcf-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="05bcf-107">Type</span></span>

<span data-ttu-id="05bcf-108">Erro</span><span class="sxs-lookup"><span data-stu-id="05bcf-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="05bcf-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="05bcf-109">Description</span></span>

<span data-ttu-id="05bcf-110">Ao usar a navegação de teclado padrão (TAB ou Shift + Tab), não é possível repetir o caminho de passagem por meio da árvore de elementos do destino de verificação se a direção de passagem for invertida.</span><span class="sxs-lookup"><span data-stu-id="05bcf-110">When using standard keyboard navigation (Tab or Shift+Tab), it isn't possible to repeat the path of traversal through the element tree of the verification target if the direction of traversal is reversed.</span></span> <span data-ttu-id="05bcf-111">Por exemplo, a tabulação (Tab) x vezes do elemento A (0) para o elemento A (x) e, em seguida, tabulação retroativa (Shift + Tab) x vezes resulta no elemento A (0) recuperando o foco por meio de um conjunto diferente de elementos intermediários.</span><span class="sxs-lookup"><span data-stu-id="05bcf-111">For example, tabbing forward (Tab) x times from element A(0) to element A(x) and then tabbing backward (Shift+Tab) x times results in element A(0) regaining focus through a different set of intermediate elements.</span></span>

<span data-ttu-id="05bcf-112">Esse problema causa problemas para as pessoas que contam com um leitor de tela e um teclado para navegação porque a passagem de elementos parece irregular e imprevisível.</span><span class="sxs-lookup"><span data-stu-id="05bcf-112">This issue causes problems for people who rely on a screen-reader and keyboard for navigation because traversing elements appears erratic and unpredictable.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="05bcf-113">Possíveis causas</span><span class="sxs-lookup"><span data-stu-id="05bcf-113">Possible causes</span></span>

-   <span data-ttu-id="05bcf-114">Vários elementos ou seus pais são controles personalizados que não implementam a Tabulação corretamente.</span><span class="sxs-lookup"><span data-stu-id="05bcf-114">Multiple elements or their parents are custom controls that don't implement tabbing correctly.</span></span> <span data-ttu-id="05bcf-115">Por exemplo, a propriedade de estado MSAA não está definida corretamente.</span><span class="sxs-lookup"><span data-stu-id="05bcf-115">For example, the MSAA State property is not set correctly.</span></span>

## <a name="related-topics"></a><span data-ttu-id="05bcf-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="05bcf-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="05bcf-117">Diretrizes para design de interface de usuário de teclado</span><span class="sxs-lookup"><span data-stu-id="05bcf-117">Guidelines for Keyboard User Interface Design</span></span>](/previous-versions/windows/desktop/dnacc/guidelines-for-keyboard-user-interface-design)
</dt> </dl>

 

 