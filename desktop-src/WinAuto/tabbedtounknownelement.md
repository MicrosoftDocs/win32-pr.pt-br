---
title: TabbedToUnknownElement
description: TabbedToUnknownElement
ms.assetid: B0447B19-E281-4D30-8ED8-FC0EE13571C8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 612476d81779c882eeca807a9c3b82c41594f218
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363847"
---
# <a name="tabbedtounknownelement"></a><span data-ttu-id="ac3ca-103">TabbedToUnknownElement</span><span class="sxs-lookup"><span data-stu-id="ac3ca-103">TabbedToUnknownElement</span></span>

## <a name="text"></a><span data-ttu-id="ac3ca-104">Texto</span><span class="sxs-lookup"><span data-stu-id="ac3ca-104">Text</span></span>

<span data-ttu-id="ac3ca-105">A Tabulação foi movida para um elemento fora do HWND de destino.</span><span class="sxs-lookup"><span data-stu-id="ac3ca-105">Tabbing has gone to an element outside the target hwnd.</span></span>

## <a name="type"></a><span data-ttu-id="ac3ca-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="ac3ca-106">Type</span></span>

<span data-ttu-id="ac3ca-107">Erro</span><span class="sxs-lookup"><span data-stu-id="ac3ca-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="ac3ca-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="ac3ca-108">Description</span></span>

<span data-ttu-id="ac3ca-109">Usar a navegação de teclado padrão (TAB ou Shift + Tab) faz com que o foco seja deslocado para fora do HWND do destino de verificação.</span><span class="sxs-lookup"><span data-stu-id="ac3ca-109">Using standard keyboard navigation (Tab or Shift+Tab) causes focus to shift outside the HWND of the verification target.</span></span>

<span data-ttu-id="ac3ca-110">AccChecker move a árvore de elementos para o HWND de nível superior para o destino de verificação escolhido antes de executar qualquer tarefa de verificação.</span><span class="sxs-lookup"><span data-stu-id="ac3ca-110">AccChecker moves up the element tree to the top-level HWND for the chosen verification target before running any verification tasks.</span></span> <span data-ttu-id="ac3ca-111">Isso reduz o número de erros falsos gerados se um HWND escolhido para verificação fizer parte de uma área de cliente mais complexa.</span><span class="sxs-lookup"><span data-stu-id="ac3ca-111">This reduces the number of spurious errors generated if an HWND chosen for verification is part of a more complex client area.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="ac3ca-112">Possíveis causas</span><span class="sxs-lookup"><span data-stu-id="ac3ca-112">Possible causes</span></span>

-   <span data-ttu-id="ac3ca-113">O destino de verificação não requer uma implementação de tabulação para fornecer funcionalidade completa.</span><span class="sxs-lookup"><span data-stu-id="ac3ca-113">The verification target doesn't require a tabbing implementation to provide full functionality.</span></span>
-   <span data-ttu-id="ac3ca-114">A interação do usuário durante a verificação, como a movimentação do foco para um HWND não-alvo, interfere no processo de verificação.</span><span class="sxs-lookup"><span data-stu-id="ac3ca-114">User interaction during verification, such as moving focus to a non-target HWND, interfered with the verification process.</span></span>

 

 




