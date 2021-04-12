---
title: Depurando alocações de memória
description: Depurando alocações de memória
ms.assetid: 522adb1f-0e3e-4dfb-8836-f539a79a3d9e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: beb6a7dbe313cfe571fa6b4d244df35407fa331e
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104294523"
---
# <a name="debugging-memory-allocations"></a><span data-ttu-id="26214-103">Depurando alocações de memória</span><span class="sxs-lookup"><span data-stu-id="26214-103">Debugging Memory Allocations</span></span>

<span data-ttu-id="26214-104">O COM fornece a interface [**IMallocSpy**](/windows/desktop/api/ObjIdl/nn-objidl-imallocspy) para que os desenvolvedores usem para depurar suas alocações de memória.</span><span class="sxs-lookup"><span data-stu-id="26214-104">COM provides the [**IMallocSpy**](/windows/desktop/api/ObjIdl/nn-objidl-imallocspy) interface for developers to use to debug their memory allocations.</span></span> <span data-ttu-id="26214-105">Para cada método em [**IMalloc**](/windows/win32/api/objidlbase/nn-objidlbase-imalloc), há dois métodos no **IMallocSpy**, um método "pre" e um método "post".</span><span class="sxs-lookup"><span data-stu-id="26214-105">For each method in [**IMalloc**](/windows/win32/api/objidlbase/nn-objidlbase-imalloc), there are two methods in **IMallocSpy**, a "pre" method and a "post" method.</span></span> <span data-ttu-id="26214-106">Depois que um desenvolvedor o implementa e o publica no sistema, o sistema chama o método "pre" do **IMallocSpy** logo antes do método **IMalloc** correspondente, permitindo efetivamente o código de depuração para "Spy" na operação de alocação e chama o método "post" para liberar o Spy.</span><span class="sxs-lookup"><span data-stu-id="26214-106">After a developer implements it and publishes it to the system, the system calls the **IMallocSpy** "pre" method just before the corresponding **IMalloc** method, effectively allowing the debug code to "spy" on the allocation operation, and calls the "post" method to release the spy.</span></span>

<span data-ttu-id="26214-107">Por exemplo, quando o COM detecta que a próxima chamada é uma chamada para [**IMalloc:: Alloc**](/windows/desktop/api/ObjIdl/nf-objidl-imalloc-alloc), ele [**chama IMallocSpy::P realloc**](/windows/desktop/api/ObjIdl/nf-objidl-imallocspy-prealloc), executando quaisquer operações de depuração que o desenvolvedor deseja durante a execução da **alocação** e, em seguida, quando a chamada de **alocação** retorna, chama [**IMallocSpy::P ostalloc**](/windows/desktop/api/ObjIdl/nf-objidl-imallocspy-postalloc) para liberar o Spy e retornar o controle para o código.</span><span class="sxs-lookup"><span data-stu-id="26214-107">For example, when COM detects that the next call is a call to [**IMalloc::Alloc**](/windows/desktop/api/ObjIdl/nf-objidl-imalloc-alloc), it calls [**IMallocSpy::PreAlloc**](/windows/desktop/api/ObjIdl/nf-objidl-imallocspy-prealloc), executing whatever debug operations the developer wants during the **Alloc** execution, and then, when the **Alloc** call returns, calls [**IMallocSpy::PostAlloc**](/windows/desktop/api/ObjIdl/nf-objidl-imallocspy-postalloc) to release the spy and return control to the code.</span></span>

## <a name="related-topics"></a><span data-ttu-id="26214-108">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="26214-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="26214-109">Gerenciando a alocação de memória</span><span class="sxs-lookup"><span data-stu-id="26214-109">Managing Memory Allocation</span></span>](managing-memory-allocation.md)
</dt> </dl>

 

 