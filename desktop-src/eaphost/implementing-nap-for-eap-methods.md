---
title: Implementando o suporte nap para métodos EAP
description: Saiba como implementar o suporte a NAP para um suplicant de EAPHost. Consulte tópicos NAP relacionados ao EAPHost e veja recursos adicionais disponíveis.
ms.assetid: c25e4f03-759a-47a7-8b35-bbe669501c5c
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cff84c24aeb475b83146f2c56e9e139fd930eac27656349c594f05d91c1036fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118273310"
---
# <a name="implementing-nap-support-for-eap-methods"></a>Implementando o suporte nap para métodos EAP

Este tópico explica como implementar NAP para um suplicant de EAPHost. No Windows Vista e Windows Server 2008, um cliente de imposição nap (NAP EC) está disponível para [conexões autenticadas 802.1X.](/previous-versions/windows/embedded/ms890287(v=msdn.10))

## <a name="implementing-network-access-protection-nap"></a>Implementando NAP (Proteção de Acesso à Rede)

Para dar suporte a NAP, um suplente EAPHost implementa uma função de retorno de chamada correspondente ao protótipo de retorno de chamada [**NotificationHandler**](/previous-versions/windows/desktop/api) e deve fornecer um ponteiro para essa função de retorno de chamada ao chamar [**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession).

A função de retorno de chamada aceita dois parâmetros.

-   Um GUID que identifica exclusivamente a interface associada à autenticação.
-   Um ponteiro VOID para uma estrutura de dados opaca fornecida pelo suplicant.

EAPHost chamará a função de retorno de chamada fornecida pelo suplicant com o GUID de interface exclusivo e o ponteiro VOID quando o estado de quarentena do computador mudar. Quando O EAPHost chama a função de retorno de chamada fornecida pelo suplicant, o suplicant responde ao destruir a conexão de rede lógica identificada pelo ponteiro GUID/VOID da interface e inicia a autenticação novamente usando **EapHostPeerBeginSession**.

O EAPHost pode chamar a função de retorno de chamada fornecida pelo suplicant a qualquer momento: antes, durante uma autenticação ativa ou depois que a autenticação tiver sido concluída (depois que [**EapHostPeerEndSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerendsession) tiver sido chamado, mas não antes [**de EapHostPeerClearConnection**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerclearconnection) ter sido chamado). O suplílico sempre deve responder por meio da redução da conexão de rede lógica e da autenticação.

Se o suplente estiver desligando ou escolhendo não receber mais notificação de alterações de estado de isolamento, o suplente deverá chamar [**EapHostPeerClearConnection**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerclearconnection) e especificar o GUID de interface apropriado. Se o suplente quiser determinar o isolamento da conexão de rede lógica, o suplente poderá obter essas informações de **EapHostPeerMethodResult.isolationState** quando [**O EapHostPeerMethodResult**](/windows/win32/api/eaphostpeertypes/ns-eaphostpeertypes-eaphostpeermethodresult) for obtido de [**EapHostPeerGetResult**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetresult).

## <a name="eaphost-related-nap-information"></a>Informações nap relacionadas ao EAPHost

Para obter informações nap relacionadas à API do EAPHost, consulte os tópicos a seguir.

-   [**TIPO DE ATRIBUTO EAP \_ \_**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_attribute_type)
-   [**ERRO \_ DE EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_error)
-   [Perguntas frequentes sobre o supplicant EAPHost](eaphost-supplicant-frequently-asked-questions.md)
-   [**Propriedades do método EAP**](eap-method-properties.md)
-   [**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession)
-   [**Constantes de informações e erros relacionados ao EAP**](eap-related-error-and-information-constants.md)
-   [**ESTADO \_ DE ISOLAMENTO**](/windows/desktop/api/eaphostpeertypes/ne-eaphostpeertypes-isolation_state)
-   [**NotificationHandler**](/previous-versions/windows/desktop/api)

## <a name="additional-resources"></a>Recursos adicionais


-   Para ver uma lista de recursos NAP, consulte Proteção [de Acesso à Rede.](https://go.microsoft.com/fwlink/p/?linkid=84107)
-   Para obter informações sobre a instrução de saúde, consulte Mensagens da [Instrução soH (Proteção](https://go.microsoft.com/fwlink/p/?linkid=83918)de Acesso à Rede) .
-   Para a página Enterprise web e blog do Grupo de Rede, consulte [NAP (Proteção de Acesso à Rede).](https://go.microsoft.com/fwlink/p/?linkid=83845)
-   Para obter informações sobre a API NAP, consulte [Proteção de Acesso à Rede](/windows/desktop/NAP/network-access-protection-start-page).


## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Configurando o método EAP Interface do Usuário](configuring-the-eap-method-user-interface.md)
</dt> <dt>

[Habilitando Política de Grupo](enabling-group-policy.md)
</dt> <dt>

[Implementando In-Band nap para métodos EAP](enabling-in-band-nap-support.md)
</dt> <dt>

[Transferindo dados entre os métodos Supplicant e EAP](transferring-data-between-the-supplicant-and-eap-methods.md)
</dt> <dt>

[EAPHost Supplicants](eaphost-supplicants.md)
</dt> </dl>

 

 