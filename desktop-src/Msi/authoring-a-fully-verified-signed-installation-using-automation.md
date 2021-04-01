---
description: O exemplo a seguir demonstra como preencher a tabela MsiDigitalCertificate e a tabela MsiDigitalSignature usando uma sub-rotina Visual Basic for Applications (VBA).
ms.assetid: 3a23a721-0672-4eac-bdf2-434282b92590
title: Criando uma instalação assinada totalmente verificada usando a automação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e99267feffac71401f36635c08fa7f9f6598a0c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921499"
---
# <a name="authoring-a-fully-verified-signed-installation-using-automation"></a>Criando uma instalação assinada totalmente verificada usando a automação

O exemplo a seguir demonstra como preencher a [tabela MsiDigitalCertificate](msidigitalcertificate-table.md) e a [tabela MsiDigitalSignature](msidigitalsignature-table.md) usando uma sub-rotina Visual Basic for Applications (VBA). Para obter mais informações sobre como proteger Windows Installer pacotes, consulte [diretrizes para a criação de instalações seguras](guidelines-for-authoring-secure-installations.md).

O [**método FileSignatureInfo**](installer-filesignatureinfo.md) retorna um SafeArray de bytes. Para obter mais informações, consulte o [**tipo de dados SafeArray**](/windows/win32/api/oaidl/ns-oaidl-safearray). Os dados dessa matriz devem ser convertidos em Unicode porque Visual Basic não tem uma maneira de gravar bytes diretamente em um arquivo. O [**método SetStream**](record-setstream.md) pode usar o arquivo de dados convertidos para gravar dados de fluxo em um campo de registro especificado de um [**objeto de registro**](record-object.md). Observe que a conversão dos dados de byte em Unicode pode potencialmente alterar os dados e que os dados convertidos devem corresponder aos dados originais para a verificação de assinatura correta. O autor do pacote deve garantir que a correspondência de dados original e convertida.


```VB
Sub PopulateDigitalSignature()

    Dim Installer As Object
    Dim Database As Object
    Dim x() As Byte
    
    Const szSignedCabinet = "c:\test.cab"
    Const szCertFile = "c:\temp\test.cer"
    Const szDatabase = "c:\test.msi"
        
    Set Installer = CreateObject("WindowsInstaller.Installer")
    
    x = Installer.FileSignatureInfo(szSignedCabinet, 0, msiSignatureInfoCertificate)
    
    Dim fs, ts
    Dim s As String
    Set fs = CreateObject("Scripting.FileSystemObject")
    Set ts = fs.CreateTextFile(szCertFile, True)        'Create a file
    
    s = StrConv(x, vbUnicode)
    ts.Write s
    ts.Close
        
    Set Database = Installer.OpenDatabase(szDatabase, msiOpenDatabaseModeTransact)
    Set ViewCert = Database.OpenView("SELECT * FROM `MsiDigitalCertificate`")
    ViewCert.Execute 0
    Set ViewSig = Database.OpenView("SELECT * FROM `MsiDigitalSignature`")
    ViewSig.Execute 0
    
    Set RecordCert = Installer.CreateRecord(2)
    RecordCert.StringData(1) = "Test"
    RecordCert.SetStream 2, szCertFile
    ViewCert.Modify msiViewModifyInsert, RecordCert
    
    Set RecordSig = Installer.CreateRecord(4)
    RecordSig.StringData(1) = "Media"
    RecordSig.StringData(2) = "1"
    RecordSig.StringData(3) = "Test"
    ViewSig.Modify msiViewModifyInsert, RecordSig
    
    Database.Commit
      fs.DeleteFile(szCertFile)
End Sub
```



 

 
