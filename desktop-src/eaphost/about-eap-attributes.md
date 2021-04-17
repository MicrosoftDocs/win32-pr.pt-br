---
title: Atributos de EAP
description: É uma \_ estrutura de atributo EAP que contém um tipo predeterminado de dados relacionados a uma sessão de autenticação.
ms.assetid: 3c54cca2-cd3b-4149-bb0e-036d490cdd3b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5348ee300c0e4d07d6aaf110ba9074b1ac32c02a
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/18/2020
ms.locfileid: "105811994"
---
# <a name="eap-attributes"></a>Atributos de EAP

Um atributo EAP é uma estrutura de [**\_ atributo EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attribute) que contém um tipo predeterminado de dados relacionados a uma sessão de autenticação. Os atributos são usados para comunicar informações entre os métodos EAP e suplicantes ou entre métodos EAP e autenticadores. As implementações de ponto e autenticador de um método EAP podem trocar esses atributos por uma rede.

Uma lista completa dos tipos de atributo com suporte aparece no [**tópico \_ \_ tipo de atributo EAP**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_attribute_type).

## <a name="attributes-consumed-by-supplicants"></a>Atributos consumidos por suplicantes

Os seguintes tipos de atributo são consumidos por suplicantes 802.1 X.

-   **eatVendorSpecific**

Os seguintes tipos de atributo são consumidos por suplicantes de cliente PPP.

-   **eatMinimum**
-   **eatEAPTLV**

Os seguintes tipos de atributo são consumidos por suplicantes de servidor PPP.

-   **eatUserName**
-   **eatReplyMessage**
-   **eatState**
-   **eatSessionTimeout**
-   **eatEAPMessage**

## <a name="attributes-exported-by-methods"></a>Atributos exportados por métodos

Os seguintes tipos de atributo podem ser exportados por métodos EAP.

-   **eatClearTextPassword**
-   **eatQuarantineSoH**
-   **eatMethodId**

O tipo de atributo a seguir é exportado por métodos de TLS (EAP-TLS) de [nível de transporte](/previous-versions/windows/embedded/ms885336(v=msdn.10)) EAP.

-   **eatCertificateOID**

Os seguintes tipos de atributo são exportados pelos métodos [Microsoft Challenge Handshake Authentication Protocol versão 2,0](/previous-versions/windows/embedded/ms899190(v=msdn.10)) (MS-CHAPv2).

-   **eatUserName**
-   **eatCredentialsChanged**

O tipo de atributo a seguir é consumido pelo NPS (servidor de diretivas de rede).

-   **eatCertificateOID**

Os tipos de atributo a seguir são exportados por métodos [PEAP (Protected Extensible Authentication Protocol)](/previous-versions/windows/embedded/ms899190(v=msdn.10)) .

-   **eatUserName**
-   **eatPEAPEmbeddedEAPTypeId**
-   **eatPEAPFastRoamedSession**
-   **eatQuarantineSoH**

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**\_atributo EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attribute)
</dt> <dt>

[**\_tipo de atributo EAP \_**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_attribute_type)
</dt> </dl>

 

 