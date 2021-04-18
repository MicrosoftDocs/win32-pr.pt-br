---
title: Convertendo para VBScript do JavaScript
description: Convertendo para VBScript do JavaScript
ms.assetid: f302e032-4e94-42f1-839b-022dab538760
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2eda8169a665dc93133f7ac933de12ecc612f3e4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105815555"
---
# <a name="translating-to-vbscript-from-javascript"></a>Convertendo para VBScript do JavaScript

No JavaScript, há vários tipos de dados, como números, cadeias de caracteres, Boolianos, objetos e o atributo nulo. O VBScript usa apenas um tipo de dados, **Variant**, que pode ser subtipoado para representar cadeias de caracteres, números, Boolianos e assim por diante.

No JavaScript, as matrizes podem ser expandidas dinamicamente definindo um novo valor para a propriedade Length da matriz. No VBScript, as matrizes não podem ser ampliadas; Eles devem ser redimensionados usando a instrução **ReDim** .

As funções de suporte do VBScript e do JavaScript. O VBScript, no entanto, também oferece suporte a sub-rotinas. As sub-rotinas são semelhantes às funções, exceto que não retornam um valor.

JavaScript diferencia maiúsculas de minúsculas. O VBScript não é.

O JavaScript é compatível com uma ampla variedade de navegadores da Web, incluindo o Internet Explorer e o Netscape Navigator. O Netscape Navigator não oferece suporte a VBScript.

O VBScript dá suporte ao tratamento de erros por meio de seu objeto Err. Atualmente, o JavaScript não fornece um meio de interceptação e manipulação de erros.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Convertendo para VBScript](translating-to-vbscript.md)
</dt> </dl>

 

 




