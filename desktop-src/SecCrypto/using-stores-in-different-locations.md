---
description: O exemplo a seguir demonstra aspectos de trabalhar com o objeto Store. Ele mostra a abertura de lojas nos locais DE ARMAZENAMENTO DE MEMÓRIA CAPICOM, ARMAZENAMENTO DE USUÁRIO ATUAL DO CAPICOM e ARMAZENAMENTO DE \_ \_ MÁQUINAS LOCAIS \_ \_ \_ \_ \_ CAPICOM. \_
ms.assetid: bfb7ff48-1d6b-404f-9dd4-6de1898354b7
title: Usando lojas em locais diferentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e57e1c1584754f0b02b61438a7a6a83694c36cd77c633c52f6bec216721d7c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117971402"
---
# <a name="using-stores-in-different-locations"></a>Usando lojas em locais diferentes

\[CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP. Em vez disso, use o .NET Framework para implementar recursos de segurança. Para obter mais informações, [consulte Alternativas ao uso de CAPICOM.](alternatives-to-using-capicom.md)\]

O exemplo a seguir demonstra aspectos de trabalhar com o [**objeto**](store.md) Store. Ele mostra a abertura de lojas nos locais DE ARMAZENAMENTO DE MEMÓRIA CAPICOM, ARMAZENAMENTO DE USUÁRIO ATUAL DO CAPICOM e ARMAZENAMENTO DE \_ \_ MÁQUINAS LOCAIS \_ \_ \_ \_ \_ CAPICOM. \_

O exemplo mostra a exportação [*de certificados*](../secgloss/c-gly.md) de um armazenamento [*aberto,*](../secgloss/c-gly.md)escrevendo os certificados exportados em um arquivo, lendo-os novamente e importando-os para um armazenamento diferente. Os certificados recém-importados são enumerados e exibidos.

Em qualquer erro CAPICOM, um valor decimal negativo de **Err.Number** é retornado. Para obter mais informações, consulte [**CAPICOM \_ ERROR \_ CODE**](capicom-error-code.md). Para obter informações sobre valores decimais positivos de **Err.Number,** consulte Winerror.h.


```VB
Sub OpenStores()

    On Error GoTo ErrorHandler

    'Open Memory, current user, and local machine stores
    Dim MemoryStore As New Store
    Dim CurrentUserStore As New Store
    Dim LocalMachineStore As New Store
    Dim NumCerts As Integer

    MemoryStore.Open(CAPICOM_MEMORY_STORE, "MemStore", _
        CAPICOM_STORE_OPEN_READ_WRITE)
    CurrentUserStore.Open(CAPICOM_CURRENT_USER_STORE, _
        CAPICOM_MY_STORE, CAPICOM_STORE_OPEN_READ_ONLY)
    LocalMachineStore.Open(CAPICOM_LOCAL_MACHINE_STORE, _
        CAPICOM_CA_STORE, CAPICOM_STORE_OPEN_READ_ONLY)

    ' Check the number of certificates in the stores.
    NumCerts = MemoryStore.Certificates.Count
    MsgBox("There are " & NumCerts & _
        " certificates in the memory store. ")
    NumCerts = CurrentUserStore.Certificates.Count
    MsgBox("There are " & NumCerts & _
        " certificates in the current user store. ")
    NumCerts = LocalMachineStore.Certificates.Count
    MsgBox("There are " & NumCerts & _
        " certificates in the local machine store. ")


    '  Export the certificates in the current user MY store
    '  to a file.
    Dim ExportString As String
    ExportString = CurrentUserStore.Export
Open "Exportcerts.txt" For Output As #1
Write #1, ExportString
Close #1

    ' Read the store the file.
    Dim importString As String
Open "exportcerts.txt" For Input As #2
Input #2, importString
Close #2
    MemoryStore.Import(importString)

    ' Check the number of certificates in the memory store after 
    ' import()
    NumCerts = MemoryStore.Certificates.Count
    MsgBox("There are " & NumCerts & _
        " certificates now in the memory store. ")

    ' Enumerate the certificates in the memory store and display each
    ' certificate
    Dim i As Long
    For i = 1 To NumCerts
        MemoryStore.Certificates.Item(i).Display()
    Next i

    ' Release the store objects
    MemoryStore = Nothing
    CurrentUserStore = Nothing
    LocalMachineStore = Nothing
    Exit Sub
ErrorHandler:
    If Err.Number > 0 Then
        MsgBox("Visual Basic error found: " & Err.Description)
    Else
        MsgBox("CAPICOM error found : " & Err.Number)
    End If
End Sub
```



 

 
