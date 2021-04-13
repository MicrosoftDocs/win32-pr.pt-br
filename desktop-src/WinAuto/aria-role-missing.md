---
title: Erro de função do ARIA para elementos com manipuladores de eventos
description: Erro de função do ARIA para elementos com manipuladores de eventos
ms.assetid: 20BB874A-874B-4266-9C7B-49C07D4146DA
keywords:
- AriaContainerRoleErrorMessage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eede416392e8b4cb644938242a9975238118ff07
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/09/2020
ms.locfileid: "104366853"
---
# <a name="aria-role-error-for-elements-with-event-handlers"></a><span data-ttu-id="42e4b-104">Erro de função do ARIA para elementos com manipuladores de eventos</span><span class="sxs-lookup"><span data-stu-id="42e4b-104">ARIA Role Error for elements with event handlers</span></span>

## <a name="text"></a><span data-ttu-id="42e4b-105">Texto</span><span class="sxs-lookup"><span data-stu-id="42e4b-105">Text</span></span>

<span data-ttu-id="42e4b-106">O elemento tem um manipulador de eventos, mas uma função WAI-ARIA válida não está definida.</span><span class="sxs-lookup"><span data-stu-id="42e4b-106">Element has an event handler but valid WAI-ARIA role is not defined.</span></span>

## <a name="type"></a><span data-ttu-id="42e4b-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="42e4b-107">Type</span></span>

<span data-ttu-id="42e4b-108">Erro</span><span class="sxs-lookup"><span data-stu-id="42e4b-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="42e4b-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="42e4b-109">Description</span></span>

<span data-ttu-id="42e4b-110">Esse erro se aplica a elementos que não têm uma função de WAI (aplicativos de Internet sofisticado) acessível por iniciativa de acessibilidade da Web.</span><span class="sxs-lookup"><span data-stu-id="42e4b-110">This error applies to elements that do not have an implicit Web Accessibility Initiative - Accessible Rich Internet Applications (WAI-ARIA) role.</span></span>

<span data-ttu-id="42e4b-111">Esse erro indica que um elemento tem um manipulador de eventos de mouse ou de teclado (**clique**, **MouseDown**, **MouseUp**, **MouseMove**, **mouseout**, **mouseover**, **KeyUp**, **KeyDown** ou **KEYPRESS**), mas não tem o atributo de [**função**](https://developer.mozilla.org/docs/Web/HTML/Reference) definido e não é uma das marcas HTML que tem uma função implícita WAI-ARIA (por exemplo, **a**, **Button**, **img**, **entrada**, **Select** e assim por diante).</span><span class="sxs-lookup"><span data-stu-id="42e4b-111">This error indicates that an element has a mouse or keyboard event handler (**click**, **mousedown**, **mouseup**, **mousemove**, **mouseout**, **mouseover**, **keyup**, **keydown**, or **keypress**), but doesn’t have the [**role**](https://developer.mozilla.org/docs/Web/HTML/Reference) attribute set, and is not one of the HTML tags that has an implicit WAI-ARIA role (for example, **a**, **button**, **img**, **input**, **select** and so on).</span></span>

<span data-ttu-id="42e4b-112">Definir o atributo [**role**](https://developer.mozilla.org/docs/Web/HTML/Reference) para elementos interativos que não têm nenhuma função implícita (como uma marca **div** ) é necessário para expor os padrões de comportamento do elemento para leitores de tela e outras tecnologias assistenciais.</span><span class="sxs-lookup"><span data-stu-id="42e4b-112">Setting the [**role**](https://developer.mozilla.org/docs/Web/HTML/Reference) attribute for interactive elements that have no implicit role (such as a **div** tag) is necessary to expose the element's behavior patterns to screen readers and other assistive technologies.</span></span>

<span data-ttu-id="42e4b-113">Para corrigir esse erro, defina o atributo [**role**](https://developer.mozilla.org/docs/Web/HTML/Reference) como uma função WAI-ARIA válida que melhor atenda aos padrões de comportamento e aos atributos necessários do elemento.</span><span class="sxs-lookup"><span data-stu-id="42e4b-113">To fix this error, set the [**role**](https://developer.mozilla.org/docs/Web/HTML/Reference) attribute to a valid WAI-ARIA role that best fits this element's behavior patterns and required attributes.</span></span> <span data-ttu-id="42e4b-114">Por exemplo, se uma tag **div** funcionar como um botão, defina o atributo role como "Button".</span><span class="sxs-lookup"><span data-stu-id="42e4b-114">For example, if a **div** tag functions as a button, set the role attribute to "button".</span></span>

## <a name="example"></a><span data-ttu-id="42e4b-115">Exemplo</span><span class="sxs-lookup"><span data-stu-id="42e4b-115">Example</span></span>


```HTML
<!-- Setting role attribute allows screen readers to know it can be clicked -->
<div role="button" tabindex="0" aria-label="Back" onclick="mouseAction(event)" onkeyup="keyAction(event)" >
```



 

 




