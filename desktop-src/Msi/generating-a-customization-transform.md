---
description: Você pode gerar um arquivo de transformação usando MsiDatabaseGenerateTransform ou o método GenerateTransform do objeto Database.
ms.assetid: c016fcba-0d54-4b99-bcdd-36967b2c9da0
title: Gerando uma transformação de personalização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b790917100cc06da97e09fd8aabf45b580e62008d23c9fc5065e6005112d8d4e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118635994"
---
# <a name="generating-a-customization-transform"></a>Gerando uma transformação de personalização

Você pode gerar um arquivo de transformação usando [**MsiDatabaseGenerateTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegeneratetransforma) ou o [**método GenerateTransform**](database-generatetransform.md) do [**objeto Database**](database-object.md). um exemplo disso é fornecido no SDK do Windows Installer como o WiGenXfm.vbs do utilitário. o trecho a seguir, Gen.vbs, também ilustra o método de **transformação** e é para uso com Windows Host de Script.


```VB
'Gen.vbs. Argument(0) is the original database. Argument(1) is the
'    customized database. Argument(2) is the transform file.
 
Option Explicit

' Check arguments
If WScript.Arguments.Count < 2 Then
    WScript.Echo "Usage is gen.vbs [original database] [customized database] [transform file]"
    WScript.Quit(1)
End If

' Connect to Windows Installer object
On Error Resume Next
Dim installer : Set installer = Nothing
Set installer = Wscript.CreateObject("WindowsInstaller.Installer") 
' Open databases
Dim database1 : Set database1 = 
    installer.OpenDatabase(Wscript.Arguments(0), 0) 
Dim database2 : Set database2 = 
    installer.OpenDatabase(Wscript.Arguments(1), 0) 
' Generate transform
Dim transform : transform = Database2.GenerateTransform(Database1,
    Wscript.Arguments(2))
```



Para gerar o arquivo de transformação MNPtrans. MST do banco de dados MNP2000.msi original e o banco de dados de MNP2000t.msi que você modificou na [personalização de um banco de dados original](customizing-an-original-database.md), altere os diretórios para a pasta que contém Gen.vbs, o banco de dados original e o banco de dados do instalador atualizado e insira a linha de comando a seguir.

**Cscript.exe Gen.vbs MNP2000.msi MNP2000t.msi MNPtrans. MST**

[Continuar](adding-summary-information-to-customization-transform.md)

 

 



