---
description: A operação de resposta é uma resposta típica aos aplicativos para uma sessão de comunicações oferecida. Se for bem-sucedida, essa operação fará com que uma sessão faça a transição para o estado conectado.
ms.assetid: 34ac0b34-1d1b-4657-a737-27a4ed9326af
title: Resposta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e08081b32b7ba3a3a24cde3ec37c1a6118582cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104505917"
---
# <a name="answer"></a><span data-ttu-id="e45ad-104">Resposta</span><span class="sxs-lookup"><span data-stu-id="e45ad-104">Answer</span></span>

<span data-ttu-id="e45ad-105">A operação de resposta é uma resposta típica do aplicativo a uma sessão de comunicações oferecida.</span><span class="sxs-lookup"><span data-stu-id="e45ad-105">The answer operation is an application's typical response to an offered communications session.</span></span> <span data-ttu-id="e45ad-106">Se for bem-sucedida, essa operação fará com que uma sessão faça a transição para o estado conectado.</span><span class="sxs-lookup"><span data-stu-id="e45ad-106">If successful, this operation causes a session to transition into the connected state.</span></span>

<span data-ttu-id="e45ad-107">Em alguns ambientes de telefonia (como o ISDN), onde os alertas do usuário são separados da oferta de chamada, o aplicativo tem a opção de [aceitar](accept-ovr.md) uma chamada antes de responder ou rejeitar ([remover](drop-ovr.md)) ou [redirecionar](redirect-ovr.md) a chamada de *oferta* .</span><span class="sxs-lookup"><span data-stu-id="e45ad-107">In some telephony environments (like ISDN), where user alerting is separate from call offering, the application has the option to [accept](accept-ovr.md) a call prior to answering or to reject ([drop](drop-ovr.md)) or [redirect](redirect-ovr.md) the *offering* call.</span></span>

<span data-ttu-id="e45ad-108">Se uma operação de resposta for executada para uma nova sessão quando uma sessão já estiver ativa, o efeito que ela tem na sessão ativa existente dependerá dos recursos do provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="e45ad-108">If an answer operation is performed for a new session when a session is already active, the effect this has on the existing active session depends on the service provider's capabilities.</span></span> <span data-ttu-id="e45ad-109">A primeira chamada pode não ser afetada, pode ser descartada automaticamente ou pode ser automaticamente colocada em espera.</span><span class="sxs-lookup"><span data-stu-id="e45ad-109">The first call can be unaffected, it can automatically be dropped, or it can automatically be placed on hold.</span></span> <span data-ttu-id="e45ad-110">A TAPI enviará as notificações de eventos apropriadas relacionadas às duas chamadas.</span><span class="sxs-lookup"><span data-stu-id="e45ad-110">TAPI will send the appropriate event notifications concerning both calls.</span></span>

<span data-ttu-id="e45ad-111">Em uma situação de ponte, se uma chamada estiver conectada, mas no estado ativo, ela poderá ser unida usando a operação de resposta.</span><span class="sxs-lookup"><span data-stu-id="e45ad-111">In a bridged situation, if a call is connected but in the active state, it can be joined using the answer operation.</span></span>

<span data-ttu-id="e45ad-112">O aplicativo tem a opção de enviar informações do usuário no momento da resposta, se o provedor de serviços oferecer suporte a ela.</span><span class="sxs-lookup"><span data-stu-id="e45ad-112">The application has the option to send user-user information at the time of the answer, if the service provider supports it.</span></span>

<span data-ttu-id="e45ad-113">**TAPI 2. x:** Consulte [**lineAnswer**](/windows/win32/api/tapi/nf-tapi-lineanswer).</span><span class="sxs-lookup"><span data-stu-id="e45ad-113">**TAPI 2.x:** See [**lineAnswer**](/windows/win32/api/tapi/nf-tapi-lineanswer).</span></span>

<span data-ttu-id="e45ad-114">**TAPI 3. x:** Consulte [**ITBasicCallControl:: answer**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-answer).</span><span class="sxs-lookup"><span data-stu-id="e45ad-114">**TAPI 3.x:** See [**ITBasicCallControl::Answer**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-answer).</span></span>

 

 
