---
description: Um documento pode ser assinado por mais de um signatário.
ms.assetid: f81cbf7b-317d-4fab-9b30-88b6c6576db8
title: Coatribuindo um documento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb384ef47001f1df85810ac37595988da96a356ff3b36b1b140d1a6f54d0d698
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117769381"
---
# <a name="cosigning-a-document"></a>Coatribuindo um documento

\[o capicom é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP. em vez disso, use o .NET Framework para implementar recursos de segurança. Para obter mais informações, consulte [alternativas ao uso do CApicom](alternatives-to-using-capicom.md).\]

Um documento pode ser assinado por mais de um signatário. Isso acontece quando, por exemplo, duas ou mais partes assinam um contrato ou um relatório de despesas. No exemplo a seguir, um documento já assinado é recebido por um segundo assinante. Esse signatário usa o método de [**coassinatura**](signeddata-cosign.md) para anexar uma assinatura adicional ao documento.

Se ocorrer um erro CAPICOM, um valor negativo será retornado na propriedade **Err. Number** . Para obter mais informações sobre códigos de erro CAPICOM, consulte [**\_ \_ código de erro CAPICOM**](capicom-error-code.md). se o código de erro na propriedade **Err. Number** for um valor positivo, o erro será um erro de Windows. para obter informações sobre Windows códigos de erro, consulte Winerror. h.

> [!Note]
> A atribuição de um documento também exige que o coassinador tenha um [*certificado*](../secgloss/c-gly.md) disponível com uma [*chave privada*](../secgloss/p-gly.md) para criar a assinatura. Se um signatário não for especificado na chamada do método [**Sign**](signeddata-sign.md) e não houver nenhum certificado no capicont \_ My \_ Store com uma chave privada associada, o método falhará. Se houver um e apenas um certificado no capicont \_ My \_ Store com uma chave privada associada, essa chave e o certificado serão usados. Se houver mais de um certificado utilizável, será exibido um prompt para permitir que o usuário escolha o certificado desejado.
> 
> Se o método de [**coassinatura**](signeddata-cosign.md) for usado em um aplicativo baseado na Web, um prompt será sempre exibido para obter a permissão do usuário antes que uma assinatura seja criada usando a chave privada desse signatário.

 

No exemplo a seguir, os arquivos que contêm o documento a ser assinado e as assinaturas atuais nesse documento são lidos, a assinatura é coatribuída e a nova assinatura é gravada em um arquivo. O exemplo usa uma assinatura desanexada com os dados assinados e a assinatura em arquivos separados.


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



 

 
