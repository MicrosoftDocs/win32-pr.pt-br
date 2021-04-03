---
title: Comportamento do cache de PIN do SSO EAP-TLS
description: Fornece uma abordagem passo a passo para resolver as questões de retomada da sessão e a reautenticação de um usuário móvel em um ambiente EAP-TLS SSO.
ms.assetid: aeded6c9-315d-4115-9750-485f017dd8dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b7c4e3058598f98327570fbcd0347cfb84e5825
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2019
ms.locfileid: "104084283"
---
# <a name="sso-eap-tls-pin-caching-behavior"></a><span data-ttu-id="889b9-103">Comportamento do cache de PIN do SSO EAP-TLS</span><span class="sxs-lookup"><span data-stu-id="889b9-103">SSO EAP-TLS PIN Caching Behavior</span></span>

<span data-ttu-id="889b9-104">Este tópico fornece uma abordagem passo a passo para resolver as questões de retomada da sessão e a reautenticação de um usuário móvel em um ambiente EAP-TLS SSO.</span><span class="sxs-lookup"><span data-stu-id="889b9-104">This topic provides a step-by-step approach for resolving matters of session resumption and re-authentication of a roaming user in an SSO EAP-TLS environment.</span></span>

## <a name="step-by-step-approach"></a><span data-ttu-id="889b9-105">Abordagem passo a passo</span><span class="sxs-lookup"><span data-stu-id="889b9-105">Step-By-Step Approach</span></span>

<span data-ttu-id="889b9-106">A lista a seguir representa uma abordagem passo a passo para resolver as questões de retomada da sessão e a reautenticação de um usuário móvel em um ambiente SSO EAP-TLS.</span><span class="sxs-lookup"><span data-stu-id="889b9-106">The following list represents a step-by-step approach for resolving matters of session resumption and re-authentication of a roaming user in an SSO EAP-TLS environment.</span></span>

-   <span data-ttu-id="889b9-107">Após a primeira autenticação bem-sucedida em um ambiente de SSO com EAP-TLS, o suplicante retém todas as informações relacionadas à credencial do usuário por padrão.</span><span class="sxs-lookup"><span data-stu-id="889b9-107">After the first successful authentication in an SSO environment with EAP-TLS, the supplicant retains all user credential related information by default.</span></span>
    > [!Note]  
    > <span data-ttu-id="889b9-108">Embora esteja sujeito à implementação específica do suplicante, é aconselhável que o suplicante Mantenha toda a estrutura da [**matriz de campo de \_ entrada de configuração \_ \_ EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) que o suplicante usou pela última vez na chamada [**EapHostPeerQueryUserBlobFromCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuserblobfromcredentialinputfields) para EAPHost.</span><span class="sxs-lookup"><span data-stu-id="889b9-108">Although subject to the particular supplicant implementation, it's advisable for the supplicant to retain the entire [**EAP\_CONFIG\_INPUT\_FIELD ARRAY**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) structure that the supplicant last used in the [**EapHostPeerQueryUserBlobFromCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuserblobfromcredentialinputfields) call to EAPHost.</span></span>

     

-   <span data-ttu-id="889b9-109">Como o usuário primeiro faz roaming e a nova autenticação começa, o suplicante chama [**EapHostPeerQueryUserBlobFromCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuserblobfromcredentialinputfields) novamente com a mesma estrutura de [**matriz de \_ \_ \_ campo de entrada de configuração EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) ; o SUPLICAnte também deve passar no mesmo blob de usuário retido após a primeira autenticação bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="889b9-109">As the user first roams and the re-authentication begins, the supplicant calls [**EapHostPeerQueryUserBlobFromCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuserblobfromcredentialinputfields) again with the same [**EAP\_CONFIG\_INPUT\_FIELD ARRAY**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) structure; the supplicant must also pass in the same user BLOB retained after the first successful authentication.</span></span>
-   <span data-ttu-id="889b9-110">Em seguida, o EAPHost passa as informações no BLOB do usuário para o método EAP.</span><span class="sxs-lookup"><span data-stu-id="889b9-110">EAPHost then passes the information in the user BLOB to the EAP method.</span></span>
-   <span data-ttu-id="889b9-111">O método EAP, por sua vez, atualiza o BLOB do usuário com campos de credencial – o PIN, por exemplo, fornecido em *pEapConfigInputFieldArray*, e mantém os valores restantes – o certificado do servidor, por exemplo, como ele estava no blob do usuário original.</span><span class="sxs-lookup"><span data-stu-id="889b9-111">The EAP method in turn updates the user BLOB with credential fields - the PIN for example - provided in *pEapConfigInputFieldArray*, and keeps the remaining values - the server certificate for example - as it was in the original user BLOB.</span></span>
-   <span data-ttu-id="889b9-112">Depois de concluir essas etapas, o suplicante pode retomar a autenticação de forma normal chamando a função de tempo de execução [**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession) com esse blob de usuário.</span><span class="sxs-lookup"><span data-stu-id="889b9-112">After completing these steps, the supplicant can resume authentication in a normal way by calling the [**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession) run-time function with this user BLOB.</span></span>

## <a name="related-topics"></a><span data-ttu-id="889b9-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="889b9-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="889b9-114">Cenários do SSO EAPHost</span><span class="sxs-lookup"><span data-stu-id="889b9-114">SSO EAPHost Scenarios</span></span>](why-eaphost-sso.md)
</dt> <dt>

[<span data-ttu-id="889b9-115">SSO e PLAP</span><span class="sxs-lookup"><span data-stu-id="889b9-115">SSO and PLAP</span></span>](understanding-sso-and-plap.md)
</dt> </dl>

 

 




