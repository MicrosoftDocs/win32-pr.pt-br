---
description: Essa sub-rotina leva uma cadeia de caracteres de senha a ser usada para gerar uma chave de criptografia de sessão e o nome de um arquivo do qual uma mensagem criptografada será lida. Todos os parâmetros são passados para a sub-rotina por valores.
ms.assetid: 70f23d93-2bca-419b-9de7-e52ce4fb1350
title: Descriptografando uma mensagem no CAPICOM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 744878378fbe2791e66151e451029be8adde2435b451d540196a1082c4e005f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117767754"
---
# <a name="decrypting-a-message-in-capicom"></a>Descriptografando uma mensagem no CAPICOM

\[CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP. Em vez disso, use o .NET Framework para implementar recursos de segurança. Para obter mais informações, [consulte Alternativas ao uso de CAPICOM.](alternatives-to-using-capicom.md)\]

Essa sub-rotina leva uma cadeia de caracteres de senha a ser usada para gerar uma chave de criptografia de sessão e o nome de um arquivo do qual uma mensagem criptografada será lida. Todos os parâmetros são passados para a sub-rotina por valores.

> [!Note]  
> CAPICOM não dá suporte ao tipo de conteúdo PKCS 7 EncryptedData, mas usa uma estrutura ASN não padrão \# para EncryptedData. Portanto, somente CAPICOM pode descriptografar um objeto CAPICOM EncryptedData.

 

Se a descriptografia falhar, o valor **Err.Number** será verificado para determinar se o erro foi causado pelo uso de uma senha que não corresponder à senha usada para criptografar a mensagem. Nesse caso, o erro NTE \_ BAD \_ DATA é retornado.

Em qualquer erro CAPICOM, um valor decimal negativo de **Err.Number** é retornado. Para obter mais informações, consulte [**CAPICOM \_ ERROR \_ CODE**](capicom-error-code.md). Para obter informações sobre valores decimais positivos de **Err.Number,** consulte Winerror.h.


```VB
Sub DecryptMessage(ByVal hidden As String, ByVal filename As String)
On Error goto ErrorHandler

'Declare an EncryptedData object

Dim message As New EncryptedData

'Declare a string variable to hold the encrypted message.
Dim encrypted As String

' Open an input file and read in the encrypted message
Open filename For Input As #1
Input #1, encrypted
Close #1

' If a message was read in (the length of the input string is 
' greater than 0), set the password and decrypt the message.
If Len(encrypted) > 0 then
    ' Set the password used to generate the key
    ' used to decrypt the message. If the password
    ' not the same as the password used when the message
    ' was encrypted, decryption will fail.
    ' The algorithm name and key length set in the encrypting
    ' process are automatically used to decrypt the message. 
    message.SetSecret hidden
    message.Decrypt encrypted
    ' Display the decrypted message.
    MsgBox message.Content
else
    msgbox "No encrypted message was read in.
endif

' Release the EncryptedData object and exit the subroutine.
Set message = Nothing
Exit Sub

ErrorHandler:
If Err.Number > 0 Then
    MsgBox "Visual Basic error found:" & Err.Description
Else
'    Check for a bad password error.
    If Err.Number = -2146893819 Then
        MsgBox "Error. The password may not be correct."
    Else
        MsgBox "CAPICOM error found : " & Err.Number
    End If
End If
End Sub
```



 

 



