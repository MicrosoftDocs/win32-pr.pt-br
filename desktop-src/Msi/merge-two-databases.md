---
description: O arquivo VBScript WiMerge.vbs é fornecido nos componentes SDK do Windows para os desenvolvedores de Windows Installer. Este script de exemplo mescla um banco de dados Windows Installer em outro banco de dados. Para obter mais informações, consulte mesclagens e transformações.
ms.assetid: 31867082-7c1d-4530-a066-236d8ee5f023
title: Mesclar dois bancos de dados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0254cbe2bd0785b45d4ced3a16770023e617bc63
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105751435"
---
# <a name="merge-two-databases"></a>Mesclar dois bancos de dados

O arquivo VBScript WiMerge.vbs é fornecido nos [componentes SDK do Windows para os desenvolvedores de Windows Installer](platform-sdk-components-for-windows-installer-developers.md). Este script de exemplo mescla um banco de dados Windows Installer em outro banco de dados. Para obter mais informações, consulte [mesclagens e transformações](merges-and-transforms.md).

A função [**MsiDatabaseMerge**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea) e o método [**Merge**](database-merge.md) do objeto [**Database**](database-object.md) não podem ser usados para mesclar um módulo incluído no pacote de instalação. Eles não devem ser usados para mesclar [módulos de mesclagem](merge-modules.md) em um pacote Windows Installer. Para incluir um módulo de mesclagem em um pacote de instalação, os autores de pacotes de instalação devem seguir as diretrizes descritas no tópico [aplicando módulos de mesclagem](applying-merge-modules.md) .

O exemplo demonstra o uso do seguinte:

-   [**Método OpenDatabase (objeto instalador)**](installer-opendatabase.md)
-   [**Método LastErrorRecord**](installer-lasterrorrecord.md) do [ **objeto do instalador**](installer-object.md)
-   [**Método OpenView**](database-openview.md)
-   [**Método Merge**](database-merge.md)
-   [**Método Commit**](database-commit.md) do [ **objeto Database**](database-object.md)
-   [**Método Fetch**](view-fetch.md)
-   [**Exibir objeto**](view-object.md)
-   [**Propriedade StringData**](record-stringdata.md) do [ **objeto Record**](record-object.md)

Você deve ter a versão CScript.exe ou WScript.exe do Windows Script Host para usar este exemplo. Para usar CScript.exe para executar este exemplo, digite uma linha de comando no prompt de comando usando a sintaxe a seguir. A ajuda será exibida se o primeiro argumento for/? ou se poucos argumentos forem especificados. Para redirecionar a saída para um arquivo, termine a linha de comando com VBS > \[ caminho para o arquivo \] . O exemplo retorna um valor de 0 para êxito, 1 se a ajuda for invocada e 2 se o script falhar.

**cscript WiMerge.vbs \[ caminho para o caminho do banco \] \[ de dados para o nome da tabela de banco de dados \] \[\]**

Especifique o caminho para o banco de dados de Windows Installer que está recebendo a mesclagem. Especifique o caminho para o banco de dados que está sendo importado para o primeiro. Você pode especificar um nome opcional para uma tabela para manter os erros de mesclagem. Se nenhum nome de tabela for especificado, o instalador usará o nome \_ MergeErrors e descartará a tabela depois de exibir o conteúdo.

Para obter exemplos de script adicionais, consulte [Windows Installer exemplos de script](windows-installer-scripting-examples.md). Para utilitários de exemplo que não exigem o Windows Script Host, consulte [Windows Installer ferramentas de desenvolvimento](windows-installer-development-tools.md).

 

 



