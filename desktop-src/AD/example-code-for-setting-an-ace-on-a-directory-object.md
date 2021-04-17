---
title: Código de exemplo para definir uma ACE em um objeto de diretório
description: Este tópico inclui vários exemplos de código que adicionam uma ACE (entrada de controle de acesso) à DACL (lista de controle de acesso discricionário) do descritor de segurança de um objeto de diretório.
ms.assetid: fb1ad9f5-af2f-4ad1-a58b-6439cca6fd23
ms.tgt_platform: multiple
keywords:
- Exemplos de Active Directory Active Directory, definindo uma ACE em um objeto de diretório
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e16180a2e1216c749c35d68ff607e81320a1482c
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "105762849"
---
# <a name="example-code-for-setting-an-ace-on-a-directory-object"></a><span data-ttu-id="94da0-104">Código de exemplo para definir uma ACE em um objeto de diretório</span><span class="sxs-lookup"><span data-stu-id="94da0-104">Example Code for Setting an ACE on a Directory Object</span></span>

## <a name="define-the-setright-function"></a><span data-ttu-id="94da0-105">Definir a função SetRight</span><span class="sxs-lookup"><span data-stu-id="94da0-105">Define the SetRight function</span></span>

<span data-ttu-id="94da0-106">O exemplo de código a seguir define uma função que adiciona uma ACE (entrada de controle de acesso) à DACL (lista de controle de acesso discricionário) do descritor de segurança de um objeto especificado no Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="94da0-106">The following code example defines a function that adds an Access Control Entry (ACE) to the Discretionary Access Control List (DACL) of the security descriptor of a specified object in Active Directory Domain Services.</span></span> <span data-ttu-id="94da0-107">A sub-rotina permite que você:</span><span class="sxs-lookup"><span data-stu-id="94da0-107">The subroutine enables you to:</span></span>

-   <span data-ttu-id="94da0-108">Conceder ou negar acesso ao objeto inteiro.</span><span class="sxs-lookup"><span data-stu-id="94da0-108">Grant or deny access to the entire object.</span></span>
-   <span data-ttu-id="94da0-109">Conceder ou negar acesso a uma propriedade específica no objeto.</span><span class="sxs-lookup"><span data-stu-id="94da0-109">Grant or deny access to a specific property on the object.</span></span>
-   <span data-ttu-id="94da0-110">Conceder ou negar acesso a um conjunto de propriedades no objeto.</span><span class="sxs-lookup"><span data-stu-id="94da0-110">Grant or deny access to a set of properties on the object.</span></span>
-   <span data-ttu-id="94da0-111">Conceda ou negue o direito de criar um tipo específico de objeto filho.</span><span class="sxs-lookup"><span data-stu-id="94da0-111">Grant or deny the right to create a specific type of child object.</span></span>
-   <span data-ttu-id="94da0-112">Defina uma ACE que possa ser herdada por todos os objetos filho ou por objetos filho de uma classe de objeto especificada.</span><span class="sxs-lookup"><span data-stu-id="94da0-112">Set an ACE that can be inherited by all child objects or by child objects of a specified object class.</span></span>

<span data-ttu-id="94da0-113">Seguir este Visual Basic exemplo de código são vários exemplos de código que mostram como usar a função **SetRight** para definir diferentes tipos de ACEs.</span><span class="sxs-lookup"><span data-stu-id="94da0-113">Following this Visual Basic code example are several code examples that show how to use the **SetRight** function to set different types of ACEs.</span></span>


