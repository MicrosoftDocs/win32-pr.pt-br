---
description: Módulos de saída personalizados devem implementar a interface ICertExit, que é chamada pelo mecanismo do servidor.
ms.assetid: 509e7945-b656-4c4c-b5eb-45fbe80377c7
title: Gravando módulos de saída personalizados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81798996059e878ef11dbcdf290298094d0849cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105766814"
---
# <a name="writing-custom-exit-modules"></a><span data-ttu-id="9da26-103">Gravando módulos de saída personalizados</span><span class="sxs-lookup"><span data-stu-id="9da26-103">Writing Custom Exit Modules</span></span>

<span data-ttu-id="9da26-104">Módulos de saída personalizados devem implementar a interface [**ICertExit**](/windows/desktop/api/Certexit/nn-certexit-icertexit) , que é chamada pelo mecanismo do servidor.</span><span class="sxs-lookup"><span data-stu-id="9da26-104">Custom exit modules must implement the [**ICertExit**](/windows/desktop/api/Certexit/nn-certexit-icertexit) interface, which is called by the server engine.</span></span> <span data-ttu-id="9da26-105">O método [**ICertExit:: Initialize**](/windows/desktop/api/Certexit/nf-certexit-icertexit-initialize) é chamado pelo mecanismo de servidor quando o módulo de saída é carregado.</span><span class="sxs-lookup"><span data-stu-id="9da26-105">The [**ICertExit::Initialize**](/windows/desktop/api/Certexit/nf-certexit-icertexit-initialize) method is called by the server engine when the exit module is loaded.</span></span> <span data-ttu-id="9da26-106">Ele permite que o módulo de saída execute a inicialização e retorne um valor que informará ao mecanismo do servidor os tipos de eventos para os quais ele deseja notificação.</span><span class="sxs-lookup"><span data-stu-id="9da26-106">It allows the exit module to perform initialization and returns a value that informs the server engine of the kinds of events for which it wants notification.</span></span> <span data-ttu-id="9da26-107">O método [**ICertExit:: GetDescription**](/windows/desktop/api/Certexit/nf-certexit-icertexit-getdescription) deve retornar uma cadeia de caracteres de descrição quando o mecanismo do servidor a solicitar.</span><span class="sxs-lookup"><span data-stu-id="9da26-107">The [**ICertExit::GetDescription**](/windows/desktop/api/Certexit/nf-certexit-icertexit-getdescription) method must return a description string when the server engine requests it.</span></span> <span data-ttu-id="9da26-108">O método [**ICertExit:: Notify**](/windows/desktop/api/Certexit/nf-certexit-icertexit-notify) é chamado pelo mecanismo de servidor para notificar o módulo de saída de que um evento ocorreu.</span><span class="sxs-lookup"><span data-stu-id="9da26-108">The [**ICertExit::Notify**](/windows/desktop/api/Certexit/nf-certexit-icertexit-notify) method is called by the server engine to notify the exit module that an event has occurred.</span></span>

<span data-ttu-id="9da26-109">Os módulos de saída podem chamar a interface [**ICertServerExit**](/windows/desktop/api/Certif/nn-certif-icertserverexit) , que dá suporte a muitos dos mesmos métodos da interface [**ICertServerPolicy**](/windows/desktop/api/Certif/nn-certif-icertserverpolicy) , com exceção dos métodos [**SetCertificateExtension**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateextension) e [**setcertificaproperty**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateproperty) .</span><span class="sxs-lookup"><span data-stu-id="9da26-109">Exit modules can call the [**ICertServerExit**](/windows/desktop/api/Certif/nn-certif-icertserverexit) interface, which supports many of the same methods as the [**ICertServerPolicy**](/windows/desktop/api/Certif/nn-certif-icertserverpolicy) interface, with the exception of the [**SetCertificateExtension**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateextension) and [**SetCertificateProperty**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateproperty) methods.</span></span>

<span data-ttu-id="9da26-110">Para obter informações sobre como remover o módulo de saída existente e instalar um novo, consulte o tópico sobre a personalização do módulo de saída na ajuda.</span><span class="sxs-lookup"><span data-stu-id="9da26-110">For information about removing the existing exit module and installing a new one, see the Exit Module Customization topic in Help.</span></span>

 

 



