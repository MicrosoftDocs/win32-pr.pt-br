---
title: Noções básicas sobre problemas de desempenho
description: Este tópico descreve os problemas de desempenho associados ao uso dos padrões de controle Text e TextRange.
ms.assetid: D78BFFA8-E303-441D-9D32-AD22E1B1A249
keywords:
- clientes, compreendendo problemas de desempenho
- clientes, controles baseados em texto
- clientes, intervalos de texto
- clientes, padrão de controle de texto
- clientes, padrão de controle TextRange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61d8d9b9b6c5cb0ef3ed34c6960e5aeafa623068
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104294623"
---
# <a name="understanding-performance-issues"></a><span data-ttu-id="2a065-108">Noções básicas sobre problemas de desempenho</span><span class="sxs-lookup"><span data-stu-id="2a065-108">Understanding Performance Issues</span></span>

<span data-ttu-id="2a065-109">Este tópico descreve os problemas de desempenho associados ao uso dos padrões de controle [Text e TextRange](uiauto-implementingtextandtextrange.md) .</span><span class="sxs-lookup"><span data-stu-id="2a065-109">This topic describes performance issues associated with using the [Text and TextRange](uiauto-implementingtextandtextrange.md) control patterns.</span></span>


<span data-ttu-id="2a065-110">As interfaces [**IUIAutomationTextPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextpattern) e [**IUIAutomationTextRange**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange) dependem de chamadas de processo cruzado — elas não fornecem um mecanismo de cache para melhorar o desempenho ao recuperar ou processar conteúdo textual.</span><span class="sxs-lookup"><span data-stu-id="2a065-110">The [**IUIAutomationTextPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextpattern) and [**IUIAutomationTextRange**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange) interfaces rely on cross-process calls—they do not provide a caching mechanism to improve performance when retrieving or processing textual content.</span></span>

<span data-ttu-id="2a065-111">Um aplicativo cliente pode melhorar o desempenho usando o método [**IUIAutomationTextRange:: gettext**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext) para recuperar blocos de texto de tamanho moderado.</span><span class="sxs-lookup"><span data-stu-id="2a065-111">A client application can improve performance by using the [**IUIAutomationTextRange::GetText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext) method to retrieve moderately sized blocks of text.</span></span> <span data-ttu-id="2a065-112">Por exemplo, usar **gettext** para recuperar caracteres únicos incorrerá em um impacto de desempenho entre processos para cada caractere, enquanto não especificar um comprimento máximo ao chamar **gettext** incorrerá em um impacto entre processos, mas poderá ter alta latência dependendo do tamanho do intervalo de texto.</span><span class="sxs-lookup"><span data-stu-id="2a065-112">For example, using **GetText** to retrieve single characters will incur a cross-process performance hit for each character, whereas not specifying a maximum length when calling **GetText** will incur one cross-process hit, but can have high latency depending on the size of the text range.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2a065-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2a065-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2a065-114">Padrões de controle Text e TextRange</span><span class="sxs-lookup"><span data-stu-id="2a065-114">Text and TextRange Control Patterns</span></span>](uiauto-implementingtextandtextrange.md)
</dt> <dt>

[<span data-ttu-id="2a065-115">Suporte à automação da interface do usuário para conteúdo textual</span><span class="sxs-lookup"><span data-stu-id="2a065-115">UI Automation Support for Textual Content</span></span>](uiauto-ui-automation-textpattern-overview.md)
</dt> <dt>

[<span data-ttu-id="2a065-116">Trabalhando com controles baseados em texto</span><span class="sxs-lookup"><span data-stu-id="2a065-116">Working with Text-based Controls</span></span>](uiauto-workingwithtextbasedcontrols.md)
</dt> </dl>

 

 




