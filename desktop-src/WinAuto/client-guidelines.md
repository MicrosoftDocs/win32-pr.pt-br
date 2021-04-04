---
title: Diretrizes do cliente
description: Os desenvolvedores de cliente devem usar a seguinte funcionalidade para obter informações sobre os elementos da interface do usuário
ms.assetid: 0e102e60-4d11-490e-88d5-dfadba620781
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9ced411c24ed0b7aa3ab97cbe1ce2511d4e6b05
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "103916939"
---
# <a name="client-guidelines"></a><span data-ttu-id="8b128-103">Diretrizes do cliente</span><span class="sxs-lookup"><span data-stu-id="8b128-103">Client Guidelines</span></span>

<span data-ttu-id="8b128-104">Os desenvolvedores de cliente devem usar a seguinte funcionalidade para obter informações sobre os elementos da interface do usuário:</span><span class="sxs-lookup"><span data-stu-id="8b128-104">Client developers should use the following functionality to get information about the user interface elements:</span></span>

-   <span data-ttu-id="8b128-105">Para obter uma interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para objetos, chame [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow), [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)ou [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent).</span><span class="sxs-lookup"><span data-stu-id="8b128-105">To get an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface to objects, call [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow), [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint), or [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent).</span></span>
-   <span data-ttu-id="8b128-106">Para examinar e manipular objetos acessíveis, use as propriedades e os métodos do [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .</span><span class="sxs-lookup"><span data-stu-id="8b128-106">To examine and manipulate accessible objects, use the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties and methods.</span></span>
-   <span data-ttu-id="8b128-107">Para receber [WinEvents](winevents-overview.md), chame [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook) para registrar uma função de retorno de chamada WinEvent para os eventos que são relevantes para o aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="8b128-107">To receive [WinEvents](winevents-overview.md), call [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook) to register a WinEvent callback function for those events that are relevant to the client application.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="8b128-108">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="8b128-108">In this section</span></span>

-   [<span data-ttu-id="8b128-109">Como os clientes obtêm IDs filho</span><span class="sxs-lookup"><span data-stu-id="8b128-109">How Clients Obtain Child IDs</span></span>](how-clients-obtain-child-ids.md)

 

 




