---
title: convertendo para JScript do JavaScript
description: convertendo para JScript do JavaScript
ms.assetid: 86067a69-a6a1-474f-b8d8-85caf384a311
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51c25276d569c5b461693a666d1bf8cf706b6896c0995972e1d2af0071c5760b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129558"
---
# <a name="translating-to-jscript-from-javascript"></a>convertendo para JScript do JavaScript

o JScript é amplamente compatível com o JavaScript. no entanto, JScript versão 5,0 inclui alguns objetos que não têm suporte no momento pelo JavaScript, como activexobject, enumerador, erro, Global e VBArray.

o JScript 5,0 dá suporte à manipulação de exceção por meio de **try**... instruções **Catch** . Atualmente, o JavaScript não fornece um mecanismo de entrega de erros.

ao trabalhar com o JScript ou o JavaScript, há algumas diferenças sutis entre as implementações do modelo de objeto com suporte em vários navegadores da Web. Para gravar o script que é executado no Internet Explorer e no Netscape Navigator, limite os recursos usados pelos seus scripts aos especificados no padrão de World Wide Web Consortium (W3C) para HTML versão 3,2. Para obter mais informações sobre esse padrão, consulte [especificação de referência de HTML 3,2](https://www.w3.org/TR/REC-html32.html).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Convertendo para JScript](translating-to-jscript.md)
</dt> </dl>

 

 




