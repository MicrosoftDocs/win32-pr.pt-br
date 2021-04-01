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
# <a name="receiving-an-enveloped-data-message"></a><span data-ttu-id="f9d82-103">Recebendo uma mensagem de dados envelopada</span><span class="sxs-lookup"><span data-stu-id="f9d82-103">Receiving an Enveloped Data Message</span></span>

<span data-ttu-id="f9d82-104">\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="f9d82-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="f9d82-105">Em vez disso, use o .NET Framework para implementar recursos de segurança.</span><span class="sxs-lookup"><span data-stu-id="f9d82-105">Instead, use the .NET Framework to implement security features.</span></span> <span data-ttu-id="f9d82-106">Para obter mais informações, consulte [alternativas ao uso do CApicom](alternatives-to-using-capicom.md).\]</span><span class="sxs-lookup"><span data-stu-id="f9d82-106">For more information, see [Alternatives to Using CAPICOM](alternatives-to-using-capicom.md).\]</span></span>

<span data-ttu-id="f9d82-107">Para descriptografar uma mensagem envelopada, o destinatário corresponde a um [*certificado*](../secgloss/c-gly.md) do meu repositório que tem uma chave privada disponível com um certificado na mensagem envelopada.</span><span class="sxs-lookup"><span data-stu-id="f9d82-107">To decrypt an enveloped message, the recipient matches a [*certificate*](../secgloss/c-gly.md) from the My store that has an available private key with a certificate in the enveloped message.</span></span> <span data-ttu-id="f9d82-108">Se uma correspondência for encontrada, a chave criptografada associada a esse certificado será descriptografada e essa chave descriptografada será usada para descriptografar a mensagem envelopada.</span><span class="sxs-lookup"><span data-stu-id="f9d82-108">If a match is found, the encrypted key associated with that certificate is decrypted and that decrypted key is used to decrypt the enveloped message.</span></span> <span data-ttu-id="f9d82-109">Um destinatário de mensagem que não tem um certificado correspondente com uma chave privada disponível não pode descriptografar a mensagem.</span><span class="sxs-lookup"><span data-stu-id="f9d82-109">A message recipient that does not have a matching certificate with an available private key cannot decrypt the message.</span></span>

<span data-ttu-id="f9d82-110">No exemplo a seguir, um nome de arquivo é passado para a sub-rotina, esse arquivo é aberto e uma mensagem envelopada é lida em.</span><span class="sxs-lookup"><span data-stu-id="f9d82-110">In the example that follows, a file name is passed into the subroutine, that file is opened and an enveloped message is read in.</span></span> <span data-ttu-id="f9d82-111">A mensagem envelopada é descriptografada.</span><span class="sxs-lookup"><span data-stu-id="f9d82-111">The enveloped message is then decrypted.</span></span> <span data-ttu-id="f9d82-112">As etapas de correspondência de um certificado de usuário com um certificado na mensagem envelopada, da descriptografia da chave de criptografia e, por fim, da descriptografia da mensagem são todas feitas nos bastidores.</span><span class="sxs-lookup"><span data-stu-id="f9d82-112">The steps of matching a user certificate with a certificate in the enveloped message, of decrypting the encryption key, and finally of decrypting the message are all done behind the scenes.</span></span> <span data-ttu-id="f9d82-113">Um erro será gerado se uma correspondência de certificado não for encontrada ou se a descriptografia falhar.</span><span class="sxs-lookup"><span data-stu-id="f9d82-113">An error is raised if a certificate match is not found or if the decryption fails.</span></span>

<span data-ttu-id="f9d82-114">Em qualquer erro de CAPICOM, um valor decimal negativo de **Err. Number** é retornado.</span><span class="sxs-lookup"><span data-stu-id="f9d82-114">On any CAPICOM error, a negative decimal value of **Err.Number** is returned.</span></span> <span data-ttu-id="f9d82-115">Para obter mais informações, [**consulte \_ \_ código de erro CAPICOM**](capicom-error-code.md).</span><span class="sxs-lookup"><span data-stu-id="f9d82-115">For more information, see [**CAPICOM\_ERROR\_CODE**](capicom-error-code.md).</span></span> <span data-ttu-id="f9d82-116">Para obter informações sobre valores decimais positivos de **Err. Number**, consulte Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="f9d82-116">For information about positive decimal values of **Err.Number**, see Winerror.h.</span></span>


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



 

 
