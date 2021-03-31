---
title: Implementando o suporte do In-Band NAP para métodos EAP
description: Pode ser habilitado para métodos de EAP do EAPHost que dão suporte à transmissão de TLVs (objetos de valor-tamanho-de-tipo).
ms.assetid: 298c89d9-7a6a-4280-9af9-77c7c00cab92
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa9eae9fc17e99b27f620fbab1ed42cbd4b73800
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/09/2020
ms.locfileid: "103642928"
---
# <a name="implementing-in-band-nap-support-for-eap-methods"></a>Implementando o suporte do In-Band NAP para métodos EAP

O suporte à NAP ( [proteção de acesso à rede](/windows/desktop/NAP/network-access-protection-start-page) ) em banda para um método EAP pode ser habilitado para métodos de EAP do EAPHost que dão suporte à transmissão de TLVs (objetos de valor-comprimento). Quando o suporte a NAP em banda está habilitado, os pacotes NAP são transportados dentro de pacotes de método EAP.

Por outro lado, quando o suporte a NAP fora de banda está habilitado, a troca de soh ( [instrução NAP de integridade](https://go.microsoft.com/fwlink/p/?linkid=83917) ) ocorre por meio de meios diferentes dos pacotes de método EAP.

Todos os TLVs são específicos do fornecedor.

## <a name="implementing-nap-support-on-eap-peer-methods"></a>Implementando o suporte a NAP em métodos de pares EAP

A implementação do método EAP peer recebe um TLV que contém o TLV de solicitação soh ( [declaração de integridade](https://go.microsoft.com/fwlink/p/?linkid=83917) ) de um servidor EAP.

Em seguida, a implementação do método EAP peer passa o TLV que contém o TLV de solicitação SoH para EAPHost da seguinte maneira.

-   A implementação do método EAP peer retorna o código de ação [**EapPeerMethodResponseActionRespond**](/windows/win32/api/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) para EAPHost no retorno de [**EapPeerProcessRequestPacket**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerprocessrequestpacket).
-   O EAPHost chama [**EapPeerGetResponseAttributes**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresponseattributes) da implementação do método EAP peer. Os atributos são passados no processo.
-   A implementação do método EAP peer retorna o TLV que contém o TLV de solicitação SoH em [**EapPeerGetResponseAttributes**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresponseattributes). Os atributos são recebidos no processo.

A implementação do método EAP peer recebe um TLV que contém um TLV SoH do EAPHost da seguinte maneira.

-   O EAPHost chama [**EapPeerSetResponseAttributes**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetresponseattributes) da implementação do método EAP peer. **EapPeerSetResponseAttributes** contém um TLV que hospeda um TLV soh.
-   A implementação do método EAP peer envia o TLV SoH para o servidor EAP.
-   A implementação do método EAP peer recebe um TLV que contém um TLV de resposta SoH do servidor EAP.

A implementação do método EAP peer passa o TLV que contém o TLV de resposta SoH para EAPHost da seguinte maneira.

-   A implementação do método EAP peer retorna o código de ação **EapPeerMethodResponseActionRespond** para EAPHost no retorno de [**EapPeerProcessRequestPacket**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerprocessrequestpacket).
-   O EAPHost chama [**EapPeerGetResponseAttributes**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresponseattributes) das implementações do método EAP peer. A estrutura de [**\_ atributos EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attributes) é passada no processo.
-   A implementação do método EAP peer retorna o TLV que contém o TLV de resposta SoH em [**EapPeerSetResponseAttributes**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetresponseattributes).

> [!Note]  
> O membro **eapType** da estrutura [**de \_ atributo do EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attribute) sempre será definido como **eatEAPTLV** e o **membro de nome da série** apontará para o primeiro byte do TLV que contém o TLV de resposta soh.

 

### <a name="implementing-nap-support-on-eap-server-methods"></a>Implementando o suporte a NAP em métodos de servidor EAP

A implementação do método de servidor EAP constrói um TLV que contém um TLV de solicitação SoH. A implementação do método de servidor EAP envia esse TLV contendo o TLV de solicitação SoH para o par EAP. A implementação do método de servidor EAP recebe o TLV do ponto EAP.

A implementação do método de servidor EAP passa o TLV que contém um TLV SoH para o EAPHost da seguinte maneira.

-   A implementação do método do servidor EAP retorna a **resposta do autenticador do método EAP do código de ação \_ \_ \_ \_ responderá** a EAPHost no retorno de [**EapMethodAuthenticatorReceivePacket**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorreceivepacket).
-   O EAPHost chama [**EapMethodAuthenticatorGetAttributes**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorgetattributes) da implementação do método de servidor EAP.
-   A implementação do método de servidor EAP retorna o TLV que contém o TLV SoH em [**EapMethodAuthenticatorGetAttributes**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorgetattributes).

A implementação do método de servidor EAP recebe um TLV que contém um TLV de resposta SoH do EAPHost da seguinte maneira.

-   O EAPHost chama [**EapMethodAuthenticatorSetAttributes**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorsetattributes) da implementação do método de servidor EAP.
-   O TLV que contém o TLV de resposta SoH é retornado em [ **EapMethodAuthenticatorSetAttributes**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorsetattributes)
-   A implementação do método de servidor EAP envia o TLV que contém o TLV de resposta SoH.

> [!Note]  
> O membro **eapType** da estrutura [**de \_ atributo do EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attribute) sempre será definido como **eatEAPTLV** e o **membro de nome da série** apontará para o primeiro byte do TLV que contém o TLV de resposta soh.

 

### <a name="messages"></a>Mensagens

O TLV de SoH EAP é usado para encapsular o protocolo SoH para transmissão por meio de um método EAP. Todos os TLVs de SoH do EAP têm a mesma estrutura, diferente somente na ID da mensagem e na parte de dados da mensagem.

Para obter mais informações, consulte [mensagens de soh (proteção de acesso à rede)](https://go.microsoft.com/fwlink/p/?linkid=83918).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Configurando a interface do usuário do método EAP](configuring-the-eap-method-user-interface.md)
</dt> <dt>

[Habilitando Política de Grupo](enabling-group-policy.md)
</dt> <dt>

[Implementando o suporte a NAP para métodos EAP](implementing-nap-for-eap-methods.md)
</dt> <dt>

[Transferindo dados entre os métodos suplicante e EAP](transferring-data-between-the-supplicant-and-eap-methods.md)
</dt> <dt>

[Suplicantes do EAPHost](eaphost-supplicants.md)
</dt> </dl>

 

 