```VB
Const ACL_REVISION_DS = &H4

Public Function SetRight(objectDN As String, _
               accessrights As Long, _
               accesstype As Long, _
               aceinheritflags As Long, _
               objectGUID As String, _
               inheritedObjectGUID As String, _
               trustee As String) As Boolean
             
Dim dsobject As IADs
Dim sd As IADsSecurityDescriptor
Dim dacl As IADsAccessControlList
Dim newace As New AccessControlEntry
Dim lflags As Long

On Error GoTo Cleanup
 
' Bind to the specified object.
Set dsobject = GetObject(objectDN)
 
' Read the security descriptor on the object.
Set sd = dsobject.Get("ntSecurityDescriptor")
 
' Get the DACL from the security descriptor.
Set dacl = sd.DiscretionaryAcl
 
' Set the properties of the new ACE.
newace.AccessMask = accessrights
newace.AceType = accesstype
newace.AceFlags = aceinheritflags
newace.trustee = trustee
 
' Set the GUID for the object type or inherited object type.
lflags = 0

If Not objectGUID = vbNullString Then
   newace.ObjectType = objectGUID
   lflags = lflags Or &H1 'ADS_FLAG_OBJECT_TYPE_PRESENT
End If

If Not inheritedObjectGUID = vbNullString Then
   newace.InheritedObjectType = inheritedObjectGUID
   lflags = lflags Or &H2 'ADS_FLAG_INHERITED_OBJECT_TYPE_PRESENT
End If

If Not (lflags = 0) Then newace.Flags = lflags
 
' Set the ACL Revision.
dacl.AclRevision = ACL_REVISION_DS

' Add the ACE to the DACL and to the security descriptor.
dacl.AddAce newace
sd.DiscretionaryAcl = dacl
 
' Apply it to the object.
dsobject.Put "ntSecurityDescriptor", sd
dsobject.SetInfo
SetRight = True
Exit Function

Cleanup:
Set dsobject = Nothing
Set sd = Nothing
Set dacl = Nothing
Set newace = Nothing
SetRight = False

End Function
```




```C++
HRESULT SetRight(
          IADs *pObject,
          long lAccessMask,
          long lAccessType,
          long lAccessInheritFlags,
          LPOLESTR szObjectGUID,
          LPOLESTR szInheritedObjectGUID,
          LPOLESTR szTrustee)
{
VARIANT varSD;
HRESULT hr = E_FAIL;
IADsAccessControlList *pACL = NULL;
IADsSecurityDescriptor *pSD = NULL;
IDispatch *pDispDACL = NULL;
IADsAccessControlEntry *pACE = NULL;
IDispatch *pDispACE = NULL;
long lFlags = 0L;
 
// The following code example takes the szTrustee in an expected naming format 
// and assumes it is the name for the correct trustee.
// The application should validate the specified trustee.
if (!szTrustee || !pObject)
    return E_INVALIDARG;
 
VariantInit(&varSD);
 
// Get the nTSecurityDescriptor.
// Type should be VT_DISPATCH - an IDispatch pointer to the security descriptor object.
hr = pObject->Get(_bstr_t("nTSecurityDescriptor"), &varSD);
if ( FAILED(hr) || varSD.vt != VT_DISPATCH ) {
    wprintf(L"get nTSecurityDescriptor failed: 0x%x\n", hr);
    return hr;
}
 
hr = V_DISPATCH( &varSD )->QueryInterface(IID_IADsSecurityDescriptor,(void**)&pSD);
if ( FAILED(hr) ) {
    wprintf(L"QueryInterface for IADsSecurityDescriptor failed: 0x%x\n", hr);
    goto cleanup;
}
 
// Get the DACL.
hr = pSD->get_DiscretionaryAcl(&pDispDACL);
if (SUCCEEDED(hr)) 
    hr = pDispDACL->QueryInterface(IID_IADsAccessControlList,(void**)&pACL);
if ( FAILED(hr) ) {
    wprintf(L"Could not get DACL: 0x%x\n", hr);
    goto cleanup;
}
 
// Create the COM object for the new ACE.
hr  = CoCreateInstance( 
               CLSID_AccessControlEntry,
               NULL,
               CLSCTX_INPROC_SERVER,
               IID_IADsAccessControlEntry,
               (void **)&pACE
               );
if ( FAILED(hr) ) {
    wprintf(L"Could not create ACE object: 0x%x\n", hr);
    goto cleanup;
}
 
// Set the properties for the new ACE.
 
// Set the mask that specifies the access right.
hr = pACE->put_AccessMask( lAccessMask );
 
// Set the trustee.
hr = pACE->put_Trustee( szTrustee );
 
// Set AceType.
hr = pACE->put_AceType( lAccessType );
 
// Set AceFlags to specify whether other objects can inherit the ACE from the specified object.
hr = pACE->put_AceFlags( lAccessInheritFlags );
 
// If an szObjectGUID is specified, add ADS_FLAG_OBJECT_TYPE_PRESENT 
// to the lFlags mask and set the ObjectType.
if (szObjectGUID)
{
    lFlags |= ADS_FLAG_OBJECT_TYPE_PRESENT;
    hr = pACE->put_ObjectType( szObjectGUID );
}
 
// If an szInheritedObjectGUID is specified, add ADS_FLAG_INHERITED_OBJECT_TYPE_PRESENT 
// to the lFlags mask and set the InheritedObjectType.
if (szInheritedObjectGUID)
{
    lFlags |= ADS_FLAG_INHERITED_OBJECT_TYPE_PRESENT;
    hr = pACE->put_InheritedObjectType( szInheritedObjectGUID );
}
 
// Set flags if ObjectType or InheritedObjectType were set.
if (lFlags)
    hr = pACE->put_Flags(lFlags);
 
// Add the ACE to the ACL to the SD to the cache to the object.
// Call the QueryInterface method for the IDispatch pointer to pass to the AddAce method.
hr = pACE->QueryInterface(IID_IDispatch, (void**)&pDispACE);
if (SUCCEEDED(hr))
{
    // Set the ACL revision.
    hr = pACL->put_AclRevision(ACL_REVISION_DS);

    // Add the ACE.
    hr = pACL->AddAce(pDispACE);
    if (SUCCEEDED(hr))
    {
        // Write the DACL.
        hr = pSD->put_DiscretionaryAcl(pDispDACL);
        if (SUCCEEDED(hr))
        {
            // Write the ntSecurityDescriptor property to the property cache.
            hr = pObject->Put(CComBSTR("nTSecurityDescriptor"), varSD);
            if (SUCCEEDED(hr))
            {
                // Call SetInfo to update the property on the object in the directory.
                hr = pObject->SetInfo();
            }
        }
    }
}
 
cleanup:
if (pDispACE)
    pDispACE->Release();
if (pACE)
    pACE->Release();
if (pACL)
    pACL->Release();
if (pDispDACL)
    pDispDACL->Release();
if (pSD)
    pSD->Release();
 
VariantClear(&varSD);
return hr;
}
```



