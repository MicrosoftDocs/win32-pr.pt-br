---
description: O arquivo VBScript WiLstXfm.vbs é fornecido nos componentes SDK do Windows para os desenvolvedores de Windows Installer. Este exemplo de script pode ser usado para exibir um arquivo de transformação.
ms.assetid: c2e3dd56-b0e5-481a-b7b8-5000fa686850
title: Exibir uma transformação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69f4a858f8deb115de967da3b4d485b596f85cee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105749566"
---
# <a name="view-a-transform"></a>Exibir uma transformação

O arquivo VBScript WiLstXfm.vbs é fornecido nos [componentes SDK do Windows para os desenvolvedores de Windows Installer](platform-sdk-components-for-windows-installer-developers.md). Este exemplo de script pode ser usado para exibir um arquivo de transformação.

O exemplo demonstra o uso de:

-   [\_Tabela de transformview](-transformview-table.md)
-   [**Método OpenDatabase (objeto instalador)**](installer-opendatabase.md)
-   [**Método LastErrorRecord**](installer-lasterrorrecord.md) do [ **objeto do instalador**](installer-object.md)
-   [**Método ApplyTransform**](database-applytransform.md)
-   [**Método OpenView**](database-openview.md)
-   [**Método Commit**](database-commit.md) do [ **objeto Database**](database-object.md)
-   [**Propriedade IsNull**](record-isnull.md)
-   [**Propriedade StringData**](record-stringdata.md) do [ **objeto Record**](record-object.md)

O uso deste exemplo requer a versão CScript.exe do Windows Script Host. Para usar CScript.exe para executar este exemplo, digite um comando no prompt de comando usando a sintaxe a seguir. A ajuda será exibida se o primeiro argumento for/? ou se poucos argumentos forem especificados. Para redirecionar a saída para um arquivo, termine a linha de comando com VBS > \[ *caminho para o arquivo* \] . O exemplo retorna um valor de 0 para êxito, 1 se a ajuda for invocada e 2 se o script falhar.

**cscript WiLstXfm.vbs** *\[ caminho para o caminho de opção de banco de dados de referência \] \[ \] \[ a ser exibido \] para transformação*

Especifique o caminho para a referência Windows Installer banco de dados. Especifique uma lista de caminhos para transformar os arquivos que estão sendo exibidos. Cada caminho na lista pode ser precedido por um valor numérico opcional. Esse valor especifica um conjunto de condições de erro que devem ser suprimidas. Você pode adicionar esses valores juntos para suprimir várias condições. Se nenhuma opção numérica for especificada, todas as condições de erro serão suprimidas. Os argumentos nessa lista são executados na ordem da esquerda para a direita na qual aparecem na linha de comando.



| Valor | Condição de erro para suprimir                   |
|-------|-----------------------------------------------|
| 1     | Adicionando uma linha que já existe.             |
| 2     | Excluindo uma linha que não existe.           |
| 4     | Adicionando uma tabela que já existe.           |
| 8     | Excluindo uma tabela que não existe.         |
| 16    | Atualizando uma linha que não existe.           |
| 256   | Incompatibilidade de páginas de código de banco de dados e transformação. |



 

Para obter exemplos de script adicionais, consulte [Windows Installer exemplos de script](windows-installer-scripting-examples.md). Para utilitários de exemplo que não exigem o Windows Script Host, consulte [Windows Installer ferramentas de desenvolvimento](windows-installer-development-tools.md).

 

 



