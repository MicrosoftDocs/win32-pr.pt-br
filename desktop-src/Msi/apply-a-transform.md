---
description: O arquivo VBScript WiUseXfm.vbs é fornecido nos componentes do SDK do Windows para desenvolvedores Windows instaladores. Este exemplo mostra como o script pode ser usado para aplicar uma transformação a um banco de dados Windows Instalador.
ms.assetid: e647388e-5211-463d-9e3e-b502af01fc0c
title: Aplicar uma transformação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 001737b1a08ea33ce233fa0aad90e96e23a1079f2c28f9d6308219cba270f6ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118381605"
---
# <a name="apply-a-transform"></a>Aplicar uma transformação

O arquivo VBScript WiUseXfm.vbs é fornecido nos componentes [do SDK do Windows para](platform-sdk-components-for-windows-installer-developers.md)desenvolvedores Windows instalador. Este exemplo mostra como o script pode ser usado para aplicar uma transformação a um banco de dados Windows Instalador.

O exemplo demonstra o uso de

-   [**Método OpenDatabase (Objeto do Instalador)**](installer-opendatabase.md)
-   [**Método LastErrorRecord**](installer-lasterrorrecord.md) do [ **objeto Installer**](installer-object.md)
-   [**Método ApplyTransform**](database-applytransform.md)
-   [**Método commit do**](database-commit.md) objeto [ **Database**](database-object.md)

Você exigirá a versão CScript.exe ou WScript.exe do host Windows Script para usar este exemplo. Para usar CScript.exe executar este exemplo, digite uma linha de comando no prompt de comando usando a sintaxe a seguir. A ajuda será exibida se o primeiro argumento for /? ou se poucos argumentos são especificados. Para redirecionar a saída para um arquivo, termine a linha de comando com VBS > \[ *caminho para o arquivo* \] . O exemplo retornará um valor de 0 para êxito, 1 se a ajuda for invocada e 2 se o script falhar.

**cscript WiUseXfm.vbs \[ caminho para o caminho do banco de dados original para transformar opções de \] \[ \] \[ arquivo\]**

Especifique o caminho para o banco de Windows do Instalador. Especifique o caminho para o arquivo de transformação. Se o caminho para o arquivo de transformação for omitido, os dois bancos de dados serão comparados apenas. O terceiro argumento é um valor numérico opcional que especifica um conjunto de condições de erro que devem ser suprimidas. Adicione esses valores juntos para suprimir várias condições.



| Valor | Condição de erro a ser suprimida                   |
|-------|-----------------------------------------------|
| 1     | Adicionando uma linha que já existe.             |
| 2     | Excluindo uma linha que não existe.           |
| 4     | Adicionar uma tabela que já existe.           |
| 8     | Excluindo uma tabela que não existe.         |
| 16    | Atualizando uma linha que não existe.           |
| 256   | Incompatibilidade de páginas de código de banco de dados e transformação. |



 

Para obter exemplos de script adicionais, [consulte exemplos Windows script do instalador.](windows-installer-scripting-examples.md) Para ver os utilitários de exemplo que não exigem Windows host de script, consulte Windows ferramentas de [desenvolvimento do instalador.](windows-installer-development-tools.md)

 

 