## <a name="grant-or-deny-access-to-the-entire-object"></a><span data-ttu-id="94da0-114">Conceder ou negar acesso ao objeto inteiro</span><span class="sxs-lookup"><span data-stu-id="94da0-114">Grant or deny access to the entire object</span></span>

<span data-ttu-id="94da0-115">O exemplo de código a seguir Visual Basic cria uma cadeia de vinculação para o contêiner Usuários e, em seguida, chama a função **SetRight** para definir uma ACE no contêiner Users.</span><span class="sxs-lookup"><span data-stu-id="94da0-115">The following Visual Basic code example builds a binding string for the Users container and then calls the **SetRight** function to set an ACE on the Users container.</span></span> <span data-ttu-id="94da0-116">Este exemplo define uma ACE que concede ao objeto de confiança o direito de leitura ou gravação de qualquer propriedade em Object.</span><span class="sxs-lookup"><span data-stu-id="94da0-116">This example sets an ACE that grants the trustee the right to read or write any property on the object.</span></span>


```VB
Dim rootDSE As IADs
Dim objectDN As String
Dim bResult As Boolean
Const ADS_RIGHT_READ_PROP = &H10
Const ADS_RIGHT_WRITE_PROP = &H20
 
' Bind to the Users container in the local domain.
Set rootDSE = GetObject("LDAP://rootDSE")
objectDN = "LDAP://cn=users," & rootDSE.Get("defaultNamingContext")
 
' Grant trustee the right to read/write any property.
bResult = SetRight objectDN, _
  ADS_RIGHT_READ_PROP Or ADS_RIGHT_WRITE_PROP, _
   ADS_ACETYPE_ACCESS_ALLOWED, _
    0, _
    vbNullString, _
    vbNullString, _
    "someone@fabrikam.com" ' Trustee

If bResult = True Then
    MsgBox ("The trustee can read or write any property.")
Else
    MsgBox ("An error occurred.")
End If
```



<span data-ttu-id="94da0-117">O exemplo de código C++ a seguir define uma ACE que concede a permissão de confiança para ler ou gravar qualquer propriedade no objeto.</span><span class="sxs-lookup"><span data-stu-id="94da0-117">The following C++ code example sets an ACE that grants the trustee permission to read or write any property on the object.</span></span> <span data-ttu-id="94da0-118">O exemplo de código supõe que *pObject* e *szTrustee* são definidos como valores válidos.</span><span class="sxs-lookup"><span data-stu-id="94da0-118">The code example assumes that *pObject* and *szTrustee* are set to valid values.</span></span> <span data-ttu-id="94da0-119">Para obter mais informações, consulte [definindo direitos de acesso em um objeto](setting-access-rights-on-an-object.md).</span><span class="sxs-lookup"><span data-stu-id="94da0-119">For more information, see [Setting Access Rights on an Object](setting-access-rights-on-an-object.md).</span></span>


