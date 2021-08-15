---
title: Estruturas de método de par do EAPHost
description: Saiba mais sobre estruturas de API do método par do EAPHost, como EapCertificateCredential e EapSimCredential.
ms.assetid: 546ef715-8f51-4f5a-a569-8bf64d52de85
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56582c920536cabd294680df265d16ae51d8b4bd951f8efcdb988de677a2a2ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118498615"
---
# <a name="eaphost-peer-method-structures"></a>Estruturas de método de par do EAPHost

As estruturas de API do método par do EAPHost são as seguintes.



| Estrutura                                                              | Descrição                                                                                                                                                                                        |
|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**EapCertificateCredential**](/windows/desktop/api/eaptypes/ns-eaptypes-eapcertificatecredential)           | Contém informações sobre o certificado que o método EAP usa para autenticação.                                                                                                            |
| [**EapCredential**](/windows/desktop/api/eaptypes/ns-eaptypes-eapcredential)                                 | Contém informações sobre o tipo de credenciais e as credenciais apropriadas. Isso é passado como uma entrada para a API [**EapPeerGetConfigBlobAndUserBlob**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetconfigblobanduserblob) . |
| [**\_ \_ rotinas do método EAP peer \_**](/windows/desktop/api/eapmethodpeerapis/ns-eapmethodpeerapis-eap_peer_method_routines)        | Contém um conjunto de ponteiros de função para as APIs do método de par do EAPHost.                                                                                                                               |
| [**EapPeerMethodOutput**](/windows/win32/api/eapauthenticatoractiondefine/ns-eapauthenticatoractiondefine-eappeermethodoutput)                     | Contém as informações de ação retornadas por um método de par EAP.                                                                                                                                    |
| [**EapPeerMethodResult**](/windows/win32/api/eapmethodpeerapis/ns-eapmethodpeerapis-eappeermethodresult)                     | Contém dados de resultado gerados por um método EAP durante a autenticação.                                                                                                                             |
| [**EapSimCredential**](/windows/desktop/api/eaptypes/ns-eaptypes-eapsimcredential)                           | Contém informações sobre o SIM que é usado pelo método EAP para autenticação.                                                                                                              |
| [**EapUsernamePasswordCredential**](/windows/desktop/api/eaptypes/ns-eaptypes-eapusernamepasswordcredential) | Contém o nome de usuário e a senha que são usados pelo método EAP para autenticar o usuário.                                                                                                     |



 

 

 




