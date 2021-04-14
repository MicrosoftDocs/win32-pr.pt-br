---
title: Exemplo de código para determinar o modo de operação
description: Este tópico inclui um exemplo de código que lê a propriedade ntMixedDomain de um domínio e determina o modo de operação.
ms.assetid: 4ea1ddc5-6f48-45d3-9763-7ef0e6e704e3
ms.tgt_platform: multiple
keywords:
- Exemplos de Active Directory Active Directory, determinando o modo de operação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a059a750cf98efc066ac510c2c8acf58a65ab8c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104453506"
---
# <a name="example-code-for-determining-the-operation-mode"></a>Exemplo de código para determinar o modo de operação

Este tópico inclui um exemplo de código que lê a propriedade **ntMixedDomain** de um domínio e determina o modo de operação.

O exemplo de código C++ a seguir lê a propriedade **ntMixedDomain** de um domínio e determina o modo de operação.


```C++
HRESULT GetDomainMode(IADs *pDomain, BOOL *bIsMixed)
{
HRESULT hr = E_FAIL;
VARIANT var;
if (pDomain)
{
    VariantClear(&var);
 
    // Get the ntMixedDomain attribute.
    hr = pDomain->Get(CComBSTR("ntMixedDomain"), &var);
    if (SUCCEEDED(hr))
    {
 
        // Type should be VT_I4.
        if (var.vt==VT_I4)
        {
 
            // Zero means native mode.
            if (var.lVal == 0)
                *bIsMixed = FALSE;
 
            // One means mixed mode.
            else if (var.lVal == 1)
                *bIsMixed = TRUE;
            else
                hr=E_FAIL;
        }
    }
    VariantClear(&var);
}
return hr;
 
}
```



O exemplo de código a seguir Visual Basic lê a propriedade **ntMixedDomain** de um domínio e determina o modo de operação.


```VB
' Example: Detects if a domain is in mixed mode or native mode.
 
Dim IADsRootDSE As IADs
Dim IADsDomain As IADs
 
On Error Resume Next
sComputer = InputBox("This script detects if a Windows 2000 domain " _
                     & "is running in mixed or native mode." _
                     & vbCrLf & vbCrLf _
                     & "Specify the domain name or the name of a" _
                     & " domain controller in the domain :")
 
sPrefix = "LDAP://" & sComputer & "/"
 
''''''''''''''''''''
' Bind to a ds server
''''''''''''''''''''
Set IADsRootDSE = GetObject(sPrefix & "rootDSE")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method"
   Exit Sub
End If
sDomain = IADsRootDSE.Get("defaultNamingContext")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on Get method"
   Exit Sub
End If
Set IADsDomain = GetObject(sPrefix & sDomain)
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method"
   Exit Sub
End If
 
''''''''''''''''''''
' Get ntMixedDomain property
''''''''''''''''''''
sMode = IADsDomain.Get("ntMixedDomain")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on Get ntMixedDomain property"
   Exit Sub
End If
''''''''''''''''''''
' Get name property
''''''''''''''''''''
sName = IADsDomain.Get("name")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on Get name property"
   Exit Sub
End If
 
If (sMode = 0) Then
   sModeString = "Native"
ElseIf (sMode = 1) Then
   sModeString = "Mixed"
Else
   BailOnFailure sMode, "Invalid ntMixedDomain value: " & sMode
   Exit Sub
End If
 
 strText = "The domain " & sName & " is in " _
           & sModeString & " mode."
 
MsgBox strText
''''''''''''''''''''
' Display subroutines
''''''''''''''''''''
Sub show_groups(strText, strName)
    MsgBox strText, vbInformation, "Groups on " & strName
End Sub
 
Sub BailOnFailure(ErrNum, ErrText)   
    strText = "Error 0x" & Hex(ErrNum) & " " & ErrText
    MsgBox strText, vbInformation, "ADSI Error"
    WScript.Quit
End Sub
```



O exemplo de código a seguir Visual Basic Scripting Edition lê a propriedade **ntMixedDomain** de um domínio e determina o modo de operação.


```VB
' Example: Detects if a domain is in mixed mode or native mode.
 
Dim IADsRootDSE
Dim IADsDomain

On Error Resume Next
sComputer = InputBox("Specify the domain name or the name " _
                     & "of a domain controller in the domain :")
 
sPrefix = "LDAP://" & sComputer & "/"
 
''''''''''''''''''''
' Bind to a ds server
''''''''''''''''''''
Set IADsRootDSE = GetObject(sPrefix & "rootDSE")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method"
   Exit Sub
End If
sDomain = IADsRootDSE.Get("defaultNamingContext")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on Get method"
   Exit Sub
End If
Set IADsDomain = GetObject(sPrefix & sDomain)
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method"
   Exit Sub
End If
 
''''''''''''''''''''
' Get ntMixedDomain property
''''''''''''''''''''
sMode = IADsDomain.Get("ntMixedDomain")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on Get ntMixedDomain property"
   Exit Sub
End If
''''''''''''''''''''
' Get name property
''''''''''''''''''''
sName = IADsDomain.Get("name")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on Get name property"
   Exit Sub
End If
 
If (sMode = 0) Then
   sModeString = "Native"
ElseIf (sMode = 1) Then
   sModeString = "Mixed"
Else
   BailOnFailure sMode, "Invalid ntMixedDomain value: " & sMode
   Exit Sub
End If
 
 strText = "The domain " & sName & " is in " & sModeString & " mode."
 
MsgBox strText
''''''''''''''''''''
' Display subroutines
''''''''''''''''''''
Sub BailOnFailure(ErrNum, ErrText)    
    strText = "Error 0x" & Hex(ErrNum) & " " & ErrText
    MsgBox strText, vbInformation, "ADSI Error"
    WScript.Quit
End Sub
```



 

 




