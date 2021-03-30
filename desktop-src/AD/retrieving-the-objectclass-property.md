---
title: Recuperando o atributo objectClass
description: O atributo objectClass contém a classe da qual o objeto é uma instância, bem como todas as classes das quais essa classe é derivada.
ms.assetid: 6066d9c3-f97b-482a-88c7-0fde1dc2f4c4
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f237efff1e13c7f3498a51f38588c9885fbab76
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103634923"
---
# <a name="retrieving-the-objectclass-attribute"></a>Recuperando o atributo objectClass

O atributo **objectClass** contém a classe da qual o objeto é uma instância, bem como todas as classes das quais essa classe é derivada. Por exemplo, a classe **User** herda de **Top**, **Person** e **OrganizationalPerson**; Portanto, o atributo **objectClass** contém os nomes dessas classes, bem como o usuário. Então, como descobrir de qual classe o objeto é uma instância? O atributo **objectClass** é o único atributo com vários valores que tem valores ordenados. O primeiro valor é o topo da hierarquia de classe, que é a classe Top, e o último valor é a classe mais derivada, que é a classe da qual o objeto é uma instância do.

A função a seguir usa um ponteiro para uma coluna que contém um atributo **objectClass** e retorna a **objectClass** instanciada do objeto.


```C++
HRESULT GetClass(ADS_SEARCH_COLUMN *pcol, LPOLESTR *ppClass)
{
  if (!pcol)
    return E_POINTER;
 
  HRESULT hr = E_FAIL;
  if (ppClass)
  {
    LPOLESTR szClass = new OLECHAR[MAX_PATH];
    wcscpy_s(szClass, L"");
    if ( _wcsicmp(pcol->pszAttrName,L"objectClass") == 0 )
    {
      for (DWORD x = 0; x< pcol->dwNumValues; x++)
      {
        wcscpy_s(szClass, pcol->pADsValues[x].CaseIgnoreString);
      }
    }
    if (0==wcscmp(L"", szClass))
    {
      hr = E_FAIL;
    }
    else
    {
      //Allocate memory for string.
      //Caller must free using CoTaskMemFree.
      *ppClass = (OLECHAR *)CoTaskMemAlloc (
                             sizeof(OLECHAR)*(wcslen(szClass)+1));
      if (*ppClass)
      {
        wcscpy_s(*ppClass, szClass);
        hr = S_OK;
      }
      else
      hr=E_FAIL;
    }
  }
  return hr;
}
```



 

 




