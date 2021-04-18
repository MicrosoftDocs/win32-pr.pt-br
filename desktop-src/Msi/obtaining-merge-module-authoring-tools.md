---
description: Para gerar um módulo de mesclagem, você precisa obter uma ferramenta de software com a qual editar um arquivo. msm.
ms.assetid: bc14d36a-b299-4c61-ade2-43fad142d21d
title: Obtendo ferramentas de criação de módulo de mesclagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dac673c7cfa191cecb1b576e1b17f2f4a7a1f4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105757380"
---
# <a name="obtaining-merge-module-authoring-tools"></a>Obtendo ferramentas de criação de módulo de mesclagem

Para gerar um módulo de mesclagem, você precisa obter uma ferramenta de software com a qual editar um arquivo. msm. Como um arquivo. msm é basicamente um arquivo. msi simplificado, talvez você possa usar as mesmas ferramentas usadas para criar um banco de dados de instalação. Por exemplo, o aplicativo Orca.exe fornecido com o SDK do Windows Installer.

Uma alternativa é comprar uma das ferramentas de empacotamento do instalador para estar disponível de fornecedores de software independentes. Há várias ferramentas de terceiros em desenvolvimento que podem ser usadas para produzir módulos de mesclagem. Se você optar por usar uma ferramenta de terceiros, deverá verificar se ela gera módulos de mesclagem consistentes com o padrão descrito neste documento. Em particular, você deve determinar que as ferramentas de edição não fizeram nenhuma das ações a seguir para o módulo de mesclagem.

-   Adicionadas tabelas estranhas ao módulo de mesclagem que não são referenciadas na [tabela ModuleIgnoreTable](moduleignoretable-table.md).

    Exclua essas tabelas ou adicione-as à tabela ModuleIgnoreTable.

-   Adicionada uma [tabela de TextStyle](textstyle-table.md) desnecessária ao módulo de mesclagem.

    Se o módulo de mesclagem não tiver nenhuma interface do usuário (e geralmente não deveria), você poderá excluir essa tabela com segurança.

-   Foram adicionadas entradas desnecessárias à [tabela de diretórios](directory-table.md).

    Remova as entradas desnecessárias da tabela de diretórios.

-   Informações da esquerda da tabela de validação do módulo de mesclagem \_ .

    Isso impede a validação do módulo de mesclagem. Adicione uma \_ tabela de validação completa.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando interfaces de usuário em módulos de mesclagem](authoring-user-interfaces-in-merge-modules.md)
</dt> <dt>

[Criando tabelas de diretório do módulo de mesclagem](authoring-merge-module-directory-tables.md)
</dt> <dt>

[Validando módulos de mesclagem](validating-merge-modules.md)
</dt> </dl>

 

 



