---
description: Em alguns ambientes, um usuário não é automaticamente alertado para uma chamada de oferta, como por toque ou por uma mensagem na tela do computador.
ms.assetid: 50684e2a-0799-458b-9402-0958e35026d7
title: Aceitar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dd23d8ca1ed483b23d1b56fe98721b9fc53fb3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164385"
---
# <a name="accept"></a><span data-ttu-id="9a79d-103">Aceitar</span><span class="sxs-lookup"><span data-stu-id="9a79d-103">Accept</span></span>

<span data-ttu-id="9a79d-104">Em alguns ambientes, um usuário não é automaticamente alertado para uma chamada de oferta, como por toque ou por uma mensagem na tela do computador.</span><span class="sxs-lookup"><span data-stu-id="9a79d-104">In some environments, a user is not automatically alerted to an offering call, such as by ringing or by a message on their computer screen.</span></span> <span data-ttu-id="9a79d-105">A operação de aceitação inicia o processo de alerta (geralmente tocando) e a operação de [resposta](answer-ovr.md) ocorre posteriormente.</span><span class="sxs-lookup"><span data-stu-id="9a79d-105">The accept operation starts the process of alerting (usually ringing), and the [answer](answer-ovr.md) operation takes place afterward.</span></span> <span data-ttu-id="9a79d-106">O aplicativo pode [descartar](drop-ovr.md) a sessão, [redirecioná](redirect-ovr.md) -la ou aceitá-la.</span><span class="sxs-lookup"><span data-stu-id="9a79d-106">The application may [drop](drop-ovr.md) the session, [redirect](redirect-ovr.md) it, or accept it.</span></span>

<span data-ttu-id="9a79d-107">Se o provedor de serviços atual oferecer suporte a ele, o aplicativo terá a opção de enviar informações de usuário do usuário no momento da aceitação.</span><span class="sxs-lookup"><span data-stu-id="9a79d-107">If the current service provider supports it, the application has the option to send user-user information at the time of the accept.</span></span> <span data-ttu-id="9a79d-108">Não há nenhuma garantia de que a rede fornecerá essas informações à parte de chamada.</span><span class="sxs-lookup"><span data-stu-id="9a79d-108">There is no guarantee that the network will deliver this information to the calling party.</span></span>

<span data-ttu-id="9a79d-109">Nem todos os provedores de serviço dão suporte ao uso desta operação.</span><span class="sxs-lookup"><span data-stu-id="9a79d-109">Not all service providers support use of this operation.</span></span>

<span data-ttu-id="9a79d-110">**TAPI 2. x:** Consulte [**lineAccept**](/windows/win32/api/tapi/nf-tapi-lineaccept).</span><span class="sxs-lookup"><span data-stu-id="9a79d-110">**TAPI 2.x:** See [**lineAccept**](/windows/win32/api/tapi/nf-tapi-lineaccept).</span></span>

 

 
