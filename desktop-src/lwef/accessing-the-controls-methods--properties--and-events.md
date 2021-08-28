---
title: Acessando os métodos, propriedades e eventos de controles
description: Acessando os métodos, propriedades e eventos de controles
ms.assetid: 70a3b011-0290-4df4-9b66-23b27bcb14e9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed14138da0e6aef0bba46be796813cbe0945195dec2243bbb8bb763ddfb47517
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118480742"
---
# <a name="accessing-the-controls-methods-properties-and-events"></a>Acessando os métodos, propriedades e eventos de controles

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

Usar o controle do Microsoft Agent com Visual Basic é muito semelhante ao uso do controle com VBScript, exceto que os eventos no Visual Basic devem incluir o tipo de dados dos parâmetros passados. Adicionar o controle do Microsoft Agent a um formulário incluirá automaticamente os eventos do Microsoft Agent com seus parâmetros apropriados. Ele também criará automaticamente uma conexão com o servidor do Agent quando o aplicativo for executado.

Você também pode usar a sintaxe de criação do objeto da linguagem de programação para criar uma instância do controle em runtime. Por exemplo, no Visual Basic (5.0 ou posterior), se você incluir o Controle do Microsoft Agent 2.0 nas referências do projeto, poderá usar um [**Com**](https://www.bing.com/search?q=**With+Events**)Eventos .. [**Nova**](https://www.bing.com/search?q=**New**) declaração. Se você não incluir a referência, a VB gera um erro indicando que o Microsoft Agent não pôde iniciar (código de erro 80042502).

``` syntax
   ' Declare a global variable for the control
   Dim WithEvents MyAgent as Agent

   ' Create an instance of the control using New
   Set MyAgent = New Agent

' Load a character
   MyAgent.Characters.Load "Genie", " Genie.acs"

   ' Display the character
   MyAgent.Characters("Genie").Show
```

Para versões da VB anteriores à 5.0, você pode usar a palavra-chave Nova [**VB**](https://www.bing.com/search?q=**New**) sem a declaração [**WithEvents**](https://www.bing.com/search?q=**WithEvents**) ou a função [**CreateObject**](https://msdn.microsoft.com/library/Bb545141(v=VS.85).aspx) do VB, mas essas convenções não exporão os eventos do controle agent. Você também precisa usar a [**propriedade Connected**](https://www.bing.com/search?q=**Connected**) antes de referenciar quaisquer métodos ou propriedades do Agent. Se isso não for feito, a VB gera um erro indicando que o Microsoft Agent não pôde iniciar (código de erro 80042502).

Da mesma forma, para outras linguagens de programação, talvez seja preciso usar a propriedade [**Connected**](https://www.bing.com/search?q=**Connected**) para estabelecer uma conexão com o servidor COM (Agente Component Object Model) antes que seu código possa chamar qualquer um dos métodos ou propriedades do controle Agent. Além disso, para algumas linguagens de programação, os métodos e as propriedades do Agent podem não ser expostos diretamente, a menos que você declare o controle agent usando seu tipo. Por exemplo, no Microsoft Access 97, você precisará declarar o objeto como tipo Agent para ver os métodos e propriedades exibidos na caixa de lista de membros da lista automática de membros ao digitar.

A maioria das linguagens de programação que ActiveX controles de programação segue convenções semelhantes às Visual Basic. Para linguagens de programação que não têm suporte para coleções de objetos, você pode usar o método [**Character**](https://www.bing.com/search?q=**Character**) e o método [**Command**](https://www.bing.com/search?q=**Command**) para acessar métodos e propriedades de itens na coleção.

Linguagens de programação como Visual Basic, que fornecem acesso aos tipos de objeto expostos pelo controle Agent, permitem que você as use em suas declarações de objeto. Por exemplo, em vez de declarar um objeto como um tipo genérico:

``` syntax
   Dim Genie as Object
```

Você pode declarar um objeto como um tipo específico:

``` syntax
   Dim Genie as IAgentCtlCharacterEx
```

Isso pode melhorar o desempenho geral do seu aplicativo.

Para alguns tipos de objeto, você pode encontrar dois tipos que são os mesmos, exceto o sufixo "Ex". Quando ambos existirem, use o tipo "Ex", pois isso fornece a funcionalidade completa do Agent. As contrapartes que não são "Ex" são incluídas apenas para compatibilidade com backward.

 

 




