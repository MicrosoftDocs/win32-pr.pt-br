---
title: Erro de acessibilidade do teclado (sem o descendente ativo) da função de contêiner do ARIA
description: Erro de acessibilidade do teclado (sem o descendente ativo) da função de contêiner do ARIA
ms.assetid: 15EDD3CC-FC2A-42FC-95DD-B04D9AF3515E
keywords:
- AriaContainerWithoutActiveDescendantKeyboardAccessiblityId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d9e30e0194f156426e2b61aa774ac1f3e0f5b91
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822619"
---
# <a name="aria-container-role-without-active-descendant-keyboard-accessibility-error"></a><span data-ttu-id="3fc1b-104">Erro de acessibilidade do teclado (sem o descendente ativo) da função de contêiner do ARIA</span><span class="sxs-lookup"><span data-stu-id="3fc1b-104">ARIA Container Role (without active descendant) Keyboard Accessibility Error</span></span>

## <a name="text"></a><span data-ttu-id="3fc1b-105">Texto</span><span class="sxs-lookup"><span data-stu-id="3fc1b-105">Text</span></span>

<span data-ttu-id="3fc1b-106">O elemento é um contêiner com foco sem um descendente ativo definido e sem os / manipuladores de eventos de AoApertarTecla **OnKeyPress** / **onkeyup** (nem no contêiner nem em um dos elementos filho).</span><span class="sxs-lookup"><span data-stu-id="3fc1b-106">Element is a focusable container without active descendant defined and without **OnKeyDown**/**OnKeyPress**/**OnKeyUp** event handlers (neither on container nor on one of child elements).</span></span>

## <a name="type"></a><span data-ttu-id="3fc1b-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="3fc1b-107">Type</span></span>

<span data-ttu-id="3fc1b-108">Erro</span><span class="sxs-lookup"><span data-stu-id="3fc1b-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="3fc1b-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="3fc1b-109">Description</span></span>

<span data-ttu-id="3fc1b-110">Este erro se aplica a elementos que têm uma função de contêiner, não têm um atributo **Aria-activedescendant** e não estão desabilitados.</span><span class="sxs-lookup"><span data-stu-id="3fc1b-110">This error applies to elements that have a container role, do not have an **aria-activedescendant** attribute, and are not disabled.</span></span> <span data-ttu-id="3fc1b-111">Esses elementos implementam a navegação por teclado entre elementos filho usando o conceito conhecido como *índice de movimentação*.</span><span class="sxs-lookup"><span data-stu-id="3fc1b-111">These elements implement keyboard navigation among child elements by using the concept known as *roving index*.</span></span> <span data-ttu-id="3fc1b-112">Nesse conceito, os atributos **TabIndex** dos elementos filho são mantidos dinamicamente, garantindo que, em todos os momentos, apenas um elemento filho esteja na ordem de tabulação.</span><span class="sxs-lookup"><span data-stu-id="3fc1b-112">In this concept, the **tabindex** attributes of child elements are maintained dynamically, ensuring that at all times only one child element is in tab order.</span></span>

<span data-ttu-id="3fc1b-113">Esse erro indica que um elemento de contêiner que não tem o atributo **Aria-activedescendant** e que não está desabilitado não está acessível para usuários de teclado.</span><span class="sxs-lookup"><span data-stu-id="3fc1b-113">This error indicates that a container element that does not have the **aria-activedescendant** attribute, and that is not disabled, is not accessible to keyboard users.</span></span> <span data-ttu-id="3fc1b-114">O problema existe porque o contêiner não tem os manipuladores de eventos de teclado necessários (**KeyDown**, **KeyUp** ou **KeyPress**) e nenhum dos elementos filho do contêiner.</span><span class="sxs-lookup"><span data-stu-id="3fc1b-114">The problem exists because the container does not have the needed keyboard event handlers (**keydown**, **keyup**, or **keypress**), and neither do any of the container's child elements.</span></span>

<span data-ttu-id="3fc1b-115">Para corrigir esse erro, defina um manipulador de eventos **KeyDown**, **KeyUp** ou **KeyPress** para o contêiner ou um de seus elementos filho.</span><span class="sxs-lookup"><span data-stu-id="3fc1b-115">To fix this error, define a **keydown**, **keyup**, or **keypress** event handler for the container or one of its child elements.</span></span>

## <a name="example"></a><span data-ttu-id="3fc1b-116">Exemplo</span><span class="sxs-lookup"><span data-stu-id="3fc1b-116">Example</span></span>


```HTML
<div role="listbox" id="listbox1" >
  <div role="option" id="listbox1-1" tabindex="0" class="selected">Item 1</div>
  <div role="option" id="listbox1-2">Item 2</div>
  <div role="option" id="listbox1-3">Item 3</div>
  ...
<div>

<script>

  ...

  listbox1.addEventListener('keyup', function(e) {
    var itm = e.srcElement;
    var prev = itm.previousElementSibling;
    var next = itm.nextElementSibling;

    if (e.keyCode == 38 && prev) {
      // On arrow up move focus to the previous item.
      itm.setAttribute('tabindex', '-1');
      prev.setAttribute('tabindex','0');
      prev.focus();
    }

    else if (e.keyCode == 40 && next) {
      // On arrow down move focus to the next item.
      itm.setAttribute('tabindex', '-1');
      next.setAttribute('tabindex','0');
      next.focus();
    }
  });

</script>
```



## <a name="related-topics"></a><span data-ttu-id="3fc1b-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3fc1b-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3fc1b-118">Erro de acessibilidade do teclado da função de contêiner do ARIA</span><span class="sxs-lookup"><span data-stu-id="3fc1b-118">ARIA Container Role Keyboard Accessibility Error</span></span>](aria-container-keyboard-events.md)
</dt> </dl>

 

 




