---
title: Estruturas IKE/AuthIP
description: Estruturas IKE/AuthIP
ms.assetid: 3267EA3C-FD1F-4ED1-9794-92551222EFE1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5de46cd72ec382dd360e6311930e946da3bf4189855adeaa49915b15ce3a9865
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069086"
---
# <a name="ikeauthip-structures"></a>Estruturas IKE/AuthIP

## <a name="in-this-section"></a>Nesta seção

-   [**\_METHOD0 de autenticação IKEEXT \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_authentication_method0)
-   [**\_METHOD1 de autenticação IKEEXT \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_authentication_method1)
-   [**\_METHOD2 de autenticação IKEEXT \_**](/windows/win32/api/iketypes/ns-iketypes-ikeext_authentication_method2)
-   [**\_EKUS0 do certificado IKEEXT \_**](/windows/win32/api/iketypes/ns-iketypes-ikeext_cert_ekus0)
-   [**\_NAME0 do certificado IKEEXT \_**](/windows/win32/api/iketypes/ns-iketypes-ikeext_cert_name0)
-   [**\_ \_ CONFIG0 raiz do certificado IKEEXT \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_cert_root_config0)
-   [**\_AUTHENTICATION0 do certificado IKEEXT \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_certificate_authentication0)
-   [**\_AUTHENTICATION1 do certificado IKEEXT \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_certificate_authentication1)
-   [**\_AUTHENTICATION2 do certificado IKEEXT \_**](/windows/win32/api/iketypes/ns-iketypes-ikeext_certificate_authentication2)
-   [**\_CREDENTIAL0 do certificado IKEEXT \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_certificate_credential0)
-   [**\_Credencial1 do certificado IKEEXT \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_certificate_credential1)
-   [**\_CRITERIA0 do certificado IKEEXT \_**](/windows/win32/api/iketypes/ns-iketypes-ikeext_certificate_criteria0)
-   [**\_ALGORITHM0 de codificação IKEEXT \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_cipher_algorithm0)
-   [**\_STATISTICS0 comum \_ IKEEXT**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_common_statistics0)
-   [**\_STATISTICS1 comum \_ IKEEXT**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_common_statistics1)
-   [**\_PAIR0 do cookie IKEEXT \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_cookie_pair0)
-   [**\_CREDENTIAL0 IKEEXT**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credential0)
-   [**\_CREDENCIAL1 IKEEXT**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credential1)
-   [**\_CREDENCIAL2 IKEEXT**](/windows/win32/api/iketypes/ns-iketypes-ikeext_credential2)
-   [**\_CREDENTIALS0 IKEEXT**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credentials0)
-   [**\_CREDENTIALS1 IKEEXT**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credentials1)
-   [**\_CREDENTIALS2 IKEEXT**](/windows/win32/api/iketypes/ns-iketypes-ikeext_credentials2)
-   [**\_PAIR0 credencial IKEEXT \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credential_pair0)
-   [**\_PAIR1 credencial IKEEXT \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credential_pair1)
-   [**\_PAIR2 credencial IKEEXT \_**](/windows/win32/api/iketypes/ns-iketypes-ikeext_credential_pair2)
-   [**\_AUTHENTICATION0 de EAP IKEEXT \_**](/windows/win32/api/iketypes/ns-iketypes-ikeext_eap_authentication0)
-   [**IKEEXT \_ em \_ POLICY0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_em_policy0)
-   [**IKEEXT \_ em \_ POLICY1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_em_policy1)
-   [**IKEEXT \_ em \_ POLICY2**](/windows/win32/api/iketypes/ns-iketypes-ikeext_em_policy2)
-   [**\_ALGORITHM0 de integridade IKEEXT \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_integrity_algorithm0)
-   [**\_STATISTICS0 de versão do IP IKEEXT \_ \_ específico \_ \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_ip_version_specific_common_statistics0)
-   [**\_STATISTICS1 de versão do IP IKEEXT \_ \_ específico \_ \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_ip_version_specific_common_statistics1)
-   [**STATISTICS0 de tipo específico da versão do \_ IP IKEEXT \_ \_ \_ \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_ip_version_specific_keymodule_statistics0)
-   [**STATISTICS1 de tipo específico da versão do \_ IP IKEEXT \_ \_ \_ \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_ip_version_specific_keymodule_statistics1)
-   [**\_AUTHENTICATION0 de \_ CGA \_ IPv6 IKEEXT**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_ipv6_cga_authentication0)
-   [**\_AUTHENTICATION0 Kerberos \_ IKEEXT**](/windows/win32/api/iketypes/ns-iketypes-ikeext_kerberos_authentication0)
-   [**\_AUTHENTICATION1 Kerberos \_ IKEEXT**](/windows/win32/api/iketypes/ns-iketypes-ikeext_kerberos_authentication1)
-   [**\_STATISTICS0 de KEYMODULE IKEEXT \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_keymodule_statistics0)
-   [**\_STATISTICS1 de KEYMODULE IKEEXT \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_keymodule_statistics1)
-   [**Nome do IKEEXT \_ \_ CREDENTIAL0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_name_credential0)
-   [**\_AUTHENTICATION0 de NTLM \_ v2 \_ de IKEEXT**](/windows/win32/api/iketypes/ns-iketypes-ikeext_ntlm_v2_authentication0)
-   [**\_POLICY0 IKEEXT**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_policy0)
-   [**IKEEXT \_ POLICY1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_policy1)
-   [**\_POLICY2 IKEEXT**](/windows/win32/api/iketypes/ns-iketypes-ikeext_policy2)
-   [**\_ \_ AUTHENTICATION0 de chave pré-compartilhada IKEEXT \_**](/windows/win32/api/iketypes/ns-iketypes-ikeext_preshared_key_authentication0)
-   [**\_ \_ AUTHENTICATION1 de chave pré-compartilhada IKEEXT \_**](/windows/win32/api/iketypes/ns-iketypes-ikeext_preshared_key_authentication1)
-   [**\_PROPOSAL0 IKEEXT**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_proposal0)
-   [**\_AUTHENTICATION0 reservado \_ IKEEXT**](/windows/win32/api/iketypes/ns-iketypes-ikeext_reserved_authentication0)
-   [**IKEEXT \_ SA \_ DETAILS0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_sa_details0)
-   [**IKEEXT \_ SA \_ DETAILS1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_sa_details1)
-   [**IKEEXT \_ SA \_ DETAILS2**](/windows/win32/api/iketypes/ns-iketypes-ikeext_sa_details2)
-   [**IKEEXT \_ SA \_ enum \_ TEMPLATE0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_sa_enum_template0)
-   [**\_STATISTICS0 IKEEXT**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_statistics0)
-   [**\_STATISTICS1 IKEEXT**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_statistics1)
-   [**\_TRAFFIC0 IKEEXT**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_traffic0)

 

 




