---
title: Propriedades de anotação que têm WinEvents correspondente
description: Tenha cuidado ao substituir as propriedades que mudam com frequência, especialmente aquelas que são examinadas pelos clientes como resultado de um WinEvent (como estado, valor e, para alguns controles, as propriedades de nome).
ms.assetid: 2505d015-9381-4e1c-a10f-6db3fbb25ca3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04a8849c66cb0067b63be1c846e9e140ae06f4b6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366262"
---
# <a name="annotation-properties-that-have-corresponding-winevents"></a><span data-ttu-id="250f8-103">Propriedades de anotação que têm WinEvents correspondente</span><span class="sxs-lookup"><span data-stu-id="250f8-103">Annotation Properties That Have Corresponding WinEvents</span></span>

<span data-ttu-id="250f8-104">Tenha cuidado ao substituir as propriedades que mudam com frequência, especialmente aquelas que são examinadas pelos clientes como resultado de um WinEvent (como [**estado**](state-property.md), [**valor**](value-property.md)e, para alguns controles, as propriedades de [**nome**](name-property.md) ).</span><span class="sxs-lookup"><span data-stu-id="250f8-104">Be careful when overriding properties that change frequently, particularly those that are examined by clients as a result of a WinEvent (such as [**State**](state-property.md), [**Value**](value-property.md), and, for some controls, the [**Name**](name-property.md) properties).</span></span>

<span data-ttu-id="250f8-105">Em muitos casos, especialmente para controles USER e ComCtl, o WinEvent sinalizando uma alteração de propriedade é enviado antes que o proprietário do controle seja notificado (normalmente via [ \_ notificação do WM](../controls/wm-notify.md)).</span><span class="sxs-lookup"><span data-stu-id="250f8-105">In many cases, especially for USER and ComCtl controls, the WinEvent signaling a property change is sent before the owner of the control is notified (typically via [WM\_NOTIFY](../controls/wm-notify.md)).</span></span> <span data-ttu-id="250f8-106">Atualizar a propriedade usando [**SetPropValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-setpropvalue) no manipulador de \_ notificação do WM será muito tarde; os clientes que usam a conexão no contexto já terão acessado o valor antigo.</span><span class="sxs-lookup"><span data-stu-id="250f8-106">Updating the property using [**SetPropValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-setpropvalue) in the WM\_NOTIFY handler will be too late; clients using in-context hooking will already have accessed the old value.</span></span>

<span data-ttu-id="250f8-107">Você pode lidar com esses tipos de propriedades usando objetos de servidor de chamada de retorno (usando [**SetPropServer**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-setpropserver)); no entanto, o servidor não pode usar nenhum estado que seja atualizado no manipulador de notificação do WM \_ , pois esse manipulador ainda não terá sido chamado.</span><span class="sxs-lookup"><span data-stu-id="250f8-107">You can handle these types of properties by using callback server objects (using [**SetPropServer**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-setpropserver)); however, the server cannot use any state that is updated in the WM\_NOTIFY handler because that handler will not yet have been called.</span></span> <span data-ttu-id="250f8-108">Por exemplo, em vez de usar uma variável de valor atual armazenada em cache que é atualizada no manipulador de notificação do WM \_ e estará desatualizada, o objeto de retorno de chamada [**IAccPropServer:: GetPropValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropserver-getpropvalue) deve enviar uma mensagem diretamente para o controle para obter o valor atual real para gerar a propriedade necessária.</span><span class="sxs-lookup"><span data-stu-id="250f8-108">For example, instead of using a cached current value variable that is updated in the WM\_NOTIFY handler and will be out-of-date, the [**IAccPropServer::GetPropValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropserver-getpropvalue) callback object should send a message directly to the control to get its true current value to generate the required property.</span></span>

 

 