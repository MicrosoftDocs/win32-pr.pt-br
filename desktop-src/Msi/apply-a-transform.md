---
description: O arquivo VBScript WiUseXfm.vbs é fornecido nos componentes SDK do Windows para os desenvolvedores de Windows Installer. Este exemplo mostra como o script pode ser usado para aplicar uma transformação a um banco de dados Windows Installer.
ms.assetid: e647388e-5211-463d-9e3e-b502af01fc0c
title: Aplicar uma transformação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9e86acc495fc2a0bb8dff562832e58d29483256
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828073"
---
# <a name="apply-a-transform"></a>Aplicar uma transformação

O arquivo VBScript WiUseXfm.vbs é fornecido nos [componentes SDK do Windows para os desenvolvedores de Windows Installer](platform-sdk-components-for-windows-installer-developers.md). Este exemplo mostra como o script pode ser usado para aplicar uma transformação a um banco de dados Windows Installer.

O exemplo demonstra o uso de

-   [**Método OpenDatabase (objeto instalador)**](installer-opendatabase.md)
-   [**Método LastErrorRecord**](installer-lasterrorrecord.md) do [ **objeto do instalador**](installer-object.md)
-   [**Método ApplyTransform**](database-applytransform.md)
-   [**Método Commit**](database-commit.md) do [ **objeto Database**](database-object.md)

Você precisará da versão CScript.exe ou WScript.exe do Windows Script Host para usar este exemplo. Para usar CScript.exe para executar este exemplo, digite uma linha de comando no prompt de comando usando a sintaxe a seguir. A ajuda será exibida se o primeiro argumento for/? ou se poucos argumentos forem especificados. Para redirecionar a saída para um arquivo, termine a linha de comando com VBS > \[ *caminho para o arquivo* \] . O exemplo retorna um valor de 0 para êxito, 1 se a ajuda for invocada e 2 se o script falhar.

**cscript WiUseXfm.vbs \[ caminho para o caminho do banco de dados original \] \[ para \] \[ as opções de arquivo de transformação\]**

Especifique o caminho para o banco de dados de Windows Installer. Especifique o caminho para o arquivo de transformação. Se o caminho para o arquivo de transformação for omitido, os dois bancos de dados serão comparados apenas. O terceiro argumento é um valor numérico opcional que especifica um conjunto de condições de erro que devem ser suprimidas. Adicione esses valores juntos para suprimir várias condições.



| Valor | Condição de erro para suprimir                   |
|-------|-----------------------------------------------|
| 1     | Adicionando uma linha que já existe.             |
| 2     | Excluindo uma linha que não existe.           |
| 4     | Adicionando uma tabela que já existe.           |
| 8     | Excluindo uma tabela que não existe.         |
| 16    | Atualizando uma linha que não existe.           |
| 256   | Incompatibilidade de páginas de código de banco de dados e transformação. |



 

Para obter exemplos de script adicionais, consulte [Windows Installer exemplos de script](windows-installer-scripting-examples.md). Para utilitários de exemplo que não exigem o Windows Script Host, consulte [Windows Installer ferramentas de desenvolvimento](windows-installer-development-tools.md).

 

 



