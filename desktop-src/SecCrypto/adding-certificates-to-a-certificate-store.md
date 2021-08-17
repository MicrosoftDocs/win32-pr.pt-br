---
description: Os certificados podem ser adicionados ou removidos de repositórios de certificados se o repositório for aberto com permissão de leitura/gravação.
ms.assetid: a1cb6e1e-0702-4f73-827e-3f9e9237b4b6
title: Adicionando certificados a um repositório de certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e3c4b2fafbcd11bf2d984dfd5b5a575f67dc4f6d3c70337de399ca6076029ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117774031"
---
# <a name="adding-certificates-to-a-certificate-store"></a>Adicionando certificados a um repositório de certificados

\[o capicom é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista, Windows XP. em vez disso, use o .NET Framework para implementar recursos de segurança. Para obter mais informações, consulte [alternativas ao uso do CApicom](alternatives-to-using-capicom.md).\]

Os [*certificados*](../secgloss/c-gly.md) podem ser adicionados ou removidos de [*repositórios de certificados*](../secgloss/c-gly.md) se o repositório for aberto com permissão de leitura/gravação. A permissão de leitura/gravação não é concedida a repositórios Active Directory. Embora os certificados possam ser adicionados ou removidos dos armazenamentos de memória, as alterações nos armazenamentos de memória não são mantidas entre as sessões.

Os certificados podem ser adicionados a um repositório de certificados que é aberto com permissão de leitura/gravação usando o método **Add** . Um certificado pode ser removido de um repositório de certificados que é aberto com permissão de leitura/gravação usando o método **Remove** . As novas lojas podem ser criadas e salvas nos locais de armazenamento do capicor \_ \_ armazenamento do usuário atual \_ e CAPICOM do \_ repositório do \_ computador local \_ . Repositórios recém-criados em qualquer um desses locais podem ser abertos com permissão de leitura/gravação.

No exemplo a seguir, dois repositórios de certificados são abertos. Certificados de assuntos com sobrenomes começando com F são recuperados do repositório de Active Directory. O armazenamento de usuário atual do CAPICOM \_ \_ , o \_ \_ repositório de armazenamento de AC capicor \_ é aberto como um repositório de leitura/gravação e o primeiro certificado da coleção de certificados no repositório de Active Directory é adicionado aos certificados no armazenamento do CAPICOM da \_ AC \_ .

Para fins de demonstração, o exemplo mostra a abertura de lojas no armazenamento de memória capicor \_ \_ , o armazenamento de \_ \_ usuário atual e os locais de armazenamento do \_ computador local CAPICOM \_ \_ \_ . O exemplo mostra a exportação de todos os certificados de um armazenamento aberto, gravando os certificados exportados em um arquivo, lendo-os de volta e importando-os em um repositório diferente. Os certificados recém importados são enumerados e exibidos.

Em qualquer erro de CAPICOM, um valor decimal negativo de **Err. Number** é retornado. Para obter mais informações, [**consulte \_ \_ código de erro CAPICOM**](capicom-error-code.md). Para obter informações sobre valores decimais positivos de **Err. Number**, consulte Winerror. h.

O exemplo a seguir mostra a abertura de repositórios de certificados usando Associação antecipada na declaração dos objetos de **armazenamento** e na criação de uma instância desses objetos.


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



 

 
