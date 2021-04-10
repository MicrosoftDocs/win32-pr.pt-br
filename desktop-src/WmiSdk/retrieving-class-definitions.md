---
description: As consultas de esquema são instruções WQL que solicitam definições de classe e informações sobre associações de esquema.
ms.assetid: cb65e99f-9046-4c63-ab56-60dedc45bcef
ms.tgt_platform: multiple
title: Recuperando definições de classe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d865b1a85eefa7e67b12ed4c0acc16ea9e19f9a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091302"
---
# <a name="retrieving-class-definitions"></a>Recuperando definições de classe

As consultas de esquema são instruções WQL que solicitam definições de classe e informações sobre [associações de esquema](schema-associations.md). Os provedores de classe usam consultas de esquema em suas instâncias da classe [**\_ \_ ClassProviderRegistration**](--classproviderregistration.md) para especificar as classes que dão suporte ao se registrarem com o WMI. As consultas de esquema são colocadas nas propriedades **ResultSetQueries**, **ReferencedSetQueries** e **UnsupportedQueries** da instância **\_ \_ ClassProviderRegistration** .

As consultas de esquema são semelhantes às consultas de dados, pois dão suporte às seguintes instruções WQL:

-   [SELECT](select-statement-for-schema-queries.md)
-   [ASSOCIADORES DE](schema-associations.md)
-   [REFERÊNCIAS DE](schema-associations.md)
-   [ISA](isa-operator-for-schema-queries.md)

Uma consulta de esquema é semelhante a uma [referência de consulta de](references-of-statement.md) dados que especifica a palavra-chave **ClassDefsOnly** ; em outras palavras, isso retorna um conjunto de resultados de objetos de definição de classe em vez de instâncias reais de classes de associação. No entanto, as referências de retornam definições de classe somente se houver instâncias presentes. Uma consulta de esquema retorna definições de classe se as instâncias estão presentes ou não.

 

 



