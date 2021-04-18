---
description: Um uso padrão de uma assinatura é assinar um texto e salvar esse texto assinado em um arquivo. O texto assinado também pode ser enviado pela Internet. A mensagem assinada está no \# formato PKCS 7.
ms.assetid: 67a36123-4fce-4d40-83c3-b9668221276b
title: Assinando um documento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ce1754cdfa1e89c23525474bae880dc2809c242
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756675"
---
# <a name="signing-a-document"></a><span data-ttu-id="becc9-105">Assinando um documento</span><span class="sxs-lookup"><span data-stu-id="becc9-105">Signing a Document</span></span>

<span data-ttu-id="becc9-106">\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="becc9-106">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="becc9-107">Em vez disso, use o .NET Framework para implementar recursos de segurança.</span><span class="sxs-lookup"><span data-stu-id="becc9-107">Instead, use the .NET Framework to implement security features.</span></span> <span data-ttu-id="becc9-108">Para obter mais informações, consulte [alternativas ao uso do CApicom](alternatives-to-using-capicom.md).\]</span><span class="sxs-lookup"><span data-stu-id="becc9-108">For more information, see [Alternatives to Using CAPICOM](alternatives-to-using-capicom.md).\]</span></span>

<span data-ttu-id="becc9-109">Um uso padrão de uma assinatura é assinar um texto e salvar esse texto assinado em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="becc9-109">A standard use of a signature is to sign a text and save that signed text to a file.</span></span> <span data-ttu-id="becc9-110">O texto assinado também pode ser enviado pela Internet.</span><span class="sxs-lookup"><span data-stu-id="becc9-110">The signed text could also be sent over the Internet.</span></span> <span data-ttu-id="becc9-111">A mensagem assinada está no \# formato PKCS 7.</span><span class="sxs-lookup"><span data-stu-id="becc9-111">The signed message is in PKCS \#7 format.</span></span>

<span data-ttu-id="becc9-112">Neste exemplo, a assinatura é criada para conteúdo desanexado (quando o conteúdo não está incluído com a assinatura).</span><span class="sxs-lookup"><span data-stu-id="becc9-112">In this example, the signature is created for detached content (when the content is not included with the signature).</span></span> <span data-ttu-id="becc9-113">Uma assinatura desanexada geralmente será usada se o destinatário da assinatura tiver uma cópia do texto assinado exato.</span><span class="sxs-lookup"><span data-stu-id="becc9-113">A detached signature would most often be used if the recipient of the signature has a copy of the exact signed text.</span></span> <span data-ttu-id="becc9-114">No exemplo a seguir, a mensagem original e a assinatura desanexada são gravadas em arquivos separados.</span><span class="sxs-lookup"><span data-stu-id="becc9-114">In the example below, the original message and the detached signature are written to separate files.</span></span>

<span data-ttu-id="becc9-115">Em qualquer erro de CAPICOM, um valor decimal negativo de **Err. Number** é retornado.</span><span class="sxs-lookup"><span data-stu-id="becc9-115">On any CAPICOM error, a negative decimal value of **Err.Number** is returned.</span></span> <span data-ttu-id="becc9-116">Para obter mais informações, [**consulte \_ \_ código de erro CAPICOM**](capicom-error-code.md).</span><span class="sxs-lookup"><span data-stu-id="becc9-116">For more information, see [**CAPICOM\_ERROR\_CODE**](capicom-error-code.md).</span></span> <span data-ttu-id="becc9-117">Para obter informações sobre valores decimais positivos de **Err. Number**, consulte Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="becc9-117">For information about positive decimal values of **Err.Number**, see Winerror.h.</span></span>

