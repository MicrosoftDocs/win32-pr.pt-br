---
title: Erro de TabIndex da função de contêiner do ARIA (sem o descendente ativo)
description: Erro de TabIndex da função de contêiner do ARIA (sem o descendente ativo)
ms.assetid: E3CCA500-7104-4163-927C-94EA8F1E89D8
keywords:
- AriaContainerWithoutActiveDescendantTabIndexErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6eb2198b5ad28cf8a2dd1c625342fef399eefbe3f93ed5e09f4796e06d16338
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994336"
---
# <a name="aria-container-role-without-active-descendant-tabindex-error"></a>Erro de TabIndex da função de contêiner do ARIA (sem o descendente ativo)

## <a name="text"></a>Texto

O elemento é um contêiner de foco sem definição de descendentes ativos, mas nenhum elemento filho tem **TabIndex** maior ou igual a 0.

## <a name="type"></a>Tipo

Erro

## <a name="description"></a>Descrição

Este erro se aplica a elementos que têm uma função de contêiner, não têm um atributo **Aria-activedescendant** e não estão desabilitados. Esses elementos implementam a navegação por teclado entre elementos filho usando o conceito conhecido como *índice de movimentação*. Nesse conceito, os atributos **TabIndex** dos elementos filho são mantidos dinamicamente, garantindo que, em todos os momentos, apenas um elemento filho esteja na ordem de tabulação.

Para corrigir esse erro, defina o atributo **TabIndex** de um dos elementos filho para um valor igual ou maior que 0.

## <a name="example"></a>Exemplo


```HTML
<div id="listbox" role="listbox1">
  <div role="option" id="listbox1-1" tabindex="0" class="selected">Item 1</div>
  <div role="option" id="listbox1-2">Item 2</div>
  <div role="option" id="listbox1-3">Item 3</div>
</div>

<script>

  ...

  listbox1.addEventListener('keyup', function(e) {
    var itm = e.srcElement;
    var prev = itm.previousElementSibling;
    var next = itm.nextElementSibling;

    if (e.keyCode == 38 && prev) {
      // Arrow up to move focus to the previous item.
      itm.setAttribute('tabindex', '-1');
      prev.setAttribute('tabindex','0');
      prev.focus();
    } 

    else if (e.keyCode == 40 && next) {
      // Arrow down to move focus to the next item.
      itm.setAttribute('tabindex', '-1');
      next.setAttribute('tabindex','0');
      next.focus();
    }
  });

</script>
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Erro de TabIndex de contêiner do ARIA](aria-container-tabindex.md)
</dt> </dl>

 

 




