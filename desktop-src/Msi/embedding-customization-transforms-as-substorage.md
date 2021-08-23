---
description: Você pode armazenar a transformação de personalização em um armazenamento do pacote Windows Installer para garantir que a transformação sempre estará disponível quando o pacote de instalação estiver disponível.
ms.assetid: d4c022d2-a8c4-4b4e-8a6c-b14e1bc6effe
title: Incorporação de transformaçãos de personalização como substoragem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 175c2bd1e52a58d6c73e1e46f8b95501b016bc0e4e1069b86c9c53f47859f20c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118946996"
---
# <a name="embedding-customization-transforms-as-substorage"></a>Incorporação de transformaçãos de personalização como substoragem

Você pode armazenar a transformação de personalização em um armazenamento do pacote Windows Installer para garantir que a transformação sempre estará disponível quando o pacote de instalação estiver disponível. Consulte [Embedded Transforms](embedded-transforms.md). Um exemplo disso é fornecido no SDK Windows Instalador do WiSubStg.vbs. O snippet a seguir, Emb.vbs, também ilustra o uso da tabela [Armazenamentos](-storages-table.md) para adicionar uma transformação inserida e é para uso com Windows Host de Script.


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



Para adicionar um armazenamento chamado MNPtrans1 ao MNP2000.msi e que [](adding-summary-information-to-customization-transform.md)contém a transformação criada em Adicionando informações resumidas à transformação personalização, altere os diretórios para a pasta que contém Emb.vbs, o banco de dados original e o arquivo de transformação e, em seguida, insira a linha de comando a seguir.

**Cscript.exe Emb.vbs MNP2000.msi MNPtrans.mst MNPtrans1**

Isso conclui o exemplo de transformação de personalização. Depois de incorporar a transformação em MNPtrans.mst, a transformação estará sempre disponível com o pacote de instalação. O arquivo MNPtrans.mst não precisa estar localizado na origem para aplicar a transformação.

Remova MNPtrans.mst da pasta que contém o pacote de instalação de exemplo. Clique no MNP2000.msi para iniciar uma instalação ou usar a linha de comando a seguir.

**msiexec /i MNP2000.msi**

Observe que isso instala o produto sem as personalizações. Para instalar com as personalizações, insira a linha de comando a seguir. Use dois-pontos para indicar que o valor da propriedade [**TRANSFORMS**](transforms.md) refere-se a uma transformação inserida.

msiexec /i MNP2000.msi TRANSFORMS=:MNPtrans1

Observe que o recurso De porta não aparece na árvore de seleção de recursos e que os componentes do recurso De porta não estão instalados, mesmo se um tipo de instalação Concluído estiver selecionado na interface do usuário.

## <a name="next-example"></a>Próximo exemplo

[Um pequeno exemplo de a patch de atualização](a-small-update-patching-example.md)

 

 



