---
title: ControlTypeNoExpectedPatternsSupported
description: ControlTypeNoExpectedPatternsSupported
ms.assetid: 2C9CEFEA-8207-47A7-B100-A56CFBFB792D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78c40f9f094589b312a033d6bdadf3fbf3b5020b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292249"
---
# <a name="controltypenoexpectedpatternssupported"></a><span data-ttu-id="89226-103">ControlTypeNoExpectedPatternsSupported</span><span class="sxs-lookup"><span data-stu-id="89226-103">ControlTypeNoExpectedPatternsSupported</span></span>

## <a name="text"></a><span data-ttu-id="89226-104">Texto</span><span class="sxs-lookup"><span data-stu-id="89226-104">Text</span></span>

<span data-ttu-id="89226-105">O elemento com um ControlType de {0} deve dar suporte a pelo menos um destes padrões: {1} mas esse elemento não</span><span class="sxs-lookup"><span data-stu-id="89226-105">Element with a ControlType of {0} should support at least one of these patterns:{1} but this element does not</span></span>

## <a name="type"></a><span data-ttu-id="89226-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="89226-106">Type</span></span>

<span data-ttu-id="89226-107">Erro</span><span class="sxs-lookup"><span data-stu-id="89226-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="89226-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="89226-108">Description</span></span>

<span data-ttu-id="89226-109">O suporte à automação da interface do usuário do elemento não está em conformidade com a especificação de automação da interface do usuário porque o elemento deve dar suporte a pelo menos uma das listas de padrões de controle fornecidas, mas não.</span><span class="sxs-lookup"><span data-stu-id="89226-109">The element's UI Automation support does not comply with the UI Automation specification because the element should support at least one of the provided list of control patterns, but does not.</span></span> <span data-ttu-id="89226-110">Como resultado, esse elemento pode não ser exposto corretamente a tecnologias assistenciais, o que pode ter um impacto sério na experiência do usuário.</span><span class="sxs-lookup"><span data-stu-id="89226-110">As a result, this element might not be properly exposed to assistive technologies, which could have a serious impact on user experience.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="89226-111">Possíveis causas</span><span class="sxs-lookup"><span data-stu-id="89226-111">Possible causes</span></span>

-   <span data-ttu-id="89226-112">Implementação de automação de interface do usuário incompleta.</span><span class="sxs-lookup"><span data-stu-id="89226-112">Incomplete UI Automation implementation.</span></span>
-   <span data-ttu-id="89226-113">A propriedade ControlType não está definida corretamente.</span><span class="sxs-lookup"><span data-stu-id="89226-113">The ControlType property is not set correctly.</span></span>

## <a name="remarks"></a><span data-ttu-id="89226-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="89226-114">Remarks</span></span>

<span data-ttu-id="89226-115">AccChecker registra essa mensagem de erro para uma barra de progresso indeterminada.</span><span class="sxs-lookup"><span data-stu-id="89226-115">AccChecker logs this error message for an indeterminate progress bar.</span></span> <span data-ttu-id="89226-116">Você pode ignorar essa mensagem e/ou adicioná-la à lista de supressões.</span><span class="sxs-lookup"><span data-stu-id="89226-116">You can ignore this message and/or add it to the suppressions list.</span></span>

## <a name="related-topics"></a><span data-ttu-id="89226-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="89226-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="89226-118">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="89226-118">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)
</dt> <dt>

[<span data-ttu-id="89226-119">Visão Geral dos Tipos de Controle de Automação de Interface do Usuário</span><span class="sxs-lookup"><span data-stu-id="89226-119">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="89226-120">Visão Geral de Padrões de Controle de Automação de Interface de Usuário</span><span class="sxs-lookup"><span data-stu-id="89226-120">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> </dl>

 

 




