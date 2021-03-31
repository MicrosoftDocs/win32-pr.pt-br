---
title: Criar novos objetos acessíveis
description: Criar novos objetos acessíveis
ms.assetid: d34a52d1-1eb2-4bb4-989c-a1ca4b5d815f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5efa85e44d6d51105e6363d276ecb7e5f33d8378
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636099"
---
# <a name="create-new-accessible-objects"></a>Criar novos objetos acessíveis

Nesse cenário, o servidor cria um novo objeto acessível em resposta a cada solicitação [**de \_ cliente do OBJID**](object-identifiers.md) .

No código de exemplo a seguir, um ponteiro para o controle é recuperado dos dados da janela extra. Isso e o identificador de janela são passados para o construtor do objeto de servidor de acessibilidade personalizado (AccServer). Esse objeto é criado sempre que o [**\_ cliente OBJID**](object-identifiers.md) é recebido.

Quando o objeto é criado, o servidor Obtém uma referência, que deve ser liberada após chamar [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject), para que o objeto seja destruído assim que o cliente for concluído com ele. Observe que o **LresultFromObject** incrementa a contagem de referência várias vezes, mas é responsabilidade dos aplicativos cliente e do tempo de execução do Microsoft acessibilidade ativa, para liberar essas referências.


```C++
case WM_GETOBJECT:
{
    // Return the IAccessible object. 
    if ((DWORD)lParam == OBJID_CLIENT)
    {
        // Get the control.  
        CustomListControl* pCustomList = (CustomListControl*)(LONG_PTR)GetWindowLongPtr(hwnd, 0);
        AccServer* pAccServer = new AccServer(hwnd, pCustomList);
        if (pAccServer != NULL)  // NULL if out of memory. 
        {
            LRESULT Lresult = LresultFromObject(IID_IAccessible, wParam, pAccServer);
            pAccServer->Release();
            return Lresult;
        }
        else return 0;
    }
    break;
}
```



 

 




