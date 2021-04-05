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
# <a name="implementing-nap-support-for-eap-methods"></a>Implementando o suporte a NAP para métodos EAP

Este tópico explica como implementar a NAP para um suplicante do EAPHost. No Windows Vista e no Windows Server 2008, um cliente de imposição de NAP (NAP EC) está disponível para conexões autenticadas [802.1 x](/previous-versions/windows/embedded/ms890287(v=msdn.10)) .

## <a name="implementing-network-access-protection-nap"></a>Implementando a NAP (proteção de acesso à rede)

Para oferecer suporte a NAP, um suplicante EAPHost implementa uma função de retorno de chamada que corresponde ao protótipo de retorno de chamada [**NotificationHandler**](/previous-versions/windows/desktop/api) e deve fornecer um ponteiro para essa função de retorno de chamada ao chamar [**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession).

A função de retorno de chamada usa dois parâmetros.

-   Um GUID que identifica exclusivamente a interface associada à autenticação.
-   Um ponteiro VOID para uma estrutura de dados opaca que é fornecida pelo suplicante.

O EAPHost chamará a função de retorno de chamada fornecida pelo suplicante com o GUID de interface exclusivo e o ponteiro VOID quando o estado de quarentena da máquina for alterado. Quando o EAPHost chama a função de retorno de chamada fornecida pelo suplicante, o suplicante responde subdividindo a conexão de rede lógica identificada pelo ponteiro da interface GUID/VOID e começa a autenticação novamente usando **EapHostPeerBeginSession**.

O EAPHost pode chamar a função de retorno de chamada fornecida pelo suplicante a qualquer momento: antes, durante uma autenticação ativa ou após a conclusão da autenticação (após [**EapHostPeerEndSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerendsession) ter sido chamado, mas não antes de [**EapHostPeerClearConnection**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerclearconnection) ser chamado). O suplicante deve sempre responder subdividindo a conexão de rede lógica e autenticando novamente.

Se o suplicante estiver sendo desligado ou optar por não receber mais notificação de alterações de estado de isolamento, o suplicante deverá chamar [**EapHostPeerClearConnection**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerclearconnection) e especificar o GUID de interface apropriado. Se o suplicante quiser determinar o isolamento da conexão de rede lógica, o suplicante poderá obter essas informações de **EapHostPeerMethodResult. isolable** quando o [**EapHostPeerMethodResult**](/windows/win32/api/eaphostpeertypes/ns-eaphostpeertypes-eaphostpeermethodresult) for obtido de [**EapHostPeerGetResult**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetresult).

## <a name="eaphost-related-nap-information"></a>Informações de NAP relacionadas ao EAPHost

Para obter informações de NAP relacionadas à API EAPHost, consulte os tópicos a seguir.

-   [**\_tipo de atributo EAP \_**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_attribute_type)
-   [**erro de EAP \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_error)
-   [Perguntas frequentes sobre suplicantes do EAPHost](eaphost-supplicant-frequently-asked-questions.md)
-   [**Propriedades do método EAP**](eap-method-properties.md)
-   [**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession)
-   [**Constantes de erro e informações relacionadas a EAP**](eap-related-error-and-information-constants.md)
-   [**Estado de isolamento \_**](/windows/desktop/api/eaphostpeertypes/ne-eaphostpeertypes-isolation_state)
-   [**NotificationHandler**](/previous-versions/windows/desktop/api)

## <a name="additional-resources"></a>Recursos adicionais


-   Para obter uma lista de recursos NAP, consulte [proteção de acesso à rede](https://go.microsoft.com/fwlink/p/?linkid=84107).
-   Para obter informações de declaração de integridade, consulte [mensagens de soh (proteção de acesso à rede)](https://go.microsoft.com/fwlink/p/?linkid=83918).
-   Para a página da Web e o blog do grupo de rede empresarial, consulte [NAP (proteção de acesso à rede)](https://go.microsoft.com/fwlink/p/?linkid=83845).
-   Para obter informações sobre a API NAP, consulte [proteção de acesso à rede](/windows/desktop/NAP/network-access-protection-start-page).


## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Configurando a interface do usuário do método EAP](configuring-the-eap-method-user-interface.md)
</dt> <dt>

[Habilitando Política de Grupo](enabling-group-policy.md)
</dt> <dt>

[Implementando o suporte do In-Band NAP para métodos EAP](enabling-in-band-nap-support.md)
</dt> <dt>

[Transferindo dados entre os métodos suplicante e EAP](transferring-data-between-the-supplicant-and-eap-methods.md)
</dt> <dt>

[Suplicantes do EAPHost](eaphost-supplicants.md)
</dt> </dl>

 

 