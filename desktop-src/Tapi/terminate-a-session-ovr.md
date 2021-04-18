---
description: O encerramento da sessão pode ser originado com uma solicitação do usuário, desconexão remota por outra parte ou por motivos específicos do aplicativo.
ms.assetid: 69ed2e2c-f1c7-4f69-86a0-3cfdd80e423d
title: Encerrar uma sessão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac433f1c8104ec41a3c42dc44c32a2b110d79469
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105760325"
---
# <a name="terminate-a-session"></a><span data-ttu-id="04bff-103">Encerrar uma sessão</span><span class="sxs-lookup"><span data-stu-id="04bff-103">Terminate a Session</span></span>

<span data-ttu-id="04bff-104">O encerramento da sessão pode ser originado com uma solicitação do usuário, desconexão remota por outra parte ou por motivos específicos do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="04bff-104">Session termination may originate with a user request, remote disconnection by the other party, or for application-specific reasons.</span></span> <span data-ttu-id="04bff-105">Quando uma sessão é encerrada, o [identificador de sessão](session-identifier-ovr.md) permanece válido até ser liberado especificamente e pode ser usado para coletar dados de pós-conexão.</span><span class="sxs-lookup"><span data-stu-id="04bff-105">When a session is terminated, the [session identifier](session-identifier-ovr.md) remains valid until specifically released and can be used to gather post-connection data.</span></span>

<span data-ttu-id="04bff-106">O encerramento da sessão é concluído pela desalocação e liberação dos recursos associados à sessão.</span><span class="sxs-lookup"><span data-stu-id="04bff-106">Session termination is completed by deallocating and releasing the resources associated with the session.</span></span> <span data-ttu-id="04bff-107">Se uma sessão for meramente descartada ou desconectada, mas os recursos não forem liberados, o resultado será um vazamento de memória no aplicativo e possivelmente no provedor de serviços também.</span><span class="sxs-lookup"><span data-stu-id="04bff-107">If a session is merely dropped or disconnected but resources are not released, the result is a memory leak in the application and possibly in the service provider as well.</span></span>

<span data-ttu-id="04bff-108">**TAPI 2. x:** Consulte [**lineDrop**](/windows/win32/api/tapi/nf-tapi-linedrop), [**lineDeallocateCall**](/windows/win32/api/tapi/nf-tapi-linedeallocatecall).</span><span class="sxs-lookup"><span data-stu-id="04bff-108">**TAPI 2.x:** See [**lineDrop**](/windows/win32/api/tapi/nf-tapi-linedrop), [**lineDeallocateCall**](/windows/win32/api/tapi/nf-tapi-linedeallocatecall).</span></span>

<span data-ttu-id="04bff-109">**TAPI 3. x:** Consulte [**ITBasicCallControl::D isconnect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-disconnect), executar uma versão com padrão no ponteiro de objeto de chamada.</span><span class="sxs-lookup"><span data-stu-id="04bff-109">**TAPI 3.x:** See [**ITBasicCallControl::Disconnect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-disconnect), perform a standard COM release on the Call object pointer.</span></span>

 

 
