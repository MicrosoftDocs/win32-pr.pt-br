---
title: Transferindo dados entre os métodos Supplicant e EAP
description: Saiba mais sobre como transferir dados entre os métodos Supplicant e EAP. A transferência de dados entre métodos é realizada usando atributos EAP.
ms.assetid: f1bcff61-286a-4f18-8a5d-93d5d1fd2b5b
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca7675cac2c7e147804bc4c5ec86304e75063964bdc54cd44519fe535e28783f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118085647"
---
# <a name="transferring-data-between-the-supplicant-and-eap-methods"></a>Transferindo dados entre os métodos Supplicant e EAP

O uso de atributos EAP permite que os dados sejam trocados entre os supplicantes e os métodos de EAP.

## <a name="attribute-consumption"></a>Consumo de atributo

[**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession) consome atributos EAP que são passados diretamente para o método EAP configurado. Da mesma forma, os métodos EAP são livres para retornar um código de ação que indica ao suplicante que os atributos estão disponíveis e que ele deve coletar os atributos usando [**EapHostPeerGetResponseAttributes**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetresponseattributes).

Para obter mais informações, consulte estes tópicos.

-   [Códigos de ação suplicantes do](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction)par EAP .
-   [Códigos de razão suplicantes do](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeermethodresultreason)par EAP .
-   [Códigos de ação Authenticator método EAP](/windows/desktop/api/EapAuthenticatorActionDefine/ne-eapauthenticatoractiondefine-eap_method_authenticator_response_action).

Espera-se que os supplicantes ignorem os atributos que eles não reconhecem ou não podem agir. Usando [**EapHostPeerSetResponseAttributes,**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeersetresponseattributes) esses atributos ignorados são enviados de volta ao EAPHost e ao método EAP.

## <a name="vendor-specific-attributes"></a>Atributos específicos do fornecedor

Usando o atributo EAP específico do fornecedor, os métodos EAP e os supplicantes podem se envolver na troca de dados para uma finalidade específica. Atributos específicos do fornecedor são ignorados por supplicantes e métodos que não suportam o atributo específico do fornecedor.

Para obter mais informações, consulte estes tópicos.

-   [Atributos EAP](about-eap-attributes.md).
-   [**EAP \_ TIPO \_ DE ATRIBUTO**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_attribute_type).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Configurando o método EAP Interface do Usuário](configuring-the-eap-method-user-interface.md)
</dt> <dt>

[Habilitando Política de Grupo](enabling-group-policy.md)
</dt> <dt>

[Implementando In-Band nap para métodos EAP](enabling-in-band-nap-support.md)
</dt> <dt>

[Implementando o suporte nap para métodos EAP](implementing-nap-for-eap-methods.md)
</dt> <dt>

[EAPHost Supplicants](eaphost-supplicants.md)
</dt> </dl>

 

 




