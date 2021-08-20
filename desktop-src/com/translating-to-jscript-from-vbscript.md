---
title: convertendo para JScript do VBScript
description: convertendo para JScript do VBScript
ms.assetid: cdf04a01-8bc3-4f37-872b-3a0aae962f26
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20d1b07387ce36f574131cce9ca1afda262fd2bc40fdc90359c2ec3b18b60f0b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117917813"
---
# <a name="translating-to-jscript-from-vbscript"></a>convertendo para JScript do VBScript

No VBScript, a **para**... **Cada** loop enumera os membros de uma coleção; no JScript, a **para**... o loop **in** enumera os membros de um JScript objeto ou matriz. para enumerar uma coleção em JScript, use um objeto de enumerador.

em JScript, há vários tipos de dados, como números, cadeias de caracteres, boolianos, objetos e o atributo nulo. O VBScript usa apenas um tipo de dados, **Variant**, que pode ser subtipoado para representar cadeias de caracteres, números, Boolianos e assim por diante.

no JScript, as matrizes podem ser expandidas dinamicamente definindo um novo valor para a propriedade length da matriz. No VBScript, as matrizes não podem ser ampliadas; Eles devem ser redimensionados usando a instrução **ReDim** .

as funções de suporte a VBScript e JScript. O VBScript, no entanto, também oferece suporte a sub-rotinas. As sub-rotinas são semelhantes às funções, mas não retornam um valor.

JScript diferencia maiúsculas de minúsculas. O VBScript não é.

o JScript é compatível com o Internet Explorer e com o Netscape Navigator. O Netscape Navigator não oferece suporte a VBScript.

JScript fornece o objeto Error, que pode ser usado para interceptar e manipular erros. O objeto de erro é análogo ao objeto VBScript Err.

as matrizes de JScript não são matrizes da variante de tipo de variável **SAFEARRAY**. Se o script receber uma variável **Variant SafeArray** de um objeto com ou script VBScript, ele deverá usar um objeto VBArray para acessar a variável **Variant SafeArray** .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Convertendo para JScript](translating-to-jscript.md)
</dt> </dl>

 

 




