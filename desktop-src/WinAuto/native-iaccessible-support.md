---
title: Suporte a IAccessible nativo
description: Oleacc.dll implementa IAccIdentity em nome do \_ cliente OBJID \ 160; ponteiros de interface IAccessible e seus filhos de elemento simples imediatos.
ms.assetid: 98c6d68b-b64d-44d4-93c3-6c7c6732d59d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 606261a642f57c85f3f23a80257b7cdc498b927b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822774"
---
# <a name="native-iaccessible-support"></a><span data-ttu-id="7fcb1-103">Suporte a IAccessible nativo</span><span class="sxs-lookup"><span data-stu-id="7fcb1-103">Native IAccessible Support</span></span>

<span data-ttu-id="7fcb1-104">Oleacc.dll implementa [**IAccIdentity**](/windows/desktop/api/oleacc/nn-oleacc-iaccidentity) em nome dos ponteiros da interface [**\_ Client**](object-identifiers.md) [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) do OBJID e seus filhos de elemento simples imediatos.</span><span class="sxs-lookup"><span data-stu-id="7fcb1-104">Oleacc.dll implements [**IAccIdentity**](/windows/desktop/api/oleacc/nn-oleacc-iaccidentity) on behalf of [**OBJID\_CLIENT**](object-identifiers.md) [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointers and their immediate simple element children.</span></span> <span data-ttu-id="7fcb1-105">Um ponteiro de interface **\_ Client** **IAccessible** de OBJID é retornado quando o [**WM \_ GetObject**](wm-getobject.md) com   =  o **\_ cliente lParam OBJID** é enviado para um **HWND**, que representa a área do cliente da janela ou o controle como um todo.</span><span class="sxs-lookup"><span data-stu-id="7fcb1-105">An **OBJID\_CLIENT** **IAccessible** interface pointer is returned when [**WM\_GETOBJECT**](wm-getobject.md) with *lParam* = **OBJID\_CLIENT** is sent to an **HWND**, which represents the client area of the window or the control as a whole.</span></span> <span data-ttu-id="7fcb1-106">O pai de tal ponteiro de interface **IAccessible** normalmente terá uma função de [**janela do \_ sistema \_ de função**](object-roles.md) e é o objeto **IAccessible** retornado quando o **WM \_ GetObject** com a   =  [**\_ janela lParam OBJID**](object-identifiers.md) é enviado para um HWND.</span><span class="sxs-lookup"><span data-stu-id="7fcb1-106">The parent of such an **IAccessible** interface pointer will typically have a role of [**ROLE\_SYSTEM\_WINDOW**](object-roles.md) and is the **IAccessible** object returned when **WM\_GETOBJECT** with *lParam* = [**OBJID\_WINDOW**](object-identifiers.md) is sent to an hwnd.</span></span>

<span data-ttu-id="7fcb1-107">Esses ponteiros de interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) normalmente ocorrem onde um proxy de Oleacc.dll é subclasse, ou onde um simples controle personalizado (como um **IAccessible** de contêiner mais um nível de filhos de elemento simples) fornece uma implementação de **IAccessible** nativo.</span><span class="sxs-lookup"><span data-stu-id="7fcb1-107">These [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointers typically occur where an Oleacc.dll proxy is subclassed, or where a simple custom control (such as a container **IAccessible** plus one level of simple element children) provides a native **IAccessible** implementation.</span></span>

<span data-ttu-id="7fcb1-108">Implementações mais complicadas do [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) nativo, como o local em que uma hierarquia de **IAccessible** s existe ou onde as IDs de objeto personalizado são usadas devem implementar as próprias [**IAccIdentity**](/windows/desktop/api/oleacc/nn-oleacc-iaccidentity) .</span><span class="sxs-lookup"><span data-stu-id="7fcb1-108">More complicated native [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) implementations such as where a hierarchy of **IAccessible** s exists or where custom object IDs are used must implement [**IAccIdentity**](/windows/desktop/api/oleacc/nn-oleacc-iaccidentity) themselves.</span></span>

 

 




