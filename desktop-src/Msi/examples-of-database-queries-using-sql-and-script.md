---
description: Um exemplo de uso de consultas de banco de dados controladas por script é fornecido no SDK (Kit de Desenvolvimento de Software) do Windows Installer como o utilitário WiRunSQL.vbs.
ms.assetid: aa38dbe5-411d-432e-b3fe-09994fc59c75
title: Exemplos de consultas de banco de dados usando SQL e script
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f137927ba47c4fae5eef4534b7dfab1fa5c8fa1af2ba28d27669cc4605f836b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118947048"
---
# <a name="examples-of-database-queries-using-sql-and-script"></a>Exemplos de consultas de banco de dados usando SQL e script

Um exemplo de como usar consultas de banco de dados controladas por script é fornecido no SDK [(Software Development Kit)](platform-sdk-components-for-windows-installer-developers.md) do Windows Installer como o utilitário WiRunSQL.vbs. Esse utilitário lida com consultas de banco de dados usando Windows versão do SQL do SQL descrita na seção [sintaxe SQL .](sql-syntax.md)

**Excluir um registro de uma tabela**

A linha de comando a seguir exclui o registro que tem a chave primária RED da [tabela Recurso](feature-table.md) do banco de Test.msi dados.

**Cscript WiRunSQL.vbs Test.msi "DELETE FROM \` Feature WHERE Feature \` \` \` . \` Recurso \` ='RED'"**

**Adicionar uma tabela a um banco de dados**

A linha de comando a seguir adiciona a [tabela Directory](directory-table.md) ao banco de Test.msi dados.

**CScript WiRunSQL.vbs Test.msi "CREATE TABLE Directory \` \` ( \` Diretório \` CHAR(72) NOT NULL, \` DIRECTORY Parent \_ \` CHAR(72), \` DefaultDir \` CHAR(255) NOT NULL LOCALIZABLE PRIMARY KEY \` Directory \` )"**

**Remover uma tabela de um banco de dados**

A linha de comando a seguir remove a [tabela Recurso](feature-table.md) do banco de Test.msi dados.

**Cscript WiRunSQL.vbs Test.msi "Recurso DROP \` \` TABLE"**

**Adicionar uma nova coluna a uma tabela**

A linha de comando a seguir adiciona a coluna Test à [tabela CustomAction](customaction-table.md) do banco de Test.msi dados.

**CScript WiRunSQL.vbs Test.msi "ALTER TABLE \` CustomAction \` ADD \` Test \` INTEGER"**

**Inserir um novo registro em uma tabela**

A linha de comando a seguir insere um novo registro na [tabela Recurso](feature-table.md) do banco Test.msi dados.

**O Cscript WiRunSQL.vbs Test.msi "INSERT INTO \` Feature \` ( Feature \` \` . \` Recurso \` , \` Recurso \` . \` Pai \_ do \` recurso, Recurso \` \` . \` Título \` , \` Recurso \` . \` Descrição \` , \` Recurso \` . \` Exibir \` , \` Recurso \` . \` Nível \` , \` Recurso \` . \` Diretório \_ \` , Recurso \` \` . \` Atributos \` ) VALUES ('Jogador', 'Esporte', 'Jogador', 'Jogador', 25,3,'SPORTDIR',2)"**

Isso insere o registro a seguir na [tabela](feature-table.md) Recurso do Test.msi.

[Recurso](feature-table.md) Tabela



| Recurso | Pai do \_ recurso | Título  | Descrição | Exibir | Nível | Diretório\_ | Atributos |
|---------|-----------------|--------|-------------|---------|-------|-------------|------------|
| Tênis  | Esporte           | Tênis | Torneio  | 25      | 3     | SPORTDIR    | 2          |



 

Observe que os dados binários não podem ser inseridos em uma tabela diretamente usando as consultas INSERT INTO ou UPDATE SQL. Para obter [informações, consulte Adicionando dados binários a uma tabela usando SQL](adding-binary-data-to-a-table-using-sql.md).

**Modificar um registro existente em uma tabela**

A linha de comando a seguir altera o valor existente no campo Título para "Desempenhos". O registro atualizado tem "Delas" como sua chave primária e está na tabela Recurso do banco de Test.msi dados.

**Cscript WiRunSQL.vbs Test.msi "Recurso UPDATE \` FEATURE \` SET Feature \` \` . \` Título \` ='Performances' WHERE \` Feature \` . \` Feature \` ='Ninja'"**

**Selecionar um grupo de registros**

A linha de comando a seguir seleciona o nome e o tipo de todos os controles que pertencem ao ErrorDialog no banco de Test.msi dados.

**CScript WiRunSQL.vbs Test.msi "SELECT \` Control \` , Type FROM Control WHERE Dialog \` \` \` \` \` \_ \` ='ErrorDialog' "**

**Manter uma tabela na memória**

A linha de comando a seguir bloqueia [a tabela Componente](component-table.md) do banco de Test.msi na memória.

**CScript WiRunSQL.vbs Test.msi "ALTER TABLE \` Component \` HOLD"**

**Liberar uma tabela na memória**

A linha de comando a seguir libera a [tabela Componente](component-table.md) do banco de Test.msi de dados da memória.

**CScript WiRunSQL.vbs Test.msi "ALTER TABLE \` Component \` FREE"**

 

 