```C++
HRESULT hr;
IADs *pObject;
LPWSTR szTrustee;
 
hr = SetRight(
          pObject,  // IADs pointer to the object
          ADS_RIGHT_READ_PROP | ADS_RIGHT_WRITE_PROP,
          ADS_ACETYPE_ACCESS_ALLOWED,
          0,        // Not inheritable
          NULL,     // No object type GUID
          NULL,     // No inherited object type GUID
          szTrustee
          );
```



## <a name="grant-or-deny-access-to-a-specific-property-on-the-object"></a><span data-ttu-id="94da0-120">Conceder ou negar acesso a uma propriedade específica no objeto</span><span class="sxs-lookup"><span data-stu-id="94da0-120">Grant or deny access to a specific property on the object</span></span>

<span data-ttu-id="94da0-121">Este exemplo de código chama a função **SetRight** para conceder ao objeto de confiança o direito de leitura ou gravação de uma propriedade específica sobre ele.</span><span class="sxs-lookup"><span data-stu-id="94da0-121">This code example calls the **SetRight** function to grant the trustee the right to read or write a specific property on the object.</span></span> <span data-ttu-id="94da0-122">Lembre-se de que você deve especificar o **schemaIDGUID** da propriedade e especificar o **\_ objeto de \_ acesso \_ permitido \_ pelo ADS ACETYPE** para indicar que se trata de uma ACE específica do objeto.</span><span class="sxs-lookup"><span data-stu-id="94da0-122">Be aware that you must specify the **schemaIDGUID** of the property and you must specify **ADS\_ACETYPE\_ACCESS\_ALLOWED\_OBJECT** to indicate that this is an object-specific ACE.</span></span> <span data-ttu-id="94da0-123">Este exemplo de código também especifica o sinalizador **\_ \_ \_ Ace ACEFLAG de herança do ADS** , que indica que a Ace pode ser herdada por objetos filho.</span><span class="sxs-lookup"><span data-stu-id="94da0-123">This code example also specifies the **ADS\_ACEFLAG\_INHERIT\_ACE** flag which indicates that the ACE can be inherited by child objects.</span></span>


```VB
' Grant trustee the right to read the Telephone-Number property
' of all child objects in the Users container. 
' {bf967a49-0de6-11d0-a285-00aa003049e2} is the schemaIDGUID of 
' the Telephone-Number property.

bResult = SetRight objectDN, _
     ADS_RIGHT_WRITE_PROP Or ADS_RIGHT_READ_PROP, _
     ADS_ACETYPE_ACCESS_ALLOWED_OBJECT, _
      ADS_ACEFLAG_INHERIT_ACE, _
       "{bf967a49-0de6-11d0-a285-00aa003049e2}", _
       vbNullString, _
       "someone@fabrikam.com" ' Trustee

If bResult = True Then
    MsgBox ("The trustee can read the telephone number property.")
Else
    MsgBox ("An error occurred.")
End If
```




```C++
// Grant trustee the right to read the Telephone-Number property
// of all child objects in the Users container. 
// {bf967a49-0de6-11d0-a285-00aa003049e2} is the schemaIDGUID of 
// the Telephone-Number property.
hr = SetRight(
          pObject,  // IADs pointer to the object.
          ADS_RIGHT_READ_PROP | ADS_RIGHT_WRITE_PROP,
          ADS_ACETYPE_ACCESS_ALLOWED_OBJECT,
          ADS_ACEFLAG_INHERIT_ACE,
          L"{bf967a49-0de6-11d0-a285-00aa003049e2}",
          NULL,     // No inherited object type GUID.
          szTrustee
          );
```



## <a name="grant-or-deny-access-to-a-set-of-properties-on-the-object"></a><span data-ttu-id="94da0-124">Conceder ou negar acesso a um conjunto de propriedades no objeto</span><span class="sxs-lookup"><span data-stu-id="94da0-124">Grant or deny access to a set of properties on the object</span></span>

