---
description: Os tipos de formato de texto de dados configuráveis podem ser cadeias de caracteres de texto de qualquer comprimento. Nulos inseridos não são permitidos.
ms.assetid: 71b89f87-43ba-41cd-a969-765d45da4ba4
title: Tipos de formato de texto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4a8f05a0804569667a74c52392d322f3fed2818
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105748566"
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

 

 



