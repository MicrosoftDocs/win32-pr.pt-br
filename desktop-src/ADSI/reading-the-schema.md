---
title: Lendo o esquema
description: A maioria dos provedores oferece suporte ao esquema fornecido com o Active Directory.
ms.assetid: cc35789e-5cfe-49e9-9fb3-489b949768c5
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2091d225c1be90d887f6994eda782ad7a7adb65
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822188"
---
# <a name="reading-the-schema"></a><span data-ttu-id="eb0bb-103">Lendo o esquema</span><span class="sxs-lookup"><span data-stu-id="eb0bb-103">Reading the Schema</span></span>

<span data-ttu-id="eb0bb-104">A maioria dos provedores oferece suporte ao esquema fornecido com o Active Directory.</span><span class="sxs-lookup"><span data-stu-id="eb0bb-104">Most providers support the schema that is shipped with Active Directory.</span></span> <span data-ttu-id="eb0bb-105">O esquema contém definições de classe e de atributo.</span><span class="sxs-lookup"><span data-stu-id="eb0bb-105">The schema contains class and attribute definitions.</span></span> <span data-ttu-id="eb0bb-106">A ADSI abstrai o esquema em "Provider://schema".</span><span class="sxs-lookup"><span data-stu-id="eb0bb-106">ADSI abstracts the schema in "Provider://schema".</span></span> <span data-ttu-id="eb0bb-107">Cada objeto transporta o local do esquema no qual sua classe é definida.</span><span class="sxs-lookup"><span data-stu-id="eb0bb-107">Each object carries the schema location in which its class is defined.</span></span> <span data-ttu-id="eb0bb-108">Você pode usar o método [**IADs:: get \_ Class**](iads-property-methods.md) Property para obter essas informações.</span><span class="sxs-lookup"><span data-stu-id="eb0bb-108">You can use the [**IADs::get\_Class**](iads-property-methods.md) property method to obtain this information.</span></span>

<span data-ttu-id="eb0bb-109">Para associar ao contêiner de esquema em um domínio específico, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="eb0bb-109">To bind to the schema container on a particular domain, do the following:</span></span>


```VB
Dim SchemaContainer As Object
Set SchemaContainer = GetObject("LDAP://Fabrikam/Schema")
```


```C++

hr = ADsGetObject(L&quot;LDAP://Fabrikam/Schema&quot;, IID_IADsContainer, (void**) &pSchema );
```





<span data-ttu-id="eb0bb-110">Para listar informações no contêiner de esquema, associe-se ao contêiner e enumere cada objeto no contêiner, conforme mostrado a seguir:</span><span class="sxs-lookup"><span data-stu-id="eb0bb-110">To list information in the schema container, bind to the container and enumerate each object in the container as shown in the following:</span></span>


```VB
Dim prop As Object
Dim obj As Object
Dim SchemaContainer As Object
Dim Class As Object

Set SchemaContainer = GetObject("LDAP://Fabrikam/Schema")
'Show all items in the schema container
For Each obj In SchemaContainer
     Debug.Print obj.Name & " (" & obj.Class & ")"
Next

'Show the optional attributes
For Each prop In Class.OptionalProperties
   Debug.Print prop
Next
```


```C++

IADsContainer *pSchema=NULL;
 HRESULT hr;

 CoInitialize(NULL);

 hr = ADsGetObject(L&quot;LDAP://Fabrikam/Schema&quot;, 
                   IID_IADsContainer, (void**) &pSchema );

 if ( !SUCCEEDED(hr) )
 {
   return hr;
 }

 // Enumerate schema objects
 IEnumVARIANT *pEnum = NULL;
 hr = ADsBuildEnumerator( pSchema, &pEnum );
 pSchema->Release(); // This is no longer needed, since we have the enumerator already.
    
 if ( SUCCEEDED(hr) )
 {
   VARIANT var;
   ULONG lFetch;
   IADs *pChild=NULL;
   VariantInit(&var);
        
   while( SUCCEEDED(ADsEnumerateNext( pEnum, 1, &var, &lFetch )) && lFetch == 1 )
   {
     hr = V_DISPATCH(&var)->QueryInterface( IID_IADs, (void**) &pChild );
     if ( SUCCEEDED(hr) )
     {
       BSTR bstrName;
       BSTR bstrClass;
       // Get more information on the child classes
       pChild->get_Name(&bstrName);
       pChild->get_Class(&bstrClass);
                
       printf(&quot;%S\t\t(%S)\n&quot;, bstrName, bstrClass );
                
       // Clean-up
       SysFreeString(bstrName);
       SysFreeString(bstrClass);
                
       pChild->Release();
     }
     VariantClear(&var);
   }
 }

 CoUninitialize();
```





<span data-ttu-id="eb0bb-111">Você também pode associar a um objeto e obter o local do esquema, conforme mostrado a seguir:</span><span class="sxs-lookup"><span data-stu-id="eb0bb-111">You can also bind to an object and get the schema location, as shown in the following:</span></span>


```VB
Dim prop As Object
Dim dom As Object
Dim Class As Object

Set dom = GetObject("LDAP://Fabrikam")
Debug.Print dom.Schema
Set Class = GetObject(dom.Schema)
'Mandatory attributes
For Each prop In Class.MandatoryProperties
    Debug.Print prop
Next
```



 

 




