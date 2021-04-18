---
description: O banco de dados do instalador permite que o desenvolvedor de um pacote de instalação controle a transferência de um aplicativo de uma origem para uma imagem de destino.
ms.assetid: 058cefcd-83dd-4a13-bd55-11d52f9d41f5
title: Usando o banco de dados do instalador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb22b9c66547c849b4c9cbd012e78b22d9301756
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105778555"
---
# <a name="using-the-installer-database"></a>Usando o banco de dados do instalador

O [banco de dados do instalador](installer-database.md) permite que o desenvolvedor de um pacote de instalação controle a transferência de um aplicativo de uma origem para uma imagem de destino. O layout das imagens de origem e de destino do aplicativo é especificado na tabela de [diretórios](directory-table.md) e as ações que instalam o aplicativo são especificadas em seis tabelas de sequência:

-   Tabela [InstallUISequence](installuisequence-table.md)
-   Tabela [InstallExecuteSequence](installexecutesequence-table.md)
-   Tabela [AdminUISequence](adminuisequence-table.md)
-   Tabela [AdminExecuteSequence](adminexecutesequence-table.md)
-   Tabela [AdvtUISequence](advtuisequence-table.md)
-   Tabela [AdvtExecuteSequence](advtexecutesequence-table.md)

As seções a seguir descrevem como usar o [banco de dados do instalador](installer-database.md):

-   [Usando a tabela de diretórios](using-the-directory-table.md)
-   [Usando uma tabela de sequência](using-a-sequence-table.md)
-   [Obtendo um identificador de banco de dados](obtaining-a-database-handle.md)
-   [Confirmando bancos de dados](committing-databases.md)
-   [Importando e exportando](importing-and-exporting.md)
-   [Mesclando bancos de dados](merging-databases.md)
-   [Nomeando tabelas, propriedades e ações personalizadas](naming-custom-tables-properties-and-actions.md)
-   [Limitações de OLE em fluxos](ole-limitations-on-streams.md)
-   [Trabalhando com consultas](working-with-queries.md)
-   [Adicionando dados binários a uma tabela usando SQL](adding-binary-data-to-a-table-using-sql.md)
-   [Trabalhando com registros](working-with-records.md)
-   [Trabalhando com locais de pasta](working-with-folder-locations.md)
-   [Especificando a ordem de auto-registro](specifying-the-order-of-self-registration.md)
-   [Ações de condicionamento a serem executadas durante a remoção](conditioning-actions-to-run-during-removal.md)
-   [Chamando funções de banco de dados de programas](calling-database-functions-from-programs.md)
-   [Sintaxe de instrução condicional](conditional-statement-syntax.md)
-   [Formato de definição de coluna](column-definition-format.md)
-   [Determinando se uma coluna é uma chave primária ou externa](determining-whether-a-column-is-a-primary-or-external-key.md)

 

 



