---
description: Descartar ou desconectar uma sessão encerra a comunicação. O aplicativo tem a opção de enviar informações do usuário no momento da desconexão, se o provedor de serviços oferecer suporte a ela.
ms.assetid: dc348bb2-d564-40f8-afe3-5473c5769fa4
title: Remover
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a9bf3705d9b104b8816ce4b493ec6b188c5fe1c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920797"
---
# <a name="drop"></a><span data-ttu-id="739ff-104">Remover</span><span class="sxs-lookup"><span data-stu-id="739ff-104">Drop</span></span>

<span data-ttu-id="739ff-105">Descartar ou desconectar uma sessão encerra a comunicação.</span><span class="sxs-lookup"><span data-stu-id="739ff-105">Dropping or disconnecting a session terminates communication.</span></span> <span data-ttu-id="739ff-106">O aplicativo tem a opção de enviar informações do usuário no momento da desconexão, se o provedor de serviços oferecer suporte a ela.</span><span class="sxs-lookup"><span data-stu-id="739ff-106">The application has the option of sending user-user information at the time of the disconnect, if the service provider supports it.</span></span>

<span data-ttu-id="739ff-107">Os motivos usuais para descartar uma sessão é que um usuário solicitou uma desconexão ou a outra extremidade da sessão foi descartada.</span><span class="sxs-lookup"><span data-stu-id="739ff-107">The usual reasons for dropping a session is a user has requested a disconnect or the other end of the session has dropped.</span></span> <span data-ttu-id="739ff-108">Uma operação de remoção também pode ser chamada quando a TAPI oferece uma sessão para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="739ff-108">A drop operation may also be called when TAPI offers a session to the application.</span></span> <span data-ttu-id="739ff-109">Se o provedor de serviços oferecer suporte a isso, o efeito é que o aplicativo rejeita a chamada.</span><span class="sxs-lookup"><span data-stu-id="739ff-109">If the service provider supports this, the effect is that the application rejects the call.</span></span>

<span data-ttu-id="739ff-110">Ao invocar uma operação de remoção, as sessões relacionadas às vezes podem ser também afetadas.</span><span class="sxs-lookup"><span data-stu-id="739ff-110">When invoking a drop operation, related sessions can sometimes be affected as well.</span></span> <span data-ttu-id="739ff-111">Por exemplo, remover uma chamada de conferência pode descartar todos os participantes individuais.</span><span class="sxs-lookup"><span data-stu-id="739ff-111">For example, dropping a conference call can drop all individual participants.</span></span> <span data-ttu-id="739ff-112">As mensagens de alteração de estado são enviadas para o aplicativo para todas as chamadas cujo estado é afetado.</span><span class="sxs-lookup"><span data-stu-id="739ff-112">State change messages are sent to the application for all calls whose state is affected.</span></span>

<span data-ttu-id="739ff-113">Em várias configurações de ponte ou de linha de terceiros quando várias partes estão na chamada, uma operação de soltar pode não limpar realmente a chamada.</span><span class="sxs-lookup"><span data-stu-id="739ff-113">In various bridged or party-line configurations when multiple parties are on the call, a drop operation may not actually clear the call.</span></span> <span data-ttu-id="739ff-114">Por exemplo, em uma situação de ponte, a chamada pode não ser descartada porque o status de outras estações na chamada pode governar.</span><span class="sxs-lookup"><span data-stu-id="739ff-114">For example, in a bridged situation, the call may not be dropped because the status of other stations on the call may govern.</span></span> <span data-ttu-id="739ff-115">Em vez disso, a chamada pode ser simplesmente alterada para o estado inativo enquanto estiver restante conectada em outras estações.</span><span class="sxs-lookup"><span data-stu-id="739ff-115">Instead, the call may simply be changed to the inactive state while remaining connected at other stations.</span></span>

<span data-ttu-id="739ff-116">Após uma operação de soltar, o identificador de sessão e a maioria dos recursos associados à sessão permanecerão utilizáveis para a maioria das operações de consulta.</span><span class="sxs-lookup"><span data-stu-id="739ff-116">Following a drop operation, the session identifier and most resources associated with the session will remain usable for most query operations.</span></span> <span data-ttu-id="739ff-117">Quando um aplicativo não exige mais esses recursos, ele deve [encerrar a sessão](terminate-a-session-ovr.md) para evitar vazamentos de memória.</span><span class="sxs-lookup"><span data-stu-id="739ff-117">When an application no longer requires these resources, it must [terminate the session](terminate-a-session-ovr.md) in order to avoid memory leaks.</span></span>

<span data-ttu-id="739ff-118">**TAPI 2. x:** Consulte [**lineDrop**](/windows/win32/api/tapi/nf-tapi-linedrop).</span><span class="sxs-lookup"><span data-stu-id="739ff-118">**TAPI 2.x:** See [**lineDrop**](/windows/win32/api/tapi/nf-tapi-linedrop).</span></span>

<span data-ttu-id="739ff-119">**TAPI 3. x:** Consulte [**ITBasicCallControl::D isconnect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-disconnect).</span><span class="sxs-lookup"><span data-stu-id="739ff-119">**TAPI 3.x:** See [**ITBasicCallControl::Disconnect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-disconnect).</span></span>

 

 
