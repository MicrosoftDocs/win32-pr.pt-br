---
title: Erro de acessibilidade do teclado da Função de Contêiner do ARIA (sem descendente ativo)
description: Erro de acessibilidade do teclado da Função de Contêiner do ARIA (sem descendente ativo)
ms.assetid: 15EDD3CC-FC2A-42FC-95DD-B04D9AF3515E
keywords:
- AriaContainerWithoutActiveDescendantKeyboardAccessiblityId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30b653ac3bf2dc8254b25c52a89cdb3503b89b9f05997a3ea9fb4f4ef3a77cb7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120071876"
---
# <a name="aria-container-role-without-active-descendant-keyboard-accessibility-error"></a>Erro de acessibilidade do teclado da Função de Contêiner do ARIA (sem descendente ativo)

## <a name="text"></a>Texto

O elemento é um contêiner focalizado sem descendente ativo definido e sem manipuladores de eventos / **OnKeyPress OnKeyUp** / **onKeyPress** (nem no contêiner nem em um dos elementos filho).

## <a name="type"></a>Tipo

Erro

## <a name="description"></a>Descrição

Esse erro se aplica a elementos que têm uma função de contêiner, não têm um atributo **aria-activedescendant** e não estão desabilitados. Esses elementos implementam a navegação por teclado entre elementos filho usando o conceito conhecido como *índice de aprovação*. Nesse conceito, os atributos **tabindex** de elementos filho são mantidos dinamicamente, garantindo que, em todos os momentos, apenas um elemento filho está na ordem de tabulação.

Esse erro indica que um elemento de contêiner que não tem o atributo **aria-activedescendant** e que não está desabilitado não está acessível aos usuários de teclado. O problema existe porque o contêiner não tem os manipuladores de eventos de teclado necessários **(keydown,** **keyup** ou **keypress)** e nenhum dos elementos filho do contêiner.

Para corrigir esse erro, defina um manipulador de eventos **keydown**, **keyup** ou **keypress** para o contêiner ou um de seus elementos filho.

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

 

 




