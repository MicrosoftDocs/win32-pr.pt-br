---
description: O arquivo VBScript WiLstScr.vbs é fornecido nos componentes do SDK do Windows para desenvolvedores Windows instaladores. Este script de exemplo demonstra o Windows visualizador de script do instalador.
ms.assetid: 18989c16-e0c8-4d11-b915-730951b6845b
title: Exibir script do instalador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4797d73c4c90266b94a02b9d73657fb95de75e153617ef1e34797f28035ee701
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117803977"
---
# <a name="view-installer-script"></a>Exibir script do instalador

O arquivo VBScript WiLstScr.vbs é fornecido nos componentes [do SDK do Windows para desenvolvedores Windows instalador.](platform-sdk-components-for-windows-installer-developers.md) Este script de exemplo demonstra o Windows visualizador de script do instalador.

O exemplo demonstra o uso de:

-   [**Método OpenDatabase (Objeto do Instalador)**](installer-opendatabase.md)
-   [**Método LastErrorRecord**](installer-lasterrorrecord.md) do [**objeto Installer**](installer-object.md)
-   [**Método OpenView**](database-openview.md) do objeto [**Database**](database-object.md)
-   [**Método Fetch**](view-fetch.md) do [**objeto View**](view-object.md)
-   [**Método FormatText**](record-formattext.md)
-   [**Propriedade FieldCount**](record-fieldcount.md)
-   [**Propriedade StringData**](record-stringdata.md) do [**objeto Record**](record-object.md)
-   [\_Tabela TransformView](-transformview-table.md)

Usar este exemplo requer a CScript.exe do host Windows Script. Para usar CScript.exe executar este exemplo, digite um comando no prompt de comando usando a sintaxe a seguir. A ajuda será exibida se o primeiro argumento for /? ou se poucos argumentos são especificados. Para redirecionar a saída para um arquivo, end end the command line with VBS > \[ *path to file* \] . O exemplo retornará um valor de 0 para êxito, 1 se a ajuda for invocada e 2 se o script falhar.

**cscript WiLstScr.vbs** *\[ caminho para Windows de execução do \] instalador*

Especifique o caminho para o script de execução do instalador.

Para obter exemplos de script adicionais, [consulte exemplos Windows script do instalador.](windows-installer-scripting-examples.md) Para ver os utilitários de exemplo que não exigem Windows Host de Script, consulte Windows Ferramentas de Desenvolvimento [do Instalador](windows-installer-development-tools.md)do .

 

 



