---
description: O arquivo VBScript WiDiffDb.vbs é fornecido nos componentes SDK do Windows para os desenvolvedores de Windows Installer. Esse script de exemplo gera um arquivo de transformação temporário entre dois bancos de dados do Windows Installer e exibe a transformação.
ms.assetid: 9750ddc6-de8d-48e9-a984-892f0cf4ac3b
title: Exibir diferenças entre dois bancos de dados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b0c97afc0bd7145170209ed87497b6af90e64d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501596"
---
# <a name="view-differences-between-two-databases"></a>Exibir diferenças entre dois bancos de dados

O arquivo VBScript WiDiffDb.vbs é fornecido nos [componentes SDK do Windows para os desenvolvedores de Windows Installer](platform-sdk-components-for-windows-installer-developers.md). Esse script de exemplo gera um arquivo de transformação temporário entre dois bancos de dados do Windows Installer e exibe a transformação.

O exemplo demonstra o uso de:

-   [**Método OpenDatabase (objeto instalador)**](installer-opendatabase.md)
-   [**Método LastErrorRecord**](installer-lasterrorrecord.md) do [ **objeto do instalador**](installer-object.md)
-   [**Método OpenView**](database-openview.md)
-   [**Propriedade SummaryInformation (objeto Database)**](database-summaryinformation.md)
-   [**Método GenerateTransform**](database-generatetransform.md)
-   [**Método ApplyTransform**](database-applytransform.md)
-   [**Objeto de banco de dados**](database-object.md)
-   [**Método FETCH**](view-fetch.md) do [ **objeto View**](view-object.md)
-   [**Propriedade IsNull**](record-isnull.md)
-   [**Propriedade StringData**](record-stringdata.md) do [ **objeto Record**](record-object.md)
-   [\_Tabela de transformview](-transformview-table.md)

O uso deste exemplo requer a versão CScript.exe do Windows Script Host. Para usar CScript.exe para executar este exemplo, digite um comando no prompt de comando usando a sintaxe a seguir. A ajuda será exibida se o primeiro argumento for/? ou se poucos argumentos forem especificados. Para redirecionar a saída para um arquivo, termine a linha de comando com VBS > \[ *caminho para o arquivo* \] . O exemplo retorna um valor de 0 para êxito, 1 se a ajuda for invocada e 2 se o script falhar.

**cscript WiDiffDb.vbs** *\[ caminho do caminho do banco de dados original \] \[ para o banco de dados \] revisado*

Especifique o caminho para o banco de dados de Windows Installer original. Especifique o caminho para o banco de dados revisado. O script de exemplo exibirá a transformação.

Para obter exemplos de script adicionais, consulte [Windows Installer exemplos de script](windows-installer-scripting-examples.md). Para utilitários de exemplo que não exigem o Windows Script Host, consulte [Windows Installer ferramentas de desenvolvimento](windows-installer-development-tools.md).

 

 



