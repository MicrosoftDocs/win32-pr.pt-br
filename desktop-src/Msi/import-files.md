---
description: O arquivo VBScript WiImport.vbs é fornecido nos componentes SDK do Windows para os desenvolvedores de Windows Installer. Este exemplo mostra como gravar um script para importar tabelas para um banco de dados Windows Installer.
ms.assetid: 37580bd6-30c7-4239-9717-223a381ba021
title: Importar arquivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8508ee4e385e3edc737515f1b524de074489fb2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105752254"
---
# <a name="import-files"></a>Importar arquivos

O arquivo VBScript WiImport.vbs é fornecido nos [componentes SDK do Windows para os desenvolvedores de Windows Installer](platform-sdk-components-for-windows-installer-developers.md). Este exemplo mostra como gravar um script para importar tabelas para um banco de dados Windows Installer.

O script se conecta a um objeto do [**instalador**](installer-object.md) , abre um banco de dados, processa uma lista de arquivos e confirma as alterações antes de fechar o banco de dados.

O exemplo demonstra o uso de:

-   [**Método OpenDatabase (objeto instalador)**](installer-opendatabase.md)
-   [**Método LastErrorRecord**](installer-lasterrorrecord.md) do [ **objeto do instalador**](installer-object.md)
-   [**Método Import**](database-import.md)
-   [**Método Commit**](database-commit.md) do [ **objeto Database**](database-object.md)

Você precisará da versão CScript.exe ou WScript.exe do Windows Script Host para usar este exemplo. Para usar CScript.exe para executar este exemplo, use a sintaxe a seguir no prompt de comando.

**cscript WiImport.vbs \[ caminho para o caminho do banco \] \[ de dados para \] \[ as opções de pasta lista de \] \[ arquivos de arquivo**\]

A ajuda será exibida se o primeiro argumento for/? ou se poucos argumentos forem especificados. Para redirecionar a saída para um arquivo, termine a linha de comando com VBS > \[ caminho para o arquivo \] . O exemplo retorna um valor de 0 para êxito, 1 se a ajuda for invocada e 2 se o script falhar.

Especifique o caminho para um banco de dados do Windows Installer que será criado ou que deve receber as tabelas importadas. Especifique o caminho para a pasta que contém os arquivos mortos das tabelas que estão sendo importadas. Liste os nomes dos arquivos mortos que estão sendo importados. Nomes de arquivo curinga, como \* . IDT, podem ser usados para importar vários arquivos.

As opções a seguir podem ser especificadas em qualquer lugar na linha de comando antes da lista de arquivos.



| Opção              | Descrição                                                                                                                          |
|---------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| nenhuma opção especificada | Importe a lista de arquivos de tabela arquivados da pasta especificada para o banco de dados Windows Installer.                                |
| /c                  | Crie um banco de dados Windows Installer e importe a lista de arquivos de tabela de arquivo da pasta especificada para o novo banco de dados. |



 

Para obter mais informações, consulte [Windows Installer exemplos de script](windows-installer-scripting-examples.md) para obter exemplos de script adicionais. Para utilitários de exemplo que não exigem o Windows Script Host, consulte [Windows Installer ferramentas de desenvolvimento](windows-installer-development-tools.md).

Observe que [um exemplo de localização](a-localization-example.md) também demonstra a [importação de tabelas de erro e ActionText localizadas](importing-localized-error-and-actiontext-tables.md).

 

 



