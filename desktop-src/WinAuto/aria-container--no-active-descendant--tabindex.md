---
title: Erro de TabIndex da função de contêiner do ARIA (sem o descendente ativo)
description: Erro de TabIndex da função de contêiner do ARIA (sem o descendente ativo)
ms.assetid: E3CCA500-7104-4163-927C-94EA8F1E89D8
keywords:
- AriaContainerWithoutActiveDescendantTabIndexErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a01d3391d93b7e7f146f379bcfecd629e14bce7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159847"
---
# <a name="aria-container-role-without-active-descendant-tabindex-error"></a><span data-ttu-id="57355-104">Erro de TabIndex da função de contêiner do ARIA (sem o descendente ativo)</span><span class="sxs-lookup"><span data-stu-id="57355-104">ARIA Container Role (without active descendant) Tabindex Error</span></span>

## <a name="text"></a><span data-ttu-id="57355-105">Texto</span><span class="sxs-lookup"><span data-stu-id="57355-105">Text</span></span>

<span data-ttu-id="57355-106">O elemento é um contêiner de foco sem definição de descendentes ativos, mas nenhum elemento filho tem **TabIndex** maior ou igual a 0.</span><span class="sxs-lookup"><span data-stu-id="57355-106">Element is a focusable container without active descendant defined, but no child element has **tabindex** greater or equal to 0.</span></span>

## <a name="type"></a><span data-ttu-id="57355-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="57355-107">Type</span></span>

<span data-ttu-id="57355-108">Erro</span><span class="sxs-lookup"><span data-stu-id="57355-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="57355-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="57355-109">Description</span></span>

<span data-ttu-id="57355-110">Este erro se aplica a elementos que têm uma função de contêiner, não têm um atributo **Aria-activedescendant** e não estão desabilitados.</span><span class="sxs-lookup"><span data-stu-id="57355-110">This error applies to elements that have a container role, do not have an **aria-activedescendant** attribute, and are not disabled.</span></span> <span data-ttu-id="57355-111">Esses elementos implementam a navegação por teclado entre elementos filho usando o conceito conhecido como *índice de movimentação*.</span><span class="sxs-lookup"><span data-stu-id="57355-111">These elements implement keyboard navigation among child elements by using the concept known as *roving index*.</span></span> <span data-ttu-id="57355-112">Nesse conceito, os atributos **TabIndex** dos elementos filho são mantidos dinamicamente, garantindo que, em todos os momentos, apenas um elemento filho esteja na ordem de tabulação.</span><span class="sxs-lookup"><span data-stu-id="57355-112">In this concept, the **tabindex** attributes of child elements are maintained dynamically, ensuring that at all times only one child element is in tab order.</span></span>

<span data-ttu-id="57355-113">Para corrigir esse erro, defina o atributo **TabIndex** de um dos elementos filho para um valor igual ou maior que 0.</span><span class="sxs-lookup"><span data-stu-id="57355-113">To fix this error, set the **tabindex** attribute of one of the child elements to a value equal to or greater than 0.</span></span>

## <a name="example"></a><span data-ttu-id="57355-114">Exemplo</span><span class="sxs-lookup"><span data-stu-id="57355-114">Example</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="57355-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="57355-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="57355-116">Erro de TabIndex de contêiner do ARIA</span><span class="sxs-lookup"><span data-stu-id="57355-116">ARIA Container Tabindex Error</span></span>](aria-container-tabindex.md)
</dt> </dl>

 

 




