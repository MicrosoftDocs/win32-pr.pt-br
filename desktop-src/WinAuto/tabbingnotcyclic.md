---
title: TabbingNotCyclic
description: TabbingNotCyclic
ms.assetid: F6BCC613-1EA1-438C-AC09-8A282870E021
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e08fd2e9f6613e07840f432b646c1bdc06a34b5f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007771"
---
# <a name="tabbingnotcyclic"></a><span data-ttu-id="d35a8-103">TabbingNotCyclic</span><span class="sxs-lookup"><span data-stu-id="d35a8-103">TabbingNotCyclic</span></span>

## <a name="text"></a><span data-ttu-id="d35a8-104">Texto</span><span class="sxs-lookup"><span data-stu-id="d35a8-104">Text</span></span>

<span data-ttu-id="d35a8-105">A Tabulação neste aplicativo não é cíclica.</span><span class="sxs-lookup"><span data-stu-id="d35a8-105">The tabbing in this application is not cyclic.</span></span> <span data-ttu-id="d35a8-106">A Tabulação ou os horários anteriores não retornam {0} ao mesmo controle.</span><span class="sxs-lookup"><span data-stu-id="d35a8-106">Tabbing forwards or backwards {0} times doesn't come back to the same control.</span></span>

## <a name="type"></a><span data-ttu-id="d35a8-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="d35a8-107">Type</span></span>

<span data-ttu-id="d35a8-108">Erro</span><span class="sxs-lookup"><span data-stu-id="d35a8-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="d35a8-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="d35a8-109">Description</span></span>

<span data-ttu-id="d35a8-110">Ao usar a navegação de teclado padrão (TAB ou Shift + Tab), não é possível atravessar a árvore de elementos do destino de verificação até que o elemento inicial se torne o elemento final (usando o mesmo número de pressionamentos de teclas), revertendo a direção da passagem.</span><span class="sxs-lookup"><span data-stu-id="d35a8-110">When using standard keyboard navigation (Tab or Shift+Tab), it isn't possible to traverse the element tree of the verification target until the starting element becomes the ending element (using the same number of keystrokes) by reversing the direction of traversal.</span></span> <span data-ttu-id="d35a8-111">Por exemplo, a tabulação (Tab) x vezes do elemento A (0) para o elemento A (x) e, em seguida, tabulação retroativa (Shift + Tab) x vezes não resulta no elemento A (0) ao obter o foco.</span><span class="sxs-lookup"><span data-stu-id="d35a8-111">For example, tabbing forward (Tab) x times from element A(0) to element A(x) and then tabbing backward (Shift+Tab) x times does not result in element A(0) regaining focus.</span></span>

<span data-ttu-id="d35a8-112">Esse problema causa problemas para as pessoas que contam com um leitor de tela e um teclado para navegação porque não há uma maneira previsível de retornar a um controle depois de ele ter sido visitado.</span><span class="sxs-lookup"><span data-stu-id="d35a8-112">This issue causes problems for people who rely on a screen-reader and keyboard for navigation because there is no predictable way to return to a control after it has been visited.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="d35a8-113">Possíveis causas</span><span class="sxs-lookup"><span data-stu-id="d35a8-113">Possible causes</span></span>

-   <span data-ttu-id="d35a8-114">O elemento ou seu pai é um controle personalizado que não implementa a Tabulação corretamente.</span><span class="sxs-lookup"><span data-stu-id="d35a8-114">The element or its parent is a custom control that doesn't implement tabbing correctly.</span></span> <span data-ttu-id="d35a8-115">Por exemplo, a propriedade de estado MSAA não está definida corretamente.</span><span class="sxs-lookup"><span data-stu-id="d35a8-115">For example, the MSAA State property isn't set correctly.</span></span>
-   <span data-ttu-id="d35a8-116">Alguns aplicativos, como o bloco de notas, exibem esse comportamento innatemente.</span><span class="sxs-lookup"><span data-stu-id="d35a8-116">Some applications, such as the Notepad, exhibit this behavior innately.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d35a8-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d35a8-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d35a8-118">Diretrizes para design de interface de usuário de teclado</span><span class="sxs-lookup"><span data-stu-id="d35a8-118">Guidelines for Keyboard User Interface Design</span></span>](/previous-versions/windows/desktop/dnacc/guidelines-for-keyboard-user-interface-design)
</dt> </dl>

 

 