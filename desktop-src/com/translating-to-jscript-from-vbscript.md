---
title: Convertendo para JScript do VBScript
description: Convertendo para JScript do VBScript
ms.assetid: cdf04a01-8bc3-4f37-872b-3a0aae962f26
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a18c2ccb11ffa4f5f000d8cfc73f7db6f857cf6b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635079"
---
# <a name="translating-to-jscript-from-vbscript"></a>Convertendo para JScript do VBScript

No VBScript, a **para**... **Cada** loop enumera os membros de uma coleção; no JScript, a **para**... o loop **in** enumera os membros de um objeto ou matriz JScript. Para enumerar uma coleção em JScript, use um objeto de enumerador.

No JScript, há vários tipos de dados, como números, cadeias de caracteres, Boolianos, objetos e o atributo nulo. O VBScript usa apenas um tipo de dados, **Variant**, que pode ser subtipoado para representar cadeias de caracteres, números, Boolianos e assim por diante.

No JScript, as matrizes podem ser expandidas dinamicamente definindo um novo valor para a propriedade Length da matriz. No VBScript, as matrizes não podem ser ampliadas; Eles devem ser redimensionados usando a instrução **ReDim** .

As funções de suporte a VBScript e JScript. O VBScript, no entanto, também oferece suporte a sub-rotinas. As sub-rotinas são semelhantes às funções, mas não retornam um valor.

O JScript diferencia maiúsculas de minúsculas. O VBScript não é.

O JScript é compatível com o Internet Explorer e com o Netscape Navigator. O Netscape Navigator não oferece suporte a VBScript.

O JScript fornece o objeto Error, que pode ser usado para interceptar e manipular erros. O objeto de erro é análogo ao objeto VBScript Err.

As matrizes JScript não são matrizes do tipo de variável **Variant SafeArray**. Se o script receber uma variável **Variant SafeArray** de um objeto com ou script VBScript, ele deverá usar um objeto VBArray para acessar a variável **Variant SafeArray** .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Traduzindo para o JScript](translating-to-jscript.md)
</dt> </dl>

 

 




