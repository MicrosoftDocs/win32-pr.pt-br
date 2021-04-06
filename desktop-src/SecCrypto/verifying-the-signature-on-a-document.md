---
description: Quando um documento assinado é recebido, a validade da assinatura ou das assinaturas pode ser verificada.
ms.assetid: 088915d8-768c-4378-a9dd-9347a428aff9
title: Verificando a assinatura em um documento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f2886edcb9629011ddf1a0b5fb45a12a11f0556
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828555"
---
# <a name="verifying-the-signature-on-a-document"></a>Verificando a assinatura em um documento

\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP. Em vez disso, use o .NET Framework para implementar recursos de segurança. Para obter mais informações, consulte [alternativas ao uso do CApicom](alternatives-to-using-capicom.md).\]

Quando um documento assinado é recebido, a validade da assinatura ou das assinaturas pode ser verificada. Uma assinatura pode ser verificada:

-   Validade do hash de assinatura
-   Validade do certificado do signatário

O [*hash*](../secgloss/h-gly.md) de assinatura é descriptografado usando a [*chave pública*](../secgloss/p-gly.md) do assinante encontrado no [*certificado*](../secgloss/c-gly.md)do signatário, incluído como parte da assinatura. Se a assinatura descriptografada corresponder a um novo hash do documento original, a assinatura foi criada pelo proprietário da chave privada associada à chave pública usada para descriptografar o hash. Além disso, o documento no qual a assinatura se baseia é garantido que não foi alterado após a criação da assinatura.

O certificado que forneceu a chave pública e a identidade do signatário também pode ser verificado quanto à validade, incluindo problemas como se o certificado foi revogado, se o certificado está desatualizado ou se o certificado foi emitido por um emissor de certificado confiável.

No exemplo a seguir, o conteúdo assinado e o objeto **SignedData** são lidos em um arquivo e a assinatura, e a validade do certificado usado para criar a assinatura é verificada.

> [!Note]  
> Se a assinatura não for criptograficamente válida ou o certificado do assinante não for válido, uma exceção será gerada e o programa de verificação deverá tratar a exceção. Em qualquer erro de CAPICOM, um valor decimal negativo de **Err. Number** é retornado. Para obter mais informações, [**consulte \_ \_ código de erro CAPICOM**](capicom-error-code.md). Para obter informações sobre valores decimais positivos de **Err. Number**, consulte Winerror. h.

 


```VB
Sub VerifySig(ByVal FileToVerify As String, ByVal FileBase As String)
On Error GoTo ErrorHandler

Dim sdContent As String
Dim sdCheck As String
Dim mySD As SignedData
Set mySD = New SignedData

' Open a file and read the signature.
Open FileToVerify For Input As #1
Input #1, sdCheck
Close #1

' Open a file and input the plaintext content that was signed.
Open FileBase For Input As #2
Input #2, sdContent
Close #1

' Set the detached content upon which the signature is based.
mySD.Content = sdContent

' Verify the detached signature.
On Error Resume Next
    mySD.Verify sdCheck, True
If Err.Number <> 0 Then
    MsgBox "Signature verification failed. " & Err.Description
Else
    MsgBox "Verification complete."
End If

' Release the SignedData object.
Set mySD = Nothing

Exit Sub
ErrorHandler:
    If Err.Number > 0 Then
        MsgBox "Visual Basic error found: " & Err.Description
    Else
        MsgBox "CAPICOM error found: " & Hex(Err.Number)
    End If
End Sub

```



 

 
