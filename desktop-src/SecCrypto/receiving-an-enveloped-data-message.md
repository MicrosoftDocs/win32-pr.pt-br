---
description: Para descriptografar uma mensagem envelopada, o destinatário corresponde a um certificado do meu repositório que tem uma chave privada disponível com um certificado na mensagem envelopada.
ms.assetid: 536f9977-102c-4df9-9d07-97b4b434b845
title: Recebendo uma mensagem de dados envelopada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d32276193e8fd03904aed1ad626cd3ed241c654
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103836981"
---
# <a name="receiving-an-enveloped-data-message"></a>Recebendo uma mensagem de dados envelopada

\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP. Em vez disso, use o .NET Framework para implementar recursos de segurança. Para obter mais informações, consulte [alternativas ao uso do CApicom](alternatives-to-using-capicom.md).\]

Para descriptografar uma mensagem envelopada, o destinatário corresponde a um [*certificado*](../secgloss/c-gly.md) do meu repositório que tem uma chave privada disponível com um certificado na mensagem envelopada. Se uma correspondência for encontrada, a chave criptografada associada a esse certificado será descriptografada e essa chave descriptografada será usada para descriptografar a mensagem envelopada. Um destinatário de mensagem que não tem um certificado correspondente com uma chave privada disponível não pode descriptografar a mensagem.

No exemplo a seguir, um nome de arquivo é passado para a sub-rotina, esse arquivo é aberto e uma mensagem envelopada é lida em. A mensagem envelopada é descriptografada. As etapas de correspondência de um certificado de usuário com um certificado na mensagem envelopada, da descriptografia da chave de criptografia e, por fim, da descriptografia da mensagem são todas feitas nos bastidores. Um erro será gerado se uma correspondência de certificado não for encontrada ou se a descriptografia falhar.

Em qualquer erro de CAPICOM, um valor decimal negativo de **Err. Number** é retornado. Para obter mais informações, [**consulte \_ \_ código de erro CAPICOM**](capicom-error-code.md). Para obter informações sobre valores decimais positivos de **Err. Number**, consulte Winerror. h.


```VB
Sub ReceiveMessage(ByVal InFile As String)
On Error GoTo ErrorHandler

'Declare an EnvelopedData object

Dim Envmessage As New EnvelopedData

'Declare a string variable to hold the encrypted message.

Dim Encrypted As String

' Open an input file and read in the encrypted message
Open InFile For Input As #1
Input #1, Encrypted
Close #1

' If the length of the input string is greater than 0, 
' an encrypted message string is available. Decrypt the message.
' Note: to decrypt the message, a certificate with access to
' a user's private key must be available, and that certificate must
' match one of the certificates in the Recipients collection of 
' certificates.
If Len(Encrypted) > 0 Then
    ' Receive and decrypt the message
    Envmessage.Decrypt encrypted
    
    ' Display the decrypted message.
    MsgBox Envmessage.Content
Else
    MsgBox "No enveloped message was read in."
End If
' Release the EncryptedData object.
Set Envmessage = Nothing
Exit Sub

ErrorHandler:
If Err.Number > 0 Then
    MsgBox "Visual Basic error found:" & Err.Description
Else
    MsgBox "CAPICOM error found : " & Err.Number
End If
End Sub
```



 

 
