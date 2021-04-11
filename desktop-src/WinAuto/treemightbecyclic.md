---
title: TreeMightBeCyclic
description: TreeMightBeCyclic
ms.assetid: 9A997949-A1A2-448C-9739-BE176621F1B4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9647f4429ba17226f342a8dceb3c51b033d08b4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294108"
---
# <a name="treemightbecyclic"></a><span data-ttu-id="e1661-103">TreeMightBeCyclic</span><span class="sxs-lookup"><span data-stu-id="e1661-103">TreeMightBeCyclic</span></span>

## <a name="text"></a><span data-ttu-id="e1661-104">Texto</span><span class="sxs-lookup"><span data-stu-id="e1661-104">Text</span></span>

<span data-ttu-id="e1661-105">A árvore tem {0} níveis de profundidade.</span><span class="sxs-lookup"><span data-stu-id="e1661-105">Tree is {0} levels deep.</span></span> <span data-ttu-id="e1661-106">Isso pode indicar que a árvore de acessibilidade é cíclica e, portanto, pareceria infinita.</span><span class="sxs-lookup"><span data-stu-id="e1661-106">This might indicate that the accessibility tree is cyclic, and thus it would appear to be infinite.</span></span>

## <a name="type"></a><span data-ttu-id="e1661-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="e1661-107">Type</span></span>

<span data-ttu-id="e1661-108">Erro</span><span class="sxs-lookup"><span data-stu-id="e1661-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="e1661-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="e1661-109">Description</span></span>

<span data-ttu-id="e1661-110">A árvore de elementos é cíclica e a profundidade da árvore pode ser infinita.</span><span class="sxs-lookup"><span data-stu-id="e1661-110">The element tree is cyclic and the tree depth might be infinite.</span></span>

<span data-ttu-id="e1661-111">Esse problema causa problemas para as pessoas que contam com um leitor de tela e um teclado para navegação porque não haverá nenhum limite aparente para a passagem de elementos no aplicativo de destino.</span><span class="sxs-lookup"><span data-stu-id="e1661-111">This issue causes problems for people who rely on a screen-reader and keyboard for navigation because there will be no apparent limit to the traversal of elements in the target application.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="e1661-112">Possíveis causas</span><span class="sxs-lookup"><span data-stu-id="e1661-112">Possible causes</span></span>

<span data-ttu-id="e1661-113">Vários elementos, ou seus pais, são controles personalizados que não implementam a Tabulação corretamente.</span><span class="sxs-lookup"><span data-stu-id="e1661-113">Multiple elements, or their parents, are custom controls that do not implement tabbing correctly.</span></span> <span data-ttu-id="e1661-114">Por exemplo, a propriedade de [estado](state-property.md) MSAA não é atualizada corretamente.</span><span class="sxs-lookup"><span data-stu-id="e1661-114">For example, the MSAA [State](state-property.md) property is not updated correctly.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e1661-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e1661-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e1661-116">Diretrizes para design de interface de usuário de teclado</span><span class="sxs-lookup"><span data-stu-id="e1661-116">Guidelines for Keyboard User Interface Design</span></span>](/previous-versions/windows/desktop/dnacc/guidelines-for-keyboard-user-interface-design)
</dt> <dt>

[<span data-ttu-id="e1661-117">Diretrizes de interação da experiência do usuário do Windows – teclado</span><span class="sxs-lookup"><span data-stu-id="e1661-117">Windows User Experience Interaction Guidelines - Keyboard</span></span>](https://msdn.microsoft.com/library/bb545460.aspx#guidelines)
</dt> </dl>

 

 