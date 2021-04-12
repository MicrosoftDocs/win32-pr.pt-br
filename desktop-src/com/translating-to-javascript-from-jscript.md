---
title: Convertendo para JavaScript do JScript
description: Convertendo para JavaScript do JScript
ms.assetid: 11d31c8c-868d-4220-9298-6d24a209dc47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71b18972f407cf008626245798b3f7740d98058e
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/20/2020
ms.locfileid: "104365667"
---
# <a name="translating-to-javascript-from-jscript"></a>Convertendo para JavaScript do JScript

O JScript é amplamente compatível com o JavaScript. No entanto, o JScript inclui alguns objetos que não têm suporte no momento pelo JavaScript, como o ActiveXobject, o enumerador, o erro, o global e o VBArray.

A versão 5,0 do JScript dá suporte ao tratamento de exceções por meio de **try**... instruções **Catch** . Atualmente, o JavaScript não fornece um mecanismo de entrega de erros.

Ao trabalhar com JScript ou JavaScript, há algumas diferenças sutis entre as implementações do modelo de objeto com suporte em vários navegadores da Web. Para gravar o script que é executado no Internet Explorer e no Netscape Navigator, limite os recursos usados pelos seus scripts aos especificados no padrão de World Wide Web Consortium (W3C) [para HTML versão 3,2](https://www.w3.org/tr/rec-html32.html).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Convertendo para JavaScript](translating-to-javascript.md)
</dt> </dl>

 

 




