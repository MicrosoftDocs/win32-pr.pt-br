---
title: Criar novas interfaces para o mesmo objeto
description: Criar novas interfaces para o mesmo objeto
ms.assetid: 127c44b6-51a6-4fd6-9edc-9fbe0d08d458
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b641eed3918af3acbf399427ad5f7427112f399
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105755928"
---
# <a name="create-new-interfaces-to-the-same-object"></a>Criar novas interfaces para o mesmo objeto

Nesse cenário, o servidor responde a cada solicitação [**de \_ cliente OBJID**](object-identifiers.md) , obtendo um novo ponteiro de interface para o mesmo objeto.

No código de exemplo a seguir, *m \_ pUIObj* é um ponteiro para um objeto que dá suporte a mais de uma interface com (Component Object Model). Embora um objeto existente seja reutilizado, um novo ponteiro de interface é criado cada vez que o objeto é recuperado, portanto, a contagem de referência deve ser decrementada.


```C++
case WM_GETOBJECT:
   if ((DWORD)lParam == OBJID_CLIENT)
   {
      // Get a new interface to the same object. 
      IAccessible *pAcc = NULL;
      // The following increments the reference count. 
      m_pUIObj->QueryInterface(IID_IAccessible, (LPVOID*)&pAcc); 
      LRESULT lAcc = LresultFromObject(IID_IAccessible, wParam, 
            (LPUNKNOWN) &pAcc); 
      // Release our reference to the object.             
      pAcc->Release();               
      return lAcc;
   }
   break;  // Fall through to DefWindowProc. 
   
```



 

 




