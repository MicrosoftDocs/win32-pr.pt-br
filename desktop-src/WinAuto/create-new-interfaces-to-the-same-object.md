---
title: Criar novas interfaces para o mesmo objeto
description: Criar novas interfaces para o mesmo objeto
ms.assetid: 127c44b6-51a6-4fd6-9edc-9fbe0d08d458
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7aae1d6328b6d803e4d20207381fe596c5f584fee8281e1e6651ffc2325fb044
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119998706"
---
# <a name="create-new-interfaces-to-the-same-object"></a>Criar novas interfaces para o mesmo objeto

Nesse cenário, o servidor responde a cada [**solicitação OBJID \_ CLIENT**](object-identifiers.md) obtendo um novo ponteiro de interface para o mesmo objeto.

No código de exemplo a seguir, *m \_ pUIObj* é um ponteiro para um objeto que dá suporte a mais de Component Object Model (COM). Embora um objeto existente seja reutilizado, um novo ponteiro de interface é criado sempre que o objeto é recuperado, portanto, a contagem de referência deve ser decrementada.


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



 

 




