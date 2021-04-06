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
# <a name="verifying-the-signature-on-a-document"></a><span data-ttu-id="f4003-103">Verificando a assinatura em um documento</span><span class="sxs-lookup"><span data-stu-id="f4003-103">Verifying the Signature on a Document</span></span>

<span data-ttu-id="f4003-104">\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="f4003-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="f4003-105">Em vez disso, use o .NET Framework para implementar recursos de segurança.</span><span class="sxs-lookup"><span data-stu-id="f4003-105">Instead, use the .NET Framework to implement security features.</span></span> <span data-ttu-id="f4003-106">Para obter mais informações, consulte [alternativas ao uso do CApicom](alternatives-to-using-capicom.md).\]</span><span class="sxs-lookup"><span data-stu-id="f4003-106">For more information, see [Alternatives to Using CAPICOM](alternatives-to-using-capicom.md).\]</span></span>

<span data-ttu-id="f4003-107">Quando um documento assinado é recebido, a validade da assinatura ou das assinaturas pode ser verificada.</span><span class="sxs-lookup"><span data-stu-id="f4003-107">When a signed document is received, the validity of the signature or signatures can be checked.</span></span> <span data-ttu-id="f4003-108">Uma assinatura pode ser verificada:</span><span class="sxs-lookup"><span data-stu-id="f4003-108">A signature can be checked for:</span></span>

-   <span data-ttu-id="f4003-109">Validade do hash de assinatura</span><span class="sxs-lookup"><span data-stu-id="f4003-109">Validity of the signature hash</span></span>
-   <span data-ttu-id="f4003-110">Validade do certificado do signatário</span><span class="sxs-lookup"><span data-stu-id="f4003-110">Validity of the signer's certificate</span></span>

<span data-ttu-id="f4003-111">O [*hash*](../secgloss/h-gly.md) de assinatura é descriptografado usando a [*chave pública*](../secgloss/p-gly.md) do assinante encontrado no [*certificado*](../secgloss/c-gly.md)do signatário, incluído como parte da assinatura.</span><span class="sxs-lookup"><span data-stu-id="f4003-111">The signature [*hash*](../secgloss/h-gly.md) is decrypted using the [*public key*](../secgloss/p-gly.md) of the signer found on the signer's [*certificate*](../secgloss/c-gly.md), included as part of the signature.</span></span> <span data-ttu-id="f4003-112">Se a assinatura descriptografada corresponder a um novo hash do documento original, a assinatura foi criada pelo proprietário da chave privada associada à chave pública usada para descriptografar o hash.</span><span class="sxs-lookup"><span data-stu-id="f4003-112">If the decrypted signature matches a new hash of the original document, the signature was created by the owner of the private key associated with the public key used to decrypt the hash.</span></span> <span data-ttu-id="f4003-113">Além disso, o documento no qual a assinatura se baseia é garantido que não foi alterado após a criação da assinatura.</span><span class="sxs-lookup"><span data-stu-id="f4003-113">In addition, the document that the signature is based on is guaranteed not to have been changed after the signature was created.</span></span>

<span data-ttu-id="f4003-114">O certificado que forneceu a chave pública e a identidade do signatário também pode ser verificado quanto à validade, incluindo problemas como se o certificado foi revogado, se o certificado está desatualizado ou se o certificado foi emitido por um emissor de certificado confiável.</span><span class="sxs-lookup"><span data-stu-id="f4003-114">The certificate that provided the public key and the identity of the signer can also be checked for validity including such issues as whether the certificate has been revoked, whether the certificate is out of date, or whether the certificate was issued by a trusted certificate issuer.</span></span>

<span data-ttu-id="f4003-115">No exemplo a seguir, o conteúdo assinado e o objeto **SignedData** são lidos em um arquivo e a assinatura, e a validade do certificado usado para criar a assinatura é verificada.</span><span class="sxs-lookup"><span data-stu-id="f4003-115">In the following example, the content signed and the **SignedData** object are read in from a file and the signature and the validity of the certificate used to create the signature are checked.</span></span>

> [!Note]  
> <span data-ttu-id="f4003-116">Se a assinatura não for criptograficamente válida ou o certificado do assinante não for válido, uma exceção será gerada e o programa de verificação deverá tratar a exceção.</span><span class="sxs-lookup"><span data-stu-id="f4003-116">If the signature is not cryptographically valid or the certificate of the signer is not valid, an exception is raised and the verifying program must handle the exception.</span></span> <span data-ttu-id="f4003-117">Em qualquer erro de CAPICOM, um valor decimal negativo de **Err. Number** é retornado.</span><span class="sxs-lookup"><span data-stu-id="f4003-117">On any CAPICOM error, a negative decimal value of **Err.Number** is returned.</span></span> <span data-ttu-id="f4003-118">Para obter mais informações, [**consulte \_ \_ código de erro CAPICOM**](capicom-error-code.md).</span><span class="sxs-lookup"><span data-stu-id="f4003-118">For more information, see [**CAPICOM\_ERROR\_CODE**](capicom-error-code.md).</span></span> <span data-ttu-id="f4003-119">Para obter informações sobre valores decimais positivos de **Err. Number**, consulte Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="f4003-119">For information about positive decimal values of **Err.Number**, see Winerror.h.</span></span>

 


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



 

 
