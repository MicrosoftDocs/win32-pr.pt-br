---
title: Implementando In-Band nap para métodos EAP
description: Pode ser habilitado para métodos EAPHost EAP que suportam a transmissão de TLVs (objetos de valor de comprimento de tipo).
ms.assetid: 298c89d9-7a6a-4280-9af9-77c7c00cab92
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 477ad8f2ee033b3f98f9cac0e7ee34d18dc62f00dd5bd7c0e09509ad32bcfa7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117904272"
---
# <a name="implementing-in-band-nap-support-for-eap-methods"></a>Implementando In-Band nap para métodos EAP

O suporte à NAP [(Proteção](/windows/desktop/NAP/network-access-protection-start-page) de Acesso à Rede) em banda para um método EAP pode ser habilitado para métodos EAPHost EAP que suportam a transmissão de TLVs (objetos de valor de comprimento de tipo). Quando o suporte a NAP na banda está habilitado, os pacotes NAP são transportados dentro de pacotes de método EAP.

Por outro lado, quando o suporte a [NAP](https://go.microsoft.com/fwlink/p/?linkid=83917) fora de banda está habilitado, a troca de SoH (Instrução NAP de saúde) ocorre por meio de meios diferentes dos pacotes de método EAP internos.

Todas as TLVs são específicas do fornecedor.

## <a name="implementing-nap-support-on-eap-peer-methods"></a>Implementando o suporte a NAP em métodos pares de EAP

A implementação do método par EAP recebe um TLV que contém a solicitação de SoH (Instrução de [Saúde)](https://go.microsoft.com/fwlink/p/?linkid=83917) TLV de um servidor EAP.

A implementação do método par EAP passa o TLV que contém a solicitação soH TLV para EAPHost da seguinte forma.

-   A implementação do método par EAP retorna o código de ação [**EapPeerMethodResponseActionRespond**](/windows/win32/api/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) para EAPHost no retorno [**de EapPeerProcessRequestPacket**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerprocessrequestpacket).
-   EAPHost chama [**EapPeerGetResponseAttributes da**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresponseattributes) implementação do método par EAP. Os atributos são passados no processo.
-   A implementação do método par EAP retorna o TLV que contém a solicitação soH TLV em [**EapPeerGetResponseAttributes**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresponseattributes). Os atributos são recebidos no processo.

A implementação do método par EAP recebe um TLV que contém um TLV SoH de EAPHost da seguinte forma.

-   EAPHost chama [**EapPeerSetResponseAttributes da**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetresponseattributes) implementação do método par EAP. **EapPeerSetResponseAttributes** contém um TLV que contém um SoH TLV.
-   A implementação do método par de EAP envia o TLV do SoH para o servidor EAP.
-   A implementação do método par EAP recebe um TLV que contém um TLV de resposta SoH do servidor EAP.

A implementação do método par EAP passa o TLV que contém a resposta SoH TLV para EAPHost da seguinte forma.

-   A implementação do método par EAP retorna o código de ação **EapPeerMethodResponseActionRespond** para EAPHost no retorno [**de EapPeerProcessRequestPacket**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerprocessrequestpacket).
-   EAPHost chama [**EapPeerGetResponseAttributes**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresponseattributes) das implementações de método par de EAP. A [**estrutura ATRIBUTOS \_ de EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attributes) é passada no processo.
-   A implementação do método par EAP retorna o TLV que contém a resposta SoH TLV em [**EapPeerSetResponseAttributes**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetresponseattributes).

> [!Note]  
> O membro **eapType** da estrutura [**EAP \_ ATTRIBUTE**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attribute) sempre será definido como **eatEAPTLV** e o membro **pValue** apontará para o primeiro byte do TLV que contém o TLV de resposta SoH.

 

### <a name="implementing-nap-support-on-eap-server-methods"></a>Implementando o suporte nap em métodos de servidor EAP

A implementação do método de servidor EAP constrói um TLV que contém um TLV de solicitação SoH. A implementação do método de servidor EAP envia esse TLV que contém o TLV de Solicitação SoH para o par de EAP. A implementação do método de servidor EAP recebe o TLV do par EAP.

A implementação do método de servidor EAP passa o TLV que contém um SoH TLV para EAPHost da seguinte forma.

-   A implementação do método de servidor EAP retorna o código de ação **EAP \_ METHOD \_ AUTHENTICATOR \_ RESPONSE \_ RESPOND** to EAPHost no retorno [**de EapMethodAuthenticatorReceivePacket**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorreceivepacket).
-   EAPHost chama [**EapMethodAuthenticatorGetAttributes da**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorgetattributes) implementação do método de servidor EAP.
-   A implementação do método de servidor EAP retorna o TLV que contém o SoH TLV [**em EapMethodAuthenticatorGetAttributes**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorgetattributes).

A implementação do método de servidor EAP recebe um TLV que contém um TLV de resposta SoH do EAPHost da seguinte forma.

-   EAPHost chama [**EapMethodAuthenticatorSetAttributes da**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorsetattributes) implementação do método de servidor EAP.
-   O TLV que contém a resposta SoH TLV é retornado [ **em EapMethodAuthenticatorSetAttributes**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorsetattributes)
-   A implementação do método de servidor EAP envia o TLV que contém a resposta SoH TLV.

> [!Note]  
> O membro **eapType** da estrutura [**EAP \_ ATTRIBUTE**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attribute) sempre será definido como **eatEAPTLV** e o membro **pValue** apontará para o primeiro byte do TLV que contém o TLV de resposta SoH.

 

### <a name="messages"></a>Mensagens

O EAP SoH TLV é usado para encapsular o protocolo SoH para transmissão por meio de um método EAP. Todos os TLVs de SoH de EAP têm a mesma estrutura, diferente apenas da ID da mensagem e da parte de dados da mensagem.

Para obter mais informações, consulte [Mensagens de SoH (Instrução de Health)](https://go.microsoft.com/fwlink/p/?linkid=83918)da NAP (Proteção de Acesso à Rede).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Configurando o método EAP Interface do Usuário](configuring-the-eap-method-user-interface.md)
</dt> <dt>

[Habilitando Política de Grupo](enabling-group-policy.md)
</dt> <dt>

[Implementando o suporte nap para métodos EAP](implementing-nap-for-eap-methods.md)
</dt> <dt>

[Transferindo dados entre os métodos Supplicant e EAP](transferring-data-between-the-supplicant-and-eap-methods.md)
</dt> <dt>

[EAPHost Supplicants](eaphost-supplicants.md)
</dt> </dl>

 

 