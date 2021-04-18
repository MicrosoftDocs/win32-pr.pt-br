---
description: No exemplo a seguir, os certificados em um repositório local são enumerados e verificados quanto à validade.
ms.assetid: 59ae22f6-aa6d-4b53-8a27-73e1e5c62755
title: Coletando e verificando certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0b160f373d5ade65679fcc4dd87e3c1c86dc4ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105779369"
---
# <a name="collecting-and-verifying-certificates"></a><span data-ttu-id="8454c-103">Coletando e verificando certificados</span><span class="sxs-lookup"><span data-stu-id="8454c-103">Collecting and Verifying Certificates</span></span>

<span data-ttu-id="8454c-104">\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="8454c-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="8454c-105">Em vez disso, use o .NET Framework para implementar recursos de segurança.</span><span class="sxs-lookup"><span data-stu-id="8454c-105">Instead, use the .NET Framework to implement security features.</span></span> <span data-ttu-id="8454c-106">Para obter mais informações, consulte [alternativas ao uso do CApicom](alternatives-to-using-capicom.md).\]</span><span class="sxs-lookup"><span data-stu-id="8454c-106">For more information, see [Alternatives to Using CAPICOM](alternatives-to-using-capicom.md).\]</span></span>

<span data-ttu-id="8454c-107">Geralmente, um grupo de [*certificados*](../secgloss/c-gly.md) precisa ser coletado e verificado.</span><span class="sxs-lookup"><span data-stu-id="8454c-107">Often a group of [*certificates*](../secgloss/c-gly.md) needs to be collected and verified.</span></span> <span data-ttu-id="8454c-108">Isso geralmente seria feito para preparar um grupo de destinatários para uma mensagem envelopada.</span><span class="sxs-lookup"><span data-stu-id="8454c-108">This would often be done to prepare a group of recipients for an enveloped message.</span></span> <span data-ttu-id="8454c-109">No exemplo a seguir, os certificados em um repositório local são enumerados e verificados quanto à validade.</span><span class="sxs-lookup"><span data-stu-id="8454c-109">In the example that follows, the certificates in a local store are enumerated and checked for validity.</span></span> <span data-ttu-id="8454c-110">Em seguida, um repositório de Active Directory é aberto para recuperar e adicionar ao repositório local novos certificados.</span><span class="sxs-lookup"><span data-stu-id="8454c-110">Next, an Active Directory store is opened to retrieve and add to the local store new certificates.</span></span> <span data-ttu-id="8454c-111">Os certificados recuperados do repositório do Active Directory são verificados quanto à validade e, se forem válidos, são adicionados ao repositório local.</span><span class="sxs-lookup"><span data-stu-id="8454c-111">The certificates retrieved from the active directory store are checked for validity and, if valid, are added to the local store.</span></span> <span data-ttu-id="8454c-112">Os dois repositórios são então fechados.</span><span class="sxs-lookup"><span data-stu-id="8454c-112">Both stores are then closed.</span></span>

<span data-ttu-id="8454c-113">Em qualquer erro de CAPICOM, um valor decimal negativo de **Err. Number** é retornado.</span><span class="sxs-lookup"><span data-stu-id="8454c-113">On any CAPICOM error, a negative decimal value of **Err.Number** is returned.</span></span> <span data-ttu-id="8454c-114">Para obter mais informações, [**consulte \_ \_ código de erro CAPICOM**](capicom-error-code.md).</span><span class="sxs-lookup"><span data-stu-id="8454c-114">For more information, see [**CAPICOM\_ERROR\_CODE**](capicom-error-code.md).</span></span> <span data-ttu-id="8454c-115">Para obter informações sobre valores decimais positivos de **Err. Number**, consulte Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="8454c-115">For information about positive decimal values of **Err.Number**, see Winerror.h.</span></span>

<span data-ttu-id="8454c-116">Neste exemplo, o nome do repositório local é passado como um parâmetro de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="8454c-116">In this example, the name of the local store is passed in as a string parameter.</span></span> <span data-ttu-id="8454c-117">Uma cadeia de caracteres que indica os critérios de pesquisa para certificados no repositório de Active Directory também é passada como um parâmetro.</span><span class="sxs-lookup"><span data-stu-id="8454c-117">A string indicating the search criteria for certificates in the Active Directory store is also passed in as a parameter.</span></span>


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



 

 
