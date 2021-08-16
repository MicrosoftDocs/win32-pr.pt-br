---
description: O arquivo VBScript WiDiffDb.vbs é fornecido nos componentes do SDK do Windows para desenvolvedores Windows instaladores. Este script de exemplo gera um arquivo de transformação temporário entre dois Windows do Instalador e exibe a transformação.
ms.assetid: 9750ddc6-de8d-48e9-a984-892f0cf4ac3b
title: Exibir diferenças entre dois bancos de dados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cbb04ad6ed1ecaa9d4d5be73708c5edc7dc8c84c9fe230a3725f971d949d335
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118375909"
---
# <a name="view-differences-between-two-databases"></a>Exibir diferenças entre dois bancos de dados

O arquivo VBScript WiDiffDb.vbs é fornecido nos componentes [do SDK do Windows para desenvolvedores Windows instalador.](platform-sdk-components-for-windows-installer-developers.md) Este script de exemplo gera um arquivo de transformação temporário entre dois Windows do Instalador e exibe a transformação.

O exemplo demonstra o uso de:

-   [**Método OpenDatabase (Objeto do Instalador)**](installer-opendatabase.md)
-   [**Método LastErrorRecord**](installer-lasterrorrecord.md) do [ **objeto Installer**](installer-object.md)
-   [**Método OpenView**](database-openview.md)
-   [**Propriedade SummaryInformation (Objeto de Banco de Dados)**](database-summaryinformation.md)
-   [**Método GenerateTransform**](database-generatetransform.md)
-   [**Método ApplyTransform**](database-applytransform.md)
-   [**Objeto de banco de dados**](database-object.md)
-   [**Método Fetch**](view-fetch.md) do [ **objeto View**](view-object.md)
-   [**Propriedade IsNull**](record-isnull.md)
-   [**Propriedade StringData**](record-stringdata.md) do [ **objeto Record**](record-object.md)
-   [\_Tabela TransformView](-transformview-table.md)

Usar este exemplo requer a CScript.exe do host Windows Script. Para usar CScript.exe executar este exemplo, digite um comando no prompt de comando usando a sintaxe a seguir. A ajuda será exibida se o primeiro argumento for /? ou se poucos argumentos são especificados. Para redirecionar a saída para um arquivo, end end the command line with VBS > \[ *path to file* \] . O exemplo retornará um valor de 0 para êxito, 1 se a ajuda for invocada e 2 se o script falhar.

**cscript WiDiffDb.vbs** *\[ caminho do banco de dados original \] \[ para o banco de dados revisado \]*

Especifique o caminho para o banco de dados Windows Instalador original. Especifique o caminho para o banco de dados revisado. O script de exemplo exibirá a transformação.

Para obter exemplos de script adicionais, [consulte exemplos Windows script do instalador.](windows-installer-scripting-examples.md) Para ver os utilitários de exemplo que não exigem Windows Host de Script, consulte Windows Ferramentas de Desenvolvimento [do Instalador](windows-installer-development-tools.md)do .

 

 



