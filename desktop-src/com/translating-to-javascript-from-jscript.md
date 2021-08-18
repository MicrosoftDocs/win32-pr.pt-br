---
title: Traduzindo para JavaScript de JScript
description: Traduzindo para JavaScript de JScript
ms.assetid: 11d31c8c-868d-4220-9298-6d24a209dc47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49c4adb5827952cc9bab0dac268997b5b73a52ecd1403e5431cdb3939b08c7e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129578"
---
# <a name="translating-to-javascript-from-jscript"></a>Traduzindo para JavaScript de JScript

JScript é amplamente compatível com JavaScript. No entanto, JScript inclui alguns objetos que atualmente não são suportados pelo JavaScript, como ActiveXObject, Enumerator, Error, Global e VBArray.

JScript versão 5.0 dá suporte ao tratamento de exceções por **meio de try**... **Instruções catch.** Atualmente, o JavaScript não fornece um mecanismo de entrega de erros.

Ao trabalhar com JScript ou JavaScript, há algumas diferenças sutis entre as implementações de modelo de objeto com suporte de vários navegadores da Web. Para escrever scripts executados no Internet Explorer e no Netscape Navigator, limite os recursos usados por seus scripts aos especificados no padrão World Wide Web Consortium (W3C) para HTML versão [3.2.](https://www.w3.org/tr/rec-html32.html)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Traduzindo para JavaScript](translating-to-javascript.md)
</dt> </dl>

 

 




