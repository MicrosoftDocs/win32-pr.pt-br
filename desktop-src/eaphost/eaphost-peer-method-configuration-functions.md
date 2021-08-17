---
title: Funções de configuração do método par EAPHost
description: Saiba mais sobre as funções de configuração do método par EAPHost. Confira uma lista das funções de configuração e veja recursos adicionais disponíveis.
ms.assetid: ba5c90b2-5185-4810-84a2-d08e62e8105c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 355784647be6c6e13d4110303d544670e80ce09e7f9f99be02b662205e8ead82
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118785191"
---
# <a name="eaphost-peer-method-configuration-functions"></a>Funções de configuração do método par EAPHost

As funções de configuração da API de Método Par de EAP são as a seguir.



| Função                                                                                                  | Descrição                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**EapPeerConfigBlob2Xml**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerconfigblob2xml)                                                    | Converte o blob de configuração em XML.                                                                                                                                                                                                                          |
| [**EapPeerConfigXml2Blob**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerconfigxml2blob)                                                    | Converte XML no blob de configuração.                                                                                                                                                                                                                        |
| [**EapPeerCredentialsXml2Blob**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeercredentialsxml2blob)                                          | Converte credenciais XML em um BLOB.                                                                                                                                                                                                                            |
| [**EapPeerFreeErrorMemory**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerfreeerrormemory)                                                  | Libera toda a memória específica de erro de EAP retornada por APIs de par EapHost.                                                                                                                                                                                               |
| [**EapPeerFreeMemory**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerfreememory)                                                            | Libera toda a memória alocada pelos parâmetros OUT do método EAP.                                                                                                                                                                                                      |
| [**EapPeerInvokeConfigUI**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinvokeconfigui)                                                    | Gera a caixa de diálogo de interface do usuário de configuração de conexão específica do método EAP no cliente.                                                                                                                                                                   |
| [**EapPeerInvokeIdentityUI**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinvokeidentityui)                                                | Gera uma caixa de diálogo de interface do usuário interativa personalizada para obter informações de identidade do usuário para o método EAP no cliente.                                                                                                                                          |
| [**EapPeerInvokeInteractiveUI**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinvokeinteractiveui)                                          | Gera uma caixa de diálogo de interface do usuário interativa personalizada para o método EAP no cliente.                                                                                                                                                                              |
| [**EapPeerQueryCredentialInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerquerycredentialinputfields)                            | Define a implementação de uma função específica do método EAP que obtém os campos de entrada de credencial de SSO (logout único) do EAP para esse método EAP                                                                                                              |
| [**EapPeerQueryInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryinteractiveuiinputfields)                      | Define a implementação de uma função flexível de EAP que obtém os campos de entrada para componentes interativos da interface do usuário a ser aumentada no suplicant.                                                                                                     |
| [**EapPeerQueryUIBlobFromInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryuiblobfrominteractiveuiinputfields)  | Converte informações do usuário em um BLOB de usuário que pode ser consumido por funções de tempo de executar EAPHost.                                                                                                                                                                   |
| [**EapPeerQueryUserBlobFromCredentialInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryuserblobfromcredentialinputfields) | Define a implementação de uma função específica do método EAP que gera um blob de credenciais de usuário de EAP de uma estrutura [**EAP \_ CONFIG \_ INPUT FIELD \_ \_ ARRAY**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) que contém dados de credencial fornecidos por um usuário flexível. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Funções de Run-Time EAPHost Peer](eaphost-peer-method-run-time-functions.md)
</dt> </dl>

 

 




