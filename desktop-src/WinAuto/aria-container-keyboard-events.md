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
# <a name="aria-container-role-keyboard-accessibility-error"></a>Erro de acessibilidade do teclado da função de contêiner do ARIA

## <a name="text"></a>Texto

O elemento é um contêiner com o descendente ativo e a funcionalidade personalizada do mouse, mas sem a funcionalidade de teclado correspondente: manipuladores de eventos JavaScript para **OnKeyDown** ou **OnKeyPress**.

## <a name="type"></a>Tipo

Erro

## <a name="description"></a>Descrição

Esse erro se aplica a elementos que têm o atributo **Aria-activedescendant** . Esses elementos têm um ou mais manipuladores de eventos do mouse (**MouseMove**, **MouseDown** ou **MouseUp**), mas estão faltando os manipuladores de eventos de teclado equivalentes (**KeyDown**, **KeyUp** ou **KeyPress**). Os manipuladores de eventos de teclado são necessários para garantir que o usuário possa invocar a funcionalidade do elemento usando o teclado e para garantir que o elemento Mantenha o atributo **Aria-activedescendant** .

Para corrigir esse erro, implemente um dos manipuladores de eventos de teclado.

## <a name="example"></a>Exemplo


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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Erro de acessibilidade do teclado (sem o descendente ativo) da função de contêiner do ARIA](aria-container--no-active-descendants--keyboard-events.md)
</dt> </dl>

 

 




