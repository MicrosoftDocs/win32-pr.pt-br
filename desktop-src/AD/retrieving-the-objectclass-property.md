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
# <a name="retrieving-the-objectclass-attribute"></a><span data-ttu-id="b4292-103">Recuperando o atributo objectClass</span><span class="sxs-lookup"><span data-stu-id="b4292-103">Retrieving the objectClass Attribute</span></span>

<span data-ttu-id="b4292-104">O atributo **objectClass** contém a classe da qual o objeto é uma instância, bem como todas as classes das quais essa classe é derivada.</span><span class="sxs-lookup"><span data-stu-id="b4292-104">The **objectClass** attribute contains the class of which the object is an instance, as well as all classes from which that class is derived.</span></span> <span data-ttu-id="b4292-105">Por exemplo, a classe **User** herda de **Top**, **Person** e **OrganizationalPerson**; Portanto, o atributo **objectClass** contém os nomes dessas classes, bem como o usuário.</span><span class="sxs-lookup"><span data-stu-id="b4292-105">For example, the **user** class inherits from **top**, **person**, and **organizationalPerson**; therefore, the **objectClass** attribute contains the names of those classes, as well as user.</span></span> <span data-ttu-id="b4292-106">Então, como descobrir de qual classe o objeto é uma instância?</span><span class="sxs-lookup"><span data-stu-id="b4292-106">So, how do you find out what class the object is an instance of?</span></span> <span data-ttu-id="b4292-107">O atributo **objectClass** é o único atributo com vários valores que tem valores ordenados.</span><span class="sxs-lookup"><span data-stu-id="b4292-107">The **objectClass** attribute is the only attribute with multiple values that has ordered values.</span></span> <span data-ttu-id="b4292-108">O primeiro valor é o topo da hierarquia de classe, que é a classe Top, e o último valor é a classe mais derivada, que é a classe da qual o objeto é uma instância do.</span><span class="sxs-lookup"><span data-stu-id="b4292-108">The first value is the top of the class hierarchy, which is the top class, and the last value is the most derived class, which is the class that the object is an instance of.</span></span>

<span data-ttu-id="b4292-109">A função a seguir usa um ponteiro para uma coluna que contém um atributo **objectClass** e retorna a **objectClass** instanciada do objeto.</span><span class="sxs-lookup"><span data-stu-id="b4292-109">The following function takes a pointer to a column containing an **objectClass** attribute and returns the instantiated **objectClass** of the object.</span></span>


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



 

 




