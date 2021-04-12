---
description: O banco de dados de um módulo de mesclagem contém todas as propriedades de instalação e a lógica de instalação para o módulo.
ms.assetid: 72e42392-54e6-4be8-9a43-04158552be3d
title: Mesclar banco de dados do módulo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74158e38d10b302c28520f6c1736e9cc6d823641
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297080"
---
# <a name="merge-module-database"></a>Mesclar banco de dados do módulo

O banco de dados de um módulo de mesclagem contém todas as propriedades de instalação e a lógica de instalação para o módulo. Ele é essencialmente um [banco de dados do instalador](installer-database.md) simplificado ou arquivo. msi. Os arquivos de banco de dados do módulo de mesclagem padrão são indicados por uma extensão. msm. Para obter uma lista de todas as tabelas de banco de dados que podem existir em módulos de mesclagem, consulte [mesclar tabelas de banco de dados](merge-module-database-tables.md). As tabelas a seguir são necessárias no banco de dados de cada arquivo. msm:

[Componente](component-table.md)

[Diretório](directory-table.md)

[FeatureComponents](featurecomponents-table.md)

[Arquivo](file-table.md)

[ModuleSignature](modulesignature-table.md)

[ModuleComponents](modulecomponents-table.md)

Observe que o componente, o diretório, o FeatureComponents e as tabelas de arquivos também estão presentes em todos os arquivos. msi. Um banco de dados de módulo de mesclagem não contém uma [tabela de recursos](feature-table.md) e, portanto, o arquivo. msm não pode ser instalado sozinha. Para instalar um módulo de mesclagem, ele deve primeiro ser mesclado usando uma ferramenta de mesclagem em um arquivo. msi.

A [tabela ModuleSignature](modulesignature-table.md) está presente apenas em arquivos. msi que foram mesclados com pelo menos um arquivo. msm. Se essa tabela estiver presente em um arquivo. msi, ela conterá um registro para cada módulo de mesclagem que foi mesclado anteriormente no banco de dados de instalação.

Os módulos de mesclagem podem conter tabelas de sequência MergeModule opcionais. Essas tabelas ocorrem somente em arquivos. msm. Quando os arquivos. msm são mesclados em um arquivo. msi, essas tabelas modificam as [*tabelas de sequência*](s-gly.md) de ação do arquivo. msi.

Os módulos de mesclagem podem conter tabelas personalizadas. Essas tabelas são usadas por [ações personalizadas](custom-actions.md) definidas no módulo de mesclagem.

Os módulos de mesclagem raramente exigem tabelas de interface do usuário. Essas tabelas precisam estar presentes apenas em casos raros em que o módulo de mesclagem requer entrada do usuário durante a instalação. Para obter mais informações, consulte [Criando interfaces do usuário em módulos de mesclagem](authoring-user-interfaces-in-merge-modules.md).

 

 



