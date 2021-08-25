---
title: Traduzindo para VBScript de JScript
description: Traduzindo para VBScript de JScript
ms.assetid: db1115e1-2abd-4b06-ad8d-c1f917cd3087
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3900ba82b258e6ee19cf06edb2f97247033778da5fcabaffe4a854e66a5fef73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992246"
---
# <a name="translating-to-vbscript-from-jscript"></a>Traduzindo para VBScript de JScript

No VBScript, o **para**... **Cada** loop enumera os membros de uma coleção; em JScript, o **para**... **in** loop enumera os membros de um objeto JScript ou matriz. Para enumerar uma coleção em JScript, use um objeto Enumerator.

JScript fornece o objeto Error, que pode ser usado para interceptar e tratar erros. O objeto Error é análogo ao objeto Err do VBScript.

No JScript, há vários tipos de dados, como números, cadeias de caracteres, boolianas, objetos e o atributo nulo. O VBScript usa apenas um tipo de dados, **Variant**, que pode ser subtipo para representar cadeias de caracteres, números, boolianas e assim por diante.

No JScript, as matrizes podem ser expandidas dinamicamente definindo um novo valor para a propriedade de comprimento da matriz. No VBScript, as matrizes não podem ser ampliadas; eles devem ser redimensionados usando a **instrução redim.**

O VBScript e JScript funções de suporte. No entanto, o VBScript também dá suporte a sub-rotinas. As sub-rotinas são semelhantes às funções, mas não retornam um valor.

JScript é sensível a minúsculas. O VBScript não é.

JScript há suporte para uma ampla variedade de navegadores da Web, incluindo o Internet Explorer e o Netscape Navigator. O Netscape Navigator não dá suporte ao VBScript.

JScript matrizes não são matrizes do tipo de variável **VARIANT SAFEARRAY**. Um JScript script deve usar um objeto VBArray para acessar a **variável VARIANT SAFEARRAY.** Scripts VBScript podem acessar **variáveis VARIANT SAFEARRAY** diretamente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Traduzindo para VBScript](translating-to-vbscript.md)
</dt> </dl>

 

 




