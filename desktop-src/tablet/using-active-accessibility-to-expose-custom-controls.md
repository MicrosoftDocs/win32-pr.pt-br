---
description: Descrição do uso da acessibilidade ativa para expor controles personalizados para o Tablet PC.
ms.assetid: 1557bde2-c382-4259-ae0c-a70902fa91bd
title: Usando Acessibilidade Ativa para expor controles personalizados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d33d4c2b57a881cfbdc15f14e71e339ed7f9e84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105810869"
---
# <a name="using-active-accessibility-to-expose-custom-controls"></a><span data-ttu-id="2cef2-103">Usando Acessibilidade Ativa para expor controles personalizados</span><span class="sxs-lookup"><span data-stu-id="2cef2-103">Using Active Accessibility to Expose Custom Controls</span></span>

<span data-ttu-id="2cef2-104">Você pode usar o Microsoft Acessibilidade Ativa como uma maneira eficaz de tornar os controles personalizados compatíveis com os recursos de acessibilidade.</span><span class="sxs-lookup"><span data-stu-id="2cef2-104">You can use Microsoft Active Accessibility as an effective way to make custom controls compatible with accessibility aids.</span></span> <span data-ttu-id="2cef2-105">Acessibilidade Ativa requer que o aplicativo:</span><span class="sxs-lookup"><span data-stu-id="2cef2-105">Active Accessibility requires that the application:</span></span>

-   <span data-ttu-id="2cef2-106">Crie objetos COM (Component Object Model) que representem controles personalizados individuais ou grupos de controles que dão suporte adequado à interface **IAccessible** .</span><span class="sxs-lookup"><span data-stu-id="2cef2-106">Create Component Object Model (COM) objects that represent individual custom controls or groups of controls that properly support the **IAccessible** interface.</span></span> <span data-ttu-id="2cef2-107">(O objeto pode ser criado sob demanda quando solicitado por um cliente Acessibilidade Ativa.)</span><span class="sxs-lookup"><span data-stu-id="2cef2-107">(The object may be created on demand when it is requested by an Active Accessibility client.)</span></span>
-   <span data-ttu-id="2cef2-108">Chame [**NotifyWinEvent**](/windows/win32/api/winuser/nf-winuser-notifywinevent) quando os controles forem criados ou destruídos, obter ou perder o foco ou alterar o estado.</span><span class="sxs-lookup"><span data-stu-id="2cef2-108">Call [**NotifyWinEvent**](/windows/win32/api/winuser/nf-winuser-notifywinevent) when the controls are created or destroyed, gain or lose focus, or otherwise change state.</span></span>
-   <span data-ttu-id="2cef2-109">Manipule a mensagem do WM \_ GetObject quando usada para consultar as propriedades do objeto ou dos objetos.</span><span class="sxs-lookup"><span data-stu-id="2cef2-109">Handle the WM\_GETOBJECT message when used to query properties of the object or objects.</span></span>

<span data-ttu-id="2cef2-110">Para os fins desta discussão, uma janela que contém outros objetos personalizados também precisa ser exposta a Acessibilidade Ativa, permitindo que o cliente descubra e navegue para os objetos filho.</span><span class="sxs-lookup"><span data-stu-id="2cef2-110">For the purposes of this discussion, a window containing other custom objects also needs to be exposed to Active Accessibility, allowing the client to discover and navigate to the child objects.</span></span> <span data-ttu-id="2cef2-111">Para obter mais informações sobre como tornar os controles personalizados compatíveis com os recursos de acessibilidade, consulte [acessibilidade](../accessibility/accessibility.md).</span><span class="sxs-lookup"><span data-stu-id="2cef2-111">For more information about how to make custom controls compatible with accessibility aids, see [Accessibility](../accessibility/accessibility.md).</span></span>

 

 
