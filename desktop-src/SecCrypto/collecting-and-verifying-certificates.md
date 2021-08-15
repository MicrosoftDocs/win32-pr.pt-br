---
description: No exemplo a seguir, os certificados em um repositório local são enumerados e verificados quanto à validade.
ms.assetid: 59ae22f6-aa6d-4b53-8a27-73e1e5c62755
title: Coletando e verificando certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60b793cf4aeca7d05d166a4b205b924db53faee09683cefcef7b0244a9eb0289
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117769526"
---
# <a name="collecting-and-verifying-certificates"></a>Coletando e verificando certificados

\[o capicom é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP. em vez disso, use o .NET Framework para implementar recursos de segurança. Para obter mais informações, consulte [alternativas ao uso do CApicom](alternatives-to-using-capicom.md).\]

Geralmente, um grupo de [*certificados*](../secgloss/c-gly.md) precisa ser coletado e verificado. Isso geralmente seria feito para preparar um grupo de destinatários para uma mensagem envelopada. No exemplo a seguir, os certificados em um repositório local são enumerados e verificados quanto à validade. Em seguida, um repositório de Active Directory é aberto para recuperar e adicionar ao repositório local novos certificados. Os certificados recuperados do repositório do Active Directory são verificados quanto à validade e, se forem válidos, são adicionados ao repositório local. Os dois repositórios são então fechados.

Em qualquer erro de CAPICOM, um valor decimal negativo de **Err. Number** é retornado. Para obter mais informações, [**consulte \_ \_ código de erro CAPICOM**](capicom-error-code.md). Para obter informações sobre valores decimais positivos de **Err. Number**, consulte Winerror. h.

Neste exemplo, o nome do repositório local é passado como um parâmetro de cadeia de caracteres. Uma cadeia de caracteres que indica os critérios de pesquisa para certificados no repositório de Active Directory também é passada como um parâmetro.


```VB
Sub CollectValidCerts(ByVal storename As String, ByVal _
    certname As String)

    On Error GoTo errorhandler

    ' Prepare a local certificate store to contain valid
    ' certificates for the recipients of an enveloped
    ' message.

    ' Open the local store and go to the certificates in the store
    '   1. Display the certificate
    '   2. Check the validity of the certificate
    '   3. Remove certificates that are not valid from the store

    Dim LocalStore As New Store
    Dim ADStore As New Store
    Dim i As Long

    LocalStore.Open(CAPICOM_CURRENT_USER_STORE, storename, _
        CAPICOM_STORE_OPEN_READ_WRITE)

    MsgBox("There are " & LocalStore.Certificates.Count & _
        " certificates in this store ")
    For i = 1 To LocalStore.Certificates.Count
        If LocalStore.Certificates.Item(i).IsValid Then
            LocalStore.Certificates.Item(i).Display()
        Else
            MsgBox("A certificate that is not valid was found.")
        End If
    Next i

    ' Open the AD store and retrieve a certificate based
    ' on a string passed into the function. Add any valid
    ' certificates found to the local store.

    ADStore.Open(CAPICOM_ACTIVE_DIRECTORY_USER_STORE, certname, _
        CAPICOM_STORE_OPEN_READ_ONLY)
    MsgBox("There are " & ADStore.Certificates.Count & _
        " certificates in the AD store.")

    For i = 1 To ADStore.Certificates.Count
        If ADStore.Certificates.Item(i).IsValid Then
            ADStore.Certificates.Item(i).Display()
            LocalStore.Add(ADStore.Certificates.Item(i))
        Else
            MsgBox("the certificate from the AD store is not valid.")
        End If
    Next i

    LocalStore = Nothing
    ADStore = Nothing
    MsgBox("Sub finished without error ")
    Exit Sub
errorhandler:
    If Err.Number > 0 Then
        MsgBox("Visual Basic error found:" & Err.Description)
    Else
        MsgBox("CAPICOM error found : " & Err.Number)
    End If
End Sub
```



 

 
