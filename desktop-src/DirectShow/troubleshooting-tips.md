---
description: Dicas de solução de problemas
ms.assetid: e87ad3bd-07ae-4b9d-b465-2ce4688bdd83
title: Dicas de solução de problemas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c0280702c7ce2131d1252ec75b8bee4be231e29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105770427"
---
# <a name="troubleshooting-tips"></a><span data-ttu-id="34234-103">Dicas de solução de problemas</span><span class="sxs-lookup"><span data-stu-id="34234-103">Troubleshooting Tips</span></span>

<span data-ttu-id="34234-104">Estas dicas a seguir ajudarão você a evitar deadlocks ou falhas em seu aplicativo do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="34234-104">This following tips will help you to avoid deadlocks or crashes in your DirectShow application.</span></span>

<span data-ttu-id="34234-105">**Objetos globais**</span><span class="sxs-lookup"><span data-stu-id="34234-105">**Global Objects**</span></span>

<span data-ttu-id="34234-106">Um objeto C++ global não deve criar objetos DirectShow em seu método construtor ou liberá-los em seu método destruidor.</span><span class="sxs-lookup"><span data-stu-id="34234-106">A global C++ object should not create DirectShow objects in its constructor method or release them in its destructor method.</span></span> <span data-ttu-id="34234-107">Isso pode fazer com que o aplicativo seja bloqueado indefinidamente, pelo seguinte motivo:</span><span class="sxs-lookup"><span data-stu-id="34234-107">Doing so can cause the application to block indefinitely, for the following reason:</span></span>

<span data-ttu-id="34234-108">Não é possível sair de threads enquanto estiver dentro da função de ponto de entrada de uma DLL.</span><span class="sxs-lookup"><span data-stu-id="34234-108">Threads cannot exit while inside a DLL's entry-point function.</span></span> <span data-ttu-id="34234-109">O kernel 32 mantém um bloqueio de processo global durante a função de ponto de entrada e o bloqueio impede que o thread seja encerrado.</span><span class="sxs-lookup"><span data-stu-id="34234-109">Kernel 32 holds a global process lock during the entry-point function, and the lock prevents the thread from exiting.</span></span> <span data-ttu-id="34234-110">Como alguns objetos do DirectShow possuem threads, eles podem ser bloqueados se forem liberados de dentro de uma função de ponto de entrada de DLL.</span><span class="sxs-lookup"><span data-stu-id="34234-110">Because some DirectShow objects own threads, they can block if released from inside a DLL entry-point function.</span></span> <span data-ttu-id="34234-111">Se um aplicativo tiver um objeto C++ global, a DLL de tempo de execução C chamará o destruidor do objeto quando a DLL for descarregada.</span><span class="sxs-lookup"><span data-stu-id="34234-111">If an application has a global C++ object, the C runtime DLL calls the object's destructor when the DLL is unloaded.</span></span> <span data-ttu-id="34234-112">Se o destruidor liberar objetos do DirectShow, ele poderá bloquear como resultado.</span><span class="sxs-lookup"><span data-stu-id="34234-112">If the destructor releases DirectShow objects, it can block as a result.</span></span>

<span data-ttu-id="34234-113">Por motivos semelhantes, uma DLL não deve criar ou liberar objetos do DirectShow em sua rotina de ponto de entrada.</span><span class="sxs-lookup"><span data-stu-id="34234-113">For similar reasons, a DLL should not create or release DirectShow objects in its entry point routine.</span></span>

<span data-ttu-id="34234-114">**Liberando interfaces**</span><span class="sxs-lookup"><span data-stu-id="34234-114">**Releasing Interfaces**</span></span>

<span data-ttu-id="34234-115">Você deve liberar todos os ponteiros de interface do DirectShow enquanto seu aplicativo ainda estiver processando mensagens, antes de sair do loop de mensagem.</span><span class="sxs-lookup"><span data-stu-id="34234-115">You should release all DirectShow interface pointers while your application is still processing messages, before it exits the message loop.</span></span> <span data-ttu-id="34234-116">Caso contrário, você poderá ver várias declarações, pois alguns objetos do DirectShow enviam mensagens durante suas rotinas de limpeza.</span><span class="sxs-lookup"><span data-stu-id="34234-116">Otherwise, you might see various asserts, because some DirectShow objects send messages during their clean-up routines.</span></span>

<span data-ttu-id="34234-117">(Como um registro, se você estiver usando a classe **CWindowImpl** do ATL, não espere até que **OnFinalMessage** libere as interfaces.</span><span class="sxs-lookup"><span data-stu-id="34234-117">(As a corollary, if you are using the ATL **CWindowImpl** class, do not wait until **OnFinalMessage** to free the interfaces.</span></span> <span data-ttu-id="34234-118">Em vez disso, libere-os quando você manipular a mensagem de fechamento do WM \_ .)</span><span class="sxs-lookup"><span data-stu-id="34234-118">Instead, free them when you handle the WM\_CLOSE message.)</span></span>

<span data-ttu-id="34234-119">**Contagens de referência**</span><span class="sxs-lookup"><span data-stu-id="34234-119">**Reference Counts**</span></span>

<span data-ttu-id="34234-120">Quando a versão de depuração do Quartz.dll descarrega, ela verifica se algum objeto do DirectShow tem contagens de referência que não foram lançadas.</span><span class="sxs-lookup"><span data-stu-id="34234-120">When the debug version of Quartz.dll unloads, it checks whether any DirectShow objects have reference counts that were not released.</span></span> <span data-ttu-id="34234-121">Nesse caso, ele gera uma asserção:</span><span class="sxs-lookup"><span data-stu-id="34234-121">If so, it throws an assertion:</span></span>


```C++
g_cFGObjects == 0 
```



<span data-ttu-id="34234-122">Quando essa asserção falha, significa que seu aplicativo perdeu uma contagem de referência.</span><span class="sxs-lookup"><span data-stu-id="34234-122">When this assertion fails, it means your application has leaked a reference count.</span></span> <span data-ttu-id="34234-123">Examine seu código e certifique-se de liberar todos os ponteiros de interface.</span><span class="sxs-lookup"><span data-stu-id="34234-123">Review your code and make sure that you release all interface pointers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="34234-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="34234-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="34234-125">Depuração no DirectShow</span><span class="sxs-lookup"><span data-stu-id="34234-125">Debugging in DirectShow</span></span>](debugging-in-directshow.md)
</dt> </dl>

 

 