<span data-ttu-id="94da0-125">Este exemplo de código chama a função **SetRight** para conceder ao objeto de confiança o direito de leitura ou gravação de um conjunto específico de propriedades em Object.</span><span class="sxs-lookup"><span data-stu-id="94da0-125">This code example calls the **SetRight** function to grant the trustee the right to read or write a specific set of properties on the object.</span></span> <span data-ttu-id="94da0-126">Especifique **o \_ \_ \_ \_ objeto de acesso permitido pelo ADS ACETYPE** para indicar que se trata de uma ACE específica do objeto.</span><span class="sxs-lookup"><span data-stu-id="94da0-126">Specify **ADS\_ACETYPE\_ACCESS\_ALLOWED\_OBJECT** to indicate that this is an object-specific ACE.</span></span>

<span data-ttu-id="94da0-127">Um conjunto de propriedades é definido por um objeto **controlAccessRight** no contêiner de direitos estendidos da partição de configuração.</span><span class="sxs-lookup"><span data-stu-id="94da0-127">A property set is defined by a **controlAccessRight** object in the Extended Rights container of the Configuration partition.</span></span> <span data-ttu-id="94da0-128">Para identificar o conjunto de propriedades na ACE, especifique a propriedade **rightsGUID** de um objeto **controlAccessRight** .</span><span class="sxs-lookup"><span data-stu-id="94da0-128">To identify the property set in the ACE, specify the **rightsGUID** property of a **controlAccessRight** object.</span></span> <span data-ttu-id="94da0-129">Lembre-se de que esse GUID do conjunto de propriedades também é definido na propriedade **attributeSecurityGUID** de todos os objetos **attributeSchema** incluídos no conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="94da0-129">Be aware that this property set GUID is also set in the **attributeSecurityGUID** property of every **attributeSchema** object included in the property set.</span></span> <span data-ttu-id="94da0-130">Para obter mais informações, consulte [controlar direitos de acesso](control-access-rights.md).</span><span class="sxs-lookup"><span data-stu-id="94da0-130">For more information, see [Control Access Rights](control-access-rights.md).</span></span>

<span data-ttu-id="94da0-131">Este exemplo de código também especifica sinalizadores de herança que definem a ACE como herdável por objetos filho, mas ineficaz no objeto imediato.</span><span class="sxs-lookup"><span data-stu-id="94da0-131">This code example also specifies inheritance flags that set the ACE as inheritable by child objects, but ineffective on the immediate object.</span></span> <span data-ttu-id="94da0-132">Além disso, o exemplo especifica o GUID da classe User, que indica que a ACE pode ser herdada somente por objetos dessa classe.</span><span class="sxs-lookup"><span data-stu-id="94da0-132">In addition, the sample specifies the GUID of the User class, which indicates that the ACE can be inherited only by objects of that class.</span></span>


```VB
' Grant trustee permission to read or write a set of properties.
' {77B5B886-944A-11d1-AEBD-0000F80367C1} is a GUID that identifies 
' a property set.
' {bf967aba-0de6-11d0-a285-00aa003049e2} is a GUID that identifies the
' User class, so this ACE is inherited only by objects of that class.

bResult = SetRight objectDN, _
        ADS_RIGHT_READ_PROP Or ADS_RIGHT_WRITE_PROP, _
          ADS_ACETYPE_ACCESS_ALLOWED_OBJECT, _
          ADS_ACEFLAG_INHERIT_ACE Or ADS_ACEFLAG_INHERIT_ONLY_ACE, _
          "{77B5B886-944A-11d1-AEBD-0000F80367C1}", _
          "{bf967aba-0de6-11d0-a285-00aa003049e2}", _
          "someone@fabrikam.com" ' Trustee

If bResult = True Then
    MsgBox ("The trustee can read or write a set of properties.")
Else
    MsgBox ("An error occurred.")
End If
```




```C++
// Grant trustee the right to read or write a set of properties.
// {77B5B886-944A-11d1-AEBD-0000F80367C1} is a GUID that identifies 
// a property set (rightsGUID of a controlAccessRight object).
// {bf967aba-0de6-11d0-a285-00aa003049e2} is the schemaIDGUID of the
// User class, so this ACE is inherited only by objects of that class.
hr = SetRight(
          pObject,  // IADs pointer to the object.
          ADS_RIGHT_READ_PROP | ADS_RIGHT_WRITE_PROP,
          ADS_ACETYPE_ACCESS_ALLOWED_OBJECT,
          ADS_ACEFLAG_INHERIT_ACE | ADS_ACEFLAG_INHERIT_ONLY_ACE,
          L"{77B5B886-944A-11d1-AEBD-0000F80367C1}",
          L"{bf967aba-0de6-11d0-a285-00aa003049e2}",
          szTrustee
          );
```



