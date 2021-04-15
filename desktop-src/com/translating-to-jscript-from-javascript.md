---
title: Convertendo para JScript do JavaScript
description: Convertendo para JScript do JavaScript
ms.assetid: 86067a69-a6a1-474f-b8d8-85caf384a311
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45535807a5ef2baf59c2e068007a5a8df8bf4863
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/20/2020
ms.locfileid: "104498995"
---
# <a name="translating-to-jscript-from-javascript"></a>Convertendo para JScript do JavaScript

O JScript é amplamente compatível com o JavaScript. No entanto, a versão 5,0 do JScript inclui alguns objetos que não têm suporte no momento pelo JavaScript, como ActiveXobject, enumerador, erro, global e VBArray.

O JScript 5,0 dá suporte à manipulação de exceção por meio de **try**... instruções **Catch** . Atualmente, o JavaScript não fornece um mecanismo de entrega de erros.

Ao trabalhar com JScript ou JavaScript, há algumas diferenças sutis entre as implementações do modelo de objeto com suporte em vários navegadores da Web. Para gravar o script que é executado no Internet Explorer e no Netscape Navigator, limite os recursos usados pelos seus scripts aos especificados no padrão de World Wide Web Consortium (W3C) para HTML versão 3,2. Para obter mais informações sobre esse padrão, consulte [especificação de referência de HTML 3,2](https://www.w3.org/TR/REC-html32.html).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Traduzindo para o JScript](translating-to-jscript.md)
</dt> </dl>

 

 




