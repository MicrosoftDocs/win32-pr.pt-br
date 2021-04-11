---
title: Sequência de chamada da API do método de túnel
description: Saiba mais sobre a sequência de chamadas de API para métodos de túnel. Consulte uma visão geral e exiba recursos adicionais disponíveis.
ms.assetid: 48aad213-1d29-4809-9599-b56325b2b8e8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef5f6b30fda111162585fb5c8b2aa370fa6af61e
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104294516"
---
# <a name="tunnel-method-api-call-sequence"></a><span data-ttu-id="e785b-104">Sequência de chamada da API do método de túnel</span><span class="sxs-lookup"><span data-stu-id="e785b-104">Tunnel Method API Call Sequence</span></span>

<span data-ttu-id="e785b-105">Este tópico aborda a sequência de chamadas de API para métodos de túnel</span><span class="sxs-lookup"><span data-stu-id="e785b-105">This topic covers the API call sequence for Tunnel Methods</span></span>

## <a name="tunnel-method-call-sequence-overview"></a><span data-ttu-id="e785b-106">Visão geral da sequência de chamada do método de túnel</span><span class="sxs-lookup"><span data-stu-id="e785b-106">Tunnel Method Call Sequence Overview</span></span>

<span data-ttu-id="e785b-107">Quando o suplicante recebe solicitação para dados de usuário e identidade de usuário, normalmente ocorre o seguinte fluxo de chamada de API.</span><span class="sxs-lookup"><span data-stu-id="e785b-107">When Supplicant gets request for user identity and user data the following API call flow typically occurs.</span></span>

-   <span data-ttu-id="e785b-108">O suplicante chama EapHostPeerProcessReceivedPacket no EapHost para processar o pacote recebido do autenticador.</span><span class="sxs-lookup"><span data-stu-id="e785b-108">The Supplicant calls EapHostPeerProcessReceivedPacket on EapHost, to process the packet received from the authenticator.</span></span>
-   <span data-ttu-id="e785b-109">Ao processar esse pacote, o EAPHost o determina como pacote IdentityRequest e chama o [**EapPeerGetIdentity**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetidentity) no método de túnel para obter a identidade do usuário a ser usada para autenticação.</span><span class="sxs-lookup"><span data-stu-id="e785b-109">Upon processing this packet, EAPHost determines it as IdentityRequest packet and calls [**EapPeerGetIdentity**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetidentity) on tunnel method to obtain the user identity to use for authentication.</span></span>
-   <span data-ttu-id="e785b-110">Se o método de túnel precisar obter a identidade do usuário a partir do método interno, ele chamará [**EAPHostPeerGetIdentity**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetidentity) no EAPHost interno que, por sua vez, chamará [**EapPeerGetIdentity**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetidentity) no método interno.</span><span class="sxs-lookup"><span data-stu-id="e785b-110">If tunnel method needs to obtain user identity from the inner method, it calls [**EAPHostPeerGetIdentity**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetidentity) on inner EAPHost, which in turn calls [**EapPeerGetIdentity**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetidentity) on the inner method.</span></span>

## <a name="user-interaction-with-the-tunnel-methods-api-call-flow"></a><span data-ttu-id="e785b-111">Interação do usuário com o fluxo de chamadas da API dos métodos de túnel</span><span class="sxs-lookup"><span data-stu-id="e785b-111">User Interaction with the Tunnel Methods API Call Flow</span></span>

<span data-ttu-id="e785b-112">Em determinados casos, quando a identidade não está disponível ou quando o usuário deve fornecer informações adicionais, o método EAP gera uma caixa de diálogo de interface do usuário no suplicante.</span><span class="sxs-lookup"><span data-stu-id="e785b-112">In certain cases, when the identity is not available, or when the user must provide additional information, Eap Method raises an user interface dialog box on the supplicant.</span></span>

<span data-ttu-id="e785b-113">Nesses casos, a seqüência de chamada a seguir normalmente ocorre para obter informações diretamente do usuário.</span><span class="sxs-lookup"><span data-stu-id="e785b-113">In such cases following call sequence typically takes place to get information directly from the user.</span></span>

