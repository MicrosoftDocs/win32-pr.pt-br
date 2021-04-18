---
title: Reutilizar ponteiros existentes para objetos
description: Reutilizar ponteiros existentes para objetos
ms.assetid: 7e1610c6-89b2-4e7e-aee5-94a6cab87a22
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c151b8d957fb82718721ad81b452a81a2c71ec84
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105760555"
---
# <a name="reuse-existing-pointers-to-objects"></a>Reutilizar ponteiros existentes para objetos

Nesse cenário, o servidor responde a uma solicitação [**de \_ cliente OBJID**](object-identifiers.md) usando o mesmo ponteiro de interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) a cada vez.

No código de exemplo a seguir, o objeto de controle é recuperado dos dados da janela extra e um método do controle é chamado para recuperar o objeto de servidor de acessibilidade (a classe AccServer definida pelo aplicativo), se houver. Se o servidor de acessibilidade ainda não existir, ele será criado.

Quando o objeto de servidor de acessibilidade é criado, ele tem uma contagem de referência de 1. [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) incrementa a contagem de referência várias vezes, mas essas referências serão liberadas quando o cliente for concluído com o objeto. O servidor libera sua referência quando a janela de controle é destruída.


```C++
case WM_GETOBJECT:
    {
        // Return the IAccessible object. 
        if ((DWORD)lParam == (DWORD)OBJID_CLIENT)
        {
            // Get the control.  
            CustomListControl* pCustomList = (CustomListControl*)(LONG_PTR)GetWindowLongPtr(hwnd, 0);
            // Create the accessible object. 
            AccServer* pAccServer = pCustomList->GetAccServer();
            if (pAccServer == NULL)
            {
                pAccServer = new AccServer(hwnd, pCustomList);
                pCustomList->SetAccServer(pAccServer);
            }
            if (pAccServer != NULL)  // NULL if out of memory. 
            {
                LRESULT Lresult = LresultFromObject(IID_IAccessible, wParam, pAccServer);
                return Lresult;
            }
            else return 0;
        }
        break;
    }

    
case WM_DESTROY:
    {
    CustomListControl* pCustomList = (CustomListControl*)(LONG_PTR)GetWindowLongPtr(hwnd, 0);
    AccServer* pAccServer = pCustomList->GetAccServer();
    if (pAccServer!= NULL)
    {
        // Notify the accessibility object that the control no longer exists. 
        pAccServer->SetControlIsAlive(false);
        // Release the reference created in WM_GETOBJECT. 
        pAccServer->Release(); 
    }   
    // Destroy the control. 
    delete pCustomList;
     break;
    }
```



 

 




