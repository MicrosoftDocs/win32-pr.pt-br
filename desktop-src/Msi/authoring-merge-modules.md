---
description: O procedimento a seguir descreve as etapas gerais para criar módulos de mesclagem.
ms.assetid: 4b3871c0-f452-4935-9ee3-78b0ac847e67
title: Criando módulos de mesclagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ece67151872a8d065d321c6adaae660be643ad8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169199"
---
# <a name="authoring-merge-modules"></a>Criando módulos de mesclagem

O procedimento a seguir descreve as etapas gerais para criar módulos de mesclagem.

**Para criar um novo módulo de mesclagem**

1.  Obtenha uma ferramenta de software que você pode usar para editar o banco de dados do módulo de mesclagem.
2.  Obtenha um banco de dados de módulo de mesclagem em branco.
3.  Gere um [GUID](guid.md) para o módulo de mesclagem. Você precisa usar esse GUID ao criar as chaves primárias das tabelas de banco de dados no módulo de mesclagem.
4.  Adicione um registro à [tabela de componentes](component-table.md) para cada componente entregue pela mesclagem. Uma tabela de componentes é necessária em cada módulo de mesclagem. Observe que os módulos de mesclagem operam com componentes e não com recursos. Em alguns casos, no entanto, uma entrada de tabela de banco de dados pode precisar fazer referência a um recurso. Para obter detalhes, consulte [Referenciando recursos em módulos de mesclagem](referencing-features-in-merge-modules.md).
5.  Adicione uma [tabela de diretórios](directory-table.md) ao módulo de mesclagem que especifica o layout dos diretórios que o módulo de mesclagem adiciona ao banco de dados de destino. Uma tabela de diretório é necessária em cada módulo de mesclagem.
6.  Importe uma [tabela FeatureComponents](featurecomponents-table.md) em branco para o banco de dados do módulo de mesclagem. Esta tabela vazia fornece uma diretriz para a ferramenta de mesclagem em casos em que o arquivo. msi não contém sua própria tabela FeatureComponents.
7.  Colete todos os arquivos entregues por esse módulo de mesclagem e crie o arquivo de gabinete [MergeModule.CABinet](mergemodule-cabinet.md) . Adicione o gabinete ao módulo de mesclagem como um fluxo dentro do arquivo. msm.
8.  Adicione um registro à tabela de arquivos para cada arquivo armazenado no MergeModule.CABinet.
9.  Adicione as informações necessárias para identificar o módulo de mesclagem na [tabela ModuleSignature](modulesignature-table.md). Cada módulo de mesclagem requer uma tabela ModuleSignature.
10. Liste os componentes no módulo mesclar na [tabela ModuleComponents](modulecomponents-table.md). Cada módulo de mesclagem requer uma tabela ModuleComponents.
11. Adicione tabelas de sequência do módulo de mesclagem ao arquivo. msm somente se o módulo de mesclagem precisar modificar as [*tabelas de sequência*](s-gly.md) do banco de dados de instalação de destino.
12. Adicione uma \_ tabela de validação ao módulo de mesclagem. Um módulo de mesclagem requer uma \_ tabela de validação para passar na validação.
13. Os módulos de mesclagem exigem uma interface do usuário somente em casos raros. Não é recomendável incluir uma interface do usuário com um módulo de mesclagem. Nos casos em que uma interface de usuário é necessária, as tabelas de interface do usuário podem ser mescladas no arquivo. msi da mesma forma que outras tabelas.
14. Adicione informações de registro às tabelas de registro apropriadas no banco de dados do módulo de mesclagem. Adicione informações de registro para bibliotecas de tipos, classes, extensões e verbos nas tabelas [TypeLib](typelib-table.md), [Class](class-table.md), [AppID](appid-table.md), [ProgID](progid-table.md), [extensão](extension-table.md), [verbo](verb-table.md)ou [MIME](mime-table.md) . Todas as outras informações do registro podem entrar na [tabela do registro](registry-table.md). O uso da tabela SelfReg não é recomendado.
15. Adicione as informações de resumo ao [fluxo de informações resumidas do módulo de mesclagem](merge-module-summary-information-stream-reference.md).
16. Execute a validação em todos os módulos de mesclagem antes de tentar instalar o.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Obtendo bancos de dados de módulo de mesclagem em branco](obtaining-blank-merge-module-databases.md)
</dt> <dt>

[Obtendo ferramentas de criação de módulo de mesclagem](obtaining-merge-module-authoring-tools.md)
</dt> <dt>

[Nomeando chaves primárias em bancos de dados do módulo de mesclagem](naming-primary-keys-in-merge-module-databases.md)
</dt> <dt>

[Criando tabelas de componentes do módulo de mesclagem](authoring-merge-module-component-tables.md)
</dt> <dt>

[Criando tabelas de diretório do módulo de mesclagem](authoring-merge-module-directory-tables.md)
</dt> <dt>

[Criando tabelas FeatureComponents do módulo de mesclagem](authoring-merge-module-featurecomponents-tables.md)
</dt> <dt>

[Gerando MergeModule.CABarquivos de gabinete inet](generating-mergemodule-cabinet-cabinet-files.md)
</dt> <dt>

[Criando tabelas de arquivos do módulo de mesclagem](authoring-merge-module-file-tables.md)
</dt> <dt>

[Criando tabelas ModuleSignature](authoring-modulesignature-tables.md)
</dt> <dt>

[Criando tabelas ModuleComponents](authoring-modulecomponents-tables.md)
</dt> <dt>

[Criando tabelas de sequências do módulo de mesclagem](authoring-merge-module-sequence-tables.md)
</dt> <dt>

[Validando módulos de mesclagem](validating-merge-modules.md)
</dt> <dt>

[Criando interfaces de usuário em módulos de mesclagem](authoring-user-interfaces-in-merge-modules.md)
</dt> <dt>

[Criando tabelas de registro do módulo de mesclagem](authoring-merge-module-registry-tables.md)
</dt> <dt>

[Criando fluxos de informações de resumo do módulo de mesclagem](authoring-merge-module-summary-information-streams.md)
</dt> <dt>

[Referência de fluxo de informações de resumo do módulo de mesclagem](merge-module-summary-information-stream-reference.md)
</dt> <dt>

Validando módulos de mesclagem
</dt> <dt>

[Usando módulos de mesclagem de 64 bits](using-64-bit-merge-modules.md)
</dt> </dl>

 

 



