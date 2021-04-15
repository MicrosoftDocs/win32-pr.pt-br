---
description: Os certificados podem ser adicionados ou removidos de repositórios de certificados se o repositório for aberto com permissão de leitura/gravação.
ms.assetid: a1cb6e1e-0702-4f73-827e-3f9e9237b4b6
title: Adicionando certificados a um repositório de certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6f4c018be697f48e40d52480f49694762fb956f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104505921"
---
# <a name="adding-certificates-to-a-certificate-store"></a><span data-ttu-id="41d87-103">Adicionando certificados a um repositório de certificados</span><span class="sxs-lookup"><span data-stu-id="41d87-103">Adding Certificates to a Certificate Store</span></span>

<span data-ttu-id="41d87-104">\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista, Windows XP.</span><span class="sxs-lookup"><span data-stu-id="41d87-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="41d87-105">Em vez disso, use o .NET Framework para implementar recursos de segurança.</span><span class="sxs-lookup"><span data-stu-id="41d87-105">Instead, use the .NET Framework to implement security features.</span></span> <span data-ttu-id="41d87-106">Para obter mais informações, consulte [alternativas ao uso do CApicom](alternatives-to-using-capicom.md).\]</span><span class="sxs-lookup"><span data-stu-id="41d87-106">For more information, see [Alternatives to Using CAPICOM](alternatives-to-using-capicom.md).\]</span></span>

<span data-ttu-id="41d87-107">Os [*certificados*](../secgloss/c-gly.md) podem ser adicionados ou removidos de [*repositórios de certificados*](../secgloss/c-gly.md) se o repositório for aberto com permissão de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="41d87-107">[*Certificates*](../secgloss/c-gly.md) can be added to or removed from [*certificate stores*](../secgloss/c-gly.md) if the store is opened with read/write permission.</span></span> <span data-ttu-id="41d87-108">A permissão de leitura/gravação não é concedida a repositórios Active Directory.</span><span class="sxs-lookup"><span data-stu-id="41d87-108">Read/write permission is not granted to Active Directory stores.</span></span> <span data-ttu-id="41d87-109">Embora os certificados possam ser adicionados ou removidos dos armazenamentos de memória, as alterações nos armazenamentos de memória não são mantidas entre as sessões.</span><span class="sxs-lookup"><span data-stu-id="41d87-109">While certificates can be added to or removed from memory stores, changes in memory stores are not persisted between sessions.</span></span>

<span data-ttu-id="41d87-110">Os certificados podem ser adicionados a um repositório de certificados que é aberto com permissão de leitura/gravação usando o método **Add** .</span><span class="sxs-lookup"><span data-stu-id="41d87-110">Certificates can be added to a certificate store that is opened with read/write permission by using the **Add** method.</span></span> <span data-ttu-id="41d87-111">Um certificado pode ser removido de um repositório de certificados que é aberto com permissão de leitura/gravação usando o método **Remove** .</span><span class="sxs-lookup"><span data-stu-id="41d87-111">A certificate can be removed from a certificate store that is opened with read/write permission by using the **Remove** method.</span></span> <span data-ttu-id="41d87-112">As novas lojas podem ser criadas e salvas nos locais de armazenamento do capicor \_ \_ armazenamento do usuário atual \_ e CAPICOM do \_ repositório do \_ computador local \_ .</span><span class="sxs-lookup"><span data-stu-id="41d87-112">New stores can be created and saved in the CAPICOM\_CURRENT\_USER\_STORE and CAPICOM\_LOCAL\_MACHINE\_STORE locations.</span></span> <span data-ttu-id="41d87-113">Repositórios recém-criados em qualquer um desses locais podem ser abertos com permissão de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="41d87-113">Newly created stores in either of these locations can be opened with read/write permission.</span></span>

<span data-ttu-id="41d87-114">No exemplo a seguir, dois repositórios de certificados são abertos.</span><span class="sxs-lookup"><span data-stu-id="41d87-114">In the following example, two certificate stores are opened.</span></span> <span data-ttu-id="41d87-115">Certificados de assuntos com sobrenomes começando com F são recuperados do repositório de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="41d87-115">Certificates of subjects with last names beginning with F are retrieved from the Active Directory store.</span></span> <span data-ttu-id="41d87-116">O armazenamento de usuário atual do CAPICOM \_ \_ , o \_ \_ repositório de armazenamento de AC capicor \_ é aberto como um repositório de leitura/gravação e o primeiro certificado da coleção de certificados no repositório de Active Directory é adicionado aos certificados no armazenamento do CAPICOM da \_ AC \_ .</span><span class="sxs-lookup"><span data-stu-id="41d87-116">The CAPICOM\_CURRENT\_USER\_STORE, CAPICOM\_CA\_STORE store is then opened as a read/write store and the first certificate from the collection of certificates in the Active Directory store is added to the certificates in the CAPICOM\_CA\_STORE.</span></span>

