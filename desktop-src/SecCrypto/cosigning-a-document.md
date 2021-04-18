---
description: Um documento pode ser assinado por mais de um signatário.
ms.assetid: f81cbf7b-317d-4fab-9b30-88b6c6576db8
title: Coatribuindo um documento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa06cbbc95dc0fe558c6e704bd18102e80221dbc
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "105761868"
---
# <a name="cosigning-a-document"></a><span data-ttu-id="a5721-103">Coatribuindo um documento</span><span class="sxs-lookup"><span data-stu-id="a5721-103">Cosigning a Document</span></span>

<span data-ttu-id="a5721-104">\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a5721-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="a5721-105">Em vez disso, use o .NET Framework para implementar recursos de segurança.</span><span class="sxs-lookup"><span data-stu-id="a5721-105">Instead, use the .NET Framework to implement security features.</span></span> <span data-ttu-id="a5721-106">Para obter mais informações, consulte [alternativas ao uso do CApicom](alternatives-to-using-capicom.md).\]</span><span class="sxs-lookup"><span data-stu-id="a5721-106">For more information, see [Alternatives to Using CAPICOM](alternatives-to-using-capicom.md).\]</span></span>

<span data-ttu-id="a5721-107">Um documento pode ser assinado por mais de um signatário.</span><span class="sxs-lookup"><span data-stu-id="a5721-107">A document can be signed by more than one signer.</span></span> <span data-ttu-id="a5721-108">Isso acontece quando, por exemplo, duas ou mais partes assinam um contrato ou um relatório de despesas.</span><span class="sxs-lookup"><span data-stu-id="a5721-108">This happens when, for instance, two or more parties sign a contract or an expense report.</span></span> <span data-ttu-id="a5721-109">No exemplo a seguir, um documento já assinado é recebido por um segundo assinante.</span><span class="sxs-lookup"><span data-stu-id="a5721-109">In the following example, a document already signed is received by a second signer.</span></span> <span data-ttu-id="a5721-110">Esse signatário usa o método de [**coassinatura**](signeddata-cosign.md) para anexar uma assinatura adicional ao documento.</span><span class="sxs-lookup"><span data-stu-id="a5721-110">This signer uses the [**CoSign**](signeddata-cosign.md) method to attach an additional signature to the document.</span></span>

<span data-ttu-id="a5721-111">Se ocorrer um erro CAPICOM, um valor negativo será retornado na propriedade **Err. Number** .</span><span class="sxs-lookup"><span data-stu-id="a5721-111">If any CAPICOM error occurs, a negative value is returned in the **Err.Number** property.</span></span> <span data-ttu-id="a5721-112">Para obter mais informações sobre códigos de erro CAPICOM, consulte [**\_ \_ código de erro CAPICOM**](capicom-error-code.md).</span><span class="sxs-lookup"><span data-stu-id="a5721-112">For more information about CAPICOM error codes, see [**CAPICOM\_ERROR\_CODE**](capicom-error-code.md).</span></span> <span data-ttu-id="a5721-113">Se o código de erro na propriedade **Err. Number** for um valor positivo, o erro será um erro do Windows.</span><span class="sxs-lookup"><span data-stu-id="a5721-113">If the error code in the **Err.Number** property is a positive value, then the error is a Windows error.</span></span> <span data-ttu-id="a5721-114">Para obter informações sobre códigos de erro do Windows, consulte Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="a5721-114">For information about Windows error codes, see Winerror.h.</span></span>

> [!Note]
> <span data-ttu-id="a5721-115">A atribuição de um documento também exige que o coassinador tenha um [*certificado*](../secgloss/c-gly.md) disponível com uma [*chave privada*](../secgloss/p-gly.md) para criar a assinatura.</span><span class="sxs-lookup"><span data-stu-id="a5721-115">Cosigning a document also requires that the cosigner have an available [*certificate*](../secgloss/c-gly.md) with a [*private key*](../secgloss/p-gly.md) to create the signature.</span></span> <span data-ttu-id="a5721-116">Se um signatário não for especificado na chamada do método [**Sign**](signeddata-sign.md) e não houver nenhum certificado no capicont \_ My \_ Store com uma chave privada associada, o método falhará.</span><span class="sxs-lookup"><span data-stu-id="a5721-116">If a signer is not specified in the call of the [**Sign**](signeddata-sign.md) method and there is no certificate in CAPICOM\_MY\_STORE with an associated private key, the method fails.</span></span> <span data-ttu-id="a5721-117">Se houver um e apenas um certificado no capicont \_ My \_ Store com uma chave privada associada, essa chave e o certificado serão usados.</span><span class="sxs-lookup"><span data-stu-id="a5721-117">If there is one and only one certificate in CAPICOM\_MY\_STORE with an associated private key, that key and certificate are used.</span></span> <span data-ttu-id="a5721-118">Se houver mais de um certificado utilizável, será exibido um prompt para permitir que o usuário escolha o certificado desejado.</span><span class="sxs-lookup"><span data-stu-id="a5721-118">If there is more than one usable certificate, a prompt is displayed to allow the user to choose the desired certificate.</span></span>
> 
> <span data-ttu-id="a5721-119">Se o método de [**coassinatura**](signeddata-cosign.md) for usado em um aplicativo baseado na Web, um prompt será sempre exibido para obter a permissão do usuário antes que uma assinatura seja criada usando a chave privada desse signatário.</span><span class="sxs-lookup"><span data-stu-id="a5721-119">If the [**CoSign**](signeddata-cosign.md) method is used in a web-based application, a prompt is always displayed to get the user's permission before a signature is created by using that signer's private key.</span></span>

 

<span data-ttu-id="a5721-120">No exemplo a seguir, os arquivos que contêm o documento a ser assinado e as assinaturas atuais nesse documento são lidos, a assinatura é coatribuída e a nova assinatura é gravada em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="a5721-120">In the following example, files that contain the document to be signed and the current signatures on that document are read, the signature is cosigned, and the new signature is written to a file.</span></span> <span data-ttu-id="a5721-121">O exemplo usa uma assinatura desanexada com os dados assinados e a assinatura em arquivos separados.</span><span class="sxs-lookup"><span data-stu-id="a5721-121">The example uses a detached signature with the data signed and the signature in separate files.</span></span>


```VB
Sub CoSignContent(ByVal InputFile1Name As String, ByVal _
    InputFile2Name As String, ByVal OutputFileName As String)

    On Error GoTo ErrorHandler
    Dim c As String
    Dim s As String
    Dim CS As String
    Dim Signobj As New SignedData
    Open InputFile1Name for Input as #1
    Input #1, s
    Close #1
    Open InputFileName2 for input as #2
    Input #2, c 
    Close #2

    Signobj.Content = c
    Signobj.Verify(s)
    CS = Signobj.CoSign
    Open OutputFileName for output as #3
    Write #3, CS
    Close # 3
    Signobj = Nothing
    MsgBox("Cosign finished. Cosignature saved to a file.")
    Exit Sub
ErrorHandler:
    If err.number > 0 Then
        MsgBox("Visual Basic error found:" & err.description)
    Else
        MsgBox("CAPICOM error found : " & err.number)
    End If
End Sub
```



 

 
