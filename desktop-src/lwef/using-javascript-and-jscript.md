---
title: Usando JavaScript e JScript
description: Usando JavaScript e JScript
ms.assetid: c6927663-9432-4fa9-8de6-abb7237909b9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fbac6d69de69daecbf21c50aafdafce81ed9d95
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104084518"
---
# <a name="using-javascript-and-jscript"></a>Usando JavaScript e JScript

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

Se você usar o JavaScript ou o Microsoft JScript para acessar a interface de programação do Microsoft Agent, siga as convenções para este idioma para especificar métodos ou propriedades:

``` syntax
agent.object.Method (parameter)
agent.object.Property = value
```

No momento, o JavaScript não tem uma sintaxe de evento para objetos não HTML. No entanto, com o Internet Explorer, você pode usar a `<SCRIPT>` marca **para...** Sintaxe do evento:

``` syntax
<SCRIPT LANGUAGE="JScript" FOR="object" EVENT="event()">
statements
</SCRIPT>
```

Como nem todos os navegadores dão suporte a essa sintaxe de evento, talvez você queira usar o JavaScript somente para páginas que dão suporte ao Microsoft Internet Explorer ou para códigos que não exigem manipulação de eventos.

Para acessar as coleções de objetos do agente, use a função de [**enumerador**](https://www.bing.com/search?q=**Enumerator**) do JScript. No entanto, as versões do JScript incluídas antes do Internet Explorer 4,0 não dão suporte a essa função e não oferecem suporte a coleções. Para acessar métodos e propriedades do objeto [**Character**](/windows/desktop/lwef/the-characters-object) , use o método [**Character**](character-method.md) . Da mesma forma, para acessar as propriedades de um objeto de [**comando**](/windows/desktop/lwef/the-command-object) , use o método de [**comando**](command-method.md) .

 

 