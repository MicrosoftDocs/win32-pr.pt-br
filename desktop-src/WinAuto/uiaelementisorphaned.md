---
title: UiaElementIsOrphaned
description: UiaElementIsOrphaned
ms.assetid: F85F08E7-5A9C-4F08-B680-8B251D51168A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0ec0861a586fd5275a674d9ef8ba6a0e72364b2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105788732"
---
# <a name="uiaelementisorphaned"></a><span data-ttu-id="584be-103">UiaElementIsOrphaned</span><span class="sxs-lookup"><span data-stu-id="584be-103">UiaElementIsOrphaned</span></span>

## <a name="text"></a><span data-ttu-id="584be-104">Texto</span><span class="sxs-lookup"><span data-stu-id="584be-104">Text</span></span>

<span data-ttu-id="584be-105">O elemento é um AutomationElement órfão na árvore</span><span class="sxs-lookup"><span data-stu-id="584be-105">Element is an orphaned AutomationElement in the tree</span></span>

## <a name="type"></a><span data-ttu-id="584be-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="584be-106">Type</span></span>

<span data-ttu-id="584be-107">Erro</span><span class="sxs-lookup"><span data-stu-id="584be-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="584be-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="584be-108">Description</span></span>

<span data-ttu-id="584be-109">O endereço da interface [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) do objeto obtido para as coordenadas fornecidas é uma referência a um elemento órfão na árvore de elementos.</span><span class="sxs-lookup"><span data-stu-id="584be-109">The address of the object's [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) interface obtained for the given coordinates is a reference to an orphaned element in the element tree.</span></span>

<span data-ttu-id="584be-110">Esse problema é um problema para as pessoas que contam com um leitor de tela e um teclado para navegação porque os elementos serão tratados como invisíveis e não serão anunciados para o usuário.</span><span class="sxs-lookup"><span data-stu-id="584be-110">This issue is a problem for people who rely on a screen-reader and keyboard for navigation because elements will be treated as invisible and will not be announced to the user.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="584be-111">Possíveis causas</span><span class="sxs-lookup"><span data-stu-id="584be-111">Possible causes</span></span>

-   <span data-ttu-id="584be-112">A interação do usuário durante a verificação, como a movimentação do foco para um HWND não-alvo, interfere no processo de verificação.</span><span class="sxs-lookup"><span data-stu-id="584be-112">User interaction during verification, such as moving focus to a non-target HWND, interfered with the verification process.</span></span>
-   <span data-ttu-id="584be-113">Uma implementação de automação de interface do usuário incorreta ou inválida.</span><span class="sxs-lookup"><span data-stu-id="584be-113">An incorrect or invalid UI Automation implementation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="584be-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="584be-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="584be-115">**IUIAutomationElement.ElementFromPoint**</span><span class="sxs-lookup"><span data-stu-id="584be-115">**IUIAutomationElement.ElementFromPoint**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompoint)
</dt> </dl>

 

 




