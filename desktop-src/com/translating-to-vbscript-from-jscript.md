---
title: Convertendo para VBScript do JScript
description: Convertendo para VBScript do JScript
ms.assetid: db1115e1-2abd-4b06-ad8d-c1f917cd3087
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 704f5ac608e94f883edc3b319fd04625e9a08d18
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005208"
---
# <a name="translating-to-vbscript-from-jscript"></a>Convertendo para VBScript do JScript

No VBScript, a **para**... **Cada** loop enumera os membros de uma coleção; no JScript, a **para**... o loop **in** enumera os membros de um objeto ou matriz JScript. Para enumerar uma coleção em JScript, use um objeto de enumerador.

O JScript fornece o objeto Error, que pode ser usado para interceptar e manipular erros. O objeto de erro é análogo ao objeto VBScript Err.

No JScript, há vários tipos de dados, como números, cadeias de caracteres, Boolianos, objetos e o atributo nulo. O VBScript usa apenas um tipo de dados, **Variant**, que pode ser subtipoado para representar cadeias de caracteres, números, Boolianos e assim por diante.

No JScript, as matrizes podem ser expandidas dinamicamente definindo um novo valor para a propriedade Length da matriz. No VBScript, as matrizes não podem ser ampliadas; Eles devem ser redimensionados usando a instrução **ReDim** .

As funções de suporte a VBScript e JScript. O VBScript, no entanto, também oferece suporte a sub-rotinas. As sub-rotinas são semelhantes às funções, mas não retornam um valor.

O JScript diferencia maiúsculas de minúsculas. O VBScript não é.

O JScript é compatível com uma ampla variedade de navegadores da Web, incluindo o Internet Explorer e o Netscape Navigator. O Netscape Navigator não oferece suporte a VBScript.

As matrizes JScript não são matrizes do tipo de variável **Variant SafeArray**. Um script JScript deve usar um objeto VBArray para acessar a variável **Variant SafeArray**. Os scripts VBScript podem acessar as variáveis **Variant SafeArray** diretamente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Convertendo para VBScript](translating-to-vbscript.md)
</dt> </dl>

 

 




