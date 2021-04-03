---
title: O método Put
description: Salva o valor de uma propriedade de um Active Directory objeto pelo nome no cache de propriedades.
ms.assetid: 8534ceba-5fcb-441f-9e76-3060319478af
ms.tgt_platform: multiple
keywords:
- Colocar ADSI, sobre
- ADSI ADSI, exemplo de código Visual Basic, usando o método Put
- Propriedades ADSI, salvando um valor para uma propriedade no cache de propriedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a64a5cba8056f8eac0125fc5b32fd66bdf988dae
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822179"
---
# <a name="the-put-method"></a><span data-ttu-id="1ec47-106">O método Put</span><span class="sxs-lookup"><span data-stu-id="1ec47-106">The Put Method</span></span>

<span data-ttu-id="1ec47-107">O método [**IADs::P UT**](/windows/desktop/api/Iads/nf-iads-iads-put) salva o valor de uma propriedade para um objeto Active Directory pelo nome no cache de propriedades.</span><span class="sxs-lookup"><span data-stu-id="1ec47-107">The [**IADs::Put**](/windows/desktop/api/Iads/nf-iads-iads-put) method saves the value for a property for an Active Directory object by name into the property cache.</span></span> <span data-ttu-id="1ec47-108">Use [**IADs::P utex**](/windows/desktop/api/Iads/nf-iads-iads-putex) para salvar propriedades de valores múltiplos no cache de propriedades ou para remover uma propriedade de um objeto.</span><span class="sxs-lookup"><span data-stu-id="1ec47-108">Use [**IADs::PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex) to save multi-valued properties to the property cache, or to remove a property from an object.</span></span> <span data-ttu-id="1ec47-109">Esses valores não são persistidos no serviço de diretório subjacente até que [**IADs:: setinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) seja chamado.</span><span class="sxs-lookup"><span data-stu-id="1ec47-109">These values are not persisted to the underlying directory service until [**IADs::SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) is called.</span></span>


```VB
Dim Namespace As IADsOpenDSObject
Dim User As IADsUser
Dim NewName As Variant
Dim sUserName As String
Dim sPassword As String

On Error GoTo CleanUp
 
Set Namespace = GetObject("LDAP:")

' Insert code to safely get the user name and password
 
Set User = Namespace.OpenDSObject("LDAP://MyMachine/CN=Administrator,CN=Users,DC=MyDomain,DC=Fabrikam,DC=COM", sUserName, sPassword, ADS_SECURE_AUTHENTICATION)
 
NewName = InputBox("Enter a new name:")
 
' Set using IADs::PutMethod
User.Put "FullName", NewName
User.SetInfo

Exit Sub

CleanUp:
    Set IADsOpenDSObject = Nothing
    Set IADsUser = Nothing

End Sub
```



<span data-ttu-id="1ec47-110">O exemplo de código a seguir mostra como usar [**IADs::P UT**](/windows/desktop/api/Iads/nf-iads-iads-put) com um único valor:</span><span class="sxs-lookup"><span data-stu-id="1ec47-110">The following code example shows how to use [**IADs::Put**](/windows/desktop/api/Iads/nf-iads-iads-put) with a single value:</span></span>


```VB
Dim x As IADs
Dim sUserName As String
Dim sFull As String

On Error GoTo CleanUp

sUserName = InputBox("Enter your user name:")
 
Set x = GetObject("LDAP://CN="& sUserName &",CN=Users,DC=Fabrikam, DC=Com") 

sFull = InputBox ("Enter your full name:")
x.Put "name", sFull
 
' Commit to the directory.
x.SetInfo

Exit Sub

CleanUp:
    MsgBox ("An error has occurred. " & Err.Description)
    Set x = Nothing
```



<span data-ttu-id="1ec47-111">O exemplo de código a seguir mostra como usar [**IADs::P UT**](/windows/desktop/api/Iads/nf-iads-iads-put) com vários valores:</span><span class="sxs-lookup"><span data-stu-id="1ec47-111">The following code example shows how to use [**IADs::Put**](/windows/desktop/api/Iads/nf-iads-iads-put) with multiple values:</span></span>


```VB
Dim x As IADs
Dim sFirst As String
Dim sLast As String
Dim sUsername As String

On Error GoTo CleanUp

sUsername = InputBox("User name:")
 
Set x = GetObject("LDAP://CN=" & sUsername & ", CN=Users,DC=Fabrikam, DC=Com")

sFirst = InputBox("Enter your first name:")
sLast = InputBox("Enter your last name:")
 
x.Put "givenName", sFirst
x.Put "sn", sLast
 
'Commit to the directory
x.SetInfo

Exit Sub

CleanUp:
    MsgBox ("An error has occurred. " & Err.Description)
    Set x = Nothing
```



<span data-ttu-id="1ec47-112">O exemplo de código a seguir mostra como usar [**IADs::P UT**](/windows/desktop/api/Iads/nf-iads-iads-put) com valores múltiplos e únicos:</span><span class="sxs-lookup"><span data-stu-id="1ec47-112">The following code example shows how to use [**IADs::Put**](/windows/desktop/api/Iads/nf-iads-iads-put) with both multiple and single values:</span></span>


```C++
int main(int argc, char* argv[], LPWSTR pszADsPath)
{
   HRESULT hr;
   IADs *pADs=NULL;

   CoInitialize(NULL);

   hr = ADsGetObject(pszADsPath,
                     IID_IADs, 
                    (void**) &pADs );

   if (!SUCCEEDED(hr) )
   {
     return hr;
   }

   VARIANT var;
 
   // Using Put with a single value for the first name
   VariantInit(&var);
   V_BSTR(&var) = SysAllocString(L"Janet");
   V_VT(&var) = VT_BSTR;
   hr = pADs->Put( L"givenName", var );

   // Using Put with a single value for the last name
   VariantClear(&var);
   V_BSTR(&var) = SysAllocString(L"Johns");
   V_VT(&var) = VT_BSTR;
   hr = pADs->Put( L"sn", var ); 
   VariantClear(&var);

   // Using Put with multiple values for other telephones
   LPWSTR pszPhones[] = { L"425 844 1234", L"425 924 4321" };
   DWORD dwNumber = sizeof( pszPhones ) /sizeof(LPWSTR);

   hr = ADsBuildVarArrayStr( pszPhones, dwNumber, &var );
   hr = pADs->Put( L"otherTelephone", var ); 
   VariantClear(&var);

   hr = pADs->SetInfo();
   pADs->Release();

   if (!SUCCEEDED(hr) )
   {
     return hr;
   }

 CoUninitialize();
 return 0;
}
```



 

 




