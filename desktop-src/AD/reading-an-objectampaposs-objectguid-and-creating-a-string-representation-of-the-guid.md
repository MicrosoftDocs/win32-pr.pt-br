---
title: Lendo o objectGUID de um objeto e criando uma representação de cadeia de caracteres do GUID
description: Use o método IADs get \_ GUID para recuperar a forma de cadeia de caracteres vinculável do OBJECTguid de um objeto de diretório.
ms.assetid: 4f7f0e9d-3e06-47c9-83ce-cabed8692c15
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77bf9c346585e8604968c3f708dfdc62ee8d248f
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103640388"
---
# <a name="reading-an-objects-objectguid-and-creating-a-string-representation-of-the-guid"></a>Lendo o objectGUID de um objeto e criando uma representação de cadeia de caracteres do GUID

A propriedade **objectGUID** de cada objeto em Active Directory Domain Services é armazenada no diretório como uma cadeia de caracteres de octeto. Uma cadeia de caracteres de octeto é uma matriz de caracteres de um byte. Use o método [**IADs:: get \_ GUID**](/windows/desktop/ADSI/iads-property-methods) para recuperar a forma de cadeia de caracteres vinculável do **objectGUID** de um objeto de diretório.

Os exemplos de código a seguir mostram uma função que lê o atributo **objectGUID** e retorna uma representação de cadeia de caracteres do GUID usado para associar ao objeto.

-   [Exemplo de Visual Basic](#visual-basic-example)
-   [Exemplo de C++](#c-example)

## <a name="visual-basic-example"></a>Exemplo de Visual Basic


```VB
Dim sADsPathObject As String
Dim sObjectGUID As String
Dim sBindByGuidStr As String
 
Dim IADsObject As IADs
Dim IADsObject2 As IADs
On Error Resume Next
 
' Query the user for an ADsPath to start.
sADsPathObject = InputBox("This code binds to a directory object by ADsPath, retrieves the GUID, then rebinds by GUID." & vbCrLf & vbCrLf & "Specify the ADsPath of the object to bind to :")
 
If sADsPathObject = "" Then
    GoTo CleanUp
End If
 
MsgBox "Binding to " & sADsPathObject
 
' Bind to initial object.
Set IADsObject = GetObject(sADsPathObject)
 
If (Err.Number <> 0) Then
   MsgBox Err.Number & " on GetObject method"
   GoTo CleanUp
End If
 
' Save the GUID of the object.
sObjectGUID = IADsObject.Guid
 
MsgBox "The GUID for " & vbCrLf & vbCrLf & sADsPathObject & vbCrLf & vbCrLf & " is " & vbCrLf & vbCrLf & sObjectGUID
 
' Release the initial object.
Set IADsObject = Nothing
 
' Build a string for Binding to the object by GUID.
sBindByGuidStr = "LDAP://<GUID=" & sObjectGUID & ">"

MsgBox sBindByGuidStr
 
' Bind BACK to the Same object using the GUID.
Set IADsObject = GetObject(sBindByGuidStr)
 
If (Err.Number <> 0) Then
   MsgBox Err.Number & " on GetObject method "
   GoTo CleanUp
End If
 
MsgBox "Successfully RE bound to " & sADsPathObject & vbCrLf & vbCrLf & " using the path:" & vbCrLf & vbCrLf & sBindByGuidStr
 
' Release bind by GUID Object.
CleanUp:
   Set IADsObject = Nothing

```



## <a name="c-example"></a>Exemplo de C++


```C++
#define UNICODE
#include <ole2.h>
#include <stdio.h>
#include <activeds.h>

#define PATH_SIZE 1024

void wmain(int argc, wchar_t *argv[])
{
    // Initialize COM.
    CoInitialize(0);
     
    WCHAR wszADsPathObject[PATH_SIZE + 1];
    HRESULT hr;
    IADs *pIADsObject = NULL;
    IADs *pIADsObjectByGuid = NULL;
     
    // If no ADsPath was specified on the command line, query the user for a ADsPath to start.
    if(!argv[1])
    {
        _putws(L"This code binds to a directory object by ADsPath, retrieves the GUID,\n"
            L" then rebinds by GUID. \n\nEnter the ADsPath of the object to bind to :\n");
        fgetws(wszADsPathObject, PATH_SIZE, stdin);
    }
    else
    {
        wcsncpy_s(wszADsPathObject, argv[1], PATH_SIZE - 1);
        wszADsPathObject[PATH_SIZE] = 0;
    }
     
    if (!wszADsPathObject[0])
    {
        return;
    }
     
    wprintf(L"\nBinding to %s\n", wszADsPathObject);
     
    // Bind to initial object.
    hr = ADsGetObject(wszADsPathObject, IID_IADs, (void**)&pIADsObject);
    if (SUCCEEDED(hr))
    {
        BSTR bstrGuid = NULL;
        hr = pIADsObject->get_GUID(&bstrGuid); 
        
        if (SUCCEEDED(hr))
        {
            LPWSTR wszFormat = L"LDAP://<GUID=%s>";
            LPWSTR pwszBindByGuidStr; 

            wprintf(L"\n The GUID for\n\n%s\n\nis\n\n%s\n", wszADsPathObject, bstrGuid);
     
            // Build a string for Binding to the object by GUID.
            pwszBindByGuidStr = new WCHAR[wcslen(wszFormat) + wcslen(bstrGuid) + 1];
            if(pwszBindByGuidStr)
            {
                swprintf_s(pwszBindByGuidStr, wszFormat, bstrGuid);
         
                // Bind BACK to the Same object using the GUID.
                hr = ADsGetObject(pwszBindByGuidStr, IID_IADs, (void**)&pIADsObjectByGuid);
                 
                if (SUCCEEDED(hr))
                {
                    wprintf(L"\nSuccessfully re-bound to\n\n%s\n\nUsing the path:\n\n%s\n", 
                        wszADsPathObject, pwszBindByGuidStr);
         
                    // Release bind by GUID Object.
                    pIADsObjectByGuid->Release();
                    pIADsObjectByGuid = NULL;
                }

                delete pwszBindByGuidStr;
            }
            else
            {
                hr = E_OUTOFMEMORY;
            }
     
            SysFreeString(bstrGuid);
        }
     
        pIADsObject->Release();
        pIADsObject = NULL;
    }
     
    if (FAILED(hr))
    {
        wprintf(L"Failed");
    }
}
```



 

 