---
description: As propriedades públicas podem ser autoradas no banco de dados de instalação da mesma maneira que as propriedades privadas.
ms.assetid: 032aa55f-d97a-4455-bd32-571b0e05763b
title: Propriedades públicas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0138db2fcbe664ac9a4064379486c42c3d52a6896fc53a608b99192a8d70c75
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119828426"
---
# <a name="public-properties"></a>Propriedades públicas

As propriedades públicas podem ser autoradas no banco de dados de instalação da mesma maneira que [as propriedades privadas](private-properties.md). Além disso, os valores das propriedades públicas podem ser alterados por um usuário ou administrador do sistema definindo a propriedade na linha de comando, aplicando uma transformação ou interagindo com uma interface do usuário autoral. Os nomes de propriedade pública não podem conter letras minúsculas. Consulte [Restrições em nomes de propriedade](restrictions-on-property-names.md).

As propriedades públicas normalmente são definidas pelos usuários durante a instalação. Por exemplo, a propriedade [**pública INSTALLLEVEL**](installlevel.md) pode ser especificada na linha de comando usada para iniciar a instalação ou escolhida usando uma interface do usuário autorada.

Os valores de propriedade pública podem ser substituídos [](standard-actions.md) em [](custom-actions.md) uma linha de comando, usando uma ação padrão ou personalizada, aplicando uma transformação ou fazendo com que o usuário interaja com uma interface do usuário autorada. Para limpar uma propriedade pública na tabela de propriedades, deixe-a fora da tabela. As propriedades que devem ser definidas pela interface do usuário durante a instalação e passadas para a fase de execução da instalação devem ser públicas.

Para ver uma lista das propriedades públicas padrão usadas pelo instalador, consulte [Referência de propriedade](property-reference.md). Um autor também pode definir uma propriedade pública personalizada inserindo o nome da propriedade e um valor inicial na [tabela Propriedade](property-table.md). Todas as propriedades públicas poderão ser substituídos por todos os usuários se qualquer uma das condições a seguir for verdadeira.

-   O usuário é um administrador do sistema.
-   A política EnableUserControl por computador é definida como 1. Consulte [Política do Sistema](system-policy.md).
-   A [**propriedade EnableUserControl**](-enableusercontrol.md) é definida como 1.
-   Essa é uma instalação nãomanageda que não está sendo feita com privilégios elevados.

Se nenhuma das condições acima for verdadeira, o instalador assume como padrão limitar quais propriedades públicas podem ser substituídos por um usuário que não é um administrador do sistema. Consulte [**Propriedades públicas restritas.**](restricted-public-properties.md)

 

 



