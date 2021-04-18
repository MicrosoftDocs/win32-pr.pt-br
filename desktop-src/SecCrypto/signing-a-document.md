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
# <a name="signing-a-document"></a>Assinando um documento

\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP. Em vez disso, use o .NET Framework para implementar recursos de segurança. Para obter mais informações, consulte [alternativas ao uso do CApicom](alternatives-to-using-capicom.md).\]

Um uso padrão de uma assinatura é assinar um texto e salvar esse texto assinado em um arquivo. O texto assinado também pode ser enviado pela Internet. A mensagem assinada está no \# formato PKCS 7.

Neste exemplo, a assinatura é criada para conteúdo desanexado (quando o conteúdo não está incluído com a assinatura). Uma assinatura desanexada geralmente será usada se o destinatário da assinatura tiver uma cópia do texto assinado exato. No exemplo a seguir, a mensagem original e a assinatura desanexada são gravadas em arquivos separados.

Em qualquer erro de CAPICOM, um valor decimal negativo de **Err. Number** é retornado. Para obter mais informações, [**consulte \_ \_ código de erro CAPICOM**](capicom-error-code.md). Para obter informações sobre valores decimais positivos de **Err. Number**, consulte Winerror. h.

A criação de uma assinatura usa a [*chave privada*](../secgloss/p-gly.md)do signatário. Uma assinatura só poderá ser criada se o certificado do Assinante com uma chave privada associada estiver disponível. Este exemplo do método **Sign** não especifica um signatário. Se um signatário não for especificado e nenhum certificado no **Capicont \_ meu \_ repositório** tiver uma chave privada associada, o método **Sign** falhará. Se um e apenas um certificado no **CAPICOM \_ meu \_ repositório** tiver uma chave privada associada, esse certificado e sua chave privada serão usados para criar a assinatura. Se mais de um certificado no repositório **de \_ meu \_ repositório do capicor** tiver uma chave privada associada, uma caixa de diálogo será exibida e o usuário poderá escolher o certificado a ser usado para criar a assinatura.

Quando um aplicativo baseado na Web usa o método **Sign** , um prompt é sempre exibido e a permissão do usuário é necessária antes que uma assinatura que usa a chave privada desse signatário seja criada.


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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Store. Open**](store-open.md)
</dt> <dt>

[**Signatário. certificado**](signer-certificate.md)
</dt> <dt>

[**Atributo**](attribute.md)
</dt> <dt>

[**SignedData**](signeddata.md)
</dt> </dl>

 

 
