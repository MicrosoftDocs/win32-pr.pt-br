---
title: Atributos de EAP
description: É uma estrutura DE ATRIBUTO de EAP \_ que contém um tipo predeterminado de dados relacionados a uma sessão de autenticação.
ms.assetid: 3c54cca2-cd3b-4149-bb0e-036d490cdd3b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77898ccde0bbaf9660a7e4c3948cce9ec17d9e4f7773b0900333e7152520c013
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119117746"
---
# <a name="eap-attributes"></a>Atributos de EAP

Um atributo EAP é uma estrutura [**de \_ ATRIBUTO de EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attribute) que contém um tipo predeterminado de dados relacionados a uma sessão de autenticação. Os atributos são usados para comunicar informações entre métodos EAP e supplicantes ou entre métodos EAP e autenticadores. Implementações de par e autenticador de um método EAP podem trocar esses atributos por uma rede.

Uma lista completa dos tipos de atributo com suporte é exibida no tópico [**TIPO DE ATRIBUTO EAP \_ \_**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_attribute_type).

## <a name="attributes-consumed-by-supplicants"></a>Atributos consumidos por supplicants

Os tipos de atributo a seguir são consumidos por 802.1X supplicants.

-   **eatVendorSpecific**

Os seguintes tipos de atributo são consumidos por supplicantes de cliente PPP.

-   **eatMinimum**
-   **eatEAPTLV**

Os seguintes tipos de atributo são consumidos por supplicantes de servidor PPP.

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

O tipo de atributo a seguir é exportado pelos métodos [TLS (Transport Level Security)](/previous-versions/windows/embedded/ms885336(v=msdn.10)) (EAP-TLS).

-   **eatCertificateOID**

Os seguintes tipos de atributo são exportados pelos métodos MS-CHAPv2 (Protocolo de Autenticação de Handshake do Microsoft Challenge versão [2.0).](/previous-versions/windows/embedded/ms899190(v=msdn.10))

-   **eatUserName**
-   **eatCredentialsChanged**

O tipo de atributo a seguir é consumido pelo NPS (Servidor de Políticas de Rede).

-   **eatCertificateOID**

Os seguintes tipos de atributo são exportados por [métodos PEAP (Protocolo de](/previous-versions/windows/embedded/ms899190(v=msdn.10)) Autenticação Extensível Protegido).

-   **eatUserName**
-   **eatPEAPEmbeddedEAPTypeId**
-   **eatPEAPFastRoamedSession**
-   **eatQuarantineSoH**

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**ATRIBUTO \_ EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attribute)
</dt> <dt>

[**TIPO DE ATRIBUTO EAP \_ \_**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_attribute_type)
</dt> </dl>

 

 