---
title: Código de exemplo para verificar se há direitos para criar objetos de esquema
description: O exemplo de código C/C++ a seguir mostra uma função que verifica o atributo allowedChildClassesEffective no contêiner de esquema (o ponteiro IADs para o contêiner de esquema é passado como um parâmetro) para as classes attributeSchema e classSchema.
ms.assetid: 3abc2351-a3cf-4a6c-9a13-15dd51723883
ms.tgt_platform: multiple
keywords:
- Código de exemplo para verificar se há direitos para criar o AD de objetos de esquema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0200253fe10f91db1c1e67fbfc727d9165ecb8430aa4e2f648de9d3a1b8c73bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118694478"
---
# <a name="example-code-for-checking-for-rights-to-create-schema-objects"></a>Código de exemplo para verificar se há direitos para criar objetos de esquema

O exemplo de código C/C++ a seguir mostra uma função que verifica o atributo **allowedChildClassesEffective** no contêiner de esquema (o ponteiro IADs para o contêiner de esquema é passado como um parâmetro) para as classes **attributeSchema** e **classSchema.** Ele **retornará S \_ OK** se ambas as classes estão listadas **em allowedChildClassesEffective**. Se ambos não são, ele retorna **S \_ FALSE.**


```C++

// Function takes an IADs pointer to schema container as a parameter.
 
HRESULT HasSchemaAdditionRights(IADs *pSchema)
{
if (!pSchema)
  return E_POINTER;
HRESULT hr = E_FAIL;
VARIANT var;
VARIANT *pVar;
// Check access rights.
BOOL bIsAddAttributeAllowed = FALSE;
BOOL bIsAddClassAllowed = FALSE;
// Get AllowedChildClassesEffective. It is constructed;
// therefore, you must use GetInfoEx to explicitly 
// get it into the cache.
LPOLESTR pwszArray[] = {L"allowedChildClassesEffective"};
DWORD dwArrayItems = sizeof(pwszArray)/sizeof(LPOLESTR);
VARIANT vArray;
VariantInit(&vArray);
// Build a Variant of array type, using the specified string array.
hr = ADsBuildVarArrayStr(pwszArray, dwArrayItems, &vArray);
if (SUCCEEDED(hr))
{
  hr = pSchema->GetInfoEx(vArray,0L);
  if (SUCCEEDED(hr))
  {
    hr = pSchema->GetEx(CComBSTR("allowedChildClassesEffective"), 
                        &var);
    if (SUCCEEDED(hr))
    {
       hr = SafeArrayAccessData((SAFEARRAY*)(var.pparray), 
                                (void HUGEP* FAR*)&pVar);
       long lLBound, lUBound;
       // One-dimensional array. Get the bounds for the array.
       hr = SafeArrayGetLBound((SAFEARRAY*)(var.pparray), 
                               1,
                               &lLBound);
       hr = SafeArrayGetUBound((SAFEARRAY*)(var.pparray), 
                               1, 
                               &lUBound);
       // Get the count of elements
       long cElements = lUBound-lLBound + 1;
       // Get the elements of the array.
       if (SUCCEEDED(hr))
       {
        for (int i = 0; i < cElements; i++ ) 
        {
          // Check each element to verify that attributeSchema 
          // or classSchema is there.
          if (VT_BSTR == pVar[i].vt)
          {
            if (0==_wcsicmp(L"attributeSchema", pVar[i].bstrVal))
              bIsAddAttributeAllowed = TRUE;
            else if (0==_wcsicmp(L"classSchema", pVar[i].bstrVal))
              bIsAddClassAllowed = TRUE;
          }
        }
        if (bIsAddAttributeAllowed && bIsAddClassAllowed)
          hr = S_OK;
        else
          hr = S_FALSE;
       }
    }
    VariantClear(&var);
  }
}
 
return hr;
 
};
```



 

 




