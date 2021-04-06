---
description: O arquivo VBScript WiCompon.vbs é fornecido nos componentes SDK do Windows para os desenvolvedores de Windows Installer. Este script de exemplo pode ser usado para listar os componentes em um banco de dados Windows Installer.
ms.assetid: 4e6cc6f4-821a-4a10-a897-5c6aace1f702
title: Listar componentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b79fa34f62374632ec7fdf52a13c6da8ddbfd82a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647200"
---
# <a name="list-components"></a>Listar componentes

O arquivo VBScript WiCompon.vbs é fornecido nos [componentes SDK do Windows para os desenvolvedores de Windows Installer](platform-sdk-components-for-windows-installer-developers.md). Este script de exemplo pode ser usado para listar os componentes em um banco de dados Windows Installer.

Este exemplo demonstra o uso de várias chaves primárias na [tabela de componentes](component-table.md).

O exemplo também demonstra:

-   [**Método OpenDatabase (objeto instalador)**](installer-opendatabase.md), o [**método CreateRecord**](installer-createrecord.md)e o [**método LastErrorRecord**](installer-lasterrorrecord.md) do [**objeto instalador**](installer-object.md).
-   [**Método OpenView**](database-openview.md), a [**Propriedade TablePersistent**](database-tablepersistent.md)e a [**Propriedade primarykeys**](database-primarykeys.md) do [**objeto Database**](database-object.md).
-   [**Método execute**](view-execute.md) e o [**método FETCH**](view-fetch.md) do [**objeto View**](view-object.md).
-   Propriedade da [**Propriedade StringData**](record-stringdata.md) do [**objeto Record**](record-object.md).

O uso deste exemplo requer a versão CScript.exe ou WScript.exe do Windows Script Host. Para usar CScript.exe para executar este exemplo, digite um comando no prompt de comando usando a sintaxe a seguir. A ajuda será exibida se o primeiro argumento for/? ou se poucos argumentos forem especificados. Para redirecionar a saída para um arquivo, termine a linha de comando com VBS > \[ *caminho para o arquivo* \] . O exemplo retorna um valor de 0 para êxito, 1 se a ajuda for invocada e 2 se o script falhar.

**cscript WiCompon.vbs \[ caminho para o \] nome do componente de banco de dados \[\]**

Especifique o caminho para o banco de dados de Windows Installer. Especifique o nome do componente. O nome deve ser listado na coluna componente da tabela de [componentes](component-table.md). Se o nome do componente for omitido, todos os componentes serão listados. Se um asterisco ( \* ) for usado como o nome do componente, WiCompon.vbs listará a composição de todos os componentes. Observe que bancos de dados grandes são mais bem exibidos usando CScript em vez de WScript.

Para obter exemplos de script adicionais, consulte [Windows Installer exemplos de script](windows-installer-scripting-examples.md). Para utilitários de exemplo que não exigem o Windows Script Host, consulte [Windows Installer ferramentas de desenvolvimento](windows-installer-development-tools.md).

 

 



