---
description: As propriedades públicas podem ser criadas no banco de dados de instalação da mesma forma que as propriedades privadas.
ms.assetid: 032aa55f-d97a-4455-bd32-571b0e05763b
title: Propriedades públicas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 822dfc55e0ab659e5580580edd04eb156540cb61
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828257"
---
# <a name="public-properties"></a>Propriedades públicas

As propriedades públicas podem ser criadas no banco de dados de instalação da mesma forma que [as propriedades privadas](private-properties.md). Além disso, os valores das propriedades públicas podem ser alterados por um usuário ou administrador do sistema definindo a propriedade na linha de comando, aplicando uma transformação ou interagindo com uma interface do usuário criada. Nomes de propriedade pública não podem conter letras minúsculas. Consulte [restrições em nomes de propriedade](restrictions-on-property-names.md).

Normalmente, as propriedades públicas são definidas pelos usuários durante a instalação. Por exemplo, a propriedade Public property [**INSTALLLEVEL**](installlevel.md) pode ser especificada na linha de comando usada para iniciar a instalação ou escolhida usando uma interface do usuário criada.

Os valores de propriedade pública podem ser substituídos em uma linha de comando, usando uma ação [padrão](standard-actions.md) ou [personalizada](custom-actions.md) , aplicando uma transformação ou fazendo com que o usuário interaja com uma interface do usuário criada. Para limpar uma propriedade pública na tabela de propriedades, deixe-a fora da tabela. As propriedades que devem ser definidas pela interface do usuário durante a instalação e, em seguida, passadas para a fase de execução da instalação do devem ser públicas.

Para obter uma lista das propriedades públicas padrão usadas pelo instalador, consulte [referência de propriedade](property-reference.md). Um autor também pode definir uma propriedade pública personalizada inserindo o nome da propriedade e um valor inicial na [tabela de propriedades](property-table.md). Todas as propriedades públicas podem ser substituídas por todos os usuários se qualquer uma das condições a seguir for verdadeira.

-   O usuário é um administrador do sistema.
-   A política de EnableUserControl por máquina é definida como 1. Consulte [política do sistema](system-policy.md).
-   A propriedade [**EnableUserControl**](-enableusercontrol.md) é definida como 1.
-   Essa é uma instalação não gerenciada que não está sendo feita com privilégios elevados.

Se nenhuma das condições acima for verdadeira, o instalador assume como padrão a limitação de quais propriedades públicas podem ser substituídas por um usuário que não seja um administrador do sistema. Consulte [**Propriedades públicas restritas**](restricted-public-properties.md).

 

 



