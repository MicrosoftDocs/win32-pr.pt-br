---
description: Um aplicativo combina duas regiões chamando a função CombineRgn.
ms.assetid: d16f9ca5-33e2-4752-900e-743245838377
title: Combinando regiões
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d6550f260a70bc0f49e6b181f9e1c82a64ce4eadbe643214362444d0dcbfccd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117887516"
---
# <a name="combining-regions"></a>Combinando regiões

Um aplicativo combina duas regiões chamando a função [**CombineRgn**](/windows/desktop/api/Wingdi/nf-wingdi-combinergn) . Usando essa função, um aplicativo pode combinar partes de interseção de duas regiões, tudo exceto as partes interseccionadas de duas regiões, as duas regiões originais em sua totalidade e assim por diante. A seguir estão cinco valores que definem as combinações de regiões.



| Valor     | Significado                                                                               |
|-----------|---------------------------------------------------------------------------------------|
| RGN \_ e  | As partes de interseção de duas regiões originais definem uma nova região.                   |
| \_cópia RGN | Uma cópia da primeira (das duas regiões originais) define uma nova região.               |
| RGN \_ diff | A parte da primeira região que não faz interseção com a segunda define uma nova região. |
| RGN \_ ou   | As duas regiões originais definem uma nova região.                                         |
| \_XOR RGN  | Essas partes das duas regiões originais que não se sobrepõem definem uma nova região.      |



 

A ilustração a seguir mostra as cinco combinações possíveis de um quadrado e uma região circular resultante de uma chamada para [**CombineRgn**](/windows/desktop/api/Wingdi/nf-wingdi-combinergn).

![ilustração que demonstra os resultados descritos na tabela anterior](images/csrgn-02.png)

 

 



