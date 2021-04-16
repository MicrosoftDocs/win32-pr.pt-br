---
description: Os certificados podem ser recuperados de um repositório de Active Directory onde os certificados de usuários de um domínio são armazenados.
ms.assetid: 5c4d1629-88f3-41f4-afb3-7791cd590e6c
title: Abrir o armazenamento de Active Directory e recuperar certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd60c7414aaec8b069817b47fbd2493bb11d98c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105757469"
---
# <a name="opening-the-active-directory-store-and-retrieving-certificates"></a>Abrir o armazenamento de Active Directory e recuperar certificados

\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP. Em vez disso, use o .NET Framework para implementar recursos de segurança. Para obter mais informações, consulte [alternativas ao uso do CApicom](alternatives-to-using-capicom.md).\]

Os [*certificados*](../secgloss/c-gly.md) podem ser recuperados de um repositório de Active Directory onde os certificados de usuários de um domínio são armazenados. Um repositório de Active Directory só pode ser aberto no modo somente leitura e os aplicativos não podem adicionar certificados ou remover certificados de um armazenamento de Active Directory usando o CAPICOM.

Em qualquer erro de CAPICOM, um valor decimal negativo de **Err. Number** é retornado. Para obter mais informações, [**consulte \_ \_ código de erro CAPICOM**](capicom-error-code.md). Para obter informações sobre valores decimais positivos de **Err. Number**, consulte Winerror. h.

O exemplo a seguir mostra a abertura de um repositório de Active Directory e a recuperação de certificados desse repositório.


```VB
Sub OpenADStore()
        On Error GoTo ErrorHandler
        Dim mystore As Store
        Set mystore = New Store
        
        ' Put a string that represents the name of a certificate 
        ' subject in SubjectNameCn. In the following example, 
        ' the * wildcard character is used in the string so that
        ' the Active Directory store will be searched for all 
        ' certificates with a subject name beginning with 'S.'
       
        Dim SubjectNameCn As String
        ' The following uses 'cn=' and the * wildcard character.
        ' Using this string, all certificates in the Active Directory
        ' store with a subject name beginning with an 'S' would
        ' be returned.

        SubjectNameCn = "CN=S*"
        
        ' Active Directory stores can only be opened with read-only
        ' access.
        
         mystore.Open CAPICOM_ACTIVE_DIRECTORY_USER_STORE, _
              SubjectNameCn, CAPICOM_STORE_OPEN_READ_ONLY
        
        If mystore.Certificates.Count < 1 Then
               MsgBox "A certificate for " & SubjectNameCn & _
                      " was not found "
        Else
               MsgBox "The certificate has been retrieved."
        End If
        
        Set mystore = Nothing
        Exit Sub

ErrorHandler:
         
         If Err.Number > 0 Then
               MsgBox "Visual Basic error found:" & Err.Description
         Else
               MsgBox "CAPICOM error found : " & Err.Number
         End If
End Sub
```



 

 
