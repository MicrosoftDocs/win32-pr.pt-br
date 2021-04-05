---
title: Implementando o suporte a NAP para métodos EAP
description: Saiba como implementar o suporte a NAP para um suplicante EAPHost. Consulte os tópicos NAP relacionados ao EAPHost e exiba recursos adicionais disponíveis.
ms.assetid: c25e4f03-759a-47a7-8b35-bbe669501c5c
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e5f0bc8900ee3d9cb01edb79b64b8ef5a68df4c
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/18/2020
ms.locfileid: "104008637"
---
# <a name="implementing-nap-support-for-eap-methods"></a><span data-ttu-id="16fb1-104">Implementando o suporte a NAP para métodos EAP</span><span class="sxs-lookup"><span data-stu-id="16fb1-104">Implementing NAP Support for EAP Methods</span></span>

<span data-ttu-id="16fb1-105">Este tópico explica como implementar a NAP para um suplicante do EAPHost.</span><span class="sxs-lookup"><span data-stu-id="16fb1-105">This topic explains how to implement NAP for an EAPHost supplicant.</span></span> <span data-ttu-id="16fb1-106">No Windows Vista e no Windows Server 2008, um cliente de imposição de NAP (NAP EC) está disponível para conexões autenticadas [802.1 x](/previous-versions/windows/embedded/ms890287(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="16fb1-106">In Windows Vista and Windows Server 2008 a NAP Enforcement Client (NAP EC) is available for [802.1X](/previous-versions/windows/embedded/ms890287(v=msdn.10)) authenticated connections.</span></span>

## <a name="implementing-network-access-protection-nap"></a><span data-ttu-id="16fb1-107">Implementando a NAP (proteção de acesso à rede)</span><span class="sxs-lookup"><span data-stu-id="16fb1-107">Implementing Network Access Protection (NAP)</span></span>

<span data-ttu-id="16fb1-108">Para oferecer suporte a NAP, um suplicante EAPHost implementa uma função de retorno de chamada que corresponde ao protótipo de retorno de chamada [**NotificationHandler**](/previous-versions/windows/desktop/api) e deve fornecer um ponteiro para essa função de retorno de chamada ao chamar [**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession).</span><span class="sxs-lookup"><span data-stu-id="16fb1-108">To support NAP, an EAPHost supplicant implements a callback function matching the [**NotificationHandler**](/previous-versions/windows/desktop/api) callback prototype and must provide a pointer to this callback function when calling [**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession).</span></span>

<span data-ttu-id="16fb1-109">A função de retorno de chamada usa dois parâmetros.</span><span class="sxs-lookup"><span data-stu-id="16fb1-109">The callback function takes two parameters.</span></span>

-   <span data-ttu-id="16fb1-110">Um GUID que identifica exclusivamente a interface associada à autenticação.</span><span class="sxs-lookup"><span data-stu-id="16fb1-110">A GUID that uniquely identifies the interface associated with the authentication.</span></span>
-   <span data-ttu-id="16fb1-111">Um ponteiro VOID para uma estrutura de dados opaca que é fornecida pelo suplicante.</span><span class="sxs-lookup"><span data-stu-id="16fb1-111">A VOID pointer to an opaque data structure that is supplied by the supplicant.</span></span>

<span data-ttu-id="16fb1-112">O EAPHost chamará a função de retorno de chamada fornecida pelo suplicante com o GUID de interface exclusivo e o ponteiro VOID quando o estado de quarentena da máquina for alterado.</span><span class="sxs-lookup"><span data-stu-id="16fb1-112">EAPHost will call the supplicant-provided callback function with the unique interface GUID and the VOID pointer when the quarantine state of the machine changes.</span></span> <span data-ttu-id="16fb1-113">Quando o EAPHost chama a função de retorno de chamada fornecida pelo suplicante, o suplicante responde subdividindo a conexão de rede lógica identificada pelo ponteiro da interface GUID/VOID e começa a autenticação novamente usando **EapHostPeerBeginSession**.</span><span class="sxs-lookup"><span data-stu-id="16fb1-113">When EAPHost calls the supplicant-provided callback function, the supplicant responds by tearing down the logical network connection identified by the interface GUID/VOID pointer and begins authentication again using **EapHostPeerBeginSession**.</span></span>

<span data-ttu-id="16fb1-114">O EAPHost pode chamar a função de retorno de chamada fornecida pelo suplicante a qualquer momento: antes, durante uma autenticação ativa ou após a conclusão da autenticação (após [**EapHostPeerEndSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerendsession) ter sido chamado, mas não antes de [**EapHostPeerClearConnection**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerclearconnection) ser chamado).</span><span class="sxs-lookup"><span data-stu-id="16fb1-114">EAPHost may call the supplicant-supplied callback function at any time: before, during an active authentication, or after the authentication has been completed (after [**EapHostPeerEndSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerendsession) has been called but not before [**EapHostPeerClearConnection**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerclearconnection) has been called).</span></span> <span data-ttu-id="16fb1-115">O suplicante deve sempre responder subdividindo a conexão de rede lógica e autenticando novamente.</span><span class="sxs-lookup"><span data-stu-id="16fb1-115">The supplicant should always respond by tearing down the logical network connection and re-authenticating.</span></span>

<span data-ttu-id="16fb1-116">Se o suplicante estiver sendo desligado ou optar por não receber mais notificação de alterações de estado de isolamento, o suplicante deverá chamar [**EapHostPeerClearConnection**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerclearconnection) e especificar o GUID de interface apropriado.</span><span class="sxs-lookup"><span data-stu-id="16fb1-116">If the supplicant is shutting down or choosing to no longer receive notification of isolation state changes, the supplicant should call [**EapHostPeerClearConnection**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerclearconnection) and specify the appropriate interface GUID.</span></span> <span data-ttu-id="16fb1-117">Se o suplicante quiser determinar o isolamento da conexão de rede lógica, o suplicante poderá obter essas informações de **EapHostPeerMethodResult. isolable** quando o [**EapHostPeerMethodResult**](/windows/win32/api/eaphostpeertypes/ns-eaphostpeertypes-eaphostpeermethodresult) for obtido de [**EapHostPeerGetResult**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetresult).</span><span class="sxs-lookup"><span data-stu-id="16fb1-117">If the supplicant wishes to determine the isolation of the logical network connection, the supplicant can obtain that information from **EapHostPeerMethodResult.isolationState** when the [**EapHostPeerMethodResult**](/windows/win32/api/eaphostpeertypes/ns-eaphostpeertypes-eaphostpeermethodresult) is obtained from [**EapHostPeerGetResult**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetresult).</span></span>

## <a name="eaphost-related-nap-information"></a><span data-ttu-id="16fb1-118">Informações de NAP relacionadas ao EAPHost</span><span class="sxs-lookup"><span data-stu-id="16fb1-118">EAPHost Related NAP Information</span></span>

<span data-ttu-id="16fb1-119">Para obter informações de NAP relacionadas à API EAPHost, consulte os tópicos a seguir.</span><span class="sxs-lookup"><span data-stu-id="16fb1-119">For EAPHost API related NAP information refer to the following topics.</span></span>

-   [<span data-ttu-id="16fb1-120">**\_tipo de atributo EAP \_**</span><span class="sxs-lookup"><span data-stu-id="16fb1-120">**EAP\_ATTRIBUTE\_TYPE**</span></span>](/windows/desktop/api/eaptypes/ne-eaptypes-eap_attribute_type)
-   [<span data-ttu-id="16fb1-121">**erro de EAP \_**</span><span class="sxs-lookup"><span data-stu-id="16fb1-121">**EAP\_ERROR**</span></span>](/windows/desktop/api/eaptypes/ns-eaptypes-eap_error)
-   [<span data-ttu-id="16fb1-122">Perguntas frequentes sobre suplicantes do EAPHost</span><span class="sxs-lookup"><span data-stu-id="16fb1-122">EAPHost Supplicant Frequently Asked Questions</span></span>](eaphost-supplicant-frequently-asked-questions.md)
-   [<span data-ttu-id="16fb1-123">**Propriedades do método EAP**</span><span class="sxs-lookup"><span data-stu-id="16fb1-123">**EAP Method Properties**</span></span>](eap-method-properties.md)
-   [<span data-ttu-id="16fb1-124">**EapHostPeerBeginSession**</span><span class="sxs-lookup"><span data-stu-id="16fb1-124">**EapHostPeerBeginSession**</span></span>](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession)
-   [<span data-ttu-id="16fb1-125">**Constantes de erro e informações relacionadas a EAP**</span><span class="sxs-lookup"><span data-stu-id="16fb1-125">**EAP Related Error and Information Constants**</span></span>](eap-related-error-and-information-constants.md)
-   [<span data-ttu-id="16fb1-126">**Estado de isolamento \_**</span><span class="sxs-lookup"><span data-stu-id="16fb1-126">**ISOLATION\_STATE**</span></span>](/windows/desktop/api/eaphostpeertypes/ne-eaphostpeertypes-isolation_state)
-   [<span data-ttu-id="16fb1-127">**NotificationHandler**</span><span class="sxs-lookup"><span data-stu-id="16fb1-127">**NotificationHandler**</span></span>](/previous-versions/windows/desktop/api)

## <a name="additional-resources"></a><span data-ttu-id="16fb1-128">Recursos adicionais</span><span class="sxs-lookup"><span data-stu-id="16fb1-128">Additional Resources</span></span>


-   <span data-ttu-id="16fb1-129">Para obter uma lista de recursos NAP, consulte [proteção de acesso à rede](https://go.microsoft.com/fwlink/p/?linkid=84107).</span><span class="sxs-lookup"><span data-stu-id="16fb1-129">For a list of NAP resources, see [Network Access Protection](https://go.microsoft.com/fwlink/p/?linkid=84107).</span></span>
-   <span data-ttu-id="16fb1-130">Para obter informações de declaração de integridade, consulte [mensagens de soh (proteção de acesso à rede)](https://go.microsoft.com/fwlink/p/?linkid=83918).</span><span class="sxs-lookup"><span data-stu-id="16fb1-130">For Statement of Health information, see [Network Access Protection (NAP) Statement of Health (SoH) Messages](https://go.microsoft.com/fwlink/p/?linkid=83918).</span></span>
-   <span data-ttu-id="16fb1-131">Para a página da Web e o blog do grupo de rede empresarial, consulte [NAP (proteção de acesso à rede)](https://go.microsoft.com/fwlink/p/?linkid=83845).</span><span class="sxs-lookup"><span data-stu-id="16fb1-131">For the Enterprise Networking Group webpage and blog, see [Network Access Protection (NAP)](https://go.microsoft.com/fwlink/p/?linkid=83845).</span></span>
-   <span data-ttu-id="16fb1-132">Para obter informações sobre a API NAP, consulte [proteção de acesso à rede](/windows/desktop/NAP/network-access-protection-start-page).</span><span class="sxs-lookup"><span data-stu-id="16fb1-132">For NAP API information, see [Network Access Protection](/windows/desktop/NAP/network-access-protection-start-page).</span></span>


## <a name="related-topics"></a><span data-ttu-id="16fb1-133">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="16fb1-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="16fb1-134">Configurando a interface do usuário do método EAP</span><span class="sxs-lookup"><span data-stu-id="16fb1-134">Configuring the EAP Method User Interface</span></span>](configuring-the-eap-method-user-interface.md)
</dt> <dt>

[<span data-ttu-id="16fb1-135">Habilitando Política de Grupo</span><span class="sxs-lookup"><span data-stu-id="16fb1-135">Enabling Group Policy</span></span>](enabling-group-policy.md)
</dt> <dt>

[<span data-ttu-id="16fb1-136">Implementando o suporte do In-Band NAP para métodos EAP</span><span class="sxs-lookup"><span data-stu-id="16fb1-136">Implementing In-Band NAP Support for EAP Methods</span></span>](enabling-in-band-nap-support.md)
</dt> <dt>

[<span data-ttu-id="16fb1-137">Transferindo dados entre os métodos suplicante e EAP</span><span class="sxs-lookup"><span data-stu-id="16fb1-137">Transferring Data Between the Supplicant and EAP Methods</span></span>](transferring-data-between-the-supplicant-and-eap-methods.md)
</dt> <dt>

[<span data-ttu-id="16fb1-138">Suplicantes do EAPHost</span><span class="sxs-lookup"><span data-stu-id="16fb1-138">EAPHost Supplicants</span></span>](eaphost-supplicants.md)
</dt> </dl>

 

 