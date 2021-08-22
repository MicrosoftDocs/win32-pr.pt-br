---
title: Determinando a qual interface um objeto dá suporte
description: Determinando a qual interface um objeto dá suporte
ms.assetid: cf2aacb7-5315-4907-a49b-3eb3bbfd13d1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e5afffd2818c7a8f204363180e52fe9f94f16157aacd027582ce377b2f5211c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119497247"
---
# <a name="determining-which-interface-an-object-supports"></a>Determinando a qual interface um objeto dá suporte

O **método QueryInterface** permite que um aplicativo consulte um objeto para determinar quais interfaces ele dá suporte. O aplicativo de exemplo define o *ponteiro ppv* para a interface atual.


```C++
STDMETHODIMP CAVIFileCF::QueryInterface( 
    const IID FAR& iid, 
    void FAR* FAR* ppv) 
{ 
    if (iid == IID_IUnknown) 
        *ppv = this;                     // set the interface pointer 
                                         // to this instance 
    else if (iid == IID_IClassFactory) 
        *ppv = this;                     // second chance to set the 
                                         // interface pointer to this 
                                         // instance 
    else 
        return ResultFromScode(E_NOINTERFACE); 
    AddRef();  //Increment the reference count 
    return NULL; 
} 

```



 

 




