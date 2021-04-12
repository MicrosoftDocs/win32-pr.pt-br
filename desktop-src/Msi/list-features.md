---
description: O arquivo VBScript WiFeatur.vbs é fornecido nos componentes SDK do Windows para os desenvolvedores de Windows Installer.
ms.assetid: 797cb383-22c0-42b4-82c1-d5bcc3a8bafb
title: Listar recursos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67e166401b514f1beec9c14c74aba7ca0601f446
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296660"
---
# <a name="list-features"></a>Listar recursos

O arquivo VBScript WiFeatur.vbs é fornecido nos [componentes SDK do Windows para os desenvolvedores de Windows Installer](platform-sdk-components-for-windows-installer-developers.md). Este exemplo mostra como o script é usado para listar os recursos em um banco de dados Windows Installer. Este exemplo demonstra como adicionar colunas temporárias a um banco de dados Windows Installer somente leitura.

Este exemplo demonstra:

-   [**Método OpenDatabase (objeto Installer)**](installer-opendatabase.md), o [**método CreateRecord**](installer-createrecord.md)e o [**método LastErrorRecord**](installer-lasterrorrecord.md) do [**objeto instalador**](installer-object.md)
-   [**Método execute**](view-execute.md) e o [**método FETCH**](view-fetch.md) do [**objeto View**](view-object.md)
-   [**Método OpenView**](database-openview.md), a [**Propriedade TablePersistent**](database-tablepersistent.md)e a [**Propriedade primarykeys**](database-primarykeys.md) do [**objeto Database**](database-object.md)
-   Propriedade [**FieldCount**](record-fieldcount.md), [**Propriedade IntegerData**](record-integerdata.md)e a [**Propriedade StringData**](record-stringdata.md) do [**objeto Record**](record-object.md)

O uso deste exemplo requer a versão CScript.exe ou WScript.exe do Windows Script Host. Para usar CScript.exe para executar este exemplo, digite um comando no prompt de comando usando a sintaxe a seguir. A ajuda será exibida se o primeiro argumento for/? ou se poucos argumentos forem especificados. Para redirecionar a saída para um arquivo, termine a linha de comando com VBS > \[ *caminho para o arquivo* \] . O exemplo retorna um valor de 0 para êxito, 1 se a ajuda for invocada e 2 se o script falhar.

**cscript WiFeatur.vbs \[ caminho para o \] nome do recurso de banco de dados \[\]**

Especifique o caminho para o banco de dados de Windows Installer. Especifique o nome do recurso. Isso deve ser listado na coluna recurso da tabela de [recursos](feature-table.md). Se o nome do recurso for omitido, todos os recursos serão listados como uma árvore de recursos. Se um asterisco ( \* ) for usado como o nome do recurso, WiFeatur.vbs listará a composição de todos os recursos. Observe que bancos de dados grandes são mais bem exibidos usando CScript em vez de WScript.

Para obter mais informações, consulte [Windows Installer exemplos de script](windows-installer-scripting-examples.md) para obter exemplos de script adicionais. Para utilitários de exemplo que não exigem o Windows Script Host, consulte [Windows Installer ferramentas de desenvolvimento](windows-installer-development-tools.md).

 

 



