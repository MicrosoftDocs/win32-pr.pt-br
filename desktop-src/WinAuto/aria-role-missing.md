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
# <a name="aria-role-error-for-elements-with-event-handlers"></a>Erro de função do ARIA para elementos com manipuladores de eventos

## <a name="text"></a>Texto

O elemento tem um manipulador de eventos, mas uma função WAI-ARIA válida não está definida.

## <a name="type"></a>Tipo

Erro

## <a name="description"></a>Descrição

Esse erro se aplica a elementos que não têm uma função de WAI (aplicativos de Internet sofisticado) acessível por iniciativa de acessibilidade da Web.

Esse erro indica que um elemento tem um manipulador de eventos de mouse ou de teclado (**clique**, **MouseDown**, **MouseUp**, **MouseMove**, **mouseout**, **mouseover**, **KeyUp**, **KeyDown** ou **KEYPRESS**), mas não tem o atributo de [**função**](https://developer.mozilla.org/docs/Web/HTML/Reference) definido e não é uma das marcas HTML que tem uma função implícita WAI-ARIA (por exemplo, **a**, **Button**, **img**, **entrada**, **Select** e assim por diante).

Definir o atributo [**role**](https://developer.mozilla.org/docs/Web/HTML/Reference) para elementos interativos que não têm nenhuma função implícita (como uma marca **div** ) é necessário para expor os padrões de comportamento do elemento para leitores de tela e outras tecnologias assistenciais.

Para corrigir esse erro, defina o atributo [**role**](https://developer.mozilla.org/docs/Web/HTML/Reference) como uma função WAI-ARIA válida que melhor atenda aos padrões de comportamento e aos atributos necessários do elemento. Por exemplo, se uma tag **div** funcionar como um botão, defina o atributo role como "Button".

## <a name="example"></a>Exemplo


```HTML
<!-- Setting role attribute allows screen readers to know it can be clicked -->
<div role="button" tabindex="0" aria-label="Back" onclick="mouseAction(event)" onkeyup="keyAction(event)" >
```



 

 




