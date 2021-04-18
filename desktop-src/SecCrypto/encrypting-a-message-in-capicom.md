---
description: Essa sub-rotina usa uma cadeia de caracteres a ser criptografada, uma cadeia de caracteres de senha a ser usada para gerar uma chave de criptografia e o nome de um arquivo em que a mensagem criptografada será gravada.
ms.assetid: 9ad3199a-bca1-4990-80da-80744e349047
title: Criptografando uma mensagem no CAPICOM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8039586736c09673644cacc90759e8d5f25b6e1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105756682"
---
# <a name="encrypting-a-message-in-capicom"></a>Criptografando uma mensagem no CAPICOM

\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP. Em vez disso, use o .NET Framework para implementar recursos de segurança. Para obter mais informações, consulte [alternativas ao uso do CApicom](alternatives-to-using-capicom.md).\]

Essa sub-rotina usa uma cadeia de caracteres a ser criptografada, uma cadeia de caracteres de senha a ser usada para gerar uma chave de criptografia e o nome de um arquivo em que a mensagem criptografada será gravada. Todos os parâmetros são passados para a sub-rotina por valores. Para descriptografar a mensagem, a mesma cadeia de caracteres de senha deve ser usada. Se a senha for perdida, o texto não poderá ser descriptografado. A privacidade da mensagem será perdida se um destinatário indesejado obtiver acesso à senha.

> [!Note]  
> O CAPICOM não oferece suporte ao \# tipo de conteúdo ENCRYPTEDDATA PKCS 7, mas usa uma estrutura ASN não padrão para EncryptedData. Como resultado, somente o capicor pode descriptografar um objeto capicot EncryptedData.

 

Em qualquer erro de CAPICOM, um valor decimal negativo da propriedade **Err. Number** é retornado. Para obter mais informações, [**consulte \_ \_ código de erro CAPICOM**](capicom-error-code.md). Para obter informações sobre valores decimais positivos de **Err. Number**, consulte Winerror. h.


```VB
Sub EncryptMessage(ByVal TobeEncrypted As String, ByVal hidden _
    As String, ByVal filename As String)

    On Error GoTo ErrorHandler

    ' Declare and initialize an EncryptedData object.
    ' Algorithm.Name and KeyLength do not need to be set.

    Dim message As New EncryptedData
    message.Content = Tobeencrypted
    message.SetSecret(hidden)
    ' Optionally, the encryption algorithm and key length can be set.
    ' If these properties are not set, the default algorithm and key 
    ' length are used.
    ' Information about the algorithm and key length is saved with 
    ' the encrypted string and the individual decrypting the message
    ' does not need to set these properties.

    message.Algorithm.Name = CAPICOM_ENCRYPTION_ALGORITHM_DES

    ' Declare the string that will hold the encrypted message.

    Dim encryptedmessage As String

    ' Encrypt the message storing the result in the encryptedmessage
    ' string.
    encryptedmessage = message.Encrypt

    ' Optionally, check the length of the encrypted string to 
    ' make sure that the encrypt method worked. 

    If Len(encryptedmessage) < 1 Then
        MsgBox("no message encrypted. ")
    Else
        MsgBox(" Message is " & Len(encryptedmessage) & " characters")

        ' Open an output file and write the encrypted message to the
        ' file. The file is not opened if there is no message
        ' to write.
    Open filename For Output As #1
    Write #1, encryptedmessage
    Close #1
        MsgBox("Encrypted message written to file ")
    End If

    ' Release the EncryptedData object.
    message = Nothing

    Exit Sub

ErrorHandler:
    If Err.Number > 0 Then
        MsgBox("Visual Basic error found:" & Err.Description)
    Else
        MsgBox("CAPICOM error found : " & Err.Number)
    End If
End Sub
```



 

 



