---
description: Os Tipos de Formato de Chave de dados configuráveis podem ser usados em campos de texto para fornecer uma chave em uma tabela de banco de dados.
ms.assetid: 9f3ce218-1243-4eba-9866-113200fefa30
title: Tipos de formato de chave
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a22c4149ec89bd9a1745c28fe17cdafcbcfeaee827dcb35bd8c6badbf2acfb7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119692486"
---
# <a name="key-format-types"></a>Tipos de formato de chave

Os Tipos de Formato de Chave de dados configuráveis podem ser usados em campos de texto para fornecer uma chave em uma tabela de banco de dados. O atributo msmConfigItemNonNullable é implícito nesse formato de dados e não precisa ser definido. Null nunca é um valor válido para esse tipo. As respostas a todos os itens de formato de chave devem estar [no formato especial do CMSM](cmsm-special-format.md).

Os seguintes tipos de Formato de Chave existem:

[Tipo de diretório](directory-type.md)

[Tipo de arquivo](file-type.md)

[Tipo de propriedade](property-type.md)

[Tipo de caixa de diálogo](dialog-type.md)

[Tipo binário](binary-type.md)

[Tipo de ícone](icon-type.md)

Itens configuráveis do Tipo de Formato de Chave são usados em colunas de texto para fornecer uma chave de banco de dados e, em geral, podem ser substituídos por qualquer cadeia de caracteres de texto. Os tipos individuais podem ter restrições sintáticas adicionais, mas essas restrições não são impostas por Mergemod.dll. Itens configuráveis específicos também podem ter restrições semânticas características. Por exemplo, um item configurável específico pode ser necessário para ser uma chave na tabela [Binária](binary-table.md) para uma linha que contém uma imagem de bitmap. Essas restrições não são impostas pelo Mergemod.dll e, portanto, os autores do módulo devem estar preparados para lidar com qualquer cadeia de caracteres que atenda ao tipo de Formato de Chave especificado. A menos que especificado de outra forma por atributos ou significado semântico, null é uma resposta válida.

 

 



