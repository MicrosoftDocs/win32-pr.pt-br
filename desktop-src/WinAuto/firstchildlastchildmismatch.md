---
title: FirstChildLastChildMismatch
description: FirstChildLastChildMismatch
ms.assetid: 98726C1A-DC43-4FC7-8ECA-628F63D0AFE3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37fedb7e23ce2ac2a7f9c51c9db9e06e59ead515
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364185"
---
# <a name="firstchildlastchildmismatch"></a><span data-ttu-id="bfe39-103">FirstChildLastChildMismatch</span><span class="sxs-lookup"><span data-stu-id="bfe39-103">FirstChildLastChildMismatch</span></span>

## <a name="text"></a><span data-ttu-id="bfe39-104">Texto</span><span class="sxs-lookup"><span data-stu-id="bfe39-104">Text</span></span>

<span data-ttu-id="bfe39-105">Ao navegar chamando {0} a partir do nó testado e, em seguida, chamando repetidamente {1} , terminamos no seguinte filho: {2} .</span><span class="sxs-lookup"><span data-stu-id="bfe39-105">When navigating by calling {0} from the tested node, and then repeatedly calling {1}, we finished at the following child: {2}.</span></span> <span data-ttu-id="bfe39-106">Isso não correspondeu ao resultado da chamada {3} no nó testado, que gerou: {4} .</span><span class="sxs-lookup"><span data-stu-id="bfe39-106">This did not match the result of calling {3} on the tested node, which yielded: {4}.</span></span> <span data-ttu-id="bfe39-107">Em vez disso, o filho deve relatar como seu pai o nó de teste.</span><span class="sxs-lookup"><span data-stu-id="bfe39-107">Instead, the child should report as its parent the testing node.</span></span>

## <a name="type"></a><span data-ttu-id="bfe39-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="bfe39-108">Type</span></span>

<span data-ttu-id="bfe39-109">Erro</span><span class="sxs-lookup"><span data-stu-id="bfe39-109">Error</span></span>

## <a name="description"></a><span data-ttu-id="bfe39-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="bfe39-110">Description</span></span>

<span data-ttu-id="bfe39-111">Há um problema ao navegar entre os filhos do elemento.</span><span class="sxs-lookup"><span data-stu-id="bfe39-111">There is a problem when navigating between element’s children.</span></span> <span data-ttu-id="bfe39-112">1.</span><span class="sxs-lookup"><span data-stu-id="bfe39-112">1.</span></span> <span data-ttu-id="bfe39-113">Uma implementação de automação de interface do usuário incorreta ou inválida.</span><span class="sxs-lookup"><span data-stu-id="bfe39-113">An incorrect or invalid UI Automation implementation.</span></span>

<span data-ttu-id="bfe39-114">Esse problema pode causar problemas de navegação para ferramentas automatizadas porque a passagem de elementos pode ser irregular e imprevisível.</span><span class="sxs-lookup"><span data-stu-id="bfe39-114">This issue can cause navigation problems for automated tools because traversing elements might be erratic and unpredictable.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="bfe39-115">Possíveis causas</span><span class="sxs-lookup"><span data-stu-id="bfe39-115">Possible causes</span></span>

<span data-ttu-id="bfe39-116">Uma implementação de automação de interface do usuário incorreta ou inválida.</span><span class="sxs-lookup"><span data-stu-id="bfe39-116">An incorrect or invalid UI Automation implementation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bfe39-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bfe39-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bfe39-118">**IUIAutomationElement::GetCachedParent**</span><span class="sxs-lookup"><span data-stu-id="bfe39-118">**IUIAutomationElement::GetCachedParent**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedparent)
</dt> <dt>

[<span data-ttu-id="bfe39-119">**IUIAutomationTreeWalker**</span><span class="sxs-lookup"><span data-stu-id="bfe39-119">**IUIAutomationTreeWalker**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker)
</dt> </dl>

 

 




