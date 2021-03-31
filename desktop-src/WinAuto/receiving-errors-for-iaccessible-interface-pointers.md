---
title: Recebendo erros para ponteiros de interface IAccessible
description: Este tópico descreve as situações em que você pode receber um erro para um ponteiro de interface do IAccessible.
ms.assetid: 408bfa47-fda0-4a25-89c1-da41d967ad61
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e54d3bd9e39dae9c5de9ad1644e5955bd5fb90d2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822833"
---
# <a name="receiving-errors-for-iaccessible-interface-pointers"></a><span data-ttu-id="e7fd5-103">Recebendo erros para ponteiros de interface IAccessible</span><span class="sxs-lookup"><span data-stu-id="e7fd5-103">Receiving Errors for IAccessible Interface Pointers</span></span>

<span data-ttu-id="e7fd5-104">Este tópico descreve as situações em que você pode receber um erro para um ponteiro de interface do [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .</span><span class="sxs-lookup"><span data-stu-id="e7fd5-104">This topic describes situations in which you might receive an error for an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer.</span></span> <span data-ttu-id="e7fd5-105">As funções **IAccessible** podem retornar erros para ponteiros de interface **IAccessible** quando um usuário fecha um aplicativo ao qual o objeto pertence, ou se um usuário ignora um controle por meio da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="e7fd5-105">**IAccessible** functions can return errors for **IAccessible** interface pointers when a user closes an application that the object belongs to, or if a user dismisses a control through the user interface.</span></span>

## <a name="user-closes-an-application"></a><span data-ttu-id="e7fd5-106">O usuário fecha um aplicativo</span><span class="sxs-lookup"><span data-stu-id="e7fd5-106">User Closes an Application</span></span>

<span data-ttu-id="e7fd5-107">Se um usuário fechar o aplicativo que contém um objeto ao qual o ponteiro da interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) estava apontando, todas as chamadas futuras para esse objeto retornarão um código de erro.</span><span class="sxs-lookup"><span data-stu-id="e7fd5-107">If a user closes the application that contains an object to which the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer was pointing, then all future calls to that object will return an error code.</span></span> <span data-ttu-id="e7fd5-108">O erro, como **co \_ E \_ OBJNOTCONNECTED**, indicará que o objeto não existe mais.</span><span class="sxs-lookup"><span data-stu-id="e7fd5-108">The error, such as **CO\_E\_OBJNOTCONNECTED**, will indicate that the object does not exist anymore.</span></span> <span data-ttu-id="e7fd5-109">Isso se aplica a todos os ponteiros de interface do **IAccessible** .</span><span class="sxs-lookup"><span data-stu-id="e7fd5-109">This applies to all **IAccessible** interface pointers.</span></span>

## <a name="user-dismisses-a-control"></a><span data-ttu-id="e7fd5-110">O usuário ignora um controle</span><span class="sxs-lookup"><span data-stu-id="e7fd5-110">User Dismisses a Control</span></span>

<span data-ttu-id="e7fd5-111">Se um usuário ignorar um controle (por exemplo, pressionando um botão de ação), os clientes ainda poderão chamar métodos e propriedades de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) nesse objeto, pois o objeto não foi liberado.</span><span class="sxs-lookup"><span data-stu-id="e7fd5-111">If a user dismisses a control (for example, by pressing a push button), clients can still call [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods and properties on this object because the object has not been released.</span></span> <span data-ttu-id="e7fd5-112">No entanto, chamadas futuras receberão mensagens de erro.</span><span class="sxs-lookup"><span data-stu-id="e7fd5-112">However, future calls will receive error messages.</span></span>

<span data-ttu-id="e7fd5-113">Essa situação se aplica às seguintes funções e métodos:</span><span class="sxs-lookup"><span data-stu-id="e7fd5-113">This situation applies to the following functions and methods:</span></span>

-   [<span data-ttu-id="e7fd5-114">**AccessibleObjectFromEvent**</span><span class="sxs-lookup"><span data-stu-id="e7fd5-114">**AccessibleObjectFromEvent**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent)
-   [<span data-ttu-id="e7fd5-115">**AccessibleObjectFromPoint**</span><span class="sxs-lookup"><span data-stu-id="e7fd5-115">**AccessibleObjectFromPoint**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)
-   [<span data-ttu-id="e7fd5-116">**AccessibleObjectFromWindow**</span><span class="sxs-lookup"><span data-stu-id="e7fd5-116">**AccessibleObjectFromWindow**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow)
-   [<span data-ttu-id="e7fd5-117">**IAccessible:: accHitTest**</span><span class="sxs-lookup"><span data-stu-id="e7fd5-117">**IAccessible::accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="e7fd5-118">**IAccessible:: accNavigate**</span><span class="sxs-lookup"><span data-stu-id="e7fd5-118">**IAccessible::accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [<span data-ttu-id="e7fd5-119">**IAccessible:: obter \_ accFocus**</span><span class="sxs-lookup"><span data-stu-id="e7fd5-119">**IAccessible::get\_accFocus**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)
-   [<span data-ttu-id="e7fd5-120">**IAccessible:: obter \_ accSelection**</span><span class="sxs-lookup"><span data-stu-id="e7fd5-120">**IAccessible::get\_accSelection**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accselection)

 

 




