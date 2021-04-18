---
description: O arquivo VBScript WiLstScr.vbs é fornecido nos componentes SDK do Windows para os desenvolvedores de Windows Installer. Este exemplo de script demonstra o Windows Installer Visualizador de script.
ms.assetid: 18989c16-e0c8-4d11-b915-730951b6845b
title: Exibir o script do instalador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56888f478bb7cdd43ebcee817c86f6f9f163840e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105778551"
---
# <a name="view-installer-script"></a>Exibir o script do instalador

O arquivo VBScript WiLstScr.vbs é fornecido nos [componentes SDK do Windows para os desenvolvedores de Windows Installer](platform-sdk-components-for-windows-installer-developers.md). Este exemplo de script demonstra o Windows Installer Visualizador de script.

O exemplo demonstra o uso de:

-   [**Método OpenDatabase (objeto instalador)**](installer-opendatabase.md)
-   Método [**LastErrorRecord**](installer-lasterrorrecord.md) do objeto do [**instalador**](installer-object.md)
-   Método [**OpenView**](database-openview.md) do objeto [**Database**](database-object.md)
-   Método [**Fetch**](view-fetch.md) do objeto [**View**](view-object.md)
-   Método [**FormatText**](record-formattext.md)
-   Propriedade [**FieldCount**](record-fieldcount.md)
-   Propriedade [**StringData**](record-stringdata.md) do objeto [**Record**](record-object.md)
-   [\_Tabela de transformview](-transformview-table.md)

O uso deste exemplo requer a versão CScript.exe do Windows Script Host. Para usar CScript.exe para executar este exemplo, digite um comando no prompt de comando usando a sintaxe a seguir. A ajuda será exibida se o primeiro argumento for/? ou se poucos argumentos forem especificados. Para redirecionar a saída para um arquivo, termine a linha de comando com VBS > \[ *caminho para o arquivo* \] . O exemplo retorna um valor de 0 para êxito, 1 se a ajuda for invocada e 2 se o script falhar.

**cscript WiLstScr.vbs** *\[ caminho para Windows Installer \] script de execução*

Especifique o caminho para o script de execução do instalador.

Para obter exemplos de script adicionais, consulte [Windows Installer exemplos de script](windows-installer-scripting-examples.md). Para utilitários de exemplo que não exigem o Windows Script Host, consulte [Windows Installer ferramentas de desenvolvimento](windows-installer-development-tools.md).

 

 



