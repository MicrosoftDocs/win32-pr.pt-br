---
title: Comportamento de alteração de senha de SSO
description: Fornece uma abordagem passo a passo para resolver o comportamento de alteração de senha de SSO.
ms.assetid: c52ffeb8-ecee-4398-a7df-388b523c737c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 005fe5191b3bdccf2bb1643be50817a3b0405336
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2019
ms.locfileid: "105749417"
---
# <a name="sso-password-change-behavior"></a><span data-ttu-id="6f620-103">Comportamento de alteração de senha de SSO</span><span class="sxs-lookup"><span data-stu-id="6f620-103">SSO Password Change Behavior</span></span>

<span data-ttu-id="6f620-104">Este tópico fornece uma abordagem passo a passo para resolver o comportamento de alteração de senha de SSO.</span><span class="sxs-lookup"><span data-stu-id="6f620-104">This topic provides a step-by-step approach for resolving SSO password change behavior.</span></span>

## <a name="step-by-step-approach"></a><span data-ttu-id="6f620-105">Abordagem passo a passo</span><span class="sxs-lookup"><span data-stu-id="6f620-105">Step-By-Step Approach</span></span>

<span data-ttu-id="6f620-106">A lista a seguir representa uma abordagem passo a passo para resolver o comportamento de alteração de senha de SSO.</span><span class="sxs-lookup"><span data-stu-id="6f620-106">The following list represents a step-by-step approach for resolving SSO password change behavior.</span></span>

-   <span data-ttu-id="6f620-107">Depois que o método EAP é notificado sobre uma alteração de senha, o método notifica o EAPHost; O EAPHost, por sua vez, notifica o suplicante retornando o código de ação, [EapHostPeerResponseInvokeUI](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction).</span><span class="sxs-lookup"><span data-stu-id="6f620-107">Once the EAP method is notified about a password change, the method notifies EAPHost; EAPHost in turn notifies the supplicant by returning the action code, [EapHostPeerResponseInvokeUI](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction).</span></span>
-   <span data-ttu-id="6f620-108">Depois de receber o código de ação [EapHostPeerResponseInvokeUI](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction) do EAPHost, o suplicante Obtém o contexto da interface do usuário do método EAP chamando a função [**EapHostPeerGetUIContext**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetuicontext) ; O EAPHost Obtém o contexto da interface do usuário do método EAP chamando a função de método correspondente</span><span class="sxs-lookup"><span data-stu-id="6f620-108">After receiving the [EapHostPeerResponseInvokeUI](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction) action code from EAPHost, the supplicant obtains the UI context from the EAP method by calling the [**EapHostPeerGetUIContext**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetuicontext) function; EAPHost then obtains the UI context from the EAP method by calling the corresponding method function</span></span>
-   <span data-ttu-id="6f620-109">O suplicante passa o contexto da interface do usuário para o processo de interface do usuário (usando alguma forma de comunicação entre processos).</span><span class="sxs-lookup"><span data-stu-id="6f620-109">The supplicant passes the UI context to the UI process (using some form of inter-process communication).</span></span>
-   <span data-ttu-id="6f620-110">O processo da interface do usuário chama [**EapHostPeerQueryInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryinteractiveuiinputfields) no EAPHost.</span><span class="sxs-lookup"><span data-stu-id="6f620-110">The UI process calls [**EapHostPeerQueryInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryinteractiveuiinputfields) on EAPHost.</span></span>
-   <span data-ttu-id="6f620-111">O EAPHost coleta o contexto da interface do usuário chamando [**EapPeerQueryInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryinteractiveuiinputfields) no método EAP.</span><span class="sxs-lookup"><span data-stu-id="6f620-111">EAPHost collects the UI context by calling [**EapPeerQueryInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryinteractiveuiinputfields) on the EAP method.</span></span>
-   <span data-ttu-id="6f620-112">O método EAP fornece todas as informações de contexto da interface do usuário na estrutura de [**\_ \_ \_ dados da interface do usuário interativa do EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) , em que *DwDataType* é definido como *EapCredExpiryReq* e *PbUiData* aponta para uma estrutura do tipo req. do [**EAP de \_ credenciais \_**](eap-cred-req.md).</span><span class="sxs-lookup"><span data-stu-id="6f620-112">The EAP method provides any necessary UI context information in the [**EAP\_INTERACTIVE\_UI\_DATA**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) structure, where *dwDataType* is set to *EapCredExpiryReq* and *pbUiData* points to a structure of type [**EAP\_CRED\_REQ**](eap-cred-req.md).</span></span>
-   <span data-ttu-id="6f620-113">Ao preencher a estrutura de [**\_ \_ \_ dados da interface do usuário interativa do EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) , esse método EAP só preencherá o parâmetro *curCreds* e não definirá o sinalizador [**\_ \_ \_ \_ \_ \_ somente leitura das propriedades do campo de entrada da interface de usuário do EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_data) na estrutura de **\_ \_ \_ \_ dados do campo de entrada de configuração EAP** .</span><span class="sxs-lookup"><span data-stu-id="6f620-113">While populating the [**EAP\_INTERACTIVE\_UI\_DATA**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) structure, this EAP method will only fill in the *curCreds* parameter, and not set the [**EAP\_UI\_INPUT\_FIELD\_PROPS\_READ\_ONLY**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_data) flag in the **EAP\_CONFIG\_INPUT\_FIELD\_DATA** structure.</span></span>
    > [!Note]  
    > <span data-ttu-id="6f620-114">O [**sinalizador \_ \_ \_ \_ \_ \_ somente leitura das propriedades do campo de entrada da interface do usuário do EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_data) é para os campos de membro que precisam ser alterados.</span><span class="sxs-lookup"><span data-stu-id="6f620-114">The [**EAP\_UI\_INPUT\_FIELD\_PROPS\_READ\_ONLY**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_data) flag is for member field(s) which need to be changed.</span></span>

     