<span data-ttu-id="41d87-117">Para fins de demonstração, o exemplo mostra a abertura de lojas no armazenamento de memória capicor \_ \_ , o armazenamento de \_ \_ usuário atual e os locais de armazenamento do \_ computador local CAPICOM \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="41d87-117">For demonstration purposes, the example shows the opening of stores in the CAPICOM\_MEMORY\_STORE, CAPICOM\_CURRENT\_USER\_STORE, and CAPICOM\_LOCAL\_MACHINE\_STORE locations.</span></span> <span data-ttu-id="41d87-118">O exemplo mostra a exportação de todos os certificados de um armazenamento aberto, gravando os certificados exportados em um arquivo, lendo-os de volta e importando-os em um repositório diferente.</span><span class="sxs-lookup"><span data-stu-id="41d87-118">The example shows exporting all certificates from an open store, writing the exported certificates to a file, reading them back in, and importing them into a different store.</span></span> <span data-ttu-id="41d87-119">Os certificados recém importados são enumerados e exibidos.</span><span class="sxs-lookup"><span data-stu-id="41d87-119">The newly imported certificates are them enumerated and displayed.</span></span>

<span data-ttu-id="41d87-120">Em qualquer erro de CAPICOM, um valor decimal negativo de **Err. Number** é retornado.</span><span class="sxs-lookup"><span data-stu-id="41d87-120">On any CAPICOM error, a negative decimal value of **Err.Number** is returned.</span></span> <span data-ttu-id="41d87-121">Para obter mais informações, [**consulte \_ \_ código de erro CAPICOM**](capicom-error-code.md).</span><span class="sxs-lookup"><span data-stu-id="41d87-121">For more information, see [**CAPICOM\_ERROR\_CODE**](capicom-error-code.md).</span></span> <span data-ttu-id="41d87-122">Para obter informações sobre valores decimais positivos de **Err. Number**, consulte Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="41d87-122">For information about positive decimal values of **Err.Number**, see Winerror.h.</span></span>

<span data-ttu-id="41d87-123">O exemplo a seguir mostra a abertura de repositórios de certificados usando Associação antecipada na declaração dos objetos de **armazenamento** e na criação de uma instância desses objetos.</span><span class="sxs-lookup"><span data-stu-id="41d87-123">The following example shows opening certificate stores using early binding in the declaration of the **Store** objects and in creating an instance of those objects.</span></span>


```VB
Sub AddCert()
On Error GoTo ErrorHandler
' The following shows two different ways to declare and
' create a store object.

Dim myADstore As New Store

Dim myCAstore As Store
Set myCAstore = New Store

' In this example, the Active Directory store will be searched for a 
' certificate with a subject name that begins with the letter F. 
' This is done by using the string "SN=F*" as the name of the store.

Dim SubjectNameSN As String
SubjectNameSN = "SN=F*"

' Active Directory stores can only be opened with read-only
' access.

myADstore.Open CAPICOM_ACTIVE_DIRECTORY_USER_STORE,
                SubjectNameSN , CAPICOM_STORE_OPEN_READ_ONLY

'  This example assumes that the store opened and that
'  at least one certificate was returned.
'  A complete application would ensure that at least one certificate
'  was in the store before proceeding and would
'  also select one or more of the certificates returned
'  to be added instead of using the first certificate
'  in the collection.

'  Open the MY store so that a certificate can be added.

myCAstore.Open CAPICOM_CURRENT_USER_STORE, CAPICOM_MY_STORE,
                    CAPICOM_STORE_OPEN_READ_WRITE

myCAstore.Add myADstore.certificates.Item(1)

' Release the two store objects.

Set myCAstore = Nothing
Set myADstore = Nothing
Exit Sub

ErrorHandler:
If Err.Number > 0 Then
    MsgBox "Visual Basic error found:" & Err.Description
Else
    MsgBox "CAPICOM error found : " & Err.Number
End If
End Sub


```



 

 
