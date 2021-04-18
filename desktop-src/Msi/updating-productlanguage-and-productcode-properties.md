---
description: A propriedade ProductLanguage deve ser atualizada para o identificador de idioma numérico (LANGid) para o novo idioma.
ms.assetid: e00ef69b-c54b-41de-9230-a7582b260891
title: Atualizando Propriedades ProductLanguage e ProductCode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37a7537cdb0295075fbfd1b8b58e45a051610cf6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105758756"
---
# <a name="updating-productlanguage-and-productcode-properties"></a>Atualizando Propriedades ProductLanguage e ProductCode

A propriedade [**ProductLanguage**](productlanguage.md) deve ser atualizada para o identificador de idioma numérico (LangID) para o novo idioma. No caso do exemplo de localização, o valor da propriedade **ProductLanguage** deve ser alterado do LangID para inglês (1033) para o LANGID para francês (1036) na tabela de [Propriedades](property-table.md).

O valor da propriedade [**ProductCode**](productcode.md) na tabela de [Propriedades](property-table.md) deve ser alterado para um valor novo e exclusivo ao localizar um banco de dados, pois um produto localizado é considerado um produto diferente. Por exemplo, as versões em alemão e em inglês de um aplicativo são consideradas dois produtos diferentes e devem ter códigos de produto diferentes. Consulte [códigos de produto](product-codes.md).

Use o editor de tabela de banco de dados para atualizar os valores das propriedades ProductCode e ProductLanguage na tabela de propriedades. Não reutilize o GUID mostrado se você copiar este exemplo.

[Tabela de propriedades](property-table.md)



| Propriedade                                   | Valor                                  |
|--------------------------------------------|----------------------------------------|
| [**ProductCode**](productcode.md)         | {EE389960-E426-4EEA-B669-AD8129249881} |
| [**ProductLanguage**](productlanguage.md) | 1036                                   |



 

[Continuar](updating-a-summary-information-stream.md)

 

 