-   <span data-ttu-id="6f620-115">Depois de coletar o contexto de interface do usuário informtion, o processo da interface do usuário renderiza uma interface de usuário para coletar informações de alteração de senha.</span><span class="sxs-lookup"><span data-stu-id="6f620-115">Having collected the UI context informtion, the UI process renders a UI to collect change password information from the user.</span></span> <span data-ttu-id="6f620-116">Essas informações são populadas no parâmetro *NewCreds* da estrutura de [**\_ \_ \_ req expiração de credenciais EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_cred_expiry_req) .</span><span class="sxs-lookup"><span data-stu-id="6f620-116">This information is populated in the *NewCreds* parameter of the [**EAP\_CRED\_EXPIRY\_REQ**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_cred_expiry_req) structure.</span></span>
-   <span data-ttu-id="6f620-117">O processo da interface do usuário passa a estrutura [**\_ \_ resp de credenciais de EAP**](eap-cred-resp.md) de volta para o EAPHost por meio de [**EapHostPeerQueryUIBlobFromInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuiblobfrominteractiveuiinputfields).</span><span class="sxs-lookup"><span data-stu-id="6f620-117">The UI process passes the [**EAP\_CRED\_RESP**](eap-cred-resp.md) structure back to EAPHost via [**EapHostPeerQueryUIBlobFromInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuiblobfrominteractiveuiinputfields).</span></span>
-   <span data-ttu-id="6f620-118">O processo de IU passa esse BLOB do usuário para o suplicante, e o suplicante continua com as funções de tempo de execução do EAPHost como de costume.</span><span class="sxs-lookup"><span data-stu-id="6f620-118">The UI process passes this user BLOB to the supplicant, and the supplicant continues with EAPHost run-time functions as usual.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6f620-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6f620-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6f620-120">Cenários do SSO EAPHost</span><span class="sxs-lookup"><span data-stu-id="6f620-120">SSO EAPHost Scenarios</span></span>](why-eaphost-sso.md)
</dt> <dt>

[<span data-ttu-id="6f620-121">SSO e PLAP</span><span class="sxs-lookup"><span data-stu-id="6f620-121">SSO and PLAP</span></span>](understanding-sso-and-plap.md)
</dt> </dl>

 

 




