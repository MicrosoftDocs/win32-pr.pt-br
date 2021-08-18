---
description: O Banco de Dados do Instalador permite que o desenvolvedor de um pacote de instalação controle a transferência de um aplicativo de uma origem para uma imagem de destino.
ms.assetid: 058cefcd-83dd-4a13-bd55-11d52f9d41f5
title: Usando o banco de dados do instalador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dec91d8982a8ddac47c96303f03a33e4c85cafa70c3ef480c660df42e72f8a84
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996056"
---
# <a name="using-the-installer-database"></a>Usando o banco de dados do instalador

O [Banco de Dados do Instalador](installer-database.md) permite que o desenvolvedor de um pacote de instalação controle a transferência de um aplicativo de uma origem para uma imagem de destino. O layout das imagens de origem e de destino do aplicativo é especificado na tabela [Diretório](directory-table.md) e as ações que instalam o aplicativo são especificadas em seis tabelas de sequência:

-   [Tabela InstallUISequence](installuisequence-table.md)
-   [Tabela InstallExecuteSequence](installexecutesequence-table.md)
-   [Tabela AdminUISequence](adminuisequence-table.md)
-   [Tabela AdminExecuteSequence](adminexecutesequence-table.md)
-   [Tabela AdvtUISequence](advtuisequence-table.md)
-   [Tabela AdvtExecuteSequence](advtexecutesequence-table.md)

As seções a seguir descrevem como usar o Banco [de Dados do Instalador](installer-database.md):

-   [Usando a tabela de diretório](using-the-directory-table.md)
-   [Usando uma tabela de sequência](using-a-sequence-table.md)
-   [Obtendo um guidão de banco de dados](obtaining-a-database-handle.md)
-   [Commitindo bancos de dados](committing-databases.md)
-   [Importando e exportando](importing-and-exporting.md)
-   [Mesclando bancos de dados](merging-databases.md)
-   [Nomeando tabelas, propriedades e ações personalizadas](naming-custom-tables-properties-and-actions.md)
-   [Limitações do OLE Fluxos](ole-limitations-on-streams.md)
-   [Trabalhando com consultas](working-with-queries.md)
-   [Adicionando dados binários a uma tabela usando SQL](adding-binary-data-to-a-table-using-sql.md)
-   [Trabalhando com registros](working-with-records.md)
-   [Trabalhando com locais de pasta](working-with-folder-locations.md)
-   [Especificando a ordem de auto-registro](specifying-the-order-of-self-registration.md)
-   [Ações de condicionação a executar durante a remoção](conditioning-actions-to-run-during-removal.md)
-   [Chamando funções de banco de dados de programas](calling-database-functions-from-programs.md)
-   [Sintaxe da instrução condicional](conditional-statement-syntax.md)
-   [Formato de definição de coluna](column-definition-format.md)
-   [Determinando se uma coluna é uma chave primária ou externa](determining-whether-a-column-is-a-primary-or-external-key.md)

 

 



