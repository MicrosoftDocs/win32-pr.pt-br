---
title: Excluindo um objeto
description: Excluindo um objeto
ms.assetid: 54ea1e7d-75b5-461f-b0d6-a976c33d66fe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31f77ad42700e01e5594faa5b8bb299fcc5841d7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104453636"
---
# <a name="deleting-an-object"></a><span data-ttu-id="d2939-103">Excluindo um objeto</span><span class="sxs-lookup"><span data-stu-id="d2939-103">Deleting an Object</span></span>

<span data-ttu-id="d2939-104">O método **Release** exclui o objeto quando sua contagem de referência é zero.</span><span class="sxs-lookup"><span data-stu-id="d2939-104">The **Release** method deletes the object when its reference count is zero.</span></span>


```C++
STDMETHODIMP_(ULONG) CAVIFileCF::Release() 
{ 
    if (!--m_refs) 
    { 
        delete this;   // If O, delete this instance. 
        return 0; 
    } 
    return m_refs; 
} 

```



 

 




