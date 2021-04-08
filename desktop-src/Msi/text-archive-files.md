---
description: As tabelas de banco de dados Windows Installer podem ser exportadas para arquivos de texto ASCII usando MsiDatabaseExport ou o método de exportação do objeto de banco de dados.
ms.assetid: 49210242-bd32-4e5c-b782-a132d670fdfe
title: Arquivos mortos de texto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8baba814fd182a7da5e13fbb26eec257be96ab1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828702"
---
# <a name="text-archive-files"></a>Arquivos mortos de texto

As tabelas de banco de dados Windows Installer podem ser exportadas para arquivos de texto ASCII usando [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) ou o método de [**exportação**](database-export.md) do objeto de [**banco de dados**](database-object.md) . As informações contidas nesses arquivos de texto podem ser importadas de volta para um Windows Installer banco de dados usando o [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) ou o método de [importação](database-import.md) do objeto de **banco de dados** .

Ferramentas como [msidb.exe](msidb-exe.md) são capazes de exportar e importar arquivos mortos de texto. Consulte [exportar arquivos](export-files.md) e [importar arquivos](import-files.md) para obter [Windows Installer exemplos de script](windows-installer-scripting-examples.md) que podem exportar e importar arquivos de texto arquivados de um banco de dados.

> [!Note]  
> Arquivos de texto arquivados não são destinados a um meio de editar o banco de dados de instalação. Você deve usar uma ferramenta de edição de tabela Windows Installer, como [Orca](orca-exe.md) ou uma ferramenta de terceiros, para criar e modificar um pacote de instalação.

 

Os arquivos mortos de texto podem ser usados para as seguintes finalidades.

-   Arquivos de texto arquivados podem ser usados com sistemas de controle de versão.
-   Para remover o espaço de armazenamento desperdiçado e reduzir o tamanho final dos arquivos. msi. Consulte [reduzindo o tamanho de um arquivo. msi](reducing-the-size-of-an--msi-file.md).
-   Para adicionar informações de localização a um banco de dados de instalação. Para obter mais informações, consulte [manipulação de página de código de tabelas importadas e](code-page-handling-of-imported-and-exported-tables.md)exportadas.

-   Para determinar a página de código de um banco de dados. Consulte [determinando a página de código de um banco de dados de instalação](determining-an-installation-database-s-code-page.md).
-   Para definir a página de código de um banco de dados. Consulte [Configurando a página de código de um banco de dados](setting-the-code-page-of-a-database.md).
-   Para aumentar o limite de uma coluna de banco de dados. Exporte a tabela usando [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta), edite o arquivo. IDT exportado e importe a tabela usando [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta). Os autores não podem alterar os tipos de dados de coluna, a nulidade ou os atributos de localização de colunas em tabelas padrão. Consulte também [criando um pacote grande](authoring-a-large-package.md).

As páginas a seguir descrevem as páginas de arquivamento de texto e seus formatos.

-   [Formato de arquivo morto](archive-file-format.md)
-   [Dados ASCII em arquivos mortos de texto](ascii-data-in-text-archive-files.md)
-   [\_ForceCodepage](-forcecodepage.md)
-   [\_SummaryInformation](-summaryinformation.md)

 

 



