---
title: Acessando os métodos, as propriedades e os eventos dos controles
description: Acessando os métodos, as propriedades e os eventos dos controles
ms.assetid: 70a3b011-0290-4df4-9b66-23b27bcb14e9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 750ad6280b521cf50c2ecd1fb7f1fcec3e2c4164
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363931"
---
# <a name="accessing-the-controls-methods-properties-and-events"></a>Acessando os métodos, as propriedades e os eventos dos controles

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

Usar o controle do Microsoft Agent com o Visual Basic é muito semelhante ao uso do controle com o VBScript, exceto pelo fato de que os eventos em Visual Basic devem incluir o tipo de dados dos parâmetros passados. Adicionar o controle do Microsoft Agent a um formulário incluirá automaticamente os eventos do Microsoft Agent com seus parâmetros apropriados. Ele também criará automaticamente uma conexão com o servidor do agente quando o aplicativo for executado.

Você também pode usar a sintaxe de criação de object's da linguagem de programação para criar uma instância do controle em tempo de execução. Por exemplo, no Visual Basic (5,0 ou posterior), se você incluir o controle do Microsoft Agent 2,0 nas referências do seu projeto, poderá usar um [**com eventos**](https://www.bing.com/search?q=**With+Events**).. [**Nova**](https://www.bing.com/search?q=**New**) declaração. Se você não incluir a referência, o VB gerará um erro indicando que o Microsoft Agent não pôde ser iniciado (código de erro 80042502).

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

Para versões do VB anteriores a 5,0, você pode usar a palavra-chave [**New**](https://www.bing.com/search?q=**New**) do VB sem declaração [**WithEvents**](https://www.bing.com/search?q=**WithEvents**) ou a função do VB [**CreateObject**](https://msdn.microsoft.com/library/Bb545141(v=VS.85).aspx) , mas essas convenções não expõem os eventos do controle do agente. Você também precisa usar a propriedade [**Connected**](https://www.bing.com/search?q=**Connected**) antes de fazer referência a qualquer método ou Propriedade do agente. Se isso não for feito, o VB gerará um erro indicando que o Microsoft Agent não pôde ser iniciado (código de erro 80042502).

Da mesma forma, para outras linguagens de programação, você pode precisar usar a propriedade [**Connected**](https://www.bing.com/search?q=**Connected**) para estabelecer uma conexão com o servidor de Component Object Model de agente (com) antes que seu código possa chamar qualquer um dos métodos ou propriedades do controle Agent. Além disso, para algumas linguagens de programação, os métodos e as propriedades do agente podem não ser expostos diretamente, a menos que você declare o controle de agente usando seu tipo. Por exemplo, no Microsoft Access 97, você precisará declarar o objeto como agente de tipo para ver os métodos e as propriedades exibidos na caixa suspensa Listar Membros automaticamente ao digitar.

A maioria das linguagens de programação que dão suporte a controles ActiveX segue convenções semelhantes a Visual Basic. Para linguagens de programação que não dão suporte a coleções de objetos, você pode usar o método de [**caractere**](https://www.bing.com/search?q=**Character**) e o método de [**comando**](https://www.bing.com/search?q=**Command**) para acessar métodos e propriedades de itens na coleção.

Linguagens de programação como Visual Basic, que fornecem acesso aos tipos de objeto expostos pelo controle Agent, permitem que você as use em suas declarações de objeto. Por exemplo, em vez de declarar um objeto como um tipo genérico:

``` syntax
   Dim Genie as Object
```

Você pode declarar um objeto como um tipo específico:

``` syntax
   Dim Genie as IAgentCtlCharacterEx
```

Isso pode melhorar o desempenho geral do seu aplicativo.

Para alguns tipos de objeto, você pode encontrar dois tipos que são iguais, exceto o sufixo "ex". Onde ambos existem, use o tipo "ex" porque isso fornece a funcionalidade completa do Agent. As contrapartes não "ex" são incluídas apenas para compatibilidade com versões anteriores.

 

 




