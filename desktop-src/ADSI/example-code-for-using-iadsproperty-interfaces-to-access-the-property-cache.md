---
title: Código de exemplo para usar interfaces IADsproperty para acessar o cache de propriedades
description: O exemplo de código a seguir mostra como usar as interfaces IADsPropertyList, IADsPropertyEntry e IADsPropertyValue com C++ e ADSI.
ms.assetid: d2ac3a1e-642c-451c-a79e-baa38dacb4a2
ms.tgt_platform: multiple
keywords:
- Código de exemplo ADSI, usando as interfaces IADsproperty para acessar o cache de propriedades
- Código de exemplo para usar interfaces IADsproperty para acessar a ADSI do cache de propriedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2053e3d78120e39cb7a377eaf6e50524bb780c34
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105755264"
---
# <a name="example-code-for-using-iadsproperty-interfaces-to-access-the-property-cache"></a><span data-ttu-id="f15bb-105">Código de exemplo para usar interfaces IADsproperty para acessar o cache de propriedades</span><span class="sxs-lookup"><span data-stu-id="f15bb-105">Example Code for Using IADsProperty Interfaces to Access the Property Cache</span></span>

<span data-ttu-id="f15bb-106">O exemplo de código a seguir mostra como usar as interfaces [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist), [**IADsPropertyEntry**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry)e [**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) com C++ e ADSI.</span><span class="sxs-lookup"><span data-stu-id="f15bb-106">The following code example shows how to use the [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist), [**IADsPropertyEntry**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry), and [**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) interfaces with C++ and ADSI.</span></span>


```C++
HRESULT hr;
BSTR    bstr;
VARIANT var;
IDispatch *pDispatch;
IADsPropertyList *pPropList;
IADsPropertyEntry *pEntry;
IADsPropertyValue *pValue;
LONG  lADsType;
IADs *pADs=NULL;
 
//////////////////////////////////////////////////////////
// Be aware that, for brevity, error handling is omitted.
//////////////////////////////////////////////////////////
 
hr = ADsGetObject(L"LDAP://DC=Sales,DC=Fabrikam,DC=Com", IID_IADs, (void**) &pADs);
 
///////////////////////////////////////////////////////////////////
// Retrieve objects prior to calling IADsProperty* methods.
///////////////////////////////////////////////////////////////////
hr = pADs->GetInfo();
hr = pADs->QueryInterface(IID_IADsPropertyList, (void**) &pPropList);
pADs->Release();
 
//////////////////////////////////////////////////
// Get the DC property.
//////////////////////////////////////////////////
hr = pPropList->GetPropertyItem(CComBSTR("dc"), ADSTYPE_CASE_IGNORE_STRING, &var);
 
if (SUCCEEDED(hr))
{
    //////////////////////////////////////////
    // Get the IADsPropertyEntry interface.
    //////////////////////////////////////////
    pDispatch = V_DISPATCH( &var );
    hr = pDispatch->QueryInterface(IID_IADsPropertyEntry, (void**)&pEntry);
    VariantClear(&var);
 
    if (SUCCEEDED(hr))
    {
        VARIANT  varValueArray;
        VARIANT  varValue;
        long   idx=0;
 
        ///////////////////////////////////////////////
        // get_Values return array of VT_DISPATCH.
        ///////////////////////////////////////////////
        hr = pEntry->get_Values(&varValueArray);
        hr = pEntry->get_ADsType(&lADsType);
        hr = SafeArrayGetElement(V_ARRAY(&varValueArray), &idx, &varValue);
        pEntry->Release();  // Release entry.
 
        /////////////////////////////////////
        // IADsPropertyValue
        /////////////////////////////////////
        pDispatch = (IDispatch*) V_DISPATCH(&varValue);
        hr = pDispatch->QueryInterface(IID_IADsPropertyValue, 
                                       (void**) &pValue);
        pDispatch->Release();
 
        /////////////////////////////
        // Display the value.
        /////////////////////////////
        hr = pValue->get_CaseIgnoreString(&bstr);
        printf("%S\n", bstr);
        SysFreeString(bstr);
        pValue->Release();
    } 
}
```



<span data-ttu-id="f15bb-107">O exemplo de código a seguir mostra como usar as interfaces [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist), [**IADsPropertyEntry**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry)e [**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) usando Visual Basic e ADSI.</span><span class="sxs-lookup"><span data-stu-id="f15bb-107">The following code example shows how to use the [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist), [**IADsPropertyEntry**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry), and [**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) interfaces using Visual Basic and ADSI.</span></span>


```VB
Dim propList As IADsPropertyList
Dim propEntry As IADsPropertyEntry
Dim propVal As IADsPropertyValue
Dim count As Long
 
Set propList = GetObject("LDAP://dc01/DC=Fabrikam,DC=com")
 
propList.GetInfo
count = propList.PropertyCount
Debug.Print "No of Property Found: " & count
 
For i = 0 To count - 1
    ' Each item in the property list has a property entry.
    Set propEntry = propList.Item(i)
    Debug.Print propEntry.Name
    Debug.Print propEntry.ADsType
    
    ' Each value in property entry has property values.
    For Each v In propEntry.Values
        Set propVal = v
        Debug.Print propVal.ADsType
    Next
Next
```



 

 




