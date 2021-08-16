---
title: Habilitando Política de Grupo
description: Saiba como configurar o suplicante habilitando a política de grupo. Consulte Considerações para suplicantes e exibir recursos adicionais disponíveis.
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

Este tópico explica como configurar o suplicante habilitando a política de grupo. Os suplicantes do EAPHost podem participar da diretiva de grupo para permitir que um administrador de rede configure centralmente seus computadores de rede.

O método preciso e o mecanismo pelo qual o suplicante escolhe participar na diretiva de grupo é a critério do suplicante. Exemplos de mecanismos para participação na diretiva de grupo incluem extensões do lado do cliente/servidor, modelo administrativo e assim por diante.

## <a name="considerations-when-enabling-group-policy"></a>Considerações ao habilitar Política de Grupo

Essas são as considerações para suplicantes em relação à diretiva de grupo e ao EAP.

1.  A configuração de EAP sempre deve ser armazenada como XML sempre que possível e não no formato binário. A política de grupo pode ser aplicada a qualquer computador no domínio, e a configuração do método EAP e os dados do usuário não têm garantia de serem portáteis entre as arquiteturas de processador de 32 bits e 64 bits. O XML resolve os problemas de limite da arquitetura do processador, pois o suplicante converte localmente o XML independente da arquitetura do processador na representação binária da configuração no momento da autenticação.

    Para obter mais informações, consulte estes tópicos.

    -   [Perguntas frequentes gerais](general-frequently-asked-questions.md)
    -   [Perguntas frequentes sobre o método EAP](eap-method-frequently-asked-questions.md).
    -   [**EapHostPeerConfigXml2Blob**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerconfigxml2blob)
    -   [**EapHostPeerCredentialsXml2Blob**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeercredentialsxml2blob)

2.  Se uma extensão do lado do servidor da diretiva de grupo for usada, a extensão chamará [**EapHostPeerGetMethods**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeergetmethods) normalmente para determinar os métodos disponíveis e gerar a configuração de EAP apropriada para essa política. Em seguida, a política é enviada para os clientes de rede apropriados onde a política é aplicada.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Configurando a interface do usuário do método EAP](configuring-the-eap-method-user-interface.md)
</dt> <dt>

[Implementando o suporte do In-Band NAP para métodos EAP](enabling-in-band-nap-support.md)
</dt> <dt>

[Implementando o suporte a NAP para métodos EAP](implementing-nap-for-eap-methods.md)
</dt> <dt>

[Transferindo dados entre os métodos suplicante e EAP](transferring-data-between-the-supplicant-and-eap-methods.md)
</dt> <dt>

[Suplicantes do EAPHost](eaphost-supplicants.md)
</dt> </dl>

 

 




