---
description: Para criar módulos de mesclagem, use as diretrizes gerais descritas no tópico módulos de mesclagem de criação.
ms.assetid: 9d5e60dc-9133-4c6e-9a47-dd341f2757fa
title: Criando um módulo de mesclagem que pode ser configurado pelo End-User
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2db6ff7bd85fb1b6704fc2452c488b8a3bbc06b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170247"
---
# <a name="creating-a-merge-module-that-can-be-configured-by-the-end-user"></a>Criando um módulo de mesclagem que pode ser configurado pelo End-User

Para criar módulos de mesclagem, use as diretrizes gerais descritas no tópico [módulos de mesclagem de criação](authoring-merge-modules.md) . Além disso, você deve fazer o seguinte para criar um módulo de mesclagem que pode ser configurado pelo usuário final do módulo:

-   Os usuários finais precisam ter Mergemod.dll versão 2,0 para configurar o módulo. Os usuários com versões anteriores do Mergemod.dll podem aplicar o módulo, mas sempre obtêm as configurações padrão.
-   Adicione uma [Tabela ModuleConfiguration](moduleconfiguration-table.md) ao módulo de mesclagem para identificar os itens que podem ser configurados por um usuário final. Adicione um registro a esta tabela para cada item configurável. Esses itens são substituídos nos modelos especificados na [tabela ModuleSubstitution](modulesubstitution-table.md). Insira um nome para cada item configurável no campo nome. Insira o formato, o tipo e o contexto semântico para cada item nas colunas Format, Type e ContextData. Para obter mais informações, consulte [tipos semânticos](semantic-types.md). Insira um valor padrão para o item no campo DefaultValue usando o [formato especial CMSM](cmsm-special-format.md).
-   Adicione uma [tabela ModuleSubstitution](modulesubstitution-table.md) ao módulo mesclar. Cada registro nessa tabela corresponde a uma substituição de um ou mais itens configuráveis em um campo do banco de dados do módulo de mesclagem. Insira a tabela, linha e coluna do campo que recebe a substituição. Insira um modelo de formatação para a substituição na coluna valor usando o [formato especial CMSM](cmsm-special-format.md).
-   Adicione registros à [tabela de validação](-validation-table.md) para as tabelas ModuleSubstitution e ModuleConfiguration.
-   Adicione registros à [tabela ModuleIgnoreTable](moduleignoretable-table.md) para a [tabela ModuleSubstitution](modulesubstitution-table.md) e a [Tabela ModuleConfiguration](moduleconfiguration-table.md). Isso garante que o módulo seja compatível com os usuários que têm versões do Mergemod.dll anteriores à versão 2,0.

 

 



