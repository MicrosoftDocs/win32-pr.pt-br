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
# <a name="aria-container-role-without-active-descendant-keyboard-accessibility-error"></a>Erro de acessibilidade do teclado (sem o descendente ativo) da função de contêiner do ARIA

## <a name="text"></a>Texto

O elemento é um contêiner com foco sem um descendente ativo definido e sem os / manipuladores de eventos de AoApertarTecla **OnKeyPress** / **onkeyup** (nem no contêiner nem em um dos elementos filho).

## <a name="type"></a>Tipo

Erro

## <a name="description"></a>Descrição

Este erro se aplica a elementos que têm uma função de contêiner, não têm um atributo **Aria-activedescendant** e não estão desabilitados. Esses elementos implementam a navegação por teclado entre elementos filho usando o conceito conhecido como *índice de movimentação*. Nesse conceito, os atributos **TabIndex** dos elementos filho são mantidos dinamicamente, garantindo que, em todos os momentos, apenas um elemento filho esteja na ordem de tabulação.

Esse erro indica que um elemento de contêiner que não tem o atributo **Aria-activedescendant** e que não está desabilitado não está acessível para usuários de teclado. O problema existe porque o contêiner não tem os manipuladores de eventos de teclado necessários (**KeyDown**, **KeyUp** ou **KeyPress**) e nenhum dos elementos filho do contêiner.

Para corrigir esse erro, defina um manipulador de eventos **KeyDown**, **KeyUp** ou **KeyPress** para o contêiner ou um de seus elementos filho.

## <a name="example"></a>Exemplo


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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Erro de acessibilidade do teclado da função de contêiner do ARIA](aria-container-keyboard-events.md)
</dt> </dl>

 

 




