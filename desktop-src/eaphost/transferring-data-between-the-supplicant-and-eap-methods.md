---
title: Transferindo dados entre os métodos suplicante e EAP
description: Saiba mais sobre como transferir dados entre os métodos suplicante e EAP. A transferência de dados entre métodos é realizada usando atributos de EAP.
ms.assetid: f1bcff61-286a-4f18-8a5d-93d5d1fd2b5b
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 187858347e8630bfbaba0683700eaa39f116f6ce
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104366723"
---
# <a name="transferring-data-between-the-supplicant-and-eap-methods"></a>Transferindo dados entre os métodos suplicante e EAP

O uso de atributos de EAP permite que os dados sejam trocados entre suplicantes e métodos EAP.

## <a name="attribute-consumption"></a>Consumo de atributo

O [**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession) CONSOME atributos EAP que são passados diretamente para o método EAP configurado. Da mesma forma, os métodos EAP são livres para retornar um código de ação que indica ao suplicante que os atributos estão disponíveis e que ele deve coletar os atributos usando [**EapHostPeerGetResponseAttributes**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetresponseattributes).

Para obter mais informações, consulte os tópicos a seguir.

-   [Códigos de ação suplicante de peer EAP](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction).
-   [Códigos de motivo suplicante de peer EAP](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeermethodresultreason).
-   [Códigos de ação do método de autenticador EAP](/windows/desktop/api/EapAuthenticatorActionDefine/ne-eapauthenticatoractiondefine-eap_method_authenticator_response_action).

Os suplicantes são esperados para ignorar atributos que não reconhecem ou que não podem agir. Usando [**EapHostPeerSetResponseAttributes**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeersetresponseattributes) esses atributos ignorados são enviados de volta para o EAPHost e o método EAP.

## <a name="vendor-specific-attributes"></a>Atributos específicos do fornecedor

Usando o atributo EAP específico do fornecedor, os métodos EAP e os suplicantes podem se envolver na troca de dados para uma finalidade específica. Atributos específicos do fornecedor são ignorados por suplicantes e métodos que não dão suporte ao atributo específico do fornecedor.

Para obter mais informações, consulte os tópicos a seguir.

-   [Atributos EAP](about-eap-attributes.md).
-   [**EAP \_ \_tipo de atributo**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_attribute_type).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Configurando a interface do usuário do método EAP](configuring-the-eap-method-user-interface.md)
</dt> <dt>

[Habilitando Política de Grupo](enabling-group-policy.md)
</dt> <dt>

[Implementando o suporte do In-Band NAP para métodos EAP](enabling-in-band-nap-support.md)
</dt> <dt>

[Implementando o suporte a NAP para métodos EAP](implementing-nap-for-eap-methods.md)
</dt> <dt>

[Suplicantes do EAPHost](eaphost-supplicants.md)
</dt> </dl>

 

 