<span data-ttu-id="becc9-118">A criação de uma assinatura usa a [*chave privada*](../secgloss/p-gly.md)do signatário.</span><span class="sxs-lookup"><span data-stu-id="becc9-118">Creating a signature uses the signer's [*private key*](../secgloss/p-gly.md).</span></span> <span data-ttu-id="becc9-119">Uma assinatura só poderá ser criada se o certificado do Assinante com uma chave privada associada estiver disponível.</span><span class="sxs-lookup"><span data-stu-id="becc9-119">A signature can only be created if the signer's certificate with an associated private key is available.</span></span> <span data-ttu-id="becc9-120">Este exemplo do método **Sign** não especifica um signatário.</span><span class="sxs-lookup"><span data-stu-id="becc9-120">This example of the **Sign** method does not specify a signer.</span></span> <span data-ttu-id="becc9-121">Se um signatário não for especificado e nenhum certificado no **Capicont \_ meu \_ repositório** tiver uma chave privada associada, o método **Sign** falhará.</span><span class="sxs-lookup"><span data-stu-id="becc9-121">If a signer is not specified and no certificate in **CAPICOM\_MY\_STORE** has an associated private key, the **Sign** method fails.</span></span> <span data-ttu-id="becc9-122">Se um e apenas um certificado no **CAPICOM \_ meu \_ repositório** tiver uma chave privada associada, esse certificado e sua chave privada serão usados para criar a assinatura.</span><span class="sxs-lookup"><span data-stu-id="becc9-122">If one and only one certificate in **CAPICOM\_MY\_STORE** has an associated private key, that certificate and its private key is used to create the signature.</span></span> <span data-ttu-id="becc9-123">Se mais de um certificado no repositório **de \_ meu \_ repositório do capicor** tiver uma chave privada associada, uma caixa de diálogo será exibida e o usuário poderá escolher o certificado a ser usado para criar a assinatura.</span><span class="sxs-lookup"><span data-stu-id="becc9-123">If more than one certificate in the **CAPICOM\_MY\_STORE** store has an associated private key, a dialog box appears and the user can choose the certificate to be used to create the signature.</span></span>

<span data-ttu-id="becc9-124">Quando um aplicativo baseado na Web usa o método **Sign** , um prompt é sempre exibido e a permissão do usuário é necessária antes que uma assinatura que usa a chave privada desse signatário seja criada.</span><span class="sxs-lookup"><span data-stu-id="becc9-124">When a web-based application uses the **Sign** method, a prompt is always displayed and the user's permission is required before a signature that uses that signer's private key is created.</span></span>


```VB
Sub Signfile(ByVal InputFileName As String, _
    ByVal OutputFileName As String)
    
    On Error GoTo ErrorHandler
    Dim c As String
    Dim s As String
    Dim MyStore As New Store
    Dim Signobj As New SignedData
    Dim Signer As New Signer

    ' NOTE: the name 'Attribute' is not a unique name
    ' and must be preceded by 'CAPICOM.'
    Dim SigningTime As New CAPICOM.Attribute

    ' Open the MY store and retrieve the first certificate from the
    ' Store. The signing operation will only work if this
    ' certificate is valid and has access to the signer's private key.
    MyStore.Open CAPICOM_CURRENT_USER_STORE, "MY", _
        CAPICOM_STORE_OPEN_READ_ONLY
    Signer.Certificate = MyStore.Certificates.Item(1)

    ' Open the input file and read the content to be signed from
    ' the file.
    Open App.Path & "\" & InputFileName For Input As #1
    Input #1, c
    Close #1
    
    ' Set the content to be signed.
    Signobj.Content = c

    ' Save the time the data was signed as a signer attribute.
    SigningTime.Name = CAPICOM_AUTHENTICATED_ATTRIBUTE_SIGNING_TIME
    SigningTime.Value = Now
    Signer.AuthenticatedAttributes.Add SigningTime

    ' Sign the content using the signer's private key.
    ' The 'True' parameter indicates that the content signed is not
    ' included in the signature string.
    s = Signobj.Sign(Signer, True)

    Open App.Path & "\" & OutputFileName For Output As #2
    Write #2, s
    Close #2

    MsgBox ("Signature done - Saved to file" & OutputFileName)
    Set Signobj = Nothing
    Set MyStore = Nothing
    Set Signer = Nothing
    Set SigningTime = Nothing

    Exit Sub

ErrorHandler:
    If Err.Number > 0 Then
        MsgBox ("Visual Basic error found:" & Err.Description)
    Else
        MsgBox ("CAPICOM error found : " & Err.Number)
    End If
End Sub
```



## <a name="related-topics"></a><span data-ttu-id="becc9-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="becc9-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="becc9-126">**Store. Open**</span><span class="sxs-lookup"><span data-stu-id="becc9-126">**Store.Open**</span></span>](store-open.md)
</dt> <dt>

[<span data-ttu-id="becc9-127">**Signatário. certificado**</span><span class="sxs-lookup"><span data-stu-id="becc9-127">**Signer.Certificate**</span></span>](signer-certificate.md)
</dt> <dt>

[<span data-ttu-id="becc9-128">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="becc9-128">**Attribute**</span></span>](attribute.md)
</dt> <dt>

[<span data-ttu-id="becc9-129">**SignedData**</span><span class="sxs-lookup"><span data-stu-id="becc9-129">**SignedData**</span></span>](signeddata.md)
</dt> </dl>

 

 
