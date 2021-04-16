---
description: As propriedades privadas são usadas internamente pelo instalador e seus valores devem ser inseridos no banco de dados pelo autor do pacote de instalação ou definidos pelo instalador durante a instalação para os valores determinados pelo ambiente operacional.
ms.assetid: 7d574bf0-bcb3-4e19-9659-fe741ace9f21
title: Propriedades particulares
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab7b0196be016fecb625e139f308219582620d40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105750224"
---
# <a name="private-properties"></a>Propriedades particulares

As propriedades privadas são usadas internamente pelo instalador e seus valores devem ser inseridos no banco de dados pelo autor do pacote de instalação ou definidos pelo instalador durante a instalação para os valores determinados pelo ambiente operacional. A única maneira de um usuário poder interagir com propriedades privadas é por meio de [eventos de controle](control-events.md) na interface do usuário criada do pacote. Nomes de propriedade privada devem incluir letras minúsculas. Consulte [restrições em nomes de propriedade](restrictions-on-property-names.md).

As propriedades privadas normalmente descrevem o ambiente operacional. Por exemplo, se a instalação for executada em uma plataforma Windows, o instalador definirá a propriedade [**WindowsFolder**](windowsfolder.md) para o valor especificado na tabela de propriedades.

Os valores de propriedade privada não podem ser substituídos em uma linha de comando. Para limpar uma propriedade privada de uma instalação, deixe-a fora da [tabela de propriedades](property-table.md). No Windows XP e no Windows 2000, você não pode definir uma propriedade particular na fase de interface do usuário da instalação e, em seguida, passar o valor para a fase de execução.

Para obter uma lista de todas as propriedades particulares padrão usadas pelo instalador, consulte [referência de propriedade](property-reference.md). Você pode definir uma propriedade privada personalizada inserindo o nome da propriedade e o valor inicial na tabela de propriedades. Nomes de propriedade privada devem sempre incluir letras minúsculas.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Propriedades públicas](public-properties.md)
</dt> </dl>

 

 



