---
description: O banco de dados de um módulo de mesclagem contém todas as propriedades de instalação e a lógica de instalação do módulo.
ms.assetid: 72e42392-54e6-4be8-9a43-04158552be3d
title: Mesclar banco de dados de módulo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fb75614218e7464879f62ea1527245e36d65d1dc14f19a9b82a13a893997f1c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117804598"
---
# <a name="merge-module-database"></a>Mesclar banco de dados de módulo

O banco de dados de um módulo de mesclagem contém todas as propriedades de instalação e a lógica de instalação do módulo. Ele é essencialmente um banco de dados [instalador simplificado](installer-database.md) ou .msi arquivo. Os arquivos de banco de dados do módulo de mesclagem padrão são indicados por uma extensão .msm. Para ver uma lista de todas as tabelas de banco de dados que podem existir em módulos de mesclagem, consulte [Mesclar tabelas de](merge-module-database-tables.md)banco de dados do módulo . As tabelas a seguir são necessárias no banco de dados de cada arquivo .msm:

[Componente](component-table.md)

[Diretório](directory-table.md)

[FeatureComponents](featurecomponents-table.md)

[Arquivo](file-table.md)

[Modulesignature](modulesignature-table.md)

[ModuleComponents](modulecomponents-table.md)

Observe que as tabelas Componente, Diretório, FeatureComponents e Arquivo também estão presentes em todos os .msi arquivos. Um banco de dados de módulo de mesclagem não contém uma [Tabela de](feature-table.md) recursos e, portanto, o arquivo .msm não pode ser instalado sozinho. Para instalar um módulo de mesclagem, ele deve primeiro ser mesclado usando uma ferramenta de mesclagem em um .msi arquivo.

A [Tabela ModuleSignature](modulesignature-table.md) só está presente .msi arquivos que foram mesclados com pelo menos um arquivo .msm. Se essa tabela estiver presente em um arquivo .msi, ela conterá um registro para cada módulo de mesclagem que foi mesclado anteriormente no banco de dados de instalação.

Os módulos de mesclagem podem conter tabelas mergeModule sequence opcionais. Essas tabelas ocorrem somente em arquivos .msm. Quando os arquivos .msm são mesclados em um arquivo .msi, essas tabelas modificam as tabelas de sequência de ação do .msi arquivo. [](s-gly.md)

Os módulos de mesclagem podem conter tabelas personalizadas. Essas tabelas são usadas [por ações personalizadas](custom-actions.md) definidas no módulo de mesclagem.

Módulos de mesclagem raramente exigem tabelas de interface do usuário. Essas tabelas precisam estar presentes apenas em casos raros em que o módulo de mesclagem exige a entrada do usuário durante a instalação. Para obter mais informações, consulte [Authoring User Interfaces in Merge Modules](authoring-user-interfaces-in-merge-modules.md).

 

 



