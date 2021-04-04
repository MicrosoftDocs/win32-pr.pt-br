---
description: Um exemplo de uso de consultas de banco de dados controladas por script é fornecido no SDK (Software Development Kit) Windows Installer como o WiRunSQL.vbs do utilitário.
ms.assetid: aa38dbe5-411d-432e-b3fe-09994fc59c75
title: Exemplos de consultas de banco de dados usando SQL e script
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbd839151b40ddd5e9a265c6c370c27a4a9fd125
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103661913"
---
# <a name="examples-of-database-queries-using-sql-and-script"></a>Exemplos de consultas de banco de dados usando SQL e script

Um exemplo de uso de consultas de banco de dados controladas por script é fornecido no SDK ( [Software Development Kit](platform-sdk-components-for-windows-installer-developers.md) ) do Windows Installer como o utilitário WiRunSQL.vbs. Esse utilitário trata as consultas de banco de dados usando a versão Windows Installer do SQL descrita na sintaxe da seção [SQL](sql-syntax.md).

**Excluir um registro de uma tabela**

A linha de comando a seguir exclui o registro com a chave primária vermelha da tabela de [recursos](feature-table.md) do banco de dados Test.msi.

**Cscript WiRunSQL.vbs Test.msi "excluir do \` recurso \` em que o \` recurso \` . \` Recurso \` = ' vermelho ' "**

**Adicionar uma tabela a um banco de dados**

A linha de comando a seguir adiciona a tabela de [diretórios](directory-table.md) ao banco de dados Test.msi.

**CScript WiRunSQL.vbs Test.msi "CREATE TABLE \` Directory \` ( \` diretório \` Char (72) NOT NULL, \` diretório \_ pai \` Char (72), \` DefaultDir \` Char (255) não NULL localizály Primary Key \` Directory \` )"**

**Remover uma tabela de um banco de dados**

A linha de comando a seguir remove a tabela de [recursos](feature-table.md) do banco de dados Test.msi.

**Cscript WiRunSQL.vbs Test.msi "recurso de descartar tabela \` \` "**

**Adicionar uma nova coluna a uma tabela**

A linha de comando a seguir adiciona a coluna de teste à tabela [CustomAction](customaction-table.md) do banco de dados Test.msi.

**CScript WiRunSQL.vbs Test.msi "alterar tabela \` CustomAction \` Adicionar \` inteiro de teste \` "**

**Inserir um novo registro em uma tabela**

A linha de comando a seguir insere um novo registro na tabela de [recursos](feature-table.md) do banco de dados Test.msi.

**Cscript WiRunSQL.vbs Test.msi "recurso inserir \` em \` ( \` recurso \` . \` Recurso \` , \` recurso \` . \` Recurso \_ pai \` , \` recurso \` . \` Título \` , \` recurso \` . \` Descrição \` , \` recurso \` . \` Exibir \` , \` recurso \` . \` Nível \` , \` recurso \` . \` Diretório \_ \` , \` recurso \` . \` Attributes \` ) valores (' tênis ', ' esporte ', ' tênis ', ' Torneio ', 25, 3, ' SPORTDIR ', 2) "**

Isso insere o registro a seguir na tabela de [recursos](feature-table.md) do Test.msi.

[Recurso](feature-table.md) do Tabela



| Recurso | Pai do recurso \_ | Título  | Descrição | Monitor | Nível | Diretório\_ | Atributos |
|---------|-----------------|--------|-------------|---------|-------|-------------|------------|
| Quadra  | Esporte           | Quadra | Torneio  | 25      | 3     | SPORTDIR    | 2          |



 

Observe que os dados binários não podem ser inseridos em uma tabela diretamente usando a inserção ou a atualização de consultas SQL. Para obter informações, consulte [adicionando dados binários a uma tabela usando SQL](adding-binary-data-to-a-table-using-sql.md).

**Modificar um registro existente em uma tabela**

A linha de comando a seguir altera o valor existente no campo título para "desempenho". O registro atualizado tem "Artes" como sua chave primária e está na tabela de recursos do banco de dados Test.msi.

**Cscript WiRunSQL.vbs Test.msi recurso " \` Atualizar \` conjunto de recursos \` \` . \` Title \` = ' desempenho ' em que \` recurso \` . \` Recurso \` = ' artes ' "**

**Selecionar um grupo de registros**

A linha de comando a seguir seleciona o nome e o tipo de todos os controles que pertencem ao ErrorDialog no banco de dados Test.msi.

**CScript WiRunSQL.vbs Test.msi "selecionar \` controle \` , \` tipo \` de \` controle \` onde \` caixa de diálogo \_ \` = ' ErrorDialog '"**

**Manter uma tabela na memória**

A linha de comando a seguir bloqueia a tabela de [componentes](component-table.md) do banco de dados Test.msi na memória.

**CScript WiRunSQL.vbs Test.msi "ALTER TABLE \` componente \` Hold"**

**Liberar uma tabela na memória**

A linha de comando a seguir libera a tabela de [componentes](component-table.md) do banco de dados Test.msi da memória.

**CScript WiRunSQL.vbs Test.msi "alterar o \` componente de tabela \` gratuito"**

 

 



