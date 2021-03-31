---
title: Considerações sobre o conjunto de propriedades
description: É altamente recomendável que os conjuntos de propriedades sejam mantidos pequenos porque o fluxo do conjunto de propriedades é lido na memória antes que uma única propriedade possa ser lida ou gravada.
ms.assetid: 520db05e-81cd-40ef-af89-471d7194c634
keywords:
- Considerações sobre o conjunto de propriedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ddfd89140092b13d113122ffe1c1a2b576e654c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103637255"
---
# <a name="property-set-considerations"></a>Considerações sobre o conjunto de propriedades

É altamente recomendável que os conjuntos de propriedades sejam mantidos pequenos porque o fluxo do conjunto de propriedades é lido na memória antes que uma única propriedade possa ser lida ou gravada. "pequeno" significa menos de 32 kilobytes de dados. Isso raramente apresenta um problema porque, normalmente, as propriedades "embutidas" serão itens pequenos, como cadeias de caracteres descritivas, palavras-chave, carimbos de data/hora, contagens, nomes de autor, identificadores globais exclusivos (GUIDs), identificadores de classe (CLSIDs) e assim por diante.

Para armazenar maiores partes de dados, ou em casos em que o tamanho total de um conjunto de propriedades relacionadas excede a quantidade recomendada, o uso de tipos não simples, como o **\_ armazenamento** VT e o **\_ streaming** do UT, é altamente recomendável. Eles não são armazenados no fluxo do conjunto de propriedades, portanto, eles não afetam significativamente a sobrecarga inicial do primeiro acesso e gravação de uma propriedade. Há uma sobrecarga mínima, pois o fluxo do conjunto de propriedades contém o nome do fluxo irmão ou da propriedade com valor de armazenamento e isso requer um pequeno período de tempo adicional para ser processado.

Para obter mais informações, consulte:

-   [Considerações sobre implementação do IPropertySetStorage](ipropertysetstorage-implementation-considerations.md)
-   [Armazenando conjuntos de propriedades](storing-property-sets.md)
-   [Características de desempenho](performance-characteristics.md)
-   [Implementando o conjunto de propriedades de informações de resumo](implementing-the-summary-information-property-set.md)

 

 




