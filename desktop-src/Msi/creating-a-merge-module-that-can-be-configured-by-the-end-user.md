---
description: Para criar módulos de mesclagem, use as diretrizes gerais descritas no tópico Criando módulos de mesclagem.
ms.assetid: 9d5e60dc-9133-4c6e-9a47-dd341f2757fa
title: Criando um módulo de mesclagem que pode ser configurado pelo End-User
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0d1b4ffebe21659d33640c3872e9e6c7875518654b86d256ea4b858444ef39e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118948126"
---
# <a name="creating-a-merge-module-that-can-be-configured-by-the-end-user"></a>Criando um módulo de mesclagem que pode ser configurado pelo End-User

Para criar módulos de mesclagem, use as diretrizes gerais descritas no tópico [Criando módulos de mesclagem.](authoring-merge-modules.md) Além disso, você deve fazer o seguinte para criar um módulo de mesclagem que possa ser configurado pelo usuário final do módulo:

-   Os usuários finais precisam ter Mergemod.dll versão 2.0 para configurar seu módulo. Os usuários que têm versões anteriores do Mergemod.dll podem aplicar o módulo, mas sempre têm as configurações padrão.
-   Adicione uma [Tabela ModuleConfiguration](moduleconfiguration-table.md) ao módulo de mesclagem para identificar os itens que podem ser configurados por um usuário final. Adicione um registro nesta tabela para cada item configurável. Esses itens são substituídos nos modelos especificados na [Tabela ModuleSubstitution](modulesubstitution-table.md). Insira um nome para cada item configurável no campo Nome. Insira o formato, o tipo e o contexto semântico para cada item nas colunas Format, Type e ContextData. Para obter mais informações, consulte [Tipos semânticos](semantic-types.md). Insira um valor padrão para o item no campo DefaultValue usando o [Formato Especial do CMSM](cmsm-special-format.md).
-   Adicione uma [Tabela ModuleSubstitution](modulesubstitution-table.md) ao módulo de mesclagem. Cada registro nesta tabela corresponde a uma substituição de um ou mais itens configuráveis em um campo do banco de dados do módulo de mesclagem. Insira a tabela, a linha e a coluna do campo que recebe a substituição. Insira um modelo de formatação para a substituição na coluna Valor usando o [Formato Especial do CMSM](cmsm-special-format.md).
-   Adicione registros à Tabela [de Validação](-validation-table.md) para as tabelas ModuleSubstitution e ModuleConfiguration.
-   Adicione registros à Tabela [ModuleIgnoreTable](moduleignoretable-table.md) para a [Tabela ModuleSubstitution](modulesubstitution-table.md) e a [Tabela ModuleConfiguration](moduleconfiguration-table.md). Isso garante que o módulo seja compatível com usuários que têm versões do Mergemod.dll anteriores à versão 2.0.

 

 



