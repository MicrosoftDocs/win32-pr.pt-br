---
title: Erro de acessibilidade do teclado da função de contêiner do ARIA
description: Erro de acessibilidade do teclado da função de contêiner do ARIA
ms.assetid: 364F26D7-7B65-418B-9DA5-F3B7B59284F7
keywords:
- AriaContainerKeyboardAccessibilityErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 085591e4f4834e8088b5ca199918d621f518e678
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292425"
---
# <a name="aria-container-role-keyboard-accessibility-error"></a><span data-ttu-id="5fbc7-104">Erro de acessibilidade do teclado da função de contêiner do ARIA</span><span class="sxs-lookup"><span data-stu-id="5fbc7-104">ARIA Container Role Keyboard Accessibility Error</span></span>

## <a name="text"></a><span data-ttu-id="5fbc7-105">Texto</span><span class="sxs-lookup"><span data-stu-id="5fbc7-105">Text</span></span>

<span data-ttu-id="5fbc7-106">O elemento é um contêiner com o descendente ativo e a funcionalidade personalizada do mouse, mas sem a funcionalidade de teclado correspondente: manipuladores de eventos JavaScript para **OnKeyDown** ou **OnKeyPress**.</span><span class="sxs-lookup"><span data-stu-id="5fbc7-106">Element is a container with active descendant and custom mouse functionality but without the corresponding keyboard functionality: JavaScript event handlers for **OnKeyDown** or **OnKeyPress**.</span></span>

## <a name="type"></a><span data-ttu-id="5fbc7-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="5fbc7-107">Type</span></span>

<span data-ttu-id="5fbc7-108">Erro</span><span class="sxs-lookup"><span data-stu-id="5fbc7-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="5fbc7-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="5fbc7-109">Description</span></span>

<span data-ttu-id="5fbc7-110">Esse erro se aplica a elementos que têm o atributo **Aria-activedescendant** .</span><span class="sxs-lookup"><span data-stu-id="5fbc7-110">This error applies to elements that have the **aria-activedescendant** attribute.</span></span> <span data-ttu-id="5fbc7-111">Esses elementos têm um ou mais manipuladores de eventos do mouse (**MouseMove**, **MouseDown** ou **MouseUp**), mas estão faltando os manipuladores de eventos de teclado equivalentes (**KeyDown**, **KeyUp** ou **KeyPress**).</span><span class="sxs-lookup"><span data-stu-id="5fbc7-111">These elements have one or more mouse event handlers (**mousemove**, **mousedown** or **mouseup**), but are missing the equivalent keyboard event handlers (**keydown**, **keyup** or **keypress**).</span></span> <span data-ttu-id="5fbc7-112">Os manipuladores de eventos de teclado são necessários para garantir que o usuário possa invocar a funcionalidade do elemento usando o teclado e para garantir que o elemento Mantenha o atributo **Aria-activedescendant** .</span><span class="sxs-lookup"><span data-stu-id="5fbc7-112">The keyboard event handlers are needed to ensure that the user can invoke the element's functionality by using the keyboard, and to ensure that the element maintains the **aria-activedescendant** attribute.</span></span>

<span data-ttu-id="5fbc7-113">Para corrigir esse erro, implemente um dos manipuladores de eventos de teclado.</span><span class="sxs-lookup"><span data-stu-id="5fbc7-113">To fix this error, implement one of the keyboard event handlers.</span></span>

## <a name="example"></a><span data-ttu-id="5fbc7-114">Exemplo</span><span class="sxs-lookup"><span data-stu-id="5fbc7-114">Example</span></span>


```HTML
<div role="listbox" id="listbox1" tabindex="0" aria-activedescendant="listbox1-1"> 
  <div role="option" id="listbox1-1" class="selected">Item 1</div>
  <div role="option" id="listbox1-2">Item 2</div>
  <div role="option" id="listbox1-3">Item 3</div>
</div>

<script>

   ...

  listbox1.addEventListener('keyup', function(e) {
    var itm = document.getElementById(this.getAttribute('aria-activedescendant'));
    var prev = itm.previousElementSibling;
    var next = itm.nextElementSibling;
    
    if ( e.keyCode  38 && prev ) {
      // Arrow up to move active descendant to the previous item
      itm.removeAttribute('class’);
      prev.setAttribute("class", "selected");
      this.setAttribute ('aria-activedescendant', prev.id)
    } 

    else if ( e.keyCode == 40 && next) {
      // Arrow down to move focus to the next item
      itm.removeAttribute('class’);
      next.setAttribute("class", "selected");
      this.setAttribute ('aria-activedescendant', next.id)
    }
  });      

</script>
```



## <a name="related-topics"></a><span data-ttu-id="5fbc7-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5fbc7-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5fbc7-116">Erro de acessibilidade do teclado (sem o descendente ativo) da função de contêiner do ARIA</span><span class="sxs-lookup"><span data-stu-id="5fbc7-116">ARIA Container Role (without active descendant) Keyboard Accessibility Error</span></span>](aria-container--no-active-descendants--keyboard-events.md)
</dt> </dl>

 

 




