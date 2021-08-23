---
description: Os tipos de formato de texto de dados configuráveis podem ser cadeias de caracteres de texto de qualquer comprimento. Nulos inseridos não são permitidos.
ms.assetid: 71b89f87-43ba-41cd-a969-765d45da4ba4
title: Tipos de formato de texto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a77ef5e6948320deba8df992e2cf9447cbda82d6a20fc4329f97e761f425164
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119626326"
---
# <a name="text-format-types"></a>Tipos de formato de texto

Os tipos de formato de texto de dados configuráveis podem ser cadeias de caracteres de texto de qualquer comprimento. Nulos inseridos não são permitidos.

Existem os seguintes tipos de formato de texto:

[Texto arbitrário](arbitrary-text-type.md)

[RTF](rtf-type.md)

[Binário](formatted-type.md)

[Enumeração](enum-type.md)

[Tipo de identificador](identifier-type.md)

Os itens configuráveis do tipo de formato de texto são usados em campos de banco de dados não binários e, em geral, podem ser substituídos por qualquer cadeia de caracteres de qualquer comprimento. No entanto, determinados itens configuráveis também têm restrições semânticas. Por exemplo, um item configurável que é necessário para ser uma chave estrangeira em uma tabela específica tem restrições semânticas adicionais. Essas restrições semânticas não são impostas por Mergemod.dll e, portanto, os autores de módulo devem estar preparados para lidar com qualquer cadeia de caracteres que satisfaça o tipo de formato de texto especificado.

 

 