## <a name="grant-or-deny-permission-to-create-a-specific-type-of-child-object"></a><span data-ttu-id="94da0-133">Conceder ou negar permissão para criar um tipo específico de objeto filho</span><span class="sxs-lookup"><span data-stu-id="94da0-133">Grant or deny permission to create a specific type of child object</span></span>

<span data-ttu-id="94da0-134">O exemplo de código a seguir chama a função **SetRight** para conceder a um confiável especificado o direito de criar e excluir objetos de usuário na subárvore sob o objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="94da0-134">The following code example calls the **SetRight** function to grant a specified trustee the right to create and delete User objects in the subtree under the specified object.</span></span> <span data-ttu-id="94da0-135">Lembre-se de que o exemplo especifica o GUID da classe de usuário, o que significa que a ACE permite que apenas o objeto de confiança Crie objetos de usuário, não objetos de outras classes.</span><span class="sxs-lookup"><span data-stu-id="94da0-135">Be aware that the sample specifies the GUID of the User class, which means that the ACE allows only the trustee to create User objects, not objects of other classes.</span></span> <span data-ttu-id="94da0-136">Especifique **o \_ \_ \_ \_ objeto de acesso permitido pelo ADS ACETYPE** para indicar que se trata de uma ACE específica do objeto.</span><span class="sxs-lookup"><span data-stu-id="94da0-136">Specify **ADS\_ACETYPE\_ACCESS\_ALLOWED\_OBJECT** to indicate that this is an object-specific ACE.</span></span>


```VB
' Grant trustee the right to create or delete User objects 
' in the specified object. 
' {bf967aba-0de6-11d0-a285-00aa003049e2} is a GUID that identifies the
' User class.

bResult = SetRight objectDN, _
          ADS_RIGHT_DS_CREATE_CHILD Or ADS_RIGHT_DS_DELETE_CHILD, _
           ADS_ACETYPE_ACCESS_ALLOWED_OBJECT, _
           0, _
           "{bf967aba-0de6-11d0-a285-00aa003049e2}", _
           vbNullString, _
           "jeffsmith@fabrikam.com" 'trustee

If bResult = True Then
    MsgBox ("The trustee can create or delete User objects.")
Else
    MsgBox ("An error occurred.")
End If
```




```C++
// Grant trustee the right to create or delete User objects 
// in the specified object. 
// {bf967aba-0de6-11d0-a285-00aa003049e2} is the schemaIDGUID of the
// User class.
hr = SetRight(
          pObject,  // IADs pointer to the object.
          ADS_RIGHT_DS_CREATE_CHILD | ADS_RIGHT_DS_DELETE_CHILD,
          ADS_ACETYPE_ACCESS_ALLOWED_OBJECT,
          0,        // Not inheritable.
          L"{bf967aba-0de6-11d0-a285-00aa003049e2}",
          NULL,     // No inherited object type GUID.
          szTrustee
          );
```



<span data-ttu-id="94da0-137">Para obter mais informações e o **schemaIDGUID** de um atributo ou classe predefinido, consulte a página referência de atributo ou classe na referência de [esquema de Active Directory](/windows/desktop/ADSchema/active-directory-schema) .</span><span class="sxs-lookup"><span data-stu-id="94da0-137">For more information, and the **schemaIDGUID** of a predefined attribute or class, see the attribute or class reference page in the [Active Directory Schema](/windows/desktop/ADSchema/active-directory-schema) reference.</span></span> <span data-ttu-id="94da0-138">Para obter mais informações e um exemplo de código que pode ser usado para obter um **schemaIDGUID** de forma programática, consulte [lendo objetos attributeSchema e classSchema](reading-attributeschema-and-classschema-objects.md).</span><span class="sxs-lookup"><span data-stu-id="94da0-138">For more information, and a code example that can be used to obtain a **schemaIDGUID** programmatically, see [Reading attributeSchema and classSchema Objects](reading-attributeschema-and-classschema-objects.md).</span></span>

 

 