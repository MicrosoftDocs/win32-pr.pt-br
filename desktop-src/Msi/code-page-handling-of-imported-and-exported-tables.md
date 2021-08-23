---
description: Você pode adicionar informações de localização a um banco de dados de instalação importando e exportando arquivos mortos de texto ASCII usando MsiDatabaseExport e MsiDatabaseImport.
ms.assetid: dc52313b-38e7-43cc-abfd-86966c836fce
title: Manipulação de página de código de tabelas importadas e exportadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f9a64617ccfda25380076d62e6dd4ad8c18c55f68afd0236b3258638c899f29
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065996"
---
# <a name="code-page-handling-of-imported-and-exported-tables"></a>Manipulação de página de código de tabelas importadas e exportadas

Você pode adicionar informações de localização a um banco de dados de instalação importando e exportando arquivos mortos de texto ASCII usando [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) e [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta). Como o pool de cadeias de caracteres de banco de dados usa uma página de código ANSI, o banco de dados e os [arquivos mortos de texto](text-archive-files.md) exportados têm páginas

Quando um [arquivo morto de texto](text-archive-files.md) é exportado de um banco de dados, a página de código do arquivo morto é igual ao banco de dados pai. Para obter uma lista de páginas de código numérico, consulte [localizando as tabelas Error e ActionText](localizing-the-error-and-actiontext-tables.md).

> [!Note]  
> Exportar uma tabela para um arquivo morto de texto traduz os caracteres de controle para evitar conflitos com delimitadores de arquivo.

 

## <a name="ascii-text-archive-files"></a>Arquivos mortos de texto ASCII

Os [arquivos mortos de texto](text-archive-files.md) ASCII exportados por [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) são explicados no seguinte formato:

-   Os nomes das colunas da tabela são gravados na primeira linha.
-   Os formatos de coluna são gravados na segunda linha.
-   Se a tabela contiver apenas dados ASCII, a terceira linha do arquivo de texto será o nome da tabela seguido de uma lista das chaves primárias.
-   Se a tabela contiver dados não ASCII e o banco de dado for carimbado com uma página de código numérica, o número da página de código aparecerá no início da terceira linha.
-   Se o banco de dados contiver um dado não-ASCII, mas não estiver carimbado com a página de código numérico, o número da página de código do sistema atual será gravado no início da terceira linha.
-   As linhas restantes do arquivo de texto são os dados na página de código especificada.
-   Se uma tabela contiver fluxos, o [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) exporta cada fluxo na tabela para um arquivo separado.

### <a name="neutral-and-non-neutral-code-pages"></a>Páginas de código neutras e não neutras

Você pode facilitar a localização iniciando com um banco de dados que tem uma página de código neutra:

-   Um banco de dados em branco tem uma página de código neutra.
-   Um banco de dados que não contém caracteres estendidos que exigem uma página de código para ser representado em ASCII tem uma página de código neutra.

Para obter mais informações, consulte [criando um banco de dados com uma página de código neutra](creating-a-database-with-a-neutral-code-page.md).

As páginas de código neutras e não neutras têm as seguintes características:

-   Se um [arquivo morto de texto](text-archive-files.md) com uma página de código não neutra for importado para um banco de dados que tenha uma página de código diferente de neutro, o instalador retornará um erro quando [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) for chamado.
-   Um [arquivo morto de texto](text-archive-files.md) que tem uma página de código neutra pode ser importado para um banco de dados que tenha qualquer página de código.
-   Um [arquivo morto de texto](text-archive-files.md) que tem qualquer página de código pode ser importado para um banco de dados que tem uma página de código neutra.
-   A importação de um [arquivo morto de texto](text-archive-files.md) em um banco de dados com uma página de código neutra define a página de código do banco de dados para a página de código do arquivo morto. Todos os arquivos mortos subsequentemente importados para o banco de dados devem ter a mesma página de código que o primeiro arquivo.

Para obter mais informações, consulte [determinando uma página de código do banco de dados de instalação](determining-an-installation-database-s-code-page.md) e [definindo a página de código de um banco de dados](setting-the-code-page-of-a-database.md).

Os [arquivos mortos de texto](text-archive-files.md) exportados pelo [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) podem ser usados com sistemas de controle de versão. Use as [funções de banco](database-functions.md) de dados ou um editor de tabela de banco de dados para editar o banco de dados.

você pode adicionar informações de localização a um banco de dados de instalação usando um editor de tabela de banco de dados ou a API Windows Installer. Para obter mais informações, consulte [manipulação de página de código de cadeias de caracteres de parâmetro](code-page-handling-of-parameter-strings.md).

 

 



