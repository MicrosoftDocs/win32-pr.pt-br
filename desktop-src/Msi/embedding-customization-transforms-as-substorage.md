---
description: Você pode armazenar a transformação personalização em um armazenamento do pacote de Windows Installer para garantir que a transformação esteja sempre disponível quando o pacote de instalação estiver disponível.
ms.assetid: d4c022d2-a8c4-4b4e-8a6c-b14e1bc6effe
title: Incorporando transformações de personalização como subarmazenamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfd275d36b37b2e29ae166a2a464a62495d2ca9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105750245"
---
# <a name="embedding-customization-transforms-as-substorage"></a>Incorporando transformações de personalização como subarmazenamento

Você pode armazenar a transformação personalização em um armazenamento do pacote de Windows Installer para garantir que a transformação esteja sempre disponível quando o pacote de instalação estiver disponível. Consulte [transformações incorporadas](embedded-transforms.md). Um exemplo disso é fornecido no SDK do Windows Installer como o WiSubStg.vbs do utilitário. O trecho a seguir, Emb.vbs, também ilustra o uso da [tabela de armazenamentos](-storages-table.md) para adicionar uma transformação inserida e é para uso com o Windows Script Host.


```VB
'Emb.vbs. Argument(0) is the original database. Argument(1) is the
'    path to the transform file. Argument(2) is the name of the storage.
'
Option Explicit

' Check arguments
If WScript.Arguments.Count < 2 Then
 WScript.Echo "Usage is emb.vbs [original database] [transform] [storage name]"
 WScript.Quit(1)
End If

' Connect to Windows Installer object
On Error Resume Next
Dim installer : Set installer = Nothing
Set installer = Wscript.CreateObject("WindowsInstaller.Installer")
 
' Evaluate command-line arguments and set open and update modes
Dim databasePath: databasePath = Wscript.Arguments(0)
Dim importPath  : importPath = Wscript.Arguments(1)
Dim storageName : storageName = Wscript.Arguments(2)
 
' Open database and create a view on the _Storages table
Dim sqlQuery : sqlQuery = "SELECT `Name`,`Data` FROM _Storages"
Dim database : Set database = installer.OpenDatabase(databasePath, 1)
Dim view     : Set view = database.OpenView(sqlQuery)
 
'Create and Insert the row.
Dim record   : Set record = installer.CreateRecord(2)
record.StringData(1) = storageName
view.Execute record
 
'Insert storage - copy data into stream
record.SetStream 2, importPath
view.Modify 3, record
database.Commit
Set view = Nothing
Set database = Nothing
```



Para adicionar um armazenamento chamado MNPtrans1 ao MNP2000.msi e que contém a transformação criada na [adição de informações resumidas à transformação personalização](adding-summary-information-to-customization-transform.md), altere os diretórios para a pasta que contém Emb.vbs, o banco de dados original e o arquivo de transformação e, em seguida, insira a linha de comando a seguir.

**Cscript.exe Emb.vbs MNP2000.msi MNPtrans. MST MNPtrans1**

Isso conclui o exemplo de transformação personalização. Depois de inserir a transformação em MNPtrans. MST, a transformação estará sempre disponível com o pacote de instalação. O arquivo MNPtrans. MST não precisa estar localizado na origem para aplicar a transformação.

Remova MNPtrans. MST da pasta que contém o pacote de instalação de exemplo. Clique no ícone de MNP2000.msi para iniciar uma instalação ou use a seguinte linha de comando.

**msiexec/i MNP2000.msi**

Observe que isso instala o produto sem as personalizações. Para instalar o com as personalizações, insira a linha de comando a seguir. Use dois-pontos para indicar que o valor da propriedade [**TRANSformações**](transforms.md) se refere a uma transformação inserida.

msiexec/i MNP2000.msi transformações =: MNPtrans1

Observe que o recurso de portão não aparece na árvore de seleção de recursos e que os componentes do recurso de portão não são instalados mesmo que um tipo completo de instalação seja selecionado na interface do usuário.

## <a name="next-example"></a>Próximo exemplo

[Um exemplo de aplicação de patch de atualização pequena](a-small-update-patching-example.md)

 

 



