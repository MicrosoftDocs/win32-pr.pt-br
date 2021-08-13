---
title: Código de exemplo para adicionar um membro a um grupo
description: Este tópico contém exemplos de código que adicionam um membro a um grupo.
ms.assetid: 306fcadb-a492-41e5-bfb3-8beaaec24fb5
ms.tgt_platform: multiple
keywords:
- Exemplos do Active Directory do Active Directory, adicionando um membro a um grupo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5cccccca0fa701b4f5bc1ce9b350ac1073c6da7614c7292724138b2d433ef2e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118191289"
---
# <a name="example-code-for-adding-a-member-to-a-group"></a>Código de exemplo para adicionar um membro a um grupo

Este tópico contém exemplos de código que adicionam um membro a um grupo. Os exemplos Visual Basic VBScript (Scripting Edition) e C++ adicionam um membro adicionando o objeto [**IADs**](/windows/desktop/api/iads/nn-iads-iads) que representa o membro ao [**objeto IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup) que representa o grupo. Os Visual Basic .NET e C# modificam a propriedade membro do [objeto DirectoryEntry](/dotnet/api/system.directoryservices.directoryentry) que representa o grupo.


Os exemplos de código C# a seguir adicionam um membro existente a um grupo. A função leva o ADsPath do contêiner de grupo e o nome diferenciado do membro a ser adicionado ao grupo. O ADsPath é usado para criar um [objeto DirectoryEntry](/dotnet/api/system.directoryservices.directoryentry) que representa o grupo. O [método PropertyValueCollection.Add](/dotnet/api/system.directoryservices.propertyvaluecollection.add#System_DirectoryServices_PropertyValueCollection_Add_System_Object_) adiciona ao grupo o membro cujo nome diferenciado foi passado para a função. Em seguida, a função usa o [método DirectoryEntry.CommitChanges](/dotnet/api/system.directoryservices.directoryentry.commitchanges#System_DirectoryServices_DirectoryEntry_CommitChanges) para gravar as novas informações de membro no banco de dados.

Chame a função com os seguintes parâmetros:

-   *bindString:* um ADsPath válido para um contêiner de grupo, como "LDAP://fabrikam.com/CN=TestGroup,OU=TestOU,DC=fabrikam,DC=com"
-   *newMember*: o nome diferenciado do membro a ser adicionado ao grupo, como "CN=JeffSmith,OU=TestOU,DC=fabrikam,DC=com"


```CSharp
private void AddMemberToGroup(

                                string bindString,

                                string newMember

                                )

{

    try
    {

        DirectoryEntry ent = new DirectoryEntry( bindString );

        ent.Properties["member"].Add(newMember);

        ent.CommitChanges();

    }

    catch (Exception e)
    {

        Console.WriteLine( "An error occurred.");

        Console.WriteLine( "{0}", e.Message);

        return;

    }

}
```




