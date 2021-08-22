---
description: O exemplo a seguir demonstra como preencher a tabela MsiDigitalCertificate e a tabela MsiDigitalSignature usando uma sub-rotina Visual Basic for Applications (VBA).
ms.assetid: 3a23a721-0672-4eac-bdf2-434282b92590
title: Como autor de uma instalação assinada totalmente verificada usando a automação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e27f1b0b90296ad92e471449213e86721482a545ff1932458b2ad6b21d47b665
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119559096"
---
# <a name="authoring-a-fully-verified-signed-installation-using-automation"></a>Como autor de uma instalação assinada totalmente verificada usando a automação

O exemplo a seguir demonstra como popular a tabela [MsiDigitalCertificate](msidigitalcertificate-table.md) e a tabela [MsiDigitalSignature](msidigitalsignature-table.md) usando uma sub-rotina Visual Basic for Applications (VBA). Para obter mais informações sobre como proteger Windows do Instalador, consulte [Diretrizes para a autorização de instalações seguras.](guidelines-for-authoring-secure-installations.md)

O [**método FileSignatureInfo**](installer-filesignatureinfo.md) retorna um SAFEARRAY de bytes. Para obter mais informações, consulte [**SafeARRAY Data Type**](/windows/win32/api/oaidl/ns-oaidl-safearray). Os dados dessa matriz devem ser convertidos em Unicode porque Visual Basic não tem uma maneira de gravar bytes diretamente em um arquivo. O [**método SetStream pode**](record-setstream.md) usar o arquivo de dados convertidos para gravar dados de fluxo em um campo de registro especificado de um objeto [**Record**](record-object.md). Observe que a conversão dos dados de byte em Unicode pode potencialmente alterar os dados e que os dados convertidos devem corresponder aos dados originais para verificação de assinatura correta. O autor do pacote deve garantir que os dados originais e convertidos corresponderem.


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



 

 
