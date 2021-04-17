---
description: O arquivo VBScript WiExport.vbs é fornecido nos componentes SDK do Windows para os desenvolvedores de Windows Installer.
ms.assetid: 3ff7bd48-cb22-4d5b-a607-39eaeb67c55b
title: Exportar arquivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1512650ee144fc00c2de851051b9bbb4d98a21e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105760840"
---
# <a name="export-files"></a>Exportar arquivos

O arquivo VBScript WiExport.vbs é fornecido nos [componentes SDK do Windows para os desenvolvedores de Windows Installer](platform-sdk-components-for-windows-installer-developers.md). Este exemplo mostra como gravar script para exportar tabelas para um banco de dados Windows Installer. O script de exemplo se conecta a um objeto do [**instalador**](installer-object.md) , abre um banco de dados e exporta tabelas para arquivos mortos.

O exemplo demonstra o uso de:

-   [**Método OpenDatabase (objeto instalador)**](installer-opendatabase.md)
-   [**Método LastErrorRecord**](installer-lasterrorrecord.md) do [ **objeto do instalador**](installer-object.md)
-   [**Método de exportação**](database-export.md)
-   [**Método OpenView**](database-openview.md) do [ **objeto Database**](database-object.md)
-   [**Método FETCH**](view-fetch.md) do [ **objeto View**](view-object.md)
-   [**Propriedade StringData**](record-stringdata.md) do [ **objeto Record**](record-object.md)

Você precisará da versão CScript.exe ou WScript.exe do Windows Script Host para usar este exemplo. Para usar CScript.exe para executar este exemplo, digite uma linha de comando no prompt de comando usando a sintaxe a seguir. A ajuda será exibida se o primeiro argumento for/? ou se poucos argumentos forem especificados. Para redirecionar a saída para um arquivo, termine a linha de comando com VBS > \[ *caminho para o arquivo* \] . O exemplo retorna um valor de 0 para êxito, 1 se a ajuda for invocada e 2 se o script falhar.

**cscript WiExport.vbs \[ caminho para o caminho do banco \] \[ de dados para \] \[ as opções de pasta lista de \] \[ nomes de tabela\]**

Especifique o caminho para o banco de dados do instalador do qual as tabelas estão sendo exportadas. Especifique o caminho para a pasta na qual os arquivos mortos exportados devem ser copiados. Listar os nomes que diferenciam maiúsculas de minúsculas das [tabelas de banco de dados](database-tables.md) que estão sendo Especifique ' \* ' para exportar todas as tabelas, incluindo \_ SummaryInformation.

As opções a seguir podem ser especificadas em qualquer lugar na linha de comando antes da lista nome da tabela.



| Opção              | Descrição                                            |
|---------------------|--------------------------------------------------------|
| nenhuma opção especificada | Arquivos mortos exportados podem ter um nome de arquivo longo.      |
| /s                  | Force os arquivos exportados para terem nomes de arquivo curtos. |



 

Para obter exemplos de script adicionais, consulte [Windows Installer exemplos de script](windows-installer-scripting-examples.md). Para utilitários de exemplo que não exigem o Windows Script Host, consulte [Windows Installer ferramentas de desenvolvimento](windows-installer-development-tools.md).

 

 



