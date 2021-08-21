---
description: JSON (JavaScript Object Notation)
ms.assetid: 2F6FDE88-C852-46BC-B6B1-630C266AF0AA
title: JSON (JavaScript Object Notation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 970737e7f19c5043c418941351ea82537b36a4a2429c44428a90031699458525
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053074"
---
# <a name="javascript-object-notation-json"></a>JSON (JavaScript Object Notation)

[JavaScript Object Notation (JSON)](https://www.json.org/) é um formato simples e leve de intercâmbio de dados baseado em um subconjunto da notação literal de objeto da linguagem JavaScript. O mecanismo JavaScript no Windows Internet Explorer 8 implementa a proposta [JSON ECMAScript 3.1](https://www.ecma-international.org/) para funções nativas de manipulação de JSON (que usa a API de json2.js de [Charles Crockford).](https://github.com/douglascrockford/JSON-js/blob/master/json2.js)

Internet Explorer 8 inclui um objeto JSON nativo que está em conformidade com o suporte JSON descrito no Rascunho de Trabalho da Proposta [do ES3.1.](https://www.ecma-international.org/) Algumas páginas da Web detectam o objeto JSON nativo e o usam de maneira não padrão. Esse uso normalmente causa um erro de script e interrompe o tratamento de solicitações AJAX. O exemplo de código a seguir mostra a maneira errada de usar o objeto JSON.


```JScript
    if(!window.JSON) JSON = myJSON; 
    JSON.encode(obj); // Not part of the standard
```



Em vez disso, o exemplo de código a seguir mostra uma boa maneira de usar o objeto JSON.


```JScript
    JSON = myJSON; 
    JSON.encode(obj);
```



Windows Internet Explorer inclui suporte nativo para JSON introduzindo um objeto JSON global que tem dois métodos integrados: **stringify** **e parse**. O objeto JSON global é definido no mecanismo JavaScript e é criado durante a fase de inicialização do mecanismo. Para manter a compatibilidade com versões regressivas, esse recurso está disponível somente quando um site usa a versão mais recente dos recursos javaScript usando o modo de layout "Internet Explorer 8 Padrões" (documento). Esse recurso também pode afetar o comportamento de páginas da Web que dependem de uma variável global JSON ou usar [json2.js](https://github.com/douglascrockford/JSON-js/blob/master/json2.js).

Você pode substituir o objeto JSON global. Mas quando uma página da Web usa o modo de layout "Internet Explorer 8 Padrões" (documento), ele não é mais um objeto indefinido. Como o JSON é instautado como um nome global pelo mecanismo JavaScript, verificações como "if(!this.JSON)" são avaliadas como False e devem ser alteradas no código do usuário.

Páginas da Web que [ usam ](https://github.com/douglascrockford/JSON-js/blob/master/json2.js)json2.jsprovavelmente não serão afetadas. Com poucas exceções, essas páginas devem funcionar mais rapidamente. As exceções são devido às diferenças entre a implementação Internet Explorer JSON nativa e json2.js. Por exemplo, durante a serialização, a implementação JSON nativa detecta ciclos e não vai em recursão infinita, como json.js. Para obter mais informações sobre essas exceções, consulte [Os Blogs do JavaScript.](/archive/blogs/jscript/)

Para obter mais informações, consulte [Documentação e](https://msdn.microsoft.com/library/cc836458(VS.85).aspx) versão JSON e Suporte de versão do Mecanismo [JavaScript.](https://www.microsoft.com/windows/internet-explorer/readiness/developers-new.aspx)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Corrigindo problemas de compatibilidade em aplicativos Web usando Modo de Exibição de Compatibilidade](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 
