---
description: Os tipos de formato de chave de dados configuráveis podem ser usados em campos de texto para fornecer uma chave para uma tabela de banco de dado.
ms.assetid: 9f3ce218-1243-4eba-9866-113200fefa30
title: Tipos de formato de chave
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96687299a57ddebbb90b422ad5311c4bed1db332
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105770194"
---
# <a name="key-format-types"></a>Tipos de formato de chave

Os tipos de formato de chave de dados configuráveis podem ser usados em campos de texto para fornecer uma chave para uma tabela de banco de dado. O atributo msmConfigItemNonNullable é implícito nesse formato de dados e não precisa ser definido. NULL nunca é um valor válido para este tipo. As respostas a todos os itens de formato de chave devem estar no [formato especial CMSM](cmsm-special-format.md).

Existem os seguintes tipos de formato de chave:

[Tipo de diretório](directory-type.md)

[Tipo de arquivo](file-type.md)

[Tipo de propriedade](property-type.md)

[Tipo de caixa de diálogo](dialog-type.md)

[Tipo de binário](binary-type.md)

[Tipo de ícone](icon-type.md)

Os itens configuráveis do tipo de formato de chave são usados em colunas de texto para fornecer uma chave de banco de dados e, em geral, podem ser substituídos por qualquer cadeia de texto. Os tipos individuais podem ter restrições sintáticas adicionais, mas essas restrições não são impostas pelo Mergemod.dll. Determinados itens configuráveis também podem ter restrições semânticas de características. Por exemplo, um determinado item configurável pode precisar ser uma chave na [tabela binária](binary-table.md) para uma linha que contém uma imagem de bitmap. Essas restrições não são impostas por Mergemod.dll e, portanto, os autores de módulo devem estar preparados para lidar com qualquer cadeia de caracteres que satisfaça o tipo de formato de chave especificado. A menos que especificado de outra forma por significado semântico ou atributos, NULL é uma resposta válida.

 

 



