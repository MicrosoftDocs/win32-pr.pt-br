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
# <a name="sso-eap-tls-pin-caching-behavior"></a>Comportamento do cache de PIN do SSO EAP-TLS

Este tópico fornece uma abordagem passo a passo para resolver as questões de retomada da sessão e a reautenticação de um usuário móvel em um ambiente EAP-TLS SSO.

## <a name="step-by-step-approach"></a>Abordagem passo a passo

A lista a seguir representa uma abordagem passo a passo para resolver as questões de retomada da sessão e a reautenticação de um usuário móvel em um ambiente SSO EAP-TLS.

-   Após a primeira autenticação bem-sucedida em um ambiente de SSO com EAP-TLS, o suplicante retém todas as informações relacionadas à credencial do usuário por padrão.
    > [!Note]  
    > Embora esteja sujeito à implementação específica do suplicante, é aconselhável que o suplicante Mantenha toda a estrutura da [**matriz de campo de \_ entrada de configuração \_ \_ EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) que o suplicante usou pela última vez na chamada [**EapHostPeerQueryUserBlobFromCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuserblobfromcredentialinputfields) para EAPHost.

     

-   Como o usuário primeiro faz roaming e a nova autenticação começa, o suplicante chama [**EapHostPeerQueryUserBlobFromCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuserblobfromcredentialinputfields) novamente com a mesma estrutura de [**matriz de \_ \_ \_ campo de entrada de configuração EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) ; o SUPLICAnte também deve passar no mesmo blob de usuário retido após a primeira autenticação bem-sucedida.
-   Em seguida, o EAPHost passa as informações no BLOB do usuário para o método EAP.
-   O método EAP, por sua vez, atualiza o BLOB do usuário com campos de credencial – o PIN, por exemplo, fornecido em *pEapConfigInputFieldArray*, e mantém os valores restantes – o certificado do servidor, por exemplo, como ele estava no blob do usuário original.
-   Depois de concluir essas etapas, o suplicante pode retomar a autenticação de forma normal chamando a função de tempo de execução [**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession) com esse blob de usuário.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Cenários do SSO EAPHost](why-eaphost-sso.md)
</dt> <dt>

[SSO e PLAP](understanding-sso-and-plap.md)
</dt> </dl>

 

 




