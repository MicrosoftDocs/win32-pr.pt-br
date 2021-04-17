---
description: O arquivo VBScript WiRunSQL.vbs é fornecido nos componentes SDK do Windows para os desenvolvedores de Windows Installer.
ms.assetid: 1027b187-1237-43d1-9905-8fcdaec63903
title: Instruções SQL execute
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99da54f85b02ee867003b140d505f5754f58cc00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105749590"
---
# <a name="execute-sql-statements"></a>Instruções SQL execute

O arquivo VBScript WiRunSQL.vbs é fornecido nos [componentes SDK do Windows para os desenvolvedores de Windows Installer](platform-sdk-components-for-windows-installer-developers.md). Este exemplo mostra como o script é usado para executar consultas SQL e atualizações em um banco de dados Windows Installer. Para obter mais informações, consulte [sintaxe do SQL](sql-syntax.md) e [exemplos de consultas de banco de dados usando SQL e script](examples-of-database-queries-using-sql-and-script.md).

O script de exemplo demonstra:

-   [**Método OpenDatabase (objeto Installer)**](installer-opendatabase.md) e o [**método LastErrorRecord**](installer-lasterrorrecord.md) do [**objeto instalador**](installer-object.md)
-   [**Método OpenView**](database-openview.md)e o [**método Commit**](database-commit.md) do [**objeto Database**](database-object.md)
-   [**Método execute**](view-execute.md) do [ **objeto View**](view-object.md)
-   [**Propriedade StringData**](record-stringdata.md) Propertyof o [ **objeto Record**](record-object.md)

O uso deste exemplo requer a versão CScript.exe ou WScript.exe do Windows Script Host. Para usar CScript.exe para executar este exemplo, digite um comando no prompt de comando usando a sintaxe a seguir. A ajuda será exibida se o primeiro argumento for/? ou se poucos argumentos forem especificados. Para redirecionar a saída para um arquivo, termine a linha de comando com VBS > \[ *caminho para o arquivo* \] . O exemplo retorna um valor de 0 para êxito, 1 se a ajuda for invocada e 2 se o script falhar.

**cscript WiRunSQL.vbs \[ caminho para \] \[ consultas SQL de banco de dados\]**

Especifique o caminho para um banco de dados Windows Installer. Especifique as consultas SQL que devem ser executadas. Observe que a consulta SQL deve ser colocada entre aspas duplas. As consultas SELECT exibem as linhas da lista de resultados especificada na consulta. Colunas de dados binários selecionadas por uma consulta não são exibidas.

Para obter exemplos de script adicionais, consulte [Windows Installer exemplos de script](windows-installer-scripting-examples.md). Para utilitários de exemplo que não exigem o Windows Script Host, consulte [Windows Installer ferramentas de desenvolvimento](windows-installer-development-tools.md).

Para obter mais informações, consulte [trabalhando com consultas](working-with-queries.md) e [exemplos de consultas de banco de dados usando o SQL e o script](examples-of-database-queries-using-sql-and-script.md). O [exemplo](a-localization-example.md) a de localização demonstra como usar o SQL para [localizar colunas de banco de dados](localizing-database-columns.md) e [atualizar um fluxo de informações de resumo](updating-a-summary-information-stream.md).

 

 



