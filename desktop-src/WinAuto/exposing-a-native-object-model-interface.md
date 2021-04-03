---
title: Expondo uma interface de modelo de objeto nativo
description: Se um elemento de interface do usuário oferecer suporte a um modelo de objeto nativo diferente do Microsoft Acessibilidade Ativa ou da automação da interface do usuário, ele poderá expor a interface personalizada respondendo às \_ mensagens do WM GetObject que incluem o \_ identificador de objeto OBJID NATIVEOM.
ms.assetid: 430abeaf-e5ca-48c4-aa35-8d52a8cee2f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e52543908e89a1cea57c981d60bf7cb2b9fbd1fb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005748"
---
# <a name="exposing-a-native-object-model-interface"></a><span data-ttu-id="ce08d-103">Expondo uma interface de modelo de objeto nativo</span><span class="sxs-lookup"><span data-stu-id="ce08d-103">Exposing a Native Object Model Interface</span></span>

<span data-ttu-id="ce08d-104">Se um elemento de interface do usuário oferecer suporte a um modelo de objeto nativo diferente do Microsoft Acessibilidade Ativa ou da automação da interface do usuário, ele poderá expor a interface personalizada respondendo às mensagens do [**WM \_ GetObject**](wm-getobject.md) que incluem o identificador de objeto [**OBJID \_ NATIVEOM**](object-identifiers.md) .</span><span class="sxs-lookup"><span data-stu-id="ce08d-104">If a UI element supports a native object model other than Microsoft Active Accessibility or UI Automation, it can expose the custom interface by responding to [**WM\_GETOBJECT**](wm-getobject.md) messages that include the [**OBJID\_NATIVEOM**](object-identifiers.md) object identifier.</span></span> <span data-ttu-id="ce08d-105">Para responder, o elemento de interface do usuário deve retornar o valor recuperado por uma chamada para a função [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) .</span><span class="sxs-lookup"><span data-stu-id="ce08d-105">To respond, the UI element should return the value retrieved by a call to the [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) function.</span></span>

<span data-ttu-id="ce08d-106">Um cliente pode recuperar uma interface de um elemento de interface do usuário que dá suporte a um modelo de objeto nativo chamando a função [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) e especificando [**OBJID \_ NATIVEOM**](object-identifiers.md) como o segundo parâmetro.</span><span class="sxs-lookup"><span data-stu-id="ce08d-106">A client can retrieve an interface from a UI element that supports a native object model by calling the [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) function and specifying [**OBJID\_NATIVEOM**](object-identifiers.md) as the second parameter.</span></span>

 

 




