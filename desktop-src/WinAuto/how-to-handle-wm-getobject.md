---
title: Como lidar com WM_GETOBJECT
description: Quando recebe uma \_ mensagem do WM GetObject que contém \_ o cliente OBJID, o servidor deve retornar um ponteiro para o objeto que implementa o IAccessible.
ms.assetid: 455398b7-f748-4ab0-8953-3f74439e44f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6223d75339f537ccf1939f9c9af46a42aa47bfdb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636307"
---
# <a name="how-to-handle-wm_getobject"></a><span data-ttu-id="81735-103">Como tratar o WM \_ GETobject</span><span class="sxs-lookup"><span data-stu-id="81735-103">How to Handle WM\_GETOBJECT</span></span>

<span data-ttu-id="81735-104">Quando recebe uma mensagem do [**WM \_ GetObject**](wm-getobject.md) que contém [**o \_ cliente OBJID**](object-identifiers.md), o servidor deve retornar um ponteiro para o objeto que implementa o [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible).</span><span class="sxs-lookup"><span data-stu-id="81735-104">When it receives a [**WM\_GETOBJECT**](wm-getobject.md) message that contains [**OBJID\_CLIENT**](object-identifiers.md), the server must return a pointer to the object that implements [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible).</span></span> <span data-ttu-id="81735-105">Esse ponteiro é um LRESULT que é obtido chamando [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject).</span><span class="sxs-lookup"><span data-stu-id="81735-105">This pointer is an LRESULT that is obtained by calling [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject).</span></span> <span data-ttu-id="81735-106">O Microsoft Acessibilidade Ativa, em conjunto com a biblioteca do Component Object Model (COM), executa o marshaling apropriado e passa o ponteiro da interface **IAccessible** do servidor para o cliente.</span><span class="sxs-lookup"><span data-stu-id="81735-106">Microsoft Active Accessibility, in conjunction with the Component Object Model (COM) library, performs the appropriate marshaling and passes the **IAccessible** interface pointer from the server to the client.</span></span>

<span data-ttu-id="81735-107">Os servidores devem lidar corretamente com a contagem de referência no objeto acessível.</span><span class="sxs-lookup"><span data-stu-id="81735-107">Servers must correctly handle reference counting on the accessible object.</span></span> <span data-ttu-id="81735-108">Lembre-se de que quando você cria um objeto COM, a contagem de referência é 1.</span><span class="sxs-lookup"><span data-stu-id="81735-108">Remember that when you create a COM object, the reference count is 1.</span></span> <span data-ttu-id="81735-109">Em seguida, o [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) incrementa a contagem de referência várias vezes.</span><span class="sxs-lookup"><span data-stu-id="81735-109">[**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) then further increments the reference count several times.</span></span> <span data-ttu-id="81735-110">Todas as referências criadas por **LresultFromObject** são liberadas automaticamente quando o objeto não é mais necessário, mas o servidor é responsável por liberar a referência inicial e, a menos que isso seja feito, o objeto nunca será destruído.</span><span class="sxs-lookup"><span data-stu-id="81735-110">All the references created by **LresultFromObject** are automatically released when the object is no longer needed, but the server is responsible for releasing the initial reference, and unless it does so, the object will never be destroyed.</span></span> <span data-ttu-id="81735-111">Os exemplos nas seções a seguir mostram como liberar referências a objetos acessíveis.</span><span class="sxs-lookup"><span data-stu-id="81735-111">The examples in the following sections show how to release references to accessible objects.</span></span>

<span data-ttu-id="81735-112">Os servidores normalmente tratam do [**WM \_ GetObject**](wm-getobject.md) em uma das seguintes maneiras:</span><span class="sxs-lookup"><span data-stu-id="81735-112">Servers typically handle [**WM\_GETOBJECT**](wm-getobject.md) in one of the following ways:</span></span>

-   [<span data-ttu-id="81735-113">Criar novos objetos acessíveis</span><span class="sxs-lookup"><span data-stu-id="81735-113">Create New Accessible Objects</span></span>](create-new-accessible-objects.md)
-   [<span data-ttu-id="81735-114">Reutilizar ponteiros existentes para objetos</span><span class="sxs-lookup"><span data-stu-id="81735-114">Reuse Existing Pointers to Objects</span></span>](reuse-existing-pointers-to-objects.md)
-   [<span data-ttu-id="81735-115">Criar novas interfaces para o mesmo objeto</span><span class="sxs-lookup"><span data-stu-id="81735-115">Create New Interfaces to the Same Object</span></span>](create-new-interfaces-to-the-same-object.md)

> [!Note]  
> <span data-ttu-id="81735-116">Nesta seção, como no restante da documentação, quando um ponteiro para uma interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) é discutido, esse ponteiro pode, na verdade, ser um ponteiro para um objeto proxy que encapsula a interface **IAccessible** .</span><span class="sxs-lookup"><span data-stu-id="81735-116">In this section as in the rest of the documentation, when a pointer to an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface is discussed, this pointer may actually be a pointer to a proxy object that wraps the **IAccessible** interface.</span></span> <span data-ttu-id="81735-117">Para obter mais informações sobre objetos proxy, consulte [Creating proxy Objects](creating-proxy-objects.md).</span><span class="sxs-lookup"><span data-stu-id="81735-117">For more information about proxy objects, see [Creating Proxy Objects](creating-proxy-objects.md).</span></span>

 

<span data-ttu-id="81735-118">Para obter uma visão geral do [**WM \_ GetObject**](wm-getobject.md), consulte [como o WM \_ GetObject funciona](how-wm-getobject-works.md).</span><span class="sxs-lookup"><span data-stu-id="81735-118">For an overview of [**WM\_GETOBJECT**](wm-getobject.md), see [How WM\_GETOBJECT Works](how-wm-getobject-works.md).</span></span>

 

 




