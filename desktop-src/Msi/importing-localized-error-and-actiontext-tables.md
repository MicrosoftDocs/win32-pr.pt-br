---
description: As versões de idioma localizadas da tabela de erros e da tabela ActionText são fornecidas pelo SDK do Windows Installer. As versões do idioma francês dessas tabelas, Error. FRA e ActionTe. FRA, estão localizadas na pasta intl do SDK do Windows Installer.
ms.assetid: 8de687c8-c7da-497e-8a90-2404096ad100
title: Importando tabelas de erro e ActionText localizadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15d48a68ca1053a1a1c66899a17802ac337c3ba2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105752042"
---
# <a name="importing-localized-error-and-actiontext-tables"></a>Importando tabelas de erro e ActionText localizadas

As versões de idioma localizadas da tabela de [erros](error-table.md) e da [tabela ActionText](actiontext-table.md) são fornecidas pelo SDK do Windows Installer. As versões do idioma francês dessas tabelas, Error. FRA e ActionTe. FRA, estão localizadas na pasta intl do SDK do Windows Installer.

Você pode usar o editor de tabela Orca ou o utilitário Msidb.exe fornecido com o SDK para importar as versões em francês dessas tabelas para o banco de dados.

Um exemplo de como usar [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) e o [**método de importação**](database-import.md) do objeto de banco de [**dados**](database-object.md) é fornecido no SDK do Windows Installer como o WiImport.vbs do utilitário. O trecho a seguir, Imp.vbs, também ilustra o uso do método de importação e é para uso com o Windows Script Host.


```VB
'Imp.vbs. Argument(0) is the original database. Argument(1) is the
'    path of the folder containing the file to be imported. Argument(2) is the name of the file to be imported.
'
Option Explicit

' Check arguments
If WScript.Arguments.Count < 2 Then
    WScript.Echo "Usage is imp.vbs [original database] [folder path] [import file]"
    WScript.Quit(1)
End If

' Connect to Windows Installer object
On Error Resume Next
Dim installer : Set installer = Wscript.CreateObject("WindowsInstaller.Installer")
Dim databasePath : databasePath = Wscript.Arguments(0)
Dim folder : folder = Wscript.Arguments(1)
 
' Open database and process file
Dim database : Set database = installer.OpenDatabase(databasePath, 1)
Dim table : table = Wscript.Arguments(2)
database.Import folder, table 
 
' Commit database changes
database.Commit 'commit changes
Wscript.Quit 0
```



Para importar e substituir a tabela de erros com Error. FRA, você pode usar uma linha de comando como a seguinte.

**Cscript Imp.vbs MNPFren.msi C: \\ Observação \_ \\ erro francês do instalador. FRA**

Para importar e substituir a tabela ActionText por ActionTe. FRA, você pode usar uma linha de comando como a seguinte.

**Cscript Imp.vbs MNPFren.msi C: \\ Observação do \_ instalador \\ francês ActionTe. FRA**

Execute a validação novamente no MNPFren.msi conforme descrito em [Validando uma atualização de instalação](validating-an-installation-upgrade.md).

[Continuar](localizing-database-columns.md)

 

 



