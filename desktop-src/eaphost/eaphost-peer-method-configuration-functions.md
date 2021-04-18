---
title: Funções de configuração do método de emparelhamento EAPHost
description: Saiba mais sobre as funções de configuração do método de emparelhamento do EAPHost. Consulte uma lista das funções de configuração e exiba recursos adicionais disponíveis.
ms.assetid: ba5c90b2-5185-4810-84a2-d08e62e8105c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3081f8a54482c48c7c506a25bfaf7f18cf3193ff
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "105797513"
---
# <a name="eaphost-peer-method-configuration-functions"></a>Funções de configuração do método de emparelhamento EAPHost

As funções de configuração da API do método peer do EAP são as seguintes.



| Função                                                                                                  | Descrição                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**EapPeerConfigBlob2Xml**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerconfigblob2xml)                                                    | Converte o blob de configuração em XML.                                                                                                                                                                                                                          |
| [**EapPeerConfigXml2Blob**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerconfigxml2blob)                                                    | Converte o XML no blob de configuração.                                                                                                                                                                                                                        |
| [**EapPeerCredentialsXml2Blob**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeercredentialsxml2blob)                                          | Converte as credenciais XML em um BLOB.                                                                                                                                                                                                                            |
| [**EapPeerFreeErrorMemory**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerfreeerrormemory)                                                  | Libera toda a memória específica de erro EAP retornada pelas APIs de mesmo nível do EapHost.                                                                                                                                                                                               |
| [**EapPeerFreeMemory**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerfreememory)                                                            | Libera toda a memória alocada por parâmetros de saída do método EAP.                                                                                                                                                                                                      |
| [**EapPeerInvokeConfigUI**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinvokeconfigui)                                                    | Gera a caixa de diálogo da interface de usuário de configuração de conexão específica do método EAP no cliente.                                                                                                                                                                   |
| [**EapPeerInvokeIdentityUI**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinvokeidentityui)                                                | Gera uma caixa de diálogo personalizada da interface do usuário interativa para obter informações de identidade do usuário para o método EAP no cliente.                                                                                                                                          |
| [**EapPeerInvokeInteractiveUI**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinvokeinteractiveui)                                          | Gera uma caixa de diálogo de interface de usuário interativa personalizada para o método EAP no cliente.                                                                                                                                                                              |
| [**EapPeerQueryCredentialInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerquerycredentialinputfields)                            | Define a implementação de uma função específica do método EAP que obtém os campos de entrada de credencial de SSO (logon único) EAP para esse método EAP                                                                                                              |
| [**EapPeerQueryInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryinteractiveuiinputfields)                      | Define a implementação de uma função de suplicante EAP que obtém os campos de entrada para componentes interativos da interface do usuário a serem gerados no suplicante.                                                                                                     |
| [**EapPeerQueryUIBlobFromInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryuiblobfrominteractiveuiinputfields)  | Converte as informações do usuário em um BLOB do usuário que pode ser consumido por funções de tempo de execução do EAPHost.                                                                                                                                                                   |
| [**EapPeerQueryUserBlobFromCredentialInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryuserblobfromcredentialinputfields) | Define a implementação de uma função específica de método EAP que gera um blob de credencial de usuário EAP de uma estrutura de [**matriz de campo de \_ entrada de configuração \_ \_ \_ EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) que contém dados de credenciais fornecidos por um usuário suplicante. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Funções de Run-Time do método par do EAPHost](eaphost-peer-method-run-time-functions.md)
</dt> </dl>

 

 