Os exemplos Visual Basic código .NET a seguir adicionam um membro existente a um grupo. A função leva o ADsPath do contêiner de grupo e o nome diferenciado do membro a ser adicionado ao grupo. O ADsPath é usado para criar um [objeto DirectoryEntry](/dotnet/api/system.directoryservices.directoryentry) que representa o grupo. O [método PropertyValueCollection.Add](/dotnet/api/system.directoryservices.propertyvaluecollection.add#System_DirectoryServices_PropertyValueCollection_Add_System_Object_) adiciona ao grupo o membro cujo nome diferenciado foi passado para a função. Em seguida, a função usa o [método DirectoryEntry.CommitChanges](/dotnet/api/system.directoryservices.directoryentry.commitchanges#System_DirectoryServices_DirectoryEntry_CommitChanges) para gravar as novas informações de membro no banco de dados.

Chame a função com os seguintes parâmetros:

-   *bindString:* um ADsPath válido para um contêiner de grupo, como "LDAP://fabrikam.com/CN=TestGroup,OU=TestOU,DC=fabrikam,DC=com"
-   *newMember*: o nome diferenciado do membro a ser adicionado ao grupo, como "CN=JeffSmith,OU=TestOU,DC=fabrikam,DC=com"


```VB
Private Sub AddMemberToGroup(ByVal bindString As String, 
                                      ByVal newMember As String)

    Try

        Dim ent As New DirectoryEntry(bindString)

        ent.Properties("member").Add(newMember)

        ent.CommitChanges()

    Catch e As Exception

        Console.WriteLine("An error occurred.")

        Console.WriteLine("{0}", e.Message)

        Return

    End Try

End Sub
```




O exemplo de VBScript a seguir adiciona um membro existente a um grupo. O script adiciona o usuário, Jeff Smith, ao grupo TestGroup.


```VB
Option Explicit

On Error Resume Next

Dim scriptResult        ' Script success or failure

Dim groupPath           ' ADsPath to the group container

Dim group               ' Group object

Dim memberPath          ' ADsPath to the member

Dim member              ' Member object

Dim groupMemberList     ' Used to display group members

Dim errorText           ' Error handing text

scriptResult = False

groupPath = "LDAP://fabrikam.com/CN=TestGroup,OU=TestOU,DC=fabrikam,DC=com"

memberPath = "LDAP://CN=JeffSmith,OU=TestOU,DC=fabrikam,DC=com"

WScript.Echo("Retrieving group object")

Set group = GetObject(groupPath)

If Err.number <> vbEmpty then

    Call ErrorHandler("Could not create group object.")

End If

Call ShowMembers(groupPath)     'Optional function call

WScript.Echo("Retrieving new member object")

Set member = GetObject(memberPath)

If Err.number <> vbEmpty then

    Call ErrorHandler("Could not get new member object.")

End If

WScript.Echo("Adding member to group.")

group.Add(member.ADsPath)

If Err.number <> vbEmpty then

    Call ErrorHandler("Could not add member to group.")

End If

Call ShowMembers(groupPath)     ' Optional function call

scriptResult = True

Call FinalResult(scriptResult)

'****************************************************************
' This function displays the members of a group. The function
' takes the ADsPath of the group.
'****************************************************************

Sub ShowMembers(groupPath)

    Dim groupMember

    Dim groupMemberList

    Dim groupObject

    Set groupObject = GetObject(groupPath)

    Set groupMemberList = groupObject.Members

    Select Case groupMemberList.Count

        Case 1 

            WScript.Echo vbcrlf & "The group has one member."

        Case 0

            WScript.Echo vbcrlf & "The group has no members."

        Case Else

            WScript.Echo vbcrlf & "The group has " & groupMemberList.Count & " members."

    End Select

    If groupMemberList.Count > 0 then

        WScript.Echo vbcrlf & "Here is a member list."

        For Each groupMember in groupMemberList

            WScript.Echo groupMember.Name

        Next

        WScript.Echo vbcrlf

    End If

    Set groupObject = Nothing

    Set groupMemberList = Nothing

End Sub

'****************************************************************
' This function shows if the script succeeded or failed. The 
' function processed the scriptResult variable.
'****************************************************************

Sub FinalResult(scriptResult)

    WScript.Echo vbcrlf

    If scriptResult = False then

        WScript.Echo "Script failed."

    Else

        WScript.Echo("Script successfully completed.")

    End If

    WScript.Quit

End Sub

'****************************************************************
' This function handles errors that occur in the script.
'****************************************************************

Sub ErrorHandler( errorText )

    WScript.Echo(vbcrlf & errorText)

    WScript.Echo("Error number: " & Err.number)

    WScript.Echo("Error Description: " & Err.Description)

    Err.Clear 

    Call FinalResult(scriptResult)

End Sub

```




O exemplo de código C++ a seguir adiciona um membro existente a um grupo.


```C++
/////////////////////////////////////////////////////////////
/*  AddMemberToGroup() - Adds the passed directory object as a member 
                         of passed group
 
    Parameters
 
        IADsGroup * pGroup   - Group to hold the new IDirectoryObject.
        IADs* pIADsNewMember - Object which will become a member 
                               of the group. Object can be a user, 
                               contact, or group.
*/
HRESULT AddMemberToGroup(IADsGroup * pGroup, IADs* pIADsNewMember)
{
    HRESULT hr = E_INVALIDARG;
    if ((!pGroup)||(!pIADsNewMember))
        return hr;
 
    // Use the IADs::get_ADsPath() member to get the ADsPath.
    // When the ADsPath string is returned, to add the new
    // member to the group, call the IADsGroup::Add() member,
    // passing in the ADsPath string.
    // Query the new member for its AdsPath.
    // This is a fully qualified LDAP path to the object to add.
    BSTR bsNewMemberPath;
    hr = pIADsNewMember->get_ADsPath(&bsNewMemberPath); 
    if (SUCCEEDED(hr))
    {
 
        // Use the IADsGroup interface to add the new member.
        // Pass the LDAP path to the 
        // new member to the IADsGroup::Add() member
        hr = pGroup->Add(bsNewMemberPath);
 
        // Free the string returned from IADs::get_ADsPath()
        SysFreeString(bsNewMemberPath);
    }
    return hr;
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Adicionando membros a grupos em um domínio](adding-members-to-groups-in-a-domain.md)
</dt> <dt>

[Directoryentry](/dotnet/api/system.directoryservices.directoryentry)
</dt> <dt>

[DirectoryEntry.CommitChanges](/dotnet/api/system.directoryservices.directoryentry.commitchanges#System_DirectoryServices_DirectoryEntry_CommitChanges)
</dt> <dt>

[**Iads**](/windows/desktop/api/iads/nn-iads-iads)
</dt> <dt>

[**IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup)
</dt> <dt>

[PropertyValueCollection.Add](/dotnet/api/system.directoryservices.propertyvaluecollection.add#System_DirectoryServices_PropertyValueCollection_Add_System_Object_)
</dt> </dl>

 

 