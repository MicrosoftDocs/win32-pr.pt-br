---
description: JSON (JavaScript Object Notation)
ms.assetid: 2F6FDE88-C852-46BC-B6B1-630C266AF0AA
title: JSON (JavaScript Object Notation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b1b5f12a2c4e3a4cd0a66a8f917c3cdf41ed17d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088184"
---
# <a name="javascript-object-notation-json"></a>JSON (JavaScript Object Notation)

[JavaScript Object Notation (JSON)](https://www.json.org/) é um formato de intercâmbio de dados simples e leve baseado em um subconjunto da notação literal do objeto da linguagem JavaScript. O mecanismo de JavaScript no Windows Internet Explorer 8 implementa a [proposta de json 3,1 do ECMAScript](https://www.ecma-international.org/) para funções nativas de manipulação de JSON (que usa a [API de json2.js do Douglas Crockford](https://github.com/douglascrockford/JSON-js/blob/master/json2.js)).

O Internet Explorer 8 inclui um objeto JSON nativo que está em conformidade com o suporte a JSON descrito no [rascunho de trabalho da proposta es 3.1](https://www.ecma-international.org/). Algumas páginas da Web detectam o objeto JSON nativo e, em seguida, o utilizam de forma não padrão. Esse uso normalmente causa um erro de script e interrompe a manipulação de solicitações AJAX. O exemplo de código a seguir mostra a maneira errada de usar o objeto JSON.


```JScript
    if(!window.JSON) JSON = myJSON; 
    JSON.encode(obj); // Not part of the standard
```



Em vez disso, o exemplo de código a seguir mostra uma boa maneira de usar o objeto JSON.


```JScript
    JSON = myJSON; 
    JSON.encode(obj);
```



O Windows Internet Explorer inclui suporte nativo para JSON introduzindo um objeto JSON global que tem dois métodos internos: **stringify** e **Parse**. O objeto JSON global é definido no mecanismo de JavaScript e é criado durante a fase de inicialização do mecanismo. Para manter a compatibilidade com versões anteriores, esse recurso está disponível somente quando um site usa a versão mais recente dos recursos do JavaScript usando o modo de layout "padrões do Internet Explorer 8" (documento). Esse recurso também pode afetar o comportamento de páginas da Web que dependem de uma variável global JSON ou usam [json2.js](https://github.com/douglascrockford/JSON-js/blob/master/json2.js).

Você pode substituir o objeto JSON global. Mas quando uma página da Web usa o modo de layout (documento) "padrões do Internet Explorer 8", ela não é mais um objeto indefinido. Como o JSON é instanciado como um nome global pelo mecanismo de JavaScript, o verifica como "if (! this.JSON)" é avaliado como false e deve ser alterado no código do usuário.

As páginas da Web que usam [json2.js](https://github.com/douglascrockford/JSON-js/blob/master/json2.js) provavelmente não serão afetadas. Com poucas exceções, essas páginas devem funcionar mais rapidamente. As exceções são devido às diferenças entre a implementação do JSON nativo do Internet Explorer e o json2.js. Por exemplo, durante a serialização, a implementação JSON nativa detecta ciclos e não entra em recursão infinita como json.js. Para obter mais informações sobre essas exceções, consulte os [Blogs do JavaScript](/archive/blogs/jscript/).

Para obter mais informações, consulte [documentação](https://msdn.microsoft.com/library/cc836458(VS.85).aspx) e [controle de versão JSON e suporte de versão do mecanismo JavaScript](https://www.microsoft.com/windows/internet-explorer/readiness/developers-new.aspx).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Corrigindo problemas de compatibilidade em aplicativos Web usando o modo de exibição de compatibilidade](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 
