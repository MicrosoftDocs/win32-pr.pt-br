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
# <a name="create-new-accessible-objects"></a><span data-ttu-id="35c30-103">Criar novos objetos acessíveis</span><span class="sxs-lookup"><span data-stu-id="35c30-103">Create New Accessible Objects</span></span>

<span data-ttu-id="35c30-104">Nesse cenário, o servidor cria um novo objeto acessível em resposta a cada solicitação [**de \_ cliente do OBJID**](object-identifiers.md) .</span><span class="sxs-lookup"><span data-stu-id="35c30-104">In this scenario, the server creates a new accessible object in response to each [**OBJID\_CLIENT**](object-identifiers.md) request.</span></span>

<span data-ttu-id="35c30-105">No código de exemplo a seguir, um ponteiro para o controle é recuperado dos dados da janela extra.</span><span class="sxs-lookup"><span data-stu-id="35c30-105">In the following example code, a pointer to the control is retrieved from the extra window data.</span></span> <span data-ttu-id="35c30-106">Isso e o identificador de janela são passados para o construtor do objeto de servidor de acessibilidade personalizado (AccServer).</span><span class="sxs-lookup"><span data-stu-id="35c30-106">This and the window handle are passed to the constructor of the custom accessibility server (AccServer) object.</span></span> <span data-ttu-id="35c30-107">Esse objeto é criado sempre que o [**\_ cliente OBJID**](object-identifiers.md) é recebido.</span><span class="sxs-lookup"><span data-stu-id="35c30-107">This object is created whenever [**OBJID\_CLIENT**](object-identifiers.md) is received.</span></span>

<span data-ttu-id="35c30-108">Quando o objeto é criado, o servidor Obtém uma referência, que deve ser liberada após chamar [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject), para que o objeto seja destruído assim que o cliente for concluído com ele.</span><span class="sxs-lookup"><span data-stu-id="35c30-108">When the object is created, the server obtains a reference, which must be released after calling [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject), so that the object is destroyed as soon as the client is finished with it.</span></span> <span data-ttu-id="35c30-109">Observe que o **LresultFromObject** incrementa a contagem de referência várias vezes, mas é responsabilidade dos aplicativos cliente e do tempo de execução do Microsoft acessibilidade ativa, para liberar essas referências.</span><span class="sxs-lookup"><span data-stu-id="35c30-109">Note that **LresultFromObject** increments the reference count several times, but it is the responsibility of client applications, and the Microsoft Active Accessibility runtime, to release these references.</span></span>


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



 

 




