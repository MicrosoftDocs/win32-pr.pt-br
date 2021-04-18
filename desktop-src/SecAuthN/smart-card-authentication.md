---
description: Autenticação de cartão inteligente
ms.assetid: cb5c80ea-c15e-4f68-a94b-b458d69ff474
title: Autenticação de cartão inteligente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6241d323f4c5e982fee96f44002da316d5d645d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105751611"
---
# <a name="smart-card-authentication"></a><span data-ttu-id="b9ebe-103">Autenticação de cartão inteligente</span><span class="sxs-lookup"><span data-stu-id="b9ebe-103">Smart Card Authentication</span></span>

<span data-ttu-id="b9ebe-104">As partes básicas do [*subsistema de cartão inteligente*](../secgloss/s-gly.md) são baseadas em padrões de PC/SC (consulte as especificações em [https://www.pcscworkgroup.com/](https://www.pcscworkgroup.com/) ).</span><span class="sxs-lookup"><span data-stu-id="b9ebe-104">The basic parts of the [*smart card subsystem*](../secgloss/s-gly.md) are based on PC/SC standards (see the specifications at [https://www.pcscworkgroup.com/](https://www.pcscworkgroup.com/)).</span></span> <span data-ttu-id="b9ebe-105">Essas partes básicas incluem:</span><span class="sxs-lookup"><span data-stu-id="b9ebe-105">These basic parts include:</span></span>

-   <span data-ttu-id="b9ebe-106">Um [*Gerenciador de recursos*](../secgloss/r-gly.md) que usa uma API do Windows.</span><span class="sxs-lookup"><span data-stu-id="b9ebe-106">A [*resource manager*](../secgloss/r-gly.md) that uses a Windows API.</span></span>
-   <span data-ttu-id="b9ebe-107">Uma [*interface do usuário*](../secgloss/u-gly.md) que funciona com o Gerenciador de recursos.</span><span class="sxs-lookup"><span data-stu-id="b9ebe-107">A [*user interface*](../secgloss/u-gly.md) (UI) that works with the resource manager.</span></span>
-   <span data-ttu-id="b9ebe-108">Vários [*provedores de serviço*](../secgloss/s-gly.md) base que fornecem acesso a serviços específicos.</span><span class="sxs-lookup"><span data-stu-id="b9ebe-108">Several base [*service providers*](../secgloss/s-gly.md) that provide access to specific services.</span></span> <span data-ttu-id="b9ebe-109">Ao contrário da API do Windows do Gerenciador de recursos, os provedores de serviço usam um modelo de interface COM para fornecer serviços de [*cartão inteligente*](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="b9ebe-109">In contrast to the resource manager's Windows API, service providers use a COM interface model to provide [*smart card*](../secgloss/s-gly.md) services.</span></span>

<span data-ttu-id="b9ebe-110">A ilustração a seguir mostra as relações dessas partes na arquitetura geral do cartão inteligente.</span><span class="sxs-lookup"><span data-stu-id="b9ebe-110">The following illustration shows the relationships of these parts in the overall smart card architecture.</span></span>

![arquitetura de cartão inteligente](images/smartovr2a.png)

<span data-ttu-id="b9ebe-112">Para obter informações sobre como o [*subsistema de cartão inteligente*](../secgloss/s-gly.md) funciona com outros serviços disponíveis no Microsoft Internet Security Framework, consulte [relação a outros serviços](relation-to-other-services.md).</span><span class="sxs-lookup"><span data-stu-id="b9ebe-112">For information about how the [*smart card subsystem*](../secgloss/s-gly.md) works with other services available in the Microsoft Internet Security Framework, see [Relation to Other Services](relation-to-other-services.md).</span></span>

<span data-ttu-id="b9ebe-113">Para obter informações sobre a autenticação de cartão inteligente, consulte os tópicos a seguir.</span><span class="sxs-lookup"><span data-stu-id="b9ebe-113">For information about smart card authentication, see the following topics.</span></span>



| <span data-ttu-id="b9ebe-114">Tópicos</span><span class="sxs-lookup"><span data-stu-id="b9ebe-114">Topics</span></span>                                                                      | <span data-ttu-id="b9ebe-115">Sumário</span><span class="sxs-lookup"><span data-stu-id="b9ebe-115">Contents</span></span>                                                                                                                                                                                                                                           |
|-----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b9ebe-116">Conceitos de cartão inteligente</span><span class="sxs-lookup"><span data-stu-id="b9ebe-116">Smart Card Concepts</span></span>](smart-card-concepts.md)<br/>                   | <span data-ttu-id="b9ebe-117">Conceitos básicos e a descrição da interação entre usuários e cartões inteligentes.</span><span class="sxs-lookup"><span data-stu-id="b9ebe-117">Basic concepts and description of the interaction between users and smart cards.</span></span><br/>                                                                                                                                                        |
| [<span data-ttu-id="b9ebe-118">Gerenciador de recursos de cartão inteligente</span><span class="sxs-lookup"><span data-stu-id="b9ebe-118">Smart Card Resource Manager</span></span>](smart-card-resource-manager.md)<br/>   | <span data-ttu-id="b9ebe-119">Informações sobre a API do Gerenciador de recursos, que gerencia o acesso a [*leitores*](../secgloss/r-gly.md) e a [*cartões inteligentes*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="b9ebe-119">Information about the resource manager API, which manages the access to [*readers*](../secgloss/r-gly.md) and to [*smart cards*](../secgloss/s-gly.md).</span></span><br/> |
| [<span data-ttu-id="b9ebe-120">Interface do usuário do cartão inteligente</span><span class="sxs-lookup"><span data-stu-id="b9ebe-120">Smart Card User Interface</span></span>](smart-card-user-interface.md)<br/>       | <span data-ttu-id="b9ebe-121">Informações sobre a [*caixa de diálogo comum do cartão inteligente*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="b9ebe-121">Information about the [*smart card common dialog box*](../secgloss/s-gly.md).</span></span><br/>                                                                                   |
| [<span data-ttu-id="b9ebe-122">Provedores de serviço de cartão inteligente</span><span class="sxs-lookup"><span data-stu-id="b9ebe-122">Smart Card Service Providers</span></span>](smart-card-service-providers.md)<br/> | <span data-ttu-id="b9ebe-123">Informações sobre interfaces, comandos e wrappers que fornecem recursos de cartão inteligente.</span><span class="sxs-lookup"><span data-stu-id="b9ebe-123">Information about interfaces, commands, and wrappers that provide smart card capabilities.</span></span><br/>                                                                                                                                              |



 

<span data-ttu-id="b9ebe-124">Além disso, os desenvolvimentos de cartão inteligente atuais da Microsoft podem ser encontrados em [https://www.microsoft.com/whdc/device/input/smartcard/default.mspx](https://www.microsoft.com/whdc/device/input/smartcard/default.mspx) .</span><span class="sxs-lookup"><span data-stu-id="b9ebe-124">Additionally, current Microsoft smart card developments can be found at [https://www.microsoft.com/whdc/device/input/smartcard/default.mspx](https://www.microsoft.com/whdc/device/input/smartcard/default.mspx).</span></span>

 

 
