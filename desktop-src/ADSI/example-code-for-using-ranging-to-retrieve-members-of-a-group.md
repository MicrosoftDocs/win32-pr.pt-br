---
title: Exemplo de código para usar o intervalo para recuperar membros de um grupo
description: O exemplo de código a seguir usa a variação com ADO (ActiveX Directory Objects) para recuperar os membros de um grupo.
ms.assetid: baebefd5-7ac6-4d36-a5a4-0796d790abee
ms.tgt_platform: multiple
keywords:
- Exemplo de código para usar a variação para recuperar membros de um grupo ADSI
- código de exemplo C/C++ ADSI, usando variando para recuperar membros de um grupo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c596134b8c20bc777c77b65e6fe349884dda25a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103915900"
---
# <a name="example-code-for-using-ranging-to-retrieve-members-of-a-group"></a><span data-ttu-id="e7247-105">Exemplo de código para usar o intervalo para recuperar membros de um grupo</span><span class="sxs-lookup"><span data-stu-id="e7247-105">Example Code for Using Ranging to Retrieve Members of a Group</span></span>

<span data-ttu-id="e7247-106">O exemplo de código a seguir usa a variação com ADO (ActiveX Directory Objects) para recuperar os membros de um grupo.</span><span class="sxs-lookup"><span data-stu-id="e7247-106">The following code example uses ranging with ActiveX Directory Objects (ADO) to retrieve the members of a group.</span></span>

<span data-ttu-id="e7247-107">O trecho de código a seguir requer uma referência à biblioteca do Microsoft ActiveX Data Objects 6,0.</span><span class="sxs-lookup"><span data-stu-id="e7247-107">The following code snippet requires a reference to Microsoft ActiveX Data Objects 6.0 Library.</span></span>


```VB
 Private Sub EnumGroupWithADO(ByVal strGroupDN As String, ByVal strUsername As String, ByVal strPassword As String)
        Dim oConn
        Dim oComm
        Dim rangeStep
        Dim lowRange
        Dim highRange
        Dim lastLoop
        Dim commandPrefix
        Dim amp
        Dim commandSuffix
        Dim oRS
        Dim nRetrieved
        oConn = CreateObject("ADODB.Connection")
        oComm = CreateObject("ADODB.Command")

        oConn.Provider = "ADsDSOObject"
        oConn.Properties("ADSI Flag") = 1

        If strUsername <> "" Then
            oConn.Properties("User ID") = strUsername
            oConn.Properties("Password") = strPassword
        End If

        oConn.Open()
        oComm.ActiveConnection = oConn

        ' For compatibility with all operating systems, the number of objects
        ' retrieved by each query should not exceed 999.
        rangeStep = 999

        lastLoop = False
        lowRange = 0
        highRange = lowRange + rangeStep

        commandPrefix = "<LDAP://" & strGroupDN > ">;(objectClass=*);member;range="
        commandSuffix = ";base"

        Do
            If lastLoop Then
                ' Perform this query with the "range=<lowRange>-*" range.
                oComm.CommandText = commandPrefix & lowRange & "-*" & commandSuffix
            Else
                ' Perform this query with the "range=<lowRange>-<highRange>" range.
                oComm.CommandText = commandPrefix & lowRange & "-" & highRange & commandSuffix
            End If
            Debug.Print("Current search command: " & oComm.CommandText)

            ' Execute the query.
            oRS = oComm.Execute

            ' Reset the retrieved members counter.
            nRetrieved = 0

            ' Enumerate the retrieved members.
            While Not oRS.EOF
                For Each oField In oRS.Fields
                    If VarType(oField) = (vbArray + vbVariant) Then
                        For Each oValue In oField.Value
                            Debug.Print(vbTab & oValue)
                            nRetrieved = nRetrieved + 1
                        Next
                    End If
                Next
                oRS.MoveNext()
            End While

            ' If the last query was performed, exit the loop.
            If lastLoop = True Then
                Exit Do
            End If

            If nRetrieved = 0 Then
                ' No objects were retrieved by the last query; perform one last query
                ' with the â€œrange=<lowRange>-*â€ range.
                lastLoop = True
            Else
                ' Increment the high and low ranges to query for the next block of objects.
                lowRange = highRange + 1
                highRange = lowRange + rangeStep
            End If
        Loop While nRetrieved = lowRange
    End Sub
End Module
```



 

 




