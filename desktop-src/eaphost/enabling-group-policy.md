---
title: Habilitando Política de Grupo
description: Saiba como configurar o suplente habilitando a política de grupo. Confira considerações sobre os supplicantes e veja recursos adicionais disponíveis.
ms.assetid: ac04b83b-1322-41d4-85e0-93687f10a7f6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b2a388bf8dba155e42d5542c1379f7b0cc34d44579b92809387541d7e20cf65
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118784995"
---
# <a name="enabling-group-policy"></a>Habilitando Política de Grupo

Este tópico explica como configurar o suplente habilitando a política de grupo. Os suplicantes de EAPHost podem participar da política de grupo para permitir que um administrador de rede configure centralmente seus máquinas de rede.

O método e o mecanismo precisos pelo qual o suplente opta por participar da política de grupo está a critério do suplente. Exemplos de mecanismos para a participação da política de grupo incluem extensões do lado do cliente/servidor, modelo administrativo e assim por diante.

## <a name="considerations-when-enabling-group-policy"></a>Considerações ao habil Política de Grupo

Estas são as considerações para os supplicantes em relação à política de grupo e à EAP.

1.  A configuração de EAP sempre deve ser armazenada como XML sempre que possível e não no formato binário. A política de grupo pode ser aplicada a qualquer computador no domínio, e não há garantia de que a configuração do método EAP e os dados do usuário sejam portáteis entre arquiteturas de processador de 32 bits e 64 bits. O XML resolve os problemas de limite da arquitetura do processador à medida que o suplente converte localmente o XML independente da arquitetura do processador para a representação binária da configuração no momento da autenticação.

    Para obter mais informações, consulte estes tópicos.

    -   [Perguntas frequentes gerais](general-frequently-asked-questions.md)
    -   [Perguntas frequentes sobre o método EAP.](eap-method-frequently-asked-questions.md)
    -   [**EapHostPeerConfigXml2Blob**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerconfigxml2blob)
    -   [**EapHostPeerCredentialsXml2Blob**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeercredentialsxml2blob)

2.  Se uma extensão do lado do servidor de política de grupo for usada, a extensão chamará [**EapHostPeerGetMethods**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeergetmethods) normalmente para determinar os métodos disponíveis e gerar a configuração de EAP apropriada para essa política. Em seguida, a política é esvasada para os clientes de rede apropriados em que a política é aplicada.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Configurando o método EAP Interface do Usuário](configuring-the-eap-method-user-interface.md)
</dt> <dt>

[Implementando In-Band nap para métodos EAP](enabling-in-band-nap-support.md)
</dt> <dt>

[Implementando o suporte nap para métodos EAP](implementing-nap-for-eap-methods.md)
</dt> <dt>

[Transferindo dados entre os métodos Supplicant e EAP](transferring-data-between-the-supplicant-and-eap-methods.md)
</dt> <dt>

[EAPHost Supplicants](eaphost-supplicants.md)
</dt> </dl>

 

 




