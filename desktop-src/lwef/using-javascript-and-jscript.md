---
title: Usando JavaScript e JScript
description: Usando JavaScript e JScript
ms.assetid: c6927663-9432-4fa9-8de6-abb7237909b9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f3b32fd3d8e2c8ce9e337f489c27dadaa32bb379d6bc90c6083d62af52bee24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119960676"
---
# <a name="using-javascript-and-jscript"></a>Usando JavaScript e JScript

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

Se você usar JavaScript ou Microsoft JScript para acessar a interface de programação do Microsoft Agent, siga as convenções para essa linguagem para especificar métodos ou propriedades:

``` syntax
agent.object.Method (parameter)
agent.object.Property = value
```

Atualmente, o JavaScript não tem sintaxe de evento para objetos não HTML. No entanto, com Internet Explorer você pode usar `<SCRIPT>` a **marca para... Sintaxe do** evento:

``` syntax
<SCRIPT LANGUAGE="JScript" FOR="object" EVENT="event()">
statements
</SCRIPT>
```

Como nem todos os navegadores atualmente suportam essa sintaxe de evento, talvez você queira usar JavaScript apenas para páginas que suportam o Microsoft Internet Explorer ou para código que não exige manipulação de eventos.

Para acessar as coleções de objetos do Agent, use a função JScript [**enumerador.**](https://www.bing.com/search?q=**Enumerator**) No entanto, as versões JScript incluídas antes do Internet Explorer 4.0 não são suportadas por essa função e não são suportadas por coleções. Para acessar métodos e propriedades do objeto [**Character,**](/windows/desktop/lwef/the-characters-object) use o [**método**](character-method.md) Character. Da mesma forma, para acessar as propriedades de um [**objeto Command,**](/windows/desktop/lwef/the-command-object) use o [**método**](command-method.md) Command.

 

 