-   <span data-ttu-id="e785b-114">O método EAP de túnel retorna o código de ação para invocar a interface do usuário para EapHost.</span><span class="sxs-lookup"><span data-stu-id="e785b-114">Tunnel Eap Method returns action code to invoke UI to EapHost.</span></span> <span data-ttu-id="e785b-115">O suplicante chama [**EapHostPeerGetUIContext**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetuicontext)para obter as informações de contexto da interface do usuário atual para a caixa de diálogo interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="e785b-115">Supplicant calls [**EapHostPeerGetUIContext**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetuicontext)to obtain the current user interface context information for the user interface dialog box.</span></span>
-   <span data-ttu-id="e785b-116">Em seguida, o suplicante chama [ **EapHostPeerInvokeInteractiveUI.**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeinteractiveui)</span><span class="sxs-lookup"><span data-stu-id="e785b-116">Supplicant then calls [**EapHostPeerInvokeInteractiveUI.**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeinteractiveui)</span></span> <span data-ttu-id="e785b-117">Essa função usa as informações de contexto da interface do usuário para gerar uma interface de usuários interativa que é usada para obter informações de credenciais do usuário.</span><span class="sxs-lookup"><span data-stu-id="e785b-117">This function uses the UI context information to raise an interactive user interface which is used to get credential information from the user.</span></span> <span data-ttu-id="e785b-118">O processo da interface do usuário carrega Eappcfg.dll e obtém os ponteiros para EapPeerInvokeInteractiveUI e EapPeerFreeMemory.</span><span class="sxs-lookup"><span data-stu-id="e785b-118">The UI process loads Eappcfg.dll and obtains the pointers to EapPeerInvokeInteractiveUI and EapPeerFreeMemory.</span></span>
    > [!Note]  
    > <span data-ttu-id="e785b-119">O processo de interface do usuário normalmente coleta a interface do usuário ou manipula a interface do usuário interativa e é separado do processo suplicante.</span><span class="sxs-lookup"><span data-stu-id="e785b-119">UI process typically collects UI or handles interactive UI and is separate from the supplicant process.</span></span> <span data-ttu-id="e785b-120">Separar os dois processos não é um requisito do EAPHost, mas isso tem a vantagem de permitir que o processo da interface do usuário interaja com a área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="e785b-120">Separating the two processes is not a requirement of EAPHost, but doing so has the advantage of allowing the UI process to interact with the desktop.</span></span>

     

-   <span data-ttu-id="e785b-121">O EapHost chama [**EapPeerInvokeIdentityUI**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinvokeidentityui) no método de túnel para obter informações de identidade do usuário.</span><span class="sxs-lookup"><span data-stu-id="e785b-121">EapHost calls [**EapPeerInvokeIdentityUI**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinvokeidentityui) on tunnel method to obtain user identity information.</span></span>
-   <span data-ttu-id="e785b-122">Para obter a identidade do usuário do método interno, o método de túnel chama [**EapHostPeerInvokeIdentityUI**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeidentityui) no EAPHost interno.</span><span class="sxs-lookup"><span data-stu-id="e785b-122">In order to obtain user identity from inner method, tunnel method calls [**EapHostPeerInvokeIdentityUI**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeidentityui) on inner EAPHost.</span></span>
-   <span data-ttu-id="e785b-123">O EAPHost interno chama [**EapPeerInvokeIdentityUI**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinvokeidentityui) no método interno para invocar a IU de identidade do usuário.</span><span class="sxs-lookup"><span data-stu-id="e785b-123">Inner EAPHost calls [**EapPeerInvokeIdentityUI**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinvokeidentityui) on inner method to invoke user identity UI.</span></span>
-   <span data-ttu-id="e785b-124">[**EapHostPeerSetUIContext**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeersetuicontext) fornece uma nova ou atualizada informações de contexto de interface do usuário para o método EAP peer carregado no EAPHost depois que a interface do usuário é gerada.</span><span class="sxs-lookup"><span data-stu-id="e785b-124">[**EapHostPeerSetUIContext**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeersetuicontext) provides a new or updated UI context information to the EAP peer method loaded on EAPHost after the UI has been raised.</span></span>

<span data-ttu-id="e785b-125">O diagrama a seguir explica a sequência de chamadas de API para métodos de túnel</span><span class="sxs-lookup"><span data-stu-id="e785b-125">Following diagram explains the API Call Sequence for Tunnel Methods</span></span>

![sequência de chamadas de API de métodos de túnel](images/tunnel-identity-processing-new.png)

## <a name="related-topics"></a><span data-ttu-id="e785b-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e785b-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e785b-128">Sequência de chamadas EAPHost</span><span class="sxs-lookup"><span data-stu-id="e785b-128">EAPHost Call Sequence</span></span>](about-eaphost-call-sequences.md)
</dt> <dt>

[<span data-ttu-id="e785b-129">Sequência de chamadas da API suplicante</span><span class="sxs-lookup"><span data-stu-id="e785b-129">Supplicant API Call Sequence</span></span>](supplicant-api-call-sequence.md)
</dt> <dt>

[<span data-ttu-id="e785b-130">Referência de API do suplicante EAPHost</span><span class="sxs-lookup"><span data-stu-id="e785b-130">EAPHost Supplicant API Reference</span></span>](eap-host-supplicant-api-reference.md)
</dt> </dl>

 

 




