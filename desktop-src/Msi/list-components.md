---
description: O arquivo VBScript WiCompon.vbs é fornecido nos componentes do SDK do Windows para desenvolvedores Windows instaladores. Este script de exemplo pode ser usado para listar os componentes em um banco de dados Windows Instalador.
ms.assetid: 4e6cc6f4-821a-4a10-a897-5c6aace1f702
title: Listar componentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec396e66ed55d78131c74b85432b2f01829cdb5400fc5c00a6ced5725edadeae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129316"
---
# <a name="list-components"></a>Listar componentes

O arquivo VBScript WiCompon.vbs é fornecido nos componentes [do SDK do Windows para desenvolvedores Windows instalador.](platform-sdk-components-for-windows-installer-developers.md) Este script de exemplo pode ser usado para listar os componentes em um banco de dados Windows Instalador.

Este exemplo demonstra o uso de várias chaves primárias na [tabela Componente](component-table.md).

O exemplo também demonstra:

-   [**Método OpenDatabase (Objeto do Instalador),**](installer-opendatabase.md)o [**método CreateRecord**](installer-createrecord.md)e o [**método LastErrorRecord**](installer-lasterrorrecord.md) do [**Objeto do Instalador**](installer-object.md).
-   [**Método OpenView**](database-openview.md), a [**propriedade TablePersistent**](database-tablepersistent.md)e a [**propriedade PrimaryKeys**](database-primarykeys.md) do Objeto [**de Banco de Dados**](database-object.md).
-   [**Execute o método**](view-execute.md) e [**o método Fetch**](view-fetch.md) do Objeto de [**Exibição**](view-object.md).
-   [**Propriedade StringData**](record-stringdata.md) do [**Objeto de Registro**](record-object.md).

Usar este exemplo requer a versão CScript.exe ou WScript.exe do host Windows Script. Para usar CScript.exe executar este exemplo, digite um comando no prompt de comando usando a sintaxe a seguir. A ajuda será exibida se o primeiro argumento for /? ou se poucos argumentos são especificados. Para redirecionar a saída para um arquivo, end end the command line with VBS > \[ *path to file* \] . O exemplo retornará um valor de 0 para êxito, 1 se a ajuda for invocada e 2 se o script falhar.

**cscript WiCompon.vbs \[ caminho para o nome do componente de banco de \] \[ dados\]**

Especifique o caminho para o banco Windows do Instalador. Especifique o nome do componente. O nome deve ser listado na coluna Componente da [tabela Componente](component-table.md). Se o nome do componente for omitido, todos os componentes serão listados. Se um asterisco ( ) for usado como o nome do componente, WiCompon.vbs \* lista a composição de todos os componentes. Observe que bancos de dados grandes são melhor exibidos usando CScript em vez de WScript.

Para obter exemplos de script adicionais, [consulte exemplos Windows script do instalador.](windows-installer-scripting-examples.md) Para ver os utilitários de exemplo que não exigem Windows Host de Script, consulte Windows Ferramentas de Desenvolvimento [do Instalador](windows-installer-development-tools.md)do .

 

